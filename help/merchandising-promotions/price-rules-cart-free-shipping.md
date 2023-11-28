---
title: 買い物かごの価格ルールの例 — 送料無料プロモーション
description: 買い物かごの価格ルールを使用して送料を無料で提供する例を確認します。
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# 買い物かごの価格ルールの例 — 送料無料プロモーション

無料配送は、プロモーションとして、を使用して、またはを使用せずに提供できます。 [クーポン](price-rules-cart-coupon.md). 無料の送料クーポンまたは割引券は、顧客の受け取り注文にも適用できるので、注文を請求し、発送して、 [workflow](../stores-purchase/order-processing.md#order-workflow-and-processing).

一部の配送業者の設定では、最小注文に基づいて無料配送を提供できます。 この基本的な機能を拡張するには、買い物かごの価格ルールを使用して、複数の製品属性、買い物かごの内容、顧客グループに基づいて複雑な条件を作成します。

## 手順 1. 送料無料を有効にする

1. 有効にする [無料送料](../stores-purchase/shipping-free.md) をストア設定に追加します。

1. すべての送料の無料設定を完了します [キャリアサービス](../stores-purchase/carriers.md) 無料で送るために使いたい

## 手順 2. 買い物かごの価格ルールの作成

次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

次の手順に従って、提供する無料配送プロモーションのタイプを設定します。

### 例 1：任意の注文の無料配送

1. 次を完了： **[!UICONTROL Rule Information]** 次のように指定します。

   - を入力します。 **[!UICONTROL Rule Name]** 内部参照用。
   - 概要を入力 **[!UICONTROL Description]** ルールを説明するために使用します。
   - 設定 **[!UICONTROL Active]** から `Yes`.
   - Adobe Analytics の **[!UICONTROL Websites]** ボックスで、無料配送クーポンを利用できる各サイトを選択します。
   - を選択します。 **[!UICONTROL Customer Groups]** ルールを適用する先にドラッグします。
   - 設定 **[!UICONTROL Coupon]** を次のいずれかに変更します。
      - クーポンを使用せずに無料の送料プロモーションを提供するには、デフォルト (`No Coupon`) 設定で使用できます。
      - 価格ルールでクーポンを使用するには、「 `Specific Coupon`. 必要に応じて、 [クーポン](price-rules-cart-coupon.md).

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Actions]** 」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Apply]** から `Percent of product price discount`.
   - 設定 **[!UICONTROL Apply to Shipping Amount]** から `Yes`.
   - 設定 **[!UICONTROL Free Shipping]** から `For matching items only`.

   ![買い物かごの価格ルール — 送料無料アクション](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### 例 2:$額を超える注文の無料送料

1. 次を完了： **[!UICONTROL General Information]** 前の例で説明した設定。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Conditions]** 」セクションに入力します。

1. クリック _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) をクリックして条件を挿入し、次の操作を実行します。

   - の下のリストで **[!UICONTROL Cart Attribute]**&#x200B;を選択します。 `Subtotal`.
   - クリック **[!UICONTROL is]** を選択します。 `equals or greater than`.
   - クリック **...** 小計のしきい値を入力します。次に例を示します。 `100`、をクリックして条件を完了します。

   ![買い物かごの価格ルール — 条件](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. 必要に応じて、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Actions]** 」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Apply]** から `Percent of product price discount`.
   - 設定 **[!UICONTROL Apply to Shipping Amount]** から `Yes`.
   - 設定 **[!UICONTROL Free Shipping]** から `For matching items only`.

## 手順 3. ラベルを完成させます。

完了 [手順 4](price-rules-cart.md) を使用して、チェックアウト時に表示されるラベルを入力します。

## 手順 4. ルールを保存してテストする

{{new-price-rule}}

1. ルールが完了したら、「 **[!UICONTROL Save Rule]**.

1. ルールをテストして、正しく動作することを確認します。
