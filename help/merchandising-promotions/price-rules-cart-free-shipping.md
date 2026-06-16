---
title: カートの価格ルール例 – 送料無料プロモーション
description: カート価格ルールを使用して送料無料を提供する例を確認してください。
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 0%

---

# カートの価格ルール例 – 送料無料プロモーション

送料無料は、[ クーポン ](price-rules-cart-coupon.md)の有無を問わず、プロモーションとして提供できます。 送料無料のクーポン、またはバウチャーを顧客の受け取り注文に適用することもできるので、注文を請求して出荷して、[ ワークフロー](../stores-purchase/order-processing.md#order-workflow-and-processing)を完了できます。

配送業者の構成によっては、最低注文に基づいて送料無料を提供できるものもあります。 この基本的な機能をさらに拡張するには、ショッピングカートの価格ルールを使用して、複数の製品属性、カートの内容、顧客グループに基づいて複雑な条件を作成します。

## 手順1: 送料無料を有効にする

1. ストア設定で[送料無料](../stores-purchase/shipping-free.md)を有効にします。

1. 送料無料に使用する[ キャリア サービス ](../stores-purchase/carriers.md)の送料無料設定を完了します。

## 手順2: 買い物かごの価格ルールの作成

_管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**に移動します。

以下の手順に従って、提供する送料無料プロモーションの種類を設定します。

### 例1：任意の注文に対する送料無料

1. 次のように&#x200B;**[!UICONTROL Rule Information]**&#x200B;を入力します。

   - 内部参照用に&#x200B;**[!UICONTROL Rule Name]**&#x200B;を入力します。
   - ルールを説明する概要&#x200B;**[!UICONTROL Description]**&#x200B;を入力してください。
   - **[!UICONTROL Active]**&#x200B;を`Yes`に設定します。
   - **[!UICONTROL Websites]** ボックスで、送料無料クーポンを利用できる各サイトを選択します。
   - ルールが適用される&#x200B;**[!UICONTROL Customer Groups]**&#x200B;を選択します。
   - **[!UICONTROL Coupon]**&#x200B;を次のいずれかに設定します：
      - クーポンなしで送料無料プロモーションを提供するには、デフォルトの（`No Coupon`）設定に従います。
      - 価格ルールでクーポンを使用するには、`Specific Coupon`を選択します。 必要に応じて、手順を完了して[ クーポン ](price-rules-cart-coupon.md)を設定します。

1. 下にスクロールして、**[!UICONTROL Actions]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - **[!UICONTROL Apply]**&#x200B;を`Percent of product price discount`に設定します。
   - **[!UICONTROL Apply to Shipping Amount]**&#x200B;を`Yes`に設定します。
   - **[!UICONTROL Free Shipping]**&#x200B;を`For matching items only`に設定します。

   ![買い物かごの価格ルール – 送料無料](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### 例2:$金額を超える注文の送料無料

1. 前の例で説明したように、**[!UICONTROL General Information]**&#x200B;設定を完了します。

1. 下にスクロールして、**[!UICONTROL Conditions]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. _Add_ （![Add icon](../assets/icon-add-green-circle.png)）をクリックして条件を挿入し、次の操作を行います。

   - **[!UICONTROL Cart Attribute]**&#x200B;の下のリストで、`Subtotal`を選択します。
   - **[!UICONTROL is]**&#x200B;をクリックし、`equals or greater than`を選択します。
   - **...**&#x200B;をクリックし、`100`などの小計のしきい値を入力して、条件を完了します。

   ![買い物かごの価格ルール – 条件](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. 必要に応じて、**[!UICONTROL Actions]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - **[!UICONTROL Apply]**&#x200B;を`Percent of product price discount`に設定します。
   - **[!UICONTROL Apply to Shipping Amount]**&#x200B;を`Yes`に設定します。
   - **[!UICONTROL Free Shipping]**&#x200B;を`For matching items only`に設定します。

## 手順3: ラベルを記入してください

チェックアウト時に表示されるラベルを入力するには、カート価格ルール手順の[手順4](price-rules-cart.md)を完了します。

## 手順4: ルールを保存してテストする

{{new-price-rule}}

1. ルールが完了したら、**[!UICONTROL Save Rule]**&#x200B;をクリックします。

1. ルールをテストして、正しく動作することを確認します。
