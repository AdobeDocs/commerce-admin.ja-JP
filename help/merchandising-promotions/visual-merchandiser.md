---
title: Visual Merchandiser の概要
description: 製品を配置し、カテゴリリストに表示する製品を決定するための Visual Merchandiser ツールについて説明します。
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

The _Visual Merchandiser_ は、製品の位置付けや、カテゴリリストに表示される製品を決定する条件の適用を可能にする、一連の高度なツールです。 結果は、カタログ内の変更に合わせて調整される、動的な製品選択になる場合があります。 以下で作業できます。 _視覚モード_：各製品をグリッド上のタイルとして表示するか、カテゴリ内の製品のリストから操作できるようにします。 各モードで同じツールを使用でき、右上隅のボタンを使用して、各タイプの表示を切り替えることができます。

![タイル表示のカテゴリ製品](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Visual Merchandiser へのアクセス

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーをドリルダウンし、編集するカテゴリをクリックします。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Products in Category]** 」セクションに入力します。

1. 次をクリック： _タイルとして表示_ ( ![タイルとして表示](../assets/icon-view-tiles.png) ) ボタンをクリックして、製品をグリッドとして表示します。

1. 完了したら、「 **[!UICONTROL Save Category]**.

## 製品の位置の変更

1. 以下を使用します。 [並べ替え順](../catalog/navigation-product-listings.md) をクリックして、移動する製品を表示します。

   - **方法 1：ドラッグ&amp;ドロップ**

     を取得 _ドラッグ_ (![ドラッグアイコン](../assets/icon-move.png)) をクリックし、商品を配置します。 各製品の数は、新しい位置を反映するように調整されます。

   - **方法 2：位置値を設定**

     Adobe Analytics の _位置_ コントローラ (![位置フィールド](../assets/control-position.png)) を商品タイルで、商品を表示する番号を入力します。 入力 `0` をクリックして、製品をリストの一番上に配置します。

1. 完了したら、「 **[!UICONTROL Save Category]**.

>[!NOTE]
>
>クリーンなインストールでは、Adobe Commerceはカテゴリ ID を予約します `2` デフォルトのストアのルートカタログの場合。 ビジュアルマーチャンダイザーは、ID 番号が `3` 以上

## Workspace のコントロール

| 制御 | 説明 |
|--- |--- |
| ![リスト表示アイコン](../assets/icon-view-list.png) | リストとして表示 |
| ![タイルとして表示アイコン](../assets/icon-view-tiles.png) | タイルとして表示 |
| ![ルールで一致切り替え — いいえ](../assets/toggle-no.png) | ルールで一致 — いいえ |
| ![ルールで一致切り替え — はい](../assets/toggle-yes.png) | ルールで一致 — はい |
| ![移動アイコン](../assets/icon-move.png) | ドラッグ |
| ![位置コントローラ](../assets/control-position.png) | 位置 |
| ![カテゴリから削除アイコン](../assets/icon-delete-x.png) | カテゴリから削除 |
| ![ページコントロールごとの項目数](../assets/control-items-per-page.png) | ページごとに表示 |
| ![ページ表示の変更](../assets/control-page-display.png) | 次へ/前へ移動 |

{style="table-layout:auto"}
