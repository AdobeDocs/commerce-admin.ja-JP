---
title: デザイン設定
description: デザイン設定を使用すると、単一ページに設定を表示することで、デザイン関連のルールと設定設定を簡単に編集できます。
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
TQID: https://experienceleague.adobe.com/6sccsrSWuaF6BkKqngQq3JH2GerWxfybWd5aXcs0gIc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 0%

---

# デザイン設定

デザイン設定を使用すると、単一ページに設定を表示することで、デザイン関連のルールと設定設定を簡単に編集できます。

![&#x200B; デザイン設定ページ &#x200B;](./assets/configuration.png){width="700" zoomable="yes"}

## デザイン設定の変更

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 設定するストアビューを見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

   このページには、ストアビューの現在のデザイン設定が表示されます。

1. デフォルトのテーマを変更するには、**[!UICONTROL Applied Theme]**&#x200B;をビューに適用するテーマに設定します。

   テーマを指定しない場合は、システムのデフォルトのテーマが使用されます。 一部のサードパーティの拡張機能は、システムのデフォルトのテーマを変更します。

1. [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} テーマを特定のデバイスにのみ使用する場合は、**[!UICONTROL User Agent Rules]**&#x200B;を設定します。

   ![User-Agent ルール &#x200B;](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   テーマを指定するデバイスタイプごとに：

   - **[!UICONTROL Add New User Agent Rule]**&#x200B;をクリックします。

   - **[!UICONTROL Search String]**&#x200B;に、特定のデバイスのブラウザーIDを入力します。

     検索文字列は、正規表現またはPerl互換性のある正規表現（PCRE）のいずれかです（詳細は[User Agent](https://en.wikipedia.org/wiki/User_agent)を参照）。 次の検索文字列はFirefoxを識別します：

         /^mozilla/i
     
   - **[!UICONTROL Theme Name]**&#x200B;で、指定したデバイスに使用するテーマを選択します。

   >[!NOTE]
   >
   >指定するデバイスに対して、いくつでもルールを追加できます。 検索文字列は、入力された順序で一致します。

1. _[!UICONTROL Other Settings]_&#x200B;で、各セクションを展開し、リンクされたトピックの指示に従って、必要に応じて設定を編集します。

   - [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} [[!UICONTROL Header]](page-setup.md#header)
   - [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} [[!UICONTROL Footer]](page-setup.md#footer)
   - [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![&#x200B; デザインに影響するその他の設定](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Configuration]**&#x200B;をクリックします。
