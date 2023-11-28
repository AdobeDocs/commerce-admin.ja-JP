---
title: 製品画像の設定
description: 最大ピクセルサイズ（幅と高さ）を設定し、アップロード時に製品画像ファイルのサイズを自動的に変更する方法を説明します。
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# 製品画像の設定

大きな画像をアップロードして、 _[!UICONTROL Product Details]_ページの場合は、最大ピクセルサイズ（幅と高さ）の設定と、アップロード時にファイルのサイズを自動的に変更することを検討してください。 この種の製品画像のアップロードをサポートするために、アップロード時に大きな画像ファイルのサイズを自動的に変更できるオプションがあります。 カタログに追加するが、表示する画像アセットがまだない商品の場合は、プレースホルダー画像を設定できます。

## 製品画像のサイズ変更

製品画像をアップロードする際に、様々なサイズの大きな画像を追加して、 _[!UICONTROL Product Details]_ページに貼り付けます。 すべての画像のサイズと外観が同じになるように、すべての画像が特定のピクセルサイズに一致するようにする画像サイズ変更オプションがあります。 このオプションを選択すると、設定を使用してすべての製品画像のサイズが自動的に変更されます。これにより、ズームのパフォーマンス、画像の読み込みの高速化、製品画像の外観の統一を図ることができます。

>[!NOTE]
>
>互換性を最善にするために、すべての製品画像を `sRGB` カラープロファイル。 その他のすべてのカラープロファイルは、 `sRGB` 製品画像のアップロード中にカラープロファイルが生成され、アップロードされた画像の色に不整合が生じる可能性がありました。

最大のピクセル幅と高さを設定すると、画像のサイズがピクセル単位の物理的なサイズに変更されます。 Commerce は、比率を維持しながら、幅または高さの値が大きいほど画像のサイズを変更します。 画質イメージの画質量を減らすと、JPGイメージのファイルサイズが小さくなります。

例えば、100 %のJPGが 3000 x 2100 ピクセルの場合、画像ファイルのサイズは 5 mb 以上になります。 この画像のサイズを変更すると、幅が 1920 ピクセルに減り、縦横比と画質が 80 %になり、より小さく高品質なファイルサイズが得られます。

### 画像のサイズ変更を有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _画像のアップロード設定_ 」セクションに入力します。

   デフォルト設定を変更するには、 **[!UICONTROL Use system value]** 必要に応じて、「 」チェックボックスをオンにします。

   ![画像のアップロード設定](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   これらの設定の詳細なリストについては、 [_画像のアップロード設定_](../configuration-reference/advanced/system.md#image-upload-configuration) （内） _設定リファレンス_.

1. 有効にするには、 **[!UICONTROL Enable Frontend Resize]** が `Yes`.

1. を入力します。 **[!UICONTROL Quality]** 次の間の設定 `1` および `100`%.

   ファイルサイズを小さくして高品質にするには、80～90%の設定をお勧めします。

1. を設定します。 **[!UICONTROL Maximum Width]** 画像のピクセル単位で指定します。

   画像のサイズが変更されても、この幅を超えず、比率も保持されます。

1. を設定します。 **[!UICONTROL Maximum Height]** 画像のピクセル単位で指定します。

   画像のサイズを変更しても、この高さを超えず、比率も保持されます。

1. 完了したら、「 **[!UICONTROL Save Config]**.

### フィールドの説明

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Quality] | グローバル | サイズ変更されたJPGの画像の画質を指定します。 低い品質を指定すると、ファイルサイズが小さくなります。 80～90%が高品質でファイルサイズを小さくするのに役立つことをお勧めします。 デフォルト： 80 |
| [!UICONTROL Enable Frontend Resize] | グローバル | Commerce で、大きくて大きすぎるサイズの画像のサイズを変更できます。 _[!UICONTROL Product Details]_ページに貼り付けます。 Commerce は、ファイルのアップロード時に JavaScript を使用して画像ファイルのサイズを変更します。 画像のサイズが変更されると、「最大の幅」または「最大の高さ」の最大サイズを超えないように、正確な比率が維持されます。 デフォルト： `Yes` |
| [!UICONTROL Maximum Width] | グローバル | 画像の最大ピクセル幅を決定します。 画像のサイズが変更されても、この幅を超えることはありません。 デフォルト： `1920` |
| [!UICONTROL Maximum Height] | グローバル | 画像の最大ピクセル高を決定します。 画像のサイズが変更されても、この高さを超えることはありません。 デフォルト： `1200` |

{style="table-layout:auto"}

## 画像プレースホルダー

Adobe CommerceとMagento Open Sourceは、永久的な製品画像が使用可能になるまで、一時画像をプレースホルダーとして使用します。 役割ごとに異なるプレースホルダーをアップロードできます。 最初のプレースホルダー画像はサンプルロゴで、任意の画像に置き換えることができます。

![画像プレースホルダー](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_プレースホルダー画像をアップロードするには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張アイコン](../assets/icon-display-expand.png) の **[!UICONTROL Product Image Placeholders]** 」セクションに入力します。

   ![製品画像のプレースホルダー](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   これらの設定の詳細なリストについては、 [_製品画像のプレースホルダー_](../configuration-reference/catalog/catalog.md#product-image-placeholders) （内） _設定リファレンス_.

1. 画像の役割ごとに、 **[!UICONTROL Choose File]**、お使いのコンピューター上の画像を探し、ファイルをアップロードします。

   3 つの役割すべてに同じ画像を使用することも、役割ごとに異なるプレースホルダー画像をアップロードすることもできます。

1. 完了したら、「 **[!UICONTROL Save]**.

画像の役割と推奨サイズについて詳しくは、 [画像をアップロード](product-image.md#upload-an-image).
