---
title: 注文ステータス
description: 事前定義済みの注文ステータスと、運用ニーズに合わせてカスタム注文ステータスを定義する方法について説明します。
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# 注文ステータス

すべての注文には、注文処理のステージに関連付けられた注文ステータスがあります [ワークフロー](order-processing.md).\
注文ステータスと注文ステータスの違いは次のとおりです **[!UICONTROL order states]** は、プログラムによって使用されます。 これらは、顧客や管理者ユーザーには表示されません。 注文の流れ、特定の状態の注文に対してどの操作が可能かを決定します。\
**[!UICONTROL Order statuses]** を使用して、注文のステータスを顧客および管理者ユーザーに伝えます。
運用ニーズに合わせて、追加の注文ステータスを作成できます。 注文ステータスは、注文のピッキングや配送の進行状況など、Adobe Commerce以外の進行状況を表示する場合に便利です。 注文処理ワークフローには影響しません。\
各注文ステータスは、注文ステータスに関連付けられています。 ストアには、事前に定義された一連の注文ステータスと注文ステータス設定があります。

![注文の状態とステータス](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

各注文のステータスはに表示されます。 _ステータス_ の列 _注文件数_ グリッド。

![注文ステータス](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>一部払い戻された注文は残っています `Processing` ステータスの期限 **_all_** 注文された商品（払い戻された商品を含む）が出荷されます。 注文のステータスが「」に変わりません `Complete` 注文のすべての商品が出荷されるまで。

## 注文の状態ワークフロー

![注文の状態ワークフロー](./assets/order-state-workflow.png)

## 事前定義済みステータス

| 注文ステータス | 状態コード |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 受信済み | `received` | このステータスは、非同期の注文プレースメントが有効な場合に配置される注文の初期ステータスです。 |
| 詐欺の疑い | `fraud` | PayPal または他の支払い方法で支払われた注文は、次のようにマークされることがあります。 _詐欺の疑い_. このステータスは、注文に請求書が発行されておらず、確認メールも送信されていないことを意味します。 |
| 処理中 | `processing` | 新規オーダーのステータスが「処理中」に設定されている場合、 _すべての品目を自動的に請求_ オプションが設定で使用できるようになります。 ギフトカード、ストアクレジット、報酬ポイント、またはその他のオフラインの支払い方法を使用して注文した場合、請求書は自動的には作成されません。 |
| 保留中の支払い | `pending_payment` | このステータスは、注文が作成され、PayPal または同様の支払い方法が使用される場合に使用されます。 つまり、顧客が支払いゲートウェイの web サイトに誘導されたが、返品情報はまだ受信されていないことを意味します。 このステータスは、顧客が支払う際に変更されます。 |
| 支払いの確認 | `payment_review` | このステータスは、PayPal 支払いレビューがオンの場合に表示されます。 |
| 保留中 | `pending` | このステータスは、請求書と出荷が送信されていないことを示します。 |
| 保留中 | `holded` | このステータスは手動でのみ割り当てることができます。 どんな注文でも保留にできます。 |
| 完了 | `complete` | このステータスは、注文が作成、支払い、顧客に出荷されることを意味します。 |
| クローズ | `closed` | このステータスは、受注がクレジット・メモに割り当てられ、顧客が払戻を受け取ったことを示します。 |
| キャンセル済み | `canceled` | このステータスは、管理者で手動で割り当てられます。または、一部の支払いゲートウェイでは、顧客が指定した時間内に支払わない場合に割り当てられます。 |
| 却下 | `rejected` | このステータスは、非同期注文処理中に注文が却下されたことを意味します。 これは、非同期注文の配置中にエラーが発生した場合に発生します。 |
| PayPal キャンセル取消 | `paypay_canceled_reversal` | このステータスは、PayPal が取消をキャンセルしたことを意味します。 |
| 保留中の PayPal | `pending_paypal` | このステータスは、注文が PayPal によって受け取られたが、支払いがまだ処理されていないことを意味します。 |
| PayPal 取消 | `paypal_reversed` | このステータスは、PayPal がトランザクションを取り消したことを意味します。 |

{style="table-layout:auto"}

## カスタム注文ステータス

プリセットの注文ステータス設定に加えて、独自のカスタム注文ステータス設定を作成し、それらを注文ステータスに割り当て、注文ステータスのデフォルトの注文ステータスを設定できます。 注文状態は、注文処理ワークフロー内の注文の位置を示し、注文ステータスは、注文の位置に意味のある翻訳可能なラベルを割り当てます。 例えば、次のようなカスタムの注文ステータスが必要な場合があります `packaging"`, `backordered`、またはニーズに固有のステータスです。 カスタムステータスにわかりやすい名前を作成し、ワークフロー内の関連する注文ステータスに割り当てることができます。

>[!NOTE]
>
>注文ワークフローでは、デフォルトのカスタム注文ステータス値のみが使用されます。 デフォルトとして設定されていないカスタムステータス値は、注文のコメントセクションでのみ使用できます。

![注文ステータスの設定](./assets/order-status.png){width="700" zoomable="yes"}

### カスタム注文ステータスの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. 右上隅のをクリックします。 **[!UICONTROL Create New Status]**.

   ![新しい注文ステータスを作成](./assets/order-status-new.png){width="600" zoomable="yes"}

1. を更新 _[!UICONTROL Order Status Information]_セクション：

   - を入力 **[!UICONTROL Status Code]** 内部参照用。 最初の文字は文字（a ～ z）である必要があり、残りは文字と数字（0 ～ 9）の任意の組み合わせにすることができます。 スペースの代わりにアンダースコア文字を使用します。

   - の場合 **[!UICONTROL Status Label]**：管理者とストアフロントの両方のステータス設定を識別するラベルを入力します。

1. が含まれる _[!UICONTROL Store View Specific Labels]_セクションで、異なるストアビューに必要なラベルを入力します。

1. クリック **[!UICONTROL Save Status]**.

### 注文ステータスの状態への割り当て

1. 日 _注文ステータス_ ページ、クリック **[!UICONTROL Assign Status to State]**.

   ![割り当てステータス](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. を更新 **[!UICONTROL Assignment Information]** セクションで、次の操作を行います。

   - を選択します。 **[!UICONTROL Order Status]** 割り当てる。 ステータスラベル別にリストされます。

   - を設定 **[!UICONTROL Order State]** をワークフロー内の注文ステータスが属する場所に送信します。

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** リストにはデフォルトの割り当て済み注文ステータスが含まれます。 例： `Pending` の代わりにデフォルトの注文ステータスが `New` 注文の状態の値。

   - このステータスを注文ステータスのデフォルトにするには、 **[!UICONTROL Use Order Status as Default]** チェックボックス。

     >[!NOTE]
     >
     >注文ワークフローでは、デフォルトの注文ステータスのみが使用されます。 デフォルト以外のステータスは、 **[!UICONTROL Order Comments]** 」セクションを選択します。

   - このステータスをストアフロントから表示するには、 **[!UICONTROL Visible On Storefront]** チェックボックス。

   ![状態を状態に割り当て](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Status Assignment]**.

### 既存の注文ステータスの編集

1. が含まれる _[!UICONTROL Order Status]_グリッドで、ステータスレコードを編集モードで開きます。

1. 必要に応じて、ステータス設定を更新します。

1. クリック **[!UICONTROL Save Status]**.

### 割り当て済み状態から注文ステータスを削除する

>[!NOTE]
>
>ステータスが使用中の場合は、ステータス設定のステータスからの割り当てを解除できません。

1. が含まれる _[!UICONTROL Order Status]_グリッドで、割り当て解除する注文ステータス レコードを検索します。

1. が含まれる _[!UICONTROL Action]_列の一番右の行で、**[!UICONTROL Unassign]**リンク。

   注文ステータスが未割り当てであることを示すメッセージがワークスペースの上部に表示されます。 注文ステータスラベルはリスト内に残りますが、状態に割り当てられなくなります。 注文ステータス設定は削除できません。

>[!NOTE]
>
>デフォルトの注文ステータスが注文ステータスから割り当てられていない場合、 _**別の**_ 注文ステータス : _**自動的に設定**_ この注文状態のデフォルトとして。

## 通知

顧客は、次の方法で注文のステータスを追跡できます [RSS フィード](../merchandising-promotions/social-rss.md) 設定で「RSS フィードを注文」が有効になっている場合。 有効化すると、各注文に RSS フィードへのリンクが表示されます。

### 注文ステータス通知を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL RSS Feeds]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Order]** セクション。

1. を設定 **[!UICONTROL Customer Order Status Notification]** 対象： `Enable`.

   ![顧客注文ステータス通知](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

### 新規注文のメール通知を設定する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Sales Emails]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Order]** セクション。

   ![設定 – 注文オプション](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL New Order Confirmation Email Sender]** を次のいずれかに変更します。

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. 顧客タイプごとに使用するテンプレートを選択します。

   - **[!UICONTROL New Order Confirmation Template]**  – 登録済みのストアアカウントを持つ顧客に使用するテンプレートを選択します。
   - **[!UICONTROL New Order Confirmation Template for Guest]**  – 登録済みのストアアカウントを持たないゲスト顧客に使用するテンプレートを選択します。

1. 新しい注文について別の担当者（ビジネス マネージャなど）に通知するには、電子メール アドレスを **[!UICONTROL Send Order Email Copy To]**.

   複数の受信者が必要な場合は、複数のメールアドレスを追加できます。

1. を **[!UICONTROL Send Order Email Copy Method]** を次のいずれかに変更します。

   - `Bcc`  – 新しい注文に関するメールが 1 つだけ顧客と追加の受信者の両方に送信されるが、顧客が受け取ったメールが追加の受信者にも送信されたことは確認されない。
   - `Separate Email` - 2 通のメールが別々に送信されます。1 つは受信者に、もう 1 つは顧客に送信されます。

1. 完了したら、 **[!UICONTROL Save Config]**.
