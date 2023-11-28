---
title: 管理者ユーザーアカウントを管理
description: 管理者ユーザーアカウントを作成し、役割を割り当てて管理者機能に権限を付与する方法について説明します。
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# 管理者ユーザーアカウントを管理

ストアを初めてインストールすると、完全な管理アクセス権を付与するログイン資格情報を使用して、デフォルトの管理者アカウントが作成されます。 ベストプラクティスとして、完全な管理者アクセス権を持つ別のユーザーアカウントを作成する必要があります。 これにより、1 つのアカウントを毎日の管理活動に使用し、もう 1 つを「スーパー管理者」アカウントとして予約できます。 これは、通常の資格情報を忘れた場合や、何らかの方法で使用できなくなった場合に役立ちます。

チームやサービスプロバイダーにアクセス権を必要とする人がいる場合は、それぞれに対して個別のユーザーアカウントを作成し、ビジネス上のニーズに応じて制限付きアクセスを割り当てることができます。 管理者でユーザーがアクセスできる Web サイトやストアを制限するには、まず [役割を作成する](permissions-user-roles.md) 範囲が限られ、必要なリソースのみが選択されている場合。 その後、その役割を特定のユーザーアカウントに割り当てることができます。 制限された役割に割り当てられた管理者ユーザーは、その役割に関連付けられた Web サイトまたはストアのデータのみを表示および変更できますが、グローバル設定やデータは変更できません。

>[!NOTE]
>
>Adobe IDをお持ちで、Adobe CommerceおよびAdobeビジネス製品への効率的なログインを必要とするAdobe Commerceの商人は、コマース認証をAdobe IMS認証ワークフローと統合できます。 この統合をコマースストアで有効にした後、各管理者ユーザーは、（コマースの資格情報ではなく）Adobeの資格情報を使用してログインする必要があります。 詳しくは、 [AdobeIdentity Managementサービス (IMS) 統合の概要](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

一時的なユーザーまたはロールの場合は、ユーザーアカウントの有効期限を設定することもできます。

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## ユーザーの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. 右上隅で、 **[!UICONTROL Add New User]**.

   既存のユーザーを編集するには、グリッド内のユーザー名をクリックします。 次の項目を変更できます。 _[!UICONTROL User Info]_および_[!UICONTROL User Role]_ セクションを必要に応じて変更します。

1. Adobe Analytics の _[!UICONTROL Account Information]_セクションで、以下の操作を実行します。

   ![ユーザーアカウント情報](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - 次を入力します。 **[!UICONTROL User Name]** を設定します。

     ユーザー名は覚えやすい名前にする必要があります。 大文字と小文字は区別されません。 例えば、ユーザー名が `John`また、 `john`.

   - 次の情報を入力します。

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     各ユーザーアカウントには、一意の電子メールアドレスが必要です。

   - を入力します。 **[!UICONTROL Password]** アカウントの。

     >[!NOTE]
     >
     >管理者パスワードは 7 文字以上で、文字と数字の両方を含める必要があります。 その他のパスワードオプションについては、 [管理セキュリティの設定](security-admin.md).

   - の場合 **[!UICONTROL Password Confirmation]**」に入力し直し、パスワードが正しく入力されたことを確認します。

   - ストアに複数の言語が含まれる場合は、 **[!UICONTROL Interface Locale]** を管理インターフェイスで使用する言語に変更します。

1. 設定 **[!UICONTROL This Account is]** から `Active`.

1. カレンダーアイコンをクリックして、 **[!UICONTROL Expiration Date]** ユーザーアカウントに適用されます。

   有効期限の定義は、ユーザーまたは役割が一時的な場合に役立ちます。 有効期限後、ユーザーアカウントのステータスは「 `Inactive` 必要に応じて、およびを更新できます。

1. の下 _[!UICONTROL Current User Identity Verification]_」に、ユーザーアカウントのパスワードを入力します。

>[!IMPORTANT]
>
>を使用 _[!UICONTROL Account Information]_セクションが完了したら、ユーザーを保存できます。 新しいユーザーが_[!UICONTROL Users]_ グリッドに表示されますが、役割が割り当てられるまで、ユーザー名はログインできません。

## ユーザーロールの割り当て

1. 左側のパネルで、 **[!UICONTROL User Role]**.

   グリッドには、既存のすべてのユーザーの役割が表示されます。 新しいストアの場合、 _[!UICONTROL Administrators]_は、使用できる唯一の役割です。

   ![管理者 — 新しいユーザーロールを追加](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. Adobe Analytics の _[!UICONTROL Assigned]_列で、ユーザーの役割を選択します。

   以下が可能です。 [既存のユーザーロールを表示または追加のユーザーロールを定義します](permissions-user-roles.md). ロールを定義したら、新しいロールを割り当てるために、ユーザーアカウントを編集する必要があります。

## 2FA プロバイダーを確認またはリセット

1. Admin ユーザーアカウントを開きます。

1. 左側のパネルで、 **[!UICONTROL 2FA]**.

   ![管理者 — 新しいユーザーロールを追加](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. 使用可能な 2FA ソリューションを検証します。 _管理者_ ユーザーに問い合わせ、使用するソリューションをインストールしてからログインするよう各ユーザーに勧めます。

   にログインするには、1 つの 2FA ソリューションによる認証のみが必要です _管理者_.

1. ユーザが 2FA ソリューションを再インストールする必要がある場合は、現在の 2FA 設定をリセットできます。

   この場合、ユーザーは再度サインインする前に、設定プロセスを繰り返す必要があります。 例えば、ユーザーが新しいスマートフォンを使用していて、Google Authenticator を再インストールする必要がある場合があります。 ユーザの現在の 2FA 設定をクリアするには、 **[!UICONTROL Reset (Provider)]** クリアする各ソリューションに対して プロンプトが表示されたら、「 **[!UICONTROL OK]** をクリックして確定します。

   ユーザーが、 [2FA を設定](security-two-factor-authentication.md). リンクは 1 回だけ使用できます。 ユーザーが複数回サインインしようとした場合は、毎回新しいリンクが送信されます。

1. クリック **[!UICONTROL Save User]**.

1. ID を確認するためのパスワードを入力するよう求められたら、再度「 」をクリックします。 **[!UICONTROL Save User]**.

   The _[!UICONTROL Users]_グリッドが開き、すべてのユーザーが表示されます。

## 管理者ユーザーの削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. グリッドの上のフィルターを使用してユーザーアカウントを探し、ユーザー名をクリックします。

1. プロンプトが表示されたら、ID を確認するためのパスワードを入力します。

1. 右上隅で、 **[!UICONTROL Delete User]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## パスワードを忘れた場合とメールをリセットしてください

管理者電子メールテンプレートの設定では、ユーザーがパスワードを忘れてリセットした場合に送信する電子メールを指定します。 この設定は、メッセージの送信者として表示されるストアの連絡先と、パスワード回復リンクが有効である期間を指定します。

**_管理者の電子メールテンプレートを設定するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Admin]**.

1. 展開 ![拡張トグラー](../assets/icon-display-expand.png) の **[!UICONTROL Admin User Emails]** 」セクションに入力します。

   ![詳細設定 — 管理者の電子メールテンプレート設定](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Forgot Password Email Template]** 管理者ユーザーがパスワードを忘れたときに送信されるテンプレートに追加します。

1. 設定 **[!UICONTROL Forgot and Reset Email Sender]** メッセージの送信者として表示されるストア連絡先に追加します。

1. 設定 **[!UICONTROL User Notification Template]** 管理者通知のデフォルトとして使用される電子メールテンプレートに追加します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## ロックされたユーザー

ビジネスのセキュリティ上、ユーザーアカウントは、 [ログイン](../getting-started/admin-signin.md) 管理者に問い合わせます。 現在ロックされているユーザーアカウントは、「ロック済みユーザー」グリッドに表示されます。 アカウントは、完全な管理者権限を持つ他のユーザーによってロック解除できます。

追加のパスワードセキュリティ対策は、 [詳細管理](../configuration-reference/advanced/admin.md#security) 設定。 詳しくは、 [管理セキュリティ](security-admin.md).

![ログイン画面の警告 — アカウントが一時的に無効になっています](./assets/admin-login-locked-out-message.png){width="300"}

**_管理者アカウントのロックを解除するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. グリッドで、ロックされたアカウントのチェックボックスを選択します。

   ![権限 — ロックされたユーザーアカウント](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. 左上隅で、 **[!UICONTROL Actions]** から `Unlock`.

1. クリック **[!UICONTROL Submit]** をクリックして、アカウントをロック解除します。
