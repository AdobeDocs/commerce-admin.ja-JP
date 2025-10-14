---
title: サポートツール
description: システムの問題を特定するために使用できる、提供されているサポートツールについて説明します。
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: addde8c3e41b641712f5b08107c1d68b40cd4159
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# サポートツール

{{ee-feature}}

サポートツールは、システムの既知の問題を特定するように設計されています。 開発および最適化プロセス中のリソースとして、また、サポートチームが問題を特定して解決するのに役立つ診断ツールとして使用できます。

## システムレポート

システムレポートツールを使用すると、システムのスナップショットを定期的に完全または部分的に作成し、後で参照するために保存できます。 コード開発サイクルの前後のパフォーマンス設定や、サーバー設定に対する変更を比較できます。 システムレポートツールを使用すると、調査を開始するためにサポートが必要とする情報の準備と送信に費やす時間を大幅に短縮できます。

システムレポートグリッドでは、既存のレポートの表示とダウンロード、レポートの削除、レポートの作成を行うことができます。

### システムレポートへのアクセス

_管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Support]_/**[!UICONTROL System Report]**&#x200B;に移動します。

![&#x200B; 管理者 – システムレポート &#x200B;](./assets/reports.png){width="600" zoomable="yes"}

### レポートの生成

1. 「**[!UICONTROL New Report]**」をクリックします。

1. **[!UICONTROL Groups]** リストで、レポートに含める情報のセットを選択します。 デフォルトでは、すべてのグループが選択されます。

   ![&#x200B; システムレポート – グループを選択 &#x200B;](./assets/report-create.png){width="600" zoomable="yes"}

1. 右上隅の「**[!UICONTROL Create]**」をクリックします。

   選択したレポートタイプの数によっては、レポートの生成に数分かかることがあります。 レポートの準備が整うと、生成された日時と共にグリッドの上部に表示されます。

### モジュール情報の表示

インストールされているモジュールに関する有用な情報を確認できます。

**_インストールされている各モジュールのレポート情報を表示するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Support]_/**[!UICONTROL System Report]**&#x200B;に移動します。
1. 「**[!UICONTROL New Report]**」をクリックします。
1. リストから `Modules` を選 **[!UICONTROL Groups]** します。
1. 「**[!UICONTROL Create]**」をクリックします。
1. レポートが生成されたら、**[!UICONTROL Select]** をクリックし、**[!UICONTROL View]** をクリックして、すべてのモジュールバージョンを表示します。
1. 「**[!UICONTROL Download]**」をクリックして、レポートをダウンロードします。

### システムレポートの管理

グリッドの「**[!UICONTROL Action]**」列で、次のいずれかを選択します。

- `View` – この関数を使用して、レポートの詳細を表示します。
- `Delete` – この関数を使用して、生成されたレポートをリストから削除します。
- `Download` – この関数を使用して、レポートをHTML ファイルとして保存します。

### システムレポートの詳細の表示

1. 必要なレポートの _[!UICONTROL Actions]_&#x200B;列で「**[!UICONTROL View]**」を選択します。

1. 左側のパネルで ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、レポートの各セクションで詳細を表示します。

   ![&#x200B; システムレポートの一般情報 &#x200B;](./assets/report-information.png){width="600" zoomable="yes"}

### 使用可能なシステムレポート

| レポートグループ | 含まれる情報 |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerceのバージョン <br> データ数 <br> キャッシュステータス <br> インデックスステータス |
| [!UICONTROL Environment] | 環境情報 <br>MySQL ステータス |
| [!UICONTROL Data] | URL キーによる重複カテゴリ <br>URL キーによる重複製品 <br>SKU による重複製品 <br> 増分による重複注文 <br> メールによる重複ユーザー <br> 破損したカテゴリデータ |
| [!UICONTROL Modules] | カスタムモジュール一覧 <br> 無効なモジュール一覧 <br> すべてのモジュール一覧 |
| [!UICONTROL Configuration] | 構成 <br> 出荷方法 `app/etc/env.php`<br> 支払方法 <br> 支払機能マトリックスからのデータ <br> 支払機能 |
| [!UICONTROL Logs] | ログファイル <br> 上位のシステムメッセージ <br> 今日の上位のシステムメッセージ <br> 上位のデバッグメッセージ <br> 今日の上位のデバッグメッセージ <br> 上位の例外メッセージ <br> 今日の上位の例外メッセージ |
| [!UICONTROL Attributes] | ユーザー定義 EAV 属性 <br> 新規 EAV 属性 <br> エンティティ・タイプ <br> すべての EAV 属性 <br> カテゴリ EAV 属性 <br> 製品 EAV 属性 <br> 顧客 EAV 属性 <br> 顧客アドレス EAV 属性 <br>RMA 品目 EAV 属性 |
| [!UICONTROL Events] | カスタムグローバルイベント <br> カスタム管理イベント <br> カスタムフロントエンドイベント <br> カスタムドキュメントイベント <br> カスタム Crontab イベント <br> カスタム REST イベント <br> カスタム SOAP イベント <br> コアグローバルイベント <br> コア管理イベント <br> コアフロントエンドイベント <br> コアドキュメントイベント <br> コア Crontab イベント <br> コア REST イベント <br> コア SOAP イベント <br> すべてのグローバルイベント <br> すべての管理者イベント <br> すべてのフロントエンドイベント <br> すべてのドキュメントイベント <br> すべての REST イベント <br> すべてのSOAP イベント <br> すべての Crontab イベント |
| [!UICONTROL Cron] | ステータスコード別の Cron スケジュール <br> ジョブコード別の Cron スケジュール <br>Cron スケジュールキューのエラー <br>Cron スケジュールリスト <br> カスタムグローバル Cron ジョブ <br> カスタム設定可能な Cron ジョブ <br> コアグローバル Cron ジョブ <br> コア設定可能な Cron ジョブ <br> すべてのグローバル Cron ジョブ <br> すべての設定可能な Cron ジョブ |
| [!UICONTROL Design] | Adminhtml テーマリスト <br> フロントエンドテーマリスト |
| [!UICONTROL Stores] | Web サイトツリー <br>Web サイトのリスト <br> ストアのリスト <br> ストアの表示リスト |
| OMS コネクタ <br>_（OMS 統合で表示）_ | コネクタのバージョン <br> コネクタの監視 <br> メッセージの処理結果 |

{style="table-layout:auto"}
