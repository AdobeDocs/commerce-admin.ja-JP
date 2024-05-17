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

表示するために大きな画像をアップロードする予定がある場合 _[!UICONTROL Product Details]_ページの場合、最大ピクセルサイズ（幅と高さ）を設定し、アップロード時にファイルのサイズを自動的に変更することを検討してください。 このタイプの製品画像のアップロードをサポートするには、アップロード時に大きな画像ファイルの自動サイズ変更を有効にするオプションがあります。 カタログに追加したいが、表示する画像アセットがまだない製品については、プレースホルダー画像を設定できます。

## 製品画像のサイズ変更

製品画像をアップロードする際に、様々なサイズの大きい画像を追加して、詳細で高品質なズームを _[!UICONTROL Product Details]_ページ。 すべての画像のサイズと外観を同じにするために、すべての画像が特定のピクセルサイズと一致するように画像サイズを変更するオプションがあります。 このオプションは、設定を使用してすべての製品画像のサイズを自動的に変更します。これにより、ズームのパフォーマンス、画像の読み込みの高速化、製品画像の外観の統一に役立ちます。

>[!NOTE]
>
>最高の互換性を得るには、以下のパラメーターを使用して、すべての製品画像をアップロードすることをお勧めします `sRGB` カラープロファイル。 その他のカラープロファイルはすべて、 `sRGB` 製品画像のアップロード中にカラープロファイルが正しく設定されず、アップロードされた画像のカラーに一貫性がなくなる場合がありました。

最大のピクセル幅と高さを設定すると、画像のサイズがピクセル単位の物理的寸法に変更されます。 Commerceは、比率を維持しながら、幅または高さのいずれか高い方の量に応じて画像のサイズを変更します。 JPG画像の画質を下げると、ファイルサイズが小さくなります。

例えば、3000 x 2100 ピクセルのJPGが 100% の場合、5 mb 以上の画像ファイルになることがあります。 この画像のサイズを変更すると、幅が 1920 ピクセルに減少し、比率と画質が 80% に維持され、より小さいファイルサイズで高品質が提供されます。

### 画像のサイズ変更を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _画像アップロード設定_ セクション。

   デフォルトの設定を変更するには、 **[!UICONTROL Use system value]** 必要に応じてチェックボックスをオンにします。

   ![画像アップロード設定](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   これらの設定の詳細なリストについては、を参照してください [_画像アップロード設定_](../configuration-reference/advanced/system.md#image-upload-configuration) が含まれる _設定リファレンス_.

1. を有効にするには、以下を確認します **[!UICONTROL Enable Frontend Resize]** はに設定されています。 `Yes`.

1. を入力 **[!UICONTROL Quality]** 間の設定 `1` および `100`%。

   ファイルサイズを小さくして画質を高くするには、80～90% の設定をお勧めします。

1. を **[!UICONTROL Maximum Width]** 画像のピクセル数。

   画像のサイズを変更しても、その幅を超えることはなく、縦横比を維持します。

1. を **[!UICONTROL Maximum Height]** 画像のピクセル数。

   画像のサイズを変更しても、この高さを超えることはなく、縦横比を維持します。

1. 完了したら、 **[!UICONTROL Save Config]**.

### フィールドの説明

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Quality] | グローバル | サイズ変更された画像のJPG画質を指定します。 画質が低いとファイルサイズは小さくなります。 高品質でファイルサイズを減らすには、80～90% をお勧めします。 デフォルト：80 |
| [!UICONTROL Enable Frontend Resize] | グローバル | を使用すると、Commerceがアップロードできる大きくサイズが超過した画像のサイズを _[!UICONTROL Product Details]_ページ。 Commerceは、ファイルのアップロード時に、JavaScript を使用して画像ファイルのサイズを変更します。 画像のサイズを変更すると、最大幅または最大高さの最大サイズに合わせて、正確な比率が維持されます。 デフォルト： `Yes` |
| [!UICONTROL Maximum Width] | グローバル | 画像の最大ピクセル幅を決定します。 画像のサイズを変更しても、この幅を超えることはありません。 デフォルト： `1920` |
| [!UICONTROL Maximum Height] | グローバル | 画像の最大ピクセル高さを決定します。 画像のサイズを変更しても、この高さを超えることはありません。 デフォルト： `1200` |

{style="table-layout:auto"}

## 画像プレースホルダー

Adobe CommerceとMagento Open Sourceでは、永続的な商品画像が使用可能になるまで、一時的な画像をプレースホルダーとして使用します。 役割ごとに異なるプレースホルダーをアップロードできます。 最初のプレースホルダー画像はサンプルロゴで、選択した画像に置き換えることができます。

![画像プレースホルダー](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_プレースホルダー画像をアップロードするには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![拡張アイコン](../assets/icon-display-expand.png) この **[!UICONTROL Product Image Placeholders]** セクション。

   ![製品画像プレースホルダー](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   これらの設定の詳細なリストについては、を参照してください [_製品画像プレースホルダー_](../configuration-reference/catalog/catalog.md#product-image-placeholders) が含まれる _設定リファレンス_.

1. 各画像の役割に対して、 **[!UICONTROL Choose File]**&#x200B;をタップし、コンピューター上の画像を探してファイルをアップロードします。

   3 つの役割すべてに同じ画像を使用することも、役割ごとに異なるプレースホルダー画像をアップロードすることもできます。

1. 完了したら、 **[!UICONTROL Save]**.

画像の役割と推奨サイズについて詳しくは、を参照してください [画像をアップロード](product-image.md#upload-an-image).
