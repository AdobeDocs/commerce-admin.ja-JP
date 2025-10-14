---
title: ビジュアルマーチャンダイザーの概要
description: 製品を配置し、カテゴリリストに表示する製品を決定できるビジュアルマーチャンダイザーツールについて説明します。
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# ビジュアルマーチャンダイザー

{{ee-feature}}

_ビジュアルマーチャンダイザー_ は、製品を配置し、カテゴリリストに表示する製品を決定する条件を適用できる高度なツールのセットです。 その結果、カタログの変更に合わせて調整される製品を動的に選択することができます。 _ビジュアルモード_ で作業すると、各製品をグリッド上にタイルとして表示したり、カテゴリ内の製品のリストから作業したりできます。 各モードでは同じツールを使用でき、右上隅のボタンを使用して各タイプの表示を切り替えることができます。

![&#x200B; タイル表示のカテゴリ製品 &#x200B;](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## ビジュアルマーチャンダイザーへのアクセス

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. カテゴリツリーをドリルダウンし、編集するカテゴリをクリックします。

1. 下にスクロールして、「**[!UICONTROL Products in Category]**」セクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開します。

1. _タイルとして表示_ （![&#x200B; タイルとして表示 &#x200B;](../assets/icon-view-tiles.png)）ボタンをクリックして、製品をグリッドとして表示します。

1. 完了したら、「**[!UICONTROL Save Category]**」をクリックします。

## 商品の位置の変更

1. [&#x200B; 並べ替え順 &#x200B;](../catalog/navigation-product-listings.md) を使用して、移動する商品を表示します。

   - **方法 1：ドラッグ&amp;ドロップ**

     製品タイルの右上隅にある _ドラッグ_ （![&#x200B; ドラッグアイコン &#x200B;](../assets/icon-move.png)）コントロールをつかんで、製品を所定の位置にドロップします。 各製品の数は、新しい位置を反映するように調整されます。

   - **方法 2：位置の値を設定**

     製品タイルの _位置_ コントローラー（![&#x200B; 位置フィールド &#x200B;](../assets/control-position.png)）に、製品を表示する番号を入力します。 製品をリストの先頭に配置するには、`0` と入力します。

1. 完了したら、「**[!UICONTROL Save Category]**」をクリックします。

>[!NOTE]
>
>クリーンなインストールでは、Adobe Commerceはカテゴリ ID `2` をデフォルトストアのルートカタログに予約します。 ビジュアルマーチャンダイザーは、ID 番号が `3` 以上のカテゴリのみを使用できます。

## Workspaceの制御

| 制御 | 説明 |
|--- |--- |
| ![&#x200B; リストを表示アイコン &#x200B;](../assets/icon-view-list.png) | リストとして表示 |
| ![&#x200B; タイル表示アイコン &#x200B;](../assets/icon-view-tiles.png) | タイルとして表示 |
| ![&#x200B; ルールによる一致の切り替え – いいえ &#x200B;](../assets/toggle-no.png) | ルールによる一致 – なし |
| ![&#x200B; ルールで一致を切り替え – はい &#x200B;](../assets/toggle-yes.png) | ルールによる一致 – はい |
| ![&#x200B; 移動アイコン &#x200B;](../assets/icon-move.png) | ドラッグ |
| ![&#x200B; 位置コントローラ &#x200B;](../assets/control-position.png) | 位置 |
| ![&#x200B; カテゴリアイコンから削除 &#x200B;](../assets/icon-delete-x.png) | カテゴリから削除 |
| ![&#x200B; ページコントロールあたりの項目数 &#x200B;](../assets/control-items-per-page.png) | ページごとに表示 |
| ![&#x200B; ページ表示の変更 &#x200B;](../assets/control-page-display.png) | 次/前に移動 |

{style="table-layout:auto"}
