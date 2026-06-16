---
title: キャンセル注文を許可
description: お客様に解約機能を提供する方法について説明します。
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
TQID: https://experienceleague.adobe.com/a0jMKgF4a0qXUe15oT2syai6-kGSegU1BX56PO9SSKs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# キャンセル注文を許可

有効にすると、顧客のアカウントから直接注文をキャンセルできます。 キャンセルはデフォルトで無効になっています。

## 注文に対してキャンセルを有効にするための条件

- _注文キャンセルを許可_&#x200B;設定オプションを有効にする必要があります。

- 注文のステータスが`Hold`、`Canceled`、`Complete`、または`Closed`の場合、ストアフロントでキャンセル オプションは無効になります。

- 注文の商品のいずれかが出荷された場合、ストアフロントでキャンセルオプションは無効になります。

- 支払った商品がある場合は、キャンセル オプションが有効になり、その商品の払い戻しが作成されます。

- 注文のステータスが`Pending`または`Processing`の場合、ストアフロントでキャンセルオプションが有効になります。

## お客様の解約を許可するように設定し、解約理由をカスタマイズします

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Sales]**&#x200B;を選択します。

1. **[!UICONTROL Order cancellation]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![注文キャンセルのオプション &#x200B;](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. **[!UICONTROL Order cancellation through GraphQL]**&#x200B;を`Yes`に設定します。

   この設定により、ストアフロントの顧客アカウントからキャンセル機能が有効になります。

1. **[!UICONTROL Order Order cancellation reasons]**&#x200B;では、キャンセル理由を追加、削除、または変更できます。

   この設定では、注文をキャンセルする際に、キャンセル理由がストアフロントに表示されます。
少なくとも1つの理由を指定していることを確認してください。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

## ストアフロントからキャンセル

お客様は、次の3つのページから特定の注文のキャンセル機能を開始できます。

- _マイオーダー_ ページ

- _注文表示_ ページ

- _自分のアカウント_ ページ

### マイオーダー

注文をキャンセルできる場合は、_注文をキャンセル_ ボタンがマイオーダーページに表示されます。

![&#x200B; ストアフロントの例 – マイオーダーのページ &#x200B;](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### 注文表示ページ

注文をキャンセルできる場合は、_注文をキャンセル_ ボタンが「注文を表示」ページに表示されます。

![注文の詳細ページ &#x200B;](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### マイアカウント

注文をキャンセルできる場合は、マイアカウントページの「最近使用した注文」セクションに「_注文をキャンセル_」ボタンが表示されます。

![自分のアカウントページ &#x200B;](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
