---
title: データ管理ダッシュボード
description: カタログサービス、ライブ検索、製品Recommendationsのデータストリームに関するインサイトにアクセスする方法を説明します。
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# データ管理ダッシュボード

Data Management Dashboard は、Adobe Commerce SaaS 製品のデータストリームに関するインサイトを提供します。 のユーザー [!DNL Live Search], [!DNL Product Recommendations]、および [!DNL Catalog Service] は、単一のダッシュボードから製品同期ステータスを表示し、データを再同期できます。

データ管理ダッシュボードは、次の場所にあります。 *システム* /データ転送 > *データ管理ダッシュボード*.

![データ管理ダッシュボード](assets/data-management-dashboard.png)

## 設定

The **[!UICONTROL Settings]** ページの右側にあるボタンをクリックすると、カタログデータを再同期できるダイアログが開きます。

カタログデータを再同期すると、サービスは Commerce データベースからデータを再取得します。 このアクションは、通常、カタログ同期が 2 ～ 3 時間実行されていない場合に、初めてオンボーディングする際に使用されます。

## 同期ステータス

The _[!UICONTROL Sync]_ステータスパネルは、過去 3 時間以内に同期された製品の数を報告します。 カタログを頻繁に更新しない場合、この値は 0 になることがよくあります。 クリック&#x200B;**[!UICONTROL Refresh]**をクリックして、カウントを更新します。

## 製品数

製品数パネルには、サービスで使用可能なカタログ製品の合計数が反映されます。

The [!DNL Product Recommendations] および [!DNL Live Search] ダッシュボードには、 _表示可能な_ 製品。 [!DNL Catalog Service] 表示可能で商品をフィルタリングしないので、両方の [!DNL Catalog Service] および [!DNL Live Search] または [!DNL Product Recommendations] がインストールされている場合、2 つのダッシュボードで製品数の 2 つの異なる値が表示される可能性があります。

## 同期された製品

「同期された製品」テーブルには、インデックス内の製品の詳細が表示されます。 デフォルトでは、このテーブルは「最終更新日」で並べ替えられます。

特定の製品を検索するには、 **[!UICONTROL Search by SKU]** フィールドに入力します。
表示する列を制御するには、 **[!UICONTROL Customize Table]** テーブルの右側に
