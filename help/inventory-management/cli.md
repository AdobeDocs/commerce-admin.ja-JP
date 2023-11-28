---
title: '''[!DNL Inventory Management] CLI リファレンス`'
description: が提供するコマンドの詳細 [!DNL Inventory Management] 在庫データと構成設定を管理するモジュールです。
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI リファレンス

[!DNL Inventory Management] には、インベントリデータと構成設定を管理するコマンドが用意されています。

次のコマンドが含まれます。

- 販売可能数量に影響する予約の不整合の確認と解決
- 距離優先度アルゴリズムのジオコードの追加

## 予約の不整合を解決

予約では、在庫ごとの製品 SKU に対して販売可能数量の保留を設定します。 出荷時、製品の追加、取消、または受注の返金時に、報酬予約が入力され、これらの保留を設定または解除します。

[!DNL Inventory Management] には、予約の不整合を確認して解決する 2 つのコマンドが用意されています。

- [&#39;在庫:reservation:list-unconsices&#39;](#list-inconsistencies-command)
- [&#39;在庫:reservation:create-compensations&#39;](#create-compensations-command)

### 予約の不整合の原因

[!DNL Inventory Management] はキーイベントの予約を生成します。

- 注文の配置（最初の予約）
- 注文出荷（報酬の予約）
- 払い戻し命令またはクレジットメモ（報酬の予約）を発行
- 注文のキャンセル（報酬の予約）

予約の不整合は、次の場合に発生する可能性があります。

- [!DNL Inventory Management] 最初の予約を失い、多くの予約報酬を受け入れ過ぎる（過補償で、不整合な量につながる）
- [!DNL Inventory Management] は最初の予約を正しく配置しますが、代償的な予約を失います。

予約の確認は、 `inventory_reservation` 表。

次の設定とイベントは、予約に不整合が生じる可能性があります。

- **2.3.x にアップグレードし、注文が最終状態にならない（完了、キャンセル、クローズ済み）ようにします。** [!DNL Inventory Management] これらの注文に対して報酬引当を作成しますが、販売可能数量から差し引かれる初期引当に入るか、または当初予約を持っていません。 2.1.x または 2.2.x からAdobe CommerceまたはMagento Open Sourcev2.3.x にアップグレードした後に、これらのコマンドを使用することをお勧めします。 保留中の注文がある場合、コマンドは、販売および注文の受け渡しに対する販売可能数量と予約を正しく更新します。
- **後でこの設定を変更した後は、在庫を管理しません。** 2.3.x の使用は、 **[!UICONTROL Manage Stock]** に設定 `No` を設定に含めます。 [!DNL Commerce] は、注文の配置および出荷イベントに予約を配置しません。 後で **[!UICONTROL Manage Stock]** 設定と一部の注文が作成された場合、その注文を処理して満たすと、報酬予約で販売可能数量が破損します。
- **注文が Web サイトに送信される間に、Web サイトの在庫を再割り当てする**. 初期予約が初期在庫に入り、すべての報酬予約が新しい在庫に入ります。
- **全ての予約の合計が～に解決しないかもしれない `0`.** 最終状態（完了、キャンセル、クローズ）の注文の範囲内のすべての予約は、 `0`、すべての売上可能数量の保留をクリアします。

### リストの不整合コマンド

The `list-inconsistencies` コマンドは、すべての予約の不整合を検出してリストします。 完了または不完全な注文のみ、またはすべてを確認するには、コマンドオプションを使用します。

```bash
bin/magento inventory:reservation:list-inconsistencies
```

コマンドオプション：

- `-c`, `--complete-orders`  — 完了した注文に対して不整合を戻します。 完了した注文に対して、誤った予約が保留中の可能性があります。
- `-i`, `--incomplete-orders`  — 不完全な注文（一部出荷済、未出荷）に対して矛盾を戻します。 予約が正しくない場合は、注文の販売可能数量が多すぎるか、不十分な可能性があります。
- `-b`, `--bunch-size`  — 一度に読み込む注文の数を定義します。
- `-r`, `--raw`  — 生の出力。

次を使用した応答： `-r` 戻る `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` 形式：

- 注文 ID は不一致の範囲を示します。
- SKU は不整合がある商品を示します。
- 「数量」は、予約報酬に入力する金額を設定します。
- 在庫 ID は在庫の範囲を定義し、予約を使用して販売可能数量を計算します。

例:

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

問題が見つからない場合は、次のメッセージが返されます。順序の不整合は見つかりませんでした。

### 補正コマンドを作成

The `create-compensations` コマンドは補正の予約を作成します。 問題に応じて、新しい予約が作成され、販売可能数量の保留が解除されます。

予約を作成するには、フォーマットを使用して報酬を提供します `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` 例： `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

コマンドオプション：

- `-r`, `--raw`  — 生の出力を戻します。

リクエストの形式が正しくない場合、次のメッセージが表示されます。

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

コマンドが予約を作成すると、SKU、注文、在庫別の更新を示すメッセージが表示されます。

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

報酬エントリの SKU にスペースが含まれる場合は、SKU を引用符で囲みます。

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### 不整合を検出し、報酬を作成する

矛盾を検出し、パイプを使用して両方の `list-inconsistencies` および `create-compensations`. 以下を使用します。 `-r` 生データを生成して次に送信するコマンドオプション `create-compensations`.

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

更新が完了したら、list コマンドを実行して次を確認します。

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

コマンドをパイプ処理して不整合を検出し、不完全な (`-i`) または完了 (`-c`) 注文件数。

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## ジオコードを読み込む

[!DNL Inventory Management] には、 [距離優先度のアルゴリズム](distance-priority-algorithm.md)：完全な注文または一部の注文を発送する最適なオプションを決定するのに役立ちます。 アルゴリズムは、GPS 情報またはジオコードを使用して、注文内の各品目のソース（倉庫または他の物理的な位置）と配送先住所との間の距離を計算します。 これらの結果に基づいて、アルゴリズムは、どのソースを使用して各品目を注文で出荷するかを推奨します。

マーチャントは、距離の計算に必要な GPS またはジオコードデータのプロバイダーを選択します。

- **Google MAP** uses [Google Maps Platform](https://mapsplatform.google.com/) 配送先住所と発送元の場所の間の距離と時間を計算するサービス。 このオプションを使用するにはGoogle課金プランが必要で、Googleを通じて料金が発生する場合があります。

- **オフライン計算** からダウンロードしたデータを使用して距離を計算します。 [geonames.org](https://www.geonames.org/) コマンドを使用してコマースに読み込まれました。 このオプションは無料です。

オフライン計算用にジオコードを読み込むには、次の手順に従います。

次のコマンドをスペースで区切って入力します。 [ISO-3166 alpha2 国コード](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

例：

```bash
bin/magento inventory-geonames:import us ca gb de
```

システムは、ジオコードデータをデータベースにダウンロードおよび読み込んでから、メッセージを表示します  `Importing <country code>: OK`.
