---
title: 管理者セキュリティの設定
description: ストア管理者のセキュリティを設定する方法を説明します。
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# 管理者セキュリティの設定

ストアのセキュリティを保護するために、多面的なアプローチを取ることをお勧めします。 まず、 [カスタム管理 URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) これは、明らかな「管理者」や「バックエンド」というよりは、推測が容易ではありません。 デフォルトでは、 [ログイン](../getting-started/admin-signin.md) を管理者に渡すには、7 文字以上で、文字と数字の両方を含める必要があります。 As a [ベストプラクティス](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)では、文字、数字、記号の組み合わせを含む堅牢な管理者パスワードのみを使用します。 Adobe CommerceとMagento Open Sourceは、アカウントに割り当てられた最後の 4 つのパスワードを再利用できません。

管理セキュリティ設定では、次の操作を実行できます。

- URL への秘密鍵の追加
- パスワードで大文字と小文字を区別する必要があります
- 管理セッションの長さを制限
- パスワードの有効期間を制限
- Admin ユーザーアカウントが有効になるまでに実行できるログイン試行回数を制限します [ロック済み](permissions-users-all.md#locked-users).

セキュリティを強化するために、現在のセッションが期限切れになるまでのキーボードの操作不能時間を設定し、ユーザー名とパスワードで大文字と小文字を区別するように設定できます。

この節のセキュリティ設定に加えて、 [二段階認証](security-two-factor-authentication.md) (2FA) は、アプリまたはデバイスで生成される 1 回限りのパスワードを使用してユーザーの ID を検証するために必要です。 初めて管理者にログインする際に、2FA を設定するよう求められます。 セキュリティを強化するために、管理者ログインを [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>を有効にしたストア [!DNL Adobe Identity Management Services] (IMS) 認証では、ネイティブのAdobe CommerceとMagento Open Source2FA が無効になっています。 コマースインスタンスにログインしている管理者Adobeは、多くの管理者タスクを再認証する必要はありません。 認証は、管理者Adobe IMSが現在のセッションにログインする際にユーザーによって処理されます。 詳しくは、 [[!DNL Adobe Identity Management Service] (IMS) 統合の概要](../getting-started/adobe-ims-integration-overview.md).

技術情報については、 [セキュリティの概要](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;}（開発者向けドキュメント）。

![管理セキュリティ](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## 管理者セキュリティの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL Advanced]_を選択します。**[!UICONTROL Admin]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Security]** 」セクションに入力します。

1. 管理者ユーザーが異なるデバイスで同じアカウントからログインするのを防ぐには、 **[!UICONTROL Admin Account Sharing]** から `No`.

1. パスワードリセット要求の管理に使用する方法を決定するには、 **[!UICONTROL Password Reset Protection Type]** を次のいずれかに変更します。

   - `By IP and Email`  — パスワードは、通知からの応答を Admin アカウントに関連付けられた電子メールアドレスに送信した後に、オンラインでリセットできます。
   - `By IP`  — パスワードは、追加の確認なしでオンラインでリセットできます。
   - `By Email`  — パスワードは、Admin アカウントに関連付けられた電子メールアドレスに送信される通知に電子メールで応答することによってのみ、リセットできます。
   - `None`  — パスワードは、ストア管理者のみがリセットできます。

1. ログインセキュリティオプションを設定します。

   - の場合 **[!UICONTROL Recovery Link Expiration Period (hours)]**&#x200B;に設定した場合は、パスワード回復リンクが有効である時間数を入力します。

   - 1 時間に送信できるパスワード要求の最大数を決定するには、次の数を入力します： **[!UICONTROL Max Number of Password Reset Requests]**.

   - の場合 **[!UICONTROL Min Time Between Password Reset Requests]**」に値を入力する場合は、パスワードリセット要求の間隔の最小値を分単位で入力します。

   - 悪用に対する予防策として秘密鍵を管理 URL に追加するには、 **[!UICONTROL Add Secret Key to URLs]** から `Yes`. この設定は、デフォルトで有効になっています。

   - 入力されたログイン資格情報での大文字と小文字の使用が、システムに保存されているものと一致するようにするには、 **[!UICONTROL Login is Case Sensitive]** から `Yes`.

   - タイムアウト前の管理者セッションの長さを判断するには、セッションの期間を秒単位で入力します。 **[!UICONTROL Admin Session Lifetime (seconds)]** フィールドに入力します。 値は 60 秒以上にする必要があります。

   - の場合 **[!UICONTROL Maximum Login Failures to Lockout Account]**」には、ユーザーがアカウントがロックされる前に Admin へのログインを試行できる回数を入力します。 デフォルトでは、6 回の試行が許可されます。 ログイン試行を無制限におこなう場合は、このフィールドを空のままにします。

   - の場合 **[!UICONTROL Lockout Time (minutes)]**&#x200B;を使用する場合は、最大試行回数に達したときに管理者アカウントがロックされる時間（分）を入力します。

1. パスワードオプションを設定：

   - 管理者パスワードの有効期間を制限するには、パスワードが有効な日数を入力します。 **[!UICONTROL Password Lifetime (days)]**. 無制限の有効期間は、「 」フィールドを空白のままにします。

   - 設定 **[!UICONTROL Password Change]** を次のいずれかに変更します。

      - `Forced`  — 管理者ユーザーは、アカウント設定後にパスワードを変更する必要があります。
      - `Recommended`  — 管理者ユーザーは、アカウント設定後にパスワードを変更することをお勧めします。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 管理者パスワードの要件

デフォルトでは、管理者パスワードは 7 文字以上で、文字と数字の両方を含める必要があります。
