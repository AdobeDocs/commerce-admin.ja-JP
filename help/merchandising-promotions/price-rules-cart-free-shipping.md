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

送料無料は、プロモーションとして提供できます（有無は問わない） [クーポン](price-rules-cart-coupon.md). 送料無料クーポンまたは割引券は、顧客の受け取り注文にも適用できます。これにより、注文を請求して出荷し、 [ワークフロー](../stores-purchase/order-processing.md#order-workflow-and-processing).

一部の配送業者の設定では、最小注文に基づいて送料無料を提供できます。 この基本機能をさらに拡張するには、買い物かごの価格ルールを使用して、複数の製品属性、買い物かごの内容、顧客グループに基づいて複雑な条件を作成します。

## 手順 1. 送料無料を有効にする

1. Enable （有効） [送料無料](../stores-purchase/shipping-free.md) ストア設定で指定します。

1. 以下の無料設定を完了してください [通信事業者サービス](../stores-purchase/carriers.md) 送料無料でご利用ください。

## 手順 2. 買い物かご価格ルールの作成

日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

次の手順に従って、提供する送料無料プロモーションのタイプを設定します。

### 例 1：あらゆる注文に対する送料無料

1. を完了する **[!UICONTROL Rule Information]** 次のように設定します。

   - を入力 **[!UICONTROL Rule Name]** 内部参照用。
   - 概要を入力 **[!UICONTROL Description]** ルールを記述します。
   - を設定 **[!UICONTROL Active]** 対象： `Yes`.
   - が含まれる **[!UICONTROL Websites]** ボックスに、送料無料クーポンを利用できる各サイトを選択します。
   - 「」を選択します **[!UICONTROL Customer Groups]** 規則を適用する。
   - を設定 **[!UICONTROL Coupon]** を次のいずれかに変更します。
      - クーポンのない送料無料プロモーションを提供するには、デフォルトを受け入れます（`No Coupon`）を設定します。
      - 価格ルールでクーポンを使用するには、次を選択します `Specific Coupon`. 必要に応じて、の設定手順を実行します。 [クーポン](price-rules-cart-coupon.md).

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Actions]** を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Apply]** 対象： `Percent of product price discount`.
   - を設定 **[!UICONTROL Apply to Shipping Amount]** 対象： `Yes`.
   - を設定 **[!UICONTROL Free Shipping]** 対象： `For matching items only`.

   ![買い物かご価格ルール – 無料配送アクション](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### 例 2:$金額を超える注文の送料無料

1. を完了する **[!UICONTROL General Information]** 前述の例で説明した設定。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Conditions]** セクション。

1. クリック _追加_ （![アイコンを追加](../assets/icon-add-green-circle.png)）を使用して条件を挿入し、次の手順を実行します。

   - の下のリスト **[!UICONTROL Cart Attribute]**、を選択 `Subtotal`.
   - クリック **[!UICONTROL is]** を選択します `equals or greater than`.
   - クリック **...** 次のように、小計のしきい値を入力します `100`、条件を完了します。

   ![買い物かご価格ルール – 条件](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. 必要に応じて、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Actions]** を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Apply]** 対象： `Percent of product price discount`.
   - を設定 **[!UICONTROL Apply to Shipping Amount]** 対象： `Yes`.
   - を設定 **[!UICONTROL Free Shipping]** 対象： `For matching items only`.

## 手順 3. ラベルを完成させる

完了 [手順 4](price-rules-cart.md) （チェックアウト時に表示されるラベルを入力するための買い物かご価格ルール手順）。

## 手順 4. ルールを保存してテストする

{{new-price-rule}}

1. ルールが完了したら、 **[!UICONTROL Save Rule]**.

1. ルールをテストして、正しく動作することを確認します。
