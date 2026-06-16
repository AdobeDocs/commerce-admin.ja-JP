---
title: カートの価格ルールの例 – 最低商品価格での割引
description: カート価格ルールを使用して、最低商品価格の割引を提供する例を紹介します。
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/IRVMCZ8C4uOJ4cBYLEv0YnOsehv0T9XWSIkyjBLhFw4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 0%

---

# カートの価格ルールの例 – 最低商品価格での割引

カートの価格ルールを利用して、カート内の最低商品価格に基づいて、パーセンテージ割引を提供することができます。 次の例では、指定したカテゴリの価格が30.00 ドルを超える少なくとも1つの商品がカートに追加された場合、カート全体のすべての商品に10%の割引が適用されます。 割引の形式は次のとおりです。

少なくとも1つの商品がY カテゴリーのもので、価格がZ ドルを超える場合、買い物客全体のX%がオフになります。

## 手順1: 買い物かごルールの作成

基本的な[手順](price-rules-cart.md)に従って、買い物かごルールを作成します。

## 手順2: 条件の定義

1. 下にスクロールして、**[!UICONTROL Conditions]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. _追加_ （![&#x200B; アイコンを追加](../assets/icon-add-green-circle.png)）をクリックし、**[!UICONTROL Product Attribute Combination]**&#x200B;を選択します。

   ![買い物かごの価格ルール条件 – 製品属性の組み合わせ](./assets/condition1.png){width="500" zoomable="yes"}

1. 次の行の先頭にある&#x200B;_追加_ （![追加アイコン &#x200B;](../assets/icon-add-green-circle.png)）をクリックし、**[!UICONTROL Product Attribute]**&#x200B;の下のリストで「**[!UICONTROL Category]**」を選択します。

   - 「（**...**） _more_」リンクをクリックして、追加のオプションを表示します。

     ![買い物かごの価格ルール条件 – カテゴリ オプション &#x200B;](./assets/condition3.png){width="600" zoomable="yes"}

   - _Chooser_ （![&#x200B; リストアイコン &#x200B;](../assets/icon-list-chooser.png)）アイコンをクリックすると、使用可能なカテゴリが表示されます。 カテゴリーツリーで、含める各カテゴリのチェックボックスを選択します。 チェックアイコンをクリックして、カテゴリの選択を確定します。

     ![買い物かごの価格ルール条件 – カテゴリ &#x200B;](./assets/condition4.png){width="600" zoomable="yes"}

1. 次の行の先頭にある「_追加_」（![追加アイコン &#x200B;](../assets/icon-add-green-circle.png)）をクリックし、次の操作を行います。

   - **[!UICONTROL Cart Item Attribute]**&#x200B;の下のリストで、**[!UICONTROL Price in cart]**&#x200B;を選択します。

     ![買い物かごの価格ルール条件 – カート項目属性](./assets/condition5.png){width="500"}

   - **is**&#x200B;をクリックし、`equals or greater than`を選択します。

   - 「**...**」をクリックし、条件を満たすためにカート内の価格が必要な金額を入力します。 例えば、`30`と入力します。

     ![買い物かごの価格ルール条件 – カート内の価格](./assets/condition6.png){width="500"}

1. **[!UICONTROL Save and Continue Edit]**&#x200B;をクリックします。

## 手順3: アクションの定義

1. **[!UICONTROL Actions]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![買い物かごの価格ルール アクション &#x200B;](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - **[!UICONTROL Apply]**&#x200B;を`Percent of product price discount`に設定します。

   - **[!UICONTROL Discount Amount]**&#x200B;を入力します。 例えば、10%割引の場合は`10`と入力します。

   - 購入に追加のプロモーションが適用されないようにするには、**[!UICONTROL Discard subsequent rules]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Save and Continue Edit]**&#x200B;をクリックし、必要に応じてルールを完了します。

## 手順4: ラベルを記入してください

チェックアウト時に表示されるラベルを入力するには、カート価格ルール手順の[手順4](price-rules-cart.md)を完了します。

## 手順5：ルールの保存とテスト

{{new-price-rule}}

1. ルールが完了したら、**[!UICONTROL Save Rule]**&#x200B;をクリックします。
1. ルールをテストして、正しく動作することを確認します。
