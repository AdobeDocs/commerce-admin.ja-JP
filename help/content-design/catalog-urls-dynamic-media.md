---
title: Dynamic Media の URL
description: 画像または他のメディアアセットへの相対参照として Dynamic Media URL を使用する方法について説明します。
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Dynamic Media の URL

Dynamic Media URL は、画像またはその他のメディアアセットへの相対参照です。 有効にすると、Dynamic Media URL を使用して、サーバー上のアセットや、（コンテンツ配信ネットワーク [ に保存されたファイルに直接リンクでき ](media-storage-content-delivery-network.md) す。 Dynamic Media URL を使用すると、カタログのパフォーマンスに影響を与える可能性があり、静的 URL または Dynamic Media URL を使用するように [ エディター ](editor.md#configure-the-editor) を設定できます。

すべての [ マークアップタグ ](../systems/markup-tags.md) と同様に、ディレクティブは二重の中括弧で囲まれています。 Dynamic Media URL の形式は次のようになります。

`\{\{media url="path/to/image.jpg"}}`

動的 URL ディレクティブは、ページがストアフロントでレンダリングされる際に、保存されたHTML コンテンツから処理されます。 ページがレンダリングされるたびに、コンテンツの `\{\{media url="..."}}` がスキャンされ、各ディレクティブが対応するメディア URL に置き換えられます。

{{$include /help/_includes/directives-caution.md}}

## 静的メディア URL の設定

デフォルトでは、WYSIWYG エディターからカタログに挿入された画像には、相対的な動的 URL が割り当てられます。 静的 URL を使用する場合は、設定を変更できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL WYSIWYG Options]**」セクションを展開します。

   ![WYSIWYG オプション ](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** を次のいずれかに設定します。

   - `Yes` - WYSIWYG エディターで挿入されるメディアコンテンツに静的 URL を使用します。 静的 URL は絶対 URL で、ストアの [ ベース URL](../stores-purchase/store-urls.md) が変更された場合は壊れます。

   - `No` – （デフォルト） `\{\{media url="..."}}` ディレクティブに基づいて、WYSIWYG エディターで挿入されるメディアコンテンツに動的 URL を使用します。 動的 URL は相対 URL で、ストアのベース URL が変更された場合でも破損しません。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
