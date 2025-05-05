---
title: '[!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector]'
description: Commerce Admin の [!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector] ページで設定を確認します。
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 0020db425032254fb7661701533d1e700d98260c
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

ストアをAdobe Commerce サービスに接続する方法については、[Commerce サービス ](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html?lang=ja) を参照してください。

{{config}}

## [!UICONTROL Sandbox API Keys]

![ サンドボックス API キー ](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | グローバル | 作成者とその使用権限を識別する API キー（存在する場合）。 |
| [!UICONTROL Sandbox private API key] | グローバル | API キーに関連付けられた秘密鍵。 |

{style="table-layout:auto"}

## [!UICONTROL Production Keys]

![ 実稼動 API キー ](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Production public API key] | グローバル | 作成者とその使用権限を識別する API キー（存在する場合）。 |
| [!UICONTROL Production private API key] | グローバル | API キーに関連付けられた秘密鍵。 |

{style="table-layout:auto"}

## [!UICONTROL SaaS Identifier]

![SaaS 識別子 ](./assets/saas-identifier.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Project] | グローバル | すべての SaaS データ スペースをグループ化する SaaS プロジェクトの名前。 SaaS プロジェクトが存在しない場合は、「_プロジェクトを作成_」ボタンが表示されます。 |
| [!UICONTROL Data Space] | グローバル | 指定した SaaS プロジェクトの SaaS データ スペースを一覧表示します。 SaaS データスペースの数は、[Commerce ライセンスによって異なります ](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html?lang=ja):<br />Adobe Commerce - 1 つの実稼動データスペース；2 つのテスト用データスペース；<br />Magento Open Source - 1 つの実稼動データスペース；テスト用データスペース |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![IMS 組織 ](./assets/ims-organization.png)<!-- zoom -->

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | Adobe IDは通常、メンバーシップを開始したとき、またはAdobe アプリケーションやサービスを購入したときに最初に使用したメールアドレスです。 Adobe IDは、Adobe アカウントにアクセスするために必要なキーです。 |

{style="table-layout:auto"}
