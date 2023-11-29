---
title: '[!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector]'
description: 次のページで設定を確認します： [!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector] コマース管理のページ。
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

ストアをAdobe Commerceサービスに接続する方法については、 [コマースサービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html).

{{config}}

## [!UICONTROL Sandbox API Keys]

![サンドボックス API キー](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | グローバル | 作成者とその権限（存在する場合）を識別する API キー。 |
| [!UICONTROL Sandbox private API key] | グローバル | API キーに関連付けられた秘密鍵。 |

{style="table-layout:auto"}

## [!UICONTROL Production Keys]

![実稼動 API キー](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Production public API key] | グローバル | 作成者とその権限（存在する場合）を識別する API キー。 |
| [!UICONTROL Production private API key] | グローバル | API キーに関連付けられた秘密鍵。 |

{style="table-layout:auto"}

## [!UICONTROL SaaS Identifier]

![SaaS 識別子](./assets/saas-identifier.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Project] | グローバル | すべての SaaS データスペースをグループ化する SaaS プロジェクトの名前。 A _プロジェクトを作成_ ボタンが表示されます。 |
| [!UICONTROL Data Space] | グローバル | 指定した SaaS プロジェクトの SaaS データスペースを一覧表示します。 SaaS データスペースの数は、 [コマースライセンス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html):<br />Adobe Commerce - 1 つの実稼動データ領域、2 つのテストデータ領域<br />Magento Open Source:1 つの実稼動データ領域。テスト用のデータ領域なし |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![IMS 組織](./assets/ims-organization.png)<!-- zoom -->

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | 通常、Adobe IDは、メンバーシップを開始したとき、またはAdobeのアプリやサービスを購入したときに最初に使用した電子メールアドレスです。 Adobe IDは、Adobeアカウントにアクセスするために必要なキーです。 |

{style="table-layout:auto"}
