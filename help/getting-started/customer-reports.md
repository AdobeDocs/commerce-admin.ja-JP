---
title: 顧客レポート
description: Adobe CommerceとMagento Open Sourceで使用できる顧客レポートでは、指定した期間または日付範囲における顧客のアクティビティに関するインサイトを得ることができます。
exl-id: 7bee414b-b605-4aed-9749-78bb8056a6a4
feature: Customers, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 1%

---

# 顧客レポート

顧客レポートは、指定した期間または日付範囲における顧客のアクティビティに関するインサイトを提供します。

## [!UICONTROL Order Total Report]

この [!UICONTROL Order Total Report] 指定した期間または日付範囲の顧客の注文を表示します。 レポートには、顧客あたりの注文数、平均注文額、合計金額が含まれます。

日 _Admin_ サイドバー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL Order Total]**.

![注文合計レポート](./assets/customers-order-total.png){width="600"}

### ワークスペースコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL From / To] | 開始日と終了日に基づいて注文の検索を定義するために使用します。 |
| [!UICONTROL Show By] | 注文レコード分割の精度を定義します。 オプション： `Month` / `Day` / `Year` |
| [!UICONTROL Refresh] | 指定したフィルターにグリッドを更新します。 |
| [!UICONTROL Export] | 選択したレコードを CSV または Excel XML ファイルとしてエクスポートします。 |
| [!UICONTROL Scope] | レポートの生成対象となるサイトまたはストアを設定するために使用されます。 |

{style="table-layout:auto"}

### 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Interval] | 注文の合計間隔（） `Month` / `Day` / `Year`. |
| [!UICONTROL Customer] | 注文を行った顧客の名前。 |
| [!UICONTROL Orders] | 指定した期間の注文数。 |
| [!UICONTROL Average] | 平均注文額。 |
| [!UICONTROL Total] | 期間のすべての注文の合計。 |

{style="table-layout:auto"}

## [!UICONTROL Order Count Report]

この [!UICONTROL Order Count Report] 指定した時間間隔または日付範囲での、顧客ごとの注文数を表示します。 レポートには、顧客あたりの注文数、平均注文額、合計金額が含まれます。

日 _Admin_ サイドバー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL Order Count]**.

![注文数レポート](./assets/customer-order-count.png){width="600"}

### ワークスペースコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL From / To] | 開始日と終了日に基づいて注文の検索を定義するために使用します。 |
| [!UICONTROL Show By] | 注文レコード分割の精度を定義します。 オプション： `Month` / `Day` / `Year` |
| [!UICONTROL Refresh] | 指定したフィルターにグリッドを更新します。 |
| [!UICONTROL Export] | 選択したレコードを CSV または Excel XML ファイルとしてエクスポートします。 |
| [!UICONTROL Scope] | レポートの生成対象となるサイトまたはストアを設定するために使用されます。 |

{style="table-layout:auto"}

### 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Interval] | 順序数の間隔 `Month` / `Day` / `Year`. |
| [!UICONTROL Customer] | 注文を行った顧客。 |
| [!UICONTROL Orders] | 指定した期間の注文数。 |
| [!UICONTROL Average] | 平均注文額。 |
| [!UICONTROL Total] | 期間のすべての注文の合計。 |

{style="table-layout:auto"}

## [!UICONTROL New Accounts Report]

この [!UICONTROL New Accounts Report] 指定した期間または日付範囲で開設された新規カスタマー・アカウントの数を表示します。

日 _Admin_ サイドバー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL New]**.

![新規アカウントレポート](./assets/customers-new-accounts.png){width="600"}

### ワークスペースコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL From / To] | 開始日と終了日に基づいて新しいアカウントの検索を定義するために使用します。 |
| [!UICONTROL Show By] | 注文レコード分割の精度を定義します。 オプション：月/日/年 |
| [!UICONTROL Refresh] | 指定したフィルターにグリッドを更新します。 |
| [!UICONTROL Export] | 選択したレコードを CSV または Excel XML ファイルとしてエクスポートします。 |
| [!UICONTROL Scope] | レポートの生成対象となるサイトまたはストアを設定するために使用されます。 |

{style="table-layout:auto"}

### 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Interval] | 新規アカウントの作成間隔（月/日/年別）。 |
| [!UICONTROL New Accounts] | 特定の間隔で作成された新しいアカウントの数。 |

{style="table-layout:auto"}

## [!UICONTROL Customer Wish List Report]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

この [!UICONTROL Customer Wish List Report] 顧客のウィッシュリストに関する情報を提供します。

日 _Admin_ サイドバー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL Wish Lists]**.

![ウィッシュリストレポート](./assets/customer-wish-list.png){width="600"}

### ワークスペースコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL Scope] | レポートの生成対象となるサイトまたはストアを設定するために使用されます。 |
| [!UICONTROL Search] | 指定されたパラメータによる検索を開始します。 |
| [!UICONTROL Reset Filter] | すべての検索パラメーターのリセットを開始します。 |
| [!UICONTROL Per Page] | 1 つのページに表示されるレコードの数を設定します。 |
| [!UICONTROL Export] | 選択したレコードを CSV または Excel XML ファイルとしてエクスポートします。 |
| [!UICONTROL From / To] | 開始日と終了日に基づいてウィッシュリストの検索を定義するために使用されます。 |
| [!UICONTROL Wishlist] | 名前によるウィッシュリスト検索を開始します。 |
| [!UICONTROL Status] | ウィッシュリストのステータス。 オプション： `Private` / `Public` |
| [!UICONTROL Comment] | ウィッシュリストのコメントのテキストで検索を開始します。 |

{style="table-layout:auto"}

### 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Added] | ウィッシュリストが作成された日付。 |
| [!UICONTROL Customer] | ウィッシュリストを作成した顧客の姓と名 |
| [!UICONTROL Wishlist] | ウィッシュリストの名前。 |
| [!UICONTROL Status] | ウィッシュリストのステータス。 オプション： `Private` / `Public` |
| [!UICONTROL Product] | ウィッシュリストに追加された商品の名前。 |
| [!UICONTROL SKU] | ウィッシュリストに追加された商品の SKU。 |
| [!UICONTROL Comment] | ウィッシュリストの作成時に入力されたコメントテキスト。 |

{style="table-layout:auto"}

## [!UICONTROL Customer Segment Report]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

この [!UICONTROL Customer Segment Report] は、各セグメントの顧客数に関する情報を提供します。

日 _Admin_ サイドバー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Customers]_>**[!UICONTROL Segments]**.

![セグメントレポート](./assets/customers-segments.png){width="600"}

### ワークスペースコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL Search] | 指定されたパラメータによる検索を開始します。 |
| [!UICONTROL Reset Filter] | すべての検索パラメーターのリセットを開始します。 |
| [!UICONTROL Action] | セグメントの表示をパラメーターで開始します。 オプション： `Action` / `View Combined Report` |
| [!UICONTROL Per Page] | 1 つのページに表示されるレコードの数を設定します。 |

{style="table-layout:auto"}

### 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 各セグメントに割り当てられる一意の数値識別子。 |
| [!UICONTROL Segment] | セグメント名。 |
| [!UICONTROL Status] | セグメントステータス。 オプション： `Active` / `Inactive` |
| [!UICONTROL Website] | セグメントが割り当てられている web サイト。 |
| [!UICONTROL Customers] | セグメントに割り当てられた顧客の数。 |

{style="table-layout:auto"}
