---
title: 管理者セキュリティの設定
description: ストア管理者のセキュリティを設定する方法について説明します。
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: ad01f8aaa40f6bda0fe329a0e906915f6034972f
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# 管理者セキュリティの設定

ストアのセキュリティを保護するために、多面的なアプローチを採用することをお勧めします。 最初に、わかりやすい「管理者」や「バックエンド」ではなく、推測しにくい[&#x200B; カスタム管理者URL](../stores-purchase/store-urls.md#use-a-custom-admin-url)を使用することから始めます。 デフォルトでは、管理者に[&#x200B; ログインするために使用されるパスワードは、7文字以上で、英数字の両方が含まれている必要があります。 &#x200B;](../getting-started/admin-signin.md)組織のニーズに基づいてセキュリティを強化するために、最小パスワード長の要件を設定できます。 [&#x200B; ベストプラクティス &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=ja)として、文字、数字、記号の組み合わせを含む強力な管理者パスワードのみを使用してください。 Adobe CommerceとMagento Open Sourceでは、アカウントに割り当てられた最後の4つのパスワードを再利用できません。

管理者セキュリティ設定では、次の機能を使用できます。

- URLに秘密鍵を追加
- パスワードでは大文字と小文字を区別する
- パスワード長の最小要件の設定
- 管理者セッションの長さを制限する
- パスワードの有効期間を制限
- 管理者ユーザーアカウントが[&#x200B; ロック &#x200B;](permissions-users-all.md#locked-users)される前に実行できるログイン試行回数を制限します。

セキュリティを強化するには、現在のセッションが期限切れになる前にキーボードの非アクティブな長さを設定し、ユーザー名とパスワードを大文字と小文字を区別する必要があります。

このセクションのセキュリティ設定に加えて、アプリまたはデバイスによって生成された1回限りのパスワードでユーザーのIDを確認するには、[二要素認証](security-two-factor-authentication.md) （2FA）が必要です。 管理者に初めてログインしたときに、2FAを設定するように求められます。 セキュリティを強化するために、管理者ログインを設定して[CAPTCHA](security-captcha.md)を必要とすることもできます。

>[!NOTE]
>
>[!DNL Adobe Identity Management Services] （IMS）認証を有効にしているストアでは、ネイティブ Adobe CommerceとMagento Open Source 2FAが無効になっています。 Adobeの資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理者タスクで再認証を行う必要はありません。 認証は、管理者ユーザーが現在のセッションにログインしたときにAdobe IMSによって処理されます。 [[!DNL Adobe Identity Management Service]  （IMS）統合の概要](../getting-started/adobe-ims-integration-overview.md)を参照してください。

技術情報については、開発者用マニュアルの[&#x200B; セキュリティの概要](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"}を参照してください。

![管理者セキュリティ &#x200B;](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## 管理者セキュリティの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL Advanced]_&#x200B;の下の左側のパネルで、**[!UICONTROL Admin]**&#x200B;を選択します。

1. **[!UICONTROL Security]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. 管理者ユーザーが異なるデバイスで同じアカウントからログインできないようにするには、**[!UICONTROL Admin Account Sharing]**&#x200B;を`No`に設定します。

1. パスワード リセット要求の管理に使用する方法を決定するには、**[!UICONTROL Password Reset Protection Type]**&#x200B;を次のいずれかに設定します。

   - `By IP and Email` – 通知から応答を受け取った後、パスワードをオンラインでリセットし、管理者アカウントに関連付けられた電子メールアドレスに送信できます。
   - `By IP` — パスワードは、追加確認なしでオンラインでリセットできます。
   - `By Email` — パスワードは、管理者アカウントに関連付けられた電子メールアドレスに送信される通知に電子メールで応答することによってのみリセットできます。
   - `None` — パスワードは、ストア管理者のみがリセットできます。

1. ログインセキュリティオプションの設定：

   - **[!UICONTROL Recovery Link Expiration Period (hours)]**&#x200B;の場合、パスワード回復リンクが有効な時間数を入力します。

   - 1時間に送信できるパスワード要求の最大数を決定するには、**[!UICONTROL Max Number of Password Reset Requests]**&#x200B;の数を入力します。

   - **[!UICONTROL Min Time Between Password Reset Requests]**&#x200B;について、パスワードのリセット要求の間に通過する必要がある最小分数を入力します。

   - 悪用に対する予防策として管理者URLに秘密鍵を追加するには、**[!UICONTROL Add Secret Key to URLs]**&#x200B;を`Yes`に設定します。 この設定はデフォルトで有効になっています。

   - 入力されたログイン資格情報の大文字と小文字の使用が、システムに保存されている内容と一致することを要求するには、**[!UICONTROL Login is Case Sensitive]**&#x200B;を`Yes`に設定します。

   - タイムアウトする前に管理者セッションの長さを決定するには、**[!UICONTROL Admin Session Lifetime (seconds)]** フィールドにセッションの期間を秒単位で入力します。 値は60秒以上にする必要があります。

   - **[!UICONTROL Maximum Login Failures to Lockout Account]**&#x200B;の場合、ユーザーがアカウントをロックする前に管理者にログインできる回数を入力します。 デフォルトでは、6回の試行が許可されています。 無制限のログイン試行の場合は、フィールドを空のままにします。

   - **[!UICONTROL Lockout Time (minutes)]**&#x200B;について、最大試行回数に達したときに管理者アカウントがロックされる分数を入力します。

1. パスワードのオプションを設定：

   - **[!UICONTROL Minimum Admin Password Length]**&#x200B;に、管理者パスワードに必要な最小文字数を入力します。 デフォルト値は7で、最小値は7です。

     >[!WARNING]
     >
     >この値をデフォルトから変更すると、既存のサービスとの下位互換性の問題が発生する可能性があります。 この設定は、管理者パスワードの変更、管理者インターフェイスとCLIの両方からの新しい管理者ユーザーの作成、および管理者からのパスワードリセット操作に影響します。

   - 管理者パスワードの有効期間を制限するには、パスワードが&#x200B;**[!UICONTROL Password Lifetime (days)]**&#x200B;に有効な日数を入力します。 無制限のライフタイムの場合は、フィールドを空白のままにします。

   - **[!UICONTROL Password Change]**&#x200B;を次のいずれかに設定します：

      - `Forced` – 管理者ユーザーがアカウントの設定後にパスワードを変更する必要があります。
      - `Recommended` – 管理者ユーザーがアカウントの設定後にパスワードを変更することをお勧めします。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## 管理者パスワードの要件

デフォルトでは、管理者パスワードは7文字以上で、文字と数字の両方が含まれている必要があります。 **[!UICONTROL Minimum Admin Password Length]**&#x200B;設定を使用して、組織のセキュリティ基準を満たすためにパスワードの長さの最小要件を設定できます。 ただし、この値を大きくすると、既存のサービスや統合との互換性に影響を与える可能性があります。
