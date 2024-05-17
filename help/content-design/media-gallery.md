---
title: この [!DNL Media Gallery]
description: メディア ギャラリーを使用して、サーバー上のメディア ファイルを整理および管理します。
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# この [!DNL Media Gallery]

Adobe CommerceまたはMagento Open Source 2.4 では、マーチャントは新しいを使用できます _enhanced_ [!DNL Media Gallery] サーバー上のメディアファイルを整理および管理します。 この新しい [!DNL Media Gallery] 既存のメディアストレージと同じ機能を持ちますが、ユーザーインターフェイスが改善され、との統合が強化されています。 [Adobe Stock][adobe-stock].

![Media Gallery グリッドに表示される画像](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>に追加された製品画像 [_[!UICONTROL Images and Videos]_製品セクション](../catalog/product-image.md#upload-an-image) が管理していない [!DNL Media Gallery]. で使用される画像のみ_[!UICONTROL Content]_ 製品セクションのフィールドが表示され、新しいフィールドでフィルタリングされる [!DNL Media Gallery].

## 新しいの有効化 [!DNL Media Gallery]

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![詳細設定 –  [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enable Old Media Gallery]** 対象： `No`.

1. クリック **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、 **[!UICONTROL Cache Management]** システムメッセージ内のリンクをクリックし、無効なキャッシュを更新します。

   この [[!UICONTROL Content] メニュー](/help/content-design/content-menu.md) に新しいが表示されるようになりました。 _[!UICONTROL Media Gallery]_オプション。

>[!NOTE]
>
>新規製品の全機能 [!DNL Media Gallery] が必要 `media.gallery.synchronization` および `media.content.synchronization` 初期同期のために開始されるキューコンシューマー。 参照： [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) が含まれる _設定ガイド_ を参照してください。

## 新しいにアクセス [!DNL Media Gallery]

新しい [!DNL Media Gallery] は、コンテンツ メニューから、または次の場合にアクセスできます [ページの追加または編集](/help/content-design/page-add.md). また、次の場合にもアクセスできます [カテゴリの作成または編集](/help/catalog/category-create.md)または次の場合 [コンテンツエディターを使用した画像の挿入](/help/content-design/editor-insert-image.md).

新しいにアクセスするには [!UICONTROL Media Gallery] 経由 [!UICONTROL Content] メニュー：

- 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

ページの追加または編集中に新しいメディアギャラリーにアクセスするには：

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. クリック **[!UICONTROL Add a New Page]**.

   既存のページを編集する場合は、 _[!UICONTROL Action]_クリックする列&#x200B;**[!UICONTROL Select]**を選択します&#x200B;**[!UICONTROL Edit]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** を選択し、次の操作を実行します。

   - 以下がある場合： [ページビルダー有効](../page-builder/setup.md)を展開します **[!UICONTROL Media]** パネルを開いてドラッグ **[!UICONTROL Image]** ターゲットコンテナへのプレースホルダー。 次に、 **[!UICONTROL Select from Gallery]**.

     ![画像をステージにドラッグ](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - 次のような場合： [WYSIWYG エディター有効](/help/content-design/editor.md)を選択し、 **[!UICONTROL Show/Hide Editor]** 次に、をクリックします **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] デモ

について詳しくは、 [!DNL Media Gallery]次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

