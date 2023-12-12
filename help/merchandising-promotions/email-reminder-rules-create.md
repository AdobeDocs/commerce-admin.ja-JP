---
title: 電子メールリマインダーを作成
description: 既存の買い物かご価格ルールを使用する電子メールリマインダールールを設定する方法を説明します。
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
source-git-commit: b750accf7aab49357f04e16dc60791e704516141
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# 電子メールリマインダーを作成

電子メールリマインダールールを設定する前に、まず [買い物かごの価格ルールを設定する](price-rules-cart-create.md) をクリックして、提供されるプロモーションを定義します。 電子メールリマインダーをトリガーする際のルール条件は、買い物かごのプロパティ、ウィッシュリストのプロパティ、またはその両方に基づいて設定できます。

>[!NOTE]
>
>電子メールのリマインダーによって、クーポンの有無に関わらず、買い物かごの価格ルールが促進される場合があります。 自動生成されたクーポンを定義する買い物かごの価格ルールでは、各顧客に対してランダムなクーポンコードが生成されます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**.

1. 右上隅で、 **[!UICONTROL Add New Rule]**.

1. 次を完了： _[!UICONTROL Rule Information]_、次のように指定します。

   ![電子メールリマインダールール](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - を入力します。 **[!UICONTROL Rule Name]** ルールを内部で識別する。

   - 概要を入力 **[!UICONTROL Description]** 」と入力します。

   - を選択するには、以下を実行します。 **[!UICONTROL Cart Price Rule]** このリマインダーが宣伝するプロモーションの場合は、 **[!UICONTROL Select Rule…]**&#x200B;をクリックし、ルールを選択します。

     ![買い物かごルール — 選択](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - ルールをすぐに有効にする場合は、 **[!UICONTROL Status]** から `Active`.

   - ルールをアクティブにする日付範囲を設定するには、 **[!UICONTROL From]** および **[!UICONTROL To]** 日付。

     また、カレンダー ( ![カレンダーアイコン](../assets/icon-calendar.png) ) をクリックします。

   - リマインダーを複数回送信するには、次の E メールの一斉送信までの日数を **[!UICONTROL Repeat Schedule]** フィールドに入力します。

1. 左側のパネルで、を選択します。 **[!UICONTROL Conditions]**.

   ルールには、少なくとも 1 つの条件を定義する必要があります。 このプロセスは、 [カタログ価格ルール](price-rules-catalog.md)

   ![電子メールリマインダー条件](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   クリック _追加_ ( ![追加アイコン](../assets/icon-add-green-circle.png)) をクリックしてオプションのリストを表示し、次のいずれかの条件を選択します。

   - ウィッシュリスト
   - 買い物かご

   >[!NOTE]
   >
   >顧客に対して、一致しなかった買い物かご、ウィッシュリストまたはその両方の組み合わせが複数ある場合、その顧客に対して電子メールリマインダーが 1 回だけトリガーされます。 同じ電子メールリマインダーを再度トリガーするには、 _[!UICONTROL Repeat Schedule]_フィールドを使用してメール間の日数を設定します。 <br/>
   >
   >同じ電子メールリマインダーが **_再トリガーされない_** 同じ顧客のために **_新規_** 放棄された買い物かごとウィッシュリスト **_次より後_** の _[!UICONTROL Repeat Schedule]_期間が過ぎました。

   条件を完了して、電子メールリマインダーをトリガーにするシナリオを説明します。

   ![電子メールリマインダー条件の例](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. 左側のパネルで、を選択します。 **[!UICONTROL Emails and Labels]**.

   ![電子メールリマインダールール — 電子メールとラベルテンプレート ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Email Templates]** セクションで、各 Web サイトで使用する電子メールテンプレートを選択し、 [ストア階層](../getting-started/websites-stores-views.md).

   ストア表示の顧客にリマインダーの電子メールを送信しない場合は、値 `Not Selected`.

1. Adobe Analytics の _デフォルトのタイトルと説明_ セクションで、以下の操作を実行します。

   - 次を入力します。 **[!UICONTROL Rule Title for All Store Views]**.

     >[!NOTE]
     >
     >この値は、 `promotion_name` 変数を使用します。

   - 次を入力します。 **[!UICONTROL Rule Description for All Store Views]**.

     ![電子メールリマインダー — タイトルと説明](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - Adobe Analytics の _[!UICONTROL Titles and Descriptions Per Store View]_セクションに、**[!UICONTROL Rule Title]**および&#x200B;**[!UICONTROL Description]**（の）_&#x200B;デフォルトのストア表示&#x200B;_. 複数のストアビューの場合は、それぞれに適切なタイトルと説明を入力します。

     >[!NOTE]
     >
     >この説明は、 promotion_description 変数を使用して電子メールテンプレートに組み込むことができます。

     ![タイトルと説明 — ストア表示](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save]**.

## トリガー条件

| ソース | トリガー |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Rule Name] | 自動リマインダールールの名前は、ルールの内部的な識別に使用されます。 |
| [!UICONTROL Description] | 内部参照用のルールの説明。 |
| [!UICONTROL Shopping Cart Price Rule] | この電子メールリマインダーに関連付けられている買い物かごルール。 リマインダーの E メールは、クーポンの有無に関わらず、買い物かごの価格ルールを促進できます。 買い物かごの価格ルールに自動生成されたクーポンが含まれている場合、リマインダールールは、各顧客に対してランダムで一意のクーポンコードを生成します。 |
| [!UICONTROL Assigned to Website] | このルールに基づいて自動リマインダー電子メールを受け取る Web サイトです。 |
| [!UICONTROL Status] | ルールをアクティブ化します。 ステータスが非アクティブの場合、その他の設定はすべて無視され、ルールはトリガーされません。 オプション： `Active` / `Inactive` |
| [!UICONTROL From Date] | この自動リマインダールールの開始日です。 日付を指定しない場合、ルールは直ちにアクティブになります。 |
| [!UICONTROL To Date] | この自動リマインダールールの終了日です。 日付を指定しない場合、ルールは無期限にアクティブになります。 |
| [!UICONTROL Repeat Schedule] | 条件が満たされた場合に、ルールがトリガーされ、リマインダー E メールが再度送信されるまでの日数。 ルールを複数回トリガーするには、次の E メールのブラストの前の日数をコンマで区切って入力します。 例えば、 `7` ルールを 7 日後に再度トリガーするには、次のように入力します。 `7,14` を設定して、7 日後、14 日後に再度トリガーする必要があります。 |
| [!UICONTROL Email Templates] | 各ストア表示で使用する電子メールテンプレートを決定します。 |
| [!UICONTROL Rule Title for All Store Views] | 各ストアビューのルールのタイトルを決定します。 |
| [!UICONTROL Rule Description for All Store Views] | 各ストアビューのルールの説明を決定します。 |

{style="table-layout:auto"}
