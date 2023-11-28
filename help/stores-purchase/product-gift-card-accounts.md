---
title: ギフトカードのアカウント
description: ギフトカードアカウントと、コードプール管理のデフォルト設定を構成する方法について説明します。
exl-id: f8caff04-38fd-4195-ab11-77dae900976d
feature: Products, Gift, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 0%

---

# ギフトカードのアカウント

ギフトカードのアカウントは、購入したギフトカードごとに自動的に作成されます。 ギフトカードの値は、ストアでの商品の購入に適用できます。 また、プロモーションまたは顧客向けサービスとして、管理者からギフトカードアカウントを作成することもできます。 ギフトカードのアカウント番号はギフトカードのコードに対応しています。

![ギフトカードのアカウント](./assets/marketing-gift-card-accounts-grid.png){width="700" zoomable="yes"}

## ギフトカードアカウントの設定

ギフトカードの設定は、ストア表示のすべてのギフトカードのデフォルト設定を設定し、コードプールを管理します。 コードプールは、特定の形式の一意のギフトカードコードのセットです。 プールのコードは、ギフトカードのアカウントが作成されるたびに使用されます。 ギフトカードの販売に利用できる十分なコードがあることを確認するのは、店舗管理者の責任です。 ギフトカードを販売する前に、必ずコードプールを生成してください。 デフォルトでは、Adobe Commerceは 1,000 個のコードを生成します。 現在のプールに使用可能なコードがなくなるまで、新しいコードプールは生成されません。

### 手順 1：電子メール通知を設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Gift Cards]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Gift Card Email Settings]_」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Gift Card Notification Email Sender]** を追加します。

   - 設定 **[!UICONTROL Gift Card Notification Email Template]** 通知に使用するテンプレートに追加します。

   ![ギフトカードのメール設定](../configuration-reference/sales/assets/gift-cards-gift-card-email-settings.png){width="600" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Email Sent from Gift Card Account Management]_」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Gift Card Email Sender]** を追加します。

   - 設定 **[!UICONTROL Gift Card Template]** をギフトカードに使用するテンプレートに追加します。

詳しくは、 [電子メールアドレスを保存](../configuration-reference/general/store-email-addresses.md) を参照してください。

### 手順 2：一般設定の完了

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Gift Card General Settings]_」セクションに入力します。

1. お客様がカードの価値を現金で使用できるようにするには、 **[!UICONTROL Redeemable]** から `Yes`.

1. の場合 **[!UICONTROL Lifetime (days)]**」には、カードの有効期限が切れるまでの日数を入力します。

   有効期限がない場合は、フィールドを空白のままにします。

   >[!NOTE]
   >
   >場所によっては、ギフトカードが期限切れになるので、違法な可能性があります。 ギフトカードの有効期間を設定する前に、現地の法律を確認してください。

1. ギフトカードに添付するメッセージを顧客に入力するオプションを与えるには、 **[!UICONTROL Allow Gift Message]** から `Yes` メッセージに使用できる文字数を入力します。 **[!UICONTROL Gift Message Maximum Length]**.

1. 設定 **[!UICONTROL Generate Gift Card Account when Orders Item is]** を次のいずれかに変更します。

   - `Ordered`  — ギフトカードのアカウントは注文時に作成されます。
   - `Invoiced`  — ギフトカードのアカウントは、支払いが取り込まれ、注文が請求された後に作成されます。

   ![ギフトカードの一般設定](../configuration-reference/sales/assets/gift-cards-gift-card-general-settings.png){width="600" zoomable="yes"}

### 手順 3：ギフトカードコードプールの設定

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Gift Card Account General Settings]_」セクションで次の操作を実行します。

   ![ギフトカードアカウントの一般設定](../configuration-reference/sales/assets/gift-cards-gift-card-account-general-settings.png){width="600" zoomable="yes"}

   - コードをカスタマイズするには、好みに応じて次の操作を実行します。

      - コードの長さ
      - コード形式
      - コードプレフィックス
      - コードサフィックス
      - X 文字ごとにダッシュ

   - 生成するコード数を決定するには、 **[!UICONTROL New Pool Size]**.

   - コードプールを再在庫する通知を受け取るタイミングを指定するには、 **[!UICONTROL Low Code Pool Threshold]**.

1. コードプールを生成する前に、 **[!UICONTROL Save Config]**.

1. クリック **[!UICONTROL Generate]**.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 既存のギフトカードアカウントの確認

1. 現在の注文のギフトカードのアカウント番号を確認するには、次の手順を実行します。

   - 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

   - リスト内の順序を検索し、 **[!UICONTROL View]** （内） _[!UICONTROL Action]_列。

   - 下にスクロールして、 _[!UICONTROL Items Ordered]_」セクションに入力します。

   数値は _[!UICONTROL Product]_列、下&#x200B;**[!UICONTROL Gift Card Accounts]**.

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. グリッドでギフトカードのアカウントを見つけ、編集モードで開きます。

   ギフトカードコードは _情報_ 」セクションに入力します。

   ![ギフトカードのアカウント情報](./assets/gift-card-account-information.png){width="600" zoomable="yes"}

## ギフトカードアカウントの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. 右上隅で、 **[!UICONTROL Add Gift Card Account]**.

1. Adobe Analytics の _[!UICONTROL Information]_セクション、設定&#x200B;**[!UICONTROL Active]**から `Yes` 次の操作を実行します。

   - カード残高をチェックアウト時または顧客の店舗クレジットに振り替える際に償還可能にするには、 **[!UICONTROL Redeemable]** から `Yes`.

   - を選択します。 **[!UICONTROL Website]** ギフトカードアカウントを使用できる場所です。

   - 初期の **[!UICONTROL Balance]** ギフトカードに貼り付けます。

   - _（オプション）_ 次の手順で、 **[!UICONTROL Expiration Date]** ギフトカードの場合は、カレンダーから日付を選択します。 ![カレンダーアイコン](../assets/icon-calendar.png).

     空白の場合、ギフトカードのアカウントは期限切れになりません。

     ![新しいアカウント](./assets/gift-card-account-add-new.png){width="600" zoomable="yes"}

1. 左側のパネルで、を選択します。 **[!UICONTROL Send Gift Card]** 次の操作を実行します。

   - 次を入力します。 **[!UICONTROL Recipient Email]** 住所。

   - 次を入力します。 **[!UICONTROL Recipient Name]**.

   - 設定 **[!UICONTROL Send Email from the Following Store View]** ギフトカード通知の送信者として表示されるストア表示に追加します。

   ![ギフトカードの送信設定](./assets/marketing-gift-card-accounts-new-send.png){width="600" zoomable="yes"}

1. 次のいずれかの操作を行って、新しいアカウントを保存します。

   - ギフトカードを送信する準備ができていない場合は、 **[!UICONTROL Save]**.

   - 変更内容を保存し、受信者に E メールでギフトカードを送信するには、 **メールを保存して送信**.

## ギフトカードのアカウント履歴を表示

1. に移動します。 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. ギフトカードを編集モードで開きます。

1. The **[!UICONTROL History]** のギフトカードが表示されます。

   ![ギフトカード履歴](./assets/gift-card-history.png){width="600" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | ギフトカードを含む一意のアクション数値。 |
| [!UICONTROL Date] | アクションの日付。 |
| [!UICONTROL Action] | ギフトカードで実行可能なすべてのアクションを決定します。 オプション： `Created` / `Updated` / `Sent` / `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance Change] | ギフトカードの残高が変更された金額を表示します。 |
| [!UICONTROL Balance] | 使用可能な残高を示します。 |
| [!UICONTROL More Information] | ギフトカードの残高を変更した人に関する情報を表示します。 |

{style="table-layout:auto"}

## ギフトカードのアカウントを削除する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. 削除するギフトカードのアカウントを選択し、編集モードで開きます。

1. メニューバーで、 **[!UICONTROL Delete]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | ギフトカードのアカウントに割り当てられる一意の数値 ID。 |
| [!UICONTROL Code] | ギフトカードを適用するために入力する必要があるコードです。 |
| [!UICONTROL Website] | ギフトカードのアカウントを使用できる Web サイトを示します。 |
| [!UICONTROL Created] | 作成日。 |
| [!UICONTROL End] | ギフトカードの有効期限（スケジュールされている場合）。 |
| [!UICONTROL Active] | ギフトカードがアクティブかどうかを判断します。 |
| [!UICONTROL Status] | ギフトカードが顧客のアカウントで引き換えられるか、使用可能かを指定します。 オプション： `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance] | 使用可能な残高を示します。 |

{style="table-layout:auto"}
