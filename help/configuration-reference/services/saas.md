---
title: '[!UICONTROL Services] > [!UICONTROL Commerce Services Connector]'
description: Commerce管理者の[!UICONTROL Services] > [!UICONTROL Commerce Services Connector] ページで設定を確認します。
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/50XCqY8JMjvf9G-wcHLxvlskSd5noIAB0LIX6xMarL0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 238
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

ストアをAdobe Commerce サービスに接続する方法については、[Commerce サービス &#x200B;](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html)を参照してください。

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
| [!UICONTROL Data Space] | グローバル | 指定したSaaS プロジェクト内のSaaS データスペースを一覧表示します。 SaaS データスペースの数は、[Commerce ライセンス &#x200B;](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html):<br />Adobe Commerce - 1つの実稼動データスペース、2つのテスト データスペース、<br />Magento Open Source - 1つの実稼動データスペース、テスト データスペースなしによって異なります |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![IMS組織](./assets/ims-organization.png)<!-- zoom -->

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | Adobe IDは、通常、メンバーシップを開始したとき、またはAdobe アプリケーションやサービスを購入したときに最初に使用したメールアドレスです。 Adobe IDは、Adobe アカウントにアクセスするために必要なキーです。 |

{style="table-layout:auto"}
