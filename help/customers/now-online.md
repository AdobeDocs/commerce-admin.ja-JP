---
title: オンラインへようこそ
description: '[!UICONTROL Customers ] メニューの「_Now Online_」オプションには、現在ストアでオンラインになっているすべての顧客と訪問者が一覧表示されます。'
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# オンラインへようこそ

[!DNL Customers] メニューの&#x200B;**[!UICONTROL Now Online]** オプションには、現在ストアでオンラインになっているすべての顧客と訪問者が一覧表示されます。 顧客が現在オンラインとして表示される時間間隔は、設定で設定され、管理者から[!DNL Customer's] アクティビティが表示される時間を決定します。 デフォルトでは、間隔は15分です。 この期間中にキーボードを使用せず、顧客が買い物を続けるにはアカウントに再度サインインする必要がある場合、セッションは終了します。 カートの内容は後でアクセスするために保存されることに注意することが重要です。

![ オンラインのお客様](assets/customers-now-online.png){width="700" zoomable="yes"}

顧客のオンラインステータスは、顧客のログイン、登録、その他の状況を変化させるイベントでのみ更新されます。 商品の追加、削除、変更など、カート関連のイベントが含まれます。

>[!NOTE]
>
>ページへの訪問だけでは、顧客のオンラインステータスは更新されません。 このような情報を収集するには、[Google Analytics](../merchandising-promotions/google-analytics.md)を単独または[Google Tag Manager](../merchandising-promotions/google-tag-manager.md)で設定するか、Adobe Commerceで他の分析ソフトウェアを使用することをお勧めします。

## オンライン状態のすべての顧客を表示

_管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL Online Now]**&#x200B;に移動します。

>[!TIP]
>
>オンライン顧客による購入の完了を支援する方法については、[ ショッピング支援](../stores-purchase/introduction.md#shopping-assistance)を参照してください。

## 時間間隔の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Customer Configuration]**&#x200B;を選択します。

1. **[!UICONTROL Online Customers Options]** セクションを展開し、次の操作を行います。

   ![ オンラインのお客様オプション ](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - **[!UICONTROL Online Minutes Interval]**&#x200B;に、管理者から顧客セッションを表示するための分数を入力します。 デフォルトの間隔である15分を受け入れるには、フィールドを空のままにします。

   - **[!UICONTROL Customer Data Lifetime]**&#x200B;の場合、お客様が入力した未保存のデータが期限切れになるまでの分数を入力します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## 列の説明

| 列 | 説明 |
| --- | --- |
| **[!UICONTROL ID]** | 登録済み顧客の顧客ID。 |
| **[!UICONTROL First Name]** | 登録済みのお客様の名前。 |
| **[!UICONTROL Last Name]** | 登録済みのお客様の姓。 |
| **[!UICONTROL Email]** | 登録済みのお客様の電子メールアドレス。 |
| **[!UICONTROL Last Activity]** | ストアでの顧客の最後のアクティビティの日時。 |
| **[!UICONTROL Type]** | オプション：`Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | 顧客が最後に訪問したURL。 |
| **[!UICONTROL Company]** | ユーザーが属する会社の名前。 |

{style="table-layout:auto"}
