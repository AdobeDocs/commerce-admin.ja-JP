---
title: データ管理ダッシュボード
description: のデータストリームに関するインサイトにアクセスする方法を説明します [!DNL Catalog Service], [!DNL Live Search]、および [!DNL Product Recommendation]s.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 4495a27b57c04c6f9c37b2c5237b5f2233cc8532
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# データ管理ダッシュボード

Data Management Dashboard には、Commerce データベースからCommerce SaaS サービスに転送される商品データの同期ステータスの概要が表示されます。 ユーザーは、製品の同期ステータスを便利に監視でき、統合ダッシュボードからデータの再同期を開始できます。 この機能は、ストアフロントの製品データの可用性に関する貴重なインサイトを提供し、買い物客に迅速に表示できるようにします。

## オーディエンス

Data Management Dashboard は、を使用するすべてのCommerce マーチャントが追加費用なしで利用できます [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview)、または [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) アクティブなライセンスを持つ。

データ管理ダッシュボードはにあります。 *システム* > データ転送 > *データ管理ダッシュボード*.

![データ管理ダッシュボード](assets/data-management-dashboard.png)

ダッシュボードには、次のフィールドが含まれています。

| フィールド | 説明 |
|--- |--- |
| 範囲 | 同期されたデータの特定の web サイト。 |
| [!DNL Product Recommendations] | 同期ステータス、同期された製品の数、以下のテーブルを表示 [displayable](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) 同期済み製品： [!DNL Product Recommendations]. |
| [!DNL Live Search] | 同期ステータス、同期された製品の数、以下のテーブルを表示 [displayable](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) 同期済み製品： [!DNL Live Search]. |
| [!DNL Catalog Service] | の同期ステータス、同期された製品の数、同期された製品のテーブルを表示します [!DNL Catalog Service]. |
| 設定 | ダイアログが開き、次の操作を実行できます [カタログデータを手動で再同期する](#resync-catalog-data). |
| 同期ステータス | 過去 3 時間以内にCommerce データベースからいずれかの SaaS サービスに転送された商品の数を表示します。 カタログを更新する頻度が低い場合、この値は頻繁にゼロになります。 同期中の場合は、 **[!UICONTROL Refresh]** 更新されたカウントを取得します。 |
| 製品数 | サービスで利用できるカタログ製品の合計数を反映します。 この [!DNL Product Recommendations] および [!DNL Live Search] ダッシュボードに表示される合計数 _displayable_ 製品。 [!DNL Catalog Service] は表示可能な項目で製品をフィルタリングしないので、両方とも持っている場合は [!DNL Catalog Service] および [!DNL Live Search] または [!DNL Product Recommendations] インストール済みの場合、2 つのダッシュボードの製品数に 2 つの異なる値を表示できます。 |
| 同期された製品 | コア Commerce インデックスに含まれる製品に関する詳細を提供します。 デフォルトでは、このテーブルは「最終更新日」で並べ替えられます。 特定の製品を検索するには、を使用します **[!UICONTROL Search by SKU]** フィールド。 表示する列を制御するには、をクリックします **[!UICONTROL Customize Table]** テーブルの右側にあります。 |

## データ管理ダッシュボードの使用

Commerce データベース内の商品を更新すると、商品データはシステム設定に従って SaaS サービスに転送されます。 同期プロセスが開始されると、 **製品数** saaS サービスに送信される製品の数を示します。

>[!IMPORTANT]
>
>同期の完了に要する時間は、カタログのサイズと更新されたデータの量に応じて異なります。

処理された製品の数が更新された製品の数と一致する場合は、同期が完了したことを示しています。

>[!NOTE]
>
>また、Adobeは、コマンドラインインターフェイスとシステムログも提供します。これらのログは、開発者とシステムインテグレーターがCommerce SaaS サービスの同期処理の管理とトラッキング、エラーのトラブルシューティングに使用できます。 詳しくは、を参照してください [SaaS データ エクスポート ガイド](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### 同期された製品のリスト

同期された製品の詳細を表示するには、テーブルの製品をクリックします。

![Syncd 製品の詳細](assets/sync-product-detail.png)

### カタログデータを再同期

Commerce SaaS サービスを常に最新の商品情報で更新するには、次の手順を実行します [スケジュールの実装](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) （カタログデータの同期用）。

可能な限り [手動で開始](#manually-resync-catalog) カタログデータがCommerce データベースから SaaS サービスに再同期される場合は、ハードウェアリソースの負荷が高まる可能性があるので、お勧めしません。 ただし、次のような場合は、カタログを手動で再同期する必要があります。

- 新製品の追加、製品の詳細の更新、カテゴリの変更など、製品カタログに大きな変更が加えられた場合

- ストアフロントでの製品データの表示に不一致やパフォーマンスの問題が発生した場合

- Commerce データベースと SaaS サービスの統合が更新または変更された場合

- 製品データ管理または同期プロセスに影響を与えるカスタマイズまたは設定をデプロイする場合

これらのガイドラインに従い、必要に応じてカタログデータを事前に再同期することで、Adobe Commerce エコシステム全体でデータの一貫性、正確性、信頼性を維持できます。

#### カタログを手動で再同期する

カタログ データを再同期する必要がある場合は、 **[!UICONTROL Settings]** ページの右側にダイアログが表示され、再同期を開始できます。 カタログデータを再同期すると、サービスはCommerce データベースから SaaS サービスにデータを再取得する必要があります。

![製品を手動で同期](assets/resync-data.png)
