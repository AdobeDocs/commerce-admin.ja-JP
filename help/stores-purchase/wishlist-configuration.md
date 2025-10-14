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

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Wish List]**」を選択します。

1. **[!UICONTROL General Options]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; 顧客設定 – ウィッシュリストの一般設定 &#x200B;](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enabled]** を `Yes` に切り替えます。これにより、ストアのウィッシュリストモジュールがアクティブになります。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Enable Multiple Wish Lists]** を `Yes` に切り替えます。これにより、複数のウィッシュリストを作成して管理できます。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）顧客が自分のアカウントに関連付けることのできるウィッシュリストの数を制限するには、**[!UICONTROL Number of Multiple Wish Lists]** の値を入力します。

   - **[!UICONTROL Show in Sidebar]** を `Yes` に切り替えて、サイドバーにウィッシュリストを表示します。

1. **[!UICONTROL Share Options]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; 顧客設定 – ウィッシュリスト共有オプション &#x200B;](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - メッセージの送信者として表示されるストアの連絡先の **[!UICONTROL Email Sender]** を設定します。 オプション：一般連絡先、営業担当、カスタマーサポート、カスタムメール

   - 顧客がウィッシュリストを共有する際に使用する **[!UICONTROL Email Template]** を設定します。

   - 顧客が送信できるメールの合計数を制限するには、**[!UICONTROL Max Emails Allowed to be Sent]** 値を入力します。 デフォルトは 10 で、最大値は 10,000 です。

   - メッセージのサイズを制限するには、**[!UICONTROL Email Text Length Limit]** の値を入力します。 デフォルトは 255 です。

1. **[!UICONTROL My Wish List Link]** のセクションの ![&#x200B; 拡張セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、**[!UICONTROL Display Wish List Summary]** を次のいずれかに設定します。

   - `Display number of items in wish list`
   - `Display item quantities`

   ![&#x200B; 顧客設定 – ウィッシュリストの表示 &#x200B;](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## ウィッシュリスト検索を追加

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

公開されているウィッシュリストは、ウィッシュリスト検索 [widget](../content-design/widgets.md) を使用して検索できます。 このウィジェットにより、顧客はウィッシュリストの所有者の名前またはメールアドレスで検索できます。 ストア顧客は、他の顧客に属するウィッシュリストを検索したり、それらを表示して製品を注文したり、独自のウィッシュリストに製品を追加したりできます。 他の顧客が公開ウィッシュリストから購入したアイテムは、元のウィッシュリストからは削除されません。 _ウィッシュリスト検索_ ウィジェットは、ストアの任意のページに追加でき、顧客が友人や家族のウィッシュリストを簡単に見つけることができます。

![&#x200B; ストアフロントの例 – ウィッシュリスト検索 &#x200B;](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Widgets]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add Widget]**」をクリックします。

1. 「_[!UICONTROL Settings]_」タブで以下を実行します。

   - **[!UICONTROL Type]** を `Wish List Search` に設定します。

   - **[!UICONTROL Design Theme]** を、ウィッシュリストが追加されるストアのテーマに設定します。

   - 「**[!UICONTROL Continue]**」をクリックします。

1. _[!UICONTROL Storefront Properties]_&#x200B;を完了します。

   - **[!UICONTROL Widget Title]** を入力します。

   - ウィジェットを使用するビューまたは web サイトに **[!UICONTROL Assign to Store Views]** を設定します。

   - **[!UICONTROL Sort Order]**：コンテナ内でのウィジェットの配置を決定する数値を入力します。

     `0` = first （デフォルト）、`1` = second、`2` = third など。

1. 「_[!UICONTROL Layout Updates]_」セクションで「**[!UICONTROL Add Layout Update]**」をクリックし、**[!UICONTROL Display on]**&#x200B;を次のいずれかに設定します。

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

1. **[!UICONTROL Container]** リストで、ページレイアウトを配置する領域を選択します。

   ![&#x200B; ウィッシュリスト検索ウィジェット – レイアウト &#x200B;](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. 左側のパネルで「**[!UICONTROL Widget Options]**」を選択します。

1. **[!UICONTROL Quick Search Form Types]** を次のいずれかに設定します。

   - `All Forms` – お客様は、利用可能なすべてのパラメーターで検索できます。
   - `Owner Name` – お客様は、所有者名でウィッシュリストを検索できます。
   - `Owner Email` – 所有者のメールアドレスでウィッシュリストを検索できます。

   >[!NOTE]
   >
   >配送先住所はウィッシュリストには含まれません。

1. 必要に応じて、標準 [&#x200B; 手順 &#x200B;](../content-design/widget-create.md) に従って、残りのウィジェットプロパティを設定します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. プロンプトが表示されたら、無効なキャッシュをすべて更新します。
