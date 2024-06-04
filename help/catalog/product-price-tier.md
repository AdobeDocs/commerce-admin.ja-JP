---
title: 階層の価格
description: 階層価格を使用して、製品リストまたは製品ページから数量割引を提供する方法を説明します。
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# 階層の価格

階層価格を使用すると、ストアフロントの商品リストまたは商品ページから数量割引を提供できます。 割引は、特定のストア表示、顧客グループ、共有カタログに適用できます。

更新する製品が多数ある場合は、階層価格の変更を個別に入力するのではなく、インポートするのが最も効率的です。 詳しくは、を参照してください [階層の価格のインポート](../systems/data-import-price-tier.md).

![ストアフロント製品ページの階層価格](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

製品ページで数量割引が計算され、次のようなメッセージが表示されます。

`Buy 6 for $5.95 each and save 15%`

ストアフロントの価格は、高い数量から低い数量まで優先されます。 数量の階層価格がある場合 `5` と 1 つ `10`顧客が 5、6、7、8 または 9 個の品目を買い物かごに追加すると、顧客は数量の割引価格を受け取ります `5` 層 顧客が 10 番目の品目を追加すると、数量に指定された割引価格 `10` 階層は、次の量の階層よりも優先されます `5`、およびの割引価格 `10` が適用されます。

## 製品の価格階層の追加

1. 製品を編集モードで開きます。

1. の下 _[!UICONTROL Price]_フィールド、クリック&#x200B;**[!UICONTROL Advanced Pricing]**.

1. が含まれる _[!UICONTROL Tier Price]_セクションで、をクリック&#x200B;**[!UICONTROL Add]**.

   複数の価格の階層を作成する場合は、 **[!UICONTROL Add]** 追加のレベルごとに、すべての層を同時に作業できます。 グループ内の各層の web サイトと顧客グループまたは共有カタログの割り当ては同じですが、数量と価格が異なります。

## 価格層の設定

1. ストアに複数の web サイトがある場合は、 **[!UICONTROL Website]** 対象となる層の価格。

1. 必要に応じて、を選択して価格レベルの可用性を制限します。 **[!UICONTROL Customer Group]** または **[!UICONTROL Shared Catalog]** （![Adobe Commerce B2B](../assets/b2b.svg) で利用可能 [Adobe Commerce B2B](./b2b/../introduction.md) のみ）。

1. の場合 **[!UICONTROL Qty]**：割引を受けるために注文する必要がある数量を入力します。

   - **メソッド 1:** 固定金額として価格を入力してください

     を設定 **[!UICONTROL Price]** 対象： `Fixed` その階層の 1 単位の調整価格を入力します。

     ![固定金額としての階層価格](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **メソッド 2:** パーセンテージで価格を入力してください

     を設定 **[!UICONTROL Price]** 対象： `Discount` そして、割引価格を製品の基本価格に対するパーセンテージとして入力します。

     例えば、15% の割引の場合は、数値を入力します `15`. （価格は、次のような 2 桁の小数点以下の桁数で保存されます。 `15.00`.）

     >[!NOTE]
     >
     >割引価格を取得するには、で定義された値に対して、定義された割合を計算します。 _[!UICONTROL Price]_ フィールド （ではない） _[!UICONTROL Special Price]_ フィールド。

     ![階層価格（割合）](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## 価格設定の完了

1. 別の web サイトまたは顧客グループに別の階層料金セットを追加するには、前の手順を繰り返します。

1. 完了したら、 **[!UICONTROL Done]** その後 **[!UICONTROL Save]**.

>[!NOTE]
>
>この **_final_** 製品価格は次のように計算されます **_minimum_** 次の算式を使用した関連価格 <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定価格_** 製品のカスタマイズ可能なオプション _ではない_ グループ価格、階層価格、特別価格、カタログ価格ルールの影響を受けます。
