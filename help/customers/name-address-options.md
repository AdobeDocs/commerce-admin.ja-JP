---
title: 顧客名および住所のオプション
description: 顧客名および住所オプションは、名前および住所フォームに含まれるフィールドを決定します。
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# 顧客名および住所のオプション

この _名前と住所のオプション_ 顧客がを作成する際に、名前および住所フォームに含めるフィールドを決定します [アカウント](../customers/account-create.md) あなたの店で。

![顧客アカウントの新規登録フォーム](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

名前とアドレスのオプションを設定する手順は、Adobe CommerceとMagento Open Sourceでは異なります。

## Adobe Commerceの名前とアドレスのオプションを設定

アカウントの作成時にストアフロントで顧客に提示される名前と住所のオプションを設定できます。

### 手順 1：設定の範囲を設定する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Name and Address Options]** セクション。

   >[!INFO]
   >
   >name オプションと address オプションの範囲は、に適用されます。 `website` レベル。

1. ページの上部までスクロールし、設定の範囲を次のいずれかに設定します。

   - `Default Config`
   - `Main Website` （またはマルチサイトインストール用の特定のサイト）

   >[!INFO]
   >
   >この _[!UICONTROL Name and Address Options]_範囲がに設定されている場合、セクションが表示されない `Default Store View`.

   ![構成スコープ](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### 手順 2：名前とアドレスのオプションを設定する

1. に戻る [!UICONTROL _名前と住所のオプション_] このセクションは、顧客設定ページにあります。

   >[!INFO]
   >
   > を使用していない場合 `Default config` スコープの設定をクリアする必要があります `Use Default` 値を変更する前の各フィールドのチェックボックス。

   ![名前と住所のオプション](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Prefix Dropdown Options]**&#x200B;リストに表示する各接頭辞をセミコロンで区切って入力します。

   >[!IMPORTANT]
   >
   >最初の値の前にセミコロンを入れると、リストの先頭に空白の値が表示されます。

1. の場合 **[!UICONTROL Suffix Dropdown Options]**&#x200B;リストに表示する各サフィックスをセミコロンで区切って入力します。

1. 以下のフィールドを顧客フォームに含めるには、それぞれの値を次のように設定します。 `Optional` または `Required`、必要に応じて。

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### 手順 3：保存と更新

1. 完了したら、 **[!UICONTROL Save Config]**.

1. ページ上部のメッセージで、 **[!UICONTROL Cache Management]** および [更新](../systems/cache-management.md) それぞれの無効なキャッシュ。

## Magento Open Sourceの名前とアドレスのオプションを設定

アカウントの作成時にストアフロントで顧客に提示する名前および住所のオプションを設定します。

![顧客アカウントの新規登録フォーム](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### 手順 1：設定の範囲を設定する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Name and Address Options]** セクション。

   >[!IMPORTANT]
   >
   > name オプションと address オプションの範囲は、に適用されます。 `website` レベル。

   ![名前と住所のオプション](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. ページの上部までスクロールして戻り、設定の範囲を次のいずれかに設定します。

   - `Default Config`
   - `Main Website` （またはマルチサイトインストール用の特定のサイト）

   >[!NOTE]
   >
   >この _名前と住所のオプション_ 範囲がに設定されている場合、セクションが表示されない `Default Store View`.

   ![構成スコープ](assets/configuration-scope.png){width="600" zoomable="yes"}

### 手順 2：名前とアドレスのオプションを設定する

1. に戻る [!UICONTROL _名前と住所のオプション_] このセクションは、顧客設定ページにあります。

   >[!INFO]
   >
   >を使用していない場合 `Default config` スコープの設定をクリアする必要があります `Use Default` 値を変更する前の各フィールドのチェックボックス。

1. の場合 **番地の行数**&#x200B;は、1～4 の数字を入力します。

   >[!WARNING]
   >
   >デフォルトでは、住所は 3 行です。

1. プレフィックス（Mr や Ms など）を名前の一部として含めるには、を設定します **プレフィックスを表示** 対象： `Yes`.

   ![顧客登録フォームのプレフィックス](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >の場合 **プレフィックス ドロップダウンオプション**&#x200B;リストに表示する各接頭辞をセミコロンで区切って入力します。 最初の値の前にセミコロンを付けると、リストの先頭に空白の値が表示されます。

1. 顧客のミドルネームまたはイニシャルのオプションフィールドを含めるには、次のように設定します **[!UICONTROL Show Middle Name (initial)]** 対象： `Yes`.

1. 接尾辞（Jr など）を含めるには または Sr.）を設定します。 **[!UICONTROL Show Suffix]** を次のいずれかに変更します。

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >の場合 **接尾辞ドロップダウンオプション**&#x200B;リストに表示する各サフィックスをセミコロンで区切って入力します。 最初の値の前にセミコロンを付けると、リストの先頭に空白の値が表示されます。

1. 生年月日を含めるには、次のように設定します **[!UICONTROL Show Date of Birth]** を次のいずれかに変更します。

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >現在のセキュリティおよびプライバシーのベストプラクティスに従い、顧客の完全な生年月日（月、日、年）を他の個人識別子と保存することに関連して、法的およびセキュリティ上の潜在的なリスクがあることを認識しておいてください。 顧客の完全な生年月日の保存を制限し、代替として顧客の生年月日の使用を提案することをお勧めします。

   顧客はフィールドの後にカレンダーアイコンを使用して、ポップアップカレンダーから生年月日を選択できます。

   ![顧客のサインアップフォームでの生年月日](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. 顧客が税金を入力できるようにする手順は、次のとおりです。 [VAT](../stores-purchase/vat.md) 数値，セット **[!UICONTROL Show Tax/VAT Number]** を次のいずれかに変更します。

   - `Optional`
   - `Required`

1. 顧客フォームに性別フィールドを含めるには、次のように設定します **[!UICONTROL Show Gender]** を次のいずれかに変更します。

   - `Optional`
   - `Required`

   ![カスタマー登録フォームの性別オプション](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. 以下のフィールドを顧客フォームに含めるには、それぞれの値を次のように設定します。 `Optional` または `Required`、必要に応じて。

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### 手順 3：保存と更新

1. 完了したら、 **[!UICONTROL Save Config]**.

1. ページ上部のメッセージで、 **[!UICONTROL Cache Management]** および [更新](../systems/cache-management.md) それぞれの無効なキャッシュ。
