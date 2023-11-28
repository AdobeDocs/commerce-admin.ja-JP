---
title: 再注文を許可
description: 顧客に並べ替え機能を提供する方法を説明します。
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# 再注文を許可

有効にすると、顧客アカウントから直接、または _管理者_. リオーダーは、デフォルトで有効になっています。

![管理画面の顧客の並べ替えリンク](./assets/customer-reorder.png){width="700" zoomable="yes"}

## 注文に対して並べ替えを有効にするための条件

- The _並べ替えを許可_ 設定オプションを有効にする必要があります。

- 順序が次の中にある場合 `Hold` または `Payment Review` 「 」ステータスの場合、「並べ替え」オプションは無効になっています。

- 注文した項目のいずれかが使用できない場合、在庫切れの場合、または無効の場合、ストアフロントでは並べ替えオプションが無効になります。

- An _管理者_ は、在庫切れや無効になっている項目があった場合でも並べ替えることができます。

## 顧客の再注文を許可するように設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Reorder]** 」セクションに入力します。

   ![並べ替えオプション](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Allow Reorder]** から `Yes`.

   この設定により、ストアフロントの顧客アカウントまたは管理の注文リストから並べ替え機能が有効になります。

1. クリック **[!UICONTROL Save Config]**.

## ストアフロントから並べ替え

顧客は、特定の注文に対して、次の 2 つのページから並べ替え機能を開始できます。

- _注文_ ページ

- _注文ビュー_ ページ

### 注文

The _並べ替え_ ボタンは常に「注文」リストに表示されます（注文のすべての製品が並べ替えに使用できない場合でも）。

![ストアフロントの例 — マイ注文ページ](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**例 1.** 注文からのすべての製品は **利用可能** 並べ替え

ユーザーは買い物かごにリダイレクトされ、すべての製品が買い物かごに追加されます

![買い物かご](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**例 2.** 注文の一部またはすべての製品が **使用不可** 並べ替え

>[!NOTE]
>
>並べ替えは可能です `Not Visible Individually` 製品。

The _並べ替え_ ボタンが _注文_ および _注文を表示_ ページ。

![マイ注文ページ 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### 注文ビューページ

**例 1.** 注文のすべての製品を並べ替えに使用できます

ユーザーは買い物かごにリダイレクトされ、すべての製品が買い物かごに追加されます

**例 2.** 注文の一部またはすべての製品が **使用不可** 並べ替え

>[!NOTE]
>
>並べ替えは可能です `Not Visible Individually` 製品。

The _並べ替え_ ボタンが _注文_ および _注文を表示_ ページ。

![注文の詳細ページ](./assets/order-view-page.png){width="700" zoomable="yes"}

### 買い物かごが空ではありません

買い物かごが空でなく、ユーザーがクリックした場合 **[!UICONTROL Reorder]** ( _注文_  または _注文ビュー_ 」ページを参照 )、既存の製品は、追加された製品の並べ替えと共にカート内に残ります。

![項目の並べ替え](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## 管理から並べ替え

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 順序を探し、次の場所で開きます。 **[!UICONTROL View]** モード。

1. クリック **[!UICONTROL Reorder]** 上部のボタンバーに表示される

   ![管理者での注文の詳細](./assets/order-view-admin.png){width="600" zoomable="yes"}

   次をクリックした後： **[!UICONTROL Reorder]**、 _新しい注文を作成_ ページが開き、製品が並べ替えられます。

   ![並べ替えを作成](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. 必要に応じて、すべての必須フィールドに入力します。

1. 注文を送信するには、 **[!UICONTROL Submit Order]**.
