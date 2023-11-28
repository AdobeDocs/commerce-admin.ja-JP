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

任意 [動的ブロック](dynamic-blocks.md) 作成したをプロモーションに関連付けることができます。 関連付けを作成するには、まずダイナミックブロックと [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md) または [買い物かごの価格ルール](../merchandising-promotions/price-rules-cart.md). 関連付けは、価格ルールの作業中、または動的ブロックの操作中に作成できます。

>[!IMPORTANT]
>
>この関連付けを作成すると、ダイナミックブロックが表示されます **のみ** ルールが起動したとき。 プロモーションがセグメント A をターゲットとしている場合、ブロックはセグメント A に表示されます。プロモーションがアクティブでない場合、ブロックは表示されません。

## 価格ルールへの動的ブロックの関連付け

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_をクリックし、次のいずれかを選択します。

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. グリッドで、ダイナミックブロックに関連付けるルールを探し、編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. 1 列目で、フィルターをに設定します。 `Any` をクリックします。 **[!UICONTROL Reset Filter]**.

   グリッドに、使用可能なすべてのダイナミックブロックがリストされます。

1. ルールに関連付ける各ダイナミックブロックのチェックボックスをオンにします。

   ![選択した動的ブロックの追加](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save]**.

## 価格ルールと動的ブロックの関連付け

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. グリッド内のダイナミックブロックを探し、編集モードで開きます。

1. 下にスクロールして展開 **[!UICONTROL Related Promotions]**.

   現在関連付けられている価格ルールがグリッドに表示されます。

1. 新しい関連付けられたルールを追加するか、現在の関連付けを削除します。

   - 買い物かごのプロモーションを関連付けるには、 **[!UICONTROL Add Cart Price Rules]**.

   - 製品関連のプロモーションを関連付けるには、 **[!UICONTROL Add Catalog Price Rules]**.

1. グリッドで、ダイナミックブロックに関連付ける各ルールのチェックボックスをオンにします。

1. クリック **[!UICONTROL Add Selected]**.

   ![選択した価格ルールを動的ブロックに追加する](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save]**.
