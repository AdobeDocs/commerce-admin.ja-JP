---
title: カテゴリ – 表示設定
description: の使用について説明します [!UICONTROL Display] カテゴリページに表示するコンテンツ要素と製品の表示順を定義する設定。
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: a47e744cf4cc5163ca2ba0718ccb78eb65a7d404
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# カテゴリ – 表示設定

表示設定は、カテゴリページに表示するコンテンツ要素と、製品の表示順を決定します。 から CMS ブロックの有効化、カテゴリのアンカーステータスの設定、並べ替えオプションの管理を行うことができます _[!UICONTROL Display Settings]_タブ。 カテゴリがストアフロントにどのように反映されるかについては、を参照してください。 [カタログナビゲーション](navigation.md).

![カテゴリの表示設定](./assets/category-display-settings.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Display Mode] | カテゴリページに表示されるコンテンツ要素を決定します。 オプション： `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | に設定されている場合 `Yes`は、カテゴリに明示的に追加されていない場合でも、カテゴリのサブカテゴリの製品を表示し、の表示を有効にします _[!UICONTROL filter by attribute]_セクションのレイヤー化されたナビゲーション。 オプション： `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | （必須） デフォルト値は次のとおりです `Position`, `Name`、および `Price`. 並べ替えオプションをカスタマイズするには、 **[!UICONTROL Use All Available Attributes]** チェックボックスをオンにして、使用する属性を選択します。 必要に応じて、属性を定義および追加できます。 この設定は、 [!DNL Live Search] [製品一覧ページウィジェット](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | （必須） デフォルトを定義します _[!UICONTROL Sort By]_オプションで、**[!UICONTROL Use Config Settings]**チェックボックスをオンにして、属性を選択します。 この設定は、 [!DNL Live Search] [製品一覧ページウィジェット](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | デフォルトでは、Commerceは、リスト内の商品に応じて、10、100、1000 の増分で価格範囲を表示します。 価格ステップ範囲を変更するには、 **[!UICONTROL Use Config Settings]** チェックボックス。 |

{style="table-layout:auto"}
