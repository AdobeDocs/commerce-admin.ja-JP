---
title: Admin Security の設定
description: ストア管理者のセキュリティを設定する方法について説明します。
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Admin Security の設定

店舗のセキュリティを保護するために、多面的なアプローチを取ることをお勧めします。 推測が容易ではない、明らかな「管理者」や「バックエンド [&#128279;](../stores-purchase/store-urls.md#use-a-custom-admin-url) ではなく、 カスタム管理 URL」を使用して開始することができます。 デフォルトでは、管理者への [ ログイン ](../getting-started/admin-signin.md) に使用するパスワードは 7 文字以上で、文字と数字の両方を含める必要があります。 [ ベストプラクティス ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) として、文字、数字、記号の組み合わせを含む強力な管理者パスワードのみを使用します。 Adobe CommerceおよびMagento Open Sourceでは、アカウントに割り当てられた最後の 4 つのパスワードを再利用することはできません。

Admin セキュリティ設定を使用すると、次の操作を行うことができます。

- URL への秘密鍵の追加
- パスワードでは大文字と小文字を区別する必要があります
- 管理セッションの長さの制限
- パスワードの有効期間を制限する
- 管理者ユーザーアカウントが [ ロック ](permissions-users-all.md#locked-users) されるまで実行できるログイン試行回数を制限します。

セキュリティを強化するために、現在のセッションの有効期限が切れる前にキーボードが非アクティブになる期間を設定し、ユーザー名とパスワードで大文字と小文字を区別するように要求することができます。

この節のセキュリティ設定に加えて、アプリまたはデバイスで生成された 1 回限りのパスワードでユーザーの ID を検証するには、[2 要素認証 ](security-two-factor-authentication.md) （2FA）が必要です。 管理者に初めてログインすると、2FA を設定するよう求められます。 セキュリティを強化するために、[CAPTCHA](security-captcha.md) を必要とするように Admin ログインを設定することもできます。

>[!NOTE]
>
>[!DNL Adobe Identity Management Services] （IMS）認証を有効にしているストアでは、ネイティブのAdobe CommerceおよびMagento Open Source 2FA が無効になっています。 Adobe資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 [[!DNL Adobe Identity Management Service]  （IMS）統合の概要を参照してください ](../getting-started/adobe-ims-integration-overview.md)。

技術情報については、開発者向けドキュメントの [ セキュリティの概要 ](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"} を参照してください。

![ 管理者セキュリティ ](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Admin Security の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL Advanced]_&#x200B;の下の左パネルで、「**[!UICONTROL Admin]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Security]**」セクションを展開します。

1. 管理者ユーザーが異なるデバイスの同じアカウントにログインできないようにするには、**[!UICONTROL Admin Account Sharing]** を `No` に設定します。

1. パスワードリセット要求の管理に使用する方法を決定するには、**[!UICONTROL Password Reset Protection Type]** を次のいずれかに設定します。

   - `By IP and Email`：管理者アカウントに関連付けられたメールアドレスに通知から応答を受信した後に、パスワードをオンラインでリセットできます。
   - `By IP` — パスワードは、追加の確認なしにオンラインでリセットできます。
   - `By Email` — パスワードは、管理者アカウントに関連付けられたメールアドレスに送信される通知にメールで応答することによってのみリセットできます。
   - `None` — パスワードは、ストア管理者のみがリセットできます。

1. ログインセキュリティオプションの設定：

   - **[!UICONTROL Recovery Link Expiration Period (hours)]**: パスワード回復リンクの有効期間を入力します。

   - 1 時間あたりに送信できるパスワード要求の最大数を決定するには、**[!UICONTROL Max Number of Password Reset Requests]** の数を入力します。

   - **[!UICONTROL Min Time Between Password Reset Requests]**: パスワードリセットリクエストの間に経過する必要がある最小分数を入力します。

   - 悪用に対する予防策として秘密鍵を管理 URL に追加するには、**[!UICONTROL Add Secret Key to URLs]** を `Yes` に設定します。 この設定は、デフォルトで有効になっています。

   - 入力するログイン資格情報での大文字と小文字の使用がシステムに保存されている内容と一致することを必須にするには、**[!UICONTROL Login is Case Sensitive]** を `Yes` に設定します。

   - タイムアウトする前の管理者セッションの長さを判断するには、**[!UICONTROL Admin Session Lifetime (seconds)]** のフィールドにセッションの時間（秒）を入力します。 値は 60 秒以上にする必要があります。

   - **[!UICONTROL Maximum Login Failures to Lockout Account]**: アカウントがロックされるまでユーザーが管理者にログインできる回数を入力します。 デフォルトでは、6 回の試行が許可されています。 ログインの試行回数に制限がない場合は、フィールドを空のままにします。

   - **[!UICONTROL Lockout Time (minutes)]**：最大試行回数に達したときに管理者アカウントをロックする時間（分）を入力します。

1. パスワードオプションの設定：

   - 管理者パスワードの有効期間を制限するには、パスワードが有効な日数を入力し **[!UICONTROL Password Lifetime (days)]** す。 無期限の場合は、フィールドを空白のままにします。

   - **[!UICONTROL Password Change]** を次のいずれかに設定します。

      - `Forced` – 管理者ユーザーは、アカウントの設定後にパスワードを変更する必要があります。
      - `Recommended` – 管理者ユーザーに対して、アカウントの設定後にパスワードを変更することを推奨します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 管理者パスワードの要件

デフォルトでは、管理者パスワードは 7 文字以上で、文字と数字の両方を含める必要があります。
