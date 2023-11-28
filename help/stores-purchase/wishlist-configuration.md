---
title: ウィッシュリストの設定
description: ストアの顧客にウィッシュリスト機能を設定する方法を説明します。
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# ウィッシュリストの設定

ウィッシュリストの設定はウィッシュリストを有効にし、ウィッシュリストが共有される際に使用される電子メールメッセージの電子メールテンプレートと送信者を決定します。

## ウィッシュリスト機能を有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Wish List]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL General Options]** 」セクションで次の操作を実行します。

   ![顧客設定 — ウィッシュリストの一般設定](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - 切り替え **[!UICONTROL Enabled]** から `Yes`：ストアのウィッシュリストモジュールをアクティブにします。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 切り替え **[!UICONTROL Enable Multiple Wish Lists]** から `Yes`：顧客は複数のウィッシュリストを作成および管理できます。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 顧客のアカウントに関連付けることができるウィッシュリストの数を制限するには、次の値を入力します： **[!UICONTROL Number of Multiple Wish Lists]**.

   - 切り替え **[!UICONTROL Show in Sidebar]** から `Yes`：サイドバーにウィッシュリストを表示します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Share Options]** 」セクションで次の操作を実行します。

   ![顧客設定 — ウィッシュリスト共有オプション](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - を設定します。 **[!UICONTROL Email Sender]** メッセージの送信者として表示されるストアの連絡先に追加します。 オプション：一般連絡先、営業担当者、カスタマーサポート、カスタムメール。

   - を設定します。 **[!UICONTROL Email Template]** 顧客がウィッシュリストを共有する際に使用します。

   - 顧客が送信できる電子メールの合計数を制限するには、 **[!UICONTROL Max Emails Allowed to be Sent]** の値です。 デフォルトは 10 で、最大は 10,000 です。

   - メッセージのサイズを制限するには、次の値を入力します。 **[!UICONTROL Email Text Length Limit]**. デフォルト値は 255 です。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL My Wish List Link]** セクションとセット **[!UICONTROL Display Wish List Summary]** を次のいずれかに変更します。

   - `Display number of items in wish list`
   - `Display item quantities`

   ![顧客設定 — ウィッシュリストの表示](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

## ウィッシュリスト検索を追加

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )

ウィッシュリスト検索を使用すると、任意のパブリックウィッシュリストを見つけることができます。 [widget](../content-design/widgets.md). ウィジェットを使用すると、顧客はウィッシュリストの所有者の名前または電子メールアドレスで検索できます。 店舗の顧客は、他の顧客に属するウィッシュリストを検索し、その顧客から製品を表示して注文したり、独自のウィッシュリストに製品を追加したりできます。 他の顧客が公開ウィッシュリストから購入した項目は、元のウィッシュリストからは削除されません。 The _ウィッシュリスト検索_ ウィジェットをストア内の任意のページに追加すると、顧客が簡単に友人や家族の希望のリストを見つけることができます。

![ストアフロントの例 — ウィッシュリスト検索](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅で、 **[!UICONTROL Add Widget]**.

1. Adobe Analytics の _[!UICONTROL Settings]_「 」タブで、以下の操作を実行します。

   - 設定 **[!UICONTROL Type]** から `Wish List Search`.

   - 設定 **[!UICONTROL Design Theme]** を、ウィッシュリストが追加されるストアのテーマに追加します。

   - クリック **[!UICONTROL Continue]**.

1. 次を完了： _[!UICONTROL Storefront Properties]_:

   - 次を入力します。 **[!UICONTROL Widget Title]**.

   - 設定 **[!UICONTROL Assign to Store Views]** を、ウィジェットが使用されるビューまたは web サイトに追加します。

   - の場合 **[!UICONTROL Sort Order]**」に値を入力して、コンテナ内でのウィジェットの配置を決定します。

     `0` =最初（デフォルト）、 `1` =秒 `2` = 3 番目、など。

1. Adobe Analytics の _[!UICONTROL Layout Updates]_セクションで、**[!UICONTROL Add Layout Update]**と設定します。**[!UICONTROL Display on]**を次のいずれかに変更します。

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

1. Adobe Analytics の **[!UICONTROL Container]** リストで、ページレイアウトを配置する領域を選択します。

   ![ウィッシュリスト検索ウィジェット — レイアウト](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. 左側のパネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. 設定 **[!UICONTROL Quick Search Form Types]** を次のいずれかに変更します。

   - `All Forms` ：顧客は、使用可能なすべてのパラメーターで検索できます。
   - `Owner Name`  — お客様は所有者名でウィッシュリストを検索できます。
   - `Owner Email`  — 顧客は所有者の電子メールアドレスでウィッシュリストを検索できます。

   >[!NOTE]
   >
   >配送先住所はウィッシュリストに含まれません。

1. 必要に応じて、残りのウィジェットプロパティを設定します。その際、標準の [instructions](../content-design/widget-create.md).

1. 完了したら、「 **[!UICONTROL Save]**.

1. プロンプトが表示されたら、無効なキャッシュをすべて更新します。
