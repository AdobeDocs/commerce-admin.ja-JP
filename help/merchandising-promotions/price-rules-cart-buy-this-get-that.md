---
title: 買い物かご価格ルールの例 – これを購入するとそれが得られます
description: 買い物かごの価格ルールを使用して、今すぐ購入できるプロモーションを提供する例を確認します。
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# 買い物かご価格ルールの例 – これを購入するとそれが得られます

次の例は、 [買い物かご価格ルール](price-rules-cart.md) の場合 _これを購入すれば、無料で入手できます_ プロモーション。 割引の形式は次のとおりです。

_商品の X 個を購入し、Y 個を無料で取得_

## 手順 1. 買い物かご価格ルールの作成

完了 [手順 1](price-rules-cart.md) ルール情報を完了するための買い物かご価格ルールの手順。

## 手順 2. 条件の定義

完了 [手順 2](price-rules-cart.md) 価格ルールの条件を定義する買い物かご指示の。 これは、ルールに追加できる 2 つの条件の最初の条件であり、ルールがいつトリガーされるかを決定します。 これは、以下の組み合わせに基づくことができます。

- 製品属性
- 製品
- 買い物かご属性
- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）顧客セグメント

空白にした場合、ルールはすべての買い物かごに対してトリガーされます。

![買い物かご価格ルール – 条件](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## 手順 3. アクションの定義

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Actions]** を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Apply]** 対象： `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - を設定 **[!UICONTROL Discount Amount]** 対象： `1`. これは、顧客が無料で受け取る数量です。

   - 条件が満たされたときに適用できる割引の数を制限するには、数値を **[!UICONTROL Maximum Qty Discount is Applied To]** フィールド。 これはこれを使用して計算されます [数式](#maximum-quantity-discount).

   - の場合 **[!UICONTROL Discount Qty Step (Buy X)]**&#x200B;を入力し、割引を受けるために顧客が購入する必要がある数量を入力します。 この例では、顧客は 3 つを購入する必要があります。

   - 購入に他の割引が適用されないようにするには、次のように設定します **[!UICONTROL Discard subsequent rules]** 対象： `Yes`.

   ![買い物かご価格ルール - 3 つ購入すると 1 つ無料](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. ルールを買い物かごの特定の品目にのみ適用するには、条件を完了して、プロモーションに必要な買い物かごの品目や製品属性を記述します。

   次の例では、SKU を使用して、設定可能な製品の関連するすべてのバリエーションにルールを適用します。

   ![買い物かご価格ルール – 買い物かご項目の条件](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. 次を含める **[!UICONTROL Free Shipping]**、を選択 `For matching items only`.

1. クリック **[!UICONTROL Save and Continue Edit]** 必要に応じて、残りのルールを完了します。

## 手順 4. ラベルを完成させる

完了 [手順 4](price-rules-cart.md) （チェックアウト時に表示されるラベルを入力するための買い物かご価格ルールの手順）。

## 手順 5：ルールを保存してテストする

{{new-price-rule}}

1. ルールが完了したら、 **[!UICONTROL Save Rule]**.

1. ルールをテストして、正しく動作することを確認します。

## バリエーション

X を購入 Y を取得無料は、単一のアクションとして処理されます。 _行合計_ 依存関係。 プロモーションを受けるには、すべての項目が同じ SKU に属している必要があります。 例：

カテゴリ A から商品の X 個を購入し、同じ商品の Y 個を無料で取得します。

無料製品をカテゴリ A、B、C に制限するには、アクションを次のように設定します。

次のすべての条件が TRUE の場合：カテゴリは A、B、C のいずれかです

任意のカテゴリ（A、B または C）の空きアイテムを制限し、SKU （D123、E123、F123）から Y を受け取るには、アクションを次のように設定します。

これらの条件がすべて当てはまる場合：SKU は、D123、E123、F123 のいずれかです

## 最大数量割引

次の式を使用して、最大数量割引の正しい値を決定します。

数式= `(X+Y) * (M/Y)`
ここで、
`X` =購入した品目の数
`Y` =空きアイテム数
`M` =許可される空き項目の最大数

例：

5 つ買うと 2 つ無料で、最大 4 つの無料アイテムが許可されます。

    ここで、
    X = 5
    Y = 2
    M = 4
    最大数量割引= （5+2）*（4/2）=（7）*（2）=14

5 つ購入すると 3 つ無料で、最大 9 つの無料アイテムが許可されます。

    ここで、
    X = 5
    Y = 3
    M = 9
    最大数量割引= （5+3）*（9/3）=24

20 個を購入すると、最大 20 個の無料アイテムが許可され、2 個の無料アイテムが得られます。

    ここで、
    X = 20
    Y = 2
    M = 20
    最大数量割引= （20+2）*（20/2）=（22）*（10）=220
