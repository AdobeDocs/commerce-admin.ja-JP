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

![ギフト カード アカウント](./assets/marketing-gift-card-accounts-grid.png){width="700" zoomable="yes"}

## ギフト カード アカウントの構成

ギフトカードの設定では、ストア表示のすべてのギフトカードのデフォルト設定が確立され、コードプールが管理されます。 コードプールは、特定の形式の一意のギフトカードコードのセットです。 プールのコードは、ギフトカードアカウントが作成されるたびに使用されます。 ギフトカード販売に使用できるコードが十分にあることを確認するのは、店舗管理者の責任です。 ギフトカードを販売する前に、コードプールを生成してください。 デフォルトでは、Adobe Commerceは 1,000 個のコードを生成します。 新しいコード プールは、現在のプールで使用できるコードがなくなるまで生成されません。

### 手順 1：メール通知を設定する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Gift Cards]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Gift Card Email Settings]_を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Gift Card Notification Email Sender]** ギフトカード通知の送信者として表示されるストア ID に関連付けます。

   - を設定 **[!UICONTROL Gift Card Notification Email Template]** 通知に使用されるテンプレート。

   ![ギフト カードの E メール設定](../configuration-reference/sales/assets/gift-cards-gift-card-email-settings.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Email Sent from Gift Card Account Management]_を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Gift Card Email Sender]** ギフトカードの送信者として表示されるストア ID に対して指定します。

   - を設定 **[!UICONTROL Gift Card Template]** をギフトカードに使用するテンプレートに変更します。

参照： [メールアドレスの保存](../configuration-reference/general/store-email-addresses.md) （特定の設定フィールドおよびオプション用）。

### 手順 2：一般設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Gift Card General Settings]_セクション。

1. お客様がカードの値を現金に交換できるようにするには、次のように設定します **[!UICONTROL Redeemable]** 対象： `Yes`.

1. の場合 **[!UICONTROL Lifetime (days)]**&#x200B;カードの有効期限が切れるまでの日数を入力します。

   有効期限がない場合は、フィールドを空白のままにします。

   >[!NOTE]
   >
   >お住まいの地域によっては、ギフトカードの有効期限が切れる場合があります。 ギフトカードの有効期間を設定する前に、地域の法律を確認してください。

1. ギフトカードに添付するメッセージを入力するオプションを顧客に提供するには、次のように設定します **[!UICONTROL Allow Gift Message]** 対象： `Yes` およびメッセージで使用できる文字数を入力します **[!UICONTROL Gift Message Maximum Length]**.

1. を設定 **[!UICONTROL Generate Gift Card Account when Orders Item is]** を次のいずれかに変更します。

   - `Ordered`  – 注文が行われると、ギフトカードのアカウントが作成されます。
   - `Invoiced`  – 支払いがキャプチャされ、注文が請求された後にギフトカード口座が作成されます。

   ![ギフト カードの一般設定](../configuration-reference/sales/assets/gift-cards-gift-card-general-settings.png){width="600" zoomable="yes"}

### 手順 3: ギフト カードのコード プールを確立する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Gift Card Account General Settings]_を選択し、次の操作を実行します。

   ![ギフト カード アカウントの一般設定](../configuration-reference/sales/assets/gift-cards-gift-card-account-general-settings.png){width="600" zoomable="yes"}

   - コードをカスタマイズするには、必要に応じて次の手順を実行します。

      - コード長
      - コードフォーマット
      - コードプレフィックス
      - コードサフィックス
      - X 文字ごとにダッシュ

   - 生成するコードの数を決定するには、 **[!UICONTROL New Pool Size]**.

   - コードプールを再入荷する通知を受信するタイミングを指定するには、 **[!UICONTROL Low Code Pool Threshold]**.

1. コード プールを生成する前に、 **[!UICONTROL Save Config]**.

1. クリック **[!UICONTROL Generate]**.

1. 完了したら、 **[!UICONTROL Save Config]**.

## 既存のギフト カード アカウントを確認する

1. 現在の注文のギフト カード アカウントの番号を調べるには、次の操作を行います。

   - 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

   - リスト内の順序を見つけて、 **[!UICONTROL View]** が含まれる _[!UICONTROL Action]_列。

   - にスクロール ダウンします。 _[!UICONTROL Items Ordered]_セクション。

   数字はです _[!UICONTROL Product]_列、下&#x200B;**[!UICONTROL Gift Card Accounts]**.

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. グリッドでギフトカードアカウントを見つけて、編集モードで開きます。

   ギフトカードのコードは、の上部に表示されます _情報_ セクション。

   ![ギフト カード アカウント情報](./assets/gift-card-account-information.png){width="600" zoomable="yes"}

## ギフトカードアカウントの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Gift Card Account]**.

1. が含まれる _[!UICONTROL Information]_セクション、設定&#x200B;**[!UICONTROL Active]**対象： `Yes` 次の手順を実行します。

   - チェックアウト時にカード残高を引き換えたり、顧客の店舗クレジットに転送したりするには、次のように設定します **[!UICONTROL Redeemable]** 対象： `Yes`.

   - を選択します。 **[!UICONTROL Website]** ギフトカードアカウントを使用できる場所。

   - 最初のを入力 **[!UICONTROL Balance]** ギフトカードに。

   - _（オプション）_ を設定するには **[!UICONTROL Expiration Date]** ギフトカードには、カレンダーから日付を選択します ![カレンダーアイコン](../assets/icon-calendar.png).

     空白のままにすると、ギフトカードのアカウントは期限切れになりません。

     ![新しいアカウント](./assets/gift-card-account-add-new.png){width="600" zoomable="yes"}

1. 左パネルで、を選択します。 **[!UICONTROL Send Gift Card]** 次の手順を実行します。

   - を入力 **[!UICONTROL Recipient Email]** 住所。

   - を入力 **[!UICONTROL Recipient Name]**.

   - を設定 **[!UICONTROL Send Email from the Following Store View]** ギフトカード通知の送信者として表示されるストア表示に移動します。

   ![ギフト カードの設定を送信](./assets/marketing-gift-card-accounts-new-send.png){width="600" zoomable="yes"}

1. 次のいずれかの操作を行って、新しいアカウントを保存します。

   - ギフト カードを送る準備ができていない場合は、 **[!UICONTROL Save]**.

   - 変更を保存し、ギフト カードを電子メールで受信者に送信するには、 **メールを保存して送信**.

## ギフト カード アカウント履歴の表示

1. に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. ギフトカードを編集モードで開きます。

1. この **[!UICONTROL History]** ギフトカードのが表示されます。

   ![ギフト カードの履歴](./assets/gift-card-history.png){width="600" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | ギフトカードを使用したアクションの一意の数値。 |
| [!UICONTROL Date] | アクションの日付。 |
| [!UICONTROL Action] | ギフトカードを使用して、可能なすべてのアクションを決定します。 オプション： `Created` / `Updated` / `Sent` / `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance Change] | ギフト カードの残高が変更された金額を表示します。 |
| [!UICONTROL Balance] | 使用可能な残高を示します。 |
| [!UICONTROL More Information] | ギフト カードの残高を変更したユーザーに関する情報を表示します。 |

{style="table-layout:auto"}

## ギフト カード アカウントの削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**.

1. 削除するギフト カード アカウントを選択し、編集モードで開きます。

1. メニューバーで、 **[!UICONTROL Delete]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | ギフトカードアカウントに割り当てられる一意の数値識別子。 |
| [!UICONTROL Code] | ギフト カードを適用するために入力する必要があるコード。 |
| [!UICONTROL Website] | ギフト カード アカウントを利用できる Web サイトを示します。 |
| [!UICONTROL Created] | 作成日。 |
| [!UICONTROL End] | ギフト カードの有効期限（スケジュールされている場合）。 |
| [!UICONTROL Active] | ギフト カードが有効かどうかを決定します。 |
| [!UICONTROL Status] | ギフトカードを顧客のアカウントで引き換えるか、使用可能にするかを決定します。 オプション： `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance] | 使用可能な残高を示します。 |

{style="table-layout:auto"}
