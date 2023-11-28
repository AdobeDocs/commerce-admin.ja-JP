---
title: 顧客名と住所のオプション
description: 顧客名と住所のオプションによって、名前フォームと住所フォームに含めるフィールドが決まります。
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# 顧客名と住所のオプション

The _名前と住所のオプション_ 顧客が [アカウント](../customers/account-create.md) お客様のストアに置き換えます。

![顧客アカウントのサインアップフォーム](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

名前とアドレスのオプションを設定する手順は、Adobe CommerceとMagento Open Sourceで異なります。

## Adobe Commerceの名前と住所のオプションを設定

ストアフロントで顧客がアカウントを作成する際に表示する名前と住所のオプションを設定できます。

### 手順 1：設定の範囲を設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Name and Address Options]** 」セクションに入力します。

   >[!INFO]
   >
   >名前とアドレスのオプションの範囲は、 `website` レベル。

1. ページの上部までスクロールし、設定の範囲を次のいずれかに設定します。

   - `Default Config`
   - `Main Website` （マルチサイトインストールの場合は特定のサイト）

   >[!INFO]
   >
   >The _[!UICONTROL Name and Address Options]_範囲が `Default Store View`.

   ![設定範囲](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### 手順 2：名前と住所のオプションを設定する

1. に戻ります。 [!UICONTROL _名前と住所のオプション_] を参照してください。

   >[!INFO]
   >
   > を使用しない場合、 `Default config` 範囲の設定を行う場合は、 `Use Default` チェックボックスをオンにしてから値を変更してください。

   ![名前と住所のオプション](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Prefix Dropdown Options]**」では、リストに表示する各プレフィックスをセミコロンで区切って入力します。

   >[!IMPORTANT]
   >
   >最初の値の前にセミコロンを配置して、リストの先頭に空白の値を表示します。

1. の場合 **[!UICONTROL Suffix Dropdown Options]**&#x200B;を使用する場合は、リストに表示する各サフィックスをセミコロンで区切って入力します。

1. 次のフィールドを顧客フォームに含めるには、それぞれの値を `Optional` または `Required`必要に応じて。

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### 手順 3：保存して更新

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. ページ上部のメッセージで、「 **[!UICONTROL Cache Management]** および [更新](../systems/cache-management.md) 各無効なキャッシュ

## Magento Open Sourceの名前とアドレスのオプションを設定

ストアフロントで顧客がアカウントを作成する際に表示する名前と住所のオプションを設定します。

![顧客アカウントのサインアップフォーム](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### 手順 1：設定の範囲を設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Name and Address Options]** 」セクションに入力します。

   >[!IMPORTANT]
   >
   > 名前とアドレスのオプションの範囲は、 `website` レベル。

   ![名前と住所のオプション](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. ページの上部までスクロールし、設定の範囲を次のいずれかに設定します。

   - `Default Config`
   - `Main Website` （マルチサイトインストールの場合は特定のサイト）

   >[!NOTE]
   >
   >The _名前と住所のオプション_ 範囲が `Default Store View`.

   ![設定範囲](assets/configuration-scope.png){width="600" zoomable="yes"}

### 手順 2：名前と住所のオプションを設定する

1. に戻ります。 [!UICONTROL _名前と住所のオプション_] を参照してください。

   >[!INFO]
   >
   >を使用しない場合、 `Default config` 範囲の設定を行う場合は、 `Use Default` チェックボックスをオンにしてから値を変更してください。

1. の場合 **番地内の行数**、1 ～ 4 の数値を入力します。

   >[!WARNING]
   >
   >既定では、番地は 3 行です。

1. 名前の一部にプレフィックス（Mr.や Ms.など）を含めるには、 **プレフィックスを表示** から `Yes`.

   ![顧客サインアップフォームのプレフィックス](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >の場合 **プレフィックスドロップダウンオプション**」では、リストに表示する各プレフィックスをセミコロンで区切って入力します。 最初の値の前にセミコロンを配置して、リストの先頭に空白の値を表示できます。

1. 顧客のミドルネームまたはイニシャル用のオプションのフィールドを含めるには、 **[!UICONTROL Show Middle Name (initial)]** から `Yes`.

1. サフィックス (Jr. または Sr.) を顧客名の後に追加し、 **[!UICONTROL Show Suffix]** を次のいずれかに変更します。

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >の場合 **サフィックスドロップダウンオプション**&#x200B;を使用する場合は、リストに表示する各サフィックスをセミコロンで区切って入力します。 最初の値の前にセミコロンを配置して、リストの先頭に空白の値を表示できます。

1. 生年月日を含めるには、 **[!UICONTROL Show Date of Birth]** を次のいずれかに変更します。

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >現在のセキュリティおよびプライバシーのベストプラクティスに従って、顧客の生年月日（月、日、年）と他の個人識別子を含むストレージに関連する、法的リスクおよびセキュリティリスクの可能性を認識しておきます。 顧客の完全な生年月日の保存を制限し、顧客の生年月日を代替として使用することをお勧めします。

   フィールドの後にあるカレンダーアイコンを使用して、ポップアップカレンダーから生年月日を選択できます。

   ![顧客登録フォームの生年月日](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. 顧客に税金の入力を許可する手順は、次のとおりです。 [VAT](../stores-purchase/vat.md) 数値，設定 **[!UICONTROL Show Tax/VAT Number]** を次のいずれかに変更します。

   - `Optional`
   - `Required`

1. 顧客フォームに性別のフィールドを含めるには、 **[!UICONTROL Show Gender]** を次のいずれかに変更します。

   - `Optional`
   - `Required`

   ![顧客の新規登録フォームの性別オプション](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. 次のフィールドを顧客フォームに含めるには、それぞれの値を `Optional` または `Required`必要に応じて。

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### 手順 3：保存して更新

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. ページ上部のメッセージで、「 **[!UICONTROL Cache Management]** および [更新](../systems/cache-management.md) 各無効なキャッシュ
