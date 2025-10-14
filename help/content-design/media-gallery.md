---
title: ' [!DNL Media Gallery]'
description: メディア ギャラリーを使用して、サーバー上のメディア ファイルを整理および管理します。
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# [!DNL Media Gallery]

Adobe CommerceまたはMagento Open Source 2.4 では、マーチャントは新しい _enhanced_ [!DNL Media Gallery] を使用して、サーバー上のメディアファイルを整理および管理できます。 この新しい [!DNL Media Gallery] には、既存のメディアストレージと同じ機能が含まれていますが、ユーザーインターフェイスが改善され、[Adobe Stock][adobe-stock] との統合が強化されています。

![&#x200B; メディアギャラリーグリッドに表示される画像 &#x200B;](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>[_[!UICONTROL Images and Videos]_&#x200B;製品セクションに追加された製品画像は &#x200B;](../catalog/product-image.md#upload-an-image) [!DNL Media Gallery] ーザーによって管理されません。_[!UICONTROL Content]_ 製品セクションのフィールドで使用される画像のみが、新しい [!DNL Media Gallery] に表示され、フィルタリングされます。

## 新しい [!DNL Media Gallery] を有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]** を展開します。

   ![&#x200B; 詳細設定 – [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Old Media Gallery]** を `No` に設定します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

1. プロンプトが表示されたら、システムメッセージの **[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

   [[!UICONTROL Content] メニューに &#x200B;](/help/content-design/content-menu.md) 新しい _[!UICONTROL Media Gallery]_&#x200B;オプションが表示されるようになりました。

>[!NOTE]
>
>新しい [!DNL Media Gallery] の完全な機能を使用するには、初期同期のために `media.gallery.synchronization` および `media.content.synchronization` キューコンシューマーを開始する必要があります。 詳しくは [&#x200B; 設定ガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=ja) の _メッセージキューの管理_ を参照してください。

## 新しい [!DNL Media Gallery] へのアクセス

新しい [!DNL Media Gallery] ージには、コンテンツメニューからアクセスするか、[&#x200B; ページを追加または編集 &#x200B;](/help/content-design/page-add.md) するときにアクセスできます。 [&#x200B; カテゴリを作成または編集する &#x200B;](/help/catalog/category-create.md) 場合、または [&#x200B; コンテンツ エディタを使用して画像を挿入する &#x200B;](/help/content-design/editor-insert-image.md) 場合にも、この機能にアクセスできます。

[!UICONTROL Content] メニューから新しい [!UICONTROL Media Gallery] にアクセスするには：

- _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Media]_/**[!UICONTROL Media Gallery]**&#x200B;に移動します。

ページの追加または編集中に新しいメディアギャラリーにアクセスするには：

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Pages]**&#x200B;に移動します。

1. 「**[!UICONTROL Add a New Page]**」をクリックします。

   既存のページを編集する場合は、「_[!UICONTROL Action]_」列を使用して「**[!UICONTROL Select]**」をクリックし、**[!UICONTROL Edit]**&#x200B;を選択します。

1. **[!UICONTROL Content]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - [&#x200B; ページビルダーを有効 &#x200B;](../page-builder/setup.md) にしている場合は、**[!UICONTROL Media]** パネルを展開し、**[!UICONTROL Image]** プレースホルダーをターゲットコンテナにドラッグします。 次に、「**[!UICONTROL Select from Gallery]**」をクリックします。

     ![&#x200B; 画像をステージにドラッグ &#x200B;](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - [WYSIWYG Editor を有効にしている場合は &#x200B;](/help/content-design/editor.md) [**[!UICONTROL Show/Hide Editor]**]、[**[!UICONTROL Insert Image]**] の順にクリックします。

## [!DNL Media Gallery] デモ

[!DNL Media Gallery] について詳しくは、次のビデオを参照してください。

>[!VIDEO](https://video.tv.adobe.com/v/3411046?quality=12&learn=on&captions=jpn)

[adobe-stock]: https://stock.adobe.com

