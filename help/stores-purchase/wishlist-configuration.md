---
title: ウィッシュリストの設定
description: ストア顧客のウィッシュリスト機能を設定する方法について説明します。
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/pSVYKFjf0Iz-zJ7fw1HxraizUwLYj7l1ykIWtnbI30w
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 537
ht-degree: 0%

---

# ウィッシュリストの設定

ウィッシュリスト設定では、ウィッシュリストを有効にし、ウィッシュリストの共有時に使用されるメールテンプレートとメールメッセージの送信者を決定します。

## ウィッシュリスト機能を有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Wish List]**&#x200B;を選択します。

1. **[!UICONTROL General Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![お客様の設定 – ウィッシュリストの一般設定](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enabled]**&#x200B;を`Yes`に切り替えると、ストアのウィッシュリストモジュールがアクティブになります。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）切り替え&#x200B;**[!UICONTROL Enable Multiple Wish Lists]**&#x200B;から`Yes`に切り替えると、複数のウィッシュリストを作成および管理できます。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）お客様がアカウントに関連付けることができるウィッシュリストの数を制限するには、**[!UICONTROL Number of Multiple Wish Lists]**&#x200B;の値を入力します。

   - **[!UICONTROL Show in Sidebar]**&#x200B;を`Yes`に切り替えると、サイドバーにウィッシュリストが表示されます。

1. **[!UICONTROL Share Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![お客様の設定 – ウィッシュリスト共有オプション ](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - メッセージの送信者として表示されるストア連絡先に&#x200B;**[!UICONTROL Email Sender]**&#x200B;を設定します。 オプション：一般連絡先、営業担当者、カスタマーサポート、カスタムメール。

   - お客様がウィッシュリストを共有する際に使用する&#x200B;**[!UICONTROL Email Template]**&#x200B;を設定します。

   - 顧客が送信できるメールの合計数を制限するには、**[!UICONTROL Max Emails Allowed to be Sent]**&#x200B;値を入力します。 デフォルトは10で、許可される最大値は10,000です。

   - メッセージのサイズを制限するには、**[!UICONTROL Email Text Length Limit]**&#x200B;の値を入力します。 デフォルトは255です。

1. **[!UICONTROL My Wish List Link]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、**[!UICONTROL Display Wish List Summary]**&#x200B;を次のいずれかに設定します。

   - `Display number of items in wish list`
   - `Display item quantities`

   ![お客様の設定 – ウィッシュリスト表示](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## ウィッシュリスト検索を追加

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

公開されているウィッシュリストは、ウィッシュリスト検索[ ウィジェット ](../content-design/widgets.md)を使用して検索できます。 ウィジェットを使用すると、お客様はウィッシュリスト所有者の名前またはメールアドレスで検索できます。 店舗のお客様は、他のお客様に属するウィッシュリストを検索したり、それらを表示して商品を注文したり、自分のウィッシュリストに商品を追加したりできます。 他のお客様が公開のウィッシュリストから購入したアイテムは、元のウィッシュリストから削除されません。 _ウィッシュリスト検索_ ウィジェットをストアの任意のページに追加すると、顧客が友人や家族のウィッシュリストを簡単に検索できるようになります。

![ ストアフロントの例 – ウィッシュリスト検索](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**に移動します。

1. 右上隅の「**[!UICONTROL Add Widget]**」をクリックします。

1. 「_[!UICONTROL Settings]_」タブで、次の操作を行います。

   - **[!UICONTROL Type]**&#x200B;を`Wish List Search`に設定します。

   - ウィッシュリストが追加されるストアのテーマに&#x200B;**[!UICONTROL Design Theme]**&#x200B;を設定します。

   - **[!UICONTROL Continue]**&#x200B;をクリックします。

1. _[!UICONTROL Storefront Properties]_を完了：

   - **[!UICONTROL Widget Title]**&#x200B;を入力します。

   - ウィジェットを使用するビューまたはweb サイトに&#x200B;**[!UICONTROL Assign to Store Views]**&#x200B;を設定します。

   - **[!UICONTROL Sort Order]**&#x200B;に数値を入力して、ウィジェットのコンテナ内での配置を決定します。

     `0` = first （デフォルト）、`1` = second、`2` = thirdなど。

1. _[!UICONTROL Layout Updates]_セクションで、**[!UICONTROL Add Layout Update]**をクリックし、**[!UICONTROL Display on]**を次のいずれかに設定します。

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. **[!UICONTROL Container]** リストで、配置するページレイアウトの領域を選択します。

   ![ ウィッシュリスト検索ウィジェット – レイアウト ](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. 左側のパネルで、**[!UICONTROL Widget Options]**&#x200B;を選択します。

1. **[!UICONTROL Quick Search Form Types]**&#x200B;を次のいずれかに設定します：

   - `All Forms` – お客様は、使用可能なすべてのパラメーターで検索できます。
   - `Owner Name` – お客様は、所有者の名前でウィッシュリストを検索できます。
   - `Owner Email` – お客様は、所有者の電子メールアドレスでウィッシュリストを検索できます。

   >[!NOTE]
   >
   >発送先住所はウィッシュリストに含まれていません。

1. 標準の[手順](../content-design/widget-create.md)に従って、残りのウィジェットプロパティを必要に応じて設定します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

1. プロンプトが表示されたら、無効なすべてのキャッシュを更新します。
