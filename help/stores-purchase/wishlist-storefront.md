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

![ストアフロントの例 – My Wish List](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceでは、お客様のアカウントごとに複数のウィッシュリストを使用できます。

![Magento Open Source](../assets/open-source.svg) Magento Open Sourceコードベースは、お客様のアカウントごとに 1 つのウィッシュリストの使用をサポートしています。

## ウィッシュリストの作成

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

ストアフロントでは、顧客はアカウントダッシュボード、製品ページ、カタログページ、買い物かごからウィッシュリストを作成できます。

### 方法 1：顧客アカウントから

1. アカウントダッシュボードのサイドバーで、顧客は次を選択します **[!UICONTROL My Wish List]**.

1. 右上隅のをクリックします **[!UICONTROL Create New Wish List]**.

1. ウィッシュリスト名を入力します。

1. 他のユーザーがウィッシュリストを表示できるようにするには、はウィッシュリストを選択します **[!UICONTROL Public Wish List]** チェックボックス。

   >[!NOTE]
   >
   >主な違い `Public` および `Private` ウィッシュリストとは、プライベートのウィッシュリストが [検索可能](wishlist-configuration.md#add-wish-list-search) ウィッシュリストを使用します。

1. 完了したら、 **[!UICONTROL Save]**.

   ![新しいウィッシュリストを作成](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### 方法 2：カタログページから

1. 顧客はストアフロントから、ウィッシュリストに追加する製品を含むカタログページに移動します。

1. 製品にポインタを合わせます。

1. ユーザーが「」の横にある矢印をクリックします _ウィッシュリストに追加_ アイコンをクリックして、 **[!UICONTROL Create New Wish List]**.

1. ウィッシュリスト名を入力します。

1. 他のユーザーがウィッシュリストを表示できるようにするには、はウィッシュリストを選択します **[!UICONTROL Public Wish List]** チェックボックス。

1. 完了したら、をクリックします **[!UICONTROL Save]**.

### 方法 3：製品詳細ページから

1. ストアフロントから、ウィッシュリストに追加する製品の詳細ページに移動します。

1. の横の矢印をクリックします **[!UICONTROL Add to Wish List]** およびを選択 **[!UICONTROL Create New Wish List]**.

1. エントリ数： **[!UICONTROL Wish List Name]**.

1. 他のユーザーがウィッシュリストを表示できるようにするには、はウィッシュリストを選択します **[!UICONTROL Public Wish List]** チェックボックス。

1. 完了したら、をクリックします **[!UICONTROL Save]**.

   ![製品詳細ページから新しいウィッシュリストを作成](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### 方法 4：買い物かごから

1. 顧客が「」を開く **[!UICONTROL Shopping Cart]** ページ。

1. 項目の下の矢印をクリックします **[!UICONTROL Move to Wishlist]** およびを選択 **[!UICONTROL Create New Wish List]**.

1. エントリ数： **[!UICONTROL Wish List Name]**.

1. 他のユーザーがウィッシュリストを表示できるようにするには、はウィッシュリストを選択します **[!UICONTROL Public Wish List]** チェックボックス。

1. 完了したら、をクリックします **[!UICONTROL Save]**.

![買い物かごページから新しいウィッシュリストを作成](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## 製品リストの更新

1. お客様は、ウィッシュリストから製品をポイントしてオプションを表示します。

1. を追加します **[!UICONTROL Comment]** 製品については、価格の下のボックスにテキストを入力します。

   ![編集オプション](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. 製品オプションの選択を変更するには、をクリックします。 **[!UICONTROL Edit]** 次の操作を実行します。

   - 製品の詳細ページのオプションを更新します。
   - クリック数 **[!UICONTROL Update Wish List]**.

## 買い物かごにウィッシュリスト商品を追加

1. ウィッシュリストで、顧客は追加する製品を指します。

1. を更新 **[!UICONTROL Qty]** 必要に応じてその他のオプションも編集します。

1. クリック数 **[!UICONTROL Add to Cart]**.

## ウィッシュリストを共有

1. 顧客のクリック数 **[!UICONTROL Share Wishlist]**.

1. ウィッシュリストを受け取る各ユーザーのメールアドレスをコンマで区切って入力します。

1. を追加します **[!UICONTROL Message]** をメールに含めます。

1. クリック数 **[!UICONTROL Share Wish List]**.

   ![ウィッシュリストを共有](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   メッセージはプライマリから送信されます [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) また、各製品のサムネール画像とストアへのリンクが含まれます。

   ![共有ウィッシュリストのメール](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## 欲しい物のリストを編集

顧客は、アカウントダッシュボードから複数の方法でウィッシュリストを変更できます。

### 項目を別のリストに移動

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

1. 顧客は、移動する各項目のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Move Selected to Wish List]** 次のいずれかの操作を実行します。

   - 既存のウィッシュリストを選択します。
   - クリック数 **[!UICONTROL Create New Wish List]**.

### 別のリストに項目をコピー

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

1. 移動する各項目のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Copy Selected to Wish List]** 次のいずれかの操作を実行します。

   - 既存のウィッシュリストを選択します。
   - クリック数 **[!UICONTROL Create New Wish List]**.

## ウィッシュリストの削除

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

1. 削除するウィッシュリストを開きます。

1. クリック数 **[!UICONTROL Delete Wish List]**.

1. 確認を求められたら、をクリックします **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>このアクションは取り消しできません。

## 欲しい物のリスト項目をカートに転送

すべてのウィッシュリスト項目を買い物かごに転送するには、顧客がクリックします **[!UICONTROL Add All to Cart]**.

1 つの項目を追加するには、顧客が次の操作を行います。

1. 項目の上にマウスポインターを置き、 **[!UICONTROL Qty]** 買い物かごに追加する顧客。

1. クリック数 **[!UICONTROL Add to Cart]**.

## 顧客のウィッシュリストを見つける

次の場合 [ウィッシュリスト検索ウィジェット](wishlist-configuration.md#add-wish-list-search) お客様は、ストアページに含まれるを使用して、ウィッシュリストの所有者の名前またはメールアドレスで検索できます。

1. 顧客はウィッシュリスト検索ウィジェットから検索オプションを選択します。

1. ウィッシュリストの所有者の名前またはメールアドレスを入力し、クリックします **[!UICONTROL Search]**.

   この _ウィッシュリスト検索_ ページが開き、一致するウィッシュリストが「検索結果」セクションに表示されます。

   >[!NOTE]
   >
   >検索結果には、公開ウィッシュリストのみが表示されます。顧客の非公開ウィッシュリストは公開されません。

1. ウィッシュリスト項目のリストを表示するには、をクリックします **[!UICONTROL View]**.

   各ウィッシュリストに所有者名と最終更新日が表示されます。

1. 買い物かごに製品を追加するには、顧客が製品の下にあるチェックボックスをオンにしてクリックします **[!UICONTROL Add to Cart]**.

   また、他のお客様のウィッシュリストから自分のウィッシュリストに好きな項目を追加することもできます。
