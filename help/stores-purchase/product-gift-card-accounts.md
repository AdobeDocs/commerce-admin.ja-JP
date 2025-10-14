---
title: ギフト カード アカウント
description: ギフトカードアカウントと、コードプール管理のデフォルト設定について説明します。
exl-id: f8caff04-38fd-4195-ab11-77dae900976d
feature: Products, Gift, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 0%

---

# ギフト カード アカウント

購入したギフトカードごとに、ギフトカードアカウントが自動的に作成されます。 ギフトカードの値は、ストア内の製品の購入に適用できます。 また、お客様のプロモーションまたはサービスとして、管理者からギフトカードアカウントを作成することもできます。 ギフト カードの口座番号は、ギフト カード コードに対応します。

![&#x200B; ギフト カード アカウント &#x200B;](./assets/marketing-gift-card-accounts-grid.png){width="700" zoomable="yes"}

## ギフト カード アカウントの構成

ギフトカードの設定では、ストア表示のすべてのギフトカードのデフォルト設定が確立され、コードプールが管理されます。 コードプールは、特定の形式の一意のギフトカードコードのセットです。 プールのコードは、ギフトカードアカウントが作成されるたびに使用されます。 ギフトカード販売に使用できるコードが十分にあることを確認するのは、店舗管理者の責任です。 ギフトカードを販売する前に、コードプールを生成してください。 デフォルトでは、Adobe Commerceは 1,000 個のコードを生成します。 新しいコード プールは、現在のプールで使用できるコードがなくなるまで生成されません。

### 手順 1：メール通知を設定する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Gift Cards]**」を選択します。

1. _[!UICONTROL Gift Card Email Settings]_&#x200B;のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - ギフトカード通知の送信者として表示されるストア ID に **[!UICONTROL Gift Card Notification Email Sender]** を設定します。

   - 通知に使用するテンプレートに **[!UICONTROL Gift Card Notification Email Template]** を設定します。

   ![&#x200B; ギフト カード E メールの設定 &#x200B;](../configuration-reference/sales/assets/gift-cards-gift-card-email-settings.png){width="600" zoomable="yes"}

1. _[!UICONTROL Email Sent from Gift Card Account Management]_&#x200B;のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - ギフトカードの送信者として表示するストア ID に **[!UICONTROL Gift Card Email Sender]** を設定します。

   - ギフトカードに使用するテンプレートに **[!UICONTROL Gift Card Template]** を設定します。

特定の設定フィールドとオプションについては、[&#x200B; メールアドレスの保存 &#x200B;](../configuration-reference/general/store-email-addresses.md) を参照してください。

### 手順 2：一般設定を完了する

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「_[!UICONTROL Gift Card General Settings]_」セクションを展開します。

1. お客様がカードの値を現金で引き換えることができるようにするには、**[!UICONTROL Redeemable]** を `Yes` に設定します。

1. **[!UICONTROL Lifetime (days)]**：カードの有効期限が切れるまでの日数を入力します。

   有効期限がない場合は、フィールドを空白のままにします。

   >[!NOTE]
   >
   >お住まいの地域によっては、ギフトカードの有効期限が切れる場合があります。 ギフトカードの有効期間を設定する前に、地域の法律を確認してください。

1. 顧客がギフトカードに添付するメッセージを入力するオプションを提供するには、**[!UICONTROL Allow Gift Message]** を `Yes` に設定し、メッセージで使用できる文字数を **[!UICONTROL Gift Message Maximum Length]** に入力します。

1. **[!UICONTROL Generate Gift Card Account when Orders Item is]** を次のいずれかに設定します。

   - `Ordered` - ギフト カード アカウントは、注文時に作成されます。
   - `Invoiced` – 支払いがキャプチャされ、注文が請求された後にギフトカード口座が作成されます。

   ![&#x200B; ギフト カードの一般設定 &#x200B;](../configuration-reference/sales/assets/gift-cards-gift-card-general-settings.png){width="600" zoomable="yes"}

### 手順 3: ギフト カードのコード プールを確立する

1. _[!UICONTROL Gift Card Account General Settings]_&#x200B;のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; ギフト カード アカウントの一般設定 &#x200B;](../configuration-reference/sales/assets/gift-cards-gift-card-account-general-settings.png){width="600" zoomable="yes"}

   - コードをカスタマイズするには、必要に応じて次の手順を実行します。

      - コード長
      - コードフォーマット
      - コードプレフィックス
      - コードサフィックス
      - X 文字ごとにダッシュ

   - 生成するコードの数を決定するには、**[!UICONTROL New Pool Size]** を入力します。

   - コードプールを再入荷する通知を受け取るタイミングを指定するには、**[!UICONTROL Low Code Pool Threshold]** を入力します。

1. コード プールを生成する前に、[**[!UICONTROL Save Config]**] をクリックします。

1. 「**[!UICONTROL Generate]**」をクリックします。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 既存のギフト カード アカウントを確認する

1. 現在の注文のギフト カード アカウントの番号を調べるには、次の操作を行います。

   - _管理者_ サイドバーで、**[!UICONTROL Sales]**/_[!UICONTROL Operations]_/**[!UICONTROL Orders]**&#x200B;に移動します。

   - リストで順序を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL View]**&#x200B;をクリックします。

   - _[!UICONTROL Items Ordered]_&#x200B;セクションまで下にスクロールします。

   数値は「_[!UICONTROL Product]_」列の「**[!UICONTROL Gift Card Accounts]**」の下にあります。

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Promotions]_/**[!UICONTROL Gift Card Accounts]**&#x200B;に移動します。

1. グリッドでギフトカードアカウントを見つけて、編集モードで開きます。

   ギフト カード コードは、&lbrack; 情報 _セクションの上部に表示さ_ ます。

   ![&#x200B; ギフト カード アカウント情報 &#x200B;](./assets/gift-card-account-information.png){width="600" zoomable="yes"}

## ギフトカードアカウントの作成

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Promotions]_/**[!UICONTROL Gift Card Accounts]**&#x200B;に移動します。

1. 右上隅にある「**[!UICONTROL Add Gift Card Account]**」をクリックします。

1. _[!UICONTROL Information]_&#x200B;セクションで、**[!UICONTROL Active]**&#x200B;を `Yes` に設定し、以下を実行します。

   - チェックアウト時にカードの残高を引き換えたり、顧客の店舗クレジットに転送したりするには、**[!UICONTROL Redeemable]** を `Yes` に設定します。

   - ギフト カード アカウントを使用できる **[!UICONTROL Website]** を選択してください。

   - ギフト カードの最初の **[!UICONTROL Balance]** を入力します。

   - _（オプション）_ ギフトカードの **[!UICONTROL Expiration Date]** を設定するには、カレンダー ![&#x200B; カレンダーアイコン &#x200B;](../assets/icon-calendar.png) から日付を選択します。

     空白のままにすると、ギフトカードのアカウントは期限切れになりません。

     ![&#x200B; 新規アカウント &#x200B;](./assets/gift-card-account-add-new.png){width="600" zoomable="yes"}

1. 左側のパネルで「**[!UICONTROL Send Gift Card]**」を選択し、次の操作を実行します。

   - **[!UICONTROL Recipient Email]** アドレスを入力します。

   - **[!UICONTROL Recipient Name]** を入力します。

   - ギフトカード通知の送信者として表示されるストア表示に **[!UICONTROL Send Email from the Following Store View]** を設定します。

   ![&#x200B; ギフト カードの送信の設定 &#x200B;](./assets/marketing-gift-card-accounts-new-send.png){width="600" zoomable="yes"}

1. 次のいずれかの操作を行って、新しいアカウントを保存します。

   - ギフト カードを送る準備ができていない場合は、[**[!UICONTROL Save]**] をクリックします。

   - 変更を保存し、ギフト カードを電子メールで受信者に送信するには、[**保存して電子メールを送信**] をクリックします。

## ギフト カード アカウント履歴の表示

1. **[!UICONTROL Marketing]**/_[!UICONTROL Promotions]_/**[!UICONTROL Gift Card Accounts]**&#x200B;に移動します。

1. ギフトカードを編集モードで開きます。

1. ギフトカードの **[!UICONTROL History]** が表示されます。

   ![&#x200B; ギフト カードの履歴 &#x200B;](./assets/gift-card-history.png){width="600" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | ギフトカードを使用したアクションの一意の数値。 |
| [!UICONTROL Date] | アクションの日付。 |
| [!UICONTROL Action] | ギフトカードを使用して、可能なすべてのアクションを決定します。 オプション：`Created` / `Updated` / `Sent` / `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance Change] | ギフト カードの残高が変更された金額を表示します。 |
| [!UICONTROL Balance] | 使用可能な残高を示します。 |
| [!UICONTROL More Information] | ギフト カードの残高を変更したユーザーに関する情報を表示します。 |

{style="table-layout:auto"}

## ギフト カード アカウントの削除

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Promotions]_/**[!UICONTROL Gift Card Accounts]**&#x200B;に移動します。

1. 削除するギフト カード アカウントを選択し、編集モードで開きます。

1. メニューバーで、「**[!UICONTROL Delete]**」をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | ギフトカードアカウントに割り当てられる一意の数値識別子。 |
| [!UICONTROL Code] | ギフト カードを適用するために入力する必要があるコード。 |
| [!UICONTROL Website] | ギフト カード アカウントを利用できる Web サイトを示します。 |
| [!UICONTROL Created] | 作成日。 |
| [!UICONTROL End] | ギフト カードの有効期限（スケジュールされている場合）。 |
| [!UICONTROL Active] | ギフト カードが有効かどうかを決定します。 |
| [!UICONTROL Status] | ギフトカードを顧客のアカウントで引き換えるか、使用可能にするかを決定します。 オプション：`Used`/`Redeemed`/`Expired` |
| [!UICONTROL Balance] | 使用可能な残高を示します。 |

{style="table-layout:auto"}
