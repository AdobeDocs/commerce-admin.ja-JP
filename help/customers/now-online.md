---
title: 顧客がオンラインになりました
description: '[!UICONTROL Customers &#x200B;] メニューの_Now Online_ オプションには、ストアで現在オンラインになっているすべての顧客と訪問者が一覧表示されます。'
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# 顧客がオンラインになりました

[!DNL Customers] メニューの「**[!UICONTROL Now Online]**」オプションには、ストアで現在オンラインになっているすべての顧客と訪問者が一覧表示されます。 設定で、顧客が現在オンラインとして表示される時間間隔が設定され、[!DNL Customer's] のアクティビティが管理者から表示される期間が決定されます。 デフォルトでは、間隔は 15 分です。 この間キーボードを使用しないと、セッションは終了します。顧客が買い物を続行するには、もう一度アカウントにログインする必要があります。 後でアクセスできるようにカートの内容は保存されることに注意してください。

![&#x200B; オンライン顧客 &#x200B;](assets/customers-now-online.png){width="700" zoomable="yes"}

顧客のオンラインステータスは、顧客のログイン、登録、またはその他の状態変化イベントがあった場合にのみ更新されます。 製品の追加、削除、変更など、買い物かご関連のイベントが含まれます。

>[!NOTE]
>
>ページ訪問だけでは、顧客のオンラインステータスは更新されません。 このような情報を収集するには、[Google Analyticsを設定 &#x200B;](../merchandising-promotions/google-analytics.md) （単独または [Google Tag Manager](../merchandising-promotions/google-tag-manager.md) を使用）するか、他の分析ソフトウェアをAdobe Commerceと共に使用することをお勧めします。

## 現在オンライン状態のすべての顧客を表示

_管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Online Now]** に移動します。

>[!TIP]
>
>オンライン顧客の購入の支援について詳しくは、[&#x200B; 買い物サポート &#x200B;](../stores-purchase/introduction.md#shopping-assistance) を参照してください。

## 時間間隔の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Customer Configuration]**」を選択します。

1. 「**[!UICONTROL Online Customers Options]**」セクションを展開し、次の操作を実行します。

   ![&#x200B; オンライン顧客オプション &#x200B;](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - **[!UICONTROL Online Minutes Interval]**：管理者が顧客セッションを表示する時間（分）を入力します。 デフォルトの 15 分の間隔を使用するには、フィールドを空のままにします。

   - **[!UICONTROL Customer Data Lifetime]**：顧客が入力した未保存のデータが期限切れになるまでの時間（分単位）を入力します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 列の説明

| 列 | 説明 |
| --- | --- |
| **[!UICONTROL ID]** | 登録済みの顧客の顧客 ID。 |
| **[!UICONTROL First Name]** | 登録されている顧客の名。 |
| **[!UICONTROL Last Name]** | 登録済みの顧客の姓。 |
| **[!UICONTROL Email]** | 登録された顧客の電子メールアドレス。 |
| **[!UICONTROL Last Activity]** | ストアでの顧客の最後のアクティビティの日時。 |
| **[!UICONTROL Type]** | オプション：`Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | 顧客が最後に訪問した URL。 |
| **[!UICONTROL Company]** | ユーザーが所属する会社の名前。 |

{style="table-layout:auto"}
