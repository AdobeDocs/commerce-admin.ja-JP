---
title: オーダーの作成
description: コマース管理で顧客の注文を作成する方法を説明します。
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# オーダーの作成

サポートが必要な登録ユーザーの場合、管理者から直接注文全体を作成できます。 The _[!UICONTROL Create New Order]_フォームには、通常のチェックアウトプロセスに必要なすべての情報と、顧客のアカウントダッシュボードのアクティビティの概要が含まれています。

![顧客の注文の作成](./assets/create-new-order.png){width="700" zoomable="yes"}

## 手順 1：オーダーの作成

1. 次の日： _管理者_ サイドバー、クリック **[!UICONTROL Customers]**.

1. グリッド内の顧客を検索します。

1. Adobe Analytics の _アクション_ 列、クリック **[!UICONTROL Edit]**.

1. ワークスペースのヘッダーで、 **[!UICONTROL Create Order]**.

   ![Workspace ヘッダー](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   また、 [ワークスペースを並べ替え](orders.md#orders-workspace) クリックして **[!UICONTROL Create New Order]**.

## 手順 2：製品の追加

ストアに複数のビューがある場合、注文を配置するストアビューを選択します。

### から製品を追加 [!UICONTROL Customer's Activities] サイドバー

顧客のウィッシュリストから、または最近表示、比較または注文された品目から、品目を買い物かごに移動できます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) 次のセクションの 1 つ。

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. 左側のパネルで各製品のチェックボックスをオンにします。

1. 下にスクロールして、 **[!UICONTROL Update Changes]**.

   項目が注文フォームに表示されます。

   ![買い物かごに追加](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### カタログから製品を追加

1. クリック **[!UICONTROL Add Products]**.

   ![製品を追加](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. グリッドで、買い物かごに追加する各製品のチェックボックスを選択し、 **[!UICONTROL Qty]** 購入する必要があります。

   ![製品を選択](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >製品選択グリッドには、割引や買い物かごやグループの価格ルールが適用されることなく、常に製品の通常の基準価格が表示されます。 最終的な製品価格は、製品が注文/買い物かごに追加された場合にのみ計算されます。

1. 利用可能な製品オプションを設定します。

   - クリック **[!UICONTROL Configure]**.

   - 必要に応じてオプションを設定します。

   - クリック **[!UICONTROL OK]**.

   - クリック **[!UICONTROL Add Selected Product(s) to Order]** をクリックして、買い物かごを更新します。

1. 製品が [ギフトオプション](../catalog/product-gift-options.md)、必要に応じてオプションを設定します。

1. 必要に応じて、品目の価格を上書きします。

   - を選択します。 **[!UICONTROL Custom Price]** チェックボックスをオンにして、下のボックスに新しい価格を入力します。

   - 買い物かごの合計を更新するには、 **[!UICONTROL Update Items and Quantities]**.

   ![カスタム価格](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. オーダーの必要に応じて、次のセクションに入力します。

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]

>[!NOTE]
>
>詳しくは、 [支払いサービスガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/create-order.html) 支払サービス拡張機能がインストールおよび設定されている場合に、この機能をサポートする支払い方法の詳細については、を参照してください。

## 手順 3：オーダーを送信する

クリック **[!UICONTROL Submit Order]**.

確認が顧客に送信され、顧客は自分のアカウントから注文の詳細を表示できます。
