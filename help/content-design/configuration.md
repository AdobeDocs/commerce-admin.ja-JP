---
title: デザイン設定
description: デザイン設定を使用すると、設定を単一のページに表示することで、デザイン関連のルールや設定を簡単に編集できます。
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# デザイン設定

デザイン設定を使用すると、設定を単一のページに表示することで、デザイン関連のルールや設定を簡単に編集できます。

![デザイン設定ページ](./assets/configuration.png){width="700" zoomable="yes"}

## デザイン設定の変更

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 設定するストア表示を見つけ、 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

   このページには、ストアビューの現在のデザイン設定が表示されます。

1. デフォルトのテーマを変更するには、 **[!UICONTROL Applied Theme]** を、ビューに適用するテーマに追加します。

   テーマが指定されていない場合は、システムのデフォルトのテーマが使用されます。 一部のサードパーティの拡張機能は、システムのデフォルトテーマを変更します。

1. テーマを特定のデバイスにのみ使用する場合は、 **[!UICONTROL User Agent Rules]**.

   ![ユーザーエージェントルール](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   テーマを指定する各デバイスタイプに対して、次の操作を実行します。

   - クリック **[!UICONTROL Add New User Agent Rule]**.

   - の場合 **[!UICONTROL Search String]**」に、特定のデバイスのブラウザー ID を入力します。

     検索文字列は、通常の式または Perl 互換正規表現 (PCRE) を指定できます ( [ユーザーエージェント](https://en.wikipedia.org/wiki/User_agent) を参照 )。 次の検索文字列は Firefox を識別します。

         /^mozilla/i
     
   - の場合 **[!UICONTROL Theme Name]**、指定したデバイスに使用するテーマを選択します。

   >[!NOTE]
   >
   >指定するデバイスに対して追加できるルールの数に制限はありません。 検索文字列は、入力された順序で一致します。

1. の下 _[!UICONTROL Other Settings]_で、各セクションを展開し、リンクされたトピックの手順に従って、必要に応じて設定を編集します。

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![デザインに影響を与えるその他の設定](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Configuration]**.
