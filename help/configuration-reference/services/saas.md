---
title: '[!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector]'
description: の設定を確認します。 [!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector] コマース管理者のページ。
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

ストアをAdobe Commerce サービスに接続する方法については、以下を参照してください。 [Commerce サービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html).

{{config}}

## [!UICONTROL Sandbox API Keys]

![サンドボックス API キー](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | グローバル | 作成者とその使用権限を識別する API キー（存在する場合）。 |
| [!UICONTROL Sandbox private API key] | グローバル | API キーに関連付けられた秘密鍵。 |

{style="table-layout:auto"}

## [!UICONTROL Production Keys]

![実稼動 API キー](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Production public API key] | グローバル | 作成者とその使用権限を識別する API キー（存在する場合）。 |
| [!UICONTROL Production private API key] | グローバル | API キーに関連付けられた秘密鍵。 |

{style="table-layout:auto"}

## [!UICONTROL SaaS Identifier]

![SaaS 識別子](./assets/saas-identifier.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Project] | グローバル | すべての SaaS データ スペースをグループ化する SaaS プロジェクトの名前。 A _プロジェクトを作成_ saaS プロジェクトが存在しない場合は、ボタンが表示されます。 |
| [!UICONTROL Data Space] | グローバル | 指定した SaaS プロジェクトの SaaS データ スペースを一覧表示します。 SaaS データ領域の数は、 [Commerce ライセンス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html):<br />Adobe Commerce - 1 つの実稼動データスペース、2 つのテストデータスペース、<br />Magento Open Source - 1 つの実稼動データスペースで、テスト用のデータスペースはない |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![IMS 組織](./assets/ims-organization.png)<!-- zoom -->

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | Adobe IDは通常、メンバーシップを開始したとき、またはAdobeアプリやサービスを購入したときに最初に使用したメールアドレスです。 Adobe IDは、Adobeアカウントにアクセスするために必要なキーです。 |

{style="table-layout:auto"}
