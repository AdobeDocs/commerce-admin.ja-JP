---
title: ウィッシュリストの設定
description: ストアの顧客に対してウィッシュリスト機能を設定する方法を説明します。
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# ウィッシュリストの設定

ウィッシュリスト構成は、ウィッシュリストを有効化し、ウィッシュリストが共有されるときに使用される電子メールテンプレートおよび電子メールメッセージの送信者を決定する。

## ウィッシュリスト機能の有効化

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Wish List]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL General Options]** を選択し、次の操作を実行します。

   ![お客様の設定 – ウィッシュリストの一般設定](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - 切り替え **[!UICONTROL Enabled]** 対象： `Yes`：ストアのウィッシュリストモジュールを有効化します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）切り替え **[!UICONTROL Enable Multiple Wish Lists]** 対象： `Yes`を使用すると、お客様は複数のウィッシュリストを作成および管理できます。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）顧客が自分のアカウントに関連付けることができるウィッシュリストの数を制限するには、値を **[!UICONTROL Number of Multiple Wish Lists]**.

   - 切り替え **[!UICONTROL Show in Sidebar]** 対象： `Yes`サイドバーにウィッシュリストが表示されます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Share Options]** を選択し、次の操作を実行します。

   ![顧客の設定 – ウィッシュリスト共有オプション](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - を **[!UICONTROL Email Sender]** メッセージの送信者として表示されるストアの連絡先に送信されます。 オプション：一般連絡先、営業担当、カスタマーサポート、カスタムメール

   - を **[!UICONTROL Email Template]** 顧客がウィッシュリストを共有する際に使用されます。

   - 顧客が送信できるメールの合計数を制限するには、 **[!UICONTROL Max Emails Allowed to be Sent]** の値。 デフォルトは 10 で、最大値は 10,000 です。

   - メッセージのサイズを制限するには、値を **[!UICONTROL Email Text Length Limit]**. デフォルトは 255 です。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL My Wish List Link]** セクションとセット **[!UICONTROL Display Wish List Summary]** を次のいずれかに変更します。

   - `Display number of items in wish list`
   - `Display item quantities`

   ![顧客設定 – ウィッシュリストの表示](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

## ウィッシュリスト検索を追加

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

公開されているウィッシュリストは、ウィッシュリスト検索を使用して見つけることができます [ウィジェット](../content-design/widgets.md). このウィジェットにより、顧客はウィッシュリストの所有者の名前またはメールアドレスで検索できます。 ストア顧客は、他の顧客に属するウィッシュリストを検索したり、それらを表示して製品を注文したり、独自のウィッシュリストに製品を追加したりできます。 他の顧客が公開ウィッシュリストから購入したアイテムは、元のウィッシュリストからは削除されません。 この _ウィッシュリスト検索_ ウィジェットは、顧客が友人や家族のウィッシュリストを簡単に見つけられるように、ストアの任意のページに追加できます。

![ストアフロントの例 – ウィッシュリスト検索](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Widget]**.

1. が含まれる _[!UICONTROL Settings]_タブで、次の操作を実行します。

   - を設定 **[!UICONTROL Type]** 対象： `Wish List Search`.

   - を設定 **[!UICONTROL Design Theme]** をウィッシュリストが追加されるストアのテーマに追加します。

   - クリック **[!UICONTROL Continue]**.

1. を完了する _[!UICONTROL Storefront Properties]_:

   - を入力 **[!UICONTROL Widget Title]**.

   - を設定 **[!UICONTROL Assign to Store Views]** からウィジェットを使用するビューまたは web サイト。

   - の場合 **[!UICONTROL Sort Order]**&#x200B;を入力し、コンテナ内のウィジェットの配置を決定する数値を入力します。

     `0` =最初（デフォルト）、 `1` =秒、 `2` = 3 番目、以下同様です。

1. が含まれる _[!UICONTROL Layout Updates]_セクションで、をクリック&#x200B;**[!UICONTROL Add Layout Update]**およびを設定&#x200B;**[!UICONTROL Display on]**を次のいずれかに変更します。

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

1. が含まれる **[!UICONTROL Container]** リストから、ページレイアウトを配置する領域を選択します。

   ![ウィッシュリスト検索ウィジェット – レイアウト](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. 左パネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. を設定 **[!UICONTROL Quick Search Form Types]** を次のいずれかに変更します。

   - `All Forms`  – お客様は、利用可能なすべてのパラメーターで検索できます。
   - `Owner Name`  – お客様は所有者名でウィッシュリストを検索できます。
   - `Owner Email`  – 所有者のメールアドレスでウィッシュリストを検索できます。

   >[!NOTE]
   >
   >配送先住所はウィッシュリストには含まれません。

1. 必要に応じて、標準に従って、残りのウィジェットプロパティを設定します [指示](../content-design/widget-create.md).

1. 完了したら、 **[!UICONTROL Save]**.

1. プロンプトが表示されたら、無効なキャッシュをすべて更新します。
