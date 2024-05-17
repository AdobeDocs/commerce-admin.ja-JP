---
title: '[!UICONTROL Services] &gt; [!UICONTROL Magento Web API]'
description: の設定を確認します。 [!UICONTROL Services] &gt; [!UICONTROL Magento Web API] コマース管理者のページ。
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP 設定](./assets/web-api-soap-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | ストア表示 | デフォルトの文字セットを決定します。 空の場合は UTF-8 が使用されます。 |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![GraphQl 入力制限](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | ストア表示 | GraphQL呼び出しに対して入力制限が有効かどうかを判断します。 既定値： `No`. |
| [!UICONTROL Maximum Page Size] | ストア表示 | GraphQL応答でページ分割された検索結果に許可される最大項目数を設定します。 このオプションは、次の場合は使用できません _入力制限を有効にする_ = `No`. |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Web Api 入力制限](./assets/web-api-input-limits.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | ストア表示 | Web API 呼び出しに対する入力制限が有効かどうかを判断します。 既定値： `No`. |
| 入力リストの制限 | ストア表示 | Web API リクエストのエンティティ配列プロパティで許可される最大項目数を設定します。 このオプションは、次の場合は使用できません _入力制限を有効にする_ = `No`. |
| [!UICONTROL Maximum Page Size] | ストア表示 | Web API 応答でページ分割された検索結果に許可される最大項目数を設定します。 このオプションは、次の場合は使用できません _入力制限を有効にする_ = `No`. |
| [!UICONTROL Default Page Size] | ストア表示 | Web API 応答でページ分割された検索結果のデフォルトの項目数を設定します。 |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Web API セキュリティ](./assets/web-api-security.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | グローバル | ゲストが、SOAP と REST API の両方から CMS、カタログおよびストアリソースに匿名でアクセスできるかどうかを決定します。 デフォルトでは、匿名ゲストアクセスは許可されていません。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![JWT 認証](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | グローバル | JWT （JSON web トークン）暗号化に使用する JWS または JWE アルゴリズムのタイプを指定します |
| [!UICONTROL Content encryption algorithm for JWEs] | グローバル | JWE アルゴリズムが選択されている場合に、JWT 暗号化に使用するコンテンツ暗号化アルゴリズムのタイプを指定します。 JWS アルゴリズムの場合、このオプションは無視されます。 |
| [!UICONTROL Customer JWT Expires In] | グローバル | 顧客の JWT ベアラートークンが期限切れになるまでの時間（分）を設定します。 顧客 JWT ベアラートークンは、このフィールドが空または負の値の場合、30 分で有効期限が切れます。 デフォルト値 `60` |
| [!UICONTROL Admin User JWT Expires In] | グローバル | 管理者 JWT ベアラートークンが期限切れになるまでの時間（分）を設定します。 このフィールドが空か負の値の場合、管理 JWT ベアラートークンは 30 分で有効期限が切れます。 デフォルト値 `60` |

{style="table-layout:auto"}
