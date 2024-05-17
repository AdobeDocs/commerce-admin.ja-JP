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

発注書が次の場合 [会社に対して有効](purchase-order-flow.md)の場合、会社のユーザーアカウントにログインした顧客からの注文は、発注書（PO）として自動的に作成されます。 必要な権限を持つ会社ユーザーは、下位ユーザーが作成した PO と共に、自分が作成した PO を作成、編集および削除できます。

![自分の発注書](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>発注による作成 _スナップショット_ 品目価格、値引きおよび受注作成時の出荷価格の合計です。 発注の作成後に品目の価格が変更された場合は、元の価格が使用されます。

## 発注書の管理

から _発注書の表示_ ページに移動すると、顧客は顧客に応じて PO を管理できます [役割の権限](account-company-roles-permissions.md).

- PO を確認するには、をクリックします **[!UICONTROL View]**.
- PO に関するコメントを表示するには、 **[!UICONTROL Comments]** タブ。
- すべての注文履歴を表示するには、 **[!UICONTROL History Log]** タブ。

>[!IMPORTANT]
>
>発注書の品目が在庫切れか、または使用可能な数量が不十分な場合、発注書が実際の注文に変換されると、エラーが発生します。 バックオーダーが有効な場合、オーダーは通常どおり処理されます。

## 既存の発注書からの新しい発注書

顧客が既存の発注を持っていて、新しい品目を追加する場合は、新しい発注に追加された新しい製品を使用して、重複する発注を生成できます。 お客様は次の手順を完了します。

1. 日 _自分の発注_ ページを開き、顧客が発注書を見つけて、 **[!UICONTROL View]** リンク。

1. 顧客のクリック数 **[!UICONTROL Add Items to Shopping Cart]**.

   買い物かごページが開き、すべての項目がリストされます。

1. 追加や変更を行います。

1. （任意）を使用します **[!UICONTROL Custom Reference Number]** 受注に社内請求書/発注番号を追加する手順は、次のとおりです。

1. 通常のチェックアウトワークフローとクリックに従う **[!UICONTROL Place Purchase Order]**.

クリック時に買い物かごにアイテムがある場合 _[!UICONTROL Add Items to Shopping Cart]_を選択すると、ダイアログが表示されます。 このダイアログでは、買い物かごの項目を新しい項目と結合するか、買い物かごの項目を発注書内の項目に置き換えるかを選択できます。

元の発注書は、不要になった場合はクローズできます。

## 発注書承認

会社の構造に基づいて承認者として指定された顧客、または会社の役割を割り当てられた顧客の場合、 _[!UICONTROL My Purchase Orders]_ダッシュボードページには、**[!UICONTROL Requires My Approval]**タブ。 顧客はこのタブをクリックして、承認待ちの PO を確認します。 カウンターには、承認待ちの注文の数が表示されます。

クリック後 **[!UICONTROL View]** 発注および詳細のレビューの場合、承認者は次の項目をクリックできます **[!UICONTROL Approve]** または **[!UICONTROL Reject]**.

### 一括承認/却下

Adobe Commerce 2.4.1 以降では、承認者は一度に複数の発注書を承認または却下できます。

1. 日 _[!UICONTROL My Purchase Order]_ページで、**[!UICONTROL Requires My Approval]**タブ。

1. 承認または拒否する各発注書のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Approve Selected]** または **[!UICONTROL Reject Selected]**.

顧客は、アクションが許可されているステータスの発注書のみを選択できます。 会社管理者は、会社内のアクティブな発注書に対して一括承認または却下を行うことができます。
