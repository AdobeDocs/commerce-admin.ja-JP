---
title: ストアフロントエクスペリエンスを返します
description: ストアフロントで顧客が自分のアカウントから返品を管理する方法を説明します。
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# ストアフロントエクスペリエンスを返します

{{ee-feature}}

ストアフロントから RMA を要求するには、次のいずれかを使用できます。

- [注文と返品ウィジェット](../content-design/widget-orders-returns.md) サイドバー内
- _注文件数と返品数_ フッター内のリンク

ベストプラクティスとして、RMA 要件とプロセスの説明を必ずカスタマーサービスポリシーに記載してください。

>[!NOTE]
>
>返品に関する追加情報を収集したい場合は、独自のカスタム情報を追加できます [属性を返す](attributes-returns.md).

すべての顧客 RMA 情報が **[!UICONTROL My Returns]** 」ページを開き、顧客アカウントダッシュボードに表示します。

![戻り値](./assets/my-returns-page.png){width="700" zoomable="yes"}

## RMA の要求

ストアフロントで次の手順を実行して、RMA を送信します。

1. フッターで、をクリックします。 **[!UICONTROL Orders and Returns]**.

1. オーダー情報を入力します。

   - 注文 ID
   - 請求の姓
   - 電子メール

1. クリック数 **[!UICONTROL Continue]**.

   ![注文件数と返品数](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. 注文日の下で、「 」をクリックします **[!UICONTROL Return]**.

   ![注文の詳細](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. 返す項目を選択し、 **[!UICONTROL Quantity to Return]**.

1. セット **[!UICONTROL Resolution]** を次のいずれかに変更します。

   - Exchange
   - [払い戻し](../customers/refunds-customer-account.md)
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

   ![新しいリターンの作成](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. 必要に応じて、 **[!UICONTROL Contact Email Address]** および **[!UICONTROL Comments]**.

   >[!NOTE]
   >
   >注文に複数の品目が含まれ、顧客が別の品目を返したい場合、クリックできます **[!UICONTROL Add Item To Return]**、項目を選択し、前述のすべてのオプションを設定します。

1. クリック数 **[!UICONTROL Submit]**.
