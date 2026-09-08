---
title: 無料ギフトプロモーション
description: 一連の条件が満たされたときに無料ギフトを提供するために、カート価格ルールを使用した無料ギフトプロモーションを設定する方法を説明します。
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 3cddc90c619a27b1404e0be7bb4b2c9a3b77e443
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---


# 無料ギフトのプロモーション

*無料ギフト* プロモーションでは、特定の条件で無料アイテムをカートに追加する[ カート価格ルール ](price-rules-cart.md)を設定できます。

>[!NOTE]
>
>この機能は、Luma ストアフロントではサポートされていません。 [GraphQL](https://developer.adobe.com/commerce/webapi/graphql/schema/cart/mutations/select-free-gift/)からアクセスでき、Edge Delivery Services（EDS）ストアフロントで利用できます。

## 無料のギフトプロモーションを作成

このセクションでは、次の形式を使用して無料ギフトプロモーションを作成する方法について説明します。

**X製品を購入し、Y製品を無料で入手**

1. [無料ギフトのプロモーション付きのカート価格ルール ](price-rules-cart.md#step-1-add-a-rule)を作成します。

1. [価格ルールの条件を定義するカートの手順の条件](price-rules-cart.md#step-2-describe-the-conditions)を説明します。 これは、ルールに追加できる複数の条件のうち、最初のもので、ルールがトリガーされるタイミングを決定します。 以下の組み合わせに基づいて行うことができます。

   - 製品属性
   - 特定可能
   - カート属性
   - Adobe Commerceの顧客セグメント

   空白のままにすると、カートごとにルールがトリガーされます。

   ![買い物かごの価格ルール – 条件](./assets/conditions.png){width="600" zoomable="yes"}

1. カート価格ルールのアクションを定義します。

   1. 「**[!UICONTROL Actions]**」セクションの「」（../assets/icon-display-expand.png）を展開し、次の情報を入力します。

   - **[!UICONTROL Apply]**&#x200B;を`Free Gift`に設定します。
   - **[!UICONTROL Gift SKU(s)]**&#x200B;で、顧客が無料ギフトとして選択できる1つ以上のSKUを選択します。
   - **[!UICONTROL Free Gift Discount Type]**&#x200B;を&#x200B;**[!UICONTROL Price Based]**&#x200B;または&#x200B;**[!UICONTROL Discount Based]**&#x200B;に設定します。
   - **[!UICONTROL Gift Qty]**&#x200B;に、お客様が受け取る無料ギフトの数量を入力します。 例えば、顧客に2つの無料アイテムを受け取ってもらいたい場合は、`2`と入力します。
   - 他の割引が適用されないようにするには、**[!UICONTROL Discard subsequent rules]**&#x200B;を`Yes`に設定します。

   1. **[!UICONTROL Save and Continue Edit]**&#x200B;をクリックし、必要に応じてルールの残りの部分を完了します。

1. [ チェックアウト時に表示されるラベルを入力するには、カート価格ルールの手順のラベル ](price-rules-cart.md)を完了します。

![買い物かごの価格ルール – 無料ギフト ラベル ](./assets/free-gift-promotion-label.png){width="600" zoomable="yes"}

{{new-price-rule}}

1. ルールが完了したら、**[!UICONTROL Save Rule]**&#x200B;をクリックします。

## バリエーション

カートの価格ルールをカスタマイズするには、さまざまな方法があります。 無料ギフト機能は、2つの異なる割引タイプで設定できます。

- **価格ベース**：ギフト行項目が`0`の価格で追加されます。
- **割引ベース**：ギフト行項目に全額割引が適用されます。
