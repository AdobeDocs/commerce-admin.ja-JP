---
title: メールのリマインダーの作成
description: 既存の買い物かご価格ルールを使用するメールリマインダールールを設定する方法について説明します。
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
source-git-commit: b750accf7aab49357f04e16dc60791e704516141
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# メールのリマインダーの作成

E メールリマインダールールを設定する前に、まず以下を行う必要があります [買い物かごの価格ルールの設定](price-rules-cart-create.md) オファーされるプロモーションを定義します。 メールのリマインダーをトリガーするルール条件を、買い物かごのプロパティ、ウィッシュリストのプロパティ、またはその両方に基づくことができます。

>[!NOTE]
>
>メールのリマインダーでは、クーポンの有無に関わらず、買い物かごの価格ルールを促進する場合があります。 自動生成されたクーポンを定義する買い物かご価格ルールにより、各顧客にランダムクーポンコードが生成されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Rule]**.

1. を完了する _[!UICONTROL Rule Information]_を作成します。

   ![E メールリマインダールール](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - を入力 **[!UICONTROL Rule Name]** ルールを内部で識別する場合。

   - 概要を入力 **[!UICONTROL Description]** （ルールの）。

   - を選択します **[!UICONTROL Cart Price Rule]** このリマインダーがアドバタイズするプロモーションです。クリックして **[!UICONTROL Select Rule…]**&#x200B;を選択し、ルールを選択します。

     ![買い物かごルール – 選択](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - ルールをすぐに有効にする場合は、次のように設定します **[!UICONTROL Status]** 対象： `Active`.

   - ルールをアクティブにする日付範囲を設定するには、 **[!UICONTROL From]** および **[!UICONTROL To]** 日付。

     カレンダーから日付を選択することもできます（ ![カレンダーアイコン](../assets/icon-calendar.png) ）に設定します。

   - リマインダーを複数回送信するには、で次のメールが送信されるまでの日数を入力します **[!UICONTROL Repeat Schedule]** フィールド。

1. 左側のパネルで、を選択します。 **[!UICONTROL Conditions]**.

   ルールに少なくとも 1 つの条件を定義する必要があります。 プロセスは、の作成に似ています [カタログ価格ルール。](price-rules-catalog.md)

   ![メールリマインダー条件](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   クリック _追加_ （ ![アイコンを追加](../assets/icon-add-green-circle.png)）を選択してオプションのリストを表示し、次のいずれかの条件を選択します。

   - ウィッシュリスト
   - ショッピングカート

   >[!NOTE]
   >
   >顧客に、一致する放棄された買い物かご、ウィッシュリストまたはその両方の組み合わせが複数ある場合、メールのリマインダーはその顧客に対して 1 回だけトリガーされます。 同じメールのリマインダーを再度トリガーするには、 _[!UICONTROL Repeat Schedule]_メールの間隔の日数を設定するフィールド。 <br/>
   >
   >同じメールリマインダーは、 **_再トリガーされない_** 同じ顧客の **_新規_** 放棄された買い物かごとウィッシュリスト **_後_** この _[!UICONTROL Repeat Schedule]_期間が終了しました。

   メールのリマインダーをトリガーするシナリオを示す条件を入力します。

   ![メールリマインダー条件の例](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. 左側のパネルで、を選択します。 **[!UICONTROL Emails and Labels]**.

   ![メールリマインダールール – メールとラベルのテンプレート ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. が含まれる **[!UICONTROL Email Templates]** セクションで、各 web サイトとストア表示に使用するメールテンプレートを選択します [ストア階層](../getting-started/websites-stores-views.md).

   ストア表示の顧客にリマインダーメールを送信しない場合は、値のままにします `Not Selected`.

1. が含まれる _デフォルトのタイトルと説明_ セクションで、次の操作を行います。

   - を入力 **[!UICONTROL Rule Title for All Store Views]**.

     >[!NOTE]
     >
     >この値は、 `promotion_name` 変数。

   - を入力 **[!UICONTROL Rule Description for All Store Views]**.

     ![メールのリマインダー – タイトルと説明](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - が含まれる _[!UICONTROL Titles and Descriptions Per Store View]_「」セクションに、**[!UICONTROL Rule Title]**および&#x200B;**[!UICONTROL Description]**の場合_&#x200B;デフォルトのストア表示&#x200B;_. 複数のストア表示の場合は、それぞれに適切なタイトルと説明を入力します。

     >[!NOTE]
     >
     >promotion_description 変数を使用すると、説明をメールテンプレートに組み込むことができます。

     ![タイトルと説明 – ストア表示](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

## トリガー条件

| ソース | トリガー |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Rule Name] | 自動リマインダールールの名前は、ルールを内部的に識別します。 |
| [!UICONTROL Description] | 内部参照用のルールの説明。 |
| [!UICONTROL Shopping Cart Price Rule] | この E メール リマインダーに関連付けられている買い物かごルール。 リマインダーメールでは、クーポンの有無に関わらず、買い物かご価格ルールを促進できます。 買い物かご価格ルールに自動生成されたクーポンが含まれている場合、リマインダールールは顧客ごとにランダムな一意のクーポンコードを生成します。 |
| [!UICONTROL Assigned to Website] | このルールに基づく自動リマインダーメールを受信する Web サイト。 |
| [!UICONTROL Status] | ルールを有効化します。 ステータスが非アクティブの場合、他のすべての設定は無視され、ルールはトリガーされません。 オプション： `Active` / `Inactive` |
| [!UICONTROL From Date] | この自動リマインダールールの開始日。 日付を指定しない場合、ルールは直ちにアクティブになります。 |
| [!UICONTROL To Date] | この自動リマインダールールの終了日。 日付を指定しない場合、ルールは無期限にアクティブになります。 |
| [!UICONTROL Repeat Schedule] | 条件が満たされた場合に、ルールがトリガーされ、リマインダーメールが再度送信されるまでの日数。 ルールを複数回トリガーするには、次のメールブラストまでの日数をコンマで区切って入力します。 例えば、 `7` 7 日後にルールを再度トリガーするには、次のように入力します。 `7,14` で、ルールを 7 日後にトリガーし、さらに 14 日後にトリガーします。 |
| [!UICONTROL Email Templates] | 各ストア表示に使用するメールテンプレートを決定します。 |
| [!UICONTROL Rule Title for All Store Views] | 各ストア表示のルールのタイトルを決定します。 |
| [!UICONTROL Rule Description for All Store Views] | 各ストア表示のルールの説明を決定します。 |

{style="table-layout:auto"}
