---
title: 買い物かご価格ルールの例 – 送料無料プロモーション
description: 買い物かごの価格ルールを使用して送料無料を提供する例を確認します。
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# 買い物かご価格ルールの例 – 送料無料プロモーション

送料無料は、プロモーションとして、[ クーポン ](price-rules-cart-coupon.md) の有無にかかわらず提供できます。 送料無料クーポンまたは割引券を顧客の受け取り注文に適用することもできます。これにより、注文を請求および出荷して [ ワークフロー ](../stores-purchase/order-processing.md#order-workflow-and-processing) を完了できます。

一部の配送業者の設定では、最小注文に基づいて送料無料を提供できます。 この基本機能をさらに拡張するには、買い物かごの価格ルールを使用して、複数の製品属性、買い物かごの内容、顧客グループに基づいて複雑な条件を作成します。

## 手順 1. 送料無料を有効にする

1. ストアの設定で [ 送料無料 ](../stores-purchase/shipping-free.md) を有効にします。

1. 送料無料に使用する [ 配送業者サービス ](../stores-purchase/carriers.md) の送料無料設定を完了します。

## 手順 2. 買い物かご価格ルールの作成

_管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Promotions]_/**[!UICONTROL Cart Price Rules]**&#x200B;に移動します。

次の手順に従って、提供する送料無料プロモーションのタイプを設定します。

### 例 1：あらゆる注文に対する送料無料

1. **[!UICONTROL Rule Information]** を次のように入力します。

   - 内部参照の **[!UICONTROL Rule Name]** を入力します。
   - ルールの簡単な **[!UICONTROL Description]** を入力します。
   - **[!UICONTROL Active]** を `Yes` に設定します。
   - **[!UICONTROL Websites]** ボックスで、送料無料クーポンを利用できる各サイトを選択します。
   - ルールを適用する **[!UICONTROL Customer Groups]** を選択します。
   - **[!UICONTROL Coupon]** を次のいずれかに設定します。
      - クーポンなしで送料無料プロモーションを提供するには、デフォルト（`No Coupon`）設定を受け入れます。
      - 価格ルールでクーポンを使用するには、[`Specific Coupon`] を選択します。 必要に応じて、手順を完了して [ クーポン ](price-rules-cart-coupon.md) を設定します。

1. 下にスクロールして、「**[!UICONTROL Actions]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、次の操作を行います。

   - **[!UICONTROL Apply]** を `Percent of product price discount` に設定します。
   - **[!UICONTROL Apply to Shipping Amount]** を `Yes` に設定します。
   - **[!UICONTROL Free Shipping]** を `For matching items only` に設定します。

   ![ 買い物かご価格ルール – 送料無料アクション ](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### 例 2:$金額を超える注文の送料無料

1. 前の例で説明したように、**[!UICONTROL General Information]** の設定を完了します。

1. 下にスクロールして、「**[!UICONTROL Conditions]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

1. _追加_ （![ 追加アイコン ](../assets/icon-add-green-circle.png)）をクリックして条件を挿入し、次の手順を実行します。

   - **[!UICONTROL Cart Attribute]** の下のリストで、「`Subtotal`」を選択します。
   - 「**[!UICONTROL is]**」をクリックし、「`equals or greater than`」を選択します。
   - 「**...**」をクリックし、小計のしきい値（`100` など）を入力して条件を完了します。

   ![ 買い物かご価格ルール – 条件 ](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. 必要に応じて、「**[!UICONTROL Actions]**」セクションの ![ 拡張セレクター ](../assets/icon-display-expand.png) を展開し、次の操作を行います。

   - **[!UICONTROL Apply]** を `Percent of product price discount` に設定します。
   - **[!UICONTROL Apply to Shipping Amount]** を `Yes` に設定します。
   - **[!UICONTROL Free Shipping]** を `For matching items only` に設定します。

## 手順 3. ラベルを完成させる

買い物かご価格ルールの手順の [ 手順 4](price-rules-cart.md) を完了して、チェックアウト時に表示されるラベルを入力します。

## 手順 4. ルールを保存してテストする

{{new-price-rule}}

1. ルールが完成したら、「**[!UICONTROL Save Rule]**」をクリックします。

1. ルールをテストして、正しく動作することを確認します。
