---
title: 複数のSKUを含むカタログ価格ルール
description: 単一のカタログ価格ルールを複数のSKUに適用する方法について説明します。
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/nChe-8VA4V0nrC46PbeKyh7DB4Ta-0lpcezMV3uHEw0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 367
ht-degree: 0%

---

# 複数のSKUを含むカタログ価格ルール

単一のカタログ価格ルールを複数のSKUに適用できるため、商品、ブランド、カテゴリーに基づいた様々なプロモーションを作成できます。 このルールを作成する場合は、選択したSKUに一致する条件を設定する必要があります。 ルールを作成する際に、グリッドからSKUを簡単に参照して選択できます。

## 手順1: 製品属性のストアフロントプロパティを確認します

開始する前に、`sku`属性の[&#x200B; ストアフロントのプロパティ &#x200B;](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties)が`Use in Promo Rules`に設定されていることを確認してください。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**&#x200B;に移動します。

1. _[!UICONTROL Attribute Code]_&#x200B;列の上部にある検索フィルターで、`sku`と入力し、**[!UICONTROL Search]**&#x200B;をクリックします。

1. クリックして、`sku`属性を編集モードで開きます。

1. 左側のパネルで、**[!UICONTROL Storefront Properties]**&#x200B;をクリックし、**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;が`Yes`に設定されていることを確認します。

1. プロパティの値を変更した場合は、**[!UICONTROL Save Attribute]**&#x200B;をクリックします。

## 手順2: 価格ルールを複数のSKUに適用する

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**&#x200B;に移動します。

1. 次のいずれかの操作を行います。

   - 指示に従って、[&#x200B; カタログ価格ルール &#x200B;](price-rules-catalog.md)を作成します。
   - 既存のカタログ価格ルールを開きます。

1. **[!UICONTROL Conditions]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - 最初の行で、最初のパラメーターを`ANY`に設定します。

     ![&#x200B; カタログ価格ルール条件 – ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - 次の行の先頭にある&#x200B;_追加_ （![追加アイコン &#x200B;](../assets/icon-add-green-circle.png)）をクリックし、**[!UICONTROL Product Attribute]**&#x200B;の下のリストで「`SKU`」をクリックします。

     ![&#x200B; カタログ価格ルール条件 – SKUは](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}のいずれかです

   - 比較のために、オプションがあります。 SKUのリストから少なくとも1つを見つける場合は、`select is one of`。 すべて適用する必要があるSKUのグループを見つける場合は、`is`を選択します。 `is one of`を選択することをお勧めします。

     ![&#x200B; カタログ価格ルール条件 – SKUは](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}のいずれかです

   - 条件を完了するには、詳細（**...**）リンクをクリックし、利用可能な製品のリストの&#x200B;_Chooser_ （![&#x200B; リストアイコン &#x200B;](../assets/icon-list-chooser.png)）アイコンをクリックします。

     ![&#x200B; カタログ価格ルール条件 – 複数のSKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - 参照、フィルター、または検索して、追加するSKUを見つけます。 リストで、含める各製品のチェックボックスを選択します。

   - **[!UICONTROL Save and Apply]**&#x200B;をクリックして、条件にSKUを追加します。

     ![&#x200B; カタログ価格ルール条件 – 複数のSKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. 条件が満たされたときに実行される[&#x200B; アクション &#x200B;](price-rules-catalog.md)を含むルールを完了します。

1. ルールが完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

{{new-price-rule}}
