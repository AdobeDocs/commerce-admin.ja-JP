---
title: セッション管理
description: セッション管理を設定して管理者とストアフロントを保護する方法について説明します。
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# セッション管理

[セッション管理](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) は、API セキュリティのためのサービス拒否 (DoS) 対策のベストプラクティスです。 セッションとは、訪問者がサイトに滞在した時間を表し、管理者ユーザーや顧客が自分のアカウントにログインした時間とは関係ありません。

セッションとは、同じユーザーに関連付けられた一連のネットワーク HTTP リクエストと応答トランザクションです。 これは、クライアント（管理者）がサーバーにアクセスする際にデータを関連付ける方法です。 セッションは、セッション中にユーザーが Web アプリケーションとやり取りするたびに適用される、アクセス権やローカリゼーション設定などの変数を確立するために使用されます。

## セッションサイズ

管理者ユーザーとストアフロント訪問者の最大セッションサイズを制限するには、次の設定を使用します。

- **[!UICONTROL Max Session Size in Admin]** — 最大セッション・サイズをバイト単位で制限します。 用途 `0` を無効にします。
- **[!UICONTROL Max Session Size in Storefront]** — 最大セッション・サイズをバイト単位で制限します。 用途 `0` を無効にします。

>[!TIP]
>
>両方の設定はバイト単位で測定され、デフォルトでは次のようになります。 `256000` バイト（または 256 KB）。

**_最大セッションサイズを設定するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Security]** セクションを開いて、セッション設定にアクセスします。

   ![セッション設定](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. 新しいセッション・サイズをバイト単位で入力します。

   >[!WARNING]
   >
   >値を小さく設定すると、問題が発生する場合があります。 デフォルトの256000バイト以下のいずれかのオプションを設定すると、警告メッセージが表示されます。 次をクリックした場合： **[!UICONTROL No]**&#x200B;の場合、値は次の値に変更されます。 `256000`.

1. クリック **[!UICONTROL Save Config]**.

### 管理セッション

最大セッションサイズを超えた場合は、エラーメッセージが表示され、セッションサイズの制約がに記録されます。 `var/log` ディレクトリ。

セッションサイズを小さく設定した後に管理者へのアクセス権が失われた場合は、CLI を使用して設定をリセットします。

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### ストアフロントセッション

最大セッションサイズを超えた場合、エラーは表示されませんが、システムはセッションサイズの制約をに記録します。 `var/log` ディレクトリ。

## セッションの検証

Adobe CommerceとMagento Open Sourceを使用すると、セッション固定攻撃や、ユーザーセッションの毒殺またはハイジャックの試みに対する保護措置として、セッション変数を検証できます。 セッション検証設定は、各ストア訪問中のセッション変数の検証方法と、セッション ID がストアの URL に含まれているかどうかを決定します。

技術情報については、 [セッションストレージに Redis を使用](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) （内） _設定ガイド_.

![一般設定 — Web セッションの検証](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

検証では、検証変数の値と、に保存されているセッションデータを比較することで、訪問者が正しいと見なしているかを確認します。 `$_SESSION` ユーザーのデータ。 情報が期待どおりに送信されず、対応する変数が空の場合、検証は失敗します。 セッションの検証設定に応じて、セッション変数が検証プロセスに失敗した場合、クライアントセッションは直ちに終了します。

すべての検証変数を有効にすると、攻撃を防ぐのに役立ちますが、サーバーのパフォーマンスにも影響を与える場合があります。 デフォルトでは、すべてのセッション変数の検証は無効になっています。 設定を試して、Adobe CommerceまたはMagento Open Sourceのインストールに最適な組み合わせを見つけることをお勧めします。 すべての検証変数をアクティブ化すると、過度に制限がかかっている可能性があり、プロキシサーバーを経由する、またはファイアウォールの内側から接続するインターネット接続を持つ顧客へのアクセスを妨げる可能性があります。 セッション変数とその使用方法の詳細については、ご使用の Linux®システムのシステム管理に関するドキュメントを参照してください。

**_セッション検証を設定するには、次の手順に従います。_**

1. 次の日： _管理者_ サイドバー、移動  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 _[!UICONTROL General]_を選択します。**[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Session Validation Settings]** 」セクションに入力します。

1. 次の各設定オプションを設定します。

   - **[!UICONTROL Validate REMOTE_ADDR]**  — に設定します。 `Yes` リクエストの IP アドレスが、 `$_SESSION` 変数を使用します。

   - **[!UICONTROL Validate HTTP_VIA]**  — に設定します。 `Yes` 受信リクエストのプロキシアドレスが、 `$_SESSION` 変数を使用します。

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]**  — に設定します。 `Yes` を使用して、リクエストの forwarded-for アドレスが、 `$_SESSION` 変数を使用します。

   - **[!UICONTROL Validate HTTP_USER_AGENT]**  — に設定します。 `Yes` を使用して、セッション中にストアにアクセスするために使用されるブラウザーまたはデバイスが、 `$_SESSION` 変数を使用します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 管理セッションの有効期間

セキュリティ対策として、 _管理者_ は、キーボードが操作されなくなってから 900 秒（15 分）が経過すると、最初はタイムアウトに設定されます。 セッションの有効期間は、作業スタイルに合わせて調整できます。

**_管理者セッションの有効期間を調整するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 下にスクロールして展開 **[!UICONTROL Advanced]** をクリックします。

1. クリック **[!UICONTROL Admin]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Security]_」セクションに入力します。

1. の場合 **[!UICONTROL Admin Session Lifetime (seconds)]**&#x200B;を指定した場合は、セッションがタイムアウトするまでのアクティブな状態を保つ秒数を入力します。

   ![詳細設定 — 管理セキュリティ設定](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.##管理者セッションの有効期間

セキュリティ対策として、 _管理者_ は、キーボードが操作されなくなってから 900 秒（15 分）が経過すると、最初はタイムアウトに設定されます。 セッションの有効期間は、作業スタイルに合わせて調整できます。

**_管理者セッションの有効期間を調整するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 下にスクロールして展開 **[!UICONTROL Advanced]** をクリックします。

1. クリック **[!UICONTROL Admin]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _セキュリティ_ 」セクションに入力します。

1. の場合 **[!UICONTROL Admin Session Lifetime (seconds)]**&#x200B;を指定した場合は、セッションがタイムアウトするまでのアクティブな状態を保つ秒数を入力します。

   ![詳細設定 — 管理セキュリティ設定](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.
