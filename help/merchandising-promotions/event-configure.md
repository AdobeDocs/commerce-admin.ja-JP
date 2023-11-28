---
title: イベントの設定
description: 基本的な設定を完了してイベントを有効にし、ストアフロントサイドバーでイベントブロックを設定する方法を説明します。
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# イベントの設定

{{ee-feature}}

イベントを作成する前に、基本設定を完了してイベントを有効にし、サイドバーにイベントブロックを設定する必要があります。

## イベントの有効化と設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Catalog Events]** 」セクションで次の操作を実行します。

   ![カタログ設定 — カタログイベント](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Enable Catalog Events Functionality]** から `Yes`.

   - 設定 **[!UICONTROL Enable Catalog Event Widget on Storefront]** から `Yes`.

   - 次を入力します。 **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. デフォルトでは、この値はに設定されています。 `5`. スライダーで一度に 1 つのイベントのみを表示する場合は、「 `1`.

   - 次の数を入力： **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. デフォルトでは、この値はに設定されています。 `2`. スライダーをクリックしたときに次のイベントを順に表示する場合は、 `1`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## アクセス制限

プライベートセール、イベントまたはサイトへのアクセスは、ログインした登録済み顧客に限定するか、アクセス権を取得する前に登録する必要がある登録済み以外の顧客に拡張することができます。

![一般的な設定 — Web サイトの制限](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### アクセスを制限

プライベートセール、イベントまたはサイトへのアクセスは、ログインした登録済み顧客に限定するか、アクセス権を取得する前に登録する必要がある登録済み以外の顧客に拡張することができます。

![一般的な設定 — Web サイトの制限](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL General]** を選択します。 **[!UICONTROL General]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Website Restrictions]** 」セクションに入力します。

1. 設定 **[!UICONTROL Access Restriction]** から `Yes`.

1. 設定 **[!UICONTROL Restriction Mode]** を次のいずれかに変更します。

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. 設定 **[!UICONTROL Startup Page]** を次のいずれかに変更します。

   - `To login form (302 Found)` ：ユーザーは、サイトにアクセスする前に、ログインフォームにリダイレクトされます。

   - `To landing page (302 Found)` ：ユーザーは、ログインするまで、指定したランディングページにリダイレクトされます。

     >[!IMPORTANT]
     >
     >顧客がサイトにログインしてアクセスできるように、ランディングページからログインページへのリンクを必ず含めてください。

1. を選択します。 **[!UICONTROL Landing Page]** これは、顧客がプライベートセールサイトにログインする前に表示されます。

1. ランディングページが正しく、インデックスを作成する他のページがサイトにないことを検索エンジンのボットやスパイダーに知らせるには、を設定します。 **[!UICONTROL HTTP Response]** から `200 OK`.

   その他の場合は、 `503 Service Unavailable`.

   >[!NOTE]
   >
   >制限モードが _Web サイトが閉じられました_. ランディングページは生のHTMLとしてレンダリングされます。

1. 顧客ログインとパスワードを忘れた場合のフォームを、前のエントリから自動的に入力する場合は、 **[!UICONTROL Enable Autocomplete on login/forgot password forms]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

### 販売を制限

デフォルトでは、今後またはクローズされたイベントに表示される製品は、一般販売や _[!UICONTROL Add to Cart]_ボタンが製品リストまたは製品ページに表示されない。

を復元するには、以下を実行します。 _[!UICONTROL Add to Cart]_ボタンを使用して、イベントを削除する必要があります ( [イベントを更新](event-create.md#update-events)) をクリックします。 ただし、製品が販売制限のない別のカテゴリに関連付けられている場合は、製品ページの「 」ボタンが使用できます。 同様に、製品が販売制限のない別のカテゴリに関連付けられている場合、ティッカーブロックは製品ページに表示されません。
