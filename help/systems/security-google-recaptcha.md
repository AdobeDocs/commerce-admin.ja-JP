---
title: Google reCAPTCHA V3 および V2
description: 登録ユーザーによって開始される管理者アクセスおよび様々なストアフロントアクション用にGoogle reCAPTCHA を設定する方法について説明します。
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 80b2ecc9fddd7a20d6824182f41f0d19f6d51003
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 0%

---

# Google reCAPTCHA V3 および V2

[Google reCAPTCHA](https://developers.google.com/recaptcha) は、コンピューター（または「ボット」）ではなく人間が web サイトとやり取りしていることを確認します。 標準のAdobe CommerceやMagento Open Source[CAPTCHA](security-captcha.md) とは異なり、Google reCAPTCHA は、様々な表示オプションおよび表示方法を使用してセキュリティを強化します。 追加の web サイトトラフィック情報は、Google reCAPTCHA アカウントのダッシュボードで確認できます。

Google reCAPTCHA は、管理者とストアフロント用に個別に設定されます。

- 管理者の場合、Google reCAPTCHA は [&#x200B; ログイン &#x200B;](../getting-started/admin-signin.md) ページで、またユーザーがパスワードリセットをリクエストしたときに使用できます。 標準のCommerce[CAPTCHA](security-captcha.md) も有効になっている場合は、Google reCAPTCHA を問題なく同時に使用できます。

- ストアフロントでは、Google reCAPTCHA を使用して、[&#x200B; カスタマーアカウント &#x200B;](../customers/customer-sign-in.md) にサインインしたり、[&#x200B; お問い合わせ &#x200B;](../getting-started/store-details.md#contact-us-form) ページからメッセージを送信したり、他の多くのストアフロントの場所で使用したりできます。

  ![Google reCAPTCHA - カスタマーログイン &#x200B;](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA は、以下のようないくつかの方法で実装できます。

- _reCAPTCHA v3 非表示_ - アルゴリズムを使用して、ユーザーのインタラクションを評価し、スコアに基づいて、ユーザーが人間である可能性を判断します。

- _reCAPTCHA v2 Invisible_ - ユーザーの操作なしでバックグラウンド検証を実行します。 ユーザーと顧客は自動的に検証されますが、課題を完了するには特定の画像を選択する必要がある場合があります。

- _reCAPTCHA v2 （「私はロボットではありません」）_ — 「私はロボットではありません _チェックボックスでリクエストを検証_ ます。

>[!IMPORTANT]
>
>Google reCAPTCHA を設定する前に、`PHP.ini` ファイルに次の設定が含まれていることを確認してください。`allow_url_fopen = 1` これには、開発者の支援が必要になる場合があります。 インストールガイドの [&#x200B; 必要な PHP 設定 &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=ja){:target="_blank"} を参照してください。

## 手順 1:Google reCAPTCHA キーの生成

Google reCAPTCHA を有効にするには、1 組の API キーが必要です。 これらのキーは、reCAPTCHA サイトから無料で取得できます。 キーを生成する前に、使用する reCAPTCHA のタイプを知っておく必要があります。

1. Google reCAPTCHA ページを開き、アカウントにログインします。

1. **[!UICONTROL Label]**：内部参照用のキーを識別する名前を入力します。

   Adobe CommerceまたはMagento Open Sourceのインストールで使用される reCAPTCHA タイプごとに 1 セットのキーが必要です。 例：`Commerce Invisible`

1. **[!UICONTROL reCAPTCHA type]**：使用する方法を選択します。

   - _reCAPTCHA v3 非表示_
   - _reCAPTCHA v2 非表示_
   - _reCAPTCHA v2 （&quot;I am not a robot&quot;）_

1. **[!UICONTROL Domain]**: ストアのドメインを入力します。 例：mystore.com

   異なるドメインを持つ複数のストアがある場合は、各ドメインを別々の行に入力します。

   - ストアドメインとサブドメインを追加します。
   - テストの必要に応じて、`localhost`、その他のローカル VM ドメイン、ステージングドメインを追加できます。

1. **[!UICONTROL Accept the reCAPTCHA Terms of Service]** すチェックボックスを選択します。

1. （オプション）「**[!UICONTROL Send alerts to owners]**」チェックボックスをオンにすると、Googleで問題や疑わしいトラフィックが検出された場合に通知が送信されます。

1. **[!UICONTROL Submit]** をクリックして登録を完了し、キーを受け取ります。

   >[!IMPORTANT]
   >
   >すべてのキーがすべてのタイプの reCAPTCHA に適用できるわけではなく、適用を誤ると、予期しない動作が発生する可能性があります。 例えば、「I&#39;m not a robot」用に生成されたGoogle reCAPTCHA キーは、_reCAPTCHA v2 Invisible_ では機能せず、reCAPTCHA が有効になっている場合は機能をブロックする可能性があります。

## 手順 2：管理者用のGoogle reCAPTCHA の設定

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

1. 管理者アカウントにログインします。

1. 管理者サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 右上隅の **[!UICONTROL Store View]** を `Default Config` に設定します。

1. 左側のパネルで「**[!UICONTROL Security]**」を展開し、「**[!UICONTROL Google reCAPTCHA Admin Panel]**」をクリックします。

   >[!NOTE]
   >
   >設定する各フィールドの「**[!UICONTROL Use system value]**」チェックボックスをオフにします。

1. _[!DNL reCAPTCHA v2 ("I am not a robot")]_&#x200B;を使用するには、「**[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**」セクションを展開して、次の手順を実行します。

   - **[!UICONTROL Google API Website Key]**:Google reCAPTCHA アカウントの登録時にこの reCAPTCHA タイプ用に作成された web サイトキーを入力します。

   - **[!UICONTROL Google API Secret Key]**:Google reCAPTCHA アカウントに関連付けられている秘密鍵を入力します。

   - **[!UICONTROL Size]**：表示するGoogle reCAPTCHA ボックスのサイズを選択します。 オプション：`Normal (default)` / `Compact`

   - **[!UICONTROL Theme]** しくは、Google reCAPTCHA ボックスのスタイル設定に使用するテーマを選択します。 オプション：`Light Theme (default)` / `Dark Theme`

   - **[!UICONTROL Language Code]** しくは、2 文字のコードを入力して [Google reCAPTCHA テキストおよびメッセージングで使用される言語 &#x200B;](https://developers.google.com/recaptcha/docs/language) を指定します。

   ![reCAPTCHA v2 - 「私はロボットではありません」 &#x200B;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. _[!DNL reCAPTCHA v2 Invisible]_&#x200B;を使用するには、「**[!UICONTROL reCAPTCHA v2 Invisible]**」セクションを展開して、次の手順を実行します。

   - **[!UICONTROL Google API Website Key]**:Google reCAPTCHA アカウントの登録時にこの reCAPTCHA タイプ用に作成された web サイトキーを入力します。

   - **[!UICONTROL Google API Secret Key]**:Google reCAPTCHA アカウントに関連付けられている秘密鍵を入力します。

   - **[!UICONTROL Invisible Badge Position]** しくは、各ページで使用するバッジの位置を選択します。 オプション：`Inline`/`Bottom Right`/`Bottom Left`

   - **[!UICONTROL Theme]** しくは、Google reCAPTCHA ボックスのスタイル設定に使用するテーマを選択します。 オプション：`Light Theme (default)` / `Dark Theme`

   - **[!UICONTROL Language Code]** しくは、（Google reCAPTCHA テキストおよびメッセージングで使用される言語 [&#x200B; を指定する 2 文字のコードを入力し &#x200B;](https://developers.google.com/recaptcha/docs/language) す。

   ![reCAPTCHA v2 非表示 &#x200B;](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. _[!DNL reCAPTCHA v3 Invisible]_&#x200B;を使用するには、「**[!UICONTROL reCAPTCHA v3 Invisible]**」セクションを展開して、次の手順を実行します。

   - **[!UICONTROL Google API Website Key]**:Google reCAPTCHA アカウントの登録時にこの reCAPTCHA タイプ用に作成された web サイトキーを入力します。

   - **[!UICONTROL Google API Secret Key]**:Google reCAPTCHA アカウントに関連付けられている秘密鍵を入力します。

   - ユーザーインタラクションが潜在的なリスクとしてフラグ付けされるタイミングを識別する **[!UICONTROL Minimum Score Threshold]** を入力します。1.0 は一般的なユーザーインタラクションで、0.0 はボットである可能性があります。 デフォルト：`0.5`

   - **[!UICONTROL Invisible Badge Position]** しくは、各ページで使用する位置を選択します。 オプション：`Inline`/`Bottom Right`/`Bottom Left`

   - **[!UICONTROL Theme]** しくは、Google reCAPTCHA ボックスのスタイル設定に使用するテーマを選択します。 オプション：`Light Theme (default)` / `Dark Theme`

   - **[!UICONTROL Language Code]** しくは、（Google reCAPTCHA テキストおよびメッセージングで使用される言語 [&#x200B; を指定する 2 文字のコードを入力し &#x200B;](https://developers.google.com/recaptcha/docs/language) す。

   ![reCAPTCHA v3 非表示 &#x200B;](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL reCAPTCHA Validation Failure Messages]**」を展開し、検証に失敗した場合や検証を完了できない場合に管理者に表示されるメッセージを入力します。

   ![reCAPTCHA エラーメッセージ &#x200B;](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Admin Panel]**」セクションを展開し、必要に応じて以下を設定します。

   - 管理者のログインページに使用する reCAPTCHA タイプに **[!UICONTROL Enable for Login]** を設定します。

   - パスワードリセットリクエストに使用する reCAPTCHA タイプに **[!UICONTROL Enable for Forgot Password]** を設定します。

   ![reCAPTCHA 管理オプション &#x200B;](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## 手順 3：ストアフロントのGoogle reCAPTCHA の設定

1. _[!UICONTROL Security]_&#x200B;の下の左パネルで、「**[!UICONTROL Google reCAPTCHA Storefront]**」を選択します。

1. ストアフロントで使用する reCAPTCHA タイプごとに、セクションを完了します。

   各 reCAPTCHA タイプのオプションについて詳しくは、_手順 2：管理者用のGoogle reCAPTCHA の設定_ を参照してください。

1. **[!UICONTROL reCAPTCHA Validation Failure Messages]** を展開し、検証が失敗した場合や完了できなかった場合にストアフロントに表示されるメッセージを入力します。

1. 「**[!UICONTROL Storefront]**」セクションを展開します。

   >[!NOTE]
   >
   >設定する各フィールドの「**[!UICONTROL Use system value]**」チェックボックスをオフにします。

1. 各ストアフロントの場所フィールドを、使用するように設定した reCAPTCHA のタイプに設定します。

   {{recaptcha-forms-list}}

   ![&#x200B; ストアフロントオプションの設定 &#x200B;](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 手順 4：設定を保存する

1. 設定が完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. ワークスペースの上部にあるメッセージで、「**[!UICONTROL Cache Management]**」をクリックし、無効な各キャッシュを更新します。
