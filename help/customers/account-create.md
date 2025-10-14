---
title: 個々の顧客アカウントの作成
description: 訪問者は、個々の顧客アカウントを簡単に作成して、購入を管理できます。
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# 個々の顧客アカウントの作成

ストアへの訪問者はアカウントを開いて、購入とアクティビティを管理できます。 顧客は通常、ストアから独自のアカウントを作成します。 ただし、管理者から直接カスタマーアカウントを作成することもできます。これは、電話を介して顧客を支援するのに役立ちます。

以下の手順は、デフォルトの顧客アカウント設定を表しています。 フォーム内の一部のフィールドの選択と動作を変更するには、「[&#x200B; 顧客アカウントの設定 &#x200B;](../customers/customer-account-scope.md) を参照してください。

ストア管理者は、[&#x200B; 新規アカウントオプション &#x200B;](../customers/account-options-new.md) を設定して、新規登録済みの顧客に確認メールを送信することもできます。これにより、登録済みのアカウントが有効であることを確認できます。

>[!NOTE]
>
>バージョン 2.4.7 以降、ブラウザーに関係なく、メールによる確認後にアカウントにログインするには、メールとパスワードを再入力する必要があります。

## ストアフロントからアカウントを作成

店舗顧客がストアフロントでアカウントを作成します。

1. ストアフロントから、ヘッダーの右上隅にある「**[!UICONTROL Create an Account]**」をクリックします。

   ![&#x200B; アカウントの作成 &#x200B;](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. **[!UICONTROL Personal Information]** の下に、**[!UICONTROL First Name]** と **[!UICONTROL Last Name]** を入力します。

   ![&#x200B; 個人情報 &#x200B;](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. 名前とメールアドレスをニュースレター購読者のリストに追加する場合、顧客は「**[!UICONTROL Sign Up for Newsletter]**」チェックボックスを選択します。

   >[!INFO]
   >
   > このオプションは、ストアがニュースレターを公開していない場合でも表示されます。

1. 店舗のサポートスタッフに [&#x200B; 見ているものを確認 &#x200B;](../customers/login-as-customer.md) してリモートアシスタンスを提供してもらいたい場合、お客様は **[!UICONTROL Allow remote shopping assistance]** のチェックボックスを選択します。

1. **[!UICONTROL Sign-in Information]** の下に、**[!UICONTROL Email]** アドレスを入力します。

   >[!INFO]
   >
   > このメールアドレスは、ログイン資格情報の一部になり、他のカスタマーアカウントに関連付けることはできません。

   ![&#x200B; ログイン情報 &#x200B;](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. 次の 3 種類の情報を含む **[!UICONTROL Password]** を入力します。

   - 小文字
   - 大文字
   - 数値
   - 特殊文字

   **[!UICONTROL Enter]** を押すと、パスワードの強度が評価され、フィールドの下に表示されます。 パスワードが _弱_ と見なされる場合は、_強_ と評価されるまで別のパスワードを試します。

   ![&#x200B; 強力なパスワードをお勧めします &#x200B;](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. 次に、顧客が **[!UICONTROL Confirm Password]** に再度入力します。

1. 必要に応じて、「**[!UICONTROL Show Password]**」をクリックして、入力したパスワードを表示します。

1. 完了したら、「**アカウントを作成**」をクリックします。

その後、顧客はメールアドレスとパスワードを使用してアカウントに [&#x200B; ログイン &#x200B;](../customers/customer-sign-in.md) し、アドレス情報を入力できます。

## 管理者からのアカウントの作成

マーチャントは、管理者から顧客アカウントを作成できます。

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL All Customers]** に移動します。

1. 「**[!UICONTROL Add New Customer]**」をクリックします。

### 手順 1：アカウント情報の入力

![&#x200B; 顧客情報 &#x200B;](assets/new-information.png){width="700" zoomable="yes"}

1. **[!UICONTROL Account Information]** セクションで、次の操作を行います。

   - マルチサイトインストールの場合、**[!UICONTROL Associate to Website]** を顧客アカウントが適用される web サイトに設定します。
   - 該当する場合、顧客を別の **[!UICONTROL Customer Group]** ーザーに割り当てます。
   - [VAT ID 検証 &#x200B;](../stores-purchase/vat.md) を使用していて **[!UICONTROL Disable Automatic Group Change Based on VAT ID]** 認する場合は、チェックボックスを選択します。

1. 必須フィールドに入力します。

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. 必要に応じて、オプションのフィールドに入力します。

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >現在のセキュリティおよびプライバシーのベストプラクティスに従い、顧客の完全な生年月日（月、日、年）を他の個人識別子と保存することに関連して、法的およびセキュリティ上の潜在的なリスクがあることを認識しておいてください。 顧客の完全な生年月日の保存を制限し、代わりに顧客の生年月日を使用することをお勧めします。

1. _ようこそ_ メールの送信元のストア表示に **[!UICONTROL Send Welcome Email From]** を設定します。

   >[!INFO]
   >
   > ストアに異なる [&#x200B; 言語 &#x200B;](../stores-purchase/store-localize.md) のビューがある場合、この設定によってようこそメールの言語が決まります。

1. ページ上部の「**[!UICONTROL Save and Continue Edit]**」をクリックします。

   >[!INFO]
   >
   >顧客アカウントを保存すると、すべてのオプションが左側のパネルとページ上部のメニューに表示されます。 「_[!UICONTROL Customer View]_」タブには、アカウントの概要が表示されます。

   ![&#x200B; 顧客ビュー &#x200B;](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### 手順 2：アドレス情報の入力

1. 左パネルで「**[!UICONTROL Addresses]**」を選択し、「**[!UICONTROL Add New Addresses]**」をクリックします。

1. 請求と発送の両方に同じ住所が使用されている場合は、両方のオプションを切り替えます。

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![&#x200B; 顧客の住所情報の追加 &#x200B;](assets/information-addresses.png){width="600" zoomable="yes"}

1. 下にスクロールして、2 番目の列の必須のアドレスフィールドに入力します。

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. この住所の **[!UICONTROL Phone Number]** を入力してください。

1. 該当する場合は、顧客に関連付けられている **[!UICONTROL VAT Number]** を入力します。

1. このアドレスがアカウントに必要な唯一のアドレスである場合は、[**[!UICONTROL Save]**] をクリックします。

   それ以外の場合は、「**[!UICONTROL Save and Continue Edit]**」をクリックし、前の手順を繰り返してアドレスを追加します。

   新しいアドレスが [!UICONTROL Addresses] ページに表示され、選択した _[!UICONTROL Default Billing]_&#x200B;と&#x200B;_[!UICONTROL Default Shipping]_ アドレスが完全なリストの上に表示されます。

   ![&#x200B; アドレス表示 &#x200B;](assets/address-list.png){width="600" zoomable="yes"}

### 手順 3：パスワードのリセット

管理者から作成された顧客アカウントには、最初にパスワードが割り当てられていません。

1. グリッドで新しい顧客アカウントを見つけます。

1. _[!UICONTROL Action]_&#x200B;列の「**[!UICONTROL Edit]**」をクリックします。

1. ページ上部のメニューバーで、[**[!UICONTROL Reset Password]**] をクリックします。

1. パスワードの設定手順を記載した通知がアカウント所有者に送信されます。

## ボタンバー

プロファイルを初めて保存するときに、追加のボタンが使用可能になります。 詳しくは、[&#x200B; 顧客プロファイルの更新 &#x200B;](../customers/update-account.md) を参照してください。

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに _[!UICONTROL Customers]_&#x200B;ページに戻ります。 |
| **[!UICONTROL Delete Customer]** | 現在の顧客を削除します。 顧客に関連付けられている完了済み注文は削除されません。 |
| **[!UICONTROL Reset]** | 顧客フォーム内の未保存の変更をすべて以前の値にリセットします。 |
| **[!UICONTROL Create Order]** | 顧客の注文を作成します。 |
| **[!UICONTROL Reset Password]** | [&#x200B; パスワードのリセット &#x200B;](../customers/password-reset.md) リンクをメールでお客様に送信します。 |
| **[!UICONTROL Force Sign-in]** | 顧客アカウントに関連付けられている OAuth アクセストークンを失効させます。 この関数は、web API[&#x200B; 統合 &#x200B;](../systems/integrations.md) の一部として OAuth トークンが割り当てられている顧客アカウントでのみ使用できます。 詳しくは、開発者ドキュメントの [OAuth ベースの認証 &#x200B;](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) を参照してください。 |
| **[!UICONTROL Manage Shopping Cart]** | 管理者は、顧客の買い物かごを管理できます。 |
| **[!UICONTROL Save and Continue Edit]** | 変更を保存し、顧客プロファイルを開いたままにします。 |
| **[!UICONTROL Save Customer]** | 変更を保存し、顧客プロファイルを閉じます。 |

{style="table-layout:auto"}

## フィールドの説明

### [!UICONTROL Account Information]

| フィールド | 説明 |
|--- |--- |
| **[!UICONTROL Associate to Website]** | 顧客アカウントに関連付けられている web サイトを識別します。 |
| **[!UICONTROL Group]** | 顧客がメンバーである [&#x200B; 顧客グループ &#x200B;](../customers/customer-groups.md) を識別します。 該当する場合は、チェックボックスを選択して、VAT に基づく自動グループ変更を無効にします。 |
| **[!UICONTROL Name Prefix]** | 使用する場合は、顧客の名前に関連付けられたプレフィックス（Mr.、Ms.、Dr.など）。 プレフィックスの値は [configuration](../configuration-reference/customers/customer-configuration.md) によって決まります。 設定に応じて、入力コントロールはテキストフィールドまたはオプションのリストになります。 |
| **[!UICONTROL First Name]** | 顧客の名。 |
| **[!UICONTROL Middle Name / Initial]** | 顧客のミドルネームまたはイニシャル。 このフィールドは、[configuration](../configuration-reference/customers/customer-configuration.md) トピックで指定した場合にのみ含まれます。 |
| **[!UICONTROL Last Name]** | 顧客の姓。 |
| **[!UICONTROL Name Suffix]** | 使用する場合、顧客の名前に関連付けられたサフィックス （Jr.、Sr.、III など）。 サフィックスの値は [configuration](../configuration-reference/customers/customer-configuration.md) によって決まります。 設定に応じて、入力コントロールはテキストフィールドまたはオプションのドロップダウンリストになります。 |
| **[!UICONTROL Email]** | 顧客の電子メールアドレス。 |
| **[!UICONTROL Date of Birth]** | 顧客の生年月日。 [configuration](../configuration-reference/customers/customer-configuration.md) トピックで指定されている場合は、生年月日が含まれます。 <br><br> 現在のセキュリティおよびプライバシーのベストプラクティスに従い、顧客の完全な生年月日（月、日、年）を他の個人識別子と保存することに関連して、法的およびセキュリティ上の潜在的なリスクがあることを認識しておいてください。 顧客の完全な生年月日の保存を制限し、代替として顧客の生年月日の使用を提案することをお勧めします。 |
| **[!UICONTROL Tax / VAT Number]** | 顧客の税金または付加価値税番号（該当する場合）。 |
| **[!UICONTROL Gender]** | 顧客の性別を識別します。 性別は [configuration](../configuration-reference/customers/customer-configuration.md) で指定されている場合に含まれます。 オプション：`Male`/`Female`/`Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | 複数のストア表示がある場合、この設定によって、ようこそメッセージの送信元となるストア表示が識別されます。 異なる言語でストア表示を使用する場合は、この設定によってようこそメールの言語が決まります。 |

### [!UICONTROL Addresses]

| フィールド | 説明 |
|--- |--- |
| **[!UICONTROL New Addresses]** | 新しいアドレスのタイプを識別します。 オプション：`Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | 入力する住所の種類を識別する別の [ 新しい住所 ] セクションを表示します。 |
| **[!UICONTROL Company]** | この住所に該当する場合は、会社名。 |
| **[!UICONTROL Street Address]** | 顧客の住所。 [configuration](../configuration-reference/customers/customer-configuration.md) トピックで指定されている場合は、住所の 2 行目を使用できます。 |
| **[!UICONTROL City]** | 顧客の住所がある市区町村。 |
| **[!UICONTROL Country]** | 顧客の住所がある国。 |
| **[!UICONTROL State/Province]** | 顧客の住所がある都道府県。 |
| **[!UICONTROL Zip/Postal Code]** | 顧客の住所の郵便番号。 |
| **[!UICONTROL Phone Number]** | 住所に関連付けられている顧客の電話番号。 |
| **[!UICONTROL VAT Number]** | 該当する場合、この住所の顧客に適用される付加価値税番号。 |
