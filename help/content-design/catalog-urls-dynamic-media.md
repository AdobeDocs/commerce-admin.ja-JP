---
title: ダイナミックメディアの URL
description: 画像または他のメディアアセットへの相対参照としての Dynamic Media URL の使用について説明します。
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# ダイナミックメディアの URL

Dynamic Media の URL は、画像または他のメディアアセットへの相対参照です。 有効にすると、Dynamic Media URL を使用して、サーバー上のアセットや、 [コンテンツ配信ネットワーク](media-storage-content-delivery-network.md). Dynamic Media URL の使用は、カタログのパフォーマンスに影響を与える可能性があり、 [編集者](editor.md#configure-the-editor) は、静的または dynamic media URL のいずれかを使用するように設定できます。

すべてと同様 [マークアップタグ](../systems/markup-tags.md)を指定する場合、ディレクティブは二重中括弧で囲みます。 Dynamic Media URL の形式は、次のようになります。

`\{\{media url="path/to/image.jpg"}}`

ページがストアフロントにレンダリングされる際に、動的 URL ディレクティブが保存されたHTMLコンテンツから処理されます。 ページがレンダリングされるたびに、コンテンツがスキャンされて `\{\{media url="..."}}` と各ディレクティブは、対応するメディア URL に置き換えられます。

{{$include /help/_includes/directives-caution.md}}

## 静的メディア URL の設定

デフォルトでは、WYSIWYG エディターからカタログに挿入される画像には、相対的な動的 URL が含まれます。 静的 URL を使用したい場合は、設定を変更できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Content Management]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL WYSIWYG Options]** 」セクションに入力します。

   ![WYSIWYG オプション](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** を次のいずれかに変更します。

   - `Yes` - WYSIWYG エディターで挿入されるメディアコンテンツに静的 URL を使用します。 静的 URL は絶対 URL で、 [ベース URL](../stores-purchase/store-urls.md) 」という名前に変更されます。

   - `No` - （デフォルト）WYSIWYG エディターで挿入されるメディアコンテンツの動的 URL を、 `\{\{media url="..."}}` ディレクティブ。 動的 URL は相対 URL で、ストアのベース URL が変更されても壊れません。

1. 完了したら、「 **[!UICONTROL Save Config]**.
