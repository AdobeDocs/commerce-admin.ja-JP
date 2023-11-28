---
title: CAPTCHA
description: 管理者アクセス用に CAPTCHA を設定する方法と、登録ユーザーが開始した様々なストアフロントアクションについて説明します。
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# CAPTCHA

CAPTCHA は、人間がコンピュータ（または「ボット」）ではなく、サイトとやり取りしていることを確認する視覚的なデバイスです。 CAPTCHA は、 _コンピュータと人間を分かち合うための完全に自動化された公開チューリングテスト_. これは、管理者アクセスと、登録ユーザーが開始した様々なストアフロントアクションの両方に使用できます。 Adobe CommerceとMagento Open Sourceは、このトピックおよび [Google reCAPTCHA](security-google-recaptcha.md).

画像の右上隅にある再読み込みアイコンをクリックして、CAPTCHA を必要な回数だけ再読み込みできます。 CAPTCHA は完全に設定可能で、毎回、または定義されたログイン試行失敗回数の後にのみ設定できます。

![CAPTCHA でログイン](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## 管理者に対する CAPTCHA の設定

セキュリティレベルを高めるために、管理者のログインページとパスワードを忘れたページに CAPTCHA を追加できます。 管理者は、 _リロード_ ![再読み込みアイコン](./assets/CAPTCHA-icon-reload.png) アイコンをクリックします。 リロード回数は無制限です。

![管理 — CAPTCHA でログイン](./assets/security-captcha-admin.png){width="300"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Admin]**.

1. 右上隅で、 **[!UICONTROL Store View]** から `Default`.

   次の場合、 [範囲](../getting-started/websites-stores-views.md#scope-settings) コマースインストールに複数の Web サイトが含まれている場合は、CAPTCHA 設定を適用する Web サイトを選択します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL CAPTCHA]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enable CAPTCHA in Admin]** から `Yes`. 次の手順に従って、残りのオプションを完了します。

   ![管理 — CAPTCHA 設定](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - 名前を入力 **[!UICONTROL Font]** CAPTCHA シンボルに使用する ( デフォルトは： `LinLibertine`) をクリックします。

     独自のフォントを追加するには、フォントファイルが Commerce インストールと同じディレクトリに存在し、 `config.xml` 次の場所にある Captcha モジュールのファイル： `app/code/Magento/Captcha/etc`.

   - 次のいずれかを選択します。 **[!UICONTROL Forms]** ここで、CAPTCHA が使用されます。 複数のフォームを選択するには、Ctrl キー (PC) または Command キー (Mac) を押したままにします。

      - `Admin Login`
      - `Admin Forgot Password`

   - 設定 **[!UICONTROL Displaying Modes]** を次のいずれかに変更します。

      - `Always`  — 管理者にログインするには、常に CAPTCHA が必要です。
      - `After number of attempts to login`  — このオプションは、「管理者ログイン」フォームにのみ適用されます。 選択すると、 _[!UICONTROL Number of Unsuccessful Attempts to Login]_フィールドが表示されます。 許可するログイン試行回数を入力します。 0（ゼロ）の値は、表示モードを `Always`.

     ログインの失敗回数を追跡するには、1 つの E メールアドレスと 1 つの IP アドレスからログインを試みるたびに、その回数がカウントされます。 同じ IP アドレスから許可されるログイン試行の最大回数は 1,000 です。 この制限は、CAPTCHA が有効な場合にのみ適用されます。

   - の場合 **[!UICONTROL Number of Unsuccessful Attempts to Login]**」には、管理者がログインを試みてから CAPTCHA が表示されるまでの回数を入力します。 0 に設定した場合 (`0`) の場合、CAPTCHA が常に必要です。

   - の場合 **[!UICONTROL CAPTCHA Timeout (minutes)]**」には、CAPTCHA の有効期限が切れるまでの時間（分）を入力します。 CAPTCHA の有効期限が切れたら、管理者はページを再読み込みする必要があります。

   - 次を入力します。 **[!UICONTROL Number of Symbols]** を CAPTCHA に表示する。 最大 8 個 (`8`) 記号を使用できます。 各 CAPTCHA で変化するシンボルの数が可変の場合は、範囲 ( 例： `5-8`) をクリックします。

   - の場合 **[!UICONTROL Symbols Used in CAPTCHA]** CAPTCHA でランダムに表示する文字 (a ～ z、A ～ Z) と数字 (0 ～ 9) を入力します。 他のシンボルと区別しにくいシンボル（例： ） `i`, `l`または `1`のデフォルトの CAPTCHA 記号セットには含まれていません。

   - 設定 **[!UICONTROL Case Sensitive]** から `Yes` 管理者が、CAPTCHA に示すように、文字を大文字または小文字で入力する必要がある場合。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## ストアフロント用の CAPTCHA の設定

お客様は、アカウントにログインするたびに、またはログインに何度か失敗した後に、CAPTCHA を入力する必要があります。 また、ストアフロント全体で使用される多数のフォームを、CAPTCHA による検証が必要になるように設定できます。

![チェックアウト時の CAPTCHA](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Customer Configuration]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL CAPTCHA]** 」セクションに入力します。

![顧客 CAPTCHA の設定](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable CAPTCHA on Storefront]** から `Yes`. 次の手順に従って、残りのオプションを完了します。

   - 名前を入力 **[!UICONTROL Font]** CAPTCHA シンボルに使用する ( デフォルトは： `LinLibertine`) をクリックします。

     独自のフォントを追加するには、フォントファイルが Commerce インストールと同じディレクトリに存在し、 `config.xml` CAPTCHA モジュールのファイル。

   - 次のいずれかを選択します。 **[!UICONTROL Forms]** ここで、CAPTCHA が使用されます。 複数のフォームを選択するには、Ctrl キー (PC) または Command キー (Mac) を押したままにします。

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` ( [セキュリティパッチ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _ナレッジベース_ 記事 )
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ )
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )
      - `Create company` ![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B では、Adobe Commerceでのみ使用可能 )

   - 設定 **[!UICONTROL Displaying Mode]** を次のいずれかに変更します。

      - `Always`  — 選択したフォームにアクセスするには、CAPTCHA が常に必要です。
      - `After number of attempts to login` — CAPTCHA が表示されるまでのログイン試行回数を入力します。 値 0 （ゼロ）は、「常に」に似ています。 このオプションを選択すると、ログイン試行の失敗回数が表示されます。 このオプションは「パスワードを忘れた場合」フォームには適用されません。有効にした場合、常に CAPTCHA が表示されます。

   - の場合 **[!UICONTROL Number of Unsuccessful Attempts to Login]**」には、顧客が失敗して CAPTCHA が表示されるまでのログイン回数を入力します。 0 に設定した場合 (`0`) の場合、CAPTCHA が常に使用されます。

   - の場合 **[!UICONTROL CAPTCHA Timeout (minutes)]**」には、CAPTCHA の有効期限が切れるまでの時間（分）を入力します。 CAPTCHA の有効期限が切れたら、顧客はページを再読み込みして新しい CAPTCHA を生成する必要があります。

   - 次を入力します。 **[!UICONTROL Number of Symbols]** を CAPTCHA に表示する。 最大 8 個 (`8`) 記号を使用できます。 各 CAPTCHA で変化するシンボルの数が可変の場合は、範囲 ( 例： `5-8`) をクリックします。

   - の場合 **[!UICONTROL Symbols Used in CAPTCHA]** CAPTCHA でランダムに表示する文字 (a ～ z、A ～ Z) と数字 (0 ～ 9) を入力します。 デフォルトの文字セットには、次のような類似した記号は含まれません。 `I` または `1`. 最適な結果を得るには、ユーザーが簡単に識別できる記号を使用します。

   - 設定 **[!UICONTROL Case Sensitive]** から `Yes` CAPTCHA に示すように、お客様が大文字または小文字の文字を入力する必要がある場合。

1. 完了したら、「 **[!UICONTROL Save Config]**.
