---
title: 注文の作成
description: Commerce Adminで、お客様の注文を作成する方法を説明します。
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
TQID: https://experienceleague.adobe.com/0TUx-cDuonSkm4G0zWaU95ZKDuB-yhPb0aaEW57K-3g
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 0%

---

# 注文の作成

サポートが必要な登録済みのお客様は、Adminから直接注文全体を作成できます。 _[!UICONTROL Create New Order]_フォームには、通常のチェックアウトプロセスに必要なすべての情報と、顧客のアカウントダッシュボードからのアクティビティの概要が含まれています。

![顧客の注文を作成](./assets/create-new-order.png){width="700" zoomable="yes"}

## 手順1：注文の作成

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**&#x200B;をクリックします。

1. グリッド内の顧客を検索します。

1. _アクション_&#x200B;列で、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. ワークスペースのヘッダーで、**[!UICONTROL Create Order]**&#x200B;をクリックします。

   ![Workspace ヘッダー](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   **[!UICONTROL Create New Order]**&#x200B;をクリックして、[注文ワークスペース ](orders.md#orders-workspace)で注文を作成することもできます。

## 手順2：製品の追加

ストアに複数のビューがある場合は、注文を配置するストアビューを選択します。

### [!UICONTROL Customer's Activities] サイドバーから商品を追加

顧客のウィッシュリストから、または最近閲覧した商品、比較した商品、注文した商品から商品をカートに転送できます。

1. 次のいずれかのセクションで![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. 左側のパネルで各製品のチェックボックスを選択します。

1. 下にスクロールして、**[!UICONTROL Update Changes]**&#x200B;をクリックします。

   注文フォームにアイテムが表示されます。

   ![買い物かごに追加](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### カタログから商品を追加する

1. **[!UICONTROL Add Products]**&#x200B;をクリックします。

   ![製品を追加](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. グリッドで、買い物かごに追加する各商品のチェックボックスを選択し、購入する&#x200B;**[!UICONTROL Qty]**&#x200B;を入力します。

   ![製品を選択](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >商品選択グリッドには、割引やカートやグループ価格のルールが適用されることなく、商品の通常の基本価格が常に表示されます。 最終商品価格は、商品が注文/カートに追加された場合にのみ計算されます。

1. 使用可能な製品オプションを設定します。

   - **[!UICONTROL Configure]**&#x200B;をクリックします。

   - 必要に応じてオプションを完了します。

   - **[!UICONTROL OK]**&#x200B;をクリックします。

   - **[!UICONTROL Add Selected Product(s) to Order]**&#x200B;をクリックして買い物かごを更新します。

1. 商品が[ ギフトオプション ](../catalog/product-gift-options.md)用に設定されている場合は、必要に応じてオプションを設定します。

1. 必要に応じて、項目の価格を上書きします。

   - 「**[!UICONTROL Custom Price]**」チェックボックスを選択し、下のボックスに新しい価格を入力します。

   - 買い物かごの合計を更新するには、**[!UICONTROL Update Items and Quantities]**&#x200B;をクリックします。

   ![ カスタム価格](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. 注文に必要に応じて、次のセクションを完了します。

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]
   - [!UICONTROL [ カスタム注文属性]](../stores-purchase/order-processing.md#custom-order-attributes)

>[!NOTE]
>
>Payment Services拡張機能がインストールされ、設定されている場合にこの機能をサポートする支払い方法について詳しくは、[支払いサービスガイド ](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview)を参照してください。

## 手順3：注文の送信

**[!UICONTROL Submit Order]**&#x200B;をクリックします。

お客様に確認書が送信され、お客様はアカウントから注文詳細を確認できます。
