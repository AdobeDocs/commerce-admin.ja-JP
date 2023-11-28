---
title: 顧客がオンラインになりました
description: '[_Now Online_] オプション ( [!UICONTROL Customers ]メニューには、ストアで現在オンラインになっているすべての顧客と訪問者が表示されます。'
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# 顧客がオンラインになりました

The **[!UICONTROL Now Online]** オプションを [!DNL Customers] メニューには、ストアで現在オンラインになっているすべての顧客と訪問者が表示されます。 顧客が現在オンラインとして表示される時間間隔は、設定で設定され、 [!DNL Customer's] アクティビティは、管理者から表示されます。 デフォルトでは、間隔は 15 分です。 この間にキーボードを使用しなかった場合、セッションは終了し、顧客は買い物を続行するにはアカウントに再度サインインする必要があります。 買い物かごの内容は後でアクセスできるように保存されることに注意する必要があります。

![オンライン顧客](assets/customers-now-online.png){width="700" zoomable="yes"}

顧客のオンラインステータスは、顧客のログイン、登録、その他の状態変更イベントに対してのみ更新されます。 これには、製品の追加、削除、変更など、買い物かご関連のイベントが含まれます。

>[!NOTE]
>
>ページ訪問のみでは、顧客のオンラインステータスは更新されません。 このような情報を収集するには、次の手順を実行することをお勧めします。 [Google Analytics](../merchandising-promotions/google-analytics.md) ( 単独で、または [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) またはAdobe Commerceで他の analytics ソフトウェアを使用する必要があります。

## 現在オンラインになっているすべての顧客を見る

次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>オンライン顧客が購入を完了するのを支援する方法について詳しくは、 [買い物支援](../stores-purchase/introduction.md#shopping-assistance).

## 時間間隔の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Online Customers Options]** 」セクションで次の操作を実行します。

   ![オンライン顧客オプション](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - の場合 **[!UICONTROL Online Minutes Interval]**」に、顧客セッションが管理者に表示されるまでの時間（分）を入力します。 デフォルトの間隔（15 分）を受け入れるには、このフィールドを空のままにします。

   - の場合 **[!UICONTROL Customer Data Lifetime]**、顧客が入力した未保存のデータの有効期限が切れるまでの時間（分）を入力します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 列の説明

| 列 | 説明 |
| --- | --- |
| **[!UICONTROL ID]** | 登録顧客の顧客 ID。 |
| **[!UICONTROL First Name]** | 登録顧客の名。 |
| **[!UICONTROL Last Name]** | 登録済み顧客の姓。 |
| **[!UICONTROL Email]** | 登録顧客の電子メールアドレス。 |
| **[!UICONTROL Last Activity]** | ストアでの顧客の最後のアクティビティの日時。 |
| **[!UICONTROL Type]** | オプション： `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | 顧客が最後に訪問した URL。 |
| **[!UICONTROL Company]** | ユーザーが属する会社の名前。 |

{style="table-layout:auto"}
