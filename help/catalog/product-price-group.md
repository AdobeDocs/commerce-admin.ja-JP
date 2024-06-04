---
title: グループの価格
description: グループ価格を使用して、ストアの顧客グループに基づいて割引品目の価格を設定する方法を説明します。
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# グループの価格

管理者の製品設定を使用して、ストアの顧客グループに基づいて割引品目の価格を設定できます。 この戦略的価格モデルはと呼ばれます _グループ価格_.

買い物客がアカウントにログインしたときに、特定の顧客グループのメンバーに製品の割引価格を提供できます。 顧客グループ価格は、通常の価格と共に製品ページに表示されるため、買い物客は価格を簡単に比較し、それに応じて行動することができます。 買い物かごに製品を追加した後、通常の価格は、顧客グループに基づくグループ価格に置き換えられます。

顧客グループの価格は、次の要素で構成されます [階層化された価格](product-price-tier.md) と同様の方法で設定されます。 唯一の違いは、顧客グループ価格の数量が 1 であることです。

![顧客グループ割引](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## グループ価格を使用するメリット

- 卸売業者に適しています

- 顧客グループをアップグレードしてディスカウントを利用できるようにするためのインセンティブ

- ターゲットマーケティングキャンペーン

- 常連客に報いることで信頼と信頼を築く

## グループ価格を設定します

1. 製品を編集モードで開きます。

1. の下 _[!UICONTROL Price]_フィールド、クリック&#x200B;**[!UICONTROL Advanced Pricing]**.

1. が含まれる _[!UICONTROL Customer Group Price]_セクションで、をクリック&#x200B;**[!UICONTROL Add]**.

   ストアに次が含まれる場合 [Adobe Commerce B2B](../b2b/introduction.md) および次を持つ [共有カタログ](../b2b/catalog-shared.md) 有効にすると、このセクションにラベルが付けられます _[!UICONTROL Catalog and Tier Price]_.

   ![詳細価格](./assets/product-price-group.png){width="600" zoomable="yes"}

1. グループ価格を設定します。

   - マルチサイトインストールの場合は、 **[!UICONTROL Website]** グループ価格が適用される場合。

   - を選択します。 **[!UICONTROL Customer Group]** それは割引を受けることです。

   - を入力 **[!UICONTROL Quantity]** 件中 `1`.

   - の場合 **[!UICONTROL Price]**&#x200B;で、価格のタイプと金額を設定します。

      - `Fixed`  – 割引製品価格を入力します。

      - `Discount`  – 製品価格に対するパーセンテージとして割引価格を入力します。

     ![顧客グループ価格](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. 別のグループ価格を追加するには、をクリックします **[!UICONTROL Add]** 前の手順を繰り返します。

1. 完了したら、 **[!UICONTROL Done]** その後 **[!UICONTROL Save]**.

>[!NOTE]
>
>この **_final_** 製品価格は次のように計算されます **_minimum_** 次の算式を使用した関連価格 <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定価格_** 製品のカスタマイズ可能なオプション _ではない_ グループ価格、階層価格、特別価格、カタログ価格ルールの影響を受けます。
