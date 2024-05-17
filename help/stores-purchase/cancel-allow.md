---
title: 注文のキャンセルを許可
description: 顧客にキャンセル機能を提供する方法を説明します。
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
source-git-commit: a9d1dc4fe50e98f0f1dfc8ec204930e2cc885d6e
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# 注文のキャンセルを許可

有効にすると、顧客のアカウントから直接注文をキャンセルできます。 キャンセルはデフォルトで無効になっています。

## 注文のキャンセルを有効にする基準

- この _注文のキャンセルを許可_ 設定オプションを有効にする必要があります。

- 順序が次の中にある場合： `Hold`, `Canceled`, `Complete`、または `Closed` ステータスにより、ストアフロントで「キャンセル」オプションが無効になっています。

- 注文された商品のいずれかが出荷された場合、ストアフロントでキャンセルオプションが無効になります。

- 支払われた商品がある場合、キャンセルオプションが有効になり、その商品の払い戻しが作成されます。

- 順序が次の中にある場合： `Pending` または `Processing` ステータスが選択された場合、ストアフロントで「キャンセル」オプションが有効になります。

## 顧客のキャンセルを許可し、キャンセル理由をカスタマイズするように設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択して、 **[!UICONTROL Sales]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Order cancellation]** セクション。

   ![注文キャンセルオプション](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Order cancellation through GraphQL]** 対象： `Yes`.

   この設定により、ストアフロントの顧客アカウントからのキャンセル機能が有効になります。

1. が含まれる **[!UICONTROL Order Order cancellation reasons]** キャンセル理由を追加、削除または変更できます。

   この設定では、注文をキャンセルした際に、キャンセル理由が顧客に対してストアフロントに表示されます。
少なくとも 1 つの理由を指定したことを確認します。

1. クリック **[!UICONTROL Save Config]**.

## ストアフロントからのキャンセル

お客様は、次の 3 つのページから特定の注文のキャンセル機能を開始できます。

- _マイ注文_ ページ

- _Order View_ ページ

- _マイアカウント_ ページ

### マイ注文

この _注文をキャンセル_ 注文をキャンセルできる場合、「マイ注文」ページにボタンが表示されます。

![ストアフロントの例 – My Orders ページ](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### 注文ビューページ

この _注文をキャンセル_ 注文をキャンセルできる場合は、「注文を表示」ページにボタンが表示されます。

![注文の詳細ページ](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### マイアカウント

この _注文をキャンセル_ 注文をキャンセルできる場合は、マイアカウント ページの「最近の注文」セクションにボタンが表示されます。

![マイアカウントページ](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
