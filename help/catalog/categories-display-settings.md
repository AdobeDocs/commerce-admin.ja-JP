---
title: カテゴリ – 表示設定
description: '[!UICONTROL Display]設定を使用して、カテゴリーページに表示されるコンテンツ要素と、製品が表示される順序を定義する方法について説明します。'
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/t5UfvWvJ7R-kZb5kyMwpzwI2gfs3x3g1amlfWzQcAsw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# カテゴリ – 表示設定

表示設定は、カテゴリーページに表示されるコンテンツ要素と、製品が表示される順序を決定します。 CMS ブロックを有効にし、カテゴリのアンカーステータスを設定し、_[!UICONTROL Display Settings]_&#x200B;タブから並べ替えオプションを管理できます。 ストアフロントにカテゴリを反映する方法の例については、[&#x200B; カタログナビゲーション &#x200B;](navigation.md)を参照してください。

![&#x200B; カテゴリの表示設定](./assets/category-display-settings.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Display Mode] | カテゴリーページに表示されるコンテンツ要素を指定します。 オプション：`Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | `Yes`に設定すると、カテゴリに明示的に追加されていない場合でも、カテゴリ内のサブカテゴリの製品を表示し、階層化されたナビゲーションで&#x200B;_[!UICONTROL filter by attribute]_&#x200B;セクションの表示を有効にします。 オプション：`Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | （必須）デフォルト値は`Position`、`Name`、`Price`です。 並べ替えオプションをカスタマイズするには、**[!UICONTROL Use All Available Attributes]** チェックボックスの選択を解除し、使用する属性を選択します。 必要に応じて属性を定義し、追加できます。 この設定は、[!DNL Live Search] [製品リストページ ウィジェット &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/live-search/live-search-storefront/plp-styling)には適用されません。 |
| [!UICONTROL Default Product Listing Sort By] | （必須）デフォルトの&#x200B;_[!UICONTROL Sort By]_&#x200B;オプションを定義するには、「**[!UICONTROL Use Config Settings]**」チェックボックスの選択を解除し、属性を選択します。 この設定は、[!DNL Live Search] [製品リストページ ウィジェット &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/live-search/live-search-storefront/plp-styling)には適用されません。 |
| [!UICONTROL Layered Navigation Price Step] | デフォルトでは、Commerceには、リスト内の商品に応じて、価格帯が10、100、1000の増分で表示されます。 価格ステップの範囲を変更するには、**[!UICONTROL Use Config Settings]** チェックボックスの選択を解除します。 |

{style="table-layout:auto"}
