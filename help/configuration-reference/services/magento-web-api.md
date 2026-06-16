---
title: '[!UICONTROL Services] > [!UICONTROL Magento Web API]'
description: Commerce管理者の[!UICONTROL Services] > [!UICONTROL Magento Web API] ページで設定を確認します。
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP設定](./assets/web-api-soap-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | ストアビュー | デフォルトの文字セットを指定します。 空の場合は、UTF-8が使用されます。 |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![GraphQl入力制限](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | ストアビュー | GraphQL呼び出しに対して入力制限が有効かどうかを指定します。 デフォルト値：`No`。 |
| [!UICONTROL Maximum Page Size] | ストアビュー | GraphQL レスポンスでページ分割された検索結果で許可される最大項目数を設定します。 このオプションは、_入力制限を有効にする_ = `No`の場合は使用できません。 |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Web Api入力制限](./assets/web-api-input-limits.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | ストアビュー | Web API呼び出しに対して入力制限が有効かどうかを指定します。 デフォルト値：`No`。 |
| 入力リストの制限 | ストアビュー | Web API リクエストのエンティティ配列プロパティで許可されるアイテムの最大数を設定します。 このオプションは、_入力制限を有効にする_ = `No`の場合は使用できません。 |
| [!UICONTROL Maximum Page Size] | ストアビュー | Web API応答でページ分割された検索結果で許可される項目の最大数を設定します。 このオプションは、_入力制限を有効にする_ = `No`の場合は使用できません。 |
| [!UICONTROL Default Page Size] | ストアビュー | Web API応答のページ分割された検索結果のデフォルトの項目数を設定します。 |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Web API セキュリティ &#x200B;](./assets/web-api-security.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | グローバル | ゲストは、SOAPとREST APIの両方からCMS、カタログ、およびストアリソースに匿名でアクセスできます。 デフォルトでは、匿名ゲストアクセスは許可されていません。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![JWT認証](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | グローバル | JWT （JSON Web Token）暗号化に使用するJWS アルゴリズムまたはJWE アルゴリズムのタイプを指定します |
| [!UICONTROL Content encryption algorithm for JWEs] | グローバル | JWE アルゴリズムが選択されている場合に、JWT暗号化に使用するコンテンツ暗号化アルゴリズムのタイプを指定します。 このオプションは、JWS アルゴリズムでは無視されます。 |
| [!UICONTROL Customer JWT Expires In] | グローバル | 顧客JWT ベアラートークンの有効期限が切れるまでの時間（分単位）を設定します。 顧客JWT ベアラートークンは、このフィールドが空の場合、または負の値を持つ場合、30分で期限切れになります。 デフォルト値：`60` |
| [!UICONTROL Admin User JWT Expires In] | グローバル | Admin JWT ベアラートークンの有効期限が切れるまでの時間（分単位）を設定します。 admin JWT ベアラートークンは、このフィールドが空の場合、または負の値を持つ場合、30分で期限切れになります。 デフォルト値：`60` |

{style="table-layout:auto"}
