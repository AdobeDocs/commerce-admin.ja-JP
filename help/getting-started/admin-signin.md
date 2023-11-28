---
title: 管理者ユーザーアカウント
description: 管理者アカウントと、2 要素認証を使用して管理者にログインする方法について説明します。
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# 管理者アカウント

プライマリ Admin アカウントは、インストール時に最初に設定されたアカウントで、初期プレースホルダー情報やサンプルデータ情報が含まれている場合があります。 このアカウントの指定された所有者は、ユーザー名とパスワードをパーソナライズし、名、姓、電子メールアドレスをいつでも更新できます。 このアカウントは、 _スーパーユーザー_ はデフォルトですべての権限を持ち、通常、はビジネスに必要な管理者ユーザーアカウントを作成します。

- 詳しくは、 [ユーザーの作成](../systems/permissions-users-all.md#create-a-user) ユーザーの追加や編集について詳しくは、を参照してください。

- 詳しくは、 [権限](../systems/permissions.md) および [ユーザーの役割](../systems/permissions-user-roles.md) 管理者ロールとユーザーロールについて詳しくは、を参照してください。

{{ims-admin-note}}

## 管理者のログイン

The [!DNL Commerce] _管理者_ は、複数の層のセキュリティ対策によって保護されており、ストア、注文、および顧客データへの不正なアクセスを防ぎます。 初めて _管理者_&#x200B;の場合は、ユーザー名とパスワードを入力し、 [二段階認証](../systems/security-two-factor-authentication.md) (2FA)。

ストアの設定に応じて、 [CAPTCHA](../systems/security-google-recaptcha.md) 一連のキーボード文字の入力、パズルの解決、共通のテーマを持つ一連の画像のクリックなど、解決に関する課題。 これらのテストは、自動ボットではなく、ユーザーを人間として識別するように設計されています。

セキュリティを強化するために、 _管理者_ 各ユーザーが [権限](../systems/permissions.md) にアクセスし、 [ログイン試行](../configuration-reference/advanced/admin.md). デフォルトでは、6 回試行した後にアカウントがロックされ、ユーザーは数分待ってから再試行する必要があります。 [ロックされたアカウント](../systems/permissions-users-all.md#locked-users) また、 _管理者_.

>[!NOTE]
>
>初めて _管理者_&#x200B;を使用する場合、次のように求められます。 _管理者使用状況データ収集を許可_. 詳しくは、 [使用状況データの収集](admin.md#usage-data-collection) を参照してください。

![管理者のログイン](./assets/admin-login.png){width="400"}

### 手順 1:2 要素認証を設定する

にログインする前に、 _管理者_ ストアので、2 要素認証ソリューションをセットアップし、使用する準備を整える必要があります。 各ソリューションで使用される認証プロセスについて詳しくは、 [二段階認証の使用](../systems/security-two-factor-authentication-use.md). デフォルトでは、 [!DNL Commerce] サポート [Google Authenticator][1].

質問する [!DNL Commerce] ストアで 2FA ソリューションがサポートされるシステム管理者。 次に、プロバイダの指示に従って、優先する 2FA ソリューションの設定を完了します。

### 手順 2：管理者にログインする

1. 次を入力します。 _管理者_ 次の期間に指定された URL [!DNL Commerce] インストール。

   デフォルト _管理者_ URL が次のようになります `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >このドキュメントでは `admin` ほとんどの例ではベース URL として、一意で推測しにくいを選択することをお勧めします [カスタム URL](../stores-purchase/store-urls.md) （の） _管理者_ お客様のストアの

   ページのブックマークを追加したり、デスクトップにショートカットを保存してアクセスしやすくすることができます。

1. を入力します。 _管理者_ **[!UICONTROL Username]** および **[!UICONTROL Password]**.

1. （オプション）ストアに対して CAPTCHA が有効になっている場合は、画面に表示される指示に従って課題を解決します。

   詳しくは、 [CAPTCHA](../systems/security-captcha.md) および [reCAPTCHA](../systems/security-google-recaptcha.md).

1. クリック **[!UICONTROL Sign in]**.

   これが初めての _管理者_ アカウントから、設定手順へのリンクが記載された電子メールが届きます。

### 手順 3: 2FA 設定を完了する

次の例は、 _管理者_ アカウントをGoogle Authenticator に設定します。

1. QR コードが表示されたら、次のいずれかの方法を使用してコードをキャプチャし、Google Authenticator を _管理者_ アカウント。

   ![Google Authenticator のセットアップ](./assets/admin-login-google-auth-setup.png){width="400"}

   - スマートフォンを使用して QR コードをキャプチャ

     スマートフォンで、Google Authenticator を起動します。 次をタップします。 _プラス記号_ (+) をクリックします。 次に、画面の下部で、 **[!UICONTROL Scan Barcode]** QR コードを撮ります。

   - ブラウザーから QR コードをキャプチャ

     Google Authenticator がブラウザーに拡張機能としてインストールされている場合は、 **Authenticator** アイコンをクリックし、ページをキャプチャします。

   - QR コードを手動で入力

     QR コードの下のテキストの文字列をコピーします。 スマートフォンまたはブラウザーでGoogle Authenticator を起動し、プラス記号 (+) をクリックします。 次に、を選択します。 **[!UICONTROL Manual Entry]**. の下 **[!UICONTROL Account]**」に、 _管理者_ アカウントを作成し、QR コード文字列を **[!UICONTROL Key]** フィールドに入力します。

1. にログインするには、以下を実行します。 _管理者_ 2 要素認証を使用して、Google Authenticator で生成された 6 桁のコードを **[!UICONTROL Authenticator code]** 「 」フィールドで「 」をクリックし、 **[!UICONTROL Confirm]**.

   ![Authenticator コードを入力します。](./assets/admin-login-2fa-google.png){width="400"}

## パスワードをリセット

アカウントに割り当てられた最後の 4 つのパスワードの再利用は許可されていません。

1. 次を入力します。 **[!UICONTROL Email Address]** これは _管理者_ アカウント。

   ![パスワードを忘れた場合](./assets/admin-sign-in-forgot-password.png){width="400"}

1. クリック **[!UICONTROL Retrieve Password]**.

   アカウントが電子メールアドレスに関連付けられている場合は、パスワードをリセットするための電子メールが送信されます。

   >[!NOTE]
   >
   >An _管理者_ パスワードは 7 文字以上で、文字と数字の両方を含める必要があります。 詳しくは、 [設定 _管理者_ セキュリティ](../systems/security-admin.md) を参照してください。

## 管理者からのログアウト

1. 右上隅で、 _アカウント_ (![アカウント](../assets/icon-admin-user.png)) アイコンをクリックします。

1. クリック **[!UICONTROL Sign Out]**.

   ![ログアウト](./assets/admin-sign-out.png){width="700" zoomable="yes"}

The _[!UICONTROL Sign In]_ページには、ログアウトしたというメッセージが表示されます。 からサインアウト_&#x200B;管理者&#x200B;_コンピューターを無人にしておくときは常に。

## アカウント情報の編集

1. 次をクリック： _アカウント_ (![アカウントアイコン](../assets/icon-admin-user.png)) アイコンをクリックします。

1. クリック **[!UICONTROL Account Setting]**.

   ![アカウント情報](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. アカウント情報に必要な変更を加えます。

   ログイン資格情報を変更する場合は、必ず安全な場所に保存してください。

1. 現在のアカウントのパスワードを入力します。

1. クリック **[!UICONTROL Save Account]**.

## 複数の管理者ログインを許可

管理者は、注文、顧客、製品、送料、支払いの各機能を管理するためのアクセス権を提供します。 デフォルトの設定では、セキュリティのベストプラクティスとして、管理者ユーザーアカウントへの複数のログインを許可しないように設定されています。 ただし、この設定を変更して、管理者ユーザーが複数のデバイスからログインして、ビジネスワークフローに対応できるようにすることができます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Admin]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Security]** 」セクションに入力します。

1. の場合 **管理者アカウントの共有**&#x200B;を選択します。 `Yes`.

   ![管理者アカウントの共有を許可](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 管理者ユーザーのログイン名を大文字と小文字を区別するように設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Admin]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Security]** 」セクションに入力します。

1. を設定します。 **[!UICONTROL Login is Case Sensitive]** ～に向かって `Yes`.

1. クリック **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US
