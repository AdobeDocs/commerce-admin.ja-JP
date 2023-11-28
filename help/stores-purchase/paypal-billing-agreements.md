---
title: PayPal 請求契約
description: PayPal の請求契約およびストア内での支払い方法をサポートする方法を説明します。
exl-id: b0800b41-816a-4c48-a54d-41ddc1d586ce
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# PayPal 請求契約

お客様は、決済プロセスを簡単にするために、支払いサービスプロバイダーとして PayPal との請求契約を締結できます。 チェックアウト時に、顧客は支払い方法として請求契約を選択します。 支払いシステムは、請求契約を一意の番号で検証し、顧客アカウントに請求します。 請求契約が設定されているため、顧客が購入ごとに支払い情報を入力する必要がなくなりました。 顧客は、顧客アカウントのダッシュボードから請求契約を管理できます。このダッシュボードでは、各顧客のステータスが次のように表示されます。 _アクティブ_ または _キャンセル_. 請求契約がキャンセルされると、再アクティブ化できません。

## 請求契約ワークフロー

1. **顧客が請求契約にサインアップする**. 請求契約が設定された後、追加の請求契約は顧客アカウントからのみ追加できます。 顧客が作成できる請求契約の数に制限はありません。 顧客は、次のいずれかの方法を使用して請求契約に新規登録できます。

   - **顧客アカウントにサインアップ** ：顧客は、顧客アカウントから請求契約に新規登録できます。
   - **チェックアウト時にサインアップ** - PayPal Express Checkout を使用して購入を支払うお客様は、チェックボックスをマークして請求契約を作成できます。 請求契約は現在の注文には使用されませんが、顧客が次回注文を行ったときに、支払い方法オプションとして使用できるようになります。
   - **ストア管理者によるサインアップ**  — 顧客のリクエストに応じて、店舗管理者は顧客の請求契約を使用して販売注文を作成できます。

1. **PayPal が契約を検証し、記録**. 顧客が請求契約で支払いを行うと、請求契約基準 ID と販売注文支払詳細が PayPal に転送され、参照情報と共に顧客アカウントに記録される。 支払いが許可されている場合、注文は Commerce で作成されます。 請求契約参照 ID は、顧客とストアに送信されます。

## 請求契約の管理

The _[!UICONTROL Billing Agreements]_ページには、お客様と店舗の顧客との間のすべての請求契約が一覧表示されます。 マーチャントは、請求契約参照 ID、ステータス、作成日など、顧客または請求契約情報でレコードをフィルタリングできます。 各レコードには、請求契約に関する一般情報と、支払い方法として使用したすべての販売注文が含まれます。 顧客請求契約を表示、キャンセル、または削除できます。 キャンセルされた請求契約は、ストア管理者のみが削除できます。

### 請求契約の表示

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. リストで請求契約を探し、クリックして開きます。

各請求契約ページには、次の 2 つのタブが表示されます。 _[!UICONTROL General Information]_および_[!UICONTROL Related Orders]_.

#### 一般情報

このタブには、請求契約に関する一般情報が含まれます。

- [!UICONTROL Reference ID]：現在の請求契約に割り当てられる一意の数値識別子。
- [!UICONTROL Customer]：現在の請求契約に割り当てられた顧客のアカウント。
- [!UICONTROL Status]：支払い契約のステータス。
- [!UICONTROL Created At]：作成日。
- [!UICONTROL Updated At]：更新日。

![請求契約表示](./assets/billing-agreement-view.png){width="600" zoomable="yes"}

#### 関連する注文

このタブには、現在の請求契約を使用して行われた注文のリストが表示されます。

![請求契約表示](./assets/billing-agreement-related-orders.png){width="600" zoomable="yes"}

### 請求契約のキャンセル

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. リストで請求契約を探し、クリックして開きます。

1. 右上隅で、 **[!UICONTROL Cancel]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

### 請求契約の削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. リストで請求契約を探し、クリックして開きます。

1. 右上隅で、 **[!UICONTROL Delete]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

### 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 各請求契約に割り当てられる一意の数値識別子 |
| [!UICONTROL Email] | 顧客の連絡先 E メール |
| [!UICONTROL First Name] | 顧客の名 |
| [!UICONTROL Last Name] | 顧客の姓 |
| [!UICONTROL Reference ID] | 各請求契約に割り当てられる一意の数値参照 ID |
| [!UICONTROL Status] | 支払契約ステータス。 オプション： `Active` または `Canceled` |
| [!UICONTROL Created] | 作成日 |
| [!UICONTROL Updated] | 更新日 |

{style="table-layout:auto"}

## ストアフロントエクスペリエンス

支払いプロバイダーとの請求契約を締結した顧客は、契約に従って、今すぐ購入を行い、後で支払うことができます。 The

![顧客のダッシュボードの請求契約リスト](./assets/billing-agreements-dashboard.png){width="700" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Reference ID] | 各請求契約に割り当てられる一意の数値参照 ID |
| [!UICONTROL Status] | 支払契約ステータス。 オプション： `Active` または `Canceled` |
| [!UICONTROL Created At] | 作成日 |
| [!UICONTROL Updated At] | 更新日 |
| [!UICONTROL Payment Method] | 請求契約の支払いプロバイダー |
| [!UICONTROL View] | 請求契約の表示に使用するボタン |

{style="table-layout:auto"}

### 請求契約の作成

1. 顧客がアカウントダッシュボードから **[!UICONTROL Billing Agreements]**.

1. の下 **[!UICONTROL New Billing Agreement]**：支払いプロバイダーを選択します。

1. クリック **[!UICONTROL Create]**.

このアクションは、顧客を支払いシステム Web サイトにリダイレクトします。

![顧客アカウントダッシュボードでの新しい請求契約](./assets/create-billing-agreement-dashboard.png){width="700" zoomable="yes"}

### 請求契約の表示

1. 顧客がアカウントダッシュボードから **[!UICONTROL Billing Agreements]**.

1. 請求契約を選択し、クリックします **[!UICONTROL View]**.

![顧客のダッシュボードで請求契約を表示](./assets/view-billing-agreement.png){width="700" zoomable="yes"}

### 請求契約のキャンセル

1. 顧客がアカウントダッシュボードから **[!UICONTROL Billing Agreements]**.

1. 請求契約を選択し、クリックします **[!UICONTROL View]**.

1. 右上隅で、 **[!UICONTROL Cancel]** その後 **[!UICONTROL OK]** をクリックして確定します。

>[!NOTE]
>
>管理者ユーザー（商人）が請求契約をキャンセルした場合、ストアフロントでキャンセルすることはできません。 The _キャンセル_ この契約のステータスが表示されます。
