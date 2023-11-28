---
title: The [!DNL Media Gallery]
description: メディアギャラリーを使用して、サーバー上のメディアファイルを整理および管理します。
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# The [!DNL Media Gallery]

Adobe CommerceまたはMagento Open Source2.4 では、マーチャントは新しい _強化_ [!DNL Media Gallery] を使用して、サーバー上のメディアファイルを整理および管理します。 この新しい [!DNL Media Gallery] には、既存のメディアストレージと同じ機能が含まれますが、ユーザーインターフェイスの改善と [Adobe Stock][adobe-stock].

![メディアギャラリーグリッドに表示される画像](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>製品画像が [_[!UICONTROL Images and Videos]_製品セクション](../catalog/product-image.md#upload-an-image) は、 [!DNL Media Gallery]. で使用される画像のみ_[!UICONTROL Content]_ 新しい [!DNL Media Gallery].

## 新しい [!DNL Media Gallery]

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![詳細設定 — [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable Old Media Gallery]** から `No`.

1. クリック **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、 **[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

   The [[!UICONTROL Content] メニュー](/help/content-design/content-menu.md) 新しい _[!UICONTROL Media Gallery]_オプション。

>[!NOTE]
>
>新機能の完全な提供 [!DNL Media Gallery] が必要です `media.gallery.synchronization` および `media.content.synchronization` 最初の同期用に開始するコンシューマーをキューに入れます。 詳しくは、 [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) （内） _設定ガイド_ を参照してください。

## 新しい [!DNL Media Gallery]

新しい [!DNL Media Gallery] は、コンテンツメニューから、または [ページを追加または編集](/help/content-design/page-add.md). また、 [カテゴリの作成または編集](/help/catalog/category-create.md)、または [コンテンツエディターを使用して画像を挿入する](/help/content-design/editor-insert-image.md).

新しい [!UICONTROL Media Gallery] から [!UICONTROL Content] メニュー：

- 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

ページの追加または編集時に新しいメディアギャラリーにアクセスするには：

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. クリック **[!UICONTROL Add a New Page]**.

   既存のページを編集する場合は、 _[!UICONTROL Action]_列をクリック&#x200B;**[!UICONTROL Select]**を選択します。**[!UICONTROL Edit]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 」セクションで次の操作を実行します。

   - 次の条件を満たしている場合： [Page Builder が有効](../page-builder/setup.md)、を展開します。 **[!UICONTROL Media]** パネルとドラッグ **[!UICONTROL Image]** プレースホルダーをターゲットコンテナに追加します。 次に、「 **[!UICONTROL Select from Gallery]**.

     ![画像をステージにドラッグ](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - 次の条件を満たす [WYSIWYG エディタが有効](/help/content-design/editor.md)をクリックし、 **[!UICONTROL Show/Hide Editor]** 次に、「 **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] デモ

詳しくは、 [!DNL Media Gallery]、このビデオを見る：

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

