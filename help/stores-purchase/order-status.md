---
title: 注文ステータス
description: 事前定義済みの注文ステータスと、運用上のニーズに合わせてカスタム注文ステータスを定義する方法について説明します。
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# 注文ステータス

すべてのオーダーには、オーダー処理のステージに関連付けられたオーダー・ステータスがあります。 [workflow](order-processing.md).\
注文状態と注文ステータスの違いは、 **[!UICONTROL order states]** は、プログラムによって使用されます。 ユーザーや管理者ユーザーには表示されません。 オーダーのフローと、特定の状態でオーダーに対して実行可能な操作を決定します。\
**[!UICONTROL Order statuses]** は、注文のステータスを顧客および管理者ユーザーに伝えるために使用します。
オペレーショナルニーズに合わせて、追加のオーダーステータスを作成できます。 注文ステータスは、Adobe Commerce以外で進捗を表示する場合に便利です。例えば、注文のピッキングや配信の進捗を表示できます。 これらの指標は、注文処理ワークフローには影響しません。\
各注文ステータスは、注文状態に関連付けられます。 ストアには、事前に定義された注文ステータスと注文状態の設定が含まれています。

![注文の状態とステータス](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

各注文のステータスは、 _ステータス_ 列 _購入回数_ グリッド。

![注文ステータス](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>一部払い戻しの命令が残る `Processing` 次の日まで **_すべて_** 発注済品（払い戻し済品を含む）が出荷されます。 注文のステータスは、 `Complete` 注文のすべての品目が出荷されるまで。

## 注文状態のワークフロー

![注文状態のワークフロー](./assets/order-state-workflow.png)

## 事前定義済みのステータス

| 注文ステータス | ステータスコード |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 受信済み | `received` | このステータスは、非同期の注文配置が有効な場合に発行される注文の初期ステータスです。 |
| 詐欺の疑い | `fraud` | PayPal または別の支払いゲートウェイを通じて支払われた注文が、 _詐欺の疑い_. このステータスは、注文に請求書が発行されておらず、確認 E メールも送信されないことを意味します。 |
| 処理中 | `processing` | 新しい注文のステータスが「処理中」に設定されている場合、 _すべての項目を自動的に請求_ オプションが設定で使用可能になります。 請求書は、ギフトカード、店舗クレジット、報酬ポイント、またはその他のオフラインの支払い方法を使用して行われた注文に対しては、自動的に作成されません。 |
| 支払保留中 | `pending_payment` | このステータスは、注文が作成され、PayPal または類似の支払い方法が使用された場合に使用されます。 顧客が支払いゲートウェイの Web サイトに向けられたが、返品情報がまだ受け取られていないことを意味します。 このステータスは、顧客が支払う際に変更されます。 |
| 支払いレビュー | `payment_review` | このステータスは、PayPal の支払確認が有効になっている場合に表示されます。 |
| 保留中 | `pending` | このステータスは、請求書および出荷が送信されていないことを示します。 |
| 保留中 | `holded` | このステータスは手動でのみ割り当てることができます。 どんな注文でも保留にできます。 |
| 完了 | `complete` | このステータスは、注文が作成、支払われ、顧客に出荷されたことを意味します。 |
| 閉じる | `closed` | このステータスは、注文にクレジットメモが割り当てられ、顧客が返金を受け取ったことを示します。 |
| キャンセル | `canceled` | このステータスは、管理者で手動で割り当てられます。また、一部の支払いゲートウェイでは、顧客が指定期間内に支払われない場合に割り当てられます。 |
| 却下 | `rejected` | このステータスは、非同期の注文処理中に注文が却下されたことを意味します。 これは、非同期の注文配置中に en エラーが発生した場合に発生します。 |
| PayPal キャンセル済取消 | `paypay_canceled_reversal` | このステータスは、PayPal が取り消しをキャンセルしたことを意味します。 |
| PayPal の保留 | `pending_paypal` | このステータスは、注文が PayPal によって受け取られたが、支払いがまだ処理されていないことを意味します。 |
| PayPal 取り消し | `paypal_reversed` | このステータスは、PayPal がトランザクションを元に戻したことを意味します。 |

{style="table-layout:auto"}

## カスタム注文ステータス

事前設定された注文ステータス設定に加えて、独自のカスタム注文ステータス設定を作成し、それらを注文ステータスに割り当てたり、注文ステータスのデフォルトの注文ステータスを設定したりできます。 オーダー状態は、オーダー処理ワークフロー内のオーダーの位置を示し、オーダー状態は、オーダーの位置に意味のある翻訳可能なラベルを割り当てます。 例えば、次のようなカスタムの注文ステータスが必要な場合があります。 `packaging"`, `backordered`または必要に応じたステータス。 カスタムステータスのわかりやすい名前を作成し、ワークフロー内の関連する注文状態に割り当てることができます。

>[!NOTE]
>
>オーダーワークフローでは、デフォルトのカスタムオーダーステータス値のみが使用されます。 デフォルトとして設定されていないカスタムステータス値は、注文のコメントセクションでのみ使用できます。

![注文ステータスの設定](./assets/order-status.png){width="700" zoomable="yes"}

### カスタムの注文ステータスの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. 右上隅で、 **[!UICONTROL Create New Status]**.

   ![新しい注文ステータスの作成](./assets/order-status-new.png){width="600" zoomable="yes"}

1. を更新します。 _[!UICONTROL Order Status Information]_セクション：

   - を入力します。 **[!UICONTROL Status Code]** 内部参照用。 最初の文字は文字 (a ～ z) で、残りの文字は文字と数字の任意の組み合わせ (0 ～ 9) である必要があります。 スペースの代わりにアンダースコア文字を使用します。

   - の場合 **[!UICONTROL Status Label]**&#x200B;の場合は、管理者とストアフロントの両方でステータス設定を識別するラベルを入力します。

1. Adobe Analytics の _[!UICONTROL Store View Specific Labels]_「 」セクションで、異なるストアビューに必要なラベルを入力します。

1. クリック **[!UICONTROL Save Status]**.

### 州への注文ステータスの割り当て

1. 次の日： _注文ステータス_ ページ、クリック **[!UICONTROL Assign Status to State]**.

   ![ステータスの割り当て](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. を更新します。 **[!UICONTROL Assignment Information]** セクションで、以下の操作を実行します。

   - を選択します。 **[!UICONTROL Order Status]** 割り当てる対象。 これらは、ステータスラベル別に表示されます。

   - 設定 **[!UICONTROL Order State]** を、ワークフロー内の注文ステータスが属する場所に追加します。

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** リストには、デフォルトで割り当てられた注文ステータスが含まれます。 例えば、 `Pending` デフォルトの注文ステータスが、 `New` 注文状態の値。

   - このステータスを注文状態のデフォルトにするには、 **[!UICONTROL Use Order Status as Default]** チェックボックス。

     >[!NOTE]
     >
     >オーダーワークフローでは、デフォルトのオーダーステータスのみが使用されます。 デフォルト以外のステータスは、 **[!UICONTROL Order Comments]** 」セクションをクリックします。

   - このステータスをストアフロントに表示するには、「 **[!UICONTROL Visible On Storefront]** チェックボックス。

   ![ステータスを州に割り当て](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Status Assignment]**.

### 既存の注文ステータスの編集

1. Adobe Analytics の _[!UICONTROL Order Status]_グリッドで、編集モードでステータスレコードを開きます。

1. 必要に応じてステータス設定を更新します。

1. クリック **[!UICONTROL Save Status]**.

### 割り当て済みの状態から注文ステータスを削除する

>[!NOTE]
>
>ステータスが使用中の場合、状態からステータス設定の割り当てを解除することはできません。

1. Adobe Analytics の _[!UICONTROL Order Status]_グリッドで、未割り当てにする注文ステータス・レコードを検索します。

1. Adobe Analytics の _[!UICONTROL Action]_行の右端にある列で、**[!UICONTROL Unassign]**リンク。

   オーダーのステータスが未割り当てになっているというメッセージがワークスペースの上部に表示されます。 注文ステータスラベルは引き続きリストに表示されますが、ステータスに割り当てられなくなりました。 注文ステータス設定は削除できません。

>[!NOTE]
>
>デフォルトの注文ステータスが注文状態から割り当てられていない場合、 _**別の**_ 注文ステータス： _**自動的に設定**_ をこの注文状態のデフォルトとして使用します。

## 通知

顧客は、 [RSS フィード](../merchandising-promotions/social-rss.md) （設定で注文 RSS フィードが有効になっている場合）。 有効にすると、RSS フィードへのリンクが各注文に表示されます。

### 注文ステータス通知を有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL RSS Feeds]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Order]** 」セクションに入力します。

1. 設定 **[!UICONTROL Customer Order Status Notification]** から `Enable`.

   ![顧客の注文ステータスの通知](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

### 新しい注文の電子メール通知を設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales Emails]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Order]** 」セクションに入力します。

   ![設定 — 順序オプション](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL New Order Confirmation Email Sender]** を次のいずれかに変更します。

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. 各顧客タイプで使用するテンプレートを選択します。

   - **[!UICONTROL New Order Confirmation Template]**  — 登録済みストアアカウントを持つ顧客に使用するテンプレートを選択します。
   - **[!UICONTROL New Order Confirmation Template for Guest]**  — ストアアカウントを登録していないゲスト顧客に使用するテンプレートを選択します。

1. 新しい注文を別の人（ビジネスマネージャーなど）に通知するには、次の電子メールアドレスを入力します： **[!UICONTROL Send Order Email Copy To]**.

   複数の受信者が必要な場合は、複数の電子メールアドレスを追加できます。

1. を設定します。 **[!UICONTROL Send Order Email Copy Method]** を次のいずれかに変更します。

   - `Bcc`  — 新しい注文に関する電子メールが 1 つだけ顧客と追加の受信者の両方に送信されますが、受信した電子メールも追加の受信者に送信されたと顧客には見えません。
   - `Separate Email` - 2 つの異なる E メールが送信されます。1 つは受信者に、もう 1 つは顧客に対してです。

1. 完了したら、「 **[!UICONTROL Save Config]**.
