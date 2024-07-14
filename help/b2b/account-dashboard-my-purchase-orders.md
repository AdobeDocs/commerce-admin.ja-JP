---
title: "[!UICONTROL My Purchase Orders]"
description: 発注書と、それを使用して企業が購入を管理する方法について説明します。
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

発注書が [ 会社に対して有効 ](purchase-order-flow.md) になっている場合、会社のユーザーアカウントにサインインした顧客の注文はすべて発注書（PO）として自動的に作成されます。 必要な権限を持つ会社ユーザーは、下位ユーザーが作成した PO と共に、自分が作成した PO を作成、編集および削除できます。

![ 自分の発注書 ](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>発注：品目価格、値引および受注作成時の出荷価格の _スナップショット_ を作成します。 発注の作成後に品目の価格が変更された場合は、元の価格が使用されます。

## 発注書の管理

顧客は _役割の権限_ に応じて、「発注の表示 [ ページから発注を管理でき ](account-company-roles-permissions.md) す。

- 発注を表示するには、「**[!UICONTROL View]**」をクリックします。
- 発注に関するコメントを表示するには、「**[!UICONTROL Comments]**」タブをクリックします。
- すべての注文履歴を表示するには、「**[!UICONTROL History Log]**」タブをクリックします。

>[!IMPORTANT]
>
>発注書の品目が在庫切れか、または使用可能な数量が不十分な場合、発注書が実際の注文に変換されると、エラーが発生します。 バックオーダーが有効な場合、オーダーは通常どおり処理されます。

## 既存の発注書からの新しい発注書

顧客が既存の発注を持っていて、新しい品目を追加する場合は、新しい発注に追加された新しい製品を使用して、重複する発注を生成できます。 お客様は次の手順を完了します。

1. _自分の発注書_ ページで、顧客は発注書を見つけ、**[!UICONTROL View]** リンクをクリックします。

1. 顧客は「**[!UICONTROL Add Items to Shopping Cart]**」をクリックします。

   買い物かごページが開き、すべての項目がリストされます。

1. 追加や変更を行います。

1. （任意） **[!UICONTROL Custom Reference Number]** を使用して、注文に内部請求書/発注書番号を追加します。

1. 通常のチェックアウトワークフローに従い、**[!UICONTROL Place Purchase Order]** をクリックします。

買い物かごにアイテムがある状態でクリックすると、ダ _[!UICONTROL Add Items to Shopping Cart]_アログが表示されます。 このダイアログでは、買い物かごの項目を新しい項目と結合するか、買い物かごの項目を発注書内の項目に置き換えるかを選択できます。

元の発注書は、不要になった場合はクローズできます。

## 発注書承認

会社の構造に基づいて承認者として指定された顧客、または会社の役割が割り当てられた顧客の場合、_[!UICONTROL My Purchase Orders]_ダッシュボードページには「**[!UICONTROL Requires My Approval]**」タブが表示されます。 顧客はこのタブをクリックして、承認待ちの PO を確認します。 カウンターには、承認待ちの注文の数が表示されます。

発注の「**[!UICONTROL View]**」をクリックし、詳細をレビューした後、承認者は「**[!UICONTROL Approve]**」または「**[!UICONTROL Reject]**」をクリックできます。

### 一括承認/却下

Adobe Commerce 2.4.1 以降では、承認者は一度に複数の発注書を承認または却下できます。

1. _[!UICONTROL My Purchase Order]_ページで、「**[!UICONTROL Requires My Approval]**」タブをクリックします。

1. 承認または拒否する各発注書のチェックボックスを選択します。

1. **[!UICONTROL Approve Selected]** または **[!UICONTROL Reject Selected]** をクリックします。

顧客は、アクションが許可されているステータスの発注書のみを選択できます。 会社管理者は、会社内のアクティブな発注書に対して一括承認または却下を行うことができます。
