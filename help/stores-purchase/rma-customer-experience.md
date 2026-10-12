---
title: ストアフロント体験を返す
description: 顧客がストアフロントのアカウントから返品を管理する方法をご紹介します。
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
TQID: 'https://experienceleague.adobe.com/erAT7FtUSif5CxrBLlANMQY2aowkv0MDzkqXQnzzF7Q'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: ac07462c-732c-5c1c-947b-4ce533b4fcfb
    internal-label: Returns
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%
---
# ストアフロント体験を返す

{{ee-feature}}

顧客は、次のいずれかを使用して、ストアフロントからRMAをリクエストできます。

- サイドバーの[注文と返品ウィジェット &#x200B;](../content-design/widget-orders-returns.md)
- フッターの&#x200B;_注文と返品_ リンク

ベストプラクティスとして、カスタマーサービスポリシーに、RMAの要件とプロセスの説明を必ず含めてください。

>[!NOTE]
>
>返品に関連する追加情報を収集する場合は、独自のカスタム [返品属性](attributes-returns.md)を追加できます。

すべての顧客RMA情報は、顧客アカウントダッシュボードの&#x200B;**[!UICONTROL My Returns]** ページに表示されます。

![返品数](./assets/my-returns-page.png){width="700" zoomable="yes"}

## RMAの導入を検討

お客様は、ストアフロントで次の手順を実行してRMAを送信します。

1. フッターで、**[!UICONTROL Orders and Returns]**&#x200B;をクリックします。

1. 注文情報を入力します。

   - 注文ID
   - 請求先姓
   - メール

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

   ![注文と返品](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. 注文日の下で、**[!UICONTROL Return]**&#x200B;をクリックします。

   ![注文の詳細](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. 返す項目を選択し、**[!UICONTROL Quantity to Return]**&#x200B;を入力します。

1. **[!UICONTROL Resolution]**&#x200B;を次のいずれかに設定します。

   - Exchange
   - [返金](../customers/refunds-customer-account.md)
   - [ストアクレジット](../customers/store-credit-using.md)

1. **[!UICONTROL Item Condition]**&#x200B;を次のいずれかに設定します。

   - `Unopened`
   - `Opened`
   - `Damaged`

1. **[!UICONTROL Reason to Return]**&#x200B;を次のいずれかに設定します。

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![新しいReturn](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}を作成

1. 必要に応じて、**[!UICONTROL Contact Email Address]**&#x200B;と&#x200B;**[!UICONTROL Comments]**&#x200B;を設定します。

   >[!NOTE]
   >
   >注文に複数の項目が含まれており、顧客が別の項目を返す場合は、**[!UICONTROL Add Item To Return]**&#x200B;をクリックし、項目を選択してから、すべてのオプションを設定できます。

1. **[!UICONTROL Submit]**&#x200B;をクリックします。
