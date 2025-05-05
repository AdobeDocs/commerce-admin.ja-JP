---
title: Media Gallery 画像の最適化
description: メディアアセットに画像の最適化を使用する方法  [!DNL Commerce]  説明します。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Media Gallery 画像の最適化

新しい [Media Gallery](media-gallery.md) には、パフォーマンスを向上させストアフロントのメディアファイルのサイズを縮小する _画像の最適化_ 機能が用意されています。 この最適化はデフォルトで有効になっており、ストアの設定で変更できます。

## 画像の最適化の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. ![ 拡張セレクター ](../assets/icon-display-expand.png) を展開し **[!UICONTROL Media Gallery Image Optimization]** 以下を実行します。

   - **[!UICONTROL Enable Image Optimization]** を `Yes` に設定します。
   - 必要に応じて **[!UICONTROL Maximum Width]** と **[!UICONTROL Maximum Height]** の値（ピクセル単位）を入力します。

## 動作

Media Gallery の画像最適化機能が有効になっている場合、画像の最適化されたコピーが、元のファイルではなく [Media Gallery](media-gallery.md) のコンテンツに自動的に挿入されます。

設定で _最大幅_ と _最大高さ_ の値を変更すると、以前に挿入された既存の最適化画像がすべて更新されます。

Media Gallery の画像の最適化を使用するには、構成が変更されたときに最適化された画像を再生成するために、`media.gallery.renditions.update` キューコンシューマーが実行されている必要があります。 詳しくは [ 設定ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) の _メッセージキューの管理_ を参照してください。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
