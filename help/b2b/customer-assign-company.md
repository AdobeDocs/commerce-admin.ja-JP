---
title: 会社アカウントへのユーザーの追加
description: 既存の顧客を会社アカウントに追加する方法について説明します。
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# 会社アカウントへのユーザーの追加

設定で有効にした場合、会社の管理者がストアフロントから会社のユーザーを追加して管理します。 ただし、会社ユーザーのアカウントは、管理者から追加および管理することもできます。

必要に応じて、1 人のユーザーを複数の会社に割り当てることができます。 例えば、B2B 購入者が複数の会社をサポートしている場合、取引するすべての会社にユーザーアカウントを追加できます。 ストアフロントでは、複数の会社に割り当てられているバイヤーは、*[!UICONTROL Company]* のメニューで利用可能な会社から選択して、会社アカウントを切り替えることができます。

![&#x200B; 会社への関連付け &#x200B;](./assets/company-assign-multi-switcher.png){width="700"}

>[!NOTE]
>
>個人が既にストアに個人用アカウントを持っていて、後で会社に就職する場合は、その個人の個人用アカウントを会社に割り当てないでください。 代わりに、会社のメールアドレスを持つユーザーの会社ユーザーアカウントを作成します。

## 会社ユーザーを追加

会社ユーザーを追加する場合、ユーザーアカウントに最初に関連付ける会社がデフォルトの会社になります。

1. 管理サイドバーで、「**[!UICONTROL Customers > All Customers]**」に移動します。

1. 「**[!UICONTROL Add new customer]**」をクリックします。

1. 新しいアカウントを設定します。

   1. 「**[!UICONTROL Customer Active]**」切替スイッチを設定して、初期アカウントステータスを指定します。

      オンにしてアカウントをすぐにアクティベートするか、無効にして非アクティブなアカウントを作成します。

   1. リストから web サイトの範囲を選 **[!UICONTROL Associate to Website]** します。

   1. **[!UICONTROL Associate to Company]** をクリックして、利用可能な会社を表示します。

      ![&#x200B; 会社への関連付け &#x200B;](./assets/company-assign-customer-account.png){width="675"}

      必要に応じて、会社名の最初の数文字を入力ボックスに入力して、リストをフィルタリングします。

   1. リストで、顧客を割り当てる 1 つ以上の会社を選択し、「**[!UICONTROL Done]**」をクリックします。

      会社ユーザーは、アカウントに関連付けられている会社ごとに、自動的に顧客グループ（または [&#x200B; 共有カタログ &#x200B;](catalog-shared.md)）に追加されます。

   1. 必要なユーザーアカウント情報 **[!UICONTROL First Name]**、**[!UICONTROL Last Name]**、および **[!UICONTROL Email]** を入力します。

   1. **[!UICONTROL Allow remote shopping assistance]** を有効にして、営業担当者がお客様に代わってストアフロントにログインすることを許可します。

   1. 「」をクリックして変更を適用 **[!UICONTROL Save Customer]** ます。

      ![&#x200B; 会社割り当てを使用した顧客グリッド &#x200B;](./assets/company-assign-user-assignments.png){width="675"}

[!UICONTROL Customers grid] の図は、ユーザーが割り当てられている会社ごとに別々の行を示しています。 次の列が更新されます。

- _[!UICONTROL Customer Type]_&#x200B;の列が更新され、ユーザーに割り当てられた役割が表示されます。

  顧客が会社に初めて割り当てられた場合、_[!UICONTROL Customer Type]_&#x200B;の列が&#x200B;_[!UICONTROL Individual user]_ から _[!UICONTROL Company User]_&#x200B;に更新されます。

- _[!UICONTROL Group]_&#x200B;の列は、会社に割り当てられている顧客グループ（または共有カタログ）の名前に変わります。

- _[!UICONTROL Company]_&#x200B;の列には、顧客プロファイルが関連付けられた会社の名前が表示されます。

## ユーザーを 1 つ以上の会社アカウントに割り当てる

新しいユーザーを割り当てる際に、ユーザーアカウントに最初に関連付ける会社がデフォルトの会社になります。

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL All Customers]** に移動します。

1. グリッドで顧客を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

1. 左側のパネルで「**[!UICONTROL Account Information]**」を選択します。

1. **[!UICONTROL Associate to Company]** リストから、会社ユーザーに割り当てる 1 つ以上の会社を選択し、「**[!UICONTROL Done]**」をクリックします。

1. 「」をクリックして変更を適用 **[!UICONTROL Save Customer]** ます。

## ユーザーアカウントから会社の割り当てを削除

ユーザープロファイルから会社を削除すると、その会社へのユーザーアクセスが無効になります。 ユーザーデータは、管理者で引き続きアクセスできます。 すべての会社の割り当てを削除すると、_[!UICONTROL Customer Type]_&#x200B;がアカウントの B2B 機能の無効化&#x200B;*[!UICONTROL Individual user]*&#x200B;に変わります。

1. 管理者の顧客グリッドで、更新する顧客プロファイルを編集します。

1. 「*[!UICONTROL Account Information]」セクションで、会社名のラベルの **[!UICONTROL X]** をクリックして、割り当てられた会社を「**[!UICONTROL Associate to Company]**」フィールドから削除します。

1. 「」をクリックして変更を適用 **[!UICONTROL Save Customer]** ます。

>[!NOTE]
>
>会社ユーザーが会社の管理者として割り当てられている場合、会社アカウントを更新して新しい会社の管理者を割り当てるまで、このユーザーから会社の関連付けを行うことはできません。
