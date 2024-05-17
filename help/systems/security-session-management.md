---
title: セッション管理
description: 管理者とストアフロントを保護するためにセッション管理を設定する方法について説明します。
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# セッション管理

[セッション管理](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) は、API セキュリティのサービス拒否（DoS）対策のベストプラクティスです。 セッションは、訪問者がサイトに滞在した時間を表し、管理者ユーザーまたは顧客がアカウントにログインしている時間とは関係ありません。

セッションは、同じユーザーに関連付けられたネットワーク HTTP 要求および応答トランザクションのシーケンスです。 これは、クライアント（管理者）がサーバーにアクセスする際に、そのクライアントのデータに関連付けるための方法です。 セッションは、アクセス権やローカライゼーション設定などの変数を確立するために使用されます。これらの変数は、セッション中にユーザーが web アプリケーションを使用して行うすべてのインタラクションに適用されます。

## セッションサイズ

管理者ユーザーとストアフロント訪問者の最大セッションサイズを制限するには、以下の設定を使用します。

- **[!UICONTROL Max Session Size in Admin]** – セッションの最大サイズをバイト単位で制限します。 使用方法 `0` を無効にします。
- **[!UICONTROL Max Session Size in Storefront]** – セッションの最大サイズをバイト単位で制限します。 使用方法 `0` を無効にします。

>[!TIP]
>
>どちらの設定もバイト単位で測定され、デフォルトではです。 `256000` バイト （256 KB）。

**_最大セッションサイズを設定するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Security]** セクションに移動して、セッション設定にアクセスします。

   ![セッション設定](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. 新しいセッションのサイズをバイト単位で入力します。

   >[!WARNING]
   >
   >値の設定が低すぎると、問題が発生する可能性があります。 デフォルトの 256000 バイト以下のオプションのいずれかを設定すると、警告メッセージが表示されます。 クリックした場合 **[!UICONTROL No]**&#x200B;の場合、システムによって値がに変更されます `256000`.

1. クリック **[!UICONTROL Save Config]**.

### 管理セッション

最大セッションサイズを超えると、エラーメッセージが表示され、セッションサイズの制約がに記録されます。 `var/log` ディレクトリ。

セッションサイズを低く設定しすぎると管理者にアクセスできなくなる場合は、CLI を使用して設定をリセットします。

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### ストアフロントセッション

最大セッションサイズを超えると、エラーは表示されませんが、セッションサイズの制約がに記録されます。 `var/log` ディレクトリ。

## セッションの検証

Adobe CommerceとMagento Open Sourceを使用すると、セッションの固定攻撃の可能性や、ユーザーセッションの毒物またはハイジャックを試みることに対する防御手段として、セッション変数を検証できます。 セッション検証設定は、各ストア訪問の間にセッション変数を検証する方法、およびセッション ID がストアの URL に含まれるかどうかを決定します。

技術情報については、を参照してください [セッションストレージに Redis を使用](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) が含まれる _設定ガイド_.

![一般設定 – Web セッションの検証](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

検証では、検証変数の値がに保存されているセッションデータと比較されることで、訪問者が言った通りであるかを確認します。 `$_SESSION` ユーザーのデータ。 情報が期待どおりに送信されず、対応する変数が空の場合、検証は失敗します。 セッション検証設定に応じて、セッション変数が検証プロセスに失敗した場合、クライアントセッションは直ちに終了します。

すべての検証変数を有効にすると攻撃を防ぐのに役立ちますが、サーバーのパフォーマンスにも影響を与える可能性があります。 デフォルトでは、セッション変数の検証はすべて無効になっています。 設定を試して、Adobe CommerceまたはMagento Open Sourceのインストールに最適な組み合わせを見つけることをお勧めします。 すべての検証変数をアクティブ化すると、制限が過度に厳しくなる可能性があり、プロキシサーバーを通過するインターネット接続や、ファイアウォールの内側から発生するインターネット接続を持つ顧客へのアクセスが妨げられる可能性があります。 セッション変数とその使用方法について詳しくは、Linux® システムのシステム管理ドキュメントを参照してください。

**_セッション検証を設定するには：_**

1. 日 _Admin_ サイドバー、に移動  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します _[!UICONTROL General]_を選択します&#x200B;**[!UICONTROL Web]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Session Validation Settings]** セクション。

1. 各設定オプションを設定します。

   - **[!UICONTROL Validate REMOTE_ADDR]**  – に設定 `Yes` リクエストの IP アドレスが、に格納されている内容と一致することを確認するには `$_SESSION` 変数。

   - **[!UICONTROL Validate HTTP_VIA]**  – に設定 `Yes` 受信リクエストのプロキシアドレスが、に保存されているアドレスと一致することを確認するには `$_SESSION` 変数。

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]**  – に設定 `Yes` リクエストの転送先アドレスが、に格納されているアドレスと一致することを確認するには `$_SESSION` 変数。

   - **[!UICONTROL Validate HTTP_USER_AGENT]**  – に設定 `Yes` セッション中にストアにアクセスするために使用されるブラウザーまたはデバイスが、に格納されているものと一致することを確認するには `$_SESSION` 変数。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 管理セッションの有効期間

セキュリティ対策として、 _Admin_ は、キーボードが無操作状態になってから 900 秒（15 分）が経過するとタイムアウトするように最初に設定されます。 作業スタイルに合わせて、セッションの有効期間を調整できます。

**_管理者セッションの有効期間を調整するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 下にスクロールして展開 **[!UICONTROL Advanced]** 左側のパネルで。

1. クリック **[!UICONTROL Admin]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Security]_セクション。

1. の場合 **[!UICONTROL Admin Session Lifetime (seconds)]**、セッションがタイムアウトするまでアクティブなままである秒数を入力します。

   ![詳細設定 – Admin security settings](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.##管理者セッションの有効期間

セキュリティ対策として、 _Admin_ は、キーボードが無操作状態になってから 900 秒（15 分）が経過するとタイムアウトするように最初に設定されます。 作業スタイルに合わせて、セッションの有効期間を調整できます。

**_管理者セッションの有効期間を調整するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 下にスクロールして展開 **[!UICONTROL Advanced]** 左側のパネルで。

1. クリック **[!UICONTROL Admin]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _セキュリティ_ セクション。

1. の場合 **[!UICONTROL Admin Session Lifetime (seconds)]**、セッションがタイムアウトするまでアクティブなままである秒数を入力します。

   ![詳細設定 – Admin security settings](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.
