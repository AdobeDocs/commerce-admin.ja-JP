---
title: '''[!DNL Inventory Management] CLI リファレンス'
description: が提供するコマンドについて説明します [!DNL Inventory Management] インベントリ データと構成設定を管理するモジュール。
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI リファレンス

[!DNL Inventory Management] インベントリ データと構成設定を管理するコマンドを提供します。

次のコマンドがあります。

- 販売可能数量に影響する予約不整合の確認および解決
- 距離優先アルゴリズムのジオコードの追加

## 予約の不整合の解決

予約では、1 在庫あたりの製品 SKU に対して販売可能な数量が保留されます。 注文の出荷、追加、キャンセルまたは払い戻しを行うと、報酬予約が入力されて、保留の設定または解除が行われます。

[!DNL Inventory Management] には、予約の不整合を確認および解決するための 2 つのコマンドが用意されています。

- [&#39;在庫:reservation:list-inconsistencies&#39;](#list-inconsistencies-command)
- [&#39;在庫:reservation:create-compensations&#39;](#create-compensations-command)

### 予約の不整合の原因

[!DNL Inventory Management] 主要イベントの予約を生成します。

- 注文の発注（初期予約）
- 受注出荷（報酬予約）
- 受注の払戻またはクレジット・メモの発行（報酬予約）
- オーダー取消（報酬予約）

予約の不整合は、次の場合に発生する可能性があります。

- [!DNL Inventory Management] 最初の予約を失い、過剰な予約報酬を入力します（過剰補償および金額の不一致につながります）
- [!DNL Inventory Management] 最初の予約を正しく配置しますが、補償予約は失われます。

で手動で予約を確認および確認できます。 `inventory_reservation` テーブル。

次の設定とイベントが原因で、予約に不整合が生じる場合があります。

- **注文が最終状態（完了、キャンセル、クローズ）ではない 2.3.x にアップグレードします。** [!DNL Inventory Management] これらの受注に対して補償予約が作成されますが、初期予約は入力されず、または販売可能数量から控除されます。 2.1.x または 2.2.x からAdobe CommerceまたはMagento Open Source v2.3.x にアップグレードした後に、これらのコマンドを使用することをお勧めします。 保留中の受注がある場合、受注および受注の履行に対する販売可能数量および予約が正しく更新されます。
- **在庫を管理せず、後でこの設定を変更します。** で 2.3.x の使用を開始できます **[!UICONTROL Manage Stock]** をに設定 `No` 設定で指定します。 [!DNL Commerce] は、注文配置および出荷イベントで予約を配置しません。 後で有効にする場合 **[!UICONTROL Manage Stock]** 設定と一部の注文が作成されると、その注文を処理して履行する際に、販売可能数量が報酬予約で破損します。
- **Web サイトの在庫を再割り当てし、注文をその web サイトに送信する**. 初期在庫の初期予約入力と、新規在庫のすべての報酬予約入力
- **すべての予約の合計は、次の目的では解決されない場合があります `0`.** 最終状態（完了、キャンセル、クローズ）の注文の範囲内のすべての予約は、次のように解決されます `0`すべての販売可能な数量保留をクリアします。

### List inconsistencies コマンド

この `list-inconsistencies` コマンドは、すべての予約の不整合を検出して一覧表示します。 コマンドオプションを使用して、完了した注文や不完全な注文のみ、またはすべてを確認します。

```bash
bin/magento inventory:reservation:list-inconsistencies
```

コマンドオプション：

- `-c`, `--complete-orders`  – 完了した注文の不整合を返します。 完了済みの注文について、誤った予約が引き続き保留になる場合があります。
- `-i`, `--incomplete-orders`  – 未完了の注文（部分的に出荷された注文、未出荷の注文）の不整合を返します。 誤った予約は、注文に対して十分な売り上げ可能な数量を保持しない場合があります。
- `-b`, `--bunch-size`  – 一度に読み込む注文の数を定義します。
- `-r`, `--raw`  – 生の出力。

を使用した回答 `-r` 再来訪 `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` 形式：

- 注文 ID は、不整合の範囲を示します。
- SKU は、一貫性のない製品を示します。
- 「数量」には、予約報酬に入力する金額が設定されます。
- 在庫 ID は、在庫の範囲を定義します。これは、引当を使用して販売可能数量を計算します。

例：

```terminal
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```terminal
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

問題が見つからない場合は、次のメッセージが返されます。注文の不一致は見つかりませんでした。

### 「報酬の作成」コマンド

この `create-compensations` コマンドは報酬予約を作成します。 問題に応じて、販売可能数量の保留を設定または解除するために、新規予約が作成されます。

予約を作成するには、形式を使用して報酬を指定します `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` 例： `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

コマンド オプション：

- `-r`, `--raw`  – 生の出力を返します。

リクエストの形式が正しくない場合は、次のメッセージが表示されます。

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

コマンドで予約が作成されると、SKU、注文、在庫ごとの更新を示すメッセージが表示されます。

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

報酬エントリの SKU にスペースが含まれる場合は、SKU を引用符で囲みます。

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### 不整合の検出と補正の作成

不整合を検出し、パイプを使用して両方を実行することで、すぐに補正を作成できます `list-inconsistencies` および `create-compensations`. の使用 `-r` 生データを生成して送信するコマンドオプション `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

応答の例：

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```terminal
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

更新が完了したら、list コマンドを実行して確認します。

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

パイプを使用してコマンドの不整合を検出し、不完全な場合にのみ補正を作成することもできます（`-i`）または complete （`-c`）注文です。

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## ジオコードの読み込み

[!DNL Inventory Management] は、 [距離優先アルゴリズム](distance-priority-algorithm.md)（注文の全品または一部を発送するための最適なオプションを決定するのに役立ちます）。 アルゴリズムは、GPS 情報またはジオコードを使用して、注文の各品目のソース（倉庫または他の物理的な場所）と配送先住所との間の距離を計算します。 これらの結果に基づいて、アルゴリズムは、各項目を順番に出荷するためにどのソースを使用するかを推奨します。

マーチャントは、距離の計算に必要な GPS またはジオコードデータのプロバイダーを選択します。

- **Googleの地図** 使用 [Google マッププラットフォーム](https://mapsplatform.google.com/) 配送先住所と配送元場所の間の距離と時間を計算するサービス。 このオプションにはGoogle請求プランが必要で、Google経由で料金が発生する場合があります。

- **オフライン計算** からダウンロードされたデータを使用して距離を計算します [geonames.org](https://www.geonames.org/) コマンドを使用してCommerceに読み込まれます。 このオプションは無料です。

ジオコードをオフライン計算用にインポートするには：

次のコマンドを、スペース区切りリストを使用して入力します。 [ISO-3166 alpha2 国コード](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

例：

```bash
bin/magento inventory-geonames:import us ca gb de
```

システムがジオコードデータをダウンロードしてデータベースに読み込み、メッセージが表示されます  `Importing <country code>: OK`.
