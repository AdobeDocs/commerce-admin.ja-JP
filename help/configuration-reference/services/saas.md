---
title: '[!UICONTROL Services] > [!UICONTROL Commerce Services Connector]'
description: Commerce管理者の[!UICONTROL Services] > [!UICONTROL Commerce Services Connector] ページで設定を確認します。
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: 0020db425032254fb7661701533d1e700d98260c
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

ストアをAdobe Commerce サービスに接続する方法については、[Commerce サービス &#x200B;](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html?lang=ja)を参照してください。

{{config}}

## [!UICONTROL Sandbox API Keys]

![&#x200B; サンドボックス API キー](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | グローバル | 作成者とその使用権限を識別するAPI キー（存在する場合）。 |
| [!UICONTROL Sandbox private API key] | グローバル | API キーに関連付けられた秘密鍵。 |

{style="table-layout:auto"}

## [!UICONTROL Production Keys]

![実稼動API キー](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Production public API key] | グローバル | 作成者とその使用権限を識別するAPI キー（存在する場合）。 |
| [!UICONTROL Production private API key] | グローバル | API キーに関連付けられた秘密鍵。 |

{style="table-layout:auto"}

## [!UICONTROL SaaS Identifier]

![SaaS識別子](./assets/saas-identifier.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Project] | グローバル | すべてのSaaS データスペースをグループ化するSaaS プロジェクトの名前。 SaaS プロジェクトが存在しない場合、「_プロジェクトを作成_」ボタンが表示されます。 |
| [!UICONTROL Data Space] | グローバル | 指定したSaaS プロジェクト内のSaaS データスペースを一覧表示します。 SaaS データスペースの数は、[Commerce ライセンス &#x200B;](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html?lang=ja):<br />Adobe Commerce - 1つの実稼動データスペース、2つのテスト データスペース、<br />Magento Open Source - 1つの実稼動データスペース、テスト データスペースなしによって異なります |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![IMS組織](./assets/ims-organization.png)<!-- zoom -->

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | Adobe IDは、通常、メンバーシップを開始したとき、またはAdobe アプリケーションやサービスを購入したときに最初に使用したメールアドレスです。 Adobe IDは、Adobe アカウントにアクセスするために必要なキーです。 |

{style="table-layout:auto"}
