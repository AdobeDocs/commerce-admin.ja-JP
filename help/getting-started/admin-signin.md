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

プライマリ管理者アカウントは、インストール時に最初に設定されたもので、初期プレースホルダー情報やサンプルデータ情報が含まれている場合があります。 このアカウントの所有者は、ユーザー名とパスワードをパーソナライズし、姓、名、およびメールアドレスをいつでも更新できます。 このアカウントは、デフォルトですべての権限を持つ _スーパーユーザー_ であり、通常はビジネスに必要な管理者ユーザーアカウントを作成します。

- ユーザーの追加または編集については、[ ユーザーの作成 ](../systems/permissions-users-all.md#create-a-user) を参照してください。

- 管理者およびユーザーの役割について詳しくは、[ 権限 ](../systems/permissions.md) および [ ユーザーの役割 ](../systems/permissions-user-roles.md) を参照してください。

{{ims-admin-note}}

## 管理者によるログイン

[!DNL Commerce]_管理者_ は、店舗、注文、顧客データへの不正アクセスを防ぐための複数のセキュリティ対策レイヤーで保護されています。 _管理者_ に初めてログインするときは、ユーザー名とパスワードを入力し、[ 二要素認証 ](../systems/security-two-factor-authentication.md) （2FA）を設定する必要があります。

ストアの設定によっては、一連のキーボード文字の入力、パズルの解決、共通のテーマを持つ一連の画像のクリックなど、解決すべき [CAPTCHA](../systems/security-google-recaptcha.md) 課題が生じる場合があります。 これらのテストは、自動ボットではなく、人間として識別されるように設計されています。

セキュリティを強化するために、各ユーザーがアクセスできる _権限_ を持つ [ 管理者 ](../systems/permissions.md) 部分を決定したり、[ ログイン試行 ](../configuration-reference/advanced/admin.md) 数を制限したりできます。 デフォルトでは、6 回試行するとアカウントがロックされるので、ユーザーは数分待ってから再試行する必要があります。 [ ロックされたアカウント ](../systems/permissions-users-all.md#locked-users) は、_管理者_ からもリセットできます。

>[!NOTE]
>
>_管理者_ に初めてログインすると、_管理者の使用状況データ収集を許可_ するように求められます。 詳しくは、[ 使用状況データの収集 ](admin.md#usage-data-collection) を参照してください。

![ 管理者によるログイン ](./assets/admin-login.png){width="400"}

### 手順 1：二要素認証の設定

ストアの _管理者_ にログインする前に、2 要素認証ソリューションを設定し、使用できる状態にしておく必要があります。 各ソリューションで使用される認証プロセスについて詳しくは、[ 二要素認証の使用 ](../systems/security-two-factor-authentication-use.md) を参照してください。 デフォルトで、[!DNL Commerce] は、[Google Authenticator][1] をサポートします。

ストアでサポートされている 2FA ソリューションを [!DNL Commerce] システム管理者に問い合わせてください。 次に、プロバイダーの指示に従って、お好みの 2FA ソリューションの設定を完了します。

### 手順 2：管理者にログインする

1. [!DNL Commerce] のインストール時に指定した _管理者_ URL を入力します。

   デフォルトの _管理者_ URL は `https://www.yourdomain.com/your-custom-admin-domain` のようになります。

   >[!NOTE]
   >
   >このドキュメントでは、ほとんどの例でベース URL として `admin` を使用していますが、ストアの _管理者 [ に対して、一意で推測しにくい ](../stores-purchase/store-urls.md) カスタム URL_ を選択することをお勧めします。

   ページのブックマークを追加したり、デスクトップにショートカットを保存して簡単にアクセスしたりできます。

1. _Admin_ **[!UICONTROL Username]** と **[!UICONTROL Password]** を入力します。

1. （オプション）ストアで CAPTCHA が有効になっている場合は、画面の指示に従って課題を解決します。

   詳しくは、[CAPTCHA](../systems/security-captcha.md) および [reCAPTCHA](../systems/security-google-recaptcha.md) を参照してください。

1. 「**[!UICONTROL Sign in]**」をクリックします。

   アカウントから _管理者_ に初めてログインした場合は、設定手順へのリンクが記載されたメールが届きます。

### 手順 3:2FA 設定の完了

次の例は、_管理者_ アカウントをGoogle Authenticator とペアにする方法を示しています。

1. QR コードが表示されたら、次のいずれかの方法を使用してコードを取得し、Google Authenticator と _Admin_ アカウントをペアにします。

   ![Google Authenticator の設定 ](./assets/admin-login-google-auth-setup.png){width="400"}

   - スマートフォンでの QR コード取得

     スマートフォンで、Google Authenticator を起動します。 アプリの右上隅にある _プラス記号_ （+）をタップします。 次に、画面の下部にある **[!UICONTROL Scan Barcode]** をタップして、QR コードの写真を撮ります。

   - ブラウザーから QR コードを取得

     Google Authenticator がブラウザーに拡張機能としてインストールされている場合は、ツールバーの **Authenticator** アイコンをクリックしてページをキャプチャします。

   - QR コードを手動で入力

     QR コードの下のテキスト文字列をコピーします。 スマートフォンまたはブラウザーでGoogle Authenticator を起動し、プラス記号（+）をクリックします。 次に、「**[!UICONTROL Manual Entry]**」を選択します。 「**[!UICONTROL Account]**」の下に、_管理者_ アカウントに関連付けられているメールアドレスを入力し、QR コード文字列を「**[!UICONTROL Key]**」フィールドに貼り付けます。

1. 二要素認証を使用して _Admin_ にログインするには、Google Authenticator で生成された 6 桁のコードを「**[!UICONTROL Authenticator code]**」フィールドに入力し、「**[!UICONTROL Confirm]**」をクリックします。

   ![ 認証コードを入力 ](./assets/admin-login-2fa-google.png){width="400"}

## パスワードをリセット

アカウントに割り当てられた最後の 4 つのパスワードの再利用は許可されていません。

1. _Admin_ アカウントに関連付けられている **[!UICONTROL Email Address]** を入力します。

   ![ パスワードを忘れた場合 ](./assets/admin-sign-in-forgot-password.png){width="400"}

1. 「**[!UICONTROL Retrieve Password]**」をクリックします。

   アカウントがメールアドレスに関連付けられている場合、パスワードをリセットするためのメールが送信されます。

   >[!NOTE]
   >
   >_Admin_ パスワードは 7 文字以上で、文字と数字の両方を含める必要があります。 パスワードオプションについて詳しくは、[ 管理者 _セキュリティの設定_ を参照してください ](../systems/security-admin.md)。

## 管理者からサインアウト

1. 右上隅にある「_アカウント_ （![ アカウント ](../assets/icon-admin-user.png)）」アイコンをクリックします。

1. 「**[!UICONTROL Sign Out]**」をクリックします。

   ![ ログアウト ](./assets/admin-sign-out.png){width="700" zoomable="yes"}

_[!UICONTROL Sign In]_ページには、ログアウト済みのメッセージが表示されます。 コンピューターを無人のままにするときは、常に_ Admin _からサインアウトします。

## アカウント情報の編集

1. _アカウント_ （![ アカウントアイコン ](../assets/icon-admin-user.png)）アイコンをクリックします。

1. 「**[!UICONTROL Account Setting]**」をクリックします。

   ![ 口座情報 ](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. アカウント情報に必要な変更を加えます。

   ログイン資格情報を変更する場合は、必ず安全な場所に保存してください。

1. 現在のアカウントのパスワードを入力します。

1. 「**[!UICONTROL Save Account]**」をクリックします。

## 複数の管理者ログインを許可

管理者は、注文、顧客、製品、配送、支払いの各機能を管理するためのアクセス権を提供します。 デフォルトの設定では、セキュリティのベストプラクティスとして、管理者ユーザーアカウントに対して複数のログインを許可しないように設定されています。 ただし、この設定を変更して、管理者ユーザーが複数のデバイスからログインして、ビジネスワークフローに対応できるようにすることができます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のナビゲーションパネルで **[!UICONTROL Advanced]** を展開し、「**[!UICONTROL Admin]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Security]**」セクションを展開します。

1. **管理者アカウントの共有** については、「`Yes`」を選択します。

   ![ 管理者アカウントの共有を許可 ](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 管理者ユーザーのログイン名で大文字と小文字を区別するように設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のナビゲーションパネルで **[!UICONTROL Advanced]** を展開し、「**[!UICONTROL Admin]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Security]**」セクションを展開します。

1. **[!UICONTROL Login is Case Sensitive]** フィールドを `Yes` に設定します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US
