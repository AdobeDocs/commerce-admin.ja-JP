---
title: データ管理ダッシュボード
description: ' [!DNL Catalog Service]、 [!DNL Live Search]、および [!DNL Product Recommendation]のデータストリームに関するインサイトにアクセスする方法について説明します。'
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
TQID: https://experienceleague.adobe.com/5WxRmKbBDfWM4JHypuXKCmrUTn5VjQeAUdLRJUWQXtc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 802
ht-degree: 0%

---

# データ管理ダッシュボード

Data Management ダッシュボードでは、Commerce データベースからCommerce SaaS サービスに転送される製品データの同期ステータスの概要が表示されます。 製品の同期ステータスを監視し、統合ダッシュボードからデータの再同期を開始できます。 この機能は、ストアフロントの商品データの可用性に関する貴重なインサイトを提供し、買い物客に迅速に表示できるようにします。

>[!NOTE]
>
>カタログデータをAdobe Commerce Optimizerに書き出すために[Adobe Commerce Optimizer Connector](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview)をインストールした場合は、Data Management ダッシュボードではなく、Commerce Optimizer Studioの[Data Sync ページ ](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync)を使用して、正常なデータ同期を確認します。

## オーディエンス

Data Management Dashboardは、アクティブなライセンスを持つ[[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)、[[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview)、[[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)を使用しているすべてのCommerce マーチャントに追加料金なしで利用できます。

データ管理ダッシュボードは、*システム*/データ転送/*データ管理ダッシュボード*&#x200B;にあります。

![ データ管理ダッシュボード ](assets/data-management-dashboard.png)

ダッシュボードには、次のフィールドが含まれます。

| フィールド | 説明 |
|--- |--- |
| 範囲 | 同期データ用の特定のweb サイト。 |
| [!DNL Product Recommendations] | 同期ステータス、同期済み製品数、および[!DNL Product Recommendations]の[displayable](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options)同期製品のテーブルを表示します。 |
| [!DNL Live Search] | 同期ステータス、同期済み製品数、および[!DNL Live Search]の[displayable](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options)同期製品のテーブルを表示します。 |
| [!DNL Catalog Service] | 同期ステータス、同期済み製品数、および[!DNL Catalog Service]の同期済み製品のテーブルを表示します。 |
| 設定 | カタログ データを[手動で再同期できるダイアログを開きます](#resync-catalog-data)。 |
| 同期ステータス | 過去3時間以内にCommerce データベースから任意のSaaS サービスに転送された製品の数を表示します。 カタログの更新頻度が低い場合、この値は頻繁にゼロになります。 同期が進行中の場合は、**[!UICONTROL Refresh]**&#x200B;をクリックして、更新されたカウントを取得します。 |
| 製品数 | サービスで使用可能なカタログ製品の合計数を反映します。 [!DNL Product Recommendations]および[!DNL Live Search] ダッシュボードには、_表示可能_&#x200B;商品の合計数が表示されます。 [!DNL Catalog Service]はdisplayableで製品をフィルタリングしないので、[!DNL Catalog Service]と[!DNL Live Search]または[!DNL Product Recommendations]の両方がインストールされている場合、2つのダッシュボードで製品数に2つの異なる値を表示できます。 |
| 同期済み製品 | コア Commerce インデックスの商品に関する詳細を提供します。 デフォルトでは、このテーブルは「最終更新日」でソートされます。 特定の製品を検索するには、**[!UICONTROL Search by SKU]** フィールドを使用します。 表示する列を制御するには、テーブルの右側にある&#x200B;**[!UICONTROL Customize Table]**&#x200B;をクリックします。 |

## データ管理ダッシュボードの使用

Commerce データベースの製品を更新すると、製品データはシステム設定に従ってSaaS サービスに転送されます。 同期プロセスが開始されると、**製品数**&#x200B;は、SaaS サービスに送信された製品数を示します。

>[!IMPORTANT]
>
>同期を完了するのにかかる時間は、カタログサイズと更新されるデータ量によって異なります。

処理された製品数が更新された製品数と一致すると、同期が完了したことを示します。

>[!NOTE]
>
>Adobeには、開発者やシステムインテグレーターがCommerce SaaS サービスの同期操作の管理と追跡およびエラーのトラブルシューティングに使用できるコマンドラインインターフェイスとシステムログも用意されています。 詳しくは、[SaaS データ書き出しガイド ](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)を参照してください。

### 同期済み製品のリスト

同期済み製品の詳細を表示するには、テーブルから製品をクリックします。

![製品の詳細を同期](assets/sync-product-detail.png)

### カタログデータの再同期

Commerce SaaS サービスを常に最新の製品情報に保つために、[ カタログデータの同期スケジュール ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex)を実装する必要があります。

Commerce データベースからSaaS サービスへのカタログデータの再同期を[手動で](#manually-resync-catalog)開始できますが、ハードウェアリソースの負荷が増加する可能性があるため、お勧めしません。 ただし、次のシナリオでは、カタログを手動で再同期する必要がある場合があります。

- 新製品の追加、製品詳細の更新、カテゴリの変更など、製品カタログに大きな変更が加えられたときはいつでも

- ストアフロントへの商品データの表示において、矛盾やパフォーマンスの問題が発生した場合

- CommerceデータベースとSaaS サービス間の統合の更新や変更をフォローする

- 製品データの管理または同期プロセスに影響するカスタマイズまたは設定をデプロイする場合

これらのガイドラインに準拠し、必要に応じてカタログデータを積極的に再同期することで、Adobe Commerceのエコシステム全体でデータの一貫性、正確性、信頼性を維持できます。

#### カタログを手動で再同期

カタログデータを再同期する必要がある場合は、ページの右側にある&#x200B;**[!UICONTROL Settings]**&#x200B;をクリックして、再同期を開始できるダイアログを表示します。 カタログデータを再同期すると、サービスはCommerce データベースからSaaS サービスにデータを強制的にリフェッチします。

![製品を手動で同期](assets/resync-data.png)
