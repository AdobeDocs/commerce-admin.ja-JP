---
title: 注文件数
description: 注文ワークスペースと、管理で注文を見つけるために使用する検索機能について説明します。
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
feature: Orders, Admin Workspace
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1204'
ht-degree: 0%

---

# 注文件数

この _注文件数_ グリッドは、現在のすべての注文を一覧表示し、それらの進行状況を追跡します。 [注文ステータス](order-status.md) 経由 [ワークフロー](order-processing.md). 基本的なプロセスを簡単に理解するには、注文が [請求書](invoices.md)を選択すると、請求書は [出荷](shipments.md). グリッドはプロセスの最初のステージを表し、ここで実行できます [更新](order-update.md) 既存の注文と注文の作成

通常、注文は顧客がストアフロントからチェックアウトプロセスを完了したときに作成されます。 ただし、サポートが必要なお客様は、 [ショッピングカート](shopping-assisted-cart-manage.md) または [オーダーの作成](customer-account-create-order.md) 次のいずれかから _注文件数_ 顧客アカウントから直接またはグリッド化します。

## 注文ワークスペース

注文ワークスペースには、現在のすべての注文が一覧表示され、既存の注文とを編集できます [作成](customer-account-create-order.md) オーダー。 グリッドの各行は顧客の注文を表し、各列は属性（データフィールド）を表します。 標準を使用 [制御](../getting-started/admin-grid-controls.md) リストを並べ替えてフィルターするには、順序を検索し、適用します [アクション](../getting-started/admin-actions-control.md) を選択した注文に対して行います。 ページネーションコントロールの上にあるタブを使用すると、リストのフィルタリング、デフォルトの表示の変更、列の変更と並べ替え、データの書き出しを行うことができます。

![注文グリッド](./assets/orders-grid.png){width="700" zoomable="yes"}

### グリッドレイアウト

列の選択とグリッド内の順序は、必要に応じて変更できます。 新しいレイアウトは、グリッドとして保存できます _表示_. デフォルトでは、使用可能な 20 列のうち、9 列のみがグリッドに含まれます。

![グリッド列の順序](./assets/order-grid-columns.png){width="600" zoomable="yes"}

#### 列の選択の変更

右上隅のをクリックします _列_ （ ![列設定](../assets/icon-columns.png) ）を制御し、次の操作を行います。

- グリッドに追加する任意の列のチェックボックスをオンにします。
- グリッドから削除する列のチェックボックスをオフにします。

#### 列の選択をリセット

1. 「」をクリックします _列_ （ ![列設定](../assets/icon-columns.png) ） コントロールします。

1. グリッド列をリセットするには、をクリックします。 **[!UICONTROL Reset]**.

   グリッドのレイアウトは表示のみに変更されます [デフォルトの列](#column-descriptions).

#### 列の移動

1. 列のヘッダーをクリックしたままにします。

1. 列を新しい位置にドラッグして、マウスボタンを放します。

#### グリッド表示の保存

1. 「」をクリックします **[!UICONTROL View]** （ ![目のアイコン](../assets/icon-view-eye.png) ） コントロールします。

1. クリック **[!UICONTROL Save Current View]**.

1. を入力 **[!UICONTROL name]** をビューに追加します。

1. すべての変更を保存するには、矢印（ ![矢印アイコン](../assets/icon-arrow-save.png) ）に設定します。

   ビューの名前が現在のビューとして表示されます。

#### ビューの変更

「」をクリックします **[!UICONTROL View]** （ ![目のアイコン](../assets/icon-view-eye.png) ） コントロールします。 次に、次のいずれかの操作を行います。

- 別のビューを使用するには、ビューの名前をクリックします。

- ビューの名前を変更するには、 _編集_ （ ![鉛筆アイコン](../assets/icon-edit-pencil.png) ）アイコンをクリックして、名前を更新します。

### ワークスペースコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL Create New Order] | オーダーを作成します。 参照： [オーダーの作成](customer-account-create-order.md) を参照してください。 |
| [!UICONTROL Go to Archive] | アーカイブ済オーダーのリストを表示します。 |
| [!UICONTROL Search] | 現在のフィルターに基づいて注文検索を開始します。 |
| [!UICONTROL Filters] | グリッドに表示されるレコードのフィルターに使用する検索パラメーターのセットを定義します。 |
| [!UICONTROL Default View] | グリッドの既定の列レイアウトを決定します。 |
| [!UICONTROL Columns] | グリッド内の列の選択と順序を決定します。 列のレイアウトは、変更して、 _表示_. デフォルトでは、一部の列のみがグリッドに含まれます。 |
| [!UICONTROL Export] | 選択したレコードを CSV または Excel XML ファイルとしてエクスポートします。 |

{style="table-layout:auto"}

### アクション

特定の注文にアクションを適用するには、各注文の最初の列にあるチェックボックスを選択します。 すべての注文を選択または選択解除するには、列の上部にあるコントロールを使用します。

![注文アクション](./assets/orders-action.png){width="600" zoomable="yes"}

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL Actions] | 選択した注文に適用できるすべてのアクションをリストします。 注文または注文グループにアクションを適用するには、各注文の最初の列にあるチェックボックスを選択します。 <br/>注文アクション : `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） |
| [!UICONTROL Mass Actions] | アクションのターゲットとして複数のレコードを選択する場合に使用できます。 アクションの対象となる各レコードの最初の列のチェックボックスを選択します。 オプション： `Select All` / `Unselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL Submit] | 選択した注文レコードに現在のアクションを適用します。 |
| [!UICONTROL Edit] | 注文を編集モードで開きます。 |

{style="table-layout:auto"}

### 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象とする引用符のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション：すべてを選択/すべてを選択解除 |
| [!UICONTROL ID] | 新しい注文が初めて保存されるときに割り当てられる一意の連続番号。 |
| [!UICONTROL Purchase Point] | 注文が行われたストア表示を識別します。 |
| [!UICONTROL Purchase Date] | 注文が行われた日時。 デフォルトのタイムゾーンに従って常に表示されます。 |
| [!UICONTROL Bill-to Name] | 注文の支払いを担当する人物の名前。 |
| [!UICONTROL Ship-to Name] | 注文を発送する相手の名前。 |
| [!UICONTROL Grand Total (Base)] | 注文の総計。 |
| [!UICONTROL Grand Total (Purchased)] | 注文で購入した製品の合計金額。 |
| [!UICONTROL Status] | 現在の注文ステータス。 |
| [!UICONTROL Action] | _[!UICONTROL View]_注文を編集モードで開きます。 |
| [!UICONTROL Allocated sources] | その特定の注文に割り当てられたソース。 |

{style="table-layout:auto"}

使用可能な追加の列：

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Billing Address] | 注文を行った顧客の請求先住所。 |
| [!UICONTROL Shipping Address] | 注文を発送する住所。 |
| [!UICONTROL Shipping Information] | 注文を発送するために使用される方法。 |
| [!UICONTROL Customer Email] | 注文を行った人物のメールアドレス。 |
| [!UICONTROL Customer Group] | 注文した人物が割り当てられる顧客グループ。 |
| [!UICONTROL Subtotal] | 出荷および処理を伴わない注文の小計および税金。 |
| [!UICONTROL Shipping and Handling] | 出荷および処理に対して請求される金額。 |
| [!UICONTROL Customer Name] | 注文を行った顧客の姓と名。 |
| [!UICONTROL Payment Method] | 注文に使用される支払い方法。 |
| [!UICONTROL Total Refunded] | 注文から顧客に払い戻される金額。 |
| [!UICONTROL Refunded to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）注文から顧客の店舗クレジットに払い戻される金額。 |
| [!UICONTROL Company Name] | ![Adobe Commerceの B2B](../assets/b2b.svg) （Adobe Commerceの B2B で使用可能）の名前 [会社](../b2b/account-companies.md) 注文した人物。 |

{style="table-layout:auto"}

## オーダー検索

[ 受注 ] グリッドの左上にある [ 検索 ] ボックスを使用すると、キーワードで特定の受注を検索したり、グリッド内の受注レコードをフィルタ処理することができます。

![検索結果](./assets/order-search.png){width="600" zoomable="yes"}

### 一致を検索

1. ページ検索ボックスに検索語句を入力します。

1. 結果を表示するには、をクリックします _検索_ （ ![虫眼鏡アイコン](../assets/icon-magnify-search.png) ）に設定します。

### 検索のフィルタリング

1. 検索フィルターの選択を表示するには、をクリックします _フィルター_ （ ![ファネルアイコン](../assets/icon-filter-search.png) ） タブを選択します。

   ![注文フィルター](./assets/order-search-filter.png){width="600" zoomable="yes"}

1. 検索する注文を説明するフィルターをいくつでも入力します。

1. クリック **[!UICONTROL Apply Filters]** をクリックして結果を表示します。

### フィルターを検索

| フィルター | 説明 |
|--- |--- |
| [!UICONTROL Purchase Date] | 購入日に基づいて検索をフィルターします。 日付範囲内の注文を検索するには、両方を入力します **[!UICONTROL from]** および **[!UICONTROL to]** 日付。 |
| [!UICONTROL ID] | 注文 ID に基づいて検索をフィルタリングします。 |
| [!UICONTROL Grand Total (Base)] | 注文の総計（注文に適用されたクレジットを含む）に基づいて検索をフィルタリングします。 |
| [!UICONTROL Grand Total (Purchased)] | 各注文で購入された品目の総計に基づいて検索をフィルターします。 |
| [!UICONTROL Bill-to Name] | 注文の支払いを担当する人物の名前に従って検索をフィルタリングします。 |
| [!UICONTROL Ship-to Name] | 各注文の出荷先の人物の名前に従って検索をフィルタリングします。 |
| [!UICONTROL Purchase Point] | 注文が行われた web サイト、ストア、またはストア表示で検索をフィルタリングします。 |
| [!UICONTROL Status] | 注文ステータスに基づいて検索をフィルタリングします。 オプション： `Canceled` / `Closed` / `Complete` / `Suspected Fraud` / `On Hold` / `Payment Review` / `PayPal Canceled Reversal` /` PayPal Reversed` /` Pending` / `Pending Payment` / `Pending PayPal` / `Processing` |
| [!UICONTROL Braintree Transaction Source] | 取引ソースに基づいて検索をフィルタリングします。 |

{style="table-layout:auto"}

### 検索ツール

| ツール | 説明 |
|--- |--- |
| [!UICONTROL Apply Filters] | すべてのフィルターを検索結果に適用します。 |
| [!UICONTROL Cancel] | 現在の検索をキャンセルします。 |
| [!UICONTROL Clear All] | すべての検索フィルターをクリアします。 |

{style="table-layout:auto"}

## リソースのトラブルシューティング

注文に関する問題のトラブルシューティングについて詳しくは、Commerce サポートナレッジベースの次の記事を参照してください。

- [注文表示エラー](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-known-issue-orders-display-error.html)
- [PayPal 重複注文 10415 エラー](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-6/mdva-31006-magento-patch-paypal-duplicate-orders-10415-error.html)
- [新しい注文がアーカイブに送信される](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/new-orders-are-sent-to-archive.html)
- [管理の注文グリッドに表示されない注文](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/orders-not-displayed-in-the-orders-grid-in-the-admin.html)
- [注文ステータス - REST API を使用して作成された誤った出荷](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-7/mdva-30972-magento-patch-order-status-incorrect-shipment-created-via-rest-api.html)
