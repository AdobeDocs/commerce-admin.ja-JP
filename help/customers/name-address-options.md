---
title: 顧客の名前と住所のオプション
description: 「顧客の名前」および「住所」オプションは、名前および住所フォームに含まれるフィールドを決定します。
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/qMXVcVWZJCrCNywOJF3psuO5vLWkNt9LoNtgFfFBzT8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 809
ht-degree: 0%

---

# 顧客の名前と住所のオプション

顧客がストアで[ アカウント ](../customers/account-create.md)を作成する際に、_名前と住所のオプション_&#x200B;によって、名前と住所のフォームに含まれるフィールドが決まります。

![顧客アカウント登録フォーム ](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

Adobe CommerceとMagento Open Sourceでは、名前と住所のオプションを設定する手順が異なります。

## Adobe Commerceの名前と住所のオプションの設定

ストアフロントで顧客がアカウントを作成したときに表示される名前と住所のオプションを設定できます。

### 手順1：設定の範囲の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Customer Configuration]**&#x200B;を選択します。

1. **[!UICONTROL Name and Address Options]** セクションを展開します。

   >[!INFO]
   >
   >名前と住所オプションの範囲は、`website` レベルで適用されます。

1. ページの上部までスクロールし、設定の範囲を次のいずれかに設定します。

   - `Default Config`
   - `Main Website` （またはマルチサイト インストール用の特定のサイト）

   >[!INFO]
   >
   >スコープが`Default Store View`に設定されている場合、_[!UICONTROL Name and Address Options]_セクションは表示されません。

   ![設定範囲](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### 手順2：名前と住所のオプションを設定する

1. 顧客設定ページの「[!UICONTROL _名前と住所オプション_]」セクションに戻ります。

   >[!INFO]
   >
   > `Default config` スコープ設定を使用していない場合は、値を変更する前に、各フィールドの`Use Default` チェックボックスをオフにする必要があります。

   ![名前と住所のオプション ](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. **[!UICONTROL Prefix Dropdown Options]**&#x200B;の場合、リストに表示する各プレフィックスをセミコロンで区切って入力します。

   >[!IMPORTANT]
   >
   >最初の値の前にセミコロンを配置して、リストの上部に空白の値を表示します。

1. **[!UICONTROL Suffix Dropdown Options]**&#x200B;には、リストに表示するサフィックスをそれぞれセミコロンで区切って入力します。

1. 顧客フォームに次のフィールドを含めるには、必要に応じて、それぞれの値を`Optional`または`Required`に設定します。

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### ステップ 3：保存して更新

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. ページ上部のメッセージで、無効なキャッシュごとに&#x200B;**[!UICONTROL Cache Management]**&#x200B;と[更新](../systems/cache-management.md)をクリックします。

## Magento Open Sourceの名前と住所のオプションの設定

ストアフロントで顧客がアカウントを作成したときに表示される名前と住所のオプションを設定します。

![顧客アカウント登録フォーム ](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### 手順1：設定の範囲の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Customer Configuration]**&#x200B;を選択します。

1. **[!UICONTROL Name and Address Options]** セクションを展開します。

   >[!IMPORTANT]
   >
   > 名前と住所オプションの範囲は、`website` レベルで適用されます。

   ![名前と住所のオプション ](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. ページの上部までスクロールし、設定の範囲を次のいずれかに設定します。

   - `Default Config`
   - `Main Website` （またはマルチサイト インストール用の特定のサイト）

   >[!NOTE]
   >
   >スコープが`Default Store View`に設定されている場合、_名前と住所のオプション_ セクションは表示されません。

   ![設定範囲](assets/configuration-scope.png){width="600" zoomable="yes"}

### 手順2：名前と住所のオプションを設定する

1. 顧客設定ページの「[!UICONTROL _名前と住所オプション_]」セクションに戻ります。

   >[!INFO]
   >
   >`Default config` スコープ設定を使用していない場合は、値を変更する前に、各フィールドの`Use Default` チェックボックスをオフにする必要があります。

1. **住所の行数**&#x200B;に、1 ～ 4の数値を入力します。

   >[!WARNING]
   >
   >デフォルトでは、住所は3行です。

1. 接頭辞（Mr.やMs.など）を含めるには 名前の一部として、**プレフィックスを表示**&#x200B;から`Yes`に設定します。

   ![顧客登録フォームの接頭辞](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >**プレフィックスドロップダウンオプション**&#x200B;に、リストに表示する各プレフィックスをセミコロンで区切って入力します。 最初の値の前にセミコロンを配置すると、リストの上部に空白の値を表示できます。

1. 顧客のミドルネームまたはイニシャルのオプション フィールドを含めるには、**[!UICONTROL Show Middle Name (initial)]**&#x200B;を`Yes`に設定します。

1. 接尾辞（Jrなど）を含めるには、 またはシニア） 顧客名の後に、**[!UICONTROL Show Suffix]**&#x200B;を次のいずれかに設定します。

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >「**サフィックス ドロップダウンオプション**」に、リストに表示する各サフィックスをセミコロンで区切って入力します。 最初の値の前にセミコロンを配置すると、リストの上部に空白の値を表示できます。

1. 生年月日を含めるには、**[!UICONTROL Show Date of Birth]**&#x200B;を次のいずれかに設定します。

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >現在のセキュリティとプライバシーのベストプラクティスに従って、顧客の生年月日（月、日、年）を他の個人識別子と保管することに関連する潜在的な法的およびセキュリティリスクを認識してください。 お客様の生年月日の保存を制限し、お客様の生年月日を代替手段として使用することをお勧めします。

   顧客は、フィールドの後にあるカレンダーアイコンを使用して、ポップアップカレンダーから生年月日を選択できます。

   ![お客様登録フォームの生年月日](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. お客様が税金または[VAT](../stores-purchase/vat.md)番号を入力できるようにするには、**[!UICONTROL Show Tax/VAT Number]**&#x200B;を次のいずれかに設定します。

   - `Optional`
   - `Required`

1. 顧客フォームに性別のフィールドを含めるには、**[!UICONTROL Show Gender]**&#x200B;を次のいずれかに設定します。

   - `Optional`
   - `Required`

   顧客サインアップフォームの![性別オプション ](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. 顧客フォームに次のフィールドを含めるには、必要に応じて、それぞれの値を`Optional`または`Required`に設定します。

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### ステップ 3：保存して更新

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. ページ上部のメッセージで、無効なキャッシュごとに&#x200B;**[!UICONTROL Cache Management]**&#x200B;と[更新](../systems/cache-management.md)をクリックします。
