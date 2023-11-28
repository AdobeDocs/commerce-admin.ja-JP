---
title: 在庫メッセージのシナリオ
description: 製品ページの在庫状況メッセージを制御する構成設定の組み合わせと、カタログページの製品のリストについて説明します。
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 在庫メッセージのシナリオ

設定の組み合わせを使用して、製品ページ上の在庫状況メッセージや、カタログページ上の製品のリストでの在庫状況メッセージを制御できます。

![「在庫切れ」メッセージ付きのグループ化された製品](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## 製品ページの在庫メッセージ

「在庫を管理」と「在庫の可用性」の設定の組み合わせに応じて、製品ページで使用できるメッセージには様々なバリエーションがあります。

### 例 1：可用性メッセージを表示する

#### シナリオ 1

この設定の組み合わせにより、各製品の在庫状況に応じて、製品ページに可用性メッセージが表示されます。

| 在庫オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### シナリオ 2

在庫が製品に対して管理されていない場合、この設定の組み合わせを使用して、製品ページに可用性メッセージを表示できます。

| 在庫オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### 例 2：可用性メッセージを非表示にする

#### シナリオ 1

この設定と製品設定の組み合わせにより、可用性メッセージが製品ページに表示されなくなります。

| 在庫オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | なし |
|  | `Out of Stock` | なし |

#### シナリオ 2

在庫が製品に対して管理されていない場合、この設定と製品設定の組み合わせによって、製品ページに可用性メッセージが表示されなくなります。

| 在庫オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | なし |

## カタログページの在庫メッセージ

製品の可用性と構成の設定に応じて、カテゴリと検索結果のリストに対して次の表示オプションが可能です。

![カテゴリページの在庫切れメッセージ](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### 例 1:「在庫切れ」というメッセージが表示される製品

この設定の組み合わせには、カテゴリおよび検索結果リストに在庫切れの製品が含まれ、「在庫切れ」メッセージが表示されます。

| 在庫オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | なし |

### 例 2:「在庫切れ」というメッセージを表示せずに製品を表示する

この設定の組み合わせには、カテゴリおよび検索結果リストに在庫切れの製品が含まれますが、メッセージは表示されません。

| 在庫オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | なし |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### 例 3：在庫が再び入るまで製品を非表示にする

この設定では、在庫が戻るまで、カテゴリと検索結果のリストから完全に在庫品目が除外されます。

| 在庫オプション | 設定 | メッセージ |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | なし |
