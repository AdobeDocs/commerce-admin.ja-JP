---
title: 顧客データ属性リファレンス
description: 顧客データの読み込みと書き出しを操作する場合は、この顧客データ属性の参照を使用します。
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
TQID: https://experienceleague.adobe.com/-s4plXYkrsdNTL-xxMj41AAxtJJ5q1PKiBUcdnaWhlg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 483
ht-degree: 0%

---

# 顧客データ属性リファレンス

次の表に、顧客のメインファイルと顧客アドレスの一般的な書き出しからの属性を示します。 このデータの書き出しに使用されたインストールには、サンプルデータがインストールされた2つのweb サイトと複数のストアビューがあります。

各属性（フィールド）はCSV ファイルで列として表され、顧客レコードは行で表されます。 アンダースコアで始まる列は、プロパティまたは複雑なデータを含むサービスエンティティです。

## 顧客のメインファイル

| 属性 | 説明 |
|--- |--- |
| `email` | 顧客のメールアドレス。 |
| `_website` |  |
| `_store` |  |
| `confirmation` | 確認フラグ。 |
| `created_at` | 顧客アカウントの作成日。 |
| `created_in` | アカウントが作成されたストアビュー。 |
| `disable_auto_group_change` | VAT ID検証中に顧客グループを動的に割り当てることができるかどうかを指定します。 |
| `dob` | 顧客の生年月日。 <br><br>**_Important:_**&#x200B;現在のセキュリティとプライバシーのベストプラクティスに従って、お客様の生年月日（月、日、年）の保存と処理を確認してください。 他の個人識別子（_氏名_&#x200B;など）と共に収集すると、法的およびセキュリティ上のリスクが生じる可能性があります。 お客様の生年月日の保存を制限し、代わりに、お客様の生年月日を代替手段として使用することをお勧めします。 |
| `firstname` | 顧客の名前。 |
| `gender` | 顧客の性別： |
| `group_id` | 顧客が割り当てられている顧客グループのID。 |
| `lastname` | 顧客の姓。 |
| `middlename` | 顧客のミドルネームまたはミドルイニシャル。 |
| `password_hash` | パスワードハッシュ |
| `prefix` | 顧客名で使用されている接頭辞（`Mr.`、`Ms.`、`Mrs.`、`Dr.`など）。 |
| `rp_token` | パスワードトークンをリセットします。 |
| `rp_token_created_at` | パスワードがリセットされた日付。 |
| `store_id` | ストア ID |
| `suffix` | 顧客名で使用されるすべてのサフィックス（`Jr.`、`Sr.`、`Esquire`など）。 |
| `taxvat` |  |
| `website_id` | 顧客アカウントが作成されたサイトのweb サイト ID。 |
| `password` | お客様のパスワード。 |

{style="table-layout:auto"}

## 顧客の住所

| 属性 | 説明 |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | お客様の住所がある都市。 |
| `company` | この住所に該当する場合は、会社名。 |
| `country_id` | お客様の住所がある国のID。 |
| `fax` | 顧客のFAX番号（該当する場合）。 |
| `firstname` | 顧客の名前（名）。 |
| `lastname` | 顧客の姓。 |
| `middlename` | 顧客のミドルネームまたはミドルイニシャル。 |
| `postcode` | 顧客の住所がある郵便番号。 |
| `prefix` | 顧客名で使用されている接頭辞（`Mr.`、`Ms.`、`Mrs.`、`Dr.`など）。 |
| `region` | お客様の住所がある地域。 |
| `region_id` | 地域ID |
| `street` | 顧客の住所。 設定で指定されている場合は、住所の2行目を使用できます。 |
| `suffix` | 使用する場合、お客様の名前に関連付けられているサフィックス（`Jr.`、`Sr.`、または`III`など）。 |
| `telephone` | 住所に関連付けられている顧客の電話番号。 |
| `vat_id` | VAT IDは、VAT検証で使用される場合の顧客のVAT番号の内部識別子です。 |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | デフォルトの請求先住所を指定します。 値`1`は、アドレスが顧客のデフォルトの請求先住所であることを示します。 値：1 / 0 |
| `_address_default_shipping_` | デフォルトの配送先住所を指定します。 値`1`は、アドレスが顧客のデフォルトの配送先住所であることを示します。 値：`1` / `0` |

{style="table-layout:auto"}
