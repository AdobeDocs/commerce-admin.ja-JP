---
title: 価格ルールの動的ブロック
description: 動的ブロックをプロモーション価格ルールに関連付けます。
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 価格ルールの動的ブロック

{{ee-feature}}

任意 [動的ブロック](dynamic-blocks.md) 作成した情報は、プロモーションに関連付けることができます。 関連付けを行うには、まずダイナミック ブロックとダイナミック ブロックの両方を作成する必要があります。 [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md) または [買い物かご価格ルール](../merchandising-promotions/price-rules-cart.md). 関連付けは、価格ルールの作業中や、動的ブロックの作業中に行うことができます。

>[!IMPORTANT]
>
>この関連付けを作成すると、ダイナミック ブロックが表示されます **のみ** ルールが起動したとき。 プロモーションがセグメント A をターゲットにしている場合、ブロックがセグメント A に表示されます。プロモーションがアクティブでない場合、ブロックは表示されません。

## 価格ルールへの動的ブロックの関連付け

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_次のいずれかの操作を行います。

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. グリッドで、ダイナミック ブロックに関連付けるルールを見つけ、編集モードで開きます。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. 最初の列で、フィルターをに設定します `Any` をクリックして、 **[!UICONTROL Reset Filter]**.

   グリッドに、使用可能なすべてのダイナミック ブロックが一覧表示されます。

1. ルールに関連付ける各ダイナミック ブロックのチェックボックスをオンにします。

   ![選択したダイナミック ブロックを追加する](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

## 価格ルールと動的ブロックの関連付け

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. グリッドでダイナミック ブロックを見つけ、編集モードで開きます。

1. 下にスクロールして展開 **[!UICONTROL Related Promotions]**.

   現在関連付けられている価格ルールがグリッドに表示されます。

1. 新しい関連付けられたルールを追加するか、現在の関連付けを削除します。

   - 買い物かごプロモーションを関連付けるには、 **[!UICONTROL Add Cart Price Rules]**.

   - 製品に関連するプロモーションを関連付けるには、 **[!UICONTROL Add Catalog Price Rules]**.

1. グリッドで、ダイナミック ブロックに関連付ける各ルールのチェックボックスをオンにします。

1. クリック **[!UICONTROL Add Selected]**.

   ![選択した価格ルールの動的ブロックへの追加](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.
