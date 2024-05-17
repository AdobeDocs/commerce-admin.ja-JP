---
title: イベントの設定
description: イベントを有効にするための基本設定を完了し、ストアフロントサイドバーでイベントブロックを設定する方法について説明します。
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# イベントの設定

{{ee-feature}}

イベントを作成する前に、基本設定を完了してイベントを有効にし、サイドバーのイベントブロックを設定する必要があります。

## イベントの有効化と設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Catalog Events]** を選択し、次の操作を実行します。

   ![カタログの設定 – カタログイベント](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Enable Catalog Events Functionality]** 対象： `Yes`.

   - を設定 **[!UICONTROL Enable Catalog Event Widget on Storefront]** 対象： `Yes`.

   - を入力 **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. デフォルトでは、この値はに設定されています。 `5`. スライダーに一度に 1 つのイベントのみを表示する場合は、 `1`.

   - 次の数を入力 **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. デフォルトでは、この値はに設定されています。 `2`. クリックしたときにスライダーに次のイベントを順番に表示する場合は、次のように入力します `1`.

1. 完了したら、 **[!UICONTROL Save Config]**.

## アクセス制限

プライベート販売、イベント、サイトへのアクセスは、ログインした登録ユーザーに限定したり、アクセス権を得る前に登録する必要がある登録ユーザー以外のユーザーに拡張したりできます。

![一般設定 – web サイトの制限](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### アクセスを制限

プライベート販売、イベント、サイトへのアクセスは、ログインした登録ユーザーに限定したり、アクセス権を得る前に登録する必要がある登録ユーザー以外のユーザーに拡張したりできます。

![一般設定 – web サイトの制限](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL General]** を選択します **[!UICONTROL General]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Website Restrictions]** セクション。

1. を設定 **[!UICONTROL Access Restriction]** 対象： `Yes`.

1. を設定 **[!UICONTROL Restriction Mode]** を次のいずれかに変更します。

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. を設定 **[!UICONTROL Startup Page]** を次のいずれかに変更します。

   - `To login form (302 Found)` - ユーザーは、サイトにアクセスする前にログインフォームにリダイレクトされます。

   - `To landing page (302 Found)` - ユーザーはログインするまで、指定したランディングページにリダイレクトされます。

     >[!IMPORTANT]
     >
     >顧客がサイトにアクセスするためにログインできるように、ランディングページからのログインページへのリンクを必ず含めてください。

1. を選択します。 **[!UICONTROL Landing Page]** 顧客がプライベート販売サイトにログインする前に表示されます。

1. 検索エンジンボットやスパイダーに、ランディングページが正しく、インデックスを作成する他のページがサイトにないことを知らせるには、次のように設定します **[!UICONTROL HTTP Response]** 対象： `200 OK`.

   それ以外の場合は、をに設定 `503 Service Unavailable`.

   >[!NOTE]
   >
   >制限モードがに設定されている場合にのみ適用できます _Web サイト終了_. ランディングページは生のHTMLとしてレンダリングされます。

1. 顧客ログインおよびパスワードを忘れた場合のフォームのフィールドを以前の入力内容から自動的に入力する場合は、次のように設定します **[!UICONTROL Enable Autocomplete on login/forgot password forms]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

### 販売の制限

デフォルトでは、今後のイベントやクローズドイベントに表示される製品は、通常の販売はできません。 _[!UICONTROL Add to Cart]_ボタンが製品リストまたは製品ページに表示されない。

を復元するには _[!UICONTROL Add to Cart]_ボタン閉じたイベントの場合は、イベントを削除する必要があります（ [イベントの更新](event-create.md#update-events)）に設定します。 ただし、製品が販売制限のない別のカテゴリに関連付けられている場合は、製品ページでボタンを使用できます。 同様に、販売制限のない別のカテゴリに製品が関連付けられている場合、ティッカーブロックは製品ページに表示されません。
