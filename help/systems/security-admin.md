---
title: Admin Security の設定
description: ストア管理者のセキュリティを設定する方法について説明します。
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Admin Security の設定

店舗のセキュリティを保護するために、多面的なアプローチを取ることをお勧めします。 を使用して開始できます [カスタム管理 URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) これは、明白な「管理者」や「バックエンド」というよりも、推測が容易ではありません。 デフォルトでは、次の目的で使用されるパスワード [ログイン](../getting-started/admin-signin.md) 管理者には、文字と数字の両方を含む 7 文字以上の長さにする必要があります。 As a [ベストプラクティス](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)は、文字、数字、記号の組み合わせを含む強力な管理者パスワードのみを使用してください。 Adobe CommerceとMagento Open Sourceでは、アカウントに割り当てられた最後の 4 つのパスワードを再利用することはできません。

Admin セキュリティ設定を使用すると、次の操作を行うことができます。

- URL への秘密鍵の追加
- パスワードでは大文字と小文字を区別する必要があります
- 管理セッションの長さの制限
- パスワードの有効期間を制限する
- 管理者ユーザーアカウントが次の値になるまで、ログインを試行できる回数を制限します [locked](permissions-users-all.md#locked-users).

セキュリティを強化するために、現在のセッションの有効期限が切れる前にキーボードが非アクティブになる期間を設定し、ユーザー名とパスワードで大文字と小文字を区別するように要求することができます。

このセクションのセキュリティ設定に加えて、 [二要素認証](security-two-factor-authentication.md) （2FA）は、アプリまたはデバイスで生成された 1 回限りのパスワードでユーザーの ID を検証するために必要です。 管理者に初めてログインすると、2FA を設定するよう求められます。 セキュリティを強化するために、を必要とするように Admin ログインを設定することもできます [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>が有効になっているストア [!DNL Adobe Identity Management Services] （IMS）認証では、ネイティブのAdobe CommerceとMagento Open Source 2FA が無効になっています。 Adobe資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 参照： [[!DNL Adobe Identity Management Service] （IMS）統合の概要](../getting-started/adobe-ims-integration-overview.md).

技術情報については、を参照してください [セキュリティの概要](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} を参照してください。

![Admin security](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Admin Security の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL Advanced]_、を選択&#x200B;**[!UICONTROL Admin]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Security]** セクション。

1. 管理者ユーザーが異なるデバイスの同じアカウントにログインできないようにするには、次のように設定します **[!UICONTROL Admin Account Sharing]** 対象： `No`.

1. パスワードリセットリクエストの管理に使用する方法を決定するには、を設定します **[!UICONTROL Password Reset Protection Type]** を次のいずれかに変更します。

   - `By IP and Email` — パスワードは、管理者アカウントに関連付けられたメールアドレスに通知から応答を受信した後に、オンラインでリセットできます。
   - `By IP` — パスワードは、追加の確認なしにオンラインでリセットできます。
   - `By Email` — パスワードは、管理者アカウントに関連付けられた電子メール アドレスに送信される通知に電子メールで応答することによってのみリセットできます。
   - `None` — パスワードは、ストア管理者のみがリセットできます。

1. ログインセキュリティオプションの設定：

   - の場合 **[!UICONTROL Recovery Link Expiration Period (hours)]**：パスワード回復リンクの有効期間を入力します。

   - 1 時間あたりに送信できるパスワード要求の最大数を決定するには、次の数を入力します **[!UICONTROL Max Number of Password Reset Requests]**.

   - の場合 **[!UICONTROL Min Time Between Password Reset Requests]**&#x200B;を入力し、パスワードリセットリクエストの間に経過する必要がある最小分数を入力します。

   - 悪用に対する予防策として秘密鍵を管理 URL に追加するには、を設定します **[!UICONTROL Add Secret Key to URLs]** 対象： `Yes`. この設定は、デフォルトで有効になっています。

   - 入力するログイン資格情報での大文字と小文字の使用がシステムに保存されている内容と一致することを必須にするには、を設定します **[!UICONTROL Login is Case Sensitive]** 対象： `Yes`.

   - タイムアウトする前の管理者セッションの長さを判断するには、次の単位でセッションの時間（秒単位）を入力します **[!UICONTROL Admin Session Lifetime (seconds)]** フィールド。 値は 60 秒以上にする必要があります。

   - の場合 **[!UICONTROL Maximum Login Failures to Lockout Account]**：アカウントがロックされるまでユーザーが管理者にログインできる回数を入力します。 デフォルトでは、6 回の試行が許可されています。 ログインの試行回数に制限がない場合は、フィールドを空のままにします。

   - の場合 **[!UICONTROL Lockout Time (minutes)]**、最大試行回数に達したときに管理者アカウントをロックする時間（分）を入力します。

1. パスワードオプションの設定：

   - 管理者パスワードの有効期間を制限するには、パスワードの有効期間を入力してください **[!UICONTROL Password Lifetime (days)]**. 無期限の場合は、フィールドを空白のままにします。

   - を設定 **[!UICONTROL Password Change]** を次のいずれかに変更します。

      - `Forced`  – 管理者ユーザーが、アカウントの設定後にパスワードを変更する必要があります。
      - `Recommended`  – 管理者ユーザーに対して、アカウントの設定後にパスワードを変更することを推奨します。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 管理者パスワードの要件

デフォルトでは、管理者パスワードは 7 文字以上で、文字と数字の両方を含める必要があります。
