---
title: ビジュアルマーチャンダイザーの概要
description: 製品を配置し、カテゴリリストに表示する製品を決定できるビジュアルマーチャンダイザーツールについて説明します。
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# ビジュアルマーチャンダイザー

{{ee-feature}}

この _ビジュアルマーチャンダイザー_ は、製品を配置し、カテゴリリストに表示する製品を決定する条件を適用できる高度なツールのセットです。 その結果、カタログの変更に合わせて調整される製品を動的に選択することができます。 次で作業できます _視覚モード_：各製品をグリッド上のタイルとして表示したり、カテゴリ内の製品のリストから操作したりできます。 各モードでは同じツールを使用でき、右上隅のボタンを使用して各タイプの表示を切り替えることができます。

![タイル表示のカテゴリ製品](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## ビジュアルマーチャンダイザーへのアクセス

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーをドリルダウンし、編集するカテゴリをクリックします。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Products in Category]** セクション。

1. 「」をクリックします _タイルとして表示_ （ ![タイルとして表示](../assets/icon-view-tiles.png) ）ボタンをクリックし、商品をグリッドとして表示します。

1. 完了したら、 **[!UICONTROL Save Category]**.

## 商品の位置の変更

1. の使用 [並べ替え順序](../catalog/navigation-product-listings.md) 移動する商品を表示します。

   - **方法 1：ドラッグ&amp;ドロップ**

     つかむ _ドラッグ_ （![ドラッグアイコン](../assets/icon-move.png)）を選択し、製品を適切な位置にドロップします。 各製品の数は、新しい位置を反映するように調整されます。

   - **方法 2：位置の値を設定する**

     が含まれる _位置_ コントローラ （![位置フィールド](../assets/control-position.png)）を選択し、製品タイルに製品を表示する番号を入力します。 Enter `0` をクリックして、製品をリストの先頭に配置します。

1. 完了したら、 **[!UICONTROL Save Category]**.

>[!NOTE]
>
>新規インストールでは、Adobe Commerceがカテゴリ ID を予約します `2` デフォルトストアのルートカタログ用。 ビジュアルマーチャンダイザーは、ID 番号がのカテゴリのみを使用できます `3` 以上。

## ワークスペースコントロール

| 制御 | 説明 |
|--- |--- |
| ![リスト表示アイコン](../assets/icon-view-list.png) | リストとして表示 |
| ![タイル表示アイコン](../assets/icon-view-tiles.png) | タイルとして表示 |
| ![ルールによる一致の切り替え – いいえ](../assets/toggle-no.png) | ルールによる一致 – なし |
| ![ルールで一致の切替スイッチ – はい](../assets/toggle-yes.png) | ルールによる一致 – はい |
| ![移動アイコン](../assets/icon-move.png) | ドラッグ |
| ![位置コントローラ](../assets/control-position.png) | 位置 |
| ![カテゴリアイコンから削除](../assets/icon-delete-x.png) | カテゴリから削除 |
| ![ページコントロールあたりの項目数](../assets/control-items-per-page.png) | ページごとに表示 |
| ![ページ表示の変更](../assets/control-page-display.png) | 次/前に移動 |

{style="table-layout:auto"}
