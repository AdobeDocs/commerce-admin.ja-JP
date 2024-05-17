---
title: 管理者ユーザーアカウントの管理
description: 管理者ユーザーアカウントを作成し、役割を割り当てて、管理機能に権限を付与する方法について説明します。
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 0%

---

# 管理者ユーザーアカウントの管理

ストアを初めてインストールすると、完全な管理アクセス権を付与するログイン資格情報を使用して、デフォルトの管理者アカウントが作成されます。 ベストプラクティスとして、完全な管理者アクセス権を持つ別のユーザーアカウントを作成してください。 これにより、1 つのアカウントを日常の管理活動に使用し、もう 1 つを「スーパー管理者」アカウントとして予約できます。 これは、通常の資格情報を忘れた場合や、何らかの理由で使用できなくなった場合に役立ちます。

チームまたはサービスプロバイダーにアクセスを必要とする他のユーザーがいる場合は、それぞれに個別のユーザーアカウントを作成し、ビジネスで必要な知識に基づいて制限付きアクセスを割り当てることができます。 管理者としてユーザーがアクセスできる web サイトやストアを制限するには、以下を行う必要があります [役割の作成](permissions-user-roles.md) （範囲は限られており、必要なリソースのみが選択されている） 次に、その役割を特定のユーザーアカウントに割り当てることができます。 制限付き役割に割り当てられた管理者ユーザーは、その役割に関連付けられた Web サイトまたはストアのデータのみを表示および変更できますが、グローバル設定やデータは変更できません。

>[!NOTE]
>
>Adobe IDを持ち、Adobe CommerceおよびAdobeビジネス製品への効率的なログインを必要とするAdobe Commerce マーチャントは、Commerce認証をAdobe IMS認証ワークフローと統合できます。 この統合がCommerce ストアに対して有効になると、各管理者ユーザーは、Commerce資格情報ではなく、Adobe資格情報を使用してログインする必要があります。 参照： [AdobeIdentity Management サービス（IMS）の統合の概要](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

一時的なユーザーまたは役割の場合は、ユーザーアカウントの有効期限を設定することもできます。

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## ユーザーの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New User]**.

   既存のユーザーを編集するには、グリッド内のユーザー名をクリックします。 を変更できます _[!UICONTROL User Info]_および_[!UICONTROL User Role]_ 必要に応じて、「」を選択します。

1. が含まれる _[!UICONTROL Account Information]_セクションで、次の操作を行います。

   ![ユーザーアカウント情報](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - を入力 **[!UICONTROL User Name]** アカウント用。

     ユーザー名は覚えやすいものにする必要があります。 大文字と小文字は区別されません。 例えば、ユーザー名がの場合 `John`の場合は、としてログインすることもできます。 `john`.

   - 次の情報を入力します。

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     各ユーザーアカウントには、一意のメールアドレスが必要です。

   - を入力 **[!UICONTROL Password]** をアカウントに追加します。

     >[!NOTE]
     >
     >管理者パスワードは 7 文字以上で、文字と数字の両方を含める必要があります。 その他のパスワードオプションについては、を参照してください。 [Admin Security の設定](security-admin.md).

   - の場合 **[!UICONTROL Password Confirmation]**&#x200B;を入力し、パスワードが正しいことを確認します。

   - ストアに複数の言語がある場合は、を設定します **[!UICONTROL Interface Locale]** を管理者インターフェイスに使用される言語に変更します。

1. を設定 **[!UICONTROL This Account is]** 対象： `Active`.

1. カレンダーアイコンをクリックして、 **[!UICONTROL Expiration Date]** をユーザーアカウントとして使用します。

   ユーザーまたは役割が一時的な場合は、有効期限を定義すると役立ちます。 有効期限が切れると、ユーザーアカウントのステータスが「」に変わります `Inactive` 必要に応じて、およびを更新できます。

1. 次の下 _[!UICONTROL Current User Identity Verification]_：ユーザーアカウントのパスワードを入力します。

>[!IMPORTANT]
>
>（を使用） _[!UICONTROL Account Information]_セクション完了、ユーザーを保存できます。 新しいユーザーがに表示されます_[!UICONTROL Users]_ グリッドが使用できますが、ユーザー名は役割が割り当てられるまでログインできません。

## ユーザーの役割の割り当て

1. 左側のパネルで、 **[!UICONTROL User Role]**.

   グリッドには、既存のすべてのユーザーの役割が一覧表示されます。 新しいストアの場合、 _[!UICONTROL Administrators]_は、利用できる唯一の役割です。

   ![Admin - add new user role](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. が含まれる _[!UICONTROL Assigned]_列で、ユーザーの役割を選択します。

   次のことができます [既存のユーザーの役割の表示または追加のユーザーの役割の定義](permissions-user-roles.md). 役割を定義したら、ユーザーアカウントを編集して新しい役割を割り当てる必要があります。

## 2FA プロバイダの検証またはリセット

1. 管理者ユーザーアカウントを開きます。

1. 左側のパネルで、 **[!UICONTROL 2FA]**.

   ![Admin - add new user role](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. が利用できる 2FA ソリューションの検証 _Admin_ ユーザーと、ログイン前に使用するソリューションをインストールするように各ユーザーにアドバイスします。

   へのログインに必要な 2FA ソリューションは 1 つだけです。 _Admin_.

1. ユーザーが 2FA ソリューションを再インストールする必要がある場合は、現在の 2FA 設定をリセットできます。

   この場合、ユーザーは再度ログインする前に、設定プロセスを繰り返す必要があります。 例えば、新しいスマートフォンがあり、Google Authenticator を再インストールする必要がある場合です。 ユーザーの現在の 2FA 設定をクリアするには、以下をクリックします。 **[!UICONTROL Reset (Provider)]** 消去する各ソリューションに対して プロンプトが表示されたら、 **[!UICONTROL OK]** を確認します。

   ユーザーは、へのリンクが記載されたメールを受け取ります。 [2FA の設定](security-two-factor-authentication.md). リンクは 1 回だけ使用できます。 ユーザーが複数回ログインしようとすると、試行のたびに新しいリンクが送信されます。

1. クリック **[!UICONTROL Save User]**.

1. パスワードを入力して ID を確認し、再度 **[!UICONTROL Save User]**.

   この _[!UICONTROL Users]_グリッドが開き、すべてのユーザーが一覧表示されます。

## 管理者ユーザーの削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. グリッドの上にあるフィルターを使用してユーザーアカウントを見つけ、ユーザー名をクリックします。

1. プロンプトが表示されたら、パスワードを入力して ID を確認します。

1. 右上隅のをクリックします。 **[!UICONTROL Delete User]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## パスワードを忘れた場合の E メールのリセット

管理者のメールテンプレート設定は、ユーザーがパスワードを忘れたり、リセットしたりしたときに送信されるメールを決定します。 この構成では、メッセージの送信者として表示されるストアの連絡先と、パスワード回復リンクが有効なままである期間を指定します。

**_管理者 E メールテンプレートを設定するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Admin]**.

1. を展開 ![拡張トグラー](../assets/icon-display-expand.png) この **[!UICONTROL Admin User Emails]** セクション。

   ![詳細設定 – 管理者のメールテンプレート設定](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Forgot Password Email Template]** を管理者ユーザーがパスワードを忘れた場合に送信されるテンプレートに追加します。

1. を設定 **[!UICONTROL Forgot and Reset Email Sender]** メッセージの送信者として表示されるストアの連絡先に送信されます。

1. を設定 **[!UICONTROL User Notification Template]** を管理者通知用のデフォルトとして使用されるメールテンプレートに変更します。

1. 完了したら、 **[!UICONTROL Save Config]**.

## ロックされたユーザー

ビジネスのセキュリティを確保するため、に 6 回失敗すると、デフォルトでユーザーアカウントがロックされます [ログイン](../getting-started/admin-signin.md) を管理者に送信します。 現在ロックされているユーザーアカウントは、すべてロックされたユーザーグリッドに表示されます。 完全な管理者権限を持つ他のユーザーがアカウントをロック解除できます。

追加のパスワードセキュリティ対策は、 [詳細管理者](../configuration-reference/advanced/admin.md#security) 設定。 参照： [Admin Security](security-admin.md).

![ログイン画面アラート – アカウントが一時的に無効になっています](./assets/admin-login-locked-out-message.png){width="300"}

**_管理者アカウントのロックを解除するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. グリッドで、ロックされたアカウントのチェックボックスを選択します。

   ![権限 – ロックされたユーザーアカウント](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. 左上隅にを設定します **[!UICONTROL Actions]** 対象： `Unlock`.

1. クリック **[!UICONTROL Submit]** でアカウントをロック解除します。
