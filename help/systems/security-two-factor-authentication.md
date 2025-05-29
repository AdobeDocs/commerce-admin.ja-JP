---
title: 2 要素認証（2FA）
description: システムとデータのセキュリティを確保するための 2 要素認証のサポートについて説明します。
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---

# 2 要素認証（2FA）

Adobe CommerceまたはMagento Open Source インストールのCommerce _管理者_ は、ストア、注文および顧客データへのアクセスを可能にします。 データへの不正アクセスを防ぐには、_Admin_ にログインしようとするすべてのユーザーが、本人確認のために認証プロセスを完了する必要があります。

>[!NOTE]
>
>この二要素認証（2FA）の実装は、_Admin_ にのみ適用され、カスタマーアカウントでは使用できません。 Commerce アカウントを保護する二要素認証には、別の設定があります。 詳しくは、[Commerce アカウントの保護 ](../getting-started/commerce-account-secure.md) を参照してください。

2 要素認証が広く使用されており、同じアプリで異なる web サイトのアクセスコードを生成するのが一般的です。 この追加認証により、自分だけがユーザーアカウントにログインできるようになります。 パスワードを紛失した場合、またはボットがパスワードを推測した場合、二要素認証により保護レイヤーが追加されます。 例えば、Google Authenticator を使用してストアの管理者、Commerce アカウント、Google アカウントのコードを生成することができます。

![ セキュリティ設定 iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerceは、複数のプロバイダーの 2FA メソッドをサポートしています。 ID を確認するために、ユーザーがログイン時に入力するワンタイムパスワード（OTP）を生成するアプリのインストールを必要とする場合があります。 ユニバーサル第 2 係数（U2F）デバイスは、キーフォブに似ており、ID を確認するための一意のキーを生成します。 他のデバイスは、USB ポートに挿入されたときに ID を確認します。 ストア管理者は、ユーザー ID を検証するために、使用可能な 2FA メソッドを 1 つ以上要求できます。 2FA 設定は、Adobe Commerceのインストールに関連付けられているすべての web サイトとストアに適用されます。

ユーザーが初めて _Admin_ にログインしたときには、必要な各 [2FA](../configuration-reference/security/2fa.md) メソッドを設定し、関連するアプリまたはデバイスを使用して ID を検証する必要があります。 この初期設定後、ユーザーはログインするたびに設定されたメソッドのいずれかを使用して認証する必要があります。 各ユーザーの 2FA 情報は、_管理者_ アカウントに記録され、必要に応じて [ リセット ](security-two-factor-authentication-manage.md) できます。 ログインプロセスについて詳しくは、「[_管理者_ ログイン ](../getting-started/admin-signin.md)」を参照してください。

>[!NOTE]
>
>Adobe Identity Management サービス（IMS）認証を有効にしているストアでは、ネイティブのAdobe CommerceおよびMagento Open Source 2FA が無効になっています。 Adobe資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 [Adobe Identity Management Service （IMS）統合の概要 ](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html) を参照してください。

管理者での二要素認証の概要については、この [ ビデオデモ ](https://video.tv.adobe.com/v/339104?quality=12&learn=on) をご覧ください。

## 必要な 2FA プロバイダーの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Security]**」を展開し、「**[!UICONTROL 2FA]**」を選択します。

1. _[!UICONTROL General]_&#x200B;セクションで、使用するプロバイダーを選択します。

   | プロバイダ | 関数 |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | ユーザー認証用にアプリケーション内に 1 回限りのパスワードを生成します。 |
   | [!UICONTROL Duo Security] | SMS およびプッシュ通知を提供します。 |
   | [!UICONTROL Authy] | 時間に依存する 6 桁のコードを生成し、SMS または音声通話 2FA 保護またはトークンを配信します。 |
   | [!UICONTROL U2F Devices (Yubikey and others)] | [[!DNL YubiKey]](https://www.yubico.com/) などの認証に物理デバイスを使用します。 |

   複数の方法を選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各項目をクリックします。

1. 必要な 2FA 方式ごとに [settings](../configuration-reference/security/2fa.md) を入力します。

   ![ セキュリティ設定 – 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

   ユーザーが初めて _Admin_ にログインするときには、必要な 2FA 方式をそれぞれ設定する必要があります。 この初期設定の後、ログインするたびに、設定されたメソッドのいずれかで認証する必要があります。

## 2FA プロバイダー設定

必要な 2FA 方式ごとに設定を完了します。

### Google

ログイン時にワンタイムパスワード（OTP）を使用できる期間を変更するには、「**[!UICONTROL Use system value]**」チェックボックスをオフにします。 次に、**[!UICONTROL OTP Window]** を有効にする秒数を入力します。

![ セキュリティ設定 – Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Adobe Commerce 2.4.7 以降では、管理者のワンタイムパスワード（OTP）の有効期限が切れた後に、システムが OTP ウィンドウ設定を受け入れる時間（秒単位）を制御します。 この値は 30 秒未満にする必要があります。 システムのデフォルト設定は `29` です。<br><br> バージョン 2.4.6 では、OTP ウィンドウの設定によって、有効な過去および未来の OTP コードの数が決まります。 値 `1` は、現在の OTP コードに過去と未来の 1 つのコードを加えたものが、任意の時点で有効であることを示します。

### [!DNL Duo Security]

Duo Security アカウントから次の資格情報を入力します。

- クライアント ID
- クライアント秘密鍵
- 統合キー
- 秘密鍵
- API ホスト名

![ セキュリティ設定 – Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. [!DNL Authy] アカウントから API キーを入力します。

1. 認証時に表示されるデフォルトのメッセージを変更するには、「**[!UICONTROL Use system value]**」チェックボックスをオフにします。 次に、表示する **[!UICONTROL OneTouch Message]** を入力します。

   ![ セキュリティ設定 – Authy](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F デバイス （[!DNL Yubikey] など）

ストアドメインは、認証プロセス中にデフォルトで使用されます。 認証の課題にカスタムドメインを使用するには、「**[!UICONTROL Use system value]**」チェックボックスをオフにします。 次に、**[!UICONTROL WebAPi Challenge Domain]** を入力します。

![ セキュリティ設定 – U2F デバイス ](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
