---
title: ウィッシュリストのストアフロントの経験
description: ストアフロントでお客様が利用できるウィッシュリスト管理ツールについて説明します。
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# ウィッシュリストのストアフロントの経験

ウィッシュリストは、顧客が好きな製品を思い出すのに便利な方法ですが、購入する準備ができていません。 ウィッシュリストのアイテムは、他のユーザーと共有したり、買い物かごに追加したりできます。 顧客が複数のウィッシュリストを持っている場合、現在のウィッシュリストの名前がページの上部に表示されます。 顧客は、アカウントダッシュボードからウィッシュリストを管理できます。 ストア管理者は、顧客が管理者からウィッシュリストを管理するのに役立つこともできます。

![ ストアフロントの例 – My Wish List](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceでは、お客様のアカウントごとに複数のウィッシュリストの使用をサポートしています。

![Magento Open Source](../assets/open-source.svg)Magento Open Sourceコードベースでは、お客様のアカウントごとに 1 つのウィッシュリストの使用がサポートされています。

## ウィッシュリストの作成

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

ストアフロントでは、顧客はアカウントダッシュボード、製品ページ、カタログページ、買い物かごからウィッシュリストを作成できます。

### 方法 1：顧客アカウントから

1. アカウントダッシュボードのサイドバーで、顧客は **[!UICONTROL My Wish List]** を選択します。

1. 右上隅にある「**[!UICONTROL Create New Wish List]**」をクリックします。

1. ウィッシュリスト名を入力します。

1. 他のユーザーがウィッシュリストを表示できるようにするには、「**[!UICONTROL Public Wish List]**」チェックボックスを選択します。

   >[!NOTE]
   >
   >`Public` と `Private` のウィッシュリストの主な違いは、非公開のウィッシュリストがウィッシュリストを介して [ 検索 ](wishlist-configuration.md#add-wish-list-search) できないことです。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   ![ 新しいウィッシュリストの作成 ](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### 方法 2：カタログページから

1. 顧客はストアフロントから、ウィッシュリストに追加する製品を含むカタログページに移動します。

1. 製品にポインタを合わせます。

1. 顧客は「_ウィッシュリストに追加_ アイコンの横にある矢印をクリックし、**[!UICONTROL Create New Wish List]** を選択します。

1. ウィッシュリスト名を入力します。

1. 他のユーザーがウィッシュリストを表示できるようにするには、「**[!UICONTROL Public Wish List]**」チェックボックスを選択します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

### 方法 3：製品詳細ページから

1. ストアフロントから、ウィッシュリストに追加する製品の詳細ページに移動します。

1. **[!UICONTROL Add to Wish List]** の横にある矢印をクリックし、**[!UICONTROL Create New Wish List]** を選択します。

1. **[!UICONTROL Wish List Name]** を入力します。

1. 他のユーザーがウィッシュリストを表示できるようにするには、「**[!UICONTROL Public Wish List]**」チェックボックスを選択します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   ![ 製品の詳細ページから新しいウィッシュリストを作成 ](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### 方法 4：買い物かごから

1. 顧客が **[!UICONTROL Shopping Cart]** ページを開きます。

1. 項目の下の **[!UICONTROL Move to Wishlist]** の横にある矢印をクリックし、**[!UICONTROL Create New Wish List]** を選択します。

1. **[!UICONTROL Wish List Name]** を入力します。

1. 他のユーザーがウィッシュリストを表示できるようにするには、「**[!UICONTROL Public Wish List]**」チェックボックスを選択します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

![ 買い物かごページから新しいウィッシュリストを作成 ](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## 製品リストの更新

1. お客様は、ウィッシュリストから製品をポイントしてオプションを表示します。

1. 製品に関する **[!UICONTROL Comment]** を追加するには、価格の下のボックスにテキストを入力します。

   ![ 編集オプション ](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. 製品オプションの選択を変更するには、「**[!UICONTROL Edit]**」をクリックして、次の操作を実行します。

   - 製品の詳細ページのオプションを更新します。
   - **[!UICONTROL Update Wish List]** をクリックします。

## 買い物かごにウィッシュリスト商品を追加

1. ウィッシュリストで、顧客は追加する製品を指します。

1. **[!UICONTROL Qty]** を更新し、必要に応じて他のオプションを編集します。

1. **[!UICONTROL Add to Cart]** をクリックします。

## ウィッシュリストを共有

1. 顧客は「**[!UICONTROL Share Wishlist]**」をクリックします。

1. ウィッシュリストを受け取る各ユーザーのメールアドレスをコンマで区切って入力します。

1. メールに含める **[!UICONTROL Message]** を追加します。

1. **[!UICONTROL Share Wish List]** をクリックします。

   ![ ウィッシュリストを共有 ](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   メッセージはプライマリ [ ストアの連絡先 ](../getting-started/store-details.md#store-email-addresses) から送信され、各製品のサムネール画像とストアへのリンクが含まれます。

   ![ 共有ウィッシュリストのメール ](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## 欲しい物のリストを編集

顧客は、アカウントダッシュボードから複数の方法でウィッシュリストを変更できます。

### 項目を別のリストに移動

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

1. 顧客は、移動する各項目のチェックボックスを選択します。

1. **[!UICONTROL Move Selected to Wish List]** をクリックして、次のいずれかの操作を行います。

   - 既存のウィッシュリストを選択します。
   - **[!UICONTROL Create New Wish List]** をクリックします。

### 別のリストに項目をコピー

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

1. 移動する各項目のチェックボックスを選択します。

1. **[!UICONTROL Copy Selected to Wish List]** をクリックして、次のいずれかの操作を行います。

   - 既存のウィッシュリストを選択します。
   - **[!UICONTROL Create New Wish List]** をクリックします。

## ウィッシュリストの削除

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

1. 削除するウィッシュリストを開きます。

1. **[!UICONTROL Delete Wish List]** をクリックします。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL OK]**」をクリックします。

>[!IMPORTANT]
>
>このアクションは取り消しできません。

## 欲しい物のリスト項目をカートに転送

すべてのウィッシュリスト項目を買い物かごに転送するには、顧客は「**[!UICONTROL Add All to Cart]**」をクリックします。

1 つの項目を追加するには、顧客が次の操作を行います。

1. 項目の上にマウスポインターを置き、買い物かごに追加する **[!UICONTROL Qty]** を入力します。

1. **[!UICONTROL Add to Cart]** をクリックします。

## 顧客のウィッシュリストを見つける

ストアページに含まれる [ ウィッシュリスト検索ウィジェット ](wishlist-configuration.md#add-wish-list-search) の場合、お客様はウィッシュリストの所有者の名前またはメールアドレスで検索できます。

1. 顧客はウィッシュリスト検索ウィジェットから検索オプションを選択します。

1. ウィッシュリストの所有者の名前またはメールアドレスを入力し、**[!UICONTROL Search]** をクリックします。

   _ウィッシュリスト検索_ ページが開き、一致するウィッシュリストが検索結果セクションに表示されます。

   >[!NOTE]
   >
   >検索結果には、公開ウィッシュリストのみが表示されます。顧客の非公開ウィッシュリストは公開されません。

1. ウィッシュリストの項目のリストを表示するには、「**[!UICONTROL View]**」をクリックします。

   各ウィッシュリストに所有者名と最終更新日が表示されます。

1. 買い物かごに製品を追加するには、顧客が製品の下にあるチェックボックスをオンにして、**[!UICONTROL Add to Cart]** をクリックします。

   また、他のお客様のウィッシュリストから自分のウィッシュリストに好きな項目を追加することもできます。
