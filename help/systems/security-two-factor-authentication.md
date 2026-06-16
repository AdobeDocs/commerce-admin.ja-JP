---
title: 二段階認証（2FA）
description: システムとデータのセキュリティを確保するための2要素認証のサポートについて説明します。
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/-201IPkmoP1dmQL3kk4zb3XdTgrYtiUovj4-hkaNrnc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 848
ht-degree: 0%

---

# 二段階認証（2FA）

Adobe CommerceまたはMagento Open Sourceのインストール環境のCommerce _管理者_&#x200B;は、ストア、注文、顧客データにアクセスできます。 データへの不正アクセスを防ぐには、_管理者_&#x200B;にログインしようとしているすべてのユーザーが、IDを確認するための認証プロセスを完了する必要があります。

>[!NOTE]
>
>この2要素認証（2FA）の実装は、_管理者_&#x200B;にのみ適用され、顧客アカウントでは使用できません。 Commerce アカウントを保護する2要素認証には、別の設定が必要です。 詳しくは、[Commerce アカウントの保護](../getting-started/commerce-account-secure.md)にアクセスしてください。

二段階認証は広く利用されており、同じアプリでさまざまなweb サイトのアクセスコードを生成するのが一般的です。 この追加の認証により、ユーザーのみがユーザーアカウントにログインできるようになります。 パスワードを失ったり、ボットがそれを推測したりすると、二段階認証は保護のレイヤーを追加します。 例えば、Google Authenticatorを使用して、ストアの管理者、Commerce アカウント、Google アカウントのコードを生成できます。

![&#x200B; セキュリティ設定のiphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerceは、複数のプロバイダーの2FA方式をサポートしています。 ログイン時にユーザーがIDを確認するために入力するワンタイムパスワード（OTP）を生成するアプリのインストールが必要な場合もあります。 ユニバーサル第2要素（U2F）デバイスは、キーフォブに似ており、IDを検証するための一意のキーを生成します。 他のデバイスは、USB ポートに挿入されたときにIDを確認します。 ストア管理者は、ユーザーIDを検証するために、1つ以上の利用可能な2FA方法を必要とすることができます。 2FA設定は、Adobe Commerce インストールに関連付けられているすべてのweb サイトとストアに適用されます。

ユーザーが初めて&#x200B;_Admin_&#x200B;にログインする場合は、必要な各[2FA](../configuration-reference/security/2fa.md) メソッドを設定し、関連するアプリまたはデバイスを使用してIDを確認する必要があります。 この初期設定の後、ユーザーはログインするたびに、設定されたメソッドのいずれかを使用して認証する必要があります。 各ユーザーの2FA情報は&#x200B;_管理者_ アカウントに記録され、必要に応じて[&#x200B; リセット &#x200B;](security-two-factor-authentication-manage.md)できます。 サインインプロセスについて詳しくは、[_管理者_ ログイン &#x200B;](../getting-started/admin-signin.md)にアクセスしてください。

>[!NOTE]
>
>Adobe Identity Management サービス（IMS）認証を有効にしているストアでは、ネイティブのAdobe CommerceとMagento Open Source 2FAが無効になっています。 Adobeの資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理者タスクで再認証を行う必要はありません。 認証は、管理者ユーザーが現在のセッションにログインしたときにAdobe IMSによって処理されます。 [Adobe Identity Management Service （IMS）統合の概要](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=ja)を参照してください。

この[&#x200B; ビデオ デモ &#x200B;](https://video.tv.adobe.com/v/339104?quality=12&learn=on)では、管理画面での2要素認証の概要を説明しています。

## 必要な2FA プロバイダーの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Security]**&#x200B;を展開し、**[!UICONTROL 2FA]**&#x200B;を選択します。

1. 「_[!UICONTROL General]_」セクションで、使用するプロバイダーを選択します。

   | プロバイダー | 関数 |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | ユーザー認証用のアプリケーションで1回限りのパスワードを生成します。 |
   | [!UICONTROL Duo Security] | SMSとプッシュ通知を提供します。 |
   | [!UICONTROL Authy] | 時間に依存する6桁のコードを生成し、SMSまたは音声コール 2FAの保護またはトークンを配信します。 |
   | [!UICONTROL U2F Devices (Yubikey and others)] | [[!DNL YubiKey]](https://www.yubico.com/)などの物理デバイスを使用して認証します。 |

   複数の方法を選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各項目をクリックします。

1. 必要な2FA メソッドごとに[設定](../configuration-reference/security/2fa.md)を完了します。

   ![&#x200B; セキュリティ設定 – 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

   ユーザーが&#x200B;_管理者_&#x200B;に初めてログインする場合は、必要な2FA メソッドをそれぞれ設定する必要があります。 この初期設定の後、ログインするたびに、設定されたメソッドのいずれかを使用して認証する必要があります。

## 2FA プロバイダー設定

必要な2FA方式ごとに設定を行います。

### Google

ログイン時にワンタイムパスワード（OTP）を使用できる時間を変更するには、**[!UICONTROL Use system value]** チェックボックスをオフにします。 次に、**[!UICONTROL OTP Window]**&#x200B;を有効にする秒数を入力します。

![&#x200B; セキュリティ設定 – Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Adobe Commerce 2.4.7以降では、OTP ウィンドウの設定設定により、管理者の有効期限が切れた後に管理者のワンタイムパスワード（OTP）を受け入れる時間（秒単位）が制御されます。 この値は30秒未満である必要があります。 システムの既定の設定は`29`です。<br><br> バージョン 2.4.6では、OTP ウィンドウの設定によって、有効なままの過去および将来のOTP コードの数が決まります。 値`1`は、現在のOTP コードと過去の1つのコードおよび将来の1つのコードが任意の時点で有効であることを示します。

### [!DNL Duo Security]

Duo Security アカウントから次の資格情報を入力します。

- クライアント ID
- クライアント秘密鍵
- 統合キー
- 秘密鍵
- API ホスト名

![&#x200B; セキュリティ設定 – Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. [!DNL Authy] アカウントのAPI キーを入力してください。

1. 認証時に表示されるデフォルトのメッセージを変更するには、**[!UICONTROL Use system value]** チェックボックスをオフにします。 次に、表示する&#x200B;**[!UICONTROL OneTouch Message]**&#x200B;を入力します。

   ![&#x200B; セキュリティ設定 – Authy](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F デバイス （[!DNL Yubikey]およびその他）

認証プロセス中は、ストアドメインがデフォルトで使用されます。 認証の課題にカスタムドメインを使用するには、**[!UICONTROL Use system value]** チェックボックスをオフにします。 次に、**[!UICONTROL WebAPi Challenge Domain]**&#x200B;を入力します。

![&#x200B; セキュリティ設定 – U2F デバイス &#x200B;](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
