---
title: セッション管理
description: 管理者とストアフロントを保護するためにセッション管理を設定する方法について説明します。
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# セッション管理

[ セッション管理 ](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) は、API セキュリティのサービス拒否（DoS）に対するベストプラクティスです。 セッションは、訪問者がサイトに滞在した時間を表し、管理者ユーザーまたは顧客がアカウントにログインしている時間とは関係ありません。

セッションは、同じユーザーに関連付けられたネットワーク HTTP 要求および応答トランザクションのシーケンスです。 これは、クライアント（管理者）がサーバーにアクセスする際に、そのクライアントのデータに関連付けるための方法です。 セッションは、アクセス権やローカライゼーション設定などの変数を確立するために使用されます。これらの変数は、セッション中にユーザーが web アプリケーションを使用して行うすべてのインタラクションに適用されます。

## セッションサイズ

管理者ユーザーとストアフロント訪問者の最大セッションサイズを制限するには、以下の設定を使用します。

- **[!UICONTROL Max Session Size in Admin]** - セッションの最大サイズをバイト単位で制限します。 `0` を使用して無効にします。
- **[!UICONTROL Max Session Size in Storefront]** - セッションの最大サイズをバイト単位で制限します。 `0` を使用して無効にします。

>[!TIP]
>
>どちらの設定もバイト単位で測定され、デフォルトでは `256000` バイト（256 KB）に設定されます。

**_最大セッションサイズを設定するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」 **[!UICONTROL Security]** クションを展開して、セッション設定にアクセスします。

   ![ セッション設定 ](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. 新しいセッションのサイズをバイト単位で入力します。

   >[!WARNING]
   >
   >値の設定が低すぎると、問題が発生する可能性があります。 デフォルトの 256000 バイト以下のオプションのいずれかを設定すると、警告メッセージが表示されます。 「**[!UICONTROL No]**」をクリックすると、システムによって値が `256000` に変更されます。

1. 「**[!UICONTROL Save Config]**」をクリックします。

### 管理セッション

最大セッションサイズを超えると、エラーメッセージが表示され、セッションサイズの制約が `var/log` ディレクトリに記録されます。

セッションサイズを低く設定しすぎると管理者にアクセスできなくなる場合は、CLI を使用して設定をリセットします。

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### ストアフロントセッション

最大セッションサイズを超えると、エラーは表示されませんが、セッションサイズの制約が `var/log` ディレクトリに記録されます。

## セッションの検証

Adobe CommerceとMagento Open Sourceでは、セッション固定攻撃の可能性や、ユーザーセッションに対する毒物の使用またはハイジャックの試みに対する防御手段として、セッション変数を検証できます。 セッション検証設定は、各ストア訪問の間にセッション変数を検証する方法、およびセッション ID がストアの URL に含まれるかどうかを決定します。

技術情報については、_設定ガイド_ の [ セッションストレージに Redis を使用する ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html?lang=ja) を参照してください。

![ 一般設定 – Web セッションの検証 ](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

検証では、検証変数の値とユーザーのデータに保存されているセッションデータを比較することで、訪問者が言った通りの `$_SESSION` であるかを確認します。 情報が期待どおりに送信されず、対応する変数が空の場合、検証は失敗します。 セッション検証設定に応じて、セッション変数が検証プロセスに失敗した場合、クライアントセッションは直ちに終了します。

すべての検証変数を有効にすると攻撃を防ぐのに役立ちますが、サーバーのパフォーマンスにも影響を与える可能性があります。 デフォルトでは、セッション変数の検証はすべて無効になっています。 設定を試して、Adobe CommerceまたはMagento Open Sourceのインストールに最適な組み合わせを見つけることをお勧めします。 すべての検証変数をアクティブ化すると、制限が過度に厳しくなる可能性があり、プロキシサーバーを通過するインターネット接続や、ファイアウォールの内側から発生するインターネット接続を持つ顧客へのアクセスが妨げられる可能性があります。 セッション変数とその使用方法について詳しくは、Linux® システムのシステム管理ドキュメントを参照してください。

**_セッション検証を設定するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「_[!UICONTROL General]_」を展開し、「**[!UICONTROL Web]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Session Validation Settings]**」セクションを展開します。

1. 各設定オプションを設定します。

   - **[!UICONTROL Validate REMOTE_ADDR]** — リクエストの IP アドレスが `$_SESSION` 変数に格納されている IP アドレスと一致することを確認するには、`Yes` に設定します。

   - **[!UICONTROL Validate HTTP_VIA]** – 受信リクエストのプロキシ アドレスが `$_SESSION` 変数に格納されているアドレスと一致することを検証するには、`Yes` に設定します。

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — リクエストの転送先アドレスが `$_SESSION` 変数に格納されているアドレスと一致することを検証するには、`Yes` に設定します。

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — セッション中にストアにアクセスするために使用されるブラウザまたはデバイスが、`$_SESSION` 変数に格納されている値と一致することを確認するには、`Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 管理セッションの有効期間

セキュリティ対策として、_管理者_ は、最初、キーボードが無操作状態になった 900 秒（15 分）が経過するとタイムアウトするように設定されています。 作業スタイルに合わせて、セッションの有効期間を調整できます。

**_管理者セッションの有効期間を調整するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 下にスクロールして、左側のパネルの **[!UICONTROL Advanced]** を展開します。

1. 「**[!UICONTROL Admin]**」をクリックします。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Security]**」セクションを展開します。

1. **[!UICONTROL Admin Session Lifetime (seconds)]** に、セッションがタイムアウトするまでアクティブなままである秒数を入力します。

   ![ 詳細設定 – Admin security settings](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
