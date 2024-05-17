---
title: Media Gallery 画像の最適化
description: 画像の最適化をユーザーに適用する方法を説明します [!DNL Commerce] メディアアセット。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Media Gallery 画像の最適化

新しい [メディアギャラリー](media-gallery.md) 次を提供 _画像の最適化_ パフォーマンスを向上させ、ストアフロントのメディアファイルのサイズを縮小する機能。 この最適化はデフォルトで有効になっており、ストアの設定で変更できます。

## 画像の最適化の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** 次の手順を実行します。

   - を設定 **[!UICONTROL Enable Image Optimization]** 対象： `Yes`.
   - を入力 **[!UICONTROL Maximum Width]** および **[!UICONTROL Maximum Height]** 必要に応じて値（ピクセル単位）を指定します。

## 動作

Media Gallery の画像最適化機能が有効になっている場合、画像の最適化されたコピーがのコンテンツに自動的に挿入されます [メディアギャラリー](media-gallery.md) 元のファイルの代わりに使用します。

いつ _最大の幅_ および _最大高さ_ 設定で値が変更され、以前に挿入された既存の最適化画像がすべて更新されます。

Media Gallery の画像の最適化では、 `media.gallery.renditions.update` 設定が変更されると、キューコンシューマーは最適化された画像を再生成するために実行されます。 参照： [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) が含まれる _設定ガイド_ を参照してください。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
