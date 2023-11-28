---
title: "[!UICONTROL My Purchase Orders]"
description: 発注書について、および企業が発注書を使用して購入を管理する方法について説明します。
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

発注が [会社に対して有効](purchase-order-flow.md)に設定すると、顧客が会社のユーザーアカウントにサインインした場合、その顧客の注文は自動的に発注書 (PO) として作成されます。 必要な権限を持つ会社のユーザーは、自分が作成する発注書の作成、編集、削除と、下位のユーザーが作成した発注書の作成、編集、削除をおこなうことができます。

![自分の発注書](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>発注書による _スナップショット_ 注文が作成された時点での品目価格、割引、および送料の。 発注の作成後に品目の価格が変更された場合は、元の価格が使用されます。

## 発注書の管理

次から： _発注書の表示_ ページに表示される場合、顧客は自分のページに応じて PO を管理できます [役割の権限](account-company-roles-permissions.md).

- PO を確認するには、 **[!UICONTROL View]**.
- PO に関するコメントを表示するには、 **[!UICONTROL Comments]** タブをクリックします。
- 完全な注文履歴を確認するには、 **[!UICONTROL History Log]** タブをクリックします。

>[!IMPORTANT]
>
>発注書の品目が在庫切れの場合、または在庫数量が不十分な場合は、発注書が実際の注文に変換されると、エラーが発生します。 バックオーダーが有効な場合、オーダーは通常どおり処理されます。

## 既存の発注書からの新しい発注書

顧客が既存の発注書を持ち、新しい品目を追加する場合は、新しい商品が新しい発注書に追加された重複発注を生成できます。 顧客は次の手順を完了します。

1. 次の日： _自分の発注書_ ページで、顧客が発注書を検索して **[!UICONTROL View]** リンク。

1. 顧客がクリックする **[!UICONTROL Add Items to Shopping Cart]**.

   すべての項目が表示された状態で、[ 買い物かご ] ページが開きます。

1. 追加や変更を行います。

1. （オプション） **[!UICONTROL Custom Reference Number]** 内部請求書/発注番号を受注に追加します。

1. 通常のチェックアウトワークフローとクリックに従います。 **[!UICONTROL Place Purchase Order]**.

クリック時に買い物かごに品目が入っている場合 _[!UICONTROL Add Items to Shopping Cart]_をクリックすると、ダイアログが表示されます。 このダイアログでは、買い物かごの品目を新しい品目と結合するか、買い物かごの品目を発注の品目と置き換えるかを選択できます。

元の発注書は不要になった場合はクローズできます。

## 発注書承認

会社構造または割り当てられた会社の役割に基づいて承認者として指定されているお客様の場合、 _[!UICONTROL My Purchase Orders]_ダッシュボードページには、**[!UICONTROL Requires My Approval]**タブをクリックします。 顧客がこのタブをクリックして、承認を待っている発注を確認します。 カウンターは、承認を待っている注文の数を示します。

クリック後 **[!UICONTROL View]** 発注の場合は、承認者は、 **[!UICONTROL Approve]** または **[!UICONTROL Reject]**.

### 一括承認/却下

Adobe Commerce 2.4.1 以降、承認者は一度に複数の発注を承認または拒否できます。

1. 次の日： _[!UICONTROL My Purchase Order]_ページで、**[!UICONTROL Requires My Approval]**タブをクリックします。

1. 承認または却下する各発注のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Approve Selected]** または **[!UICONTROL Reject Selected]**.

顧客は、ステータスが「アクションを許可する」の発注書のみを選択できます。 会社の管理者は、会社内のアクティブな発注書に対して一括承認または却下をおこなうことができます。
