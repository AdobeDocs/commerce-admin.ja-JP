---
title: 顧客アカウントの範囲
description: 顧客アカウントの範囲は、アカウントが作成された Web サイトに限定したり、ストア階層内のすべての Web サイトおよびストアと共有したりできます。
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 2541b2d55516e2a9c824825100c8348d81201ca9
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# 顧客アカウントの範囲

ストア内の各ページのヘッダーは、買い物客の招待状を _ログインまたは登録_ ストアのアカウントに対して。 アカウントを開設したお客様には、次のような様々な利点があります。

* **顧客アカウントの作成** ：訪問者はストアフロントを登録顧客として使用できるように、顧客アカウントを作成できます。
* **会社アカウントの作成** 設定に応じて、ストアの訪問者は会社アカウントの作成を選択できます。 詳しくは、 [Adobe Commerce用 B2B](../b2b/introduction.md).
* **迅速なチェックアウト**  — 既に多くの情報がアカウントに登録されているので、登録されたお客様の方がチェックアウトを迅速に進めることができます。
* **セルフサービス**  — 登録ユーザーは、情報の更新、注文状況の確認、アカウントの並べ替えを行うことができます。

顧客は、 **[!UICONTROL My Account]** リンクをストアのヘッダーに追加します。 顧客は、アカウントから、過去および現在のアドレス、請求および配送の環境設定、ニュースレターの購読、ウィッシュリストなどの情報を表示および変更できます。

![マイアカウント](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## 顧客アカウントの範囲の設定

顧客アカウントの範囲は、アカウントが作成された Web サイトに限定したり、ストア階層内のすべての Web サイトおよびストアと共有したりできます。

>[!NOTE]
>
>顧客グループから Web サイトを除外した場合、顧客アカウントの範囲が Web サイトに限定されている場合や、すべての Web サイトと共有されている場合、顧客は Web サイトにログインできません。 詳しくは、 [顧客グループの作成](customer-groups.md#create-a-customer-group) を参照してください。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Account Sharing Options]** 」セクションに入力します。

   ![アカウント共有オプション](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Share Customer Accounts]** を次のいずれかに変更します。

   | オプション | 説明 |
   | --- | --- |
   | `Global` | 顧客アカウント情報をすべての Web サイトと共有し、インストールに保存します。 |
   | `Per Website` | 顧客アカウント情報を、アカウントが作成された Web サイトに限定します。 |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > 必要に応じて、 **[!UICONTROL User system value]** 」チェックボックスをオンにして変更を加えます。

1. 完了したら、「 **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >条件 `Global` が **マイアカウント** （アドレスと連絡先の詳細などのアカウント情報）が共有されます。
