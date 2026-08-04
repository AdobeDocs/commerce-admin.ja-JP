---
title: Commerceでのデータフィードの同期ステータスのモニタリング
description: 書き出しを追跡します。  [!DNL Catalog Service]、 [!DNL Live Search]、 [!DNL Product Recommendations]、および [!DNL Adobe Commerce Optimizer Connector]の同期の問題を診断します。
feature: Products, Customers, Data Import/Export
role: Admin
level: Beginner
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 424b379815ffbf818c2490d0195bf0bf7dd51ab7
workflow-type: tm+mt
source-wordcount: 1664
ht-degree: 0%

---


# データフィード同期ステータスの監視

[!UICONTROL Data Feed Sync Status] ページでは、Commerce管理者が管理領域の商品およびカテゴリデータフィードの書き出し正常性を監視できます。

## オーディエンスと可用性 {#audience}

データフィードの同期ステータス ページは、次のいずれかのサービスの有効なライセンスを持つCommerce マーチャントに追加料金なしで利用できます。

- [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
- [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)
- [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)
- [[!DNL Adobe Commerce Optimizer Connector]](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview)

データフィードの同期ステータス ページは、サポートされているCommerce サービス設定で自動的に使用できます。 Cloud Infrastructureおよびオンプレミスのデプロイメント上のAdobe Commerceで、対象となるサービスまたはコネクタを有効にした後にページが表示されない場合は、次の手動インストール手順に従います。 製品で管理されるSaaS エクスペリエンスには、Composerのインストール手順を使用しないでください。

## 同期ステータスページへのアクセス {#access-data-feed-sync-status-page}

管理領域から、**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**&#x200B;に移動します。

![ データフィードの書き出しアクティビティを要約したデータフィードの同期ステータス ページ ](assets/data-feed-sync-status.png){width="600" zoomable="yes"}

>[!NOTE]
>
> このページでは、書き出しステータスのみがレポートされます。 成功ステータスとは、データが正常に書き出されたことを意味します。接続されたサービスでデータが利用可能であることを確認しません。 詳しくは、[接続されたサービスのデータを確認](#confirm-data-in-connected-services)を参照してください。

## 使用可能な書き出しフィード

Data Sync Status ページから管理できる利用可能な書き出しフィードのリストは、どのCommerce サービスが接続されているかによって異なります。

- **設定されたCommerce サービスを使用する[!DNL Adobe Commerce on Cloud, On Premises, and Commerce as a Cloud Service]の場合：**、_SaaS データ書き出しガイド_&#x200B;の[ サポートされているフィード ](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/feed-table-reference#supported-feeds)を参照してください。

- **Adobe Commerce on Cloudまたはオンプレミスのデプロイメントが[!DNL Adobe Commerce Optimizer Connector]:**&#x200B;で構成されている場合は、_Adobe Commerce Optimizer コネクタ ガイド_&#x200B;の[ サポートされているフィード ](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/reference/connector-reference#supported-feeds)を参照してください。


## データフィード同期ステータスの概要 {#data-feed-sync-status-summary}

概要グリッドには、各フィードとその書き出し数が一覧表示されます。

| フィールド | 説明 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **フィード名** | エンティティまたはエンティティの一部のフィード インデクサー（製品、製品価格）。 |
| **Source レコード** | 同期が必要なCommerce レコードの数。 フィード項目の範囲が指定されているため、管理者グリッド数を超える可能性があります（例：ストアビューコード）。 |
| **レコードを正常に送信しました** | Commerceから設定されたサービスエンドポイントに正常に送信されたフィード項目の数。 これにより、ダウンストリームの取り込みやカタログの可用性が確認されるわけではありません。 同期エラーが発生した場合、この数はソースレコードの数よりも少ない可能性があります。 |
| **失敗したレコード** | 接続されたCommerce サービスに送信できなかったレコードの数。 |
| **アクション** | フィードの同期アクティビティを表示するには、**[!UICONTROL Details]**&#x200B;を選択します。 |

## データフィード同期ステータスの詳細 {#data-feed-sync-status-details}

概要ページで、フィード名を選択するか、**[!UICONTROL Details]**&#x200B;を選択して、各フィード項目の書き出しステータスを表示します。

フィード項目の状態レポートを含む![ データフィード同期ステータスの詳細ページ ](assets/data-feed-sync-status-details.png){width="600" zoomable="yes"}

| フィールド | 説明 |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **フィード項目ID** | システム目的で使用される自動生成されたID |
| **エンティティ ID** | ソースエンティティの一意の識別子（製品ID、カテゴリ IDなど） |
| **フィード識別子** | フィード項目の一意のID。 たとえば、商品フィードのSKUとストアビューのコードなどです。 値はフィードによって異なります。 |
| **ステータスの書き出し** | フィード項目の[同期ステータス ](#export-status-types)と、色分けされたインジケーター |
| **最終同期日** | Commerceからの最新の書き出しまたは送信の日時。 このタイムスタンプは、ダウンストリームの可用性を確認しません。 |
| **エンティティは削除されますか？** | Adobe Commerceでエンティティが削除されたかどうかを示します。 削除された項目は、同期に失敗した場合にのみ表示されます。 |
| **リクエスト ID** | 同期リクエストの一意のID。 エンティティの更新をトラブルシューティングする際に、サポートに提供します。 |
| **エラー** | 同期エラーの詳細なエラー情報 |

次のコントロールを使用してビューを管理できます。

- 選択したフィード項目の再同期をスケジュールする[!UICONTROL Mass Action]
- [!UICONTROL Filters]と[!UICONTROL Columns]
- [!UICONTROL Default View]を使用してフィルタされたビューを作成および保存し、ビューを切り替える

### フィードの正常性インジケーター {#feed-health-indicators}

| **インジケーター** | **説明** |
| ------------- | --------------- |
| インデクサーステータス | <ul><li>**準備完了**: インデクサーは最新です。 インデックス再作成は必要ありません。</li><li>**インデックスの再作成が必要**: Source データが変更されました。 最近の変更をキャプチャするために再インデックスを実行します。</li><li>**処理中**: インデックス作成が進行中です。</li></ul> |
| 変更ログのバックログ | <ul><li>**すべて同期**：保留中の変更はプロセスにありません。</li><li>**バックログ内のアイテム**：処理待ちの保留中の変更数。 1,000件以上のバックログは、パフォーマンスの問題を示している可能性があります。</li></ul> |
| インデクサーモード | <ul><li>**スケジュール モード** （推奨）: インデクサーがスケジュールに従って実行されるため、データ損失のリスクが軽減されます。</li><li>**保存時に更新** （リアルタイム）: ページに警告として表示されます。 リアルタイムモードは期待されておらず、負荷時にデータ損失のリスクが高まります。</li></ul> |

>[!TIP]
>
> インデックス処理について詳しくは、[ インデックス管理](index-management.md)のトピックを参照してください。

### 書き出しステータスタイプ {#export-status-types}

| **ステータス** | **説明** | **操作が必要** |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| **サービスに送信しました** | 下流処理のためにCommerceからフィード項目が正常に送信されました。 | なし |
| **失敗しました。再試行します** | 送信に失敗しましたが、システムは再送信を試みます。 | 解像度を監視 |
| **失敗しました。注意が必要です** | アプリケーションまたはデータエラーにより失敗しました。 | [!UICONTROL Error]列の問題を調査して解決します |
| **送信待ち** | 変更ログで検出されましたが、まだ処理されていません。 | 通常の処理状態 |

## データフィードのステータスの監視

Commerce データベース内の製品およびカテゴリ関連のエンティティを更新すると、フィード設定に従ってデータがCommerce サービスに転送されます。 書き出しアクティビティとその現在のステータスは、[!UICONTROL Data Feed Sync Status]概要ページから監視できます。

>[!IMPORTANT]
>
> データの同期にかかる時間は、カタログサイズ、更新されるデータ量、外部サービスのパフォーマンスなどによって異なります。

正常に送信されたカウントがフィードのソースカウントと一致し、送信待ちまたは失敗した項目が残っていない場合、Commerceはそのフィードの書き出しを完了しました。 適切なダッシュボードを使用して、[ ダウンストリームの可用性を確認](#confirm-data-in-connected-services)します。

>[!NOTE]
>
> Adobeには、開発者やシステムインテグレーターが同期操作の管理と追跡に使用できるコマンドラインインターフェイスツールとシステムログも用意されています。 詳しくは、[SaaS データ書き出しガイド ](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)を参照してください。

### 失敗した書き出しの管理 {#manage-failed-exports}

失敗した書き出しを確認し、再同期をスケジュールするには：

1. 概要ページで、失敗したレコードを含むフィードを見つけます。
1. **[!UICONTROL Details]**&#x200B;を選択します。
1. [!UICONTROL Error]列のエラーメッセージを確認します。
1. チェックボックスを使用して再同期するレコードを選択します。
1. [!UICONTROL Mass Action] メニューから、**[!UICONTROL Schedule Resync]**&#x200B;を選択し、**[!UICONTROL Submit]**&#x200B;を選択して、操作を確認します。
1. 詳細ページでステータスの変更を監視します。

システムは、特定のエラーを自動的に再試行します。

#### 手動で再同期する場合 {#resync-feed-items}

次の場合に手動で再同期します。

- 認証エラーまたは権限エラー（401または403 ステータスコード）が保持されます
- ペイロードエラーの原因となるデータ形式の問題を修正しました
- 外部サービス設定またはエンドポイントが変更されました
- データ書き出しに影響するカスタマイズがデプロイされました

### 接続されたサービスでのデータの確認 {#confirm-data-in-connected-services}

書き出し完了後にエンドツーエンドの同期を検証するには、次のいずれかの方法を使用します。 このページの書き出しステータスの制限については、上記の[ メモ ](#export-status-scope)を参照してください。

- **[!DNL Adobe Commerce as a Cloud Service]（Commerce サービス：**）該当する[ データ管理ダッシュボード ](data-dashboard.md)を確認して、ダウンストリームの可用性を確認します。
- **Adobe Commerce on Cloudまたはオンプレミス with Adobe Commerce Optimizer Connector**：まずCommerce管理者の書き出しステータスを確認してから、[!DNL Commerce Optimizer Studio]の[Data Sync ページ ](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync)を確認してください
- **[!DNL Adobe Commerce Optimizer]（スタンドアロン）:** データはCommerce バックエンドからエクスポートされません。 [!DNL Commerce Optimizer Studio]の[ データ同期ページ ](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync)を使用して、データの可用性を確認します。

>[!TIP]
>
> データ同期プロセスについて詳しくは、*SaaS データ書き出しガイド*&#x200B;の「[SaaS データ書き出しとデータを同期する](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization/data-sync-manage#view-and-manage-the-synchronization-process)」を参照してください。

## ベストプラクティス {#best-practices}

- 故障率の高いフィードについては、毎日サマリーページを確認してください。
- 商品や価格などの重要なフィードについて、毎週詳細を確認します。
- 毎月、書き出しの成功傾向を追跡して、繰り返し発生する問題を特定します。

## 一般的な問題のトラブルシューティング {#troubleshoot-common-issues}

| イシュー | 症状 | 今後の施策 |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 高い失敗率 | 多くのレコードに「*失敗、要注意*」ステータスが表示されます | <ul><li>外部サービスのステータスと設定の確認</li><li>[!UICONTROL Error]列のパターンのエラーメッセージを確認します</li><li>根本的な問題を解決した後、[失敗したエクスポートの管理と再同期](#manage-failed-exports)を参照してください</li><li>必要に応じて、外部サービスサポートに連絡してください</li></ul> |
| 書き出しのパフォーマンスが遅い | 大きな変更ログのバックログまたはステータスの更新が遅い | <ul><li>インデックスとバックログのステータスについては、[ フィード正常性インジケーター](#feed-health-indicators)を確認してください</li><li>**インデックス再作成が必要な**&#x200B;が表示されている場合は、インデックス再作成を実行します</li><li>外部サービスの応答時間の監視</li><li>可能な限りオフピーク時に書き出しをスケジュール</li><li>システムのリソースとパフォーマンスの確認</li></ul> |
| 認証エラー | [!UICONTROL Error]列の401または403 ステータスコード | <ul><li>API資格情報とトークンの検証</li><li>外部サービスアカウントの権限を確認する</li><li>期限切れのトークンを更新するか、サービスプロバイダーにお問い合わせください</li><li>資格情報を復元した後、[影響を受けるレコードを再同期](#manage-failed-exports)</li></ul> |
| データフィードの同期ステータスページがありません | 接続されたサービスを有効にした後、**[!UICONTROL Data Feed Sync Status]**&#x200B;は&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]**&#x200B;の下に表示されません | <ul><li>Commerce as a Cloud Serviceの場合、対象となるサービスが有効になっていることを確認します（[Audience and Availability](#audience)を参照）。</li><li>Commerce on Cloudまたはオンプレミスのみの場合、[拡張機能を手動でインストールする](#install-the-extension)</li></ul> |

Adobe Commerce on Cloud Infrastructureまたはオンプレミス：対象のサービスまたはAdobe Commerce Optimizer コネクタが有効になっていることを確認します。ページが表示されない場合は、手動インストールの手順に従います。
ACCSまたはAdobe Commerce Optimizer: モジュールを手動でインストールしないでください。製品で管理されている同期エクスペリエンスを使用するか、適切なサービスサポートチームにお問い合わせください。

## 拡張機能のインストール {#install-the-extension}

適格なサービスを有効にした後、管理領域に[!UICONTROL Data Feed Sync Status] ページが表示されない場合にのみ、Adobe Commerce オンクラウドまたはオンプレミスのデプロイメントに手動インストールが必要です。 [ オーディエンスと可用性](#audience)を参照してください。

### 前提条件

- Adobe Commerce 2.4.4以降。 要件の詳細については、[必要システム構成](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements)を参照してください。
- [Adobe Commerce Data Export Extension](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/manage-extension)、バージョン 103.4.15以降
- Adobe Commerce リポジトリから必要なパッケージをダウンロードする権限を持つ認証キー。 認証キーを作成し、必要なパッケージ アクセスを取得するには、[認証キーの取得](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)を参照してください。 Cloudのインストールについては、「[Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys)」を参照してください。
- Adobe Commerce アプリケーションサーバーのコマンドラインにアクセスします。

### インストール手順

Composerを使用して`magento/module-data-exporter-status` モジュールを追加します。

```shell
composer require magento/module-data-exporter-status
```

インストール手順の詳細については、次のガイドを参照してください。

- [Adobe Commerce on Cloud Infrastructureの拡張機能のインストール](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)
- [Adobe Commerce オンプレミスへの拡張機能のインストール](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

>[!MORELIKETHIS]
>
> - [ データ管理ダッシュボード ](data-dashboard.md)
> - [SaaS データ書き出しガイド ](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)
