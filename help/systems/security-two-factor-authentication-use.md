---
title: ユーザーアカウント用の 2 要素認証の設定
description: 最初の管理者ログイン時に 2 要素認証を設定し、サポートされるデバイスアプリを使用して ID を認証する方法について説明します。
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# ユーザーアカウント用の 2 要素認証の設定

以下の手順では、Adobe CommerceまたはMagento Open Sourceへの初回ログイン時に 2 要素認証を設定する方法と、次のアプリおよびデバイスを使用して ID を認証する方法を示します。

詳しい手順については、 [管理者のログイン](../getting-started/admin-signin.md).

>[!NOTE]
>
>を有効にしたストア [!DNL Adobe Identity Management Services] (IMS) 認証では、ネイティブのAdobe CommerceとMagento Open Source2FA が無効になっています。 コマースインスタンスにログインしている管理者Adobeは、多くの管理者タスクを再認証する必要はありません。 認証は、管理者Adobe IMSが現在のセッションにログインする際にユーザーによって処理されます。 詳しくは、 [[!DNL Adobe Identity Management Service] (IMS) 統合の概要](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### 手順 1：セットアップ [!DNL Google Authenticator]

1. アカウントの資格情報を入力し、 _管理者_. QR コードが入った新しい認証子画面が表示されます。

1. を開きます。 **[!UICONTROL Google Authenticator]** モバイルデバイス上のアプリを参照してください。

1. プラス記号 ( **+** ) をクリックしてエントリを追加し、赤いボックスを QR コードと並べて、スマートフォンのカメラでスキャンします。

1. 携帯電話が QR コードを認識してエントリを追加したら、その 6 桁のコードを _管理者_ **[!UICONTROL Authenticator code]** フィールドに入力します。

1. 完了したら、「 **[!UICONTROL Confirm]**.

   ![Google Authenticator QR コード](./assets/storefront-2fa-google-qrcode.png){width="300"}

### 手順 2：でログインする [!DNL Google Authenticator]

1. アカウントの資格情報を入力し、コマースにログインします _管理者_.

   ![Google Authenticator — ログイン](./assets/storefront-2fa-google-code.png){width="300"}

1. 開く [!DNL Google Authenticator] を使用して、モバイルデバイスに接続できます。

1. プロンプトが表示されたら、6 桁の認証コードを入力します。

1. 今後のログイン用に認証を保存するには、 **[!UICONTROL Trust this device, do not ask again]** チェックボックス。

1. 完了したら、「 **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] 無料体験版を提供し、アカウントに関連付けられたユーザーの数に応じて料金を請求します。 フォロー [アカウントの設定とアプリのダウンロードに関する手順](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### 手順 1：セットアップ [!DNL Duo Security]

1. アカウントの資格情報を入力し、 _管理者_.

1. 次の場合に [!DNL Duo] 「設定」ページが表示され、「 **[!UICONTROL Start setup]** 次の操作を実行します。

   ![ストアフロントの例 — Duo 設定](./assets/storefront-2fa-duo-user1.png){width="300"}

1. デバイスを選択します。

1. プロンプトが表示されたら、電話番号を入力し、 **[!UICONTROL Continue]**.

   この例では、モバイルデバイスを使用しているので、お客様の電話番号を要求します。

1. インストールを促すメッセージが表示されたら [!DNL Duo Mobile] 電話の種類で、「 」をクリックします。 **[!UICONTROL I have Duo Mobile]**.

1. 開く [!DNL Duo Mobile] QR コードをスキャンして認証子をAdobe Commerceと同期します。 アクティベーションが完了すると、チェックマークが表示されます。

1. デバイスの設定を構成するには、サインイン時に実行するアクションを選択します。

   - `Ask me to choose an authenticator method`  — でログインおよび認証を行う際に、ユーザーが選択できるようにします。 _管理者_.
   - `Automatically send this device a Duo Push`  — アクセスを許可または拒否するメッセージをデバイスに送信します。
   - `Automatically call this device`  — を呼び出し、アクセス用に入力するパスコードを提供します。

   ![Duo 検証アクション](./assets/storefront-2fa-duo-user7.png){width="300"}

### 手順 2：でログインする [!DNL Duo Security]

次の例は、 `Ask me to choose an authenticator method`:

1. プロンプトが表示されたら、 _管理者_ ログインする資格情報。

   ![Duo — サインイン](./assets/storefront-2fa-duo-auth.png){width="300"}

1. 認証に使用するメソッドを選択します。

   - `Send Me a Push`  — クリックすると、次の宛先にプッシュ通知が届きます： [!DNL Duo Mobile]. 認証を受け付けます。
   - `Call Me`  — このオプションをクリックし、コード付きの呼び出しを受け取り、パスコードを入力します。
   - `Enter a Passcode`  — パスコードを受け取り、入力するには、このオプションをクリックします。

1. プッシュまたはコードを完了して、 _管理者_.

## [!DNL Authy]

[!DNL Authy] は、ユーザーに対して無料でアプリとサービスを提供しています。 指示に従って、デバイスまたはブラウザー用のアプリをダウンロードし、セットアップします。 詳しくは、 [[!DNL Authy] ドキュメント](https://authy.com/features/setup/).

### 手順 1：認証をセットアップする

1. アカウントの資格情報を入力し、 _管理者_.

   ![[!DNL Authy] 登録](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Authy に登録するように求められたら、次の操作を行います。

   - 国を選択します。

   - 電話番号を入力してください。

   - を選択します。 **[!UICONTROL Verification method]**: `SMS` または `Call Me`

   クリック **[!UICONTROL Continue]**. メッセージは、SMS テキストまたは呼び出しを通じて電話に送信されます。

1. 受け取った検証コードを入力し、「 **[!UICONTROL Verify]**.

1. 完了したら、「 **[!UICONTROL Confirm]**.

   ![[!DNL Authy] 検証コード](./assets/storefront-2fa-authy-verify.png){width="300"}

### 手順 2：でログインする [!DNL Authy]

1. アカウントの資格情報を入力し、 _管理者_.

   ![[!DNL Authy]  — サインイン](./assets/storefront-2fa-authy-access.png){width="300"}

1. 認証するには、次のいずれかの方法を選択します。

   - `Use one touch`  — アラートを [!DNL Authy] アプリを使用します。 デスクトップアプリケーションで、アクセスを許可します。
   - `Use authy token`  — コードの入力を求めるプロンプトが表示されます。 [!DNL Authy] アプリを使用します。

1. ログインで問題が発生した場合は、コードの受信に使用する方法を選択してください。 次に、 _管理者_.

   このアプリには、これらの追加の緊急手段が含まれています。

   - `Send me a code via SMS`  — 設定済みのモバイルデバイスにテキストの SMS メッセージが送信されます。
   - `Send me a code via phone call`  — ユーザーがコード付きの電話を受け取ります。

   アカウントが確認され、開きます。

## U2F ([!DNL Yubikey] およびその他のデバイス )

ソリューションプロバイダーの指示に従って、U2F デバイスを設定します。 詳しくは、次のようなベンダードキュメントを参照してください。 [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) 作成者 [!UICONTROL Yubico].

1. アカウントの資格情報を入力し、 _管理者_.

   ![U2F キーアクセス](./assets/storefront-2fa-u2f.png){width="300"}

1. キーのボタンを押します。

   認証を直ちにトリガーし、 _管理者_.

1. を挿入します。 **[!UICONTROL U2F key]** をコンピュータの USB ポートに挿入します。
