---
title: イベントの設定
description: イベントを有効にするための基本設定を完了し、ストアフロントサイドバーでイベントブロックを設定する方法について説明します。
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# イベントの設定

{{ee-feature}}

イベントを作成する前に、基本設定を完了してイベントを有効にし、サイドバーのイベントブロックを設定する必要があります。

## イベントの有効化と設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Catalog Events]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; カタログの設定 – カタログイベント &#x200B;](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enable Catalog Events Functionality]** を `Yes` に設定します。

   - **[!UICONTROL Enable Catalog Event Widget on Storefront]** を `Yes` に設定します。

   - **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]** を入力します。 デフォルトでは、この値は `5` に設定されています。 スライダーに一度に 1 つのイベントのみを表示する場合は、「`1`」と入力します。

   - **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]** の数を入力します。 デフォルトでは、この値は `2` に設定されています。 クリック時にスライダーに次のイベントを順番に表示する場合は、「`1`」と入力します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## アクセス制限

プライベート販売、イベント、サイトへのアクセスは、ログインした登録ユーザーに限定したり、アクセス権を得る前に登録する必要がある登録ユーザー以外のユーザーに拡張したりできます。

![&#x200B; 一般設定 – web サイトの制限 &#x200B;](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### アクセスを制限

プライベート販売、イベント、サイトへのアクセスは、ログインした登録ユーザーに限定したり、アクセス権を得る前に登録する必要がある登録ユーザー以外のユーザーに拡張したりできます。

![&#x200B; 一般設定 – web サイトの制限 &#x200B;](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL General]**」を展開し、その下の「**[!UICONTROL General]**」を選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Website Restrictions]**」セクションを展開します。

1. **[!UICONTROL Access Restriction]** を `Yes` に設定します。

1. **[!UICONTROL Restriction Mode]** を次のいずれかに設定します。

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. **[!UICONTROL Startup Page]** を次のいずれかに設定します。

   - `To login form (302 Found)` - サイトにアクセスする前に、ユーザーはログインフォームにリダイレクトされます。

   - `To landing page (302 Found)` - ユーザーは、ログインするまで、指定されたランディングページにリダイレクトされます。

     >[!IMPORTANT]
     >
     >顧客がサイトにアクセスするためにログインできるように、ランディングページからのログインページへのリンクを必ず含めてください。

1. 顧客がプライベート販売サイトにログインする前に表示される **[!UICONTROL Landing Page]** を選択します。

1. 検索エンジンボットやスパイダーに、ランディングページが正しく、インデックスを作成する他のページがサイトにないことを知らせるには、**[!UICONTROL HTTP Response]** を `200 OK` に設定します。

   それ以外の場合は、`503 Service Unavailable` に設定します。

   >[!NOTE]
   >
   >制限モードが「_Web サイトを閉鎖_」に設定されている場合にのみ適用されます。 ランディングページは生のHTMLとしてレンダリングされます。

1. 顧客ログインおよびパスワードを忘れた場合のフォームのフィールドを以前の入力内容から自動的に入力する場合は、「**[!UICONTROL Enable Autocomplete on login/forgot password forms]**」を「`Yes`」に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### 販売の制限

デフォルトでは、今後のイベントやクローズドイベントに表示される製品は一般販売には使用できず、製品リストまたは製品ページに「_[!UICONTROL Add to Cart]_」ボタンは表示されません。

クローズしたイベントの「_[!UICONTROL Add to Cart]_」ボタンを復元するには、イベントを削除する必要があります（[&#x200B; イベントの更新 &#x200B;](event-create.md#update-events) を参照）。 ただし、製品が販売制限のない別のカテゴリに関連付けられている場合は、製品ページでボタンを使用できます。 同様に、販売制限のない別のカテゴリに製品が関連付けられている場合、ティッカーブロックは製品ページに表示されません。
