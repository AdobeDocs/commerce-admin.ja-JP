---
title: 買い物かご価格ルールの例 – 最小製品価格による割引
description: 買い物かご価格ルールを使用して、最小製品価格による割引を提供する例を確認します。
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 1a784e894e02090cfa3bc9edc47149b35d935e8e
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# 買い物かご価格ルールの例 – 最小製品価格による割引

買い物かご価格ルールを使用すると、買い物かご内の最小製品価格に基づいてパーセンテージの割引を提供できます。 次の例では、指定したカテゴリの価格が 30.00 ドルを超える商品が 1 つ以上カートに追加された場合に、カート全体のすべての商品に 10% の割引が適用されます。 割引の形式は次のとおりです。

少なくとも 1 つの商品が Y カテゴリのもので、その価格が$Z ドルを超える場合、買い物かご全体の X% がオフになります。

## 手順 1. 買い物かごルールの作成

基本的な [ 手順 ](price-rules-cart.md) に従って、買い物かごルールを作成します。

## 手順 2. 条件の定義

1. 下にスクロールして、「**[!UICONTROL Conditions]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

1. _追加_ （![ 追加アイコン ](../assets/icon-add-green-circle.png)）をクリックし、**[!UICONTROL Product Attribute Combination]** を選択します。

   ![ 買い物かご価格ルール条件 – 製品属性の組み合わせ ](./assets/condition1.png){width="500" zoomable="yes"}

1. 次の行の先頭にある _追加_ （![ 追加アイコン ](../assets/icon-add-green-circle.png)）をクリックし、「**[!UICONTROL Product Attribute]**」の下のリストで「**[!UICONTROL Category]**」を選択します。

   - （**...**） _その他_ リンクをクリックすると、その他のオプションが表示されます。

     ![ 買い物かご価格ルールの条件 – カテゴリオプション ](./assets/condition3.png){width="600" zoomable="yes"}

   - _選択_ （![ リストアイコン ](../assets/icon-list-chooser.png)）アイコンをクリックして、使用可能なカテゴリを表示します。 カテゴリツリーで、含める各カテゴリのチェックボックスを選択します。 チェックアイコンをクリックして、カテゴリの選択を確定します。

     ![ 買い物かご価格ルール条件 – カテゴリ ](./assets/condition4.png){width="600" zoomable="yes"}

1. 次の行の先頭にある _追加_ （![ 追加アイコン ](../assets/icon-add-green-circle.png)）をクリックし、次の手順を実行します。

   - **[!UICONTROL Cart Item Attribute]** の下のリストで、「**[!UICONTROL Price in cart]**」を選択します。

     ![ 買い物かご価格ルール条件 – 買い物かご品目属性 ](./assets/condition5.png){width="500"}

   - 「**is**」をクリックし、「`equals or greater than`」を選択します。

   - 「**...**」をクリックし、「買い物かごの価格」が条件を満たす必要がある金額を入力します。 例えば、「`30`」と入力します。

     ![ 買い物かご価格ルールの条件 – 買い物かごの価格 ](./assets/condition6.png){width="500"}

1. 「**[!UICONTROL Save and Continue Edit]**」をクリックします。

## 手順 3. アクションの定義

1. **[!UICONTROL Actions]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![ 買い物かご価格ルールアクション ](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - **[!UICONTROL Apply]** を `Percent of product price discount` に設定します。

   - **[!UICONTROL Discount Amount]** を入力します。 例えば、10% の割引を受ける場合は `10` と入力します。

   - 追加のプロモーションが購入に適用されないようにするには、**[!UICONTROL Discard subsequent rules]** を `Yes` に設定します。

1. 「**[!UICONTROL Save and Continue Edit]**」をクリックし、必要に応じてルールを入力します。

## 手順 4. ラベルを完成させる

買い物かご価格ルールの手順の [ 手順 4](price-rules-cart.md) を完了して、チェックアウト時に表示されるラベルを入力します。

## 手順 5：ルールを保存してテストする

{{new-price-rule}}

1. ルールが完成したら、「**[!UICONTROL Save Rule]**」をクリックします。
1. ルールをテストして、正しく動作することを確認します。
