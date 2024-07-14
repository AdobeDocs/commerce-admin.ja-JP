---
title: ユーザーアカウントの二要素認証の設定
description: 管理者による最初のログイン時に二要素認証を設定し、サポートされているデバイスアプリを使用して ID を認証する方法を説明します。
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# ユーザーアカウントの二要素認証の設定

これらの手順では、Adobe CommerceまたはMagento Open Sourceへの最初のログイン時に二要素認証を設定する方法と、次のアプリやデバイスを使用して ID を認証する方法を示します。

手順について詳しくは、「[ 管理者によるログイン ](../getting-started/admin-signin.md)」を参照してください。

>[!NOTE]
>
>[!DNL Adobe Identity Management Services] （IMS）認証を有効にしているストアでは、ネイティブのAdobe CommerceとMagento Open Source 2FA が無効になっています。 Adobe資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 [[!DNL Adobe Identity Management Service]  （IMS）統合の概要を参照してください ](../getting-started/adobe-ims-integration-overview.md)。

## [!DNL Google Authenticator]

### 手順 1:[!DNL Google Authenticator] の設定

1. アカウントの資格情報を入力し、_管理者_ にログインします。 新しい認証画面が開き、QR コードが表示されます。

1. モバイルデバイスで **[!UICONTROL Google Authenticator]** アプリを開きます。

1. プラス記号（**+**）をクリックしてエントリを追加し、スマートフォンのカメラでスキャンする QR コードを赤いボックスに並べます。

1. 電話が QR コードを認識してエントリを追加したら、その 6 桁のコードを _Admin_ **[!UICONTROL Authenticator code]** フィールドに入力します。

1. 完了したら、「**[!UICONTROL Confirm]**」をクリックします。

   ![Google Authenticator QR コード ](./assets/storefront-2fa-google-qrcode.png){width="300"}

### 手順 2:[!DNL Google Authenticator] でログインする

1. アカウントの資格情報を入力し、Commerce _管理者_ にログインします。

   ![Google認証 – サインイン ](./assets/storefront-2fa-google-code.png){width="300"}

1. モバイルデバイスで [!DNL Google Authenticator] を開きます。

1. プロンプトが表示されたら、6 桁の認証コードを入力します。

1. 今後のログインで使用する認証を保存するには、「**[!UICONTROL Trust this device, do not ask again]**」チェックボックスを選択します。

1. 完了したら、「**[!UICONTROL Confirm]**」をクリックします。

## [!DNL Duo Security]

[!DNL Duo] は無料トライアルを提供し、アカウントに関連付けられているユーザーの数に応じて課金されます。 [ アカウントの設定とアプリのダウンロード ](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app) の手順に従ってください。

### 手順 1:[!DNL Duo Security] の設定

1. アカウントの資格情報を入力し、_管理者_ にログインします。

1. [!DNL Duo] Setup ページが表示されたら、**[!UICONTROL Start setup]** をクリックして以下を実行します。

   ![ ストアフロントの例 – Duo 設定 ](./assets/storefront-2fa-duo-user1.png){width="300"}

1. デバイスを選択します。

1. プロンプトが表示されたら、電話番号を入力し、「**[!UICONTROL Continue]**」をクリックします。

   この例ではモバイルデバイスを使用しているため、お客様の電話番号をリクエストしています。

1. お使いの電話の種類に合わせて [!DNL Duo Mobile] をインストールするように求めるメッセージが表示されたら、[**[!UICONTROL I have Duo Mobile]**] をクリックします。

1. [!DNL Duo Mobile] を開き、QR コードをスキャンして、認証子をAdobe Commerceと同期します。 アクティベーションが完了すると、チェックマークが表示されます。

1. デバイスの設定を構成するには、サインイン時に実行する操作を選択します。

   - `Ask me to choose an authenticator method` - _Admin_ にログインして認証する際に、ユーザーが選択できるようにします。
   - `Automatically send this device a Duo Push` — アクセスを許可または拒否するメッセージをデバイスに送信します。
   - `Automatically call this device` — アクセス用に入力するパスコードを呼び出し、提供します。

   ![Duo 検証アクション ](./assets/storefront-2fa-duo-user7.png){width="300"}

### 手順 2:[!DNL Duo Security] でログインする

`Ask me to choose an authenticator method` のオプションの例は次のとおりです。

1. プロンプトが表示されたら、_管理者_ の資格情報を入力してログインします。

   ![Duo - サインイン ](./assets/storefront-2fa-duo-auth.png){width="300"}

1. 認証に使用する方法を選択します。

   - `Send Me a Push`：クリックすると、[!DNL Duo Mobile] へのプッシュ通知を受け取ります。 認証を承認します。
   - 「`Call Me`」 – このオプションをクリックして、コードを含む呼び出しを受け取り、パスコードを入力します。
   - 「`Enter a Passcode`」 – このオプションをクリックして、パスコードを受け取り、入力します。

1. プッシュまたはコードを完了して、_管理者_ に完全にログインします。

## [!DNL Authy]

[!DNL Authy] は、ユーザーに対してアプリとサービスを無料で提供します。 指示に従って、デバイスまたはブラウザー用のアプリをダウンロードして設定します。 詳しくは、[[!DNL Authy]  ドキュメント ](https://authy.com/features/setup/) を参照してください。

### 手順 1:Authy の設定

1. アカウントの資格情報を入力し、_管理者_ にログインします。

   ![[!DNL Authy] 登録 ](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Authy に登録するように求められたら、次の操作を行います。

   - 国を選択します。

   - 電話番号を入力します。

   - **[!UICONTROL Verification method]** を選択：`SMS` または `Call Me`

   「**[!UICONTROL Continue]**」をクリックします。 メッセージは、SMS テキストまたは通話を通じて電話に送信されます。

1. 受け取った確認コードを入力し、「**[!UICONTROL Verify]**」をクリックします。

1. 完了したら、「**[!UICONTROL Confirm]**」をクリックします。

   確認コ ![[!DNL Authy] ド ](./assets/storefront-2fa-authy-verify.png){width="300"}

### 手順 2:[!DNL Authy] でログインする

1. アカウントの資格情報を入力し、_管理者_ にログインします。

   ![[!DNL Authy] - サインイン ](./assets/storefront-2fa-authy-access.png){width="300"}

1. 次のいずれかの認証方法を選択します。

   - `Use one touch` - [!DNL Authy] アプリにアラートを送信します。 アプリで、アクセスを受け入れます。
   - `Use authy token` - [!DNL Authy] アプリからコードを入力するように求められます。

1. ログインできない場合は、コードの受け取りに使用する方法を選択します。 次に、_管理者_ にアクセスするために受け取るコードを入力します。

   アプリには、これらの追加の緊急時方法が含まれています。

   - `Send me a code via SMS` – テキスト SMS メッセージが設定済みのモバイルデバイスに送信されます。
   - `Send me a code via phone call` — ユーザーはコードを含む電話を受け取ります。

   アカウントが検証され、開かれます。

## U2F （[!DNL Yubikey] およびその他のデバイス）

ソリューションプロバイダーの指示に従って、U2F デバイスを設定します。 詳しくは、[!UICONTROL Yubico] による [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) など、ベンダードキュメントを参照してください。

1. アカウントの資格情報を入力し、_管理者_ にログインします。

   ![U2F キーアクセス ](./assets/storefront-2fa-u2f.png){width="300"}

1. キーのボタンを押します。

   認証はすぐにトリガーし、_Admin_ を開きます。

1. **[!UICONTROL U2F key]** をコンピューターの USB ポートに挿入します。
