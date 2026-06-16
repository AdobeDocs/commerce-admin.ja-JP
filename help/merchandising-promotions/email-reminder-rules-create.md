---
title: メールリマインダーを作成
description: 既存のカート価格ルールを使用するメール リマインダールールを設定する方法を説明します。
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
TQID: https://experienceleague.adobe.com/p7WUWpQFlu2gUeyTU6ZrIHkRJzw8XTp2Mxkvi9Vu-eU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1035
ht-degree: 0%

---

# メールリマインダーを作成

メールリマインダールールを設定する前に、最初に[ カート価格ルールを設定](price-rules-cart-create.md)して、提供するプロモーションを定義する必要があります。 カートのプロパティ、ウィッシュリストのプロパティ、またはその両方にもとづいて、メールリマインダーをトリガーできるルール条件を指定できます。

>[!NOTE]
>
>メールリマインダーは、クーポンの有無にかかわらず、カート価格ルールを宣伝する場合があります。 自動生成されたクーポンを定義するカート価格ルールは、顧客一人ひとりにランダムなクーポンコードを生成します。

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**に移動します。

1. 右上隅の「**[!UICONTROL Add New Rule]**」をクリックします。

1. 次のように、_[!UICONTROL Rule Information]_を完了します。

   ![電子メールリマインダールール ](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - 内部でルールを識別するには、**[!UICONTROL Rule Name]**&#x200B;を入力します。

   - ルールの概要&#x200B;**[!UICONTROL Description]**&#x200B;を入力します。

   - このリマインダーが広告する&#x200B;**[!UICONTROL Cart Price Rule]** プロモーションを選択するには、**[!UICONTROL Select Rule…]**&#x200B;をクリックし、ルールを選択します。

     ![買い物かごルール - select](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - ルールをすぐに有効にする場合は、**[!UICONTROL Status]**&#x200B;を`Active`に設定します。

   - ルールをアクティブにする日付範囲を設定するには、**[!UICONTROL From]**&#x200B;と&#x200B;**[!UICONTROL To]**&#x200B;の日付を入力します。

     カレンダー（![ カレンダーアイコン ](../assets/icon-calendar.png)）から日付を選択することもできます。

   - リマインダーを複数回送信するには、**[!UICONTROL Repeat Schedule]** フィールドに次のメール送信までの日数を入力します。

1. 左側のパネルで、**[!UICONTROL Conditions]**&#x200B;を選択します。

   ルールに少なくとも1つの条件を定義する必要があります。 このプロセスは、[ カタログ価格ルールの作成に似ています。](price-rules-catalog.md)

   ![電子メールリマインダー条件](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   「_追加_」（![追加アイコン ](../assets/icon-add-green-circle.png)）をクリックしてオプションのリストを表示し、次のいずれかの条件を選択します。

   - ウィッシュリスト
   - 買い物かご

   >[!NOTE]
   >
   >顧客が複数のマッチングされたカート放棄、ウィッシュリスト、またはその両方の組み合わせを持っている場合、メールリマインダーはその顧客に対して1回だけトリガーされます。 同じメールリマインダーを再度トリガーするには、_[!UICONTROL Repeat Schedule]_フィールドを使用して、メール間の日数を設定します。<br/>
   >
   >同じ顧客に対して、同じメールリマインダーが&#x200B;**_リトリガーされませんでした_** （**_new_**&#x200B;放棄されたカートとウィッシュリスト **_後_**）、_[!UICONTROL Repeat Schedule]_期間が終了しています）。
   >
   >Adobe Commerce as a Cloud Serviceには、1つのルールを複数回適用できる実験的な機能があります。詳しくは、[ ルールの繰り返し可能性](#rule-repeatability)を参照してください。

   条件を完了して、電子メールリマインダーをトリガーするシナリオを記述します。

   ![電子メールリマインダー条件の例](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. 左側のパネルで、**[!UICONTROL Emails and Labels]**&#x200B;を選択します。

   ![電子メールリマインダールール – 電子メールとラベルテンプレート ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. **[!UICONTROL Email Templates]** セクションで、[ ストア階層](../getting-started/websites-stores-views.md)のweb サイトとストアビューごとに使用する電子メールテンプレートを選択します。

   ストアビューの顧客にリマインダーメールを送信しない場合は、値`Not Selected`を残します。

1. 「_デフォルトのタイトルと説明_」セクションで、次の操作を行います。

   - **[!UICONTROL Rule Title for All Store Views]**&#x200B;を入力します。

     >[!NOTE]
     >
     >この値は、`promotion_name`変数を使用してメールテンプレートに組み込むことができます。

   - **[!UICONTROL Rule Description for All Store Views]**&#x200B;を入力します。

     ![電子メールリマインダー – タイトルと説明](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - _[!UICONTROL Titles and Descriptions Per Store View]_セクションで、_ デフォルトのストアビュー&#x200B;_の&#x200B;**[!UICONTROL Rule Title]**と&#x200B;**[!UICONTROL Description]**を入力します。 複数のストアビューの場合は、それぞれに適切なタイトルと説明を入力します。

     >[!NOTE]
     >
     >promotion_description変数を使用すると、説明をメールテンプレートに組み込むことができます。

     ![ タイトルと説明 – ストアビュー](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. [!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクト（Adobeが管理するSaaS インフラストラクチャ）にのみ適用されます。"} [!DNL Adobe Commerce as a Cloud Service]を使用している場合、[!UICONTROL Rule Repeatability] チェックボックスを選択して[ ルールの繰り返し可能性](#rule-repeatability)を有効にできます。

   >[!IMPORTANT]
   >
   >ルールの繰り返し可能性オプションは、デフォルトで無効になっている実験的な機能です。  このオプションを有効にする方法について詳しくは、[ ルールの繰り返し可能性](#rule-repeatabilty)を参照してください。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## ルールの再現性

[!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクト（Adobeが管理するSaaS インフラストラクチャ）にのみ適用されます。"}

>[!IMPORTANT]
>
>これは実験的な機能であり、デフォルトでは有効になっていません。 有効にするには、Adobe Commerce カスタマーサクセスマネージャーにお問い合わせいただくか、サポートチケットを作成してください。 今後のリリースで、すべてのAdobe Commerce as a Cloud Serviceのお客様が利用できるようになります。

ルールの繰り返し性により、複数のメールリマインダーに対して1つのルールを再利用できます。 これは、後で同じ顧客にルールを適用する場合に便利です。 ルールの繰り返し性がなければ、顧客がカートをクリアしたり、購入を完了したりすると、このルールは適用されなくなります。

「**[!UICONTROL General Information]**」タブの「**[!UICONTROL Rule Repeatability]**」チェックボックスをオンにすると、元のルールトリガーが適用されなくなった後に、ルールをユーザーに再度適用できます。

![ ルールの繰り返し可能性](./assets/rule-repeatability.png){width="600" zoomable="yes"}

>[!BEGINSHADEBOX]

次の例を考えてみましょう。

1日後にトリガーされ、3日後と5日後にリトリガーされるカート放棄ルールがあります。 買い物かごを放棄したユーザーには、1日後にカート放棄リマインダーのメールが届きます。 2日後、ユーザーは購入を完了します。 カートはもう放棄されていません。 その10日後、利用者は商品の異なる新しいカートを放棄します。

- **[!UICONTROL Rule Repeatability]**&#x200B;が有効になっている場合、ユーザーは新しいカート放棄メールのリマインダーを受け取ります。
- **[!UICONTROL Rule Repeatability]**&#x200B;が無効になっている場合、ユーザーは&#x200B;**not**&#x200B;にカート放棄に関する追加のメールリマインダーを受信します。

>[!ENDSHADEBOX]

## トリガー条件

| Source | トリガー |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Rule Name] | 自動リマインダールールの名前は、内部でルールを識別します。 |
| [!UICONTROL Description] | 内部参照用のルールの説明。 |
| [!UICONTROL Shopping Cart Price Rule] | このメールリマインダーに関連付けられているショッピングカートのルール。 リマインダーメールは、クーポンの有無にかかわらずショッピングカート価格ルールを宣伝できます。 ショッピングカートの価格ルールに自動生成されたクーポンが含まれる場合、リマインダールールは、各顧客にランダムで一意のクーポンコードを生成します。 |
| [!UICONTROL Assigned to Website] | このルールに基づいて自動リマインダーメールを受信するweb サイト。 |
| [!UICONTROL Status] | ルールをアクティブ化します。 ステータスが非アクティブの場合、他のすべての設定は無視され、ルールはトリガーされません。 オプション：`Active` / `Inactive` |
| [!UICONTROL From Date] | この自動リマインダールールの開始日。 日付が指定されていない場合、ルールはすぐにアクティブになります。 |
| [!UICONTROL To Date] | この自動リマインダールールの終了日。 日付が指定されていない場合、ルールは無期限にアクティブになります。 |
| [!UICONTROL Repeat Schedule] | ルールがトリガーされるまでの日数。条件が満たされた場合は、リマインダーメールが再度送信されます。 ルールを複数回トリガーするには、次にメールを送信するまでの日数をコンマで区切って入力します。 例えば、`7`と入力すると、7日後にルールが再びトリガーされます。`7,14`と入力すると、7日後、14日後にルールがトリガーされます。 |
| [!UICONTROL Email Templates] | 各ストアビューに使用するメールテンプレートを決定します。 |
| [!UICONTROL Rule Title for All Store Views] | 各ストアビューのルールのタイトルを決定します。 |
| [!UICONTROL Rule Description for All Store Views] | 各ストアビューのルールの説明を指定します。 |

{style="table-layout:auto"}
