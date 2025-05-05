---
title: '[!DNL Inventory Management] CLI リファレンス'
description: 'インベントリデータと設定を管理するためにモジュールが提供するコマンドについて説明します  [!DNL Inventory Management] '
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI リファレンス

[!DNL Inventory Management] には、インベントリ データと構成設定を管理するためのコマンドが用意されています。

次のコマンドがあります。

- 販売可能数量に影響する予約不整合の確認および解決
- 距離優先アルゴリズムのジオコードの追加

## 予約の不整合の解決

予約では、1 在庫あたりの製品 SKU に対して販売可能な数量が保留されます。 注文の出荷、追加、キャンセルまたは払い戻しを行うと、報酬予約が入力されて、保留の設定または解除が行われます。

[!DNL Inventory Management] には、予約の不整合を確認および解決するための 2 つのコマンドが用意されています。

- [&#39;inventory:reservation:list-inconsistencies&#39;](#list-inconsistencies-command)
- [&#39;inventory:reservation:create-compensations&#39;](#create-compensations-command)

### 予約の不整合の原因

[!DNL Inventory Management] は、主要イベントの予約を生成します。

- 注文の発注（初期予約）
- 受注出荷（報酬予約）
- 受注の払戻またはクレジット・メモの発行（報酬予約）
- オーダー取消（報酬予約）

予約の不整合は、次の場合に発生する可能性があります。

- [!DNL Inventory Management] は最初の予約を失い、過剰な予約報酬を入力します（過剰報酬が発生し、金額に一貫性がなくなります）
- [!DNL Inventory Management] は最初の予約を正しく配置しますが、補償予約を失います。

`inventory_reservation` テーブルの予約を手動で確認および確認できます。

次の設定とイベントが原因で、予約に不整合が生じる場合があります。

- **注文が最終状態（完了、キャンセル、クローズ）ではない 2.3.x にアップグレードします。** [!DNL Inventory Management] は、これらの受注に対する補償予約を作成しますが、入庫したり、販売可能数量から控除される初期予約を持つことはありません。 2.1.x または 2.2.x からAdobe CommerceまたはMagento Open Source v2.3.x にアップグレードした後に、これらのコマンドを使用することをお勧めします。 保留中の受注がある場合、受注および受注の履行に対する販売可能数量および予約が正しく更新されます。
- **在庫を管理せず、後でこの設定を変更します。** 設定で **[!UICONTROL Manage Stock]** を `No` に設定して、2.3.x の使用を開始できます。 [!DNL Commerce] では、注文および出荷イベントに予約を配置しません。 後で **[!UICONTROL Manage Stock]** 設定を有効にして、一部の注文を作成した場合、その注文を処理して履行すると、販売可能数量が破損し、報酬予約が発生します。
- **注文が web サイトに送信される間、web サイトの在庫を再割り当てします**。 初期在庫の初期予約入力と、新規在庫のすべての報酬予約入力
- **すべての予約の合計が `0` に解決されない場合があります。** 最終状態（完了、取消、クローズ）の受注の範囲内にある全予約は `0` に解決され、すべての販売可能数量保留が消去されます。

### List inconsistencies コマンド

`list-inconsistencies` コマンドは、すべての予約の不整合を検出して一覧表示します。 コマンドオプションを使用して、完了した注文や不完全な注文のみ、またはすべてを確認します。

```bash
bin/magento inventory:reservation:list-inconsistencies
```

コマンドオプション：

- `-c`, `--complete-orders` – 完了した注文の不整合を返します。 完了済みの注文について、誤った予約が引き続き保留になる場合があります。
- `-i`, `--incomplete-orders` – 未完了の注文（部分的に出荷済み、未出荷）の不整合を返します。 誤った予約は、注文に対して十分な売り上げ可能な数量を保持しない場合があります。
- `-b`, `--bunch-size` – 一度に読み込む注文の数を定義します。
- `-r`、`--raw` – 未加工の出力。

`-r` を使用した応答は、次の形式で返 `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` れます。

- 注文 ID は、不整合の範囲を示します。
- SKU は、一貫性のない製品を示します。
- 「数量」には、予約報酬に入力する金額が設定されます。
- 在庫 ID は、在庫の範囲を定義します。これは、引当を使用して販売可能数量を計算します。

例：

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

問題が見つからない場合は、次のメッセージが返されます。注文の不一致は見つかりませんでした。

### 「報酬の作成」コマンド

`create-compensations` コマンドは、報酬予約を作成します。 問題に応じて、販売可能数量の保留を設定または解除するために、新規予約が作成されます。

予約を作成するには、`172:bike-123:+2.000000:1` などの形式 `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` を使用して補償を提供します。

```bash
bin/magento inventory:reservation:create-compensations
```

コマンド オプション：

- `-r`, `--raw` – 生の出力を返します。

リクエストの形式が正しくない場合は、次のメッセージが表示されます。

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

コマンドで予約が作成されると、SKU、注文、在庫ごとの更新を示すメッセージが表示されます。

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

報酬エントリの SKU にスペースが含まれる場合は、SKU を引用符で囲みます。

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### 不整合の検出と補正の作成

不整合を検出し、パイプを使用して `list-inconsistencies` と `create-compensations` の両方を実行することで、すぐに補正を作成できます。 `-r` コマンドオプションを使用して、生データを生成し、`create-compensations` に送信します。

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

応答の例：

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

更新が完了したら、list コマンドを実行して確認します。

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

コマンドをパイプ処理して、不整合を検出し、未完了（`-i`）または完了（`-c`）の注文のみの補正を作成することもできます。

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## ジオコードの読み込み

[!DNL Inventory Management] には、注文の全品または一部を配送するための最適なオプションを決定するのに役立つ [ 距離優先アルゴリズム ](distance-priority-algorithm.md) が用意されています。 アルゴリズムは、GPS 情報またはジオコードを使用して、注文の各品目のソース（倉庫または他の物理的な場所）と配送先住所との間の距離を計算します。 これらの結果に基づいて、アルゴリズムは、各項目を順番に出荷するためにどのソースを使用するかを推奨します。

マーチャントは、距離の計算に必要な GPS またはジオコードデータのプロバイダーを選択します。

- **Google マップ** は、[Google マップ Platform](https://mapsplatform.google.com/) サービスを使用して、配送先住所と配送元住所との間の距離と時間を計算します。 このオプションにはGoogle請求プランが必要で、Google経由で料金が発生する場合があります。

- **オフライン計算** [geonames.org](https://www.geonames.org/) からダウンロードしてコマンドでCommerceに読み込んだデータを使用して距離を計算します。 このオプションは無料です。

ジオコードをオフライン計算用にインポートするには：

次のコマンドを、スペースで区切られた [ISO-3166 alpha2 国コード ](https://www.geonames.org/countries/) のリストを使用して入力します。

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

例：

```bash
bin/magento inventory-geonames:import us ca gb de
```

システムがジオコードデータをダウンロードしてデータベースに読み込み、メッセージ `Importing <country code>: OK` が表示されます。
