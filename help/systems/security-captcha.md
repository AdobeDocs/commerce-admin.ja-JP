---
title: CAPTCHA
description: 登録ユーザーによって開始される管理者アクセスおよび様々なストアフロントアクション用に CAPTCHA を設定する方法について説明します。
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 0%

---

# CAPTCHA

CAPTCHA は、コンピューター（または「ボット」）ではなく人間がサイトとやり取りしていることを保証する視覚的なデバイスです。 CAPTCHA は、の頭字語です _コンピューターと人間を区別するための完全自動化公開チューリングテスト_. 管理者アクセスと、登録済み顧客によって開始された様々なストアフロントアクションの両方に使用できます。 Adobe CommerceとMagento Open Sourceは、このトピックで説明される標準の CAPTCHA をサポートしています。 [Google reCAPTCHA](security-google-recaptcha.md).

画像の右上隅にある「再読み込み」アイコンをクリックして、CAPTCHA を必要な回数だけ再読み込みできます。 CAPTCHA は完全に設定可能で、毎回または定義した回数のログイン試行に失敗した後にのみ表示されるように設定できます。

![CAPTCHA を使用したログイン](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## 管理者用の CAPTCHA の設定

セキュリティのレベルを高めるために、管理者のログインとパスワードを忘れた場合のページに CAPTCHA を追加できます。 管理者ユーザーは、をクリックして、表示された CAPTCHA をリロードできます _Reload_ ![再読み込みアイコン](./assets/CAPTCHA-icon-reload.png) 画像の右上隅にあるアイコン。 リロードの回数に制限はありません。

![管理者 – CAPTCHA でログイン](./assets/security-captcha-admin.png){width="300"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Admin]**.

1. 右上隅で、を設定します **[!UICONTROL Store View]** 対象： `Default`.

   次の場合 [範囲](../getting-started/websites-stores-views.md#scope-settings) Commerceのインストールに複数の web サイトが含まれている場合は、CAPTCHA 設定を適用する web サイトを選択します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL CAPTCHA]** セクション。

1. を設定 **[!UICONTROL Enable CAPTCHA in Admin]** 対象： `Yes`. その後、残りのオプションを次のように設定します。

   ![管理者 – CAPTCHA 設定](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - の名前を入力 **[!UICONTROL Font]** を CAPTCHA シンボルに使用します（デフォルト： `LinLibertine`）に設定します。

     独自のフォントを追加するには、フォントファイルがCommerceのインストール先と同じディレクトリにあり、で宣言されている必要があります。 `config.xml` の Captcha モジュールのファイル `app/code/Magento/Captcha/etc`.

   - 次のいずれかを選択します **[!UICONTROL Forms]** CAPTCHA を使用する場所。 複数のフォームを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したままにします。

      - `Admin Login`
      - `Admin Forgot Password`

   - を設定 **[!UICONTROL Displaying Modes]** を次のいずれかに変更します。

      - `Always`  – 管理者にログインするには、常に CAPTCHA が必要です。
      - `After number of attempts to login`  – このオプションは、管理者ログインフォームにのみ適用されます。 選択すると、 _[!UICONTROL Number of Unsuccessful Attempts to Login]_フィールドが表示されます。 許可するログイン試行回数を入力します。 値が 0 （ゼロ）の場合は、表示モードをに設定する場合と似ています。 `Always`.

     失敗したログイン試行の回数を追跡するために、1 つのメールアドレスおよび 1 つの IP アドレスからのログイン試行がカウントされます。 同じ IP アドレスから許可されるログイン試行回数の上限は 1,000 です。 この制限は、CAPTCHA が有効な場合にのみ適用されます。

   - の場合 **[!UICONTROL Number of Unsuccessful Attempts to Login]**：管理者がログインを試みる回数を入力します。この回数を超えると CAPTCHA が表示されます。 ゼロに設定した場合（`0`）、CAPTCHA は常に必要です。

   - の場合 **[!UICONTROL CAPTCHA Timeout (minutes)]**:CAPTCHA の有効期限が切れるまでの分数を入力します。 CAPTCHA の有効期限が切れたら、管理者はページをリロードする必要があります。

   - を入力 **[!UICONTROL Number of Symbols]** CAPTCHA に表示されます。 最大 8 （`8`）記号を使用できます。 各 CAPTCHA で変化するシンボルの数を変更するには、範囲（例：）を入力します `5-8`）に設定します。

   - の場合 **[!UICONTROL Symbols Used in CAPTCHA]**&#x200B;を選択し、CAPTCHA でランダムに表示する文字（a ～ z と A ～ Z）および数字（0 ～ 9）を入力します。 次のような、他のシンボルと区別しにくいシンボル `i`, `l`、または `1`は、CAPTCHA シンボルのデフォルトセットには含まれません。

   - を設定 **[!UICONTROL Case Sensitive]** 対象： `Yes` 管理者に、CAPTCHA で示されているとおりに大文字と小文字を正確に入力させたい場合。

1. 完了したら、 **[!UICONTROL Save Config]**.

## ストアフロントの CAPTCHA の設定

顧客は、アカウントにログインするたびに、またはログインに何度か失敗した後に、CAPTCHA を入力する必要が生じる場合があります。 さらに、ストアフロント全体で使用される多数のフォームを、CAPTCHA による検証を必要とするように設定できます。

![チェックアウト中の CAPTCHA](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Customer Configuration]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL CAPTCHA]** セクション。

![顧客の CAPTCHA 設定](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enable CAPTCHA on Storefront]** 対象： `Yes`. その後、残りのオプションを次のように設定します。

   - の名前を入力 **[!UICONTROL Font]** を CAPTCHA シンボルに使用します（デフォルト： `LinLibertine`）に設定します。

     独自のフォントを追加するには、フォントファイルがCommerceのインストール先と同じディレクトリにあり、で宣言されている必要があります。 `config.xml` captcha モジュールのファイル。

   - 次のいずれかを選択します **[!UICONTROL Forms]** CAPTCHA を使用する場所。 複数のフォームを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したままにします。

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` （を参照） [セキュリティパッチ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _ナレッジベース_ 記事）
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）
      - `Create company` ![Adobe Commerceの B2B](../assets/b2b.svg) （B2B でAdobe Commerceでのみ使用可能）

   - を設定 **[!UICONTROL Displaying Mode]** を次のいずれかに変更します。

      - `Always`  – 選択したフォームにアクセスするには、常に CAPTCHA が必要です。
      - `After number of attempts to login` — CAPTCHA が表示されるまでのログイン試行回数を入力します。 値が 0 （ゼロ）の場合は、「常に」に似ています。 選択すると、失敗したログインの試行回数が表示されます。 このオプションは、「パスワードを忘れた場合」フォームには適用されません。このフォームを有効にすると、常に CAPTCHA が表示されます。

   - の場合 **[!UICONTROL Number of Unsuccessful Attempts to Login]**：顧客がログインに失敗した回数を入力します。この回数を超えると CAPTCHA が表示されます。 ゼロに設定した場合（`0`）、CAPTCHA は常に使用されます。

   - の場合 **[!UICONTROL CAPTCHA Timeout (minutes)]**:CAPTCHA の有効期限が切れるまでの分数を入力します。 CAPTCHA の有効期限が切れたら、新しい CAPTCHA を生成するために、顧客はページをリロードする必要があります。

   - を入力 **[!UICONTROL Number of Symbols]** CAPTCHA に表示されます。 最大 8 （`8`）記号を使用できます。 各 CAPTCHA で変化するシンボルの数を変更するには、範囲（例：）を入力します `5-8`）に設定します。

   - の場合 **[!UICONTROL Symbols Used in CAPTCHA]**&#x200B;を選択し、CAPTCHA でランダムに表示する文字（a ～ z と A ～ Z）および数字（0 ～ 9）を入力します。 デフォルトの文字セットには、次のような類似の記号は含まれていません `I` または `1`. 最適な結果を得るには、ユーザーが識別しやすい記号を使用します。

   - を設定 **[!UICONTROL Case Sensitive]** 対象： `Yes` ユーザーに対して、CAPTCHA で示されているとおりに大文字と小文字を入力することを求める場合。

1. 完了したら、 **[!UICONTROL Save Config]**.
