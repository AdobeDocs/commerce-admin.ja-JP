---
title: データフィード同期ステータスの監視
description: データ書き出しの同期を監視し、 [!DNL Catalog Service]、 [!DNL Live Search]、および [!DNL Product Recommendations]のフィード処理に関する問題または遅延を特定します。
feature: Products, Customers, Data Import/Export
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: 3079ee3fe394a73d5ab4168e9e40815c340e386c
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---


# データフィード同期ステータスの監視

Adobe Commerce管理者は、Commerce AdminのData Feed Sync Status ページを使用して、Adobe Commerceから接続されたCommerce サービスに書き出されたデータの同期ステータスを監視できます。

![ フィード項目の状態レポートを含むデータフィード同期ステータスの詳細ページ ](assets/data-feed-sync-status.png)

このページでは、Commerceから[!DNL Product Recommendations]、[!DNL Live Search]、[!DNL Catalog Service]などの外部サービスに商品データやカテゴリデータを転送するデータ書き出しフィードの正常性とパフォーマンスに関するリアルタイムのインサイトを提供します。

同期ステータスページには、書き出しステータスのみが表示されます。 成功ステータスは、データが正常にエクスポートされ、最終的にConnected Commerce サービスで使用できることを示します。

フィードのステータスを監視することで、データの一貫性を確保し、書き出しプロセス中に発生した問題を迅速に解決できます。 管理者は次のことが可能になります。

* **すべてのデータフィードの同期ステータスを表示**
* **フィード処理におけるエラーの特定とトラブルシューティング**
* **個々のフィード項目の詳細なステータス情報**&#x200B;にアクセスする

ステータスは、次のフィードで追跡されます。

* 製品フィード
* 製品属性フィード
* カテゴリフィード
* 製品の上書きフィード
* 製品価格フィード
* 製品バリアントフィード

## データがCommerce サービスに正常に同期されたことを確認します

データが接続されているCommerce サービスと正常に同期されていることを確認するには、次の方法を使用します。

* Adobe Commerce オンクラウドまたはオンプレミス、またはAdobe Commerce as a Cloud Serviceのデプロイメントについては、[Data management ダッシュボード ](data-dashboard.md)を確認してください。
* [Adobe Commerce Optimizer Connector](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview)で構成されたAdobe Commerce オンクラウドまたはオンプレミスのデプロイメントの場合は、Commerce Optimizer Studioの[Data Sync ページ ](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync)を確認してください。

>[!TIP]
>
>データ同期プロセスについて詳しくは、*SaaS データ書き出しガイド*&#x200B;の「[SaaS データ書き出しとデータを同期する](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization)」を参照してください。

## 拡張機能のインストール

「データフィードのステータス」ページは、次のCommerce サービスのアクティブなライセンスを持つすべてのCommerce マーチャントが利用できます。

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview)
* アクティブなライセンスを持つ[[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)

>[!NOTE]
>
>データフィードのステータス拡張機能を[[!DNL Adobe Commerce as a Cloud Service]](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview) インスタンスにインストールする必要はありません。
>この拡張機能は、Commerce デプロイメントでProduct Recommendations v6+、Live Search v4.1+、またはCatalog Service v1.17以降のいずれかのサービスが有効になっている場合、デフォルトで使用できます。

**要件**

* PHP 8.1、8.2、8.3、または8.4
* Adobe Commerce 2.4.4以降
* [Adobe Commerce Data Export Extension](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/manage-extension)、バージョン 103.4.15以降
* [repo.magento.com](https://repo.magento.com)へのアクセス

  キーを生成し、必要な権限を取得するには、[認証キーを取得](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)するを参照してください。 クラウドインストールについては、「[Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys)」を参照してください。

* Adobe Commerce アプリケーションサーバーのコマンドラインにアクセスします。

### インストール手順

Composerを使用して`magento/module-data-exporter-status` モジュールを追加します。

```shell
composer require magento/module-data-exporter-status
```

インストール手順の詳細については、次のガイドを参照してください。

* [Adobe Commerce on Cloud Infrastructureへの拡張機能のインストール](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [拡張機能Adobe Commerce オンプレミスのインストール](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

## データフィードのステータスページへのアクセス

Commerce管理者から、**[!DNL System]**/データ転送/**[!DNL Data Feed Sync Status]**&#x200B;のCommerce管理者から「データフィードのステータス」ページにアクセスします。

![ データフィードの書き出しアクティビティを要約したデータフィードの同期ステータス ページ ](assets/data-feed-sync-status.png)

データフィードのステータス監視には、次の2つのインターフェイスがあります。

* 使用可能なフィードと現在の状態を一覧表示する[ データフィード同期ステータスの概要ページ ](#data-feed-sync-status-summary)
* 選択したフィードに関する詳細情報を表示する[ データフィード同期ステータス – 詳細ページ ](#data-feed-sync-status-details)。

## データフィード同期ステータスの概要

フィード同期ステータスの概要ページには、次の情報を含むデータフィード書き出しアクティビティに関する情報が表示されます。

| フィールド | 説明 |
|-------|-------------|
| **フィード名** | 特定のエンティティまたはその一部（製品や製品価格など）の同期を担当するフィードインデクサーの名前。 |
| **Source レコード** | Commerce データベースからエクスポートできるレコードの数。 各フィード項目は、ストアビューコードなどの特定の範囲に属しているため、この数はCommerce管理者に表示されるレコード数よりも多くなる可能性があります。 |
| **レコードを正常に送信しました** | さらに処理するためにCommerce SaaSに正常に送信されたレコードの数。 送信中にエラーが発生した場合、外部サービスに正常に送信されたレコードの数。 |
| **失敗したレコード** | 書き出しに失敗し、注意が必要なレコードの数。 |
| **アクション** | フィードの同期アクティビティを表示するには、**[!UICONTROL Details]**&#x200B;を選択します。 |

## データフィード同期ステータスの詳細

データフィードのステータスの概要ページで、フィード名をクリックするか、[!DNL View Details] アクションを使用して、フィード内の個々のレコードに関する詳細情報にアクセスします。

フィード項目の状態レポート ](assets/data-feed-sync-status-details.png)を含む![[!UICONTROL Data Feed Sync Status - Details] ページ

詳細ビューには、フィード項目ごとに次の情報が表示されます。

| フィールド | 説明 |
|-------|-------------|
| **フィード項目ID** | フィード レコードの内部識別子 |
| **エンティティ ID** | ソースエンティティ ID （製品ID、カテゴリ IDなど） |
| **ステータスの書き出し** | フィード項目の[同期ステータス ](#export-status-types)。 色分けされたインジケーターを使用した書き出しの現在のステータス |
| **最終同期日** | レコードが最後にCommerce サービスに送信された時刻 |
| **エンティティは削除されますか？** | エンティティまたはその部品（製品または製品価格など）がAdobe Commerceで削除されたかどうかを示します。 同期中にエラーが発生した場合にのみ、項目が表示されます。 |
| **リクエスト ID** | 同期リクエストの一意のID。 特定のエンティティの更新をトラブルシューティングする際に、このIDをサポートに提供します。 |
| **エラー** | フィード項目の同期に失敗した場合の詳細なエラー情報。 |

次のコントロールを使用してビューを管理できます。

* 選択したフィード項目の再同期をスケジュールする[!DNL Mass Action]
* [!DNL Filters]
* [!DNL Default View]を使用してフィルタされたビューを作成および保存し、ビューを切り替える
* [!DNL Columns]を使用すると、テーブルの列を表示および非表示にできます。

### フィードの正常性インジケーター

各フィードの詳細ページの上部にあるクリティカルヘルス指標は、各フィードのシステムステータスを提供します。

#### インデクサーステータス

* **有効**: データは同期されています。インデックスの再作成は必要ありません。
* **無効**：元のデータが変更されました。インデックスを更新してください。
* **処理中**: インデックス作成が進行中です。

>[!TIP]
>
>インデックス処理について詳しくは、[ インデックス管理](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/index-management)のトピックを参照してください。

#### 変更ログのバックログ

* **すべて同期**：保留中の変更はありません
* **バックログ内のアイテム**：処理待ちの保留中の変更の数

### 書き出しステータスタイプ

このシステムは、問題をすばやく特定するのに役立つステータス指標を提供します。

#### ステータスカテゴリ

| **ステータス** | **説明** | **操作が必要** |
|--------|-----------|-------------|
| **サービスに送信しました** | フィード項目が正常にCommerce サービスにエクスポートされました。 | なし |
| **失敗しました。再試行します** | 一時的なエラー。 システムは自動的に再試行されます。 | 解像度を監視 |
| **失敗しました。注意が必要です** | アプリケーションまたはデータエラーにより失敗しました。 | [!DNL Error]列の問題を調査して解決します |
| **送信待ち** | 書き出し待ちですが、まだ処理されていません。 | 通常の処理状態 |

## データフィードのステータスの監視

Commerce データベースの製品およびカテゴリ関連エンティティを更新すると、フィード設定に従ってデータがCommerce サービスに転送されます。 データフィード同期ステータスの概要ページから、このプロセスをリアルタイムで監視できます。

>[!IMPORTANT]
>
>データの同期にかかる時間は、カタログサイズ、更新されるデータ量、外部サービスのパフォーマンスなどによって異なります。

正常に送信されたレコードの数がソースレコードの数と一致すると、同期が完了し、すべてのデータが正常に送信されたことを示します。

>[!NOTE]
>
>Adobeには、開発者やシステムインテグレーターが同期操作の管理と追跡に使用できるコマンドラインインターフェイスツールとシステムログも用意されています。 詳しくは、[SaaS データ書き出しガイド ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)を参照してください。

### 失敗した書き出しの管理

失敗した書き出しの詳細を確認し、修正アクションを実行するには：

1. フィード同期ステータス ページで、失敗したレコードを含むフィードを見つけます。
1. **[!DNL Details]**&#x200B;をクリックします。

1. 特定のエラー理由に対するエラーメッセージを確認します。

1. 一括操作を使用して、失敗した項目の再同期操作をスケジュールします。

### 失敗したデータの再同期

[!DNL Data Feed Sync Status - Details] ページの[!DNL Actions] メニューを使用して、失敗したデータフィードまたは問題のあるデータフィードを手動で再同期できます。

システムは特定のタイプのエラーを自動的に再試行しますが、次のシナリオでは手動での介入が必要になる場合があります。

* 認証エラーまたは権限エラー（401、403 ステータスコード）に注意してください。
* ペイロードエラーの原因となったデータ形式の問題を解決した後。
* 外部サービス設定またはエンドポイントに対するアップデートを実行します。
* データ書き出しプロセスに影響を与えるカスタマイズをデプロイしています。

フィードのステータスを先見的に監視し、障害を迅速に対処することで、Commerceのエコシステム全体でデータの一貫性と信頼性を維持できます。

#### フィード項目を手動で再同期する

特定のフィード項目を再同期する必要がある場合：

1. **レコードを選択**: チェックボックスを使用して、注意が必要な失敗したレコードを選択します。
2. **アクションを選択**：一括操作ドロップダウンから&#x200B;**[!DNL Schedule Resync]**&#x200B;を選択します。
3. **確認**: **[!DNL Submit]**&#x200B;をクリックして、再同期操作を確認します。
4. **結果を監視**：成功メッセージを確認し、ステータスの変更を監視します。

## ベストプラクティス

### 定期的なモニタリング

1. **日次チェック**：高い失敗率を示すフィードについては、概要ページを日次で確認します
1. **毎週の詳細な調査**：重要なフィード（製品、価格）の詳細なステータスを調べます
1. **月次分析**：書き出しの成功率とパフォーマンスの傾向を追跡

### ワークフローのトラブルシューティング

1. **問題の特定**: エラーと高いエラー数を探します
1. **インデクサーの正常性を確認**: インデクサーが有効であり、バックログが管理可能であることを確認します
1. **エラーの詳細を確認**：失敗したレコードをクリックすると、特定のエラーメッセージが表示されます
1. **スケジュール再同期**：失敗した書き出しを再試行するには、一括操作を使用します
1. **解像度を監視**：再同期済みアイテムに成功ステータスが表示されていることを確認します

### 一般的な問題の修正

#### 高い失敗率

**現象**: 「失敗しました。注意が必要です」というステータスを示す多数のレコード

**潜在的な原因**:

* 外部サービス設定の変更
* データ形式の非互換性
* 認証または権限の問題

**解決手順**:

1. 外部サービスのステータスと設定の確認
1. エラーメッセージのパターンの確認
1. 認証資格情報の確認
1. 必要に応じて、外部サービスサポートに連絡してください

#### 書き出しのパフォーマンスが遅い

**現象**：高い変更ログ バックログ、遅いステータス更新

**潜在的な原因**:

* インデクサーのパフォーマンスの問題
* 大量のデータ
* 外部サービス率の制限

**解決手順**:

1. インデクサーステータスを確認し、無効な場合は再実行します
2. 外部サービスの応答時間の監視
3. オフピーク時の書き出しをスケジュールすることを検討する
4. システムのリソースとパフォーマンスの確認

#### 認証エラー

**症状**: 401または403 ステータスコード

**解決手順**:

1. API資格情報とトークンの検証
1. 外部サービスアカウントの権限を確認する
1. 期限切れの認証トークンを更新
1. アクセスの問題については、サービスプロバイダーにお問い合わせください

>[!MORELIKETHIS]
>
>* [ データ管理ダッシュボード ](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-sync/data-dashboard)
>* [SaaS データ書き出しガイド ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)
