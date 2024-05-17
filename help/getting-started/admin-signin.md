---
title: 管理者ユーザーアカウント
description: 管理者アカウントの概要、および二要素認証を使用して管理者にログインする方法を説明します。
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# 管理者アカウント

プライマリ管理者アカウントは、インストール時に最初に設定されたもので、初期プレースホルダー情報やサンプルデータ情報が含まれている場合があります。 このアカウントの所有者は、ユーザー名とパスワードをパーソナライズし、姓、名、およびメールアドレスをいつでも更新できます。 このアカウント、 _スーパーユーザー_ デフォルトではすべての権限を持つユーザーが、ビジネスに必要な管理者ユーザーアカウントを作成します。

- 参照： [ユーザーの作成](../systems/permissions-users-all.md#create-a-user) ユーザーの追加または編集については、を参照してください。

- 参照： [権限](../systems/permissions.md) および [ユーザーの役割](../systems/permissions-user-roles.md) 管理者ロールとユーザーロールについて説明します。

{{ims-admin-note}}

## 管理者によるログイン

この [!DNL Commerce] _Admin_ は、店舗、注文、顧客データへの不正アクセスを防ぐための複数のセキュリティ対策レイヤーによって保護されています。 に初めてログインしたとき _Admin_&#x200B;に変更する場合、ユーザー名とパスワードを入力し、を設定する必要があります [二要素認証](../systems/security-two-factor-authentication.md) （2FA）。

ストアの設定によっては、次の場合があります。 [CAPTCHA](../systems/security-google-recaptcha.md) 一連のキーボード文字の入力、パズルの解き方、共通のテーマを持つ一連の画像のクリックなど、解決が難しい問題。 これらのテストは、自動ボットではなく、人間として識別されるように設計されています。

セキュリティを強化するために、の各部を指定できます _Admin_ 各ユーザーの持ち時間 [権限](../systems/permissions.md) アクセスし、数を制限します [ログイン試行](../configuration-reference/advanced/admin.md). デフォルトでは、6 回試行するとアカウントがロックされるので、ユーザーは数分待ってから再試行する必要があります。 [ロックされたアカウント](../systems/permissions-users-all.md#locked-users) は、 _Admin_.

>[!NOTE]
>
>に初めてログインしたとき _Admin_。次の操作を求められます _管理者による使用状況データの収集を許可_. 参照： [使用状況データの収集](admin.md#usage-data-collection) を参照してください。

![管理者によるログイン](./assets/admin-login.png){width="400"}

### 手順 1：二要素認証の設定

にサインインする前に _Admin_ ストアで、2 要素認証ソリューションが設定され、使用できる状態になっている必要があります。 各ソリューションで使用される認証プロセスの詳細については、を参照してください。 [二要素認証の使用](../systems/security-two-factor-authentication-use.md). デフォルトでは [!DNL Commerce] のサポート [Google Authenticator][1].

に尋ねる [!DNL Commerce] システム管理者：ストアで 2FA ソリューションがサポートされている場合。 次に、プロバイダーの指示に従って、お好みの 2FA ソリューションの設定を完了します。

### 手順 2：管理者にログインする

1. を入力 _Admin_ 次の期間で指定された URL [!DNL Commerce] インストール。

   デフォルト _Admin_ URL は次のようになります `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >ただし、このドキュメントではを使用します `admin` ほとんどの例では、ベース URL として、一意で推測しにくい URL を選択することをお勧めします [カスタム URL](../stores-purchase/store-urls.md) の場合 _Admin_ あなたの店の。

   ページのブックマークを追加したり、デスクトップにショートカットを保存して簡単にアクセスしたりできます。

1. を入力 _Admin_ **[!UICONTROL Username]** および **[!UICONTROL Password]**.

1. （オプション）ストアで CAPTCHA が有効になっている場合は、画面の指示に従って課題を解決します。

   詳しくは、 [CAPTCHA](../systems/security-captcha.md) および [reCAPTCHA](../systems/security-google-recaptcha.md).

1. クリック **[!UICONTROL Sign in]**.

   に初めてログインした場合 _Admin_ アカウントから、設定手順へのリンクが記載されたメールが届きます。

### 手順 3:2FA 設定の完了

次の例は、 _Admin_ Google Authenticator を使用しているアカウント。

1. QR コードが表示されたら、次のいずれかの方法を使用してコードを取得し、Google Authenticator とユーザーのペアを設定します _Admin_ アカウント。

   ![Google Authenticator の設定](./assets/admin-login-google-auth-setup.png){width="400"}

   - スマートフォンでの QR コード取得

     スマートフォンで、Google Authenticator を起動します。 をタップします _プラス記号_ （+）をクリックします。 次に、画面の下部にあるをタップします **[!UICONTROL Scan Barcode]** QR コードの写真を撮ります。

   - ブラウザーから QR コードを取得

     Google Authenticator がブラウザーに拡張機能としてインストールされている場合は、 **Authenticator** アイコンをクリックし、ページをキャプチャします。

   - QR コードを手動で入力

     QR コードの下のテキスト文字列をコピーします。 スマートフォンまたはブラウザーでGoogle Authenticator を起動し、プラス記号（+）をクリックします。 次に、を選択します **[!UICONTROL Manual Entry]**. 次の下 **[!UICONTROL Account]**&#x200B;に関連付けられているメールアドレスを入力します _Admin_ を説明し、QR コード文字列をに貼り付けます **[!UICONTROL Key]** フィールド。

1. にログインするには _Admin_ 二要素認証を使用する場合は、Google Authenticator で生成された 6 桁のコードを **[!UICONTROL Authenticator code]** フィールドを選択し、 **[!UICONTROL Confirm]**.

   ![認証コードを入力](./assets/admin-login-2fa-google.png){width="400"}

## パスワードをリセット

アカウントに割り当てられた最後の 4 つのパスワードの再利用は許可されていません。

1. を入力 **[!UICONTROL Email Address]** に関連付けられています _Admin_ アカウント。

   ![パスワードを忘れた](./assets/admin-sign-in-forgot-password.png){width="400"}

1. クリック **[!UICONTROL Retrieve Password]**.

   アカウントがメールアドレスに関連付けられている場合、パスワードをリセットするためのメールが送信されます。

   >[!NOTE]
   >
   >An _Admin_ パスワードは 7 文字以上で、文字と数字の両方を含める必要があります。 参照： [設定 _Admin_ セキュリティ](../systems/security-admin.md) パスワードオプションについて詳しくは、を参照してください。

## 管理者からサインアウト

1. 右上隅のをクリックします _アカウント_ （![アカウント](../assets/icon-admin-user.png)） アイコンをクリックします。

1. クリック **[!UICONTROL Sign Out]**.

   ![サインアウト](./assets/admin-sign-out.png){width="700" zoomable="yes"}

この _[!UICONTROL Sign In]_ページには、ログアウト済みのメッセージが表示されます。 からサインアウト_ Admin _コンピュータを使用せずに放置する場合。

## アカウント情報の編集

1. 「」をクリックします _アカウント_ （![アカウントアイコン](../assets/icon-admin-user.png)） アイコンをクリックします。

1. クリック **[!UICONTROL Account Setting]**.

   ![アカウント情報](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. アカウント情報に必要な変更を加えます。

   ログイン資格情報を変更する場合は、必ず安全な場所に保存してください。

1. 現在のアカウントのパスワードを入力します。

1. クリック **[!UICONTROL Save Account]**.

## 複数の管理者ログインを許可

管理者は、注文、顧客、製品、配送、支払いの各機能を管理するためのアクセス権を提供します。 デフォルトの設定では、セキュリティのベストプラクティスとして、管理者ユーザーアカウントに対して複数のログインを許可しないように設定されています。 ただし、この設定を変更して、管理者ユーザーが複数のデバイスからログインして、ビジネスワークフローに対応できるようにすることができます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルでを展開します。 **[!UICONTROL Advanced]** を選択します **[!UICONTROL Admin]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Security]** セクション。

1. の場合 **管理者アカウント共有**&#x200B;を選択 `Yes`.

   ![管理者アカウントの共有を許可](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 管理者ユーザーのログイン名で大文字と小文字を区別するように設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルでを展開します。 **[!UICONTROL Advanced]** を選択します **[!UICONTROL Admin]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Security]** セクション。

1. を **[!UICONTROL Login is Case Sensitive]** フィールド先 `Yes`.

1. クリック **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US
