---
title: 顧客アカウントの範囲
description: 顧客アカウントの範囲は、アカウントが作成された web サイトに限定することも、ストア階層内のすべての web サイトやストアと共有することもできます。
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# 顧客アカウントの範囲

ストア内のすべてのページのヘッダーに、買い物客がストアのアカウントを _ログインまたは登録_ するための招待が拡張されます。 アカウントを開設するお客様には、次のような様々なメリットがあります。

* **顧客アカウントの作成** – 訪問者は、ストアフロントを登録顧客として使用できるように顧客アカウントを作成できます。
* **会社アカウントの作成** 設定に応じて、ストアへの訪問者は会社アカウントの作成を選択できます。 詳しくは、[Adobe Commerce B2B](../b2b/introduction.md) を参照してください。
* **迅速なチェックアウト** – 多くの情報が既にアカウントに存在するので、登録済みの顧客はチェックアウトをより迅速に進めることができます。
* **セルフサービス** – 登録されたお客様は、情報の更新、注文のステータスの確認、アカウントからの並べ替えなどを行うことができます。

顧客は、ストアのヘッダーにある **[!UICONTROL My Account]** リンクをクリックしてアカウントにアクセスできます。 顧客は自分のアカウントから、過去や現在の住所、請求や配送の環境設定、ニュースレターの購読、ウィッシュリストなどの情報を表示および変更できます。

![&#x200B; マイアカウント &#x200B;](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## 顧客アカウントの範囲の設定

顧客アカウントの範囲は、アカウントが作成された web サイトに限定することも、ストア階層内のすべての web サイトやストアと共有することもできます。

>[!NOTE]
>
>Web サイトを顧客グループから除外した場合、顧客アカウントの範囲を Web サイトに限定したり、すべての Web サイトと共有したりすると、顧客は Web サイトにログインできなくなります。 Web サイトをグループから除外する方法について詳しくは、[&#x200B; 顧客グループの作成 &#x200B;](customer-groups.md#create-a-customer-group) を参照してください。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/[!UICONTROL _[!UICONTROL Settings]_]/**[!UICONTROL Configuration]** に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Customer Configuration]**」を選択します。

1. 「**[!UICONTROL Account Sharing Options]**」セクションを展開します。

   ![&#x200B; アカウント共有オプション &#x200B;](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Share Customer Accounts]** を次のいずれかに設定します。

   | オプション | 説明 |
   | --- | --- |
   | `Global` | 顧客アカウント情報をインストール内のすべての web サイトおよびストアと共有します。 |
   | `Per Website` | 顧客のアカウント情報を、そのアカウントが作成された web サイトに制限します。 |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > 必要に応じて、「**[!UICONTROL User system value]**」チェックボックスをオフにして変更を加えます。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

   >[!NOTE]
   >
   >`Global` を選択すると、**マイアカウント** の顧客情報（住所と連絡先詳細などのアカウント情報）が共有されます。
