---
title: 管理ダッシュボード
description: Admin ダッシュボード（通常、ログイン時に表示される最初のページ）について説明します。
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# 管理ダッシュボード

通常、ダッシュボードは、 _管理者_ とは、販売と顧客活動の概要をリアルタイムで提供できます。 ダッシュボードデータには、全期間の売上、平均注文額、最近の注文件数、検索語句のスナップショットが表示されます。 グラフには、選択した日付範囲の完了した注文件数と合計数が表示され、動的データ、リアルタイムデータ、または履歴の集計データから生成できます。 下部のタブには、ベストセラー商品、最も多く閲覧された製品、新規顧客、最も多くを購入した顧客を示すクイックレポートが表示されます。

処理するデータ量が多い場合は、グラフをオフにしてパフォーマンスを向上させることができます。 次の例のダッシュボードは、リアルタイムデータを使用するように設定されており、過去 24 時間の時間別に完了注文を表示します。 完了した注文ごとにグラフが更新されます。

![ダッシュボード](./assets/dashboard-full.png){zoomable=&quot;yes&quot;}

[高度なレポート機能](business-intelligence.md#advanced-reporting) は、製品、注文、顧客データに基づいてパーソナライズされたダッシュボードを表示します。

![高度なレポート機能](./assets/dashboard-advanced-reporting.png){zoomable=&quot;yes&quot;}

## ダッシュボードの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**次のいずれかの設定を行います。

1. 設定が完了したら、「 **[!UICONTROL Save Config]**.

1. 変更を保存したら、 **[!UICONTROL Cache Management]** 無効なキャッシュをすべて更新します。

### グラフを有効にする

処理するデータ量が多い場合は、グラフの表示をオフにしてパフォーマンスを向上させることができます。 有効にしない場合、以下の要約合計は生成されますが、グラフの代わりに「データが見つかりません」というメッセージが表示されます。

1. 左側のナビゲーションパネルで、 **[!UICONTROL Advanced]**&#x200B;を選択します。 **[!UICONTROL Admin]**.

1. 必要に応じて、を展開します。 **[!UICONTROL Dashboard]** 」セクションに入力します。

   ![詳細設定 — グラフを有効にする](./assets/admin-dashboard-config.png){width="600"}

1. デフォルト値を変更するには、 **[!UICONTROL Use system value]** チェックボックス。

1. 設定 **グラフを有効にする** から `Yes`.

管理者設定オプションについて詳しくは、 [設定リファレンスガイド](../configuration-reference/advanced/admin.md).

### スタートアップページを変更する

ダッシュボードがデフォルトです [スタートアップページ](../configuration-reference/advanced/admin.md) 管理者の場合は、別の起動ページを設定できます。

1. まだ管理者設定オプションを開いていない場合は、 **[!UICONTROL Admin]** under _[!UICONTROL Advanced]_（左側のナビゲーションパネル）

1. をクリックして、 **起動ページ** 」セクションに入力します。

   ![管理ダッシュボード — 起動ページの設定](./assets/admin-startup-page.png){width="600"}

1. 次をクリア： **[!UICONTROL Use system value]** チェックボックスをオンにして、 **起動ページ** 管理者にログインする際に表示する

### 開始日を選択

1. 左側のナビゲーションパネルで、 **[!UICONTROL General]**&#x200B;を選択します。 **レポート**.

1. ページで、「 **[!UICONTROL Dashboard]** 」セクションに入力します。

1. 次をクリア： **[!UICONTROL Use system value]** 日付設定のチェックボックスをオンにし、次の操作を行います。

   - 設定 **年初から日まで** から **月** および **日**.

   - 設定 **今月の開始** から **日**.

   ![管理ダッシュボード — 日付設定](./assets/reports-dashboard.png){width="600"}

詳しくは、 [!UICONTROL Reports] 設定オプション ( [_設定リファレンスガイド_](../configuration-reference/general/reports.md).

### データソースの設定

ダッシュボードのグラフは、リアルタイムで生成することも、履歴の集計データを使用して生成することもできます。 パフォーマンスが問題の場合は、集計データを使用してスピードアップできます。

1. 左側のナビゲーションパネルで、をクリックして展開します。 **セールス** を選択します。 **セールス** の下に

1. ページで、「 **[!UICONTROL Dashboard]** 」セクションに入力します。

   ![管理ダッシュボード — データソース設定](./assets/config-sales-dashboard.png){width="600"}

1. 次をクリア： **[!UICONTROL Use system value]** チェックボックスとセット **[!UICONTROL Use Aggregated Data]** を次のいずれかに変更します。

   - 履歴の集計データの場合は、 `Yes`.
   - リアルタイムデータの場合は、 `No`.

## グラフのセクション

| セクション | 説明 |
|--- |--- |
| [!UICONTROL Orders] | このタブには、現在のストア表示の完了済み注文件数と指定された期間のリアルタイムのグラフが表示されます。 |
| [!UICONTROL Amounts] | このタブには、現在のストア表示と指定した期間の完了注文額のすべてをリアルタイムで示すグラフが表示されます。 |
| [!UICONTROL Time Range] | 以下のグラフおよび集計合計に表示されるデータを決定します。 オプション： `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | グラフの下の売上高、税金、送料、数量の合計は、グラフのデータと現在の時間範囲の設定に基づいています。 |

{style="table-layout:auto"}

## スナップショットデータ

| セクション | 説明 |
|--- |--- |
| [!UICONTROL Lifetime Sales] | 店舗の全期間の合計売上高。 |
| [!UICONTROL Average Order] | ストアの有効期間内の平均注文額。 |
| [!UICONTROL Last Orders] | 最近 5 回の注文の概要。 |
| [!UICONTROL Last Search Terms] | 最近 5 つの検索語句。 |
| [!UICONTROL Top Search Terms] | 最もよく使用される検索用語の 5 つ。 |

{style="table-layout:auto"}

## レポートタブ

| セクション | 説明 |
|--- |--- |
| [!UICONTROL Bestsellers] | 指定した期間のベストセラー商品 5 つ。 |
| [!UICONTROL Most Viewed Products] | 指定期間中に最も多く閲覧された 5 つの製品。 |
| [!UICONTROL New Customers] | 指定した期間に特定のアカウントに登録した最新の 5 人の顧客。 |
| [!UICONTROL Customers] | 指定した期間に処理を完了した注文を持つ直近 5 人の顧客。 |

{style="table-layout:auto"}

## ダッシュボードボタン

| ボタン | 説明 |
|--- |--- |
| [!UICONTROL Reload Data] | ダッシュボードデータを更新します。 |
| [!UICONTROL Go to Advanced Reporting] | 製品、注文、顧客データに基づいて、動的なグラフとレポートのパーソナライズされたダッシュボードを表示します。 詳細な分析については、 [高度なレポート機能](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
