---
title: 個々の顧客アカウントの作成
description: 訪問者は、個々の顧客アカウントを簡単に作成して、購入を管理できます。
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# 個々の顧客アカウントの作成

ストアの訪問者は、アカウントを開いて購入やアクティビティを管理できます。 顧客は通常、自分のアカウントをストアから作成します。 ただし、管理者から直接顧客アカウントを作成することもできます。これは、電話で顧客をサポートするのに役立ちます。

次の手順は、デフォルトの顧客アカウント設定を表しています。 フォーム内の一部のフィールドの選択と動作を変更するには、 [顧客アカウントの設定](../customers/customer-account-scope.md).

ストア管理者は、 [新しいアカウントオプション](../customers/account-options-new.md) をクリックして、新規登録済み顧客に確認メールを送信します。これは、登録済みアカウントが有効であることを確認するのに役立ちます。

{{beta-updates}}

## ストアフロントからアカウントを作成

ストアの顧客がストアフロントにアカウントを作成します。

1. ストアフロントで、「 」をクリックします。 **[!UICONTROL Create an Account]** をクリックします。

   ![アカウントの作成](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. の下 **[!UICONTROL Personal Information]**&#x200B;を **[!UICONTROL First Name]** および **[!UICONTROL Last Name]**.

   ![個人情報](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. ニュースレター購読者のリストに自分の名前と E メールアドレスを追加する場合は、顧客が **[!UICONTROL Sign Up for Newsletter]** チェックボックス。

   >[!INFO]
   >
   > このオプションは、ストアがニュースレターを公開しない場合でも表示されます。

1. ストアサポートスタッフに [何が見えるかを見る](../customers/login-as-customer.md) リモート・アシスタンスを提供し、お客様が **[!UICONTROL Allow remote shopping assistance]** チェックボックス。

1. の下 **[!UICONTROL Sign-in Information]**&#x200B;を **[!UICONTROL Email]** 住所。

   >[!INFO]
   >
   > この電子メールアドレスはサインイン資格情報に含まれ、他の顧客アカウントと関連付けることはできません。

   ![サインイン情報](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. 次の項目に入る **[!UICONTROL Password]** には、次の 3 種類の情報が含まれます。

   - 小文字
   - 大文字
   - 数値
   - 特殊文字

   押した後 **[!UICONTROL Enter]**&#x200B;の場合、パスワードの強度が評価され、フィールドの下に表示されます。 パスワードが _弱い_、次のように評価されるまで別の操作を試します： _強_.

   ![堅牢なパスワードをお勧めします](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. 次に、顧客が再度 **[!UICONTROL Confirm Password]**.

1. 必要に応じて、クリックします。 **[!UICONTROL Show Password]** をクリックして、入力したパスワードを表示します。

1. 完了したら、「 」をクリックします **アカウントの作成**.

その後、顧客は電子メールアドレスとパスワードを [サインイン](../customers/customer-sign-in.md) をアカウントに追加し、住所情報を入力します。

## 管理者からのアカウントの作成

マーチャントは、管理者から顧客アカウントを作成できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. クリック **[!UICONTROL Add New Customer]**.

### 手順 1：アカウント情報の入力

![顧客情報](assets/new-information.png){width="700" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Account Information]** セクションで、以下の操作を実行します。

   - マルチサイトインストールの場合は、 **[!UICONTROL Associate to Website]** 顧客アカウントが適用される Web サイトに追加します。
   - 該当する場合は、顧客を別の **[!UICONTROL Customer Group]**.
   - を使用している場合、 [VAT ID の検証](../stores-purchase/vat.md) また、 **[!UICONTROL Disable Automatic Group Change Based on VAT ID]**、チェックボックスを選択します。

1. 次の必須フィールドに入力します。

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
   >現在のセキュリティおよびプライバシーのベストプラクティスに従って、顧客の生年月日（月、日、年）と他の個人識別子を含むストレージに関連する、法的リスクおよびセキュリティリスクの可能性を認識しておきます。 顧客の完全な生年月日の保存を制限することをお勧めします。また、別の方法として、顧客の生年を使用することをお勧めします。

1. 設定 **[!UICONTROL Send Welcome Email From]** をストア表示に追加します。 _ようこそ_ メールが送信されます。

   >[!INFO]
   >
   > ストアのビューが異なる場合 [言語](../stores-purchase/store-localize.md)に設定すると、「ようこそ」の電子メールの言語が決まります。

1. クリック **[!UICONTROL Save and Continue Edit]** をクリックします。

   >[!INFO]
   >
   >顧客アカウントが保存されると、左側のパネルとページ上部のメニューに、すべてのオプションが表示されます。 The _[!UICONTROL Customer View]_「 」タブには、アカウントの概要が表示されます。

   ![顧客ビュー](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### 手順 2：住所情報の入力

1. 左側のパネルで、を選択します。 **[!UICONTROL Addresses]** をクリックします。 **[!UICONTROL Add New Addresses]**.

1. 請求と送料の両方に同じ住所が使用されている場合は、両方のオプションを切り替えます。

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![顧客住所情報の追加](assets/information-addresses.png){width="600" zoomable="yes"}

1. 下にスクロールし、2 列目の必須アドレスフィールドに入力します。

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. 次を入力します。 **[!UICONTROL Phone Number]** このアドレスに対して。

1. 該当する場合は、 **[!UICONTROL VAT Number]** 顧客と関連付けられている。

1. アカウントに必要なアドレスがこのアドレスのみの場合は、 **[!UICONTROL Save]**.

   それ以外の場合は、「 **[!UICONTROL Save and Continue Edit]** 上記の手順を繰り返して、アドレスを追加します。

   新しいアドレスが [!UICONTROL Addresses] 選択したページ _[!UICONTROL Default Billing]_および_[!UICONTROL Default Shipping]_ アドレスが完全なリストの上に表示されます。

   ![アドレス表示](assets/address-list.png){width="600" zoomable="yes"}

### 手順 3：パスワードのリセット

管理者から作成された顧客アカウントには、最初はパスワードが割り当てられていません。

1. グリッドで新しい顧客アカウントを見つけます。

1. クリック **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. ページ上部のメニューバーで、 **[!UICONTROL Reset Password]**.

1. パスワードの設定手順と共に、アカウント所有者に通知が送信されます。

## ボタンバー

プロファイルを初めて保存すると、追加のボタンが使用できるようになります。 詳しくは、 [顧客プロファイルの更新](../customers/update-account.md).

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | に戻ります。 _[!UICONTROL Customers]_変更を保存せずにページを保存できます。 |
| **[!UICONTROL Delete Customer]** | 現在の顧客を削除します。 顧客に関連付けられた完了済みの注文は削除されません。 |
| **[!UICONTROL Reset]** | 顧客フォームに保存されていない変更を以前の値にリセットします。 |
| **[!UICONTROL Create Order]** | 顧客の注文を作成します。 |
| **[!UICONTROL Reset Password]** | を送信します。 [パスワードをリセット](../customers/password-reset.md) 電子メールで顧客にリンク。 |
| **[!UICONTROL Force Sign-in]** | 顧客アカウントに関連付けられている OAuth アクセストークンを取り消します。 この関数は、Web API の一部として OAuth トークンを割り当てた顧客アカウントでのみ使用できます [統合](../systems/integrations.md). 詳しくは、 [OAuth ベースの認証](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) （開発者向けドキュメント）。 |
| **[!UICONTROL Manage Shopping Cart]** | 管理者が顧客の買い物かごを管理できるようにします。 |
| **[!UICONTROL Save and Continue Edit]** | 変更を保存し、顧客プロファイルを開いたままにします。 |
| **[!UICONTROL Save Customer]** | 変更を保存し、顧客プロファイルを閉じます。 |

{style="table-layout:auto"}

## フィールドの説明

### [!UICONTROL Account Information]

| フィールド | 説明 |
|--- |--- |
| **[!UICONTROL Associate to Website]** | 顧客アカウントに関連付けられている Web サイトを識別します。 |
| **[!UICONTROL Group]** | を識別します。 [顧客グループ](../customers/customer-groups.md) 顧客がメンバーである場所。 必要に応じて、VAT に基づく自動グループ変更を無効にする場合は、このチェックボックスを選択します。 |
| **[!UICONTROL Name Prefix]** | 使用する場合は、顧客の名前に関連付けられるプレフィックス（Mr.、Ms.、Dr.など）。 プレフィックスの値は、 [設定](../configuration-reference/customers/customer-configuration.md). 設定に応じて、入力コントロールは、テキストフィールドまたはオプションのリストになります。 |
| **[!UICONTROL First Name]** | 顧客の名。 |
| **[!UICONTROL Middle Name / Initial]** | 顧客のミドルネームまたはイニシャル。 このフィールドは、 [設定](../configuration-reference/customers/customer-configuration.md) トピック。 |
| **[!UICONTROL Last Name]** | 顧客の姓。 |
| **[!UICONTROL Name Suffix]** | 使用する場合は、顧客の名前に関連付けられるサフィックス（Jr.、Sr、III など）。 サフィックスの値は、 [設定](../configuration-reference/customers/customer-configuration.md). 設定に応じて、入力コントロールは、テキストフィールドまたはオプションのドロップダウンリストになります。 |
| **[!UICONTROL Email]** | 顧客の電子メールアドレス。 |
| **[!UICONTROL Date of Birth]** | 顧客の生年月日。 生年月日が [設定](../configuration-reference/customers/customer-configuration.md) トピック。 <br><br>現在のセキュリティおよびプライバシーのベストプラクティスに従って、顧客の生年月日（月、日、年）と他の個人識別子を含むストレージに関連する、法的リスクおよびセキュリティリスクの可能性を認識しておきます。 顧客の完全な生年月日の保存を制限し、顧客の生年月日を代替として使用することをお勧めします。 |
| **[!UICONTROL Tax / VAT Number]** | 該当する場合は、顧客の税金または付加価値税番号。 |
| **[!UICONTROL Gender]** | 顧客の性別を特定します。 性別は、 [設定](../configuration-reference/customers/customer-configuration.md). オプション： `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | 複数のストア表示がある場合、この設定は、ようこそメッセージの送信元のストア表示を識別します。 ストア表示が異なる言語で使用されている場合、この設定により、お知らせメールの言語が決まります。 |

### [!UICONTROL Addresses]

| フィールド | 説明 |
|--- |--- |
| **[!UICONTROL New Addresses]** | 新しいアドレスのタイプを識別します。 オプション： `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | 入力する住所の種類を識別する別の [ 新しい住所 ] セクションを表示します。 |
| **[!UICONTROL Company]** | 会社名（該当する場合）。 |
| **[!UICONTROL Street Address]** | 顧客の住所。 住所の 2 行目が [設定](../configuration-reference/customers/customer-configuration.md) トピック。 |
| **[!UICONTROL City]** | 顧客の住所がある市区町村。 |
| **[!UICONTROL Country]** | 顧客の住所がある国。 |
| **[!UICONTROL State/Province]** | 顧客の住所がある都道府県。 |
| **[!UICONTROL Zip/Postal Code]** | 顧客の住所がある場所の郵便番号。 |
| **[!UICONTROL Phone Number]** | 住所に関連付けられている顧客の電話番号。 |
| **[!UICONTROL VAT Number]** | 該当する場合、この住所で顧客に適用される付加価値税番号。 |
