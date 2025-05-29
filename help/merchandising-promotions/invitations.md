---
title: イベント招待状
description: 顧客がイベントや個人販売への招待状を顧客アカウントのダッシュボードから送信および表示する方法について説明します。
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# イベント招待状

{{ee-feature}}

招待状を有効にすると、顧客は、顧客アカウントのダッシュボードから招待状を送信および表示できます。 招待メールには、ストアのカスタマーログインページへのリンクが含まれています。

## マイ招待状

顧客アカウントの「_[!UICONTROL My Invitations]_」セクションには、顧客から送信されたすべての招待状が一覧表示されます。 お客様は、店舗のイベント、ギフト登録、ウィッシュリストなどに関する招待状を友人や家族に送信できます。

![ 招待状 ](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### 招待ワークフロー

1. **顧客が招待状を準備**: アカウントダッシュボードから、顧客が受信者のリストを準備して招待状を完了します。 設定に応じて、カスタムメッセージを含めることができます。
1. **顧客が招待状を送信**：準備が整ったら、「_[!UICONTROL Send Invitations]_」ボタンをクリックします。
1. **システムが送信を管理**：システムは、設定に設定された数に応じて、招待をバッチで送信します。
1. **顧客モニター応答**：顧客は、アカウントダッシュボードから各招待のステータス（`Sent`、`Accepted`、`Canceled` など）をモニターします。

### 招待状を送信

1. ストアフロントのアカウントのサイドバーで、顧客は **[!UICONTROL My Invitations]** を選択します。

1. _マイ招待_ ページで、[**[!UICONTROL Send Invitation]**] をクリックします。

1. 新しい招待状項目を定義します。

   - 電子メール情報を完了します。

   - （任意） **+** をクリックして別のメールアドレスを追加することで、複数アドレスからの招待を作成します。

     1 人の招待メールには 5 つのメールアドレス制限があります。

   - （任意）付随するメッセージを入力します。

1. 完了したら、「**[!UICONTROL Send Invitation]**」をクリックします。

招待されたユーザーのメールアドレスに、アカウントを設定するための指示リンクと共に招待通知が送信されます。

>[!NOTE]
>
>ユーザーは、特定のメールアドレスに 1 つの招待状のみを送信できます。 同じ E メール アドレスに招待状を再送信しようとすると、エラーメッセージが表示され、招待状は送信されません。

## ストアへの招待を有効にする

招待状設定では、ストアの招待が有効になり、招待状の送信方法が決定されます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Invitations]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL General]**」セクションを展開します。

   ![ 顧客の設定 – 招待状の一般オプション ](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Invitations Functionality]** を `Yes` に設定します。

1. 顧客がストアフロントからの招待を管理できるようにするには、**ストアフロントでの招待を有効にする** を `Yes` に設定します。

1. **[!UICONTROL Referred Customer Group]** を次のいずれかに設定します。

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. **[!UICONTROL New Accounts Registration]** を次のいずれかに設定します。

   - `By Invitation Only`
   - `Available to All`

1. **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]** するには、「`Yes`」を選択します。

1. 一度に送信できる招待の数を制限するには、「**[!UICONTROL Max Invitations Allowed to be Sent at One Time]**」フィールドに数を入力します。

1. **[!UICONTROL Email]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![ 顧客の設定 – 招待メールのオプション ](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - **[!UICONTROL Customer Invitation Email Sender]** として使用するストア ID を選択します。

   - 送信する招待状に使用する **[!UICONTROL Customer Invitation Email Template]** を選択します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 管理画面での招待状の送信と管理

[[ プライベート販売レポート ](../getting-started/private-sales-reports.md)] セクションでは、指定した期間に送信された招待状の数、または招待状を送信した顧客を確認できます。

### 管理者での招待状の作成

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Private Sales]_/**[!UICONTROL Invitations]**に移動します。

1. 右上隅の「**[!UICONTROL Add Invitations]**」をクリックします。

1. 次の画面で、新規顧客の招待、カスタムメッセージの追加、送信者の選択、招待グループの選択を行うためのメールアドレスを入力します。

   複数のストア表示がある場合は、**[!UICONTROL Send From]** オプションを使用して、招待状の送信元のストア表示を指定します。

   ![ 招待事項 ](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

### 単一エンティティの招待を破棄

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Private Sales]_/**[!UICONTROL Invitations]**に移動します。

1. フィルターを使用して必要な招待を見つけ、編集モードで開きます。

1. 右上隅の「**[!UICONTROL Discard Invitation]**」をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。

### 複数のエンティティの招待を破棄

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Private Sales]_/**[!UICONTROL Invitations]**に移動します。

1. 破棄する招待を検索して選択します。

1. 左上で、**[!UICONTROL Actions]** メニューを使用して **[!UICONTROL Discard Selected]** を選択し、「**[!UICONTROL Submit]**」をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。

### フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Select] | チェックボックスを選択してアクションの対象となる招待を選択するか、列ヘッダーの選択コントロールを使用します。 オプション：`Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | 招待の内部 ID 番号 |
| [!UICONTROL Email] | 対応する顧客の電子メールアドレス |
| [!UICONTROL Invitee] | 招待ユーザーのメール |
| [!UICONTROL Sent] | 招待状が送信された日時 |
| [!UICONTROL Registered] | 顧客が登録された時刻とデータ |
| [!UICONTROL Status] | 招待状の状態。 オプション：`Sent`/`Not Sent`/`Accepted`/`Discarded` |
| [!UICONTROL Valid Website] | 対応する web サイト |
| [!UICONTROL Invitee Group] | 招待者の顧客グループ |

{style="table-layout:auto"}
