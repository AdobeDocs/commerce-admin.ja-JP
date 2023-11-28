---
title: 買い物かごの価格ルールの例 — 最小購入による割引
description: 買い物かごの価格ルールを使用して、最小購入価格での割引をオファーする例を確認します。
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# 買い物かごの価格ルールの例 — 最小購入による割引

買い物かごの価格ルールを使用して、最小購入に基づいて割引率をオファーできます。 次の例では、特定のカテゴリの$200.00 を超えるすべての購入に 25%の割引が適用されています。 割引の形式は次のとおりです。

$Z ドルを超えるすべての Y（カテゴリ）の X%オフ

## 手順 1. 買い物かごルールの作成

基本の [instructions](price-rules-cart.md) をクリックして、買い物かごルールを作成します。

## 手順 2. 条件の定義

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Conditions]** 」セクションに入力します。

1. クリック _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) をクリックし、を選択します。 **[!UICONTROL Product Attribute Combination]**.

   ![買い物かごの価格ルール条件 — 製品属性の組み合わせ](./assets/condition1.png){width="500" zoomable="yes"}

1. クリック _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) を次の行の先頭に配置し、リスト内の **[!UICONTROL Product Attribute]**&#x200B;を選択します。 **[!UICONTROL Category]**.

   - (**...**) _その他_ リンクをクリックして、追加のオプションを表示します。

     ![買い物かご価格ルールの条件 — カテゴリオプション](./assets/condition3.png){width="600" zoomable="yes"}

   - 次をクリック： _選択_ (![リストアイコン](../assets/icon-list-chooser.png)) アイコンをクリックして、使用可能なカテゴリを表示します。 カテゴリツリーで、含める各カテゴリのチェックボックスをオンにします。 チェックアイコンをクリックして、カテゴリの選択を受け入れます。

     ![買い物かご価格ルールの条件 — カテゴリ](./assets/condition4.png){width="600" zoomable="yes"}

1. クリック _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) を次の行の先頭に配置し、次の操作を実行します。

   - の下のリストで **[!UICONTROL Cart Item Attribute]**&#x200B;を選択します。 **[!UICONTROL Price in cart]**.

     ![買い物かご価格ルールの条件 — 買い物かごの品目属性](./assets/condition5.png){width="500"}

   - クリック **次に該当** を選択します。 `equals or greater than`.

   - クリック **...** 「買い物かご内の価格」が条件を満たすために必要な金額を入力します。 例えば、 `30`.

     ![買い物かごの価格ルール条件 — 買い物かご内の価格](./assets/condition6.png){width="500"}

1. クリック **[!UICONTROL Save and Continue Edit]**.

## 手順 3. アクションの定義

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Actions]** 」セクションで次の操作を実行します。

   ![買い物かご価格ルールのアクション](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Apply]** から `Percent of product price discount`.

   - 次を入力します。 **[!UICONTROL Discount Amount]**. 例えば、 `10` 10%の割引を受ける場合。

   - 追加のプロモーションが購入に適用されないようにするには、 **[!UICONTROL Discard subsequent rules]** から `Yes`.

1. クリック **[!UICONTROL Save and Continue Edit]** 必要に応じて、ルールを完了します。

## 手順 4. ラベルを完成させます。

完了 [手順 4](price-rules-cart.md) を使用して、チェックアウト時に表示されるラベルを入力します。

## 手順 5：ルールを保存してテストする

{{new-price-rule}}

1. ルールが完了したら、「 **[!UICONTROL Save Rule]**.

1. ルールをテストして、正しく動作することを確認します。
