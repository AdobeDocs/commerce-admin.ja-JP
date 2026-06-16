---
title: CAPTCHA
description: 管理者アクセスと登録済み顧客によって開始されたさまざまなストアフロントアクション用にCAPTCHAを設定する方法について説明します。
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/w7DLKLlK4MsGrK9kOw3-dsgEUqsGhszgjiZ7F9Vr0ak
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 992
ht-degree: 0%

---

# CAPTCHA

CAPTCHAとは、コンピューター（または「ボット」）ではなく、人間がサイトとやり取りすることを保証するビジュアルデバイスです。 CAPTCHAは、_Completely Automated Public Turing testの頭字語で、コンピューターと人間を区別します_。 これは、管理者アクセスと、登録された顧客によって開始されたさまざまなストアフロントアクションの両方に使用できます。 Adobe CommerceとMagento Open Sourceは、このトピックと[Google reCAPTCHA](security-google-recaptcha.md)に記載されている標準CAPTCHAをサポートしています。

CAPTCHAは、画像の右上隅にあるリロードアイコンをクリックすることで、必要に応じて何度でもリロードできます。 CAPTCHAは完全に設定可能であり、毎回、または定義された数のログイン試行失敗後にのみ設定できます。

![CAPTCHAでログイン &#x200B;](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## 管理者用CAPTCHAの設定

セキュリティをさらに強化するために、管理者のログインとパスワードを忘れたページにCAPTCHAを追加できます。 管理者ユーザーは、画像の右上隅にある「_リロード_ ![&#x200B; リロードアイコン &#x200B;](./assets/CAPTCHA-icon-reload.png)」アイコンをクリックして、表示されたCAPTCHAをリロードできます。 リロード数は無制限です。

![管理者 – CAPTCHA](./assets/security-captcha-admin.png){width="300"}でログイン

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL Admin]**&#x200B;を選択します。

1. 右上隅で、**[!UICONTROL Store View]**&#x200B;を`Default`に設定します。

   Commerce インストールの[scope](../getting-started/websites-stores-views.md#scope-settings)に複数のweb サイトが含まれる場合は、CAPTCHA設定を適用するweb サイトを選択します。

1. **[!UICONTROL CAPTCHA]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Enable CAPTCHA in Admin]**&#x200B;を`Yes`に設定します。 次に、残りのオプションを次のように入力します。

   ![管理者 – CAPTCHA設定](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - CAPTCHA シンボルに使用する&#x200B;**[!UICONTROL Font]**&#x200B;の名前を入力します（デフォルト：`LinLibertine`）。

     独自のフォントを追加するには、フォントファイルがCommerceのインストールと同じディレクトリに存在し、`app/code/Magento/Captcha/etc`のCaptcha モジュールの`config.xml` ファイルで宣言されている必要があります。

   - CAPTCHAを使用する次の&#x200B;**[!UICONTROL Forms]**&#x200B;のいずれかを選択します。 複数のフォームを選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押します。

      - `Admin Login`
      - `Admin Forgot Password`

   - **[!UICONTROL Displaying Modes]**&#x200B;を次のいずれかに設定します：

      - `Always` – 管理者にログインするには、常にCAPTCHAが必要です。
      - `After number of attempts to login` – このオプションは、管理者ログインフォームにのみ適用されます。 選択すると、_[!UICONTROL Number of Unsuccessful Attempts to Login]_&#x200B;フィールドが表示されます。 許可するログイン試行回数を入力します。 0 （ゼロ）の値は、表示モードを`Always`に設定することと似ています。

     失敗したログイン試行回数を追跡するには、1つの電子メールアドレスと1つのIP アドレスからログインするたびにカウントされます。 同じIP アドレスから許可されるログイン試行の最大数は1,000です。 この制限は、CAPTCHAが有効になっている場合にのみ適用されます。

   - **[!UICONTROL Number of Unsuccessful Attempts to Login]**&#x200B;の場合、CAPTCHAが表示されるまでに管理者がログインを試すことができる回数を入力します。 0に設定した場合（`0`）、CAPTCHAは常に必要です。

   - **[!UICONTROL CAPTCHA Timeout (minutes)]**&#x200B;の場合、CAPTCHAの有効期限が切れるまでの分数を入力します。 CAPTCHAの有効期限が切れると、管理者はページを再読み込みする必要があります。

   - **[!UICONTROL Number of Symbols]**&#x200B;を入力してCAPTCHAに表示します。 最大8つの（`8`）記号を使用できます。 各CAPTCHAで変化するシンボルの可変数の場合は、範囲（`5-8`など）を入力します。

   - **[!UICONTROL Symbols Used in CAPTCHA]**&#x200B;に、CAPTCHAでランダムに表示する文字（a ～ zおよびA ～ Z）と数字（0 ～ 9）を入力します。 `i`、`l`、`1`など、他のシンボルと区別しにくいシンボルは、CAPTCHA シンボルのデフォルトセットには含まれません。

   - CAPTCHAに示すように、管理者が大文字または小文字を正確に入力することを求める場合は、**[!UICONTROL Case Sensitive]**&#x200B;を`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## ストアフロントのCAPTCHAの設定

お客様は、アカウントにログインするたびに、またはログインに失敗した後に、CAPTCHAを入力する必要があります。 さらに、ストアフロント全体で使用される多数のフォームを設定して、CAPTCHAによる検証を必要とすることができます。

![&#x200B; チェックアウト中のCAPTCHA](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Customer Configuration]**&#x200B;を選択します。

1. **[!UICONTROL CAPTCHA]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

![Customer CAPTCHA設定](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable CAPTCHA on Storefront]**&#x200B;を`Yes`に設定します。 次に、残りのオプションを次のように入力します。

   - CAPTCHA シンボルに使用する&#x200B;**[!UICONTROL Font]**&#x200B;の名前を入力します（デフォルト：`LinLibertine`）。

     独自のフォントを追加するには、フォントファイルがCommerce インストールと同じディレクトリに存在し、CAPTCHA モジュールの`config.xml` ファイルで宣言されている必要があります。

   - CAPTCHAを使用する次の&#x200B;**[!UICONTROL Forms]**&#x200B;のいずれかを選択します。 複数のフォームを選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押します。

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` （[&#x200B; セキュリティパッチ &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _ナレッジベース_&#x200B;の記事を参照）
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）
      - `Create company` ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2Bでのみ利用可能）

   - **[!UICONTROL Displaying Mode]**&#x200B;を次のいずれかに設定します：

      - `Always` – 選択したフォームにアクセスするには、常にCAPTCHAが必要です。
      - `After number of attempts to login` — CAPTCHAが表示されるまでのログイン試行回数を入力します。 0 （ゼロ）の値は「Always」と似ています。 選択すると、失敗したログイン試行回数が表示されます。 このオプションは、パスワードを忘れたフォームには適用されません。このフォームを有効にすると、常にCAPTCHAが表示されます。

   - **[!UICONTROL Number of Unsuccessful Attempts to Login]**&#x200B;の場合、CAPTCHAが表示されるまでに顧客が正常にログインできない回数を入力します。 0に設定した場合（`0`）、CAPTCHAは常に使用されます。

   - **[!UICONTROL CAPTCHA Timeout (minutes)]**&#x200B;の場合、CAPTCHAの有効期限が切れるまでの分数を入力します。 CAPTCHAの有効期限が切れると、顧客はページを再読み込みして新しいCAPTCHAを生成する必要があります。

   - **[!UICONTROL Number of Symbols]**&#x200B;を入力してCAPTCHAに表示します。 最大8つの（`8`）記号を使用できます。 各CAPTCHAで変化するシンボルの可変数の場合は、範囲（`5-8`など）を入力します。

   - **[!UICONTROL Symbols Used in CAPTCHA]**&#x200B;に、CAPTCHAでランダムに表示する文字（a ～ zおよびA ～ Z）と数字（0 ～ 9）を入力します。 既定の文字セットには、`I`や`1`などの類似した記号は含まれていません。 最適な結果を得るには、ユーザーが容易に識別できる記号を使用します。

   - CAPTCHAに示されているとおりに大文字または小文字の文字を入力することを顧客に要求する場合は、**[!UICONTROL Case Sensitive]**&#x200B;を`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
