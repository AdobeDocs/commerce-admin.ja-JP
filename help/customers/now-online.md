---
title: 顧客がオンラインになりました
description: の_Now Online_ オプション [!UICONTROL Customers ]メニューには、ストアで現在オンラインになっているすべての顧客と訪問者が一覧表示されます。
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# 顧客がオンラインになりました

この **[!UICONTROL Now Online]** のオプション [!DNL Customers] メニューには、ストアで現在オンラインになっているすべての顧客と訪問者が一覧表示されます。 設定で、顧客に現在オンラインとして表示される時間間隔が設定され、この時間によって [!DNL Customer's] アクティビティは、管理者から表示されます。 デフォルトでは、間隔は 15 分です。 この間キーボードを使用しないと、セッションは終了します。顧客が買い物を続行するには、もう一度アカウントにログインする必要があります。 後でアクセスできるようにカートの内容は保存されることに注意してください。

![オンライン顧客](assets/customers-now-online.png){width="700" zoomable="yes"}

顧客のオンラインステータスは、顧客のログイン、登録、またはその他の状態変化イベントがあった場合にのみ更新されます。 製品の追加、削除、変更など、買い物かご関連のイベントが含まれます。

>[!NOTE]
>
>ページ訪問だけでは、顧客のオンラインステータスは更新されません。 このような情報を収集するには、次の操作をお勧めします。 [Google Analyticsの設定](../merchandising-promotions/google-analytics.md) （単独で、または一緒に [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)）を選択するか、Adobe Commerceで他の analytics ソフトウェアを使用します。

## 現在オンライン状態のすべての顧客を表示

日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>オンライン顧客の購入を支援する方法については、を参照してください。 [買い物かご支援](../stores-purchase/introduction.md#shopping-assistance).

## 時間間隔の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Customer Configuration]**.

1. を展開します。 **[!UICONTROL Online Customers Options]** を選択し、次の操作を実行します。

   ![オンライン顧客オプション](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - の場合 **[!UICONTROL Online Minutes Interval]**、管理者が顧客セッションを表示できる時間（分）を入力します。 デフォルトの 15 分の間隔を使用するには、フィールドを空のままにします。

   - の場合 **[!UICONTROL Customer Data Lifetime]**：顧客から入力された未保存のデータが期限切れになるまでの時間（分単位）を入力します。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 列の説明

| 列 | 説明 |
| --- | --- |
| **[!UICONTROL ID]** | 登録済みの顧客の顧客 ID。 |
| **[!UICONTROL First Name]** | 登録されている顧客の名。 |
| **[!UICONTROL Last Name]** | 登録済みの顧客の姓。 |
| **[!UICONTROL Email]** | 登録された顧客の電子メールアドレス。 |
| **[!UICONTROL Last Activity]** | ストアでの顧客の最後のアクティビティの日時。 |
| **[!UICONTROL Type]** | オプション： `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | 顧客が最後に訪問した URL。 |
| **[!UICONTROL Company]** | ユーザーが所属する会社の名前。 |

{style="table-layout:auto"}
