---
title: Google reCAPTCHA
description: 登録ユーザーによって開始される管理者アクセスおよび様々なストアフロントアクション用にGoogle reCAPTCHA を設定する方法について説明します。
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) コンピューター（または「ボット」）ではなく人間が web サイトとやり取りしていることを確認します。 標準のAdobe CommerceやMagento Open Sourceとは異なります [CAPTCHA](security-captcha.md)Google reCAPTCHA では、様々な表示オプションと表示方法を選択して、セキュリティを強化できます。 追加の web サイトトラフィック情報は、Google reCAPTCHA アカウントのダッシュボードで確認できます。

Google reCAPTCHA は、管理者とストアフロント用に個別に設定されます。

- 管理者の場合、Google reCAPTCHA は [ログイン](../getting-started/admin-signin.md) ページで、ユーザーがパスワードのリセットをリクエストした場合。 標準のCommerceの場合 [CAPTCHA](security-captcha.md) も有効になっています。Google reCAPTCHA は問題なく同時に使用できます。

- ストアフロントでは、Google reCAPTCHA を使用して、にログインできます [顧客アカウント](../customers/customer-sign-in.md)からメッセージを送信します [お問い合わせ](../getting-started/store-details.md#contact-us-form) ページなど、多数のストアフロントに設置されています。

  ![Google reCAPTCHA - カスタマーログイン](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA は、以下のようないくつかの方法で実装できます。

- _reCAPTCHA v3 Invisible_ - アルゴリズムを使用してユーザーのインタラクションを評価し、スコアに基づいてユーザーが人間である可能性を判断します。

- _reCAPTCHA v2 非表示_ - ユーザー操作なしでバックグラウンド検証を実行します。 ユーザーと顧客は自動的に検証されますが、課題を完了するには特定の画像を選択する必要がある場合があります。

- _reCAPTCHA v2 （「I am not a robot」）_  – を含むリクエストを検証します。 _「僕はロボットじゃない」_ チェックボックス。

>[!IMPORTANT]
>
>Google reCAPTCHA を設定する前に、 `PHP.ini` ファイルには次の設定が含まれます。 `allow_url_fopen = 1`. これには、開発者の支援が必要になる場合があります。 参照： [必要な PHP 設定](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)インストールガイドの {:target=&quot;_blank&quot;}。

## 手順 1:Google reCAPTCHA キーの生成

Google reCAPTCHA を有効にするには、1 組の API キーが必要です。 これらのキーは、reCAPTCHA サイトから無料で取得できます。 キーを生成する前に、使用する reCAPTCHA のタイプを知っておく必要があります。

1. Google reCAPTCHA ページを開き、アカウントにログインします。

1. の場合 **[!UICONTROL Label]**&#x200B;を入力し、内部参照用のキーを識別する名前を入力します。

   Adobe CommerceまたはMagento Open Sourceのインストールで使用される reCAPTCHA タイプごとに 1 セットのキーが必要です。 例： `Commerce Invisible`

1. の場合 **[!UICONTROL reCAPTCHA type]**&#x200B;で、使用する方法を選択します。

   - _reCAPTCHA v3 Invisible_
   - _reCAPTCHA v2 非表示_
   - _reCAPTCHA v2 （「I am not a robot」）_

1. の場合 **[!UICONTROL Domain]**&#x200B;ストアのドメインを入力します。 例：mystore.com

   異なるドメインを持つ複数のストアがある場合は、各ドメインを別々の行に入力します。

   - ストアドメインとサブドメインを追加します。
   - 次を追加できます `localhost`、その他のローカル VM ドメイン、およびテストに必要なステージングドメイン。

1. このチェックボックスを選択すると、 **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. （オプション）「」を選択します **[!UICONTROL Send alerts to owners]** Googleが問題や疑わしいトラフィックを検出した場合に通知を送信するためのチェックボックス。

1. クリック **[!UICONTROL Submit]** 登録を完了し、キーを受け取るために。

   >[!IMPORTANT]
   >
   >すべてのキーがすべてのタイプの reCAPTCHA に適用できるわけではなく、適用を誤ると、予期しない動作が発生する可能性があります。 例えば、reCAPTCHA v2 用に生成されたGoogle reCAPTCHA キー（「I&#39;m not a robot」）は、では動作しません _reCAPTCHA v2 非表示_ また、reCAPTCHA が有効になっている場合は、機能がブロックされる可能性があります。

## 手順 2：管理者用のGoogle reCAPTCHA の設定

1. 管理者アカウントにログインします。

1. 管理サイドバーで、に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 右上隅で、を設定します **[!UICONTROL Store View]** 対象： `Default Config`.

1. 左側のパネルで、を展開します **[!UICONTROL Security]** をクリックして、 **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >をクリア **[!UICONTROL Use system value]** 設定する各フィールドのチェックボックス。

1. 使用目的 _[!DNL reCAPTCHA v2 ("I am not a robot")]_を展開します&#x200B;**[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**を選択し、次の操作を実行します。

   - の場合 **[!UICONTROL Google API Website Key]**&#x200B;に、Google reCAPTCHA アカウントの登録時にこの reCAPTCHA タイプ用に作成した web サイトキーを入力します。

   - の場合 **[!UICONTROL Google API Secret Key]**&#x200B;に、Google reCAPTCHA アカウントに関連付けられている秘密鍵を入力します。

   - の場合 **[!UICONTROL Size]**&#x200B;で、表示するGoogle reCAPTCHA ボックスのサイズを選択します。 オプション： `Normal (default)` / `Compact`

   - の場合 **[!UICONTROL Theme]**&#x200B;を選択して、Google reCAPTCHA ボックスのスタイル設定に使用するテーマを選択します。 オプション： `Light Theme (default)` / `Dark Theme`

   - の場合 **[!UICONTROL Language Code]**&#x200B;を入力し、2 文字のコードを入力して、 [Google reCAPTCHA のテキストおよびメッセージングに使用する言語](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - 「私はロボットではありません」](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. 使用目的 _[!DNL reCAPTCHA v2 Invisible]_を展開します&#x200B;**[!UICONTROL reCAPTCHA v2 Invisible]**を選択し、次の操作を実行します。

   - の場合 **[!UICONTROL Google API Website Key]**&#x200B;に、Google reCAPTCHA アカウントの登録時にこの reCAPTCHA タイプ用に作成した web サイトキーを入力します。

   - の場合 **[!UICONTROL Google API Secret Key]**&#x200B;に、Google reCAPTCHA アカウントに関連付けられている秘密鍵を入力します。

   - の場合 **[!UICONTROL Invisible Badge Position]**&#x200B;を選択し、各ページで使用するバッジの位置を選択します。 オプション： `Inline` / `Bottom Right` / `Bottom Left`

   - の場合 **[!UICONTROL Theme]**&#x200B;で、Google reCAPTCHA ボックスのスタイル設定に使用するテーマを選択します。 オプション： `Light Theme (default)` / `Dark Theme`

   - の場合 **[!UICONTROL Language Code]**&#x200B;を入力します。には、 [Google reCAPTCHA のテキストおよびメッセージングに使用する言語](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 非表示](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. 使用目的 _[!DNL reCAPTCHA v3 Invisible]_を展開します&#x200B;**[!UICONTROL reCAPTCHA v3 Invisible]**を選択し、次の操作を実行します。

   - の場合 **[!UICONTROL Google API Website Key]**&#x200B;に、Google reCAPTCHA アカウントの登録時にこの reCAPTCHA タイプ用に作成した web サイトキーを入力します。

   - の場合 **[!UICONTROL Google API Secret Key]**&#x200B;に、Google reCAPTCHA アカウントに関連付けられている秘密鍵を入力します。

   - を入力 **[!UICONTROL Minimum Score Threshold]** ユーザーインタラクションが潜在的なリスクとしてフラグ付けされるタイミングを識別します。ここで、1.0 は一般的なユーザーインタラクションで、0.0 はボットである可能性があります。 デフォルト： `0.5`

   - の場合 **[!UICONTROL Invisible Badge Position]**&#x200B;各ページで使用する位置を選択します。 オプション： `Inline` / `Bottom Right` / `Bottom Left`

   - の場合 **[!UICONTROL Theme]**&#x200B;で、Google reCAPTCHA ボックスのスタイル設定に使用するテーマを選択します。 オプション： `Light Theme (default)` / `Dark Theme`

   - の場合 **[!UICONTROL Language Code]**&#x200B;を入力します。には、 [Google reCAPTCHA のテキストおよびメッセージングに使用する言語](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 Invisible](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. を展開 **[!UICONTROL reCAPTCHA Validation Failure Messages]** 検証に失敗した場合や検証を完了できない場合に、管理者に表示されるメッセージを入力します。

   ![reCAPTCHA 失敗メッセージ](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. を展開します。 **[!UICONTROL Admin Panel]** を参照し、必要に応じて次の項目を設定します。

   - を設定 **[!UICONTROL Enable for Login]** を管理者のログインページに使用する reCAPTCHA タイプに変更します。

   - を設定 **[!UICONTROL Enable for Forgot Password]** を、パスワードリセットリクエストに使用する reCAPTCHA タイプに変更します。

   ![reCAPTCHA 管理オプション](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## 手順 3：ストアフロントのGoogle reCAPTCHA の設定

1. の下の左パネルで _[!UICONTROL Security]_、を選択&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**.

1. ストアフロントで使用する reCAPTCHA タイプごとに、セクションを完了します。

   の情報を参照してください。 _手順 2：管理者用のGoogle reCAPTCHA の設定_ 各 reCAPTCHA タイプのオプションについて詳しくは、を参照してください。

1. を展開 **[!UICONTROL reCAPTCHA Validation Failure Messages]** 検証に失敗した場合や完了できない場合にストアフロントに表示されるメッセージを入力します。

1. を展開します。 **[!UICONTROL Storefront]** セクション。

   >[!NOTE]
   >
   >をクリア **[!UICONTROL Use system value]** 設定する各フィールドのチェックボックス。

1. 各ストアフロントの場所フィールドを、使用するように設定した reCAPTCHA のタイプに設定します。

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B でのみ使用可能）
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![ストアフロントオプションの設定](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 手順 4：設定を保存する

1. 設定が完了したら、 **[!UICONTROL Save Config]**.

1. ワークスペースの上部にあるメッセージで、 **[!UICONTROL Cache Management]** 無効な各キャッシュを更新します。
