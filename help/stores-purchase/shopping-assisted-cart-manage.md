---
title: 買い物かごの管理
description: 管理者から直接顧客の買い物かごを支援する方法について説明します。
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: dc19eeea03dc46b14fcbe339a8e426b249346673
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# 買い物かごの管理

{{ee-feature}}

アシストショッピングセッションを開始するには、顧客がストアフロントからアカウントにログインして、情報を利用できるようにする必要があります。 顧客がアカウントを持っていない場合は、次のことができます [1 つ作成](../customers/account-create.md).

![顧客アカウント内の買い物かご](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## アクション制御

| オプション | 説明 |
|--- |--- |
| [!UICONTROL Remove] | 現在の買い物かごからアイテムを削除します |
| [!UICONTROL Move to Wish List] | 選択された顧客ウィッシュリストに項目を移動 |

{style="table-layout:auto"}

## コントロールボタン

| ボタン | 説明 |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | 現在の買い物かごをすべての商品からクリアします。 |
| [!UICONTROL Update Items and Quantities|]に必要な数量を入力 **[!UICONTROL Qty]** フィールドに入力し、カート内の項目数を更新します。 |
| [!UICONTROL Add selections to my cart] | すべてのセクションから買い物かごに商品を追加します。 |

{style="table-layout:auto"}

## ユーザーがログインしていることを確認

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   ストアに訪問し、ログインした顧客のすべての訪問者がリストに表示されます。

   ![Customers Now Online](./assets/customers-now-online.png){width="700" zoomable="yes"}

## オファー支援ショッピング

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. リストで、顧客レコードを編集モードで開きます。

   >[!TIP]
   >
   >顧客レコードを急いで見つけるには、 [フィルター](../getting-started/admin-grid-controls.md) 制御。

   の下の顧客プロファイルで _[!UICONTROL Personal Information]_,_[!UICONTROL Last Logged In]_ 日時は、顧客がオンラインであることを示します。

   ![オンライン顧客の顧客プロファイル](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. アシストショッピングモードに入るには、 **[!UICONTROL Manage Shopping Cart]** 上部のボタンバーに移動します。

   ![アシストショッピングモード](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## 製品を属性別に買い物かごに追加

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Products]** セクション。

1. 各列の上部にあるフィルターのいずれかを使用して、製品を検索します。

1. クリック **[!UICONTROL Search]**.

1. 製品タイプに応じて、次の一連の手順のいずれかを使用します。

### シンプルな製品を追加

1. 注文する商品をクリックします。

   レコードとセットを選択します **[!UICONTROL Quantity]** デフォルト値の `1`.

1. 必要に応じて、注文数量を更新します。

1. グリッドの左上で、をクリックします。 **[!UICONTROL Add selections to my cart]**.

   ![買い物かごに製品を追加](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   行項目がページ上部の買い物かごに追加されます。

   ![買い物かごが更新されました](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### 設定を使用した製品の追加

買い物かごに追加する前に設定する必要がある製品には、次の 3 つのタイプがあります。 `Bundle Product`, `Configurable Product`、および `Grouped Product`.

1. グリッドで、をクリックします **[!UICONTROL Configure]** 製品名の隣。

   ![製品の設定](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. が含まれる _関連製品_ ダイアログで、各製品オプションを選択して注文する項目を記述し、 **[!UICONTROL Quantity]**&#x200B;を選択し、 **[!UICONTROL OK]**.

   商品がチェックマークと共に選択され、注文数量がグリッドに表示されます。

1. 商品を買い物かごに追加するには、 **[!UICONTROL Add selections to my cart]**.

   ![カート内の設定可能な製品](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. 必要に応じて、買い物かごの製品オプションを更新します。

   - クリック **[!UICONTROL Configure]**.

   - オプションを更新し、 **[!UICONTROL OK]**.

## SKU で製品を追加

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Add to Shopping Cart by SKU]** セクション。

1. 製品を個別に追加する基準 **[!UICONTROL SKU]** または、CSV ファイルをアップロードして製品を追加します。

### SKU 別に個別に項目を追加

1. を入力 **[!UICONTROL SKU]** および **[!UICONTROL Qty]** 注文する品目の。

1. 別の製品を注文するには、をクリックします。 **[!UICONTROL Add another]**.

   ![SKU 別に製品を追加](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Add selections to my cart]**.

1. 項目が設定可能な製品の場合は、プロンプトが表示されたら製品オプションを選択し、 **[!UICONTROL Add to Shopping Cart]**.

### CSV ファイルをアップロードして製品を追加

1. 準備 [csv ファイル](../systems/data-csv.md) と、買い物かごに追加されるアイテムを指定します。

   ファイルには列を 2 つだけ含め、 `sku` および `qty` ヘッダーで。

1. 準備したファイルをアップロードします。

   - クリック **[!UICONTROL Choose File]**.

   - アップロードするファイルをディレクトリから選択します。

## 項目を転送

顧客のウィッシュリストから買い物かごに項目を転送したり、最近表示した項目や比較した項目、注文した項目を転送したりできます。 各セクション内の項目数は、セクション ヘッダーの後の括弧内に表示されます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) 次のセクションの 1 つ：

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. グリッドで、注文する各製品を選択し、 **[!UICONTROL Quantity]**.

1. 設定可能な製品のオプションを入力するには、 **[!UICONTROL Configure]** 必要に応じて製品オプションを設定します。

1. クリック **[!UICONTROL Add selections to my cart]**.

1. 利用可能な場合は、1 つ以上のクーポンコードを適用します。

   - の場合 **[!UICONTROL Apply Coupon Code]**&#x200B;有効なクーポンコードを入力してください。

   - 「」をクリックします _適用_ （ ![矢印アイコン](../assets/icon-apply-arrow.png) ）矢印キー。

1. 必要に応じて注文数量を調整します。

   - が含まれる **[!UICONTROL Qty]** 調整する製品の列に、正しい金額を入力します。

   - クリック **[!UICONTROL Update Items and Quantities]**.

## オーダーの作成

1. クリック **[!UICONTROL Create Order]**.

   この _[!UICONTROL Create New Order]_ページには、カート内の商品が表示され、その後に発送情報と支払い情報が表示されます。

1. 配送および支払い情報を入力します。

1. クリック **[!UICONTROL Submit Order]**.

詳しくは、 [オーダーの作成](customer-account-create-order.md).
