---
title: 注文と返品ウィジェット
description: 注文と返品ウィジェットを使用して、顧客が注文のステータスを確認したり、請求書を印刷したり、出荷を追跡したりする方法を説明します。
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# 注文と返品ウィジェット

この _注文と返品_ ウィジェットを使用すると、顧客は注文のステータスを確認したり、請求書を印刷したり、出荷を追跡したりできます。 ウィジェットがストアフロントに追加されると、ゲストと、アカウントにログインしていない顧客に対してのみ表示されます。 ゲストは、注文 ID、請求先の姓、およびメールアドレスまたは郵便番号を指定することで、注文を検索できます。

![ストアフロントのサイドバーにある「注文と返品」ウィジェット](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## ストアフロントの注文と返品ウィジェット

1. 顧客は以下を使用できます **[!UICONTROL Find Order By]** オーダーの検索に使用する次のパラメータのいずれかを選択するオプション。

   - メールアドレス
   - 郵便番号

1. 顧客が以下を入力 **[!UICONTROL Order ID]** および **[!UICONTROL Billing Last Name]**.

1. 請求を入力 **[!UICONTROL Email Address]** または **[!UICONTROL ZIP Code]** 注文と関連付けられています。

1. クリック数 **[!UICONTROL Search]** 注文を取得します。

   ![ストアフロントに表示される注文情報](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## 注文と返品ウィジェットの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Widget]**.

1. が含まれる _[!UICONTROL Settings]_セクションで、次の操作を行います。

   - を設定 **[!UICONTROL Type]** 対象： `Orders and Returns`.

   - を選択します。 **[!UICONTROL Design Theme]** それは店で使われます。

1. クリック **[!UICONTROL Continue]**.

1. が含まれる _[!UICONTROL Storefront Properties]_セクションで、次の操作を行います。

   - の場合 **[!UICONTROL Widget Title]**、ウィジェットのわかりやすいタイトルを入力します。

     このタイトルは、管理者からのみ表示されます。

   - の場合 **[!UICONTROL Assign to Store Views]**&#x200B;で、ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択することも、 `All Store Views`. 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]**&#x200B;を入力し、この項目がページの同じ部分に他のユーザーと表示される順序を決定します。 （`0` =最初、 `1` =秒、 `3` = 3 番目、など）。

1. が含まれる _[!UICONTROL Layout Updates]_セクションで、をクリック&#x200B;**[!UICONTROL Add Layout Update]**次の手順を実行します。

   - を設定 **[!UICONTROL Display On]** を選択して、ウィジェットを表示するページのタイプを指定します。

   - ウィジェットをページ上のどこに表示するかを決定するには、残りのレイアウト更新情報を完了させます。

1. 完了したら、 **[!UICONTROL Save]**.

1. キャッシュを更新するように求めるプロンプトが表示されたら、ページ上部のメッセージに記載されているリンクをクリックし、指示に従います。
