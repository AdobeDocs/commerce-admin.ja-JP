---
title: ストックメッセージのシナリオ
description: 商品ページの在庫状況メッセージと、カタログページの商品リストの在庫状況メッセージを制御する設定の組み合わせについて説明します。
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/9kPHtr75C7PkM9vD-2-AeG8JnAfKAao0GKEH9MhkBbU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 1%

---

# ストックメッセージのシナリオ

構成設定を組み合わせて使用すると、商品ページおよびカタログページの商品リストの在庫状況メッセージを制御できます。

![商品をグループ化し、「在庫切れ」メッセージを表示](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## 製品ページのストックメッセージ

在庫の管理設定と在庫状況の設定の組み合わせに応じて、商品ページで利用できるメッセージにはいくつかのバリエーションがあります。

### 例1：可用性メッセージの表示

#### シナリオ 1

この設定の組み合わせにより、各製品の在庫状況に応じて、在庫状況メッセージが製品ページに表示されます。

| Stock オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### シナリオ 2

商品の在庫が管理されていない場合、この設定の組み合わせを使用して、商品ページに在庫状況メッセージを表示できます。

| Stock オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### 例2：可用性メッセージの非表示

#### シナリオ 1

この設定と製品設定の組み合わせにより、製品ページに可用性メッセージが表示されなくなります。

| Stock オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | なし |
|  | `Out of Stock` | なし |

#### シナリオ 2

製品の在庫が管理されていない場合、設定と製品設定を組み合わせることで、製品ページに可用性メッセージが表示されなくなります。

| Stock オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | なし |

## カタログページのストックメッセージ

製品の可用性と設定に応じて、カテゴリと検索結果リストに対して次の表示オプションを使用できます。

カテゴリーページの![在庫切れメッセージ ](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### 例1:「在庫切れ」のメッセージを表示する

この設定の組み合わせでは、カテゴリおよび検索結果リストに在庫切れ商品が含まれ、「在庫切れ」メッセージが表示されます。

| Stock オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | なし |

### 例2:「在庫切れ」メッセージを含まない商品の表示

この設定の組み合わせでは、カテゴリおよび検索結果リストに在庫切れの商品が含まれますが、メッセージは表示されません。

| Stock オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | なし |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### 例3：在庫が戻るまで商品を非表示にする

この設定では、在庫が戻るまで、カテゴリと検索結果リストから完全に在庫切れの商品が除外されます。

| Stock オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | なし |
