---
title: 買い物かごの価格ルールの例 — これを購入して取得
description: 買い物かごの価格ルールを使用して、購入 —this-get-that プロモーションをオファーする例を確認します。
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# 買い物かごの価格ルールの例 — これを購入して取得

この例では、 [買い物かごの価格ルール](price-rules-cart.md) の _これを買って、無料で手に入れる_ 昇格。 割引の形式は次のとおりです。

_X 個の製品を購入し、Y 個の数量を無料で取得_

## 手順 1. 買い物かごの価格ルールの作成

完了 [手順 1](price-rules-cart.md) 買い物かご価格ルールの指示を参照して、ルール情報を入力します。

## 手順 2. 条件の定義

完了 [手順 2](price-rules-cart.md) 買い物かご指示の情報を確認し、価格ルールの条件を定義します。 これは、ルールに追加できる 2 つの条件の 1 つ目で、ルールをトリガーするタイミングを決定します。 次の組み合わせに基づくことができます。

- 製品属性
- 製品
- 買い物かごの属性
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 顧客セグメント

空白の場合、ルールは買い物かごごとにトリガーされます。

![買い物かごの価格ルール — 条件](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## 手順 3. アクションの定義

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Actions]** 」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Apply]** から `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - 設定 **[!UICONTROL Discount Amount]** から `1`. これは、顧客が無料で受け取る数量です。

   - 条件が満たされたときに適用できる割引の数を制限するには、 **[!UICONTROL Maximum Qty Discount is Applied To]** フィールドに入力します。 これは、 [式](#maximum-quantity-discount).

   - の場合 **[!UICONTROL Discount Qty Step (Buy X)]**&#x200B;の場合は、顧客が購入する必要がある割引の数量を入力します。 この例では、顧客は 3 回購入する必要があります。

   - その他の割引が購入に適用されないようにするには、 **[!UICONTROL Discard subsequent rules]** から `Yes`.

   ![買い物かごの価格ルール — 購入 3 は無料で 1 を取得](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. ルールをカート内の特定の品目にのみ適用するには、条件を満たして、プロモーションに必要な買い物かご品目や製品属性を記述します。

   次の例では、SKU を使用して、設定可能な製品の関連するすべてのバリエーションにルールを適用しています。

   ![買い物かごの価格ルール — 買い物かごの品目の条件](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. 含める **[!UICONTROL Free Shipping]**&#x200B;を選択します。 `For matching items only`.

1. クリック **[!UICONTROL Save and Continue Edit]** 必要に応じて、残りのルールを完了します。

## 手順 4. ラベルを入力

完了 [手順 4](price-rules-cart.md) を使用して、チェックアウト時に表示されるラベルを入力します。

## 手順 5：ルールを保存してテストする

{{new-price-rule}}

1. ルールが完了したら、「 **[!UICONTROL Save Rule]**.

1. ルールをテストして、正しく動作することを確認します。

## バリエーション

Buy X Get Y Free は、 _行の合計_ 依存関係。 プロモーションの条件を満たすには、すべての項目が同じ SKU に属している必要があります。 例：

カテゴリ A から X 個の製品を購入し、同じ製品の Y 個の数量を無料で取得します。

無料製品をカテゴリ A、B、C に限定するには、アクションを次のように設定します。

次の条件のすべてが TRUE の場合：カテゴリが A、B、C のいずれか

任意のカテゴリ（A、B または C）の自由品目を制限し、SKU（D123、E123 または F123）から Y を受け取るには、次のようにアクションを設定します。

これらの条件がすべて TRUE の場合：SKU が D123、E123、F123 のいずれか

## 最大数量割引

次の式を使用して、最大数量割引の正しい値を決定します。

数式= `(X+Y) * (M/Y)`
ここで、
`X` =購入した品目の数
`Y` =空きアイテムの数
`M` =許可される最大空き項目数

例：

5 を購入し、最大 4 つの無料アイテムを許可して 2 つの無料を得る。

    ここで、
    X = 5
    Y = 2
    M = 4
    最大数量割引= (5+2)*(4/2)=(7)*(2)=14

5 を購入し、最大 9 つの無料アイテムを許可して 3 つの無料を得る。

    ここで、
    X = 5
    Y = 3
    M = 9
    最大数量割引= (5+3)*(9/3)=24

20 を購入し、最大 20 個の無料アイテムを許可して 2 つの無料を得る。

    ここで、
    X = 20
    Y = 2
    M = 20
    最大数量割引= (20+2)*(20/2)=(22)*(10)=220
