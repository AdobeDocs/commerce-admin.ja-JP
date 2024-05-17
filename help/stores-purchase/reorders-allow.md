---
title: 並べ替えを許可
description: 顧客に並べ替え機能を提供する方法を説明します。
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# 並べ替えを許可

有効にすると、顧客アカウントから直接、または内の元の注文から注文を行うことができます _Admin_. 並べ替えは、デフォルトで有効になっています。

![管理者の顧客並べ替えリンク](./assets/customer-reorder.png){width="700" zoomable="yes"}

## 注文で並べ替えを有効にする基準

- この _並べ替えを許可_ 設定オプションを有効にする必要があります。

- 順序が次の中にある場合： `Hold` または `Payment Review` ステータスで、「並べ替え」オプションが無効になっている。

- 注文した項目のいずれかが利用不可、在庫切れ、無効になっている場合、ストアフロントの並べ替えオプションは無効になります。

- An _Admin_ いずれかの項目が在庫切れまたは無効な場合でも、並べ替えることができます。

## 顧客の並べ替えを許可するようにを設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Sales]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Reorder]** セクション。

   ![オプションの並べ替え](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Allow Reorder]** 対象： `Yes`.

   この設定により、管理者のストアフロントまたは注文リストの顧客アカウントから機能を並べ替えることができます。

1. クリック **[!UICONTROL Save Config]**.

## ストアフロントから並べ替え

顧客は、次の 2 つのページから特定の注文の並べ替え機能を開始できます。

- _マイ注文_ ページ

- _Order View_ ページ

### マイ注文

この _並べ替え_ ボタンは、常に注文と共にリストに表示されます（注文のすべての製品を並べ替えに使用できない場合も含む）。

![ストアフロントの例 – My Orders ページ](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**ケース 1.** 注文に含まれるすべての製品は次のとおりです **available** 並べ替え用

ユーザーは買い物かごにリダイレクトされ、すべての製品が買い物かごに追加されます

![ショッピングカート](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**ケース 2.** 注文の一部/すべての商品は次のとおりです **利用できません** 並べ替え用

>[!NOTE]
>
>並べ替えは可能です `Not Visible Individually` 製品。

この _並べ替え_ ボタンがに表示されない _マイ注文_ および _注文を表示_ ページ。

![マイ注文ページ 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### 注文ビューページ

**ケース 1.** 注文のすべての製品は再注文できます

ユーザーは買い物かごにリダイレクトされ、すべての製品が買い物かごに追加されます

**ケース 2.** 注文の一部/すべての商品は次のとおりです **利用できません** 並べ替え用

>[!NOTE]
>
>並べ替えは可能です `Not Visible Individually` 製品。

この _並べ替え_ ボタンがに表示されない _マイ注文_ および _注文を表示_ ページ。

![注文の詳細ページ](./assets/order-view-page.png){width="700" zoomable="yes"}

### 買い物かごが空ではありません

買い物かごが空でなく、ユーザーがクリックした場合 **[!UICONTROL Reorder]** （から _マイ注文_  または _Order View_ （ページ）、既存の製品は、追加された並べ替え製品を使用して買い物かごに残ります。

![項目の並べ替え](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## 管理者から並べ替え

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 注文を見つけて、で開きます。 **[!UICONTROL View]** モード。

1. クリック **[!UICONTROL Reorder]** 上部のボタンバーに表示されます。

   ![注文の詳細：管理者](./assets/order-view-admin.png){width="600" zoomable="yes"}

   クリックした後 **[!UICONTROL Reorder]**, _新しい注文を作成_ 製品を並べ替えるとページが開きます。

   ![並べ替えを作成](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. 必要に応じて、すべての必須フィールドに入力します。

1. 注文を送信するには、 **[!UICONTROL Submit Order]**.
