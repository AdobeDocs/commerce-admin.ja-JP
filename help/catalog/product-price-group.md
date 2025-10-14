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

管理者の製品設定を使用して、ストアの顧客グループに基づいて割引品目の価格を設定できます。 この戦略的な価格モデルは _グループ価格_ と呼ばれます。

買い物客がアカウントにログインしたときに、特定の顧客グループのメンバーに製品の割引価格を提供できます。 顧客グループ価格は、通常の価格と共に製品ページに表示されるため、買い物客は価格を簡単に比較し、それに応じて行動することができます。 買い物かごに製品を追加した後、通常の価格は、顧客グループに基づくグループ価格に置き換えられます。

顧客グループ向けの価格は、[&#x200B; 階層化された価格 &#x200B;](product-price-tier.md) のコンポーネントであり、同様の方法で設定されます。 唯一の違いは、顧客グループ価格の数量が 1 であることです。

![&#x200B; 顧客グループ割引 &#x200B;](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## グループ価格を使用するメリット

- 卸売業者に適しています

- 顧客グループをアップグレードしてディスカウントを利用できるようにするためのインセンティブ

- ターゲットマーケティングキャンペーン

- 常連客に報いることで信頼と信頼を築く

## グループ価格を設定します

1. 製品を編集モードで開きます。

1. 「_[!UICONTROL Price]_」フィールドの下にある「**[!UICONTROL Advanced Pricing]**」をクリックします。

1. 「_[!UICONTROL Customer Group Price]_」セクションで、「**[!UICONTROL Add]**」をクリックします。

   ストアに [Adobe Commerce B2B](../b2b/introduction.md) が含まれ、[shared catalogs](../b2b/catalog-shared.md) が有効になっている場合、このセクションには _[!UICONTROL Catalog and Tier Price]_&#x200B;というラベルが付けられます。

   ![Advanced Pricing](./assets/product-price-group.png){width="600" zoomable="yes"}

1. グループ価格を設定します。

   - マルチサイトインストールの場合は、グループ価格が適用される **[!UICONTROL Website]** を選択します。

   - 割引を受ける **[!UICONTROL Customer Group]** を選択してください。

   - `1` の **[!UICONTROL Quantity]** を入力します。

   - **[!UICONTROL Price]** の場合は、価格タイプと金額を設定します。

      - `Fixed` – 割引製品価格を入力します。

      - `Discount` – 製品価格に対するパーセンテージとして割引価格を入力します。

     ![&#x200B; 顧客グループ価格 &#x200B;](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. 別のグループ価格を追加するには、「**[!UICONTROL Add]**」をクリックして前の手順を繰り返します。

1. 完了したら、「**[!UICONTROL Done]**」をクリックし、次に「**[!UICONTROL Save]**」をクリックします。

>[!NOTE]
>
>**_最終_** 製品価格は、次の式を使用して **_最小_** 関連価格として計算されます。<br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定価格_** 製品カスタマイズ可能なオプションは、グループ価格、階層価格、特別価格、カタログ価格ルールの影響を _受けません_。
