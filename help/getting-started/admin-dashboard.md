---
title: 管理ダッシュボード
description: 管理者ダッシュボード（通常はログイン時に表示される最初のページ）について説明します。
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# 管理ダッシュボード

ダッシュボードは、通常、にログインしたときに表示される最初のページです。 _Admin_ また、販売と顧客活動の概要をリアルタイムで提供できます。 ダッシュボードデータは、ライフタイム販売、平均注文額、最近の注文、検索語句のスナップショットを提供します。 グラフには、選択した日付範囲の完了済み注文と金額が表示され、動的、リアルタイム データ、または過去の集計データから生成できます。 下部のタブには、最も売れた製品、最も多く閲覧された製品、新規顧客、最も多く購入した顧客のクイックレポートが表示されます。

処理するデータが大量にある場合は、パフォーマンスを向上させるためにグラフをオフにできます。 次の例のダッシュボードは、リアルタイムデータを使用するように設定されており、過去 24 時間の完了済み注文を時間別に表示します。 グラフは、完了した注文ごとに更新されます。

![Dashboard](./assets/dashboard-full.png){zoomable="yes"}

[高度なレポート](business-intelligence.md#advanced-reporting) は、製品、注文、顧客のデータに基づいてパーソナライズされたダッシュボードを表示します。

![高度なレポート](./assets/dashboard-advanced-reporting.png){zoomable="yes"}

## ダッシュボードの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**次のいずれかの設定を行います。

1. 設定が完了したら、 **[!UICONTROL Save Config]**.

1. 変更を保存したら、 **[!UICONTROL Cache Management]** 無効なキャッシュをすべて更新します。

### グラフを有効にする

処理するデータが大量にある場合は、パフォーマンスを向上させるためにグラフの表示をオフにできます。 有効になっていない場合は、グラフの代わりに「データが見つかりません」というメッセージが表示されますが、下の概要合計は引き続き生成されます。

1. の下の左側のナビゲーションパネル **[!UICONTROL Advanced]**、を選択 **[!UICONTROL Admin]**.

1. 必要に応じて、 **[!UICONTROL Dashboard]** セクション。

   ![詳細設定 – グラフを有効にします](./assets/admin-dashboard-config.png){width="600"}

1. デフォルト値を変更するには、 **[!UICONTROL Use system value]** チェックボックス。

1. を設定 **グラフを有効にする** 対象： `Yes`.

管理者設定オプションについて詳しくは、を参照してください。 [設定リファレンスガイド](../configuration-reference/advanced/admin.md).

### スタートアップページの変更

ダッシュボードがデフォルトです [スタートアップページ](../configuration-reference/advanced/admin.md) 管理者の場合は、別のスタートアップページを設定できます。

1. 管理設定オプションをまだ開いていない場合は、次を選択します **[!UICONTROL Admin]** 未満 _[!UICONTROL Advanced]_左側のナビゲーションパネルで以下を実行します。

1. をクリックして、 **スタートアップページ** セクション。

   ![管理ダッシュボード – スタートアップページの設定](./assets/admin-startup-page.png){width="600"}

1. をクリア **[!UICONTROL Use system value]** チェックボックスで、 **スタートアップページ** 管理者にログインしたときに表示する名前。

### 開始日を選択

1. の下の左側のナビゲーションパネル **[!UICONTROL General]**、を選択 **報告書**.

1. ページで、を展開します **[!UICONTROL Dashboard]** セクション。

1. をクリア **[!UICONTROL Use system value]** 日付設定のチェックボックスをオンにし、次の手順を実行します。

   - を設定 **年初から年初まで** に **月** および **日**.

   - を設定 **今月の開始日** に **日**.

   ![管理ダッシュボード – 日付設定](./assets/reports-dashboard.png){width="600"}

について [!UICONTROL Reports] 設定オプションについては、を参照してください [_設定リファレンスガイド_](../configuration-reference/general/reports.md).

### データソースの設定

ダッシュボードグラフは、リアルタイムで生成することも、履歴の集計データを使用して生成することもできます。 パフォーマンスに問題がある場合は、集計データを使用して処理を高速化できます。

1. 左側のナビゲーションパネルでをクリックして展開します **売上** を選択します **売上** その下に。

1. ページで、を展開します **[!UICONTROL Dashboard]** セクション。

   ![管理ダッシュボード – データソース設定](./assets/config-sales-dashboard.png){width="600"}

1. をクリア **[!UICONTROL Use system value]** チェックボックスとセット **[!UICONTROL Use Aggregated Data]** を次のいずれかに変更します。

   - 履歴データと集計データの場合は、 `Yes`.
   - リアルタイムデータの場合は、を選択します。 `No`.

## グラフセクション

| セクション | 説明 |
|--- |--- |
| [!UICONTROL Orders] | このタブには、現在の店舗表示と指定した期間について、完了したすべての注文のリアルタイムグラフが表示されます。 |
| [!UICONTROL Amounts] | このタブには、現在の店舗表示と指定した期間について、完了したすべての注文金額のリアルタイムグラフが表示されます。 |
| [!UICONTROL Time Range] | 以下のグラフおよび概要の合計で表されるデータを決定します。 オプション： `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | グラフの下の収益、税、出荷、数量の合計は、グラフのデータと現在の時間範囲設定に基づいています。 |

{style="table-layout:auto"}

## スナップショットデータ

| セクション | 説明 |
|--- |--- |
| [!UICONTROL Lifetime Sales] | 店舗の有効期間中の集計総売上高。 |
| [!UICONTROL Average Order] | ストアの有効期間中の平均注文額。 |
| [!UICONTROL Last Orders] | 最後に行われた 5 件の注文の概要。 |
| [!UICONTROL Last Search Terms] | 最後の 5 つの検索語句。 |
| [!UICONTROL Top Search Terms] | 最もよく使用される 5 つの検索用語。 |

{style="table-layout:auto"}

## 「レポート」タブ

| セクション | 説明 |
|--- |--- |
| [!UICONTROL Bestsellers] | 指定された期間内に最も売れた 5 つの製品。 |
| [!UICONTROL Most Viewed Products] | その期間に閲覧された商品が最も多かったのは、5 つの商品です。 |
| [!UICONTROL New Customers] | 指定した期間にアカウントに登録した最新の 5 人の顧客。 |
| [!UICONTROL Customers] | 指定した期間内に処理を完了した注文の最後の 5 人の顧客。 |

{style="table-layout:auto"}

## ダッシュボードボタン

| ボタン | 説明 |
|--- |--- |
| [!UICONTROL Reload Data] | ダッシュボードデータを更新します。 |
| [!UICONTROL Go to Advanced Reporting] | 製品、注文および顧客データに基づいて、動的グラフおよびレポートのパーソナライズされたダッシュボードを表示します。 より詳細な分析については、を参照してください [高度なレポート](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
