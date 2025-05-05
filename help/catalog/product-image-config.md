---
title: 製品イメージ設定
description: アップロード中に最大ピクセルサイズ（幅と高さ）を設定し、製品画像ファイルのサイズを自動的に変更する方法について説明します。
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# 製品イメージ設定

_[!UICONTROL Product Details]_&#x200B;ページに表示する大きな画像をアップロードする場合は、最大ピクセルサイズ（幅と高さ）を設定し、アップロード時にファイルのサイズを自動的に変更することを検討してください。 このタイプの製品画像のアップロードをサポートするには、アップロード時に大きな画像ファイルの自動サイズ変更を有効にするオプションがあります。 カタログに追加したいが、表示する画像アセットがまだない製品については、プレースホルダー画像を設定できます。

## 製品画像のサイズ変更

製品画像をアップロードする際に、様々なサイズの大きい画像を追加して、_[!UICONTROL Product Details]_&#x200B;ページに詳細で高品質なズームを提供できます。 すべての画像のサイズと外観を同じにするために、すべての画像が特定のピクセルサイズと一致するように画像サイズを変更するオプションがあります。 このオプションは、設定を使用してすべての製品画像のサイズを自動的に変更します。これにより、ズームのパフォーマンス、画像の読み込みの高速化、製品画像の外観の統一に役立ちます。

>[!NOTE]
>
>最高の互換性を得るには、`sRGB` のカラープロファイルを使用してすべての製品画像をアップロードすることをお勧めします。 その他のすべてのカラープロファイルは、製品画像のアップロード中に `sRGB` カラープロファイルに自動的に変換されるので、アップロードされた画像のカラーが一貫しない場合があります。

最大のピクセル幅と高さを設定すると、画像のサイズがピクセル単位の物理的寸法に変更されます。 Commerceは、比率を維持しながら、幅または高さのいずれか高い方の量に応じて画像のサイズを変更します。 JPG画像の画質を下げると、ファイルサイズが小さくなります。

例えば、3000 x 2100 ピクセルのJPGが 100% の場合、5 mb 以上の画像ファイルになることがあります。 この画像のサイズを変更すると、幅が 1920 ピクセルに減少し、比率と画質が 80% に維持され、より小さいファイルサイズで高品質が提供されます。

### 画像のサイズ変更を有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. ![ 展開セレクター ](../assets/icon-display-expand.png) 「画像アップロード設定 _セクション_ を展開します。

   デフォルトの設定を変更するには、必要に応じて「**[!UICONTROL Use system value]**」チェックボックスの選択を解除します。

   ![ 画像のアップロード設定 ](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   これらの設定の詳細なリストについては、[_設定リファレンス_](../configuration-reference/advanced/system.md#image-upload-configuration) の _画像のアップロード設定_ を参照してください。

1. 有効にするには、**[!UICONTROL Enable Frontend Resize]** が `Yes` に設定されていることを確認します。

1. `1` ～ `100`% の **[!UICONTROL Quality]** 設定を入力します。

   ファイルサイズを小さくして画質を高くするには、80～90% の設定をお勧めします。

1. 画像の **[!UICONTROL Maximum Width]** をピクセル単位で設定します。

   画像のサイズを変更しても、その幅を超えることはなく、縦横比を維持します。

1. 画像の **[!UICONTROL Maximum Height]** をピクセル単位で設定します。

   画像のサイズを変更しても、この高さを超えることはなく、縦横比を維持します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### フィールドの説明

| フィールド | [ 範囲 ](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Quality] | グローバル | サイズ変更された画像のJPG画質を指定します。 画質が低いとファイルサイズは小さくなります。 高品質でファイルサイズを減らすには、80～90% をお勧めします。 デフォルト：80 |
| [!UICONTROL Enable Frontend Resize] | グローバル | を使用すると、_[!UICONTROL Product Details]_&#x200B;ページにアップロードできる大きい画像やサイズを超過した画像のサイズを、Commerceで変更できます。 Commerceは、ファイルのアップロード時にJavaScriptを使用して画像ファイルのサイズを変更します。 画像のサイズを変更すると、最大幅または最大高さの最大サイズに合わせて、正確な比率が維持されます。 デフォルト：`Yes` |
| [!UICONTROL Maximum Width] | グローバル | 画像の最大ピクセル幅を決定します。 画像のサイズを変更しても、この幅を超えることはありません。 デフォルト：`1920` |
| [!UICONTROL Maximum Height] | グローバル | 画像の最大ピクセル高さを決定します。 画像のサイズを変更しても、この高さを超えることはありません。 デフォルト：`1200` |

{style="table-layout:auto"}

## 画像プレースホルダー

Adobe CommerceとMagento Open Sourceでは、永続的な商品画像が使用可能になるまで、一時的な画像をプレースホルダーとして使用します。 役割ごとに異なるプレースホルダーをアップロードできます。 最初のプレースホルダー画像はサンプルロゴで、選択した画像に置き換えることができます。

![ 画像のプレースホルダー ](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_プレースホルダー画像をアップロードするには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「**[!UICONTROL Product Image Placeholders]**」セクションの ![ 展開アイコン ](../assets/icon-display-expand.png) 展開します。

   ![ 製品画像のプレースホルダー ](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   これらの設定の詳細なリストについては、[_設定リファレンス_](../configuration-reference/catalog/catalog.md#product-image-placeholders) の _製品画像プレースホルダー_ を参照してください。

1. 各画像の役割に対して「**[!UICONTROL Choose File]**」をクリックし、コンピューター上で画像を見つけてファイルをアップロードします。

   3 つの役割すべてに同じ画像を使用することも、役割ごとに異なるプレースホルダー画像をアップロードすることもできます。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

画像の役割と推奨サイズについて詳しくは、[ 画像のアップロード ](product-image.md#upload-an-image) を参照してください。
