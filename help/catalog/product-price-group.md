---
title: グループ価格
description: グループ価格を使用して、ストア内の顧客グループに基づいて割引品目の価格を設定する方法を説明します。
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# グループ価格

管理者の製品設定を使用して、ストア内の顧客グループに基づいて割引品目の価格を設定できます。 この戦略価格モデルは、と呼ばれます。 _グループ価格_.

買い物客がアカウントにログインしたときに、任意の製品の割引価格を特定の顧客グループのメンバーに提供できます。 顧客グループの価格は、買い物客が価格を簡単に比較し、それに応じて行動できるように、通常の価格と共に製品ページに表示されます。 買い物かごに製品を追加した後、通常の価格が、顧客グループに基づくグループ価格に置き換えられます。

顧客グループの価格設定は、 [階層型価格](product-price-tier.md) 同様の方法で設定されます。 唯一の違いは、顧客のグループ価格の数量が 1 であることです。

![顧客グループの割引](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## グループ価格を使用するメリット

- 卸売業者に適しています

- 割引を活用するために顧客グループをアップグレードするインセンティブ

- ターゲットを絞ったマーケティングキャンペーン

- 常連客に報いを与え、信頼と信頼を築く

## グループ価格の設定

1. 製品を編集モードで開きます。

1. 以下の _[!UICONTROL Price]_「 」フィールドで、「**[!UICONTROL Advanced Pricing]**.

1. Adobe Analytics の _[!UICONTROL Customer Group Price]_セクションで、**[!UICONTROL Add]**.

   ストアに [Adobe Commerce用 B2B](../b2b/introduction.md) および [共有カタログ](../b2b/catalog-shared.md) 有効、このセクションにラベルが付いています _[!UICONTROL Catalog and Tier Price]_.

   ![高度な価格](./assets/product-price-group.png){width="600" zoomable="yes"}

1. グループ価格を設定します。

   - マルチサイトインストールの場合は、 **[!UICONTROL Website]** グループ価格が適用される場所

   - を選択します。 **[!UICONTROL Customer Group]** それは割引を受けることです。

   - を入力します。 **[!UICONTROL Quantity]** / `1`.

   - の場合 **[!UICONTROL Price]**、価格のタイプと金額を設定します。

      - `Fixed`  — 割引製品の価格を入力します。

      - `Discount`  — 割引価格を製品価格に対する割合として入力します。

     ![顧客グループの価格](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. 別のグループ価格を追加するには、 **[!UICONTROL Add]** 前の手順を繰り返します。

1. 完了したら、「 **[!UICONTROL Done]** その後 **[!UICONTROL Save]**.

>[!NOTE]
>
>The **_最終_** 製品価格は **_最小_** 関連する価格。次の式を使用します。 <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定価格_** 製品のカスタマイズ可能なオプションは次のとおりです。 _not_ グループ価格、Tier Price、特別価格、またはカタログ価格のルールの影響を受けます。
