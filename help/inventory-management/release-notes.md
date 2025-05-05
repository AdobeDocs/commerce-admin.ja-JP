---
title: '[!DNL Inventory Management] リリースノート'
description: すべてのリリースについて詳しくは、リリースノ  [!DNL Inventory Management]  トを参照してください。
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management] リリースノート

このリリースノートは [!DNL Inventory Management] のリリースを説明しており、以下が含まれています。

![ 新機能 ](../assets/new.svg) 新機能
![ 修正された問題 ](../assets/fix.svg) 修正および改善
![ 既知の問題 ](../assets/bug.svg)

[!DNL Inventory Management] は、コントリビューター向けのMagento Open Sourceコミュニティエンジニアリング特別プロジェクトです。 参加して投稿するには、[GitHub プロジェクト ](https://github.com/magento/inventory) リポジトリ、および [wiki](https://github.com/magento/inventory/wiki) を参照して開始してください。 プロジェクトについて話し合うには、[Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) チャンネル（[ セルフ サインアップ ](https://opensource.magento.com/slack)）に参加します。

サポートされるリリースおよび互換性のあるリリースの [ リリーススケジュール ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=ja){target="_blank"}。

## v1.2.7

[!DNL Inventory Management] 1.2.7 リリースノートは、[core 2.4.7 リリースノート ](https://experienceleague.adobe.com/ja/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1) に含まれています。

## v1.2.6

[!DNL Inventory Management] 1.2.6 （モジュールバージョン：`magento/inventory-metapackage = 1.2.6`）はバージョン 2.4.6 でサポートされ、Adobe Commerceのバージョン 2.4.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースと互換性があります。

![ 修正された問題 ](../assets/fix.svg) ストアフロントには、売り切れた子製品が在庫に戻された際に、複合製品（設定可能、バンドル、グループ化）が在庫中として表示されるようになりました。 以前は、これらの条件で複合製品が在庫切れであることがストアフロントで示されていました。<!-- ACP2E-1106-->

![ 修正された問題 ](../assets/fix.svg) 数量を 0 に設定してオプションを作成し、**[!UICONTROL Display out-of-stock products]** が有効になっている場合、設定可能な製品オプションがストアフロントに在庫切れとして表示されるようになりました。<!-- ACP2E-1148-->

![ 修正された問題 ](../assets/fix.svg) 在庫数が変更され、製品がまだ在庫にある場合、カテゴリページのキャッシュが無効にならなくなりました。 ストアフロントのカテゴリページで商品の数量が変わった場合（それ以外の数量が変わった場合）に、Adobe Commerceがページを再生成する代わりに、キャッシュからページを読み込むようになりました。<!-- ACP2E-118-->

![ 修正された問題 ](../assets/fix.svg) **[!UICONTROL Display Out-Of-Stock Products]** 設定を有効にして、シングルソースモードで在庫を使用すると、カテゴリリストの製品数が正しく表示されるようになりました。 Adobe Commerceは、カウント時に商品が販売可能かどうかを確認するようになりました。<!-- ACP2E-1033-->

![ 修正された問題 ](../assets/fix.svg) 在庫が有効な場合、店舗内配信の買い物かご価格ルールが期待どおりに機能するようになりました。 以前は、これらの条件下で買い物かご価格ルールによる割引は適用されませんでした。<!-- ACP2E-1015-->

![ 修正された問題 ](../assets/fix.svg) スケジュール済みモードで製品インベントリを更新しても、すべてのキャッシュがクリアされなくなりました。 以前は、インベントリインデクサーによってすべての設定キャッシュがクリアされていました。<!-- ACP2E-1003-->

![ 修正された問題 ](../assets/fix.svg) 詳細在庫の製品の **[!UICONTROL Allow Multiple Boxes for Shipping]** 属性の値が、期待どおりに保存されるようになりました。<!-- ACP2E-992-->

![ 問題を修正 ](../assets/fix.svg)Adobe Commerceでは、店舗での集荷で注文された注文に対する部分的な払い戻しクレジットメモの後に、正確な予約報酬を発行するようになりました。 以前は、管理者ユーザーが「**[!UICONTROL Return to Stock]**」チェックボックスを選択せずにクレジットメモを作成すると、誤った予約が `inventory_reservation` テーブルに保存されていました。<!-- ACP2E-979-->

![ 修正された問題 ](../assets/fix.svg) マルチソース在庫の実装のデプロイメントで、バリエーションの 1 つが手動で在庫に戻された場合、Adobe Commerceで、設定可能な商品がストアフロントに在庫切れと表示されなくなりました。<!-- ACP2E-952-->

![ 修正された問題 ](../assets/fix.svg) 複数の在庫ソースが設定されたデプロイメントでページがリロードされた後、製品グリッド（**[!UICONTROL Catalog]**/**[!UICONTROL Products]**）の列の位置が以前の位置に戻らなくなりました。<!-- ACP2E-925-->

![ 修正済みの問題 ](../assets/fix.svg) 「**[!UICONTROL Back to stock]**」チェックボックスが選択されていない場合、仮想製品のクレジットメモを発行した後の在庫数が正しくなりました。<!-- ACP2E-908-->

![ 修正された問題 ](../assets/fix.svg) デフォルト以外の在庫に割り当てられている、製品の自動並べ替えと範囲を使用してカテゴリを保存できるようになりました。 以前は、Adobe Commerceはカテゴリを保存せず、次のエラーを表示していました：`Something went wrong while saving the category`。<!-- ACP2E-859-->

![ 修正された問題 ](../assets/fix.svg) すべての在庫切れの設定可能なバリエーションで製品を作成した場合、設定可能な製品の在庫ステータスが期待どおりに更新されるようになりました。<!-- ACP2E-813-->

![ 修正された問題 ](../assets/fix.svg) 予約不整合アナライザーツールは、設定可能な製品、バンドルおよびグループ化された製品を含む、部分的に出荷された注文で正しく機能するようになりました。 これで、複合製品タイプが分析されました。 以前は、キャンセルと払い戻しは、親製品に対してのみ保存されており、設定可能なバンドル製品および一括で出荷されるバンドル製品のサブ製品オーダー品目には保存されていませんでした。<!-- ACP2E-924-->

![ 修正された問題 ](../assets/fix.svg) 管理者ユーザーが在庫または商品に 200 以上の在庫ソースを割り当てようとすると、Adobe Commerceにエラーが表示されなくなりました。<!-- ACP2E-1180-->

![ 修正された問題 ](../assets/fix.svg)Adobe Commerceでは、商品が削除された注文に対するクレジットメモの作成をサポートするようになりました。 以前は、請求書を作成した後に製品を注文から削除すると、マーチャントはクレジットメモを作成できませんでした。 アプリケーションに次のエラーが表示されました：`Following products with requested skus were not found: s00001`。 ト <!-- ACP2E-1138--> ート・ファルソン

![ 修正された問題 ](../assets/fix.svg) 単一ストア ID と複数ストア ID の両方に基づいてストアがフィルタリングされるようになりました。 `event` 製品属性コードが、予約属性コードのリストに追加されました。 以前は、在庫モジュールがインストールされると、低在庫レポートで例外がスローされていました。<!-- ACP2E-1017-->

![ 問題を修正 ](../assets/fix.svg) 階層型ナビゲーションフィルターが期待どおりに機能し、在庫切れの製品がストアフロントのカテゴリ製品リストに追加されるようになりました。 新しい `is_out_of_stock` の並べ替え属性では、ストアフロントの製品コレクションにElasticsearchの動的フィールドマッパーを使用します。<!-- ACP2E-748-->

![ 修正された問題 ](../assets/fix.svg)REST `POST /rest/V1/inventory/source-items` 呼び出しによって子製品の在庫ステータスが変更されると、複合製品（バンドル、グループ化および設定可能）の在庫ステータスが期待どおりに更新されます。<!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 （モジュールバージョン：`magento/inventory-metapackage = 1.2.5`）は、バージョン 2.4.5 でサポートされ、Adobe Commerceのバージョン 2.4.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースと互換性があります。

![ 修正された問題 ](../assets/fix.svg) 販売者が管理者から出荷を作成すると、バンドルおよびグループ化された製品のデフォルトの在庫在庫ステータスが期待どおりに更新されるようになりました。 以前は、これらの製品のステータスは出荷作成後も変更されていません。<!--- ACP2E-418-->

![ 修正された問題 ](../assets/fix.svg) 次のいずれかの条件を満たした場合、設定可能な製品が在庫に戻されるようになりました。1. 親商品に、在庫のある保存済みの子が少なくとも 1 つあります。 2.設定可能な製品自体が更新され、**在庫** として設定され、少なくとも 1 人の子が在庫にありました。<!--- ACP2E-443-->

![ 修正された問題 ](../assets/fix.svg)REST API を通じて実装された在庫の変更が、製品の詳細ページに期待どおりに反映されるようになりました。 最後の在庫ステータスと現在の在庫ステータスを比較した後、カタログ製品のキャッシュが消去されるようになりました。 以前は、コールバック関数を省略すると、在庫ステータスの変更が誤ってトリガーされ、必要なキャッシュクリーニングが評価されていませんでした。 その結果、ストアフロントには在庫の変更が反映されていませんでした。<!--- ACP2E-161-->

![ 修正された問題 ](../assets/fix.svg) デフォルトの在庫に割り当てられ、以前は在庫切れだった製品が、`/V1/inventory/source-items` を使用してソース項目を更新した後、ストアフロントに表示されるようになりました。 以前は、この REST API エンドポイントは、間違った `stock_status` を設定していました。<!--- ACP2E-562-->

![ 修正された問題 ](../assets/fix.svg) 一括アクション（**[!UICONTROL Catalog]**/**[!UICONTROL Products]**/**[!UICONTROL Select Products]**/**[!UICONTROL Actions - Unassign Inventory Source]**）を通じて在庫ソースの割り当てを解除しても、先頭のゼロを除いて重複する SKU （`01234` や `1234` など）がソースに含まれる場合に、正常に機能するようになりました。 以前は、アプリケーションは在庫ソースの割り当てを解除せず、エラーをスローしていました。<!--- ACP2E-2641-->

![ 修正された問題 ](../assets/fix.svg) 無制限のバックオーダーが有効になり、バックオーダーされた数量に関係なく、製品がカスタム在庫に割り当てられると、製品の在庫ステータスがストアフロントで常に **在庫中** になりました。 以前は、バックオーダーが有効になっている場合でも、商品の在庫が切れていました。<!--- ACP2E-664-->

![ 修正された問題 ](../assets/fix.svg) ソース項目が `POST /V1/inventory/source-items` で更新された後、設定可能な製品の親および子製品の在庫が正しく更新されるようになりました。 API を使用して子製品が更新された後、デフォルトの在庫チェック用の新しい在庫プラグインが更新され、設定可能な製品数量とステータスが更新されます。<!--- ACP2E-442-->

![ 修正された問題 ](../assets/fix.svg) 在庫切れのグループ化製品がストアフロントのカテゴリページに表示されなくなりました。<!--- ACP2E-2082-->

![ 問題を修正しました ](../assets/fix.svg)`CatalogInventory` `composer.json` のパッケージ名を修正しました。<!--- ACP2E-2914-->

![ 修正された問題 ](../assets/fix.svg) マルチソース/在庫デプロイメントで数量が 0 の製品を使用して注文を行った後、バックオーダーステータスが管理者に正しく表示されるようになりました。 [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![ 修正された問題 ](../assets/fix.svg) 在庫セクションからバンドル製品を更新すると、在庫切れのバンドル製品がストアフロントカテゴリページに表示されなくなりました。<!--- ACP2E-2012-->

![ 修正された問題 ](../assets/fix.svg)PHP 7.4 との互換性の問題が解決されました。<!--- AC-3192-->

![ 修正された問題 ](../assets/fix.svg) 多くのオプション（複数の 100）を含むバンドル製品を含む保存操作のパフォーマンスが向上しました。 以前は、これらの大きなバンドル製品の保存に数分かかり、在庫サービスが有効になっているデプロイメントでタイムアウトが発生することがありました。 [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![ 修正された問題 ](../assets/fix.svg) 先頭の `0` を除いて SKU が重複している場合（`01234` や `1234` など）、在庫ソースを複数の製品に割り当てる際に、製品の一括アクションツール（**[!UICONTROL Select Products]**/**[!UICONTROL Actions]**/**[!UICONTROL Assign Inventory Source]**）が期待どおりに動作するようになりました。 以前は、1 つの製品のみが在庫ソースに割り当てられていました。 [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![ 修正された問題 ](../assets/fix.svg) 在庫が 0 の場合、`ProductInterface.only_x_left_in_stock` フィールドが 0 を返すようになりました。 以前は、null が返されていました。 [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![ 修正された問題 ](../assets/fix.svg) 管理者 **[!UICONTROL Stores]** ール/**[!UICONTROL Inventory]**/**[!UICONTROL Stocks]** からデフォルトの在庫を編集できるようになりました。 以前は、デフォルトの Stock に web サイトを割り当てることはできましたが、デフォルトの Stock にソースを追加または削除しようとすると、コンソールにJavaScript エラーが表示されていました。<!--- ACP2E-545-->

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-274--> **[!UICONTROL Display Out-Of-Stock Products]** 設定を有効にして在庫の単一ソースモードを使用すると、カテゴリリストの製品数が正しく表示されるようになりました。 新しいプラグインは、`AreProductsSalableInterface` と `StockConfigurationInterface` を使用して製品の合計数を決定するようになりました。 以前は、カテゴリ製品リストから誤った製品数量が返されていました。

![ 修正された問題 ](../assets/fix.svg) <!--- ACP2E-322--> 設定 **[!UICONTROL Move out of stock to the bottom]** 定が有効な場合、在庫が更新された後、設定可能な製品が製品リストの最後の位置に移動されるようになりました。 Elasticsearchインデックスの並べ替え順を否定する新しいカスタムデータベースクエリが実装されました。これは、管理者向けの並べ替え順を無視します。 以前は、この設定が有効な場合、設定可能な製品とその子製品は、リストの下部に移動されませんでした。

## v1.2.4

Inventory management 1.2.4 （モジュールバージョン：`magento/inventory-metapackage = 1.2.4`）は、バージョン 2.4.4 でサポートされ、Adobe Commerceのバージョン 2.4.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースと互換性があります。

![ 修正された問題 ](../assets/fix.svg)Commerceの管理商品リスト表示で、すべての商品の正確な販売可能数量の値が表示されるようになりました。 以前は、特殊文字を含む SKU を持つ在庫製品の売り上げ可能数量に対して空白の値が表示されていました。<!--- MC-41936-->

![ 修正された問題 ](../assets/fix.svg) 多くの（約 10,000 個の）在庫ソースを含むデプロイメントで買い物かごに製品を追加するなど、買い物かごおよびチェックアウトのアクションのパフォーマンスが向上しました。<!--- MC-42570-->

![ 修正された問題 ](../assets/fix.svg) `bin/magento inventory:reservation:list-inconsistencies` コマンドでは、データベースから予約が逃され、キャッシュがクリアされている場合でも、部分出荷の注文を正しく処理するようになりました。 以前は、事前にクリアされたキャッシュでこのコマンドを実行すると、Commerceに次のエラーが表示されていました。`Area code is not set`。<!--- MC-42142-->

![ 修正された問題 ](../assets/fix.svg) グループ化された製品の子製品の増分インデックス作成で、子を共有すると、他のグループ化された製品のインデックスが正しく作成されなくなりました。<!--- MC-41963-->

![ 修正された問題 ](../assets/fix.svg)API によってカテゴリから製品を削除した後、ストアフロントのカテゴリページに正しい製品数が表示されるようになりました。 以前は、インデックス再作成が発生するまで、カテゴリページの製品数が正しくありませんでした。<!--- MC-42287-->

![ 問題を修正 ](../assets/fix.svg) クレジットオプションが無効になっている場合、クレジットメモを作成する際に、設定可能な製品を在庫に返すことができるようになりまし **[!UICONTROL Manage Stock]**。 以前は、このオプションが無効になっている場合、Commerceのクレジットメモ作成ページに **在庫に戻る** チェックボックスが表示されていませんでした。<!--- MC-42002-->

![ 修正された問題 ](../assets/fix.svg)10,000 項目を超える在庫在庫の管理が改善されました。 以前は、パフォーマンスの問題により、マーチャントが web サイトを起動する前に管理者で在庫を編集できないことがありました。<!--- MC-42643-->

![ 修正された問題 ](../assets/fix.svg) 管理者の **[!UICONTROL User Roles]** ページが更新され、管理者に配信方法設定への制限付きアクセス権が提供されるようになりました。 _発送方法_ セクションの名前は _[!UICONTROL Delivery methods]_&#x200B;に変更され、_[!UICONTROL In-Store Pickup]_ は _[!UICONTROL Delivery methods]_&#x200B;セクションの下に移動します。 [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![ 修正された問題 ](../assets/fix.svg) クレジットメモが API で更新された後、Adobe Commerceで重複した製品予約が作成されなくなりました。<!--- MC-41757-->

![ 修正された問題 ](../assets/fix.svg) チェックアウトワークフローで「_[!UICONTROL Pick up in Store]_」タブから「_[!UICONTROL Shipping]_」タブに切り替えても、店舗内ピックアップ配信のみが使用可能な場合にJavaScript エラーがトリガーされなくなりました。<!--- MC-42808-->

![ 修正された問題 ](../assets/fix.svg) 販売可能な製品数量と在庫製品の数量が正しく同期されるようになりました。 以前は、キャンセルされた注文の在庫引当の報酬は再作成されませんでした。<!--- MC-42485-->

![ 修正された問題 ](../assets/fix.svg) バリデーターのパフォーマンスは、バンドルされた製品の出荷タイプ `Ship Together` の子製品に新しいソースを追加しないように最適化されています。<!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 （モジュールバージョン：`magento/inventory-metapackage = 1.2.3`）は、バージョン 2.4.3 でサポートされ、Adobe Commerceのバージョン 2.4.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースと互換性があります。

![ 問題を修正 ](../assets/fix.svg) フロントエンドでの複合製品の表示に関するいくつかの問題を修正しました。

![ 問題を修正 ](../assets/fix.svg) 最小限必要な量で買い物かごページ管理のパフォーマンスを向上しました。

![ 修正された問題 ](../assets/fix.svg) ソースの作成、在庫切れ項目、在庫ソーシング、割り当てられたソースの並べ替え、店舗内配信、在庫コマンドに関する問題を解決することを目的とした修正がいくつか導入されました。

![ 修正された問題 ](../assets/fix.svg) [!DNL Commerce] 店舗内配信で、3 桁のカナダの郵便番号をサポートするようになりました。 `geonames.org` で設定された制限により、6 桁のコードはサポートされていません。

![ 修正された問題 ](../assets/fix.svg) 管理者は、マルチストアデプロイメントの **製品** グリッドおよび **製品を編集** ページに、無効な製品のデフォルトの在庫の正しい数量を表示するようになりました。

![ 修正された問題 ](../assets/fix.svg) [!DNL Commerce] バンドル製品が再入荷したときに、カテゴリ製品キャッシュを更新するようになりました。

## 1.2.2

[!DNL Inventory Management] 1.2.2 （モジュールバージョン：`magento/inventory-metapackage = 1.2.2`）は、バージョン 2.4.2 でサポートされ、Adobe Commerceのバージョン 2.4.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースと互換性があります。

![ 問題を修正 ](../assets/fix.svg) フロントエンドでの複合製品の表示に関するいくつかの問題を修正しました。

![ 修正された問題 ](../assets/fix.svg)B2B で数量を更新中に、買い物かごページのパフォーマンスが向上しました。

![ 修正された問題 ](../assets/fix.svg) 店舗での受け取り、一括更新、在庫しきい値の問題を解決することを目的としたいくつかの修正。

![ 新機能 ](../assets/new.svg) 機能テ **ト。** 新しい機能テストを導入し、既存のテストの修正を提供して、安定性を高めました。

## 1.2.1

[!DNL Inventory Management] 1.2.1 （モジュールバージョン：`magento/inventory-metapackage = 1.2.1`）は、バージョン 2.4.1 でサポートされ、Adobe Commerceのバージョン 2.4.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースと互換性があります。

![ 修正された問題 ](../assets/fix.svg) `inventory_cleanup_reservations` cron ジョブに関する既知の問題を修正し、バンドル製品の店舗内ピックアップ機能に関する問題を修正しました。 この更新には、在庫計算、バンドル製品のサポート、バックオーダー機能に対する一般的な改善も含まれています。

![ 新機能 ](../assets/new.svg) 機能テ **ト。** 新しい機能テストを導入して、店舗でのピックアップ機能をさらにカバーするようになりました。

## 1.2.0

[!DNL Inventory Management] 1.2.0 （モジュールバージョン：`magento/inventory-metapackage = 1.2.0`）は、Adobe Commerceのバージョン 2.4.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースでサポートされています。

![ 問題を修正 ](../assets/fix.svg) ソース割り当て、スケーラブルな環境のサポート、および PHP 7.4、MySQL 8、PHPUNIT 9 との互換性に関する問題を解決するための多数の修正。

![ 新規 ](../assets/new.svg) ストア **配信方法。** チェックアウト時に集荷場所として使用するソースをユーザーが選択できるオプションを追加しました。 _販売および購入エクスペリエンスガイド [&#128279;](../stores-purchase/shipping-in-store-delivery.md) の  店舗での配信_ を参照してください。

![ 新規 ](../assets/new.svg) マルチソースモード用 **バンドル製品のサポート。** Inventory では、複数のソースを持つすべての製品タイプがサポートされます。

![ 新規 ](../assets/new.svg) 非同期在庫 **インデックス再作成。** 在庫を非同期で再インデックスする機能が追加され、いくつかの重要なシナリオのパフォーマンスが向上しました。

![ 新規 ](../assets/new.svg) バ **クインターフェイス。** 販売品質チェック用に新しいバルクインターフェイス `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`、`\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface` が導入されました。

![ 新 ](../assets/new.svg) テスト範囲 **拡大。** 新しい機能は、検出された問題と修正された問題を対象とする拡張テストなど、自動テストでカバーされています。

![ 既知の問題 ](../assets/bug.svg) **既知の問題。** 予約メタデータに `object_id` フィールドがないので、`inventory_cleanup_reservations` cron ジョブが正しく機能しません。 この問題は、[magento/inventory#3046](https://github.com/magento/inventory/pull/3046) で導入されました。

**回避策：** 次の MySQL クエリを実行して、予約を手動でクリーンアップします。

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 （モジュールバージョン：`inventory-composer-metapackage = 1.1.6`）はバージョン 2.3.6 でサポートされ、Adobe Commerceのバージョン 2.3.5、2.3.4、2.3.3、2.3.2、2.3.1、2.3.0、クラウドインフラストラクチャーのAdobe Commerce、およびMagento Open Sourceコードベースと互換性があります。

![ 修正された問題 ](../assets/fix.svg) バックオーダー、クレジットメモ、低在庫のレポートグリッドに関連する問題を解決するための修正、「不整合の解決」 CLI ツールに関連する修正および一般的な改善。

![ 新規 ](../assets/new.svg) 非同期在庫 **インデックス再作成。** 在庫を非同期で再インデックスする機能が追加され、いくつかの重要なシナリオのパフォーマンスが向上しました。

## 1.1.5

[!DNL Inventory Management] 1.1.5 （モジュールバージョン：`inventory-composer-metapackage = 1.1.5`）は、バージョン 2.3.5 でサポートされ、Adobe Commerceのバージョン 2.3.4、2.3.3、2.3.2、2.3.1、2.3.0、クラウドインフラストラクチャー上のAdobe Commerce、およびMagento Open Sourceコードベースと互換性があります。

![ 製品 SKU が変更された後 ](../assets/new.svg) 在庫を新規 **更新します。** 新しい動作「カタログとの同期」に切り替える新しい設定が導入されました。

![ 新機能 ](../assets/new.svg) 機能テ **ト。** テストカバレッジギャップを解消するために、新しい機能テストを導入しました。 テストの安定性と信頼性を高めるために、いくつかの問題を修正しました）。

![ 既知の問題 ](../assets/bug.svg) 製品の過剰販売を防ぐための修正、ストアフロントでの「在庫切れ」製品の表示、スケーラブルな環境サポートおよびユーザーインターフェイスの改善のための多数の修正。

## 1.1.4

[!DNL Inventory Management] 1.1.4 （モジュールバージョン：`inventory-composer-metapackage = 1.1.4`）は、バージョン 2.3.4 でサポートされ、Adobe Commerceのバージョン 2.3.3、2.3.2、2.3.1、2.3.0、クラウドインフラストラクチャー上のAdobe Commerce、およびMagento Open Sourceコードベースと互換性があります。

![ 問題を修正 ](../assets/fix.svg)**パフォーマンスが向上しました。** メモリ使用量を減らし、応答なくプロセスが停止した場合を回避するために、在庫予約 CLI コマンドのバンチングロジックが導入されました。

![ 新しくテスト範囲 ](../assets/new.svg)**拡大。** 多くの新しい機能テストを導入しました。 手動のインベントリ作成シナリオのほとんどは、自動テストでカバーされています。

![ 既知の問題 ](../assets/bug.svg) クレジットメモ、グループ化された製品、ソースと在庫の一括処理に関する問題を解決することを目的とした多数の修正。

## 1.1.3

[!DNL Inventory Management] 1.1.3 （モジュールバージョン：`inventory-composer-metapackage = 1.1.3`）は、バージョン 2.3.3 でサポートされ、Adobe Commerceのバージョン 2.3.2、2.3.1、2.3.0、クラウドインフラストラクチャー上のAdobe Commerce、およびMagento Open Sourceコードベースと互換性があります。

![ 問題を修正 ](../assets/fix.svg)**Adobe Commerceと B2B 機能との統合が改善されました。** [!DNL Inventory Management] は、デフォルト以外の在庫ソースおよび在庫を使用する web サイトで、次の機能を正しく使用できるようになりました。

- SKU で並べ替え（Adobe Commerce）
- クイックオーダー（B2B）
- 購買依頼リスト（B2B）

![ パフォーマンス ](../assets/new.svg)**向上。デフォルト** 在庫およびソースを実行している web サイトのストアフロントカタログの閲覧パフォーマンスが向上しました。

![ 新しくテスト範囲 ](../assets/new.svg)**拡大。** 自動化された機能および統合テストの対象範囲が大幅に増加しました。

## 1.1.2

[!DNL Inventory Management] 1.1.2 （モジュールバージョン：`inventory-composer-metapackage = 1.1.2`）は、バージョン 2.3.2 でサポートされ、Adobe Commerceのバージョン 2.3.1 および 2.3.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースと互換性があります。

![ 修正された問題 ](../assets/fix.svg)REST エンドポイントのGETの応答に `source_code` が追加さ `/V1/shipments` ました。<!-- https://github.com/magento/inventory/pull/2142 -->

![ 修正された問題 ](../assets/fix.svg) 未出荷注文のクレジットメモを発行した後に、予約を正しくクリアして製品数量を更新する問題を解決しました。 <!-- https://github.com/magento/inventory/pull/2179 --> すオプションを選択した場合

![ 修正された問題 ](../assets/fix.svg) 製品の作成時に数量を入力する際に、設定可能な製品の子の数量を正しく保存する問題を解決しました。<!-- https://github.com/magento/inventory/pull/2158 -->

[!DNL Inventory Management] 1.1.2 Betaの新しいモジュールには、次のものがあります。

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![ 新規 ](../assets/new.svg)**一括部分在庫転送エンドポイントを追加** – 現在の一括転送エンドポイントは、割り当てられているすべての数量を出荷元から出荷先ソースに移動します。 新しい `/rest/V1/inventory/bulk-partial-source-transfer` エンドポイントを使用すると、マーチャントは、一括操作としてソースからソースに部分的な在庫を転送できます。 特定の量を転送するには、`sku`、`qty`、`origin_source_code`、`destination_source_code` を含むリクエストをエンドポイントに入力します。 転送では、ソースが `sku` に割り当てられていること、転送に十分な数量が存在することなどを確認します。 REST API ドキュメントの [ 一括アクションのインベントリ ](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} を参照してください。<!-- https://github.com/magento/inventory/pull/2117 -->

![ 新規 ](../assets/new.svg)**追加済み予約 CLI** – 新しいコマンドを使用すると、予約の不整合を検出および解決するためのオプションが提供されます。 受注が発行およびステータス変更されると、[!DNL Inventory Management] は初期予約を生成し、報酬予約を介して更新します。 これらのコマンドは、検出された不整合のリストを注文 ID、SKU、在庫 ID 別に返し、解決するための予約を作成します。 詳細については、「[CLI リファレンス ](cli.md)」を参照してください。<!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![ 新規 ](../assets/new.svg)**ソースと SSA オプションのパフォーマンス向上** – 出荷中にソースを並べ替えて選択すると、多数のソースを持つ在庫のパフォーマンスが低下しました。 このリリースでは、出荷の SSA オプションを確認および選択する際に、使用可能なソースのリスト表示およびソートを行うパフォーマンスが大幅に向上しています。<!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![](../assets/new.svg) Inventory managementに対する新規 **追加されたGraphQLのサポート** – このリリースでは、新しい `magento/module-inventory-graph-ql` モジュールがインストールされます。 GraphQL[ProductInterface 属性 ](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} に、[!DNL Inventory Management] サポートの `only_x_left_in_stock` 属性と `stock_status` 属性が含まれるようになりました。<!-- https://github.com/magento/inventory/pull/2124 -->

![ 新規 ](../assets/new.svg)**割り当てられたソースのシンプルな UI** – 製品ページの割り当てられたソース テーブルでは、コンテンツが簡素化されて更新が容易になり、多数のソースを表示する際のパフォーマンスが向上しています。 すべてのソースがソース名別にリストされます（`source_code` の場合はカーソルを合わせます）。

![ 新規 ](../assets/new.svg)**エクスポート集計在庫サービス** – このリリースでは、Amazon、eBay、Googleのショッピング広告などの外部Sales Channelをサポートする新しいエクスポート集計在庫サービス（システム内で予約を保持）が提供されます。 <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 （モジュールバージョン：`inventory-composer-metapackage = 1.1.0`）は、Adobe Commerce、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースのバージョン 2.3.0 でサポートされ、互換性があります。 [!DNL Inventory Management] 1.1.1 は、パッケージ名のアップデートとしてのみリリースされ、バージョン 2.3.1 でサポートされ、Adobe Commerceのバージョン 2.3.0、クラウドインフラストラクチャー上のAdobe Commerce、Magento Open Sourceコードベースと互換性があります。

![ 問題を修正 ](../assets/fix.svg)**シングルソースモードとマルチソースモードのElasticsearchがサポートされるようになりました** — カスタムストックでElasticsearchを設定および使用できるようになりました。 インストールについては、[Elasticsearchサービスの設定 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html?lang=ja){target="_blank"} を参照してください。<!-- PR https://github.com/magento/inventory/pull/1943 -->

![ 修正された問題 ](../assets/fix.svg) デフォルトの Stock に関するパフォーマンスの問題を解決し、多数の操作でパフォーマンスを大幅に向上させました。 改善により、シングルソースモード、Sourceへの在庫転送、ストアフロントカテゴリページ、販売可能数量の計算のパフォーマンスが向上しました。

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![ 修正された問題 ](../assets/fix.svg) 設定可能な製品およびグループ化された製品の在庫切れステータスと在庫への一括在庫転送に関する問題を解決しました。 親製品を選択して一括アクションを実行しても、製品のステータスには影響しません。 親商品が在庫にある場合、その商品は在庫にあります。

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![New](../assets/new.svg)**Distance Priority Algorithm** — Distance Priority Algorithm は、ディスタンスベースの配送レコメンデーション用の新しい標準搭載Source Selection Algorithm です。 このアルゴリズムでは、出荷先所在地の事業所がソース事業所と比較され、出荷を履行する最も近いソースが決定されます。 距離は、読み込んだジオコードの位置データまたはGoogleの方向（ドライブ、ウォーキング、サイクリング）を使用して、物理的な距離または 1 つの場所から別の場所への移動時間によって決定される場合があります。

![ 新規 ](../assets/new.svg)**拡張されたソース数量リスト** – 多数のソースを持つマーチャントは、製品グリッドを通じて、製品ごとのすべてのソースを簡単に移動して表示できます。 各製品には、最低 5 つのソースと一致する数量が表示されます。 ソースの上にマウスポインターを置くと、ソースと現在の数量のリスト全体をスクロールできます。

![ 既知の問題 ](../assets/bug.svg) Magento Open SourceとAdobe Commerce v2.3.1 に関する既知の問題 – ソース間のデータの非同期移行では、PHP クラスとメソッド名を反映したトピック名を持つ非同期 API の変更に起因する問題が発生します。 同期操作を使用する場合は、**[!UICONTROL Run asynchronously]** を `No` に設定することをお勧めします。
