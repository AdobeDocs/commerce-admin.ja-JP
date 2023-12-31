---
title: インデックス管理
description: インデックスの再作成やベストプラクティスをトリガーするアクションなど、インデックス管理について説明します。
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---

# インデックス管理

Adobe CommerceとMagento Open Sourceは、1 つ以上の項目が変更された場合に、自動的にインデックスを再作成します。 インデックスの再作成をトリガーするアクションには、価格の変更、カタログまたは買い物かごの価格ルールの作成、新しいカテゴリの追加などがあります。 パフォーマンスを最適化するために、Commerce はインデクサーを使用してデータを特別なテーブルに蓄積します。 データが変更されると、インデックス付きのテーブルは更新（再インデックス）される必要があります。 Commerce はバックグラウンドプロセスとして再インデックスし、プロセス中、ストアにアクセス可能なままになります。

データのインデックス再作成は、処理を高速化し、顧客の待ち時間を短縮します。 例えば、品目の価格を$4.99 から$3.99 に変更した場合、Commerce はデータのインデックスを再作成して、店舗の価格の変更を表示します。 インデックス作成を行わない場合、コマースはすべての製品の価格をその場で計算する必要があります。買い物かごの価格ルール、バンドル価格、割引、価格帯などを処理します。 製品の価格の読み込みに、お客様が待つよりも時間がかかる場合があります。

インデクサーは、保存時またはスケジュール時に更新するように設定できます。 保存時にのみサポートされる顧客グリッドを除き、すべてのインデックスでどちらかのオプションを使用できます。 保存時にインデックス作成を行うと、Commerce は保存操作時にインデックス再作成を開始します。 インデックスの管理ページで、更新が完了し、1～2 分以内に再インデックスメッセージが表示された状態でキャッシュがフラッシュされます。 スケジュールに従ってインデックスを再作成する場合、インデックス再作成は、cron ジョブとしてスケジュールに従って実行されます。 次の場合にシステムメッセージが表示されます。 [cron ジョブ](cron.md) は、無効になったインデクサーを更新するために使用できません。 ストアは、インデックス再作成プロセス中もアクセス可能なままです。

>[!NOTE]
> ライブ検索、カタログサービスまたは製品Recommendationsを使用するAdobe Commerceのマーチャントは、 [SaaS ベースの価格インデクサー](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

再インデックスが必要な場合は、ページの上部に通知が表示されます。 インデックスとメッセージは、再インデックスモードと、実行する潜在的なアクションに基づいてクリアされます。 インデックス作成について詳しくは、 [アプリケーションがインデックス作成を実装する方法](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) （内） _PHP 開発者ガイド_.

![インデックス管理 — アクション](./assets/index-management.png){width="700" zoomable="yes"}

- インデックス管理では、フラットな製品カタログの表示方法が少し異なります。
- 複数の管理者ユーザーが自動インデックス再作成をトリガーするオブジェクトを更新する際の問題を回避するには、すべてのインデクサーをスケジュールに従って実行するように設定することをお勧めします。 [cron ジョブ](cron.md). そうしないと、オブジェクトが保存されるたびに、相互依存関係を持つオブジェクトがデッドロックを引き起こす可能性があります。 デッドロックの症状としては、CPU 使用率が高く、MySQL エラーが発生する場合があります。 ベストプラクティスとして、スケジュールされたインデックス作成を使用することをお勧めします。
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) デフォルトでは、インデックス再作成などの管理アクションはシステムによって記録され、 [アクションログレポート](action-log-report.md). アクションのログは、 [管理アクションのログ](action-log.md) ストアの詳細な管理設定を参照してください。

## インデックス再作成のベストプラクティス

Commerce では、インデックス再作成とキャッシュの目的が異なります。 インデックスは、データベース情報を追跡し、検索パフォーマンスの向上、ストアフロントのデータ取得の高速化などを実現します。 [キャッシュ](cache-management.md) 読み込んだデータ、画像、形式などを保存して、パフォーマンスの読み込みとストアフロントへのアクセスを向上させます。

- 通常、Commerce でデータを更新する際にインデックスを再作成します。
- 大きなストアまたは複数のストアがある場合、インデックスの再作成が可能なため、カテゴリや製品などのインデクサーを、スケジュールされた cron ジョブに設定する必要が生じる場合があります。 ピーク時以外の時間帯にスケジュールに基づいて再インデックスを設定することもできます。
- インデックスを再作成する場合、フラッシュキャッシュも実行する必要はありません。
- 新規コマースインストールの場合は、キャッシュをフラッシュしてインデックスを再作成する必要があります。
- キャッシュをフラッシュし、インデックスを再作成しても、コンピューターの Web ブラウザーのキャッシュがフラッシュされません。 ストアフロントの更新を完了したら、ブラウザーのキャッシュをクリアします。

## インデックスモードの変更

>[!IMPORTANT]
>
>を使用する店舗の場合 [Adobe Commerce用 B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) また、Elasticsearchをフルテキスト (`catalogsearch_fulltext`) インデクサー：一括権限の変更後、または「権限」インデクサーが「スケジュール済み」モードの場合は、フルテキストインデックスを再実行する必要があります。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. 変更する各インデクサーのチェックボックスをオンにします。

1. 設定 **[!UICONTROL Actions]** を次のいずれかに変更します。

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >顧客グリッドは、 `Update on Save`. このインデックスは、 **_not_** サポート `Update by Schedule`.

1. クリック **[!UICONTROL Submit]** をクリックして、選択した各インデクサに変更を適用します。

   **インデックス管理列**

   | 列 | 説明 |
   | ------ | ----------- |
   | [!UICONTROL Indexer] | インデクサーの名前。 |
   | [!UICONTROL Description] | インデクサーの説明。 |
   | [!UICONTROL Mode] | 各インデクサーの現在の更新モードを示します。 オプション： <br/>**[!UICONTROL Update on Save]**— インデックスは、エンティティの変更が保存されるたびに更新されるように設定されます。 これらのエンティティには、製品、カテゴリ、顧客が含まれます。 保存アクションが完了すると、一連の手順で変更の取得とインデックスの更新が開始されます。 インデックス管理ページで、1 ～ 2 分以内に再インデックスメッセージを更新およびフラッシュします。<br/>**[!UICONTROL Update on Schedule]**  — インデックスは、 [cron ジョブ](cron.md). cron ジョブには、インデックス再作成のスケジュール間隔が含まれ、実行時にインデックスの更新を書き込みます。 |
   | [!UICONTROL Schedule Status] | スケジュールステータスの更新を表示します。 |
   | [!UICONTROL Status] | 次のいずれかを表示します。 <br/>**[!UICONTROL Ready]**— インデックスは最新です。<br/>**[!UICONTROL Scheduled]**  — インデックスの再作成は、予定されています。 <br/>**[!UICONTROL Running]**— インデックス再作成が実行中です。<br/>**[!UICONTROL Reindex Required]**  — インデックスの再作成が必要な変更が行われましたが、インデクサーを自動的に更新することはできません。 チェックして、 [cron](cron.md) が使用可能になり、正しく設定されている。 |
   | [!UICONTROL Updated] | インデックスが最後に更新された日時を示します。 |

   {style="table-layout:auto"}

## コマンドラインを使用して再インデックスを行う

Commerce では、コマンドラインを使用して追加の再インデックスオプションを提供します。 詳細とコマンドオプションについては、 [再インデックス](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target=&quot;blank&quot;} を _設定ガイド_.

## インデックストリガーイベント

## インデックス再作成トリガー

| インデックスタイプ | イベントのインデックス再作成 |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | 顧客グループの追加<br/>構成設定の変更 |
| [!UICONTROL Flat catalog product data] | ストアを追加<br/>ストアグループを追加<br/>属性を追加、編集または削除（検索およびフィルタリング用） |
| [!UICONTROL Flat catalog category data] | ストアを追加<br/>ストアグループを追加<br/>属性を追加、編集または削除（検索およびフィルタリング用） |
| [!UICONTROL Catalog category/product index] | 製品（単一、一括、および読み込み）の追加、編集、削除<br/>製品とカテゴリの関係を変更<br/>カテゴリの追加、編集、削除<br/>ストアの追加または削除<br/>ストアグループの削除<br/>Web サイトの削除 |
| [!UICONTROL Catalog search index] | 製品（単一、一括、および読み込み）の追加、編集、削除<br/>ストアの追加または削除<br/>ストアグループの削除<br/>Web サイトの削除 |
| [!UICONTROL Stock status index] | 在庫構成設定を変更します。 |
| [!UICONTROL Category permissions index] | ストアを追加<br/>ストアグループを追加<br/>属性を追加、削除、または更新（検索とフィルタリングのため） |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>フラットカタログの使用は、ベストプラクティスとして推奨されなくなりました。 この機能を継続して使用すると、パフォーマンスが低下し、その他のインデックス作成の問題が発生することがわかっています。 詳しくは、 [フラットカタログ製品を使用](../catalog/catalog-flat.md) を参照してください。

## インデックスのアクションとコントロール

| アクション | 結果 | コントロール |
| ------ | ------ | -------- |
| ストア、新しい顧客グループ、または `Actions that Cause a Full Reindex` | 完全な再インデックス | 完全なインデックス再作成は、Adobe CommerceまたはMagento Open Sourcecron ジョブで指定されたスケジュールに従って実行されます。 |
| 項目の一括読み込み（コマースの読み込み/書き出し、Direct SQL クエリ、およびデータを直接追加、変更、または削除するその他の方法） | 部分的な再インデックス（変更された項目のみインデックスが再作成されます） | コマース cron ジョブで決定された頻度です。 |
| 範囲の変更（グローバルから Web サイトへの変更など） | 部分的な再インデックス（変更された項目のみインデックスが再作成されます） | コマース cron ジョブで決定された頻度です。 |

{style="table-layout:auto"}

## 完全なインデックス再作成をトリガーするイベント

| インデクサー | イベント |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Web ストアを作成する<br/>Web ストアビューの作成<br/>次のいずれかの属性を作成または削除します。<br/> — 詳細検索で検索可能または表示可能<br/> — フィルタリング可能<br/> — 検索でフィルタリング可能<br/> — 並べ替えに使用<br/>既存の属性を前の属性のいずれかに変更します。<br/>フラットカテゴリストアフロントオプションを有効にする |
| [!UICONTROL Catalog Product Flat Indexer] | Web ストアを作成する<br>Web ストアビューの作成<br/>次のいずれかの属性を作成または削除します。<br/> — 詳細検索で検索可能または表示可能<br> — フィルタリング可能<br> — 検索でフィルタリング可能<br/> — 並べ替えに使用 <br/>既存の属性を前の属性のいずれかに変更します。<br/>フラットカテゴリストアフロントオプションを有効にする |
| [!UICONTROL Stock status indexer] | 次の場合 _カタログ在庫オプション_ システム構成の変更：<br/>`Stock Options`  — 在庫切れの製品の表示<br/>`Product Stock Options`  — 在庫の管理 |
| [!UICONTROL Price Indexer] | 顧客グループの追加。<br/>システム構成で次のカタログ在庫オプションのいずれかが変更された場合：<br/>`Stock Options`  — 在庫切れの製品の表示<br/>`Product Stock Options`  — 在庫の管理<br/>`Price`  — カタログ価格の範囲 |
| [!UICONTROL Category or Product Indexer] | ストアビューの作成または削除<br/>ストアを削除<br/>Web サイトの削除 |

{style="table-layout:auto"}
