---
title: イベント招待状
description: 顧客がイベントや個人販売への招待状を顧客アカウントのダッシュボードから送信および表示する方法について説明します。
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# イベント招待状

{{ee-feature}}

招待状を有効にすると、顧客は、顧客アカウントのダッシュボードから招待状を送信および表示できます。 招待メールには、ストアのカスタマーログインページへのリンクが含まれています。

## マイ招待状

この _[!UICONTROL My Invitations]_顧客アカウントの「」セクションには、顧客から送信されたすべての招待状が一覧表示されます。 お客様は、店舗のイベント、ギフト登録、ウィッシュリストなどに関する招待状を友人や家族に送信できます。

![マイ招待状](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### 招待ワークフロー

1. **顧客が招待状を準備**：アカウントダッシュボードから、顧客が受信者のリストを準備して、招待を完了します。 設定に応じて、カスタムメッセージを含めることができます。
1. **顧客が招待状を送信します**：準備ができたら、顧客が _[!UICONTROL Send Invitations]_ボタン。
1. **システムが送信を管理**：設定で設定された数に従って、システムが招待状をバッチで送信します。
1. **顧客が応答を監視**：顧客は、次のように、アカウントダッシュボードから各招待のステータスを監視します `Sent`, `Accepted`、または `Canceled`.

### 招待状を送信

1. ストアフロントのアカウントのサイドバーで、顧客は次のいずれかを選択します **[!UICONTROL My Invitations]**.

1. 日 _マイ招待状_ ページ、クリック **[!UICONTROL Send Invitation]**.

1. 新しい招待状項目を定義します。

   - 電子メール情報を完了します。

   - （オプション）をクリックして複数アドレスの招待を作成します **+** 別のメールアドレスを追加する方法も説明します。

     1 人の招待メールには 5 つのメールアドレス制限があります。

   - （任意）付随するメッセージを入力します。

1. 完了したら、をクリックします **[!UICONTROL Send Invitation]**.

招待されたユーザーのメールアドレスに、アカウントを設定するための指示リンクと共に招待通知が送信されます。

>[!NOTE]
>
>ユーザーは、特定のメールアドレスに 1 つの招待状のみを送信できます。 同じ E メール アドレスに招待状を再送信しようとすると、エラーメッセージが表示され、招待状は送信されません。

## ストアへの招待を有効にする

招待状設定では、ストアの招待が有効になり、招待状の送信方法が決定されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Invitations]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL General]** セクション。

   ![顧客の設定 – 招待状の一般オプション](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enable Invitations Functionality]** 対象： `Yes`.

1. 顧客がストアフロントからの招待を管理できるようにするには、を設定します **ストアフロントでの招待状の有効化** 対象： `Yes`.

1. を設定 **[!UICONTROL Referred Customer Group]** を次のいずれかに変更します。

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. を設定 **[!UICONTROL New Accounts Registration]** を次のいずれかに変更します。

   - `By Invitation Only`
   - `Available to All`

1. 終了 **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**&#x200B;を選択 `Yes`.

1. 一度に送信できる招待の数を制限するには、次に数を入力します **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** フィールド。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Email]** を選択し、次の操作を実行します。

   ![顧客設定 – 招待メールのオプション](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - として使用するストア ID を選択します **[!UICONTROL Customer Invitation Email Sender]**.

   - 「」を選択します **[!UICONTROL Customer Invitation Email Template]** 送信された招待状に使用されます。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 管理画面での招待状の送信と管理

が含まれる [プライベート販売レポート](../getting-started/private-sales-reports.md) セクションには、指定した期間に送信された招待状の数、または招待状を送信した顧客が表示されます。

### 管理者での招待状の作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Invitations]**.

1. 次の画面で、新規顧客の招待、カスタムメッセージの追加、送信者の選択、招待グループの選択を行うためのメールアドレスを入力します。

   複数のストア表示がある場合は、を使用します **[!UICONTROL Send From]** 招待状の送信元となるストア ビューを指定するオプションです。

   ![招待状情報](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

### 単一エンティティの招待を破棄

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. フィルターを使用して必要な招待を見つけ、編集モードで開きます。

1. 右上隅のをクリックします。 **[!UICONTROL Discard Invitation]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

### 複数のエンティティの招待を破棄

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. 破棄する招待を検索して選択します。

1. 左上で、 **[!UICONTROL Actions]** 選択するメニュー **[!UICONTROL Discard Selected]** をクリックして、 **[!UICONTROL Submit]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

### フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Select] | チェックボックスを選択してアクションの対象となる招待を選択するか、列ヘッダーの選択コントロールを使用します。 オプション： `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | 招待の内部 ID 番号 |
| [!UICONTROL Email] | 対応する顧客の電子メールアドレス |
| [!UICONTROL Invitee] | 招待ユーザーのメール |
| [!UICONTROL Sent] | 招待状が送信された日時 |
| [!UICONTROL Registered] | 顧客が登録された時刻とデータ |
| [!UICONTROL Status] | 招待状の状態。 オプション： `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | 対応する web サイト |
| [!UICONTROL Invitee Group] | 招待者の顧客グループ |

{style="table-layout:auto"}
