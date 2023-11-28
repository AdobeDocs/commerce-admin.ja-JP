---
title: 価格帯
description: 階層価格を使用して、製品リストまたは製品ページから数量の割引を提供する方法を説明します。
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# 価格帯

層価格を使用すると、ストアフロントの製品リストまたは製品ページから数量の割引を提供できます。 割引は、特定のストア表示、顧客グループ、または共有カタログに適用できます。

更新する製品が多数ある場合は、階層価格の変更をインポートする方が、個別に入力するよりも効率的です。 詳しくは、 [輸入階層価格](../systems/data-import-price-tier.md).

![ストアフロント製品ページの価格を設定](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

製品ページでは、数量の割引が計算され、次のようなメッセージが表示されます。

`Buy 6 for $5.95 each and save 15%`

店頭の価格は、最も高い数量から最も低い数量の順に優先されます。 数量の段階価格がある場合 `5` そして 1 つは `10`顧客が買い物かごに 5、6、7、8、9 品目を追加すると、その顧客は数量の割引価格を受け取ります `5` 層。 顧客が 10 番目の品目を追加すると、数量に指定された割引価格 `10` ～の数量の層に取って代わる層 `5`、および割引価格 `10` 適用されます。

## 製品の価格帯を追加

1. 製品を編集モードで開きます。

1. 以下の _[!UICONTROL Price]_「 」フィールドで、「**[!UICONTROL Advanced Pricing]**.

1. Adobe Analytics の _[!UICONTROL Tier Price]_セクションで、**[!UICONTROL Add]**.

   複数の価格帯を作成する場合は、 **[!UICONTROL Add]** を追加するごとに、すべての層を同時に作業できます。 グループ内の各層には、同じ Web サイトと顧客グループまたは共有カタログの割り当てがありますが、数量と価格は異なります。

## 価格帯の設定

1. ストアに複数の Web サイトがある場合は、 **[!UICONTROL Website]** 階層価格が適用される対象となります。

1. 必要に応じて、 **[!UICONTROL Customer Group]** または **[!UICONTROL Shared Catalog]** (![Adobe Commerce用 B2B](../assets/b2b.svg) 次で使用可能： [Adobe Commerce用 B2B](./b2b/../introduction.md) のみ )。

1. の場合 **[!UICONTROL Qty]**」に、割引を受け取るために注文する必要がある数量を入力します。

   - **メソッド 1:** 価格を固定金額として入力します

     設定 **[!UICONTROL Price]** から `Fixed` そして、その階層の 1 ユニットに対する調整済みの価格を入力します。

     ![固定金額としての階層価格](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **方法 2:** 価格をパーセンテージとして入力します

     設定 **[!UICONTROL Price]** から `Discount` 割引価格を製品の基本価格からの割合で入力します。

     例えば、15%の割引の場合は、数値を入力します。 `15`. ( 価格は、 `15.00`.)

     >[!NOTE]
     >
     >割引価格を取得するために、定義された割合が、 _[!UICONTROL Price]_ フィールド（ではない） _[!UICONTROL Special Price]_ フィールドに入力します。

     ![価格をパーセンテージで表した階層](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## 価格設定の完了

1. 別の Web サイトや顧客グループに対して別の階層価格セットを追加するには、上記の手順を繰り返します。

1. 完了したら、「 **[!UICONTROL Done]** その後 **[!UICONTROL Save]**.

>[!NOTE]
>
>The **_最終_** 製品価格は **_最小_** 関連する価格。次の式を使用します。 <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定価格_** 製品のカスタマイズ可能なオプションは次のとおりです。 _not_ グループ価格、Tier Price、特別価格、またはカタログ価格のルールの影響を受けます。
