---
title: '[!DNL Inventory Management] CLI リファレンス'
description: 在庫データと構成設定を管理するために [!DNL Inventory Management]  モジュールが提供するコマンドについて説明します。
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/jdlLgwIe50ExZ2giXBiGf5cG8L4DQDZe4psbB16F5JE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 858
ht-degree: 0%

---

# [!DNL Inventory Management] CLI リファレンス

[!DNL Inventory Management]には、インベントリ データと構成設定を管理するコマンドが用意されています。

これらのコマンドには、次のものが含まれます。

- 販売可能な数量に影響する予約不整合のチェックと解決
- 距離優先アルゴリズムにジオコードを追加する

## 予約の不整合の解決

予約により、商品SKUの販売可能な数量ホールドを在庫ごとに配置できます。 商品の発送、追加、キャンセル、または注文の返金を行う場合、補償の予約は、これらの保留を配置またはクリアするために入力されます。

[!DNL Inventory Management]には、予約の不整合を確認して解決するための2つのコマンドが用意されています。

- [`inventory:reservation:list-inconsistencies`](#list-inconsistencies-command)
- [`inventory:reservation:create-compensations`](#create-compensations-command)

### 予約の不整合の原因

[!DNL Inventory Management]がキーイベントの予約を生成します：

- 注文手続き（初回予約）
- 注文発送（補償予約）
- 注文の返金またはクレジットメモの発行（補償予約）
- 注文取り消し（補償予約）

予約の不整合は、次の場合に発生する可能性があります。

- [!DNL Inventory Management]は最初の予約を失い、予約報酬が多すぎます（過剰補償と金額の一貫性の低下）
- [!DNL Inventory Management]は最初の予約を正しく配置しますが、補償予約は失われます。

`inventory_reservation` テーブルの予約を手動で確認および確認できます。

次の設定とイベントは、予約の不整合を引き起こす可能性があります。

- **注文が最終状態（完了、キャンセル済み、またはクローズ済み）でない場合は、2.3.xにアップグレードします。** [!DNL Inventory Management]は、これらの注文に対する補償引当を作成しますが、販売可能な数量から差し引かれる初期引当は入力せず、または持っていません。 2.1.xまたは2.2.xからAdobe CommerceまたはMagento Open Source v2.3.xにアップグレードした後に、これらのコマンドを使用することをお勧めします。 保留中の注文がある場合、コマンドは販売可能な数量と販売注文と注文フルフィルメントの予約を正しく更新します。
- **在庫を管理していないため、後でこの構成を変更します。** 設定で&#x200B;**[!UICONTROL Manage Stock]**&#x200B;が`No`に設定された2.3.xを使用できます。 [!DNL Commerce]は、注文の配置イベントおよび出荷イベントで予約を行っていません。 後で&#x200B;**[!UICONTROL Manage Stock]**&#x200B;設定を有効にし、一部の注文が作成された場合、その注文を処理してフルフィルメントを行うと、販売可能数量は報酬引当金で破損します。
- **注文がWeb サイトに送信されている間、Web サイトのStockを再割り当てしました**。 初期引当が初期在庫に入力され、すべての補償引当が新規在庫に入力されます。
- **すべての予約の合計が`0`に解決されない可能性があります。** 最終状態（完了、キャンセル済み、クローズ）の注文の範囲にあるすべての予約は、`0`に解決され、すべての販売可能な数量の保留がクリアされます。

### List inconsistencies コマンド

`list-inconsistencies` コマンドは、すべての予約の不整合を検出して一覧表示します。 コマンドオプションを使用して、完了または不完全な注文のみを確認するか、またはすべてを確認します。

```bash
bin/magento inventory:reservation:list-inconsistencies
```

コマンドオプション：

- `-c`、`--complete-orders` – 完了した注文の不整合を返します。 完了した注文に対して、誤った予約が引き続き保留中である可能性があります。
- `-i`、`--incomplete-orders` – 不完全な注文（一部出荷、未出荷）に対して不整合を返します。 誤った予約は、注文に対して販売可能な数量が多すぎるか、または十分でない可能性があります。
- `-b`、`--bunch-size` – 一度に読み込む注文数を定義します。
- `-r`、`--raw` – 生の出力。

`-r`を使用した回答は、`<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`形式で返されます：

- 注文IDは、不整合の範囲を示します。
- SKUは、製品に一貫性がないことを示します。
- 「数量」では、予約報酬に入力する金額を設定します。
- Stock IDは、在庫の範囲を定義し、予約を使用して販売可能な数量を計算します。

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

問題が見つからない場合、このメッセージは「注文の不整合は見つかりませんでした」を返します。

### 「補償を作成」コマンド

`create-compensations` コマンドは、補償予約を作成します。 問題に応じて、新しい予約を作成して、販売可能な数量を保留またはリリースします。

予約を作成するには、`172:bike-123:+2.000000:1`などの形式`<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`を使用して補償を提供します。

```bash
bin/magento inventory:reservation:create-compensations
```

コマンドオプション：

- `-r`, `--raw` – 生の出力を返します。

リクエストの形式が正しくない場合は、次のメッセージが表示されます。

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

コマンドが予約を作成すると、SKU、注文、在庫ごとに更新を示すメッセージが表示されます。

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

補償エントリのSKUにスペースが含まれる場合は、SKUを引用符で囲みます。

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### 不整合を検出し、補償を提供

パイプを使用して`list-inconsistencies`と`create-compensations`の両方を実行することで、矛盾を検出し、すぐに補償を作成できます。 生データを生成して`create-compensations`に送信するには、`-r` コマンド オプションを使用します。

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

更新が完了したら、list コマンドを実行して次のことを確認します。

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

コマンドをパイプ処理して不整合を検出し、不完全（`-i`）または完了（`-c`）の注文に対してのみ補償を作成することもできます。

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## ジオコードの読み込み

[!DNL Inventory Management]には[距離優先アルゴリズム &#x200B;](distance-priority-algorithm.md)が用意されており、完全または部分的な注文を出荷するための最適なオプションを決定するのに役立ちます。 このアルゴリズムは、GPS情報またはジオコードを使用して、注文の各商品のソース（倉庫またはその他の物理的な場所）と配送先住所との間の距離を計算します。 これらの結果にもとづいて、アルゴリズムは、各商品を発注するために使用するソースを推奨します。

加盟店は、距離の計算に必要なGPSまたはジオコードデータのプロバイダーを選択します。

- **Google MAP**&#x200B;では、[Google Maps Platform](https://mapsplatform.google.com/) サービスを使用して、配送先住所と送信元の場所の間の距離と時間を計算します。 このオプションにはGoogleの請求計画が必要であり、Googleを通じて請求が発生する場合があります。

- **オフライン計算**&#x200B;は、[geonames.org](https://www.geonames.org/)からダウンロードし、コマンドを使用してCommerceに読み込んだデータを使用して、距離を計算します。 このオプションは無料です。

オフライン計算用にジオコードをインポートするには：

次のコマンドを入力します。スペース区切りのリストは[ISO-3166 alpha2 country codes](https://www.geonames.org/countries/)です。

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

例：

```bash
bin/magento inventory-geonames:import us ca gb de
```

ジオコードデータをダウンロードしてデータベースに読み込み、メッセージ `Importing <country code>: OK`を表示します。
