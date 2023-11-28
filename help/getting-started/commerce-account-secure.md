---
title: セキュリティで保護 [!DNL Commerce] アカウント
description: 2 要素認証を使用して [!DNL Commerce] アカウント。
exl-id: 4847b5cb-a93a-40d0-8c31-c30afa27c0ce
feature: User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 0%

---

# セキュリティで保護 [!DNL Commerce] アカウント

2 要素認証（TFA または 2FA）は、セキュリティの層を強化し、 [!DNL Commerce] アカウントを不正なアクセスから削除しました。 ログインプロセスを完了するには、TFA で _第 2 の要因_ に加えて、標準のユーザー名およびパスワードの資格情報を追加します。 この 2 つ目の要因は、モバイルデバイスにインストールされた TFA アプリケーションで継続的に生成され、と組み合わされる一時的な検証コードの形式を取ります [!DNL Commerce] アカウント。

TFA を有効にすると、アカウントのセキュリティが高まります。 権限のないユーザーは、ユーザー名とパスワードの資格情報（第 1 の要素）と、個人用デバイス上の TFA アプリケーションから有効な検証コード（第 2 の要素）の両方を持っていない限り、ログインできません。

>[!NOTE]
>
>を保護する 2 要素認証 _管理者_ の値は別々の設定になっています。 詳しくは、 [二段階認証](../systems/security-two-factor-authentication.md).

## 始める前に

TFA を使用するには、TFA アプリケーションがパーソナルデバイス（スマートフォン、タブレット、コンピューターなど）にインストールされている必要があります。 利用可能なオプションは多数ありますが、人気の高い無料オプションは次のとおりです。

- Google Authenticator(iOS、Android™、BlackBerry®)

- 認証者 (iOS、Android™)

- Microsoft® Authenticator(iOS、Android™、Windows Phone)

## 二段階認証の有効化

1. にログインします。 [[!DNL Commerce] アカウント][1]{:target=&quot;_blank&quot;}。

1. 左側のナビゲーションウィンドウで、「 」を選択します。 **[!UICONTROL Account Settings]**&#x200B;を選択し、 **[!UICONTROL Two-factor Authentication]**.

   ![TFA を有効にする](./assets/2fa-enable.png){width="600" zoomable="yes"}

1. 選択 **[!UICONTROL Enable]** をクリックして、2 要素認証の設定プロセスを開始します。

1. 次を入力します。 **[!UICONTROL Verification Code]** メールに送信し、 **[!UICONTROL Verify Code]** をクリックして続行します。

   ![検証コードを入力](./assets/2fA-verification-code-prompt.png){width="400"}

1. ダウンロードして個人用デバイスにインストールした 2 要素認証アプリケーションを開きます。

1. 次の日： [!UICONTROL SETUP TWO-FACTOR AUTHENTICATION] フォーム、 **[!UICONTROL Setup Code]** をクリックして、Adobe Commerceを TFA アプリケーションに追加します。

   ![TFA アプリにAdobe Commerceを追加](./assets/commerce-account-2fa-setup-app.png){width="400"}

   TFA アプリケーションを使用して QR コードをスキャンするか、手動で入力することで、コードを追加できます。 このコードは、TFA アプリケーションと [!DNL Commerce] アカウントを作成し、セキュアなアカウントアクセスを実現するための検証コードを生成する権限を TFA アプリに付与します。

1. 設定を完了します。

   - 次の日： [!UICONTROL SETUP TWO FACTOR-AUTHENTICATION] フォームで、2 要素認証アプリケーションから検証コードを入力します。

   - 選択 **[!UICONTROL Verify Code]**.

   >[!NOTE]
   >
   >セキュリティのために、TFA アプリケーションの検証コードは継続的に期限切れになり、再生成されます。 **_常に_** 現在表示されているコードを使用します。

1. を保存します。 **[!UICONTROL Recovery Codes]** 安全でアクセシブルな場所に提示されていた

   ![回復コードを保存](./assets/commerce-account-2fa-store-recovery-codes.png){width="400"}

   にログインしたときに検証コードを指定できない場合 [!DNL Commerce] アカウントにアクセスするには、回復コードを使用する必要があります。

   各回復コードは 1 回だけ使用できますが、次の操作は可能です。 [生成](#generate-new-recovery-codes) 新しいもの。 回復コードでは大文字と小文字が区別されます。

1. 確認チェックボックスを選択し、「 」を選択します。 **[!UICONTROL Submit]** をクリックして続行します。

1. アカウントへのアクセス権を確実に回復するには、 **[!UICONTROL Recovery Email]**.

   この電子メールアドレスは、2 要素認証アプリケーションから検証コードを生成できず、未使用の事前生成回復コードへのアクセス権がない場合に必要です。

   24 時間に 1 回、一時的な回復コードを生成し、指定された回復用電子メールアドレスに送信できます。 このコードを使用して、アカウントへのアクセスを再度取り戻します。

   >[!IMPORTANT]
   >
   >回復用メールアカウントへのアクセスを維持します。 そうでない場合は、そのアカウントに送信された一時的な回復コードを使用できません。

   ![回復メールの設定](./assets/commerce-account-2fa-set-recovery-email.png){width="400"}

1. 確認チェックボックスを選択し、「 」を選択します。 **[!UICONTROL Submit]** をクリックして、2 要素認証の設定プロセスを完了します。

   - 通知が、 [!DNL Commerce] アカウントを使用して、2 要素認証が正常に有効になっていることを確認します。

   - 設定を確認する通知が回復用電子メールアカウントに送信されます。

>[!TIP]
>
>個人用デバイスを紛失したり、新しいデバイスを入手した場合は、 [二段階認証アプリを変更する](#change-your-two-factor-authentication-application) 新しい回復コードを生成します。

## 検証コードを使用してログイン

1. 次に移動： [!DNL Commerce] [アカウントログイン][1]{:target=&quot;_blank&quot;}。

1. ユーザー名とパスワードの資格情報を入力し、「 」を選択します。 **[!UICONTROL Login]**.

1. 次を入力します。 **[!UICONTROL Verification Code]** を 2 要素認証アプリケーションに表示します。

   ![検証コードを入力](./assets/commerce-account-2fa-login-verification-code.png){width="600"}

1. 選択 **[!UICONTROL Submit]** をクリックして、ログインプロセスを完了します。

## 回復コードを使用してログインします。

1. 次に移動： [!DNL Commerce] [アカウントログイン][1]{:target=&quot;_blank&quot;}。

1. ユーザー名とパスワードの資格情報を入力し、「 」を選択します。 **[!UICONTROL Login]**.

1. 選択 **[!UICONTROL Use recovery code]** をクリックして、検証コードプロンプトを回避します。

1. 未使用の **[!UICONTROL Recovery Code]** プロンプトが表示されたら、

   ![回復コードを入力](./assets/2fa-recovery-code.png){width="600"}

1. 選択 **[!UICONTROL Submit]** をクリックして、ログインプロセスを完了します。

## 回復用メールを使用してログインします

1. にログインします。 [[!DNL Commerce] アカウント][1]{:target=&quot;_blank&quot;}。

1. ユーザー名とパスワードの資格情報を入力し、「 」を選択します。 **[!UICONTROL Login]**.

1. 選択 **[!UICONTROL Use recovery code]** をクリックして、検証コードプロンプトを回避します。

1. E メールで一時的な回復コードを取得するには、 **[!UICONTROL recovery email]** リンク。

   ![回復メールを使用](./assets/2fa-recovery-email.png){width="600"}

1. 回復用メールアカウントを開いて一時コードを取得し、指定されたフィールドにコードを入力します。

1. 選択 **[!UICONTROL Submit]** をクリックして、ログインプロセスを完了します。

一時的な回復コードを使用してアカウントにアクセスした後、 [新しい回復コードを生成します](#generate-new-recovery-codes) を保存して、それ以上のアカウントアクセスの問題を回避します。

## 回復コードを表示します

1. 次に移動： [!DNL Commerce] [アカウントログイン][1]{:target=&quot;_blank&quot;}。

1. ユーザー名とパスワードの資格情報を入力し、「 」を選択します。 **[!UICONTROL Login]**.

1. 前述の 2 要素認証方法の 1 つを使用して、ログインプロセスを完了します。

1. 左側のナビゲーションウィンドウで、「 」を選択します。 **[!UICONTROL Account Settings]**&#x200B;を選択し、 **[!UICONTROL Two-factor Authentication]**.

   ![2FA 設定](./assets/commerce-account-2fa-manage.png){width="600" zoomable="yes"}

1. 事前に生成された回復コードを表示するには、 **回復コードの表示**.

1. 次を入力します。 **[!UICONTROL Verification Code]** メールに送信し、 **[!UICONTROL Verify Code]** をクリックして続行します。

   ![検証コードを入力](./assets/2fA-verification-code-prompt.png){width="400"}

1. を保存します。 **回復コード** 安全でアクセシブルな場所に提示されていた

   にログインするための検証コードを指定できない場合は、 [!DNL Commerce] アカウント、回復コードを使用することが、アカウントのアクセスを再び取得する唯一の方法です。

   各リカバリ・コードは 1 回だけ使用できますが、常に使用できます [生成](#generate-new-recovery-codes) 新しいもの。 回復コードでは大文字と小文字が区別されます。

   ![回復コードの表示](./assets/2fa-view-recovery.png){width="400"}

1. 確認チェックボックスを選択し、「 」を選択します。 **[!UICONTROL Submit]** をクリックしてダイアログを閉じます。

## 新しい回復コードを生成します

1. 次に移動： [!DNL Commerce] [アカウントログイン][1]{:target=&quot;_blank&quot;}。

1. ユーザー名とパスワードの資格情報を入力し、「 」を選択します。 **[!UICONTROL Login]**.

1. 前述の 2 要素認証方法の 1 つを使用して、ログインプロセスを完了します。

1. 左側のナビゲーションウィンドウで、「 」を選択します。 **[!UICONTROL Account Settings]**&#x200B;を選択し、 **[!UICONTROL Two-factor Authentication]**.

1. 新しい事前生成リカバリ・コードを生成するには、次を選択します。 **新しい回復コードの生成**.

1. 次を入力します。 **[!UICONTROL Verification Code]** メールに送信し、 **[!UICONTROL Verify Code]** をクリックして続行します。

1. を保存します。 **回復コード** 安全でアクセシブルな場所に提示されていた

   にログインしたときに検証コードを指定できない場合 [!DNL Commerce] アカウント、回復コードを使用することが、アカウントのアクセスを再び取得する唯一の方法です。

   以前に生成されたすべての回復コードが無効になり、破棄する必要があります（生成された回復コードの現在のセットのみが機能します）。 回復コードでは大文字と小文字が区別されます。

1. 確認チェックボックスを選択し、「 」を選択します。 **[!UICONTROL Submit]** をクリックしてダイアログを閉じます。

## 回復メールを変更する

1. 次に移動： [!DNL Commerce] [アカウントログイン][1]{:target=&quot;_blank&quot;}。

1. ユーザー名とパスワードの資格情報を入力し、「 」を選択します。 **[!UICONTROL Login]**.

1. 前述の 2 要素認証方法の 1 つを使用して、ログインプロセスを完了します。

1. 左側のナビゲーションウィンドウで、「 」を選択します。 **[!UICONTROL Account Settings]**&#x200B;を選択し、 **[!UICONTROL Two-factor Authentication]**.

1. 選択 **リカバリメールの変更** をクリックして、アカウントの回復メールをファイルに変更します。

1. 次を入力します。 **[!UICONTROL Verification Code]** メールに送信し、 **[!UICONTROL Verify Code]** をクリックして続行します。

1. アカウントへのアクセス権を確実に回復するには、 **回復メール**.

   この電子メールアドレスは、2 要素認証アプリケーションから検証コードを生成できず、未使用の事前生成回復コードへのアクセス権がない場合に必要です。

   24 時間に 1 回、一時的な回復コードを生成し、指定された回復用電子メールアドレスに送信できます。 このコードを使用して、アカウントへのアクセスを再度取得できます。

   >[!IMPORTANT]
   >
   >回復用メールアカウントへのアクセスを維持します。 そうでない場合は、そのアカウントに送信された一時的な回復コードを使用できません。

1. 確認チェックボックスを選択し、「 」を選択します。 **[!UICONTROL Submit]** をクリックしてダイアログを閉じます。

   システムは、特定のメールアドレスが一時的な回復コードを受け取るための回復メールとしてファイル上にあることを確認するために指定した回復メールに、電子メール通知を送信します。

## 2 要素認証アプリケーションの変更

1. 次に移動： [!DNL Commerce] [アカウントログイン][1]{:target=&quot;_blank&quot;}。

1. ユーザー名とパスワードの資格情報を入力し、「 」を選択します。 **[!UICONTROL Login]**.

1. 前述の 2 要素認証方法の 1 つを使用して、ログインプロセスを完了します。

1. 左側のナビゲーションウィンドウで、「 」を選択します。 **[!UICONTROL Account Settings]**&#x200B;を選択し、 **[!UICONTROL Two-factor Authentication]**.

1. 選択 **TFA アプリケーションを変更** magento.comアカウントで別の TFA アプリケーションを使用する場合。

1. 次を入力します。 **[!UICONTROL Verification Code]** メールに送信し、 **[!UICONTROL Verify Code]** をクリックして続行します。

1. パーソナルデバイスで二段階認証アプリケーションを開きます。

1. 次を入力します。 **コードを設定** を 2 要素認証アプリケーションに追加します。

   TFA アプリケーションを使用して QR コードをスキャンするか、手動で入力することで、コードを追加できます。 このコードは、TFA アプリケーションと [!DNL Commerce] アカウントを作成し、TFA アプリの権限を有効にして、安全なアカウントアクセス用の検証コードを生成します。

   >[!NOTE]
   >
   >セキュリティのために、TFA アプリケーションの検証コードは継続的に期限切れになり、再生成されます。 **_常に_** 現在表示されているコードを使用します。

1. TFA アプリケーションとのペアリング [!DNL Commerce] アカウントに、 **[!UICONTROL Verification Code]** を TFA アプリケーションに表示し、「 **[!UICONTROL Verify Code]** をクリックして続行します。

1. を保存します。 **回復コード** 安全でアクセシブルな場所に提示されていた

   にログインしたときに検証コードを指定できない場合 [!DNL Commerce] アカウント、アカウントのアクセスを再び取り戻す唯一の方法は、回復コードを使用することです。

   各リカバリ・コードは 1 回だけ使用できますが、常に使用できます [生成](#generate-new-recovery-codes) 新しいもの。 回復コードでは大文字と小文字が区別されます。 回復コードでは大文字と小文字が区別されます。

1. 確認するチェックボックスを選択して選択します。 **[!UICONTROL Submit]** をクリックして続行します。

1. アカウントへのアクセス権を確実に回復するには、 **回復メール**.

   この電子メールアドレスは、2 要素認証アプリケーションから検証コードを生成できず、未使用の事前生成回復コードへのアクセス権がない場合に必要です。

   24 時間に 1 回、一時的な回復コードを生成し、指定された回復用電子メールアドレスに送信できます。 このコードを使用して、アカウントへのアクセスを再度取り戻します。

   >[!IMPORTANT]
   >
   >回復用メールアカウントへのアクセスを維持します。 そうでない場合は、そのアカウントに送信された一時的な回復コードを使用できません。

1. 確認チェックボックスを選択し、「 」を選択します。 **[!UICONTROL Submit]** をクリックして、2 要素認証の設定プロセスを完了します。

   一時的な回復コードを受け取るために、特定の電子メールアドレスが回復用電子メールとしてファイル上にあることを確認するために指定した回復用電子メールに電子メール通知が送信されます。

## 二段階認証を無効にする

>[!IMPORTANT]
>
>組織のセキュリティポリシーでAdobe Commerceアカウントに多要素認証が必要な場合、二要素認証を無効にすることはできません。

1. 次に移動： [!DNL Commerce] [アカウントログイン][1]{:target=&quot;_blank&quot;}。

1. ユーザー名とパスワードの資格情報を入力し、「 」を選択します。 **[!UICONTROL Login]**.

1. 前述の 2 要素認証方法の 1 つを使用して、ログインプロセスを完了します。

1. 左側のナビゲーションウィンドウで、「 」を選択します。 **[!UICONTROL Account Settings]** を選択し、 **[!UICONTROL Two-factor Authentication]** の下に

1. 選択 **[!UICONTROL Disable]** をクリックして、TFA 非アクティブ化プロセスを開始します。

1. 次を入力します。 **[!UICONTROL Verification Code]** メールに送信し、 **[!UICONTROL Verify Code]** をクリックして続行します。

1. 確認チェックボックスを選択し、「 」を選択します。 **[!UICONTROL Submit]** をクリックして、2 要素認証の非アクティブ化を完了します。

   システムが、 [!DNL Commerce] アカウント。

   ![TFA を無効にする](./assets/2fa-disable.png){width="400"}

[1]: https://account.magento.com/customer/account/login
