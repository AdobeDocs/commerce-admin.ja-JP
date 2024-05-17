---
title: Dynamic Media の URL
description: 画像または他のメディアアセットへの相対参照として Dynamic Media URL を使用する方法について説明します。
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Dynamic Media の URL

Dynamic Media URL は、画像またはその他のメディアアセットへの相対参照です。 有効にすると、Dynamic Media の URL を使用して、サーバー上のアセットまたはに保存されたファイルに直接リンクできます [コンテンツ配信ネットワーク](media-storage-content-delivery-network.md). Dynamic Media の URL を使用すると、カタログのパフォーマンスに影響する可能性があり、 [エディター](editor.md#configure-the-editor) は、静的 URL または Dynamic Media URL を使用するように設定できます。

他と同様 [マークアップ タグ](../systems/markup-tags.md)、ディレクティブは二重の中括弧で囲まれています。 Dynamic Media URL の形式は次のようになります。

`\{\{media url="path/to/image.jpg"}}`

動的 URL ディレクティブは、ページがストアフロントでレンダリングされる際に、保存されたHTMLコンテンツから処理されます。 ページがレンダリングされるたびに、コンテンツがスキャンされます `\{\{media url="..."}}` 各ディレクティブは、対応するメディア URL に置き換えられます。

{{$include /help/_includes/directives-caution.md}}

## 静的メディア URL の設定

デフォルトでは、WYSIWYG エディターからカタログに挿入された画像には、相対的な動的 URL が割り当てられます。 静的 URL を使用する場合は、設定を変更できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Content Management]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL WYSIWYG Options]** セクション。

   ![WYSIWYG オプション](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** を次のいずれかに変更します。

   - `Yes` - WYSIWYG エディターで挿入されるメディアコンテンツに静的 URL を使用します。 静的 URL は絶対 URL で、 [ベース URL](../stores-purchase/store-urls.md) ストアの変更。

   - `No`  – （デフォルト）に基づいて、WYSIWYG エディターで挿入されたメディアコンテンツに動的 URL を使用します `\{\{media url="..."}}` ディレクティブ。 動的 URL は相対 URL で、ストアのベース URL が変更された場合でも破損しません。

1. 完了したら、 **[!UICONTROL Save Config]**.
