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

- [注文と返品ウィジェット](../content-design/widget-orders-returns.md) サイドバー内
- _注文と返品_ フッター内のリンク

ベストプラクティスとして、RMA 要件とプロセスの説明を必ずカスタマーサービスポリシーに含めてください。

>[!NOTE]
>
>返品に関する追加情報を収集する場合は、独自のカスタムを追加できます [属性を返します](attributes-returns.md).

すべての顧客 RMA 情報は、 **[!UICONTROL My Returns]** 顧客アカウントダッシュボードの「」ページ。

![自分の返品](./assets/my-returns-page.png){width="700" zoomable="yes"}

## RMA をリクエスト

お客様は、ストアフロントで次の手順を完了して RMA を送信します。

1. フッターでをクリックします **[!UICONTROL Orders and Returns]**.

1. 注文情報を入力します。

   - 注文 ID
   - 請求の姓
   - 電子メール

1. クリック数 **[!UICONTROL Continue]**.

   ![注文と返品](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. 注文日の下のクリック数 **[!UICONTROL Return]**.

   ![注文の詳細](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. 返す項目を選択し、 **[!UICONTROL Quantity to Return]**.

1. セット **[!UICONTROL Resolution]** を次のいずれかに変更します。

   - Exchange
   - [払戻](../customers/refunds-customer-account.md)
   - [店舗クレジット](../customers/store-credit-using.md)

1. セット **[!UICONTROL Item Condition]** を次のいずれかに変更します。

   - `Unopened`
   - `Opened`
   - `Damaged`

1. セット **[!UICONTROL Reason to Return]** を次のいずれかに変更します。

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![新しい返品の作成](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. 必要に応じて、を設定します **[!UICONTROL Contact Email Address]** および **[!UICONTROL Comments]**.

   >[!NOTE]
   >
   >注文に複数の品目が含まれており、顧客が別の品目を返品したい場合は、 **[!UICONTROL Add Item To Return]**&#x200B;を選択し、項目を選択して、すべてのオプションを設定します。

1. クリック数 **[!UICONTROL Submit]**.
