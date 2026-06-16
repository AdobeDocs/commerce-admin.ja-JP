---
title: ダイナミックメディア URL
description: 画像またはその他のメディアアセットへの相対参照としてDynamic Media URLを使用する方法について説明します。
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/nml-pHTHdSPcvIVnRwlyjJPhEo2PWdTEKfkn2AFKjvA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# ダイナミックメディア URL

ダイナミックメディア URLは、画像またはその他のメディアアセットへの相対参照です。 有効にすると、ダイナミックメディア URLを使用して、サーバー上のアセットに直接リンクしたり、[&#x200B; コンテンツ配信ネットワーク &#x200B;](media-storage-content-delivery-network.md)に保存されているファイルにリンクしたりできます。 ダイナミックメディア URLの使用はカタログのパフォーマンスに影響を与える可能性があり、[&#x200B; エディター](editor.md#configure-the-editor)は静的URLまたは動的メディア URLのいずれかを使用するように設定できます。

すべての[&#x200B; マークアップタグ &#x200B;](../systems/markup-tags.md)と同様に、ディレクティブは二重中括弧で囲まれます。 Dynamic Media URLの形式は次のようになります。

`\{\{media url="path/to/image.jpg"}}`

ページがストアフロントでレンダリングされると、保存されたHTML コンテンツから動的URL ディレクティブが処理されます。 ページがレンダリングされるたびに、コンテンツが`\{\{media url="..."}}`に対してスキャンされ、各ディレクティブは対応するメディア URLに置き換えられます。

{{$include /help/_includes/directives-caution.md}}

## 静的メディア URLの設定

デフォルトでは、WYSIWYG エディターからカタログに挿入された画像には、相対URLと動的URLが設定されています。 静的URLを使用する場合は、設定設定を変更できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左側のパネルで、**[!UICONTROL Content Management]**&#x200B;を選択します。

1. **[!UICONTROL WYSIWYG Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![WYSIWYG オプション &#x200B;](../configuration-reference/general/assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

>[!NOTE]
>
>TinyMCEは、Magento 2.4.6以降のバージョンのデフォルトのWYSIWYG エディターとしてHugerteに置き換えられました。

1. **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]**&#x200B;を次のいずれかに設定します：

   - `Yes` - WYSIWYG エディターと共に挿入されるメディアコンテンツに静的URLを使用します。 静的URLは絶対であり、ストアの[&#x200B; ベース URL](../stores-purchase/store-urls.md)が変更された場合は壊れます。

   - `No` - （デフォルト） `\{\{media url="..."}}` ディレクティブに基づいて、WYSIWYG エディターと共に挿入されるメディアコンテンツに動的URLを使用します。 動的URLは相対URLであり、ストアのベース URLが変更されても壊れません。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
