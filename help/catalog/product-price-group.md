---
title: グループ価格
description: グループ価格を使用して、ストア内の顧客グループに基づいて割引商品の価格を設定する方法を説明します。
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
TQID: https://experienceleague.adobe.com/OCeX5pLtUzWdwOW5W8qpI4DCeab2PTAVi5xF8HUr91A
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 0%

---

# グループ価格

管理画面の製品設定を使用して、ストアの顧客グループに基づいて割引商品の価格を設定できます。 この戦略的価格モデルは&#x200B;_グループ価格_&#x200B;と呼ばれます。

買い物客がアカウントにログインすると、特定の顧客グループのメンバーに商品の割引価格を提供できます。 商品ページには、お客様グループの価格と通常価格が表示されるので、買い物客は価格を簡単に比較し、それに応じて行動することができます。 商品をカートに入れた後、通常価格は、顧客グループに基づくグループ価格に置き換えられます。

顧客グループの価格は[階層価格](product-price-tier.md)のコンポーネントであり、同様の方法で設定されます。 唯一の違いは、顧客グループの価格の数量が1であることです。

![顧客グループ割引](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## グループ価格設定を利用する利点

- 卸売バイヤーに適しています

- 顧客グループをアップグレードして割引を活用するインセンティブ

- ターゲットマーケティング施策

- ロイヤルティの高い顧客への報酬を提供して、信頼と信頼性を向上

## グループ価格の設定

1. 製品を編集モードで開きます。

1. _[!UICONTROL Price]_フィールドの下にある「**[!UICONTROL Advanced Pricing]**」をクリックします。

1. _[!UICONTROL Customer Group Price]_セクションで、**[!UICONTROL Add]**をクリックします。

   ストアに[Adobe Commerce B2B](../b2b/introduction.md)が含まれ、[共有カタログ ](../b2b/catalog-shared.md)が有効になっている場合、このセクションには&#x200B;_[!UICONTROL Catalog and Tier Price]_というラベルが付けられます。

   ![詳細な価格設定](./assets/product-price-group.png){width="600" zoomable="yes"}

1. グループ価格を設定します。

   - マルチサイト インストールの場合は、グループ価格が適用される&#x200B;**[!UICONTROL Website]**&#x200B;を選択します。

   - 割引を受け取る&#x200B;**[!UICONTROL Customer Group]**&#x200B;を選択します。

   - `1`の&#x200B;**[!UICONTROL Quantity]**&#x200B;を入力してください。

   - **[!UICONTROL Price]**&#x200B;の場合、価格タイプと金額を設定します。

      - `Fixed` – 割引商品価格を入力します。

      - `Discount` – 割引価格を製品価格に対する割合として入力します。

     ![顧客グループの価格](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. 別のグループ価格を追加するには、**[!UICONTROL Add]**&#x200B;をクリックして、前の手順を繰り返します。

1. 完了したら、**[!UICONTROL Done]**&#x200B;をクリックし、**[!UICONTROL Save]**&#x200B;をクリックします。

>[!NOTE]
>
>**_final_**&#x200B;の製品価格は、次の式を使用して&#x200B;**_minimum_**&#x200B;の関連価格として計算されます：<br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定価格_**&#x200B;製品のカスタマイズ可能なオプションは、グループ価格、階層価格、特別価格、カタログ価格のルールの影響を受ける&#x200B;_not_&#x200B;です。
