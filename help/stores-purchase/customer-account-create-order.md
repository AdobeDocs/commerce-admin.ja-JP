---
title: オーダーの作成
description: Commerce Admin で顧客の注文を作成する方法を説明します。
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# オーダーの作成

サポートが必要な登録ユーザーの場合は、管理者から直接注文全体を作成できます。 この _[!UICONTROL Create New Order]_フォームには、通常のチェックアウトプロセスに必要なすべての情報と、顧客のアカウントダッシュボードに表示されるアクティビティ概要が含まれます。

![顧客の注文の作成](./assets/create-new-order.png){width="700" zoomable="yes"}

## 手順 1：オーダーの作成

1. 日 _Admin_ サイドバー、クリック **[!UICONTROL Customers]**.

1. グリッドで顧客を検索します。

1. が含まれる _アクション_ 列、クリック **[!UICONTROL Edit]**.

1. ワークスペースヘッダーで、 **[!UICONTROL Create Order]**.

   ![ワークスペースヘッダー](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   で注文を作成することもできます [注文ワークスペース](orders.md#orders-workspace) クリックして **[!UICONTROL Create New Order]**.

## 手順 2：製品を追加

ストアに複数のビューがある場合は、注文を行うストア表示を選択します。

### からの製品の追加 [!UICONTROL Customer's Activities] サイドバー

顧客のウィッシュリストから買い物かごに項目を転送したり、最近表示した項目、比較した項目または注文した項目を転送したりできます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) 次のセクションの 1 つ：

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. 左側のパネルで各製品のチェックボックスをオンにします。

1. 下にスクロールして、 **[!UICONTROL Update Changes]**.

   項目が注文フォームに表示されます。

   ![カートに追加](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### カタログから製品を追加

1. クリック **[!UICONTROL Add Products]**.

   ![製品を追加](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. グリッドで、カートに追加する各製品のチェックボックスを選択し、 **[!UICONTROL Qty]** 購入予定。

   ![製品を選択](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >商品選択グリッドには、割引や買い物かごまたはグループ価格ルールが適用されていなくても、常に商品の通常の基本価格が表示されます。 最終製品価格は、製品が注文/買い物かごに追加された場合にのみ計算されます。

1. 使用可能な製品オプションを設定します。

   - クリック **[!UICONTROL Configure]**.

   - 必要に応じてオプションを入力します。

   - クリック **[!UICONTROL OK]**.

   - クリック **[!UICONTROL Add Selected Product(s) to Order]** ：買い物かごを更新します。

1. 製品が次のように設定されている場合： [ギフトオプション](../catalog/product-gift-options.md)必要に応じてオプションを設定します。

1. 必要に応じて品目の価格を上書きします。

   - 「」を選択します **[!UICONTROL Custom Price]** チェックボックスをオンにして、下のボックスに新しい価格を入力します。

   - 買い物かごの合計を更新するには、をクリックします **[!UICONTROL Update Items and Quantities]**.

   ![カスタム価格](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. 注文の際に必要に応じて、以下の節を完了してください。

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]

>[!NOTE]
>
>を参照してください。 [支払いサービスガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/create-order.html) 支払いサービス拡張機能がインストールおよび設定されている場合に、この機能をサポートする支払い方法の詳細を確認します。

## 手順 3：注文を送信する

クリック **[!UICONTROL Submit Order]**.

確認が顧客に送信され、顧客は自分のアカウントから注文の詳細を表示できます。
