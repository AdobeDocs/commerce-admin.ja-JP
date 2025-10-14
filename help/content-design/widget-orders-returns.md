---
title: 注文と返品ウィジェット
description: 注文と返品ウィジェットを使用して、顧客が注文のステータスを確認したり、請求書を印刷したり、出荷を追跡したりする方法を説明します。
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# 注文と返品ウィジェット

_注文と返品_ ウィジェットを使用すると、ゲストは注文のステータスを確認したり、請求書を印刷したり、出荷を追跡したりできます。 ウィジェットがストアフロントに追加されると、ゲストと、アカウントにログインしていない顧客に対してのみ表示されます。 ゲストは、注文 ID、請求先の姓、およびメールアドレスまたは郵便番号を指定することで、注文を検索できます。

![&#x200B; ストアフロントのサイドバーにある「注文と返品」ウィジェット &#x200B;](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## ストアフロントの注文と返品ウィジェット

1. 顧客は、**[!UICONTROL Find Order By]** のオプションを使用して、注文を検索するために使用する次のパラメーターの 1 つを選択できます。

   - メールアドレス
   - 郵便番号

1. 顧客が **[!UICONTROL Order ID]** と **[!UICONTROL Billing Last Name]** を入力します。

1. 注文に関連付けられた請求 **[!UICONTROL Email Address]** または **[!UICONTROL ZIP Code]** を入力します。

1. **[!UICONTROL Search]** をクリックして注文を取得します。

   ![&#x200B; ストアフロントに表示する注文情報 &#x200B;](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## 注文と返品ウィジェットの設定

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Widgets]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add Widget]**」をクリックします。

1. _[!UICONTROL Settings]_&#x200B;セクションで、次の操作を行います。

   - **[!UICONTROL Type]** を `Orders and Returns` に設定します。

   - ストアで使用される **[!UICONTROL Design Theme]** を選択します。

1. 「**[!UICONTROL Continue]**」をクリックします。

1. _[!UICONTROL Storefront Properties]_&#x200B;セクションで、次の操作を行います。

   - **[!UICONTROL Widget Title]** しくは、ウィジェットのわかりやすいタイトルを入力します。

     このタイトルは、管理者からのみ表示されます。

   - **[!UICONTROL Assign to Store Views]**：ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択することも、`All Store Views` を選択することもできます。 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]** の場合は、数字を入力して、この項目がページの同じ部分に他の項目と共に表示される順序を決定します。 （`0` = 1 番目、`1` = 2 番目、`3` = 3 番目など）。

1. 「_[!UICONTROL Layout Updates]_」セクションで「**[!UICONTROL Add Layout Update]**」をクリックし、次の操作を実行します。

   - ウィジェットを表示するページのタイプに **[!UICONTROL Display On]** を設定します。

   - ウィジェットをページ上のどこに表示するかを決定するには、残りのレイアウト更新情報を完了させます。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. キャッシュを更新するように求めるプロンプトが表示されたら、ページ上部のメッセージに記載されているリンクをクリックし、指示に従います。
