---
title: メディアギャラリー画像の最適化
description: 画像の最適化を [!DNL Commerce] メディアアセット。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# メディアギャラリー画像の最適化

新しい [メディアギャラリー](media-gallery.md) を指定します。 _画像最適化_ 機能を使用すると、パフォーマンスが向上し、ストアフロント上のメディアファイルのサイズが小さくなります。 この最適化はデフォルトで有効になっており、ストア設定で変更できます。

## 画像の最適化を設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** 次の操作を実行します。

   - 設定 **[!UICONTROL Enable Image Optimization]** から `Yes`.
   - 次を入力します。 **[!UICONTROL Maximum Width]** および **[!UICONTROL Maximum Height]** の値（ピクセル単位）を指定します。

## 動作

メディアギャラリーの画像最適化機能を有効にすると、最適化された画像のコピーが [メディアギャラリー](media-gallery.md) 元のファイルの代わりに。

次の場合に _最大幅_ および _最大の高さ_ の値が設定内で変更されると、以前に挿入された既存の最適化済み画像がすべて更新されます。

メディアギャラリーの画像の最適化では、 `media.gallery.renditions.update` キューコンシューマーは、設定が変更されたときに最適化された画像を再生成するために実行中です。 詳しくは、 [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) （内） _設定ガイド_ を参照してください。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
