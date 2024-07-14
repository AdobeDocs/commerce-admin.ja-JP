---
title: ストアフロントのエクスペリエンスを返します
description: 顧客がストアフロントのアカウントから製品の返品を管理する方法を説明します。
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# ストアフロントのエクスペリエンスを返します

{{ee-feature}}

お客様は、次のいずれかを使用して、ストアフロントから RMA をリクエストできます。

- [ 注文と返品ウィジェット ](../content-design/widget-orders-returns.md) サイドバー内
- フッターの _注文と返品_ リンク

ベストプラクティスとして、RMA 要件とプロセスの説明を必ずカスタマーサービスポリシーに含めてください。

>[!NOTE]
>
>返品に関連する追加情報を収集する場合は、独自のカスタム [ 返品属性 ](attributes-returns.md) を追加できます。

すべての顧客 RMA 情報は、顧客アカウントダッシュボードの **[!UICONTROL My Returns]** ページに表示されます。

![ 返品数 ](./assets/my-returns-page.png){width="700" zoomable="yes"}

## RMA をリクエスト

お客様は、ストアフロントで次の手順を完了して RMA を送信します。

1. フッターで、[**[!UICONTROL Orders and Returns]**] をクリックします。

1. 注文情報を入力します。

   - 注文 ID
   - 請求の姓
   - 電子メール

1. **[!UICONTROL Continue]** をクリックします。

   ![ 受注と返品 ](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. 注文日の下で、「**[!UICONTROL Return]**」をクリックします。

   ![ 注文詳細 ](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. 返す項目を選択し、**[!UICONTROL Quantity to Return]** を入力します。

1. **[!UICONTROL Resolution]** を次のいずれかに設定します。

   - Exchange
   - [払戻](../customers/refunds-customer-account.md)
   - [店舗クレジット](../customers/store-credit-using.md)

1. **[!UICONTROL Item Condition]** を次のいずれかに設定します。

   - `Unopened`
   - `Opened`
   - `Damaged`

1. **[!UICONTROL Reason to Return]** を次のいずれかに設定します。

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![ 新しい返品の作成 ](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. 必要に応じて、**[!UICONTROL Contact Email Address]** と **[!UICONTROL Comments]** を設定します。

   >[!NOTE]
   >
   >注文に複数の品目が含まれており、顧客が別の品目を返品したい場合は、**[!UICONTROL Add Item To Return]** をクリックし、品目を選択して、すべての言及されたオプションを設定できます。

1. **[!UICONTROL Submit]** をクリックします。
