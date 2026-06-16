---
title: '[!UICONTROL My Purchase Orders]'
description: 発注と、それを使用して購買を管理する方法について説明します。
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
TQID: https://experienceleague.adobe.com/3Vb9ux3eccHF7GUlNdiKIkc12vLFNJv9R3Rkz81ch4M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

会社[&#128279;](purchase-order-flow.md)に対して発注書が有効になっている場合、会社のユーザーアカウントにサインインしている顧客に対する注文は、発注書（PO）として自動的に作成されます。 必要な権限を持つ会社ユーザーは、自分が作成したPOと、下位ユーザーが作成したPOを作成、編集および削除できます。

![自分の発注書](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>注文作成時に、商品の価格、割引、配送価格の&#x200B;_スナップショット_&#x200B;が作成されます。 POの作成後に商品の価格が変更された場合は、元の価格が使用されます。

## 発注の管理

_発注書を表示_ ページから、お客様は[役割の権限](account-company-roles-permissions.md)に応じてPOを管理できます。

- POを表示するには、**[!UICONTROL View]**&#x200B;をクリックします。
- POに関するコメントを表示するには、「**[!UICONTROL Comments]**」タブをクリックします。
- 完全な注文履歴を表示するには、「**[!UICONTROL History Log]**」タブをクリックします。

>[!IMPORTANT]
>
>発注の品目が在庫切れであるか、数量が不足している場合、発注が実際の注文に変換されると、エラーが発生します。 バックオーダーが有効になっている場合、注文は正常に処理されます。

## 既存の発注からの新規発注

お客様が既存の発注書を持っていて、新しい品目を追加したい場合は、新しい製品を新しい発注書に追加した状態で、重複した発注書を生成できます。 お客様は次の手順を実行します。

1. _My Purchase Order_ ページで、お客様は発注書を見つけ、**[!UICONTROL View]** リンクをクリックします。

1. お客様は&#x200B;**[!UICONTROL Add Items to Shopping Cart]**&#x200B;をクリックします。

   ショッピングカートページが開き、すべてのアイテムが表示されます。

1. 追加や変更を加えます。

1. （オプション） **[!UICONTROL Custom Reference Number]**&#x200B;を使用して、内部請求書/PO番号を注文に追加します。

1. 通常のチェックアウト ワークフローに従って、**[!UICONTROL Place Purchase Order]**&#x200B;をクリックします。

_[!UICONTROL Add Items to Shopping Cart]_&#x200B;をクリックしたときに買い物かごにアイテムがある場合は、ダイアログが表示されます。 このダイアログでは、買い物かごのアイテムを新しいアイテムに結合するか、買い物かごのアイテムをPOのアイテムに置き換えるかを選択できます。

元の発注は、不要になった場合にクローズできます。

## 発注の承認

会社構造または割り当てられた会社の役割に基づいて承認者として指定された顧客の場合、_[!UICONTROL My Purchase Orders]_&#x200B;ダッシュボードページには「**[!UICONTROL Requires My Approval]**」タブが表示されます。 お客様は、このタブをクリックして、承認を待っているPOを確認します。 カウンターには、承認待ちの注文数が表示されます。

発注書の&#x200B;**[!UICONTROL View]**&#x200B;をクリックし、詳細を確認した後、承認者は&#x200B;**[!UICONTROL Approve]**&#x200B;または&#x200B;**[!UICONTROL Reject]**&#x200B;をクリックできます。

### 一括承認/却下

Adobe Commerce 2.4.1以降、承認者は一度に複数の発注を承認または却下できます。

1. _[!UICONTROL My Purchase Order]_&#x200B;ページで、「**[!UICONTROL Requires My Approval]**」タブをクリックします。

1. 承認または却下する各発注のチェックボックスを選択します。

1. **[!UICONTROL Approve Selected]**&#x200B;または&#x200B;**[!UICONTROL Reject Selected]**&#x200B;をクリックします。

顧客は、アクションを許可するステータスを持つ発注のみを選択できます。 会社の管理者は、会社のアクティブな発注に対して一括承認または却下を行うことができます。
