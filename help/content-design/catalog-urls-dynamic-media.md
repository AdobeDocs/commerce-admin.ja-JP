---
title: ダイナミックメディア URL
description: 画像またはその他のメディアアセットへの相対参照としてDynamic Media URLを使用する方法について説明します。
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: e2b1250c346f4eea68e08e616bf43671cb62794e
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# ダイナミックメディア URL

ダイナミックメディア URLは、画像またはその他のメディアアセットへの相対参照です。 有効にすると、ダイナミックメディア URLを使用して、サーバー上のアセットに直接リンクしたり、[ コンテンツ配信ネットワーク ](media-storage-content-delivery-network.md)に保存されているファイルにリンクしたりできます。 ダイナミックメディア URLの使用はカタログのパフォーマンスに影響を与える可能性があり、[ エディター](editor.md#configure-the-editor)は静的URLまたは動的メディア URLのいずれかを使用するように設定できます。

すべての[ マークアップタグ ](../systems/markup-tags.md)と同様に、ディレクティブは二重中括弧で囲まれます。 Dynamic Media URLの形式は次のようになります。

`\{\{media url="path/to/image.jpg"}}`

ページがストアフロントでレンダリングされると、保存されたHTML コンテンツから動的URL ディレクティブが処理されます。 ページがレンダリングされるたびに、コンテンツが`\{\{media url="..."}}`に対してスキャンされ、各ディレクティブは対応するメディア URLに置き換えられます。

{{$include /help/_includes/directives-caution.md}}

## 静的メディア URLの設定

デフォルトでは、WYSIWYG エディターからカタログに挿入された画像には、相対URLと動的URLが設定されています。 静的URLを使用する場合は、設定設定を変更できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左側のパネルで、**[!UICONTROL Content Management]**を選択します。

1. **[!UICONTROL WYSIWYG Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![WYSIWYG オプション ](../configuration-reference/general/assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

>[!NOTE]
>
>TinyMCEは、Magento 2.4.6以降のバージョンのデフォルトのWYSIWYG エディターとしてHugerteに置き換えられました。

1. **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]**&#x200B;を次のいずれかに設定します：

   - `Yes` - WYSIWYG エディターと共に挿入されるメディアコンテンツに静的URLを使用します。 静的URLは絶対であり、ストアの[ ベース URL](../stores-purchase/store-urls.md)が変更された場合は壊れます。

   - `No` - （デフォルト） `\{\{media url="..."}}` ディレクティブに基づいて、WYSIWYG エディターと共に挿入されるメディアコンテンツに動的URLを使用します。 動的URLは相対URLであり、ストアのベース URLが変更されても壊れません。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
