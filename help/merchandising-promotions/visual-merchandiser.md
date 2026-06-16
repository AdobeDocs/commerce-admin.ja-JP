---
title: Visual Merchandiserの概要
description: 商品を配置し、カテゴリ リストに表示される商品を決定できるビジュアル マーチャンダイザーツールについて説明します。
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/MbeCfIBdepAr5U2B1I-lfFGNm1b5DiKGevM5365brpo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

_Visual Merchandiser_&#x200B;は、製品を配置し、カテゴリ リストに表示される製品を決定する条件を適用できる高度なツールのセットです。 その結果、カタログの変更に合わせて調整される製品の動的な選択が得られます。 各プロダクトをタイルとしてグリッド上に表示する&#x200B;_ビジュアルモード_&#x200B;で作業したり、カテゴリ内のプロダクトのリストから作業したりできます。 各モードで同じツールを使用でき、右上隅のボタンを使用して各タイプの表示を切り替えることができます。

![ タイル表示のカテゴリ製品](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Visual Merchandiserへのアクセス

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. カテゴリーツリーをドリルダウンして、編集するカテゴリをクリックします。

1. 下にスクロールして、**[!UICONTROL Products in Category]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. 「_タイルとして表示_ （![ タイルとして表示](../assets/icon-view-tiles.png)）」ボタンをクリックすると、商品がグリッドとして表示されます。

1. 完了したら、**[!UICONTROL Save Category]**&#x200B;をクリックします。

## 製品の位置を変更する

1. [並べ替え順序](../catalog/navigation-product-listings.md)を使用して、移動する商品を表示します。

   - **方法1: ドラッグ&amp;ドロップ**

     製品タイルの右上隅にある&#x200B;_ドラッグ_ （![ ドラッグアイコン ](../assets/icon-move.png)）コントロールを使用して、製品を配置します。 各商品の数は、新しい位置を反映するように調整されます。

   - **方法2: ポジション値を設定**

     製品タイルの&#x200B;_位置_ コントローラー（![位置フィールド ](../assets/control-position.png)）に、製品を表示する番号を入力します。 `0`と入力して、商品をリストの一番上に配置します。

1. 完了したら、**[!UICONTROL Save Category]**&#x200B;をクリックします。

>[!NOTE]
>
>クリーンなインストールでは、Adobe Commerceはデフォルトストアのルートカタログのカテゴリ ID `2`を予約します。 Visual Merchandiserは、ID番号が`3`以上のカテゴリのみを使用できます。

## Workspaceコントロール

| 制御 | 説明 |
|--- |--- |
| ![ リストアイコンを表示](../assets/icon-view-list.png) | リストとして表示 |
| ![ タイルとして表示アイコン ](../assets/icon-view-tiles.png) | タイルとして表示 |
| ![ ルールによる一致の切り替え – no](../assets/toggle-no.png) | ルールによる一致 – いいえ |
| ![ ルールで一致トグル – はい](../assets/toggle-yes.png) | ルールによる一致 – はい |
| ![移動アイコン ](../assets/icon-move.png) | ドラッグ |
| ![位置コントローラー](../assets/control-position.png) | 位置 |
| ![ カテゴリーアイコンから削除](../assets/icon-delete-x.png) | カテゴリから削除 |
| ![ ページコントロールごとの項目](../assets/control-items-per-page.png) | ページ単位で表示 |
| ![ ページ表示の変更](../assets/control-page-display.png) | 次/前に移動 |

{style="table-layout:auto"}
