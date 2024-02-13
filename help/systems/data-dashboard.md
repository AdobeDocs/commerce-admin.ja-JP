---
title: データ管理ダッシュボード
description: データ管理ダッシュボードの詳細
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# データ管理ダッシュボード

Data Management Dashboard は、Adobe Commerce SaaS 製品のデータストリームに関するインサイトを提供します。 のユーザー [!DNL Live Search], [!DNL Product Recommendations]、および [!DNL Catalog Service] は、単一のダッシュボードから製品同期ステータスを表示し、データを再同期できます。

データ管理ダッシュボードは、次の場所にあります。 *システム* /データ転送 > *データ管理ダッシュボード*.

![データ管理ダッシュボード](assets/data-management-dashboard.png)

## 設定

ページの右側にある「設定」ボタンをクリックすると、 [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) 設定ダイアログ。

通常、 [!DNL Catalog Sync] プロセスは、1 時間に 1 回、自動的に実行されます。

カタログデータを再同期すると、サービスはコマースデータベースからデータを再取得し、最新の変更がサービスおよびサイトに反映されるようにします。 複数の製品を変更し、通常の自動同期プロセスの前に変更を更新する必要がある場合は、このボタンを使用します。

## 同期ステータス

The _[!UICONTROL Sync]_ステータスパネルは、過去 3 時間以内に同期された製品の数を報告します。 カタログを頻繁に更新しない場合、この値は 0 になることがよくあります。 クリック&#x200B;**[!UICONTROL Refresh]**をクリックして、カウントを更新します。

## 製品数

製品数パネルには、サービスで使用可能なカタログ製品の合計数が反映されます。

The [!DNL Catalog Service] 「ダッシュボード」には、サービスで使用可能なカタログ内の製品の合計数が反映されます。 これは、通常、Commerce データベース内のすべての製品です。

製品Recommendationsおよびライブ検索ダッシュボードには、合計数が表示されます [_検索可能な_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) 製品。 一部の製品が検索可能に設定されていない場合は、 [!DNL Product Recommendations] および [!DNL Live Search]、および [!DNL Catalog Service].

## 同期された製品

「同期されたカタログ製品」テーブルには、インデックス内の製品の詳細が表示されます。 デフォルトでは、このテーブルは「最終更新日」で並べ替えられます。

特定の製品を検索するには、**[!UICONTROL Search by SKU]**フィールドに入力します。
表示する列を制御するには、 **[!UICONTROL Customize Table]** テーブルの右側に
