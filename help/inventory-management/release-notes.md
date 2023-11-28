---
title: '''[!DNL Inventory Management] リリースノート'
description: すべての [!DNL Inventory Management] リリース。
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '3361'
ht-degree: 0%

---

# [!DNL Inventory Management] リリースノート

これらのリリースノートでは、 [!DNL Inventory Management] およびを含めます。

![新規](../assets/new.svg) 新機能
![修正された問題](../assets/fix.svg) 修正点および改善点
![既知の問題](../assets/bug.svg) 既知の問題

[!DNL Inventory Management] は、寄稿者向けのMagento Open Sourceコミュニティエンジニアリング特別プロジェクトです。 参加して貢献するには、 [GitHub プロジェクト](https://github.com/magento/inventory) リポジトリと [wiki](https://github.com/magento/inventory/wiki) をクリックして開始します。 プロジェクトについて話し合うには、 [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) チャネル ([自己登録](https://opensource.magento.com/slack)) をクリックします。

[リリーススケジュール](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} を参照してください。

## v1.2.6

[!DNL Inventory Management] 1.2.6 ( モジュールバージョン： `magento/inventory-metapackage = 1.2.6`) はバージョン 2.4.6 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースのバージョン 2.4.0 と互換性があります。

![修正された問題](../assets/fix.svg) 売り切れた子製品が在庫に戻されると、ストアフロントに複合製品（設定可能、バンドル、グループ化）が在庫として表示されるようになりました。 以前は、店頭では、このような状況で複合製品が在庫切れであったことを示していました。 <!-- ACP2E-1106-->

![修正された問題](../assets/fix.svg) 数量が 0 に設定されたオプションが作成された場合、設定可能な製品オプションが、在庫切れとしてストアフロントに表示されるようになりました。 **[!UICONTROL Display out-of-stock products]** が有効になっている。 <!-- ACP2E-1148-->

![修正された問題](../assets/fix.svg) 在庫数量が変更され、製品が在庫に残っている場合、カテゴリページキャッシュが無効化されなくなりました。 storefront カテゴリページの製品数（およびその他の何も）が変更されたときに、Adobe Commerceがキャッシュからページを読み込むようになりました。 <!-- ACP2E-118-->

![修正された問題](../assets/fix.svg) シングルソースモードで **[!UICONTROL Display Out-Of-Stock Products]** 設定を有効にします。 Adobe Commerceは、カウント時に製品が販売可能かどうかを確認できるようになりました。 <!-- ACP2E-1033-->

![修正された問題](../assets/fix.svg) 在庫が有効な場合に、店舗内配信の買い物かごの価格ルールが期待どおりに動作するようになりました。 以前は、買い物かご価格のルールによって生成された割引が、これらの条件では適用されていませんでした。 <!-- ACP2E-1015-->

![修正された問題](../assets/fix.svg) スケジュールモードで製品在庫を更新しても、すべてのキャッシュがクリアされなくなりました。 以前は、インベントリインデクサーはすべての設定キャッシュをクリアしていました。 <!-- ACP2E-1003-->

![修正された問題](../assets/fix.svg) の値 **[!UICONTROL Allow Multiple Boxes for Shipping]** Advanced Inventory の製品の属性が期待どおりに保存されるようになりました。 <!-- ACP2E-992-->

![修正された問題](../assets/fix.svg) Adobe Commerceは、店頭受け取りで発注された注文に対して、部分払い戻しクレジットメモの後に、正確な予約補償を発行するようになりました。 以前は、に保存された誤った予約 `inventory_reservation` 管理者ユーザーがクレジット・メモを選択せずに作成した場合の表 **[!UICONTROL Return to Stock]** チェックボックス。 <!-- ACP2E-979-->

![修正された問題](../assets/fix.svg) Adobe Commerceでは、マルチソースインベントリを実装するデプロイメントで、そのバリエーションの 1 つが手動で在庫に戻された場合に、設定可能な製品がストアフロントに在庫切れとして表示されなくなりました。 <!-- ACP2E-952-->

![修正された問題](../assets/fix.svg) 製品グリッド上の列の位置 (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) は、複数の在庫ソースが設定されたデプロイメントでページがリロードされた後、以前の位置に戻らなくなりました。 <!-- ACP2E-925-->

![修正された問題](../assets/fix.svg) 仮想製品に対してクレジットメモを発行した後、在庫数が正しくなり、 **[!UICONTROL Back to stock]** チェックボックスが選択されていません。 <!-- ACP2E-908-->

![修正された問題](../assets/fix.svg) デフォルト以外の在庫に割り当てられた自動製品並べ替えと範囲で、カテゴリを保存できるようになりました。 以前は、Adobe Commerceはカテゴリを保存せず、次のエラーを表示していました。 `Something went wrong while saving the category`. <!-- ACP2E-859-->

![修正された問題](../assets/fix.svg) 製品が在庫切れの設定可能なバリエーションをすべて含む状態で作成された場合、設定可能な製品在庫ステータスが期待どおりに更新されるようになりました。 <!-- ACP2E-813-->

![修正された問題](../assets/fix.svg) 予約不整合アナライザーツールは、構成可能な製品、バンドル、およびグループ化された製品を含む部分出荷済の注文で正しく機能するようになりました。 複合製品タイプを解析しました。 以前は、キャンセルと返金は、構成可能なバンドル製品の下位製品の注文項目ではなく、親製品に対してのみ保存されていました。 <!-- ACP2E-924-->

![修正された問題](../assets/fix.svg) 管理者ユーザーが 200 以上の在庫ソースを在庫または製品に割り当てようとすると、Adobe Commerceでエラーが表示されなくなりました。 <!-- ACP2E-1180-->

![修正された問題](../assets/fix.svg) Adobe Commerceでは、商品の削除元となる注文のクレジットメモの作成がサポートされるようになりました。 以前は、請求書の作成後に商品が注文から削除された場合、商人はクレジットメモを作成できませんでした。 アプリケーションが次のエラーを表示しました： `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![修正された問題](../assets/fix.svg) ストアは、1 つのストア ID と複数のストア ID の両方に基づいてフィルタリングされるようになりました。 The `event` 予約済み属性コードのリストに製品属性コードが追加されました。 以前は、在庫モジュールのインストール時に、低在庫レポートで例外がスローされていました。 <!-- ACP2E-1017-->

![修正された問題](../assets/fix.svg) レイヤー化されたナビゲーションフィルターが期待どおりに機能し、在庫切れの製品がストアフロントのカテゴリ製品リストに追加されるようになりました。 新しい `is_out_of_stock` 並べ替え属性では、storefrontElasticsearchコレクションに動的フィールドマッパーが使用されます。 <!-- ACP2E-748-->

![修正された問題](../assets/fix.svg) 子製品の在庫ステータスが REST によって変更されると、複合製品（バンドル、グループ化、および設定可能）の在庫ステータスが期待どおりに更新されます `POST /rest/V1/inventory/source-items` を呼び出します。 <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 ( モジュールバージョン： `magento/inventory-metapackage = 1.2.5`) はバージョン 2.4.5 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースのバージョン 2.4.0 と互換性があります。

![修正された問題](../assets/fix.svg) マーチャントが管理者から出荷を作成する際に、バンドルおよびグループ化された製品のデフォルトの在庫ステータスが期待どおりに更新されるようになりました。 以前は、出荷後も、これらの製品のステータスは変わりませんでした。 <!--- ACP2E-418-->

![修正された問題](../assets/fix.svg) 次の条件の 1 つを満たした場合、構成可能な製品が在庫に戻されるようになりました。 1. 親製品には、少なくとも 1 つの保存済み子が在庫に含まれています。 2.設定可能な製品自体が更新され、次のように設定されました。 **在庫** 少なくとも一人の子供が在庫にいた <!--- ACP2E-443-->

![修正された問題](../assets/fix.svg) REST API を通じて実装された在庫の変更が、製品の詳細ページに期待どおりに反映されるようになりました。 前回と現在の在庫ステータスを比較した後に、カタログ製品のキャッシュが消去されるようになりました。 以前は、コールバック関数を省略すると、在庫ステータスの変更が誤って評価され、必要なキャッシュのクリーニングにトリガーが生じていませんでした。 その結果、ストアフロントに在庫の変更が反映されませんでした。 <!--- ACP2E-161-->

![修正された問題](../assets/fix.svg) デフォルトの在庫に割り当てられ、以前は在庫切れだった製品は、ソース項目が次を使用して更新された後、ストアフロントに表示されるようになりました。 `/V1/inventory/source-items`. 以前は、この REST API エンドポイントが間違った `stock_status`. <!--- ACP2E-562-->

![修正された問題](../assets/fix.svg) 一括処理 (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) ソースに、先頭のゼロを除く重複のある SKU が含まれている場合 ( 例えば、 `01234` および `1234`) をクリックします。 以前は、アプリケーションは在庫ソースの割り当てを解除せず、エラーをスローしていました。 <!--- ACP2E-2641-->

![修正された問題](../assets/fix.svg) 製品の在庫ステータスが常に **在庫** ストアフロントで、無限の逆注文が有効になっていて、商品がバックオーダーされた数量に関係なくカスタム在庫に割り当てられている場合。 以前は、逆注文が有効になっていても、製品が在庫切れになっていました。 <!--- ACP2E-664-->

![修正された問題](../assets/fix.svg) ソース品目が `POST /V1/inventory/source-items`. API を通じて子製品が更新された後、デフォルトの在庫チェック用の新しい在庫プラグインが追加され、設定可能な製品数量とステータスが更新されます。 <!--- ACP2E-442-->

![修正された問題](../assets/fix.svg) 在庫切れのグループ化された製品がストアフロントのカテゴリページに表示されなくなりました。 <!--- ACP2E-2082-->

![修正された問題](../assets/fix.svg) でパッケージ名を修正しました。 `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![修正された問題](../assets/fix.svg) 複数のソース/在庫のデプロイメントで、数量がゼロの製品を注文した後、管理画面に逆オーダーのステータスが正しく表示されるようになりました。 [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![修正された問題](../assets/fix.svg) 在庫セクションからバンドル製品が更新されると、在庫切れのバンドル製品がストアフロントのカテゴリページに表示されなくなりました。 <!--- ACP2E-2012-->

![修正された問題](../assets/fix.svg) PHP 7.4 との互換性の問題は解決されました。 <!--- AC-3192-->

![修正された問題](../assets/fix.svg) 多数のオプション（数件の 100）を含むバンドル製品を含む保存操作のパフォーマンスが向上しました。 以前は、これらの大きなバンドル製品の保存に数分かかり、在庫サービスが有効な状態でデプロイメントがタイムアウトになることがありました。 [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![修正された問題](../assets/fix.svg) 製品の一括アクションツール (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) が複数の製品に割り当てられる際に、主要な製品を除いて SKU が重複している場合に、在庫ソースが期待どおりに動作するようになりました `0` ( 例： `01234` および `1234`) をクリックします。 以前は、在庫ソースが割り当てられた製品は 1 つだけでした。 [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![修正された問題](../assets/fix.svg) The `ProductInterface.only_x_left_in_stock` 在庫が 0 の場合、フィールドは 0 を返すようになりました。 以前は null を返していました。 [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![修正された問題](../assets/fix.svg) 管理者からデフォルトの在庫を編集できるようになりました **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. 以前は、Web サイトをデフォルトの在庫に割り当てることは可能でしたが、デフォルトの在庫にソースを追加または削除しようとすると、JavaScript エラーがコンソールに表示されていました。 <!--- ACP2E-545-->

![修正された問題](../assets/fix.svg) <!--- ACP2E-274--> 在庫シングルソースモードで **[!UICONTROL Display Out-Of-Stock Products]** 設定を有効にします。 新しいプラグインでは、 `AreProductsSalableInterface` および `StockConfigurationInterface` をクリックして製品の合計数を判断します。 以前は、カテゴリの製品リストから誤った製品数が返されていました。

![修正された問題](../assets/fix.svg) <!--- ACP2E-322--> 在庫が更新された後、設定可能な製品が製品リストの最後の位置に移動され、 **[!UICONTROL Move out of stock to the bottom]** の設定が有効になっています。 Elasticsearchインデックスの並べ替え順を無効にする新しいカスタムデータベースクエリが実装され、管理者が有効にした並べ替え順が無視されます。 以前は、この設定が有効になっている場合、設定可能な製品とその子製品がリストの下部に移動されませんでした。

## v1.2.4

Inventory management 1.2.4( モジュールバージョン： `magento/inventory-metapackage = 1.2.4`) はバージョン 2.4.4 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースのバージョン 2.4.0 と互換性があります。

![修正された問題](../assets/fix.svg) Commerce では、管理製品リスト表示ですべての製品に対して正確な販売可能数量値が表示されるようになりました。 以前は、特殊文字を含む SKU を使用した在庫品の販売可能数量に対して空白の値が表示されていました。 <!--- MC-41936-->

![修正された問題](../assets/fix.svg) 多数（約 10,000）の在庫ソースを持つデプロイメントで、買い物かごに製品を追加するなど、買い物かごとチェックアウトのアクションのパフォーマンスが向上しました。 <!--- MC-42570-->

![修正された問題](../assets/fix.svg) The `bin/magento inventory:reservation:list-inconsistencies` コマンドは、予約がデータベースから失われ、キャッシュがクリアされた場合でも、一部出荷の注文を正しく処理するようになりました。 以前は、このコマンドがキャッシュが事前にクリアされて実行された場合、Commerce で次のエラーが表示されていました。 `Area code is not set`. <!--- MC-42142-->

![修正された問題](../assets/fix.svg) グループ化された製品の子製品の増分インデックスを作成すると、子が共有されているときに、他のグループ化された製品のインデックスが誤って作成されることはなくなりました。 <!--- MC-41963-->

![修正された問題](../assets/fix.svg) API でカテゴリから製品を削除した後、ストアフロントカテゴリページに正しい製品数が表示されるようになりました。 以前は、カテゴリページの製品数が、インデックスの再作成がおこなわれるまで正しくありませんでした。 <!--- MC-42287-->

![修正された問題](../assets/fix.svg) クレジットメモを作成する際に、設定可能な製品を在庫に戻すことができるようになりました ( **[!UICONTROL Manage Stock]** オプションは無効です。 以前は、Commerce で **在庫に戻る** このオプションが無効な場合は、「クレジット・メモ作成」ページのチェック・ボックス。 <!--- MC-42002-->

![修正された問題](../assets/fix.svg) 10,000 品目を超える在庫の管理が改善しました。 以前は、パフォーマンスの問題により、マーチャントが Web サイトを起動する前に Admin で在庫を編集できないことがありました。 <!--- MC-42643-->

![修正された問題](../assets/fix.svg) The **[!UICONTROL User Roles]** 管理のページが更新され、管理者に配信方法設定へのアクセス権が制限されます。 The _発送方法_ 「 」セクションの名前が「 」に変更されました。 _[!UICONTROL Delivery methods]_、および_[!UICONTROL In-Store Pickup]_ が _[!UICONTROL Delivery methods]_」セクションに入力します。 [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![修正された問題](../assets/fix.svg) Adobe Commerceは、クレジットメモが API によって更新された後、重複する製品予約を作成しなくなりました。 <!--- MC-41757-->

![修正された問題](../assets/fix.svg) 次からの切り替え： _[!UICONTROL Pick up in Store]_タブで_[!UICONTROL Shipping]_ ストア内ピックアップ配信のみが使用可能な場合に、チェックアウトワークフローのタブに JavaScript エラーがトリガーされなくなりました。 <!--- MC-42808-->

![修正された問題](../assets/fix.svg) 販売可能な製品数と在庫内の製品数が正しく同期されるようになりました。 以前は、キャンセルされた注文に対して在庫予約報酬が再作成されていませんでした。 <!--- MC-42485-->

![修正された問題](../assets/fix.svg) バリデータのパフォーマンスは、出荷タイプがバンドルされた製品の子製品に新しいソースが追加されるのを防ぐために最適化されています `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 ( モジュールバージョン： `magento/inventory-metapackage = 1.2.3`) はバージョン 2.4.3 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースのバージョン 2.4.0 と互換性があります。

![修正された問題](../assets/fix.svg) フロントエンドでの複合製品の表示に関するいくつかの問題を修正しました。

![修正された問題](../assets/fix.svg) 必要最小限の数量で買い物かごのページ管理のパフォーマンスが向上しました。

![修正された問題](../assets/fix.svg) ソースの作成、在庫品目の不足、在庫ソーシング、割り当て済みソースの並べ替え、店舗内配信、在庫コマンドの問題を解決するために、いくつかの修正がおこなわれました。

![修正された問題](../assets/fix.svg) [!DNL Commerce] では、店舗での配信に 3 桁のカナダの郵便番号がサポートされるようになりました。 6 桁のコードは、 `geonames.org`.

![修正された問題](../assets/fix.svg) 管理者が、 **製品** グリッドと **製品を編集** マルチストアデプロイメント用のページ。

![修正された問題](../assets/fix.svg) [!DNL Commerce] バンドル製品が在庫に戻ったときにカテゴリ製品キャッシュを更新するようになりました。

## 1.2.2

[!DNL Inventory Management] 1.2.2 ( モジュールバージョン： `magento/inventory-metapackage = 1.2.2`) はバージョン 2.4.2 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースのバージョン 2.4.0 と互換性があります。

![修正された問題](../assets/fix.svg) フロントエンドでの複合製品の表示に関するいくつかの問題を修正しました。

![修正された問題](../assets/fix.svg) B2B での数量更新時の買い物かごページのパフォーマンスが向上しました。

![修正された問題](../assets/fix.svg) いくつかの修正は、店舗でのピックアップ、一括更新、および在庫しきい値の問題を解決することを目的におこなわれました。

![新規](../assets/new.svg) **機能テスト。** 新しい機能テストを導入し、既存のテストの修正を提供して安定性を高めました。

## 1.2.1

[!DNL Inventory Management] 1.2.1 ( モジュールバージョン： `magento/inventory-metapackage = 1.2.1`) はバージョン 2.4.1 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースのバージョン 2.4.0 と互換性があります。

![修正された問題](../assets/fix.svg) 次に関連する既知の問題を修正しました： `inventory_cleanup_reservations` cron ジョブを実行し、バンドル製品のストア内ピックアップ機能に関する問題に対処しました。 このアップデートには、在庫計算、バンドル製品のサポート、バックオーダー機能の全般的な改善も含まれています。

![新規](../assets/new.svg) **機能テスト。** 店舗でのピックアップ機能を追加する新しい機能テストが導入されました。

## 1.2.0

[!DNL Inventory Management] 1.2.0 ( モジュールバージョン： `magento/inventory-metapackage = 1.2.0`) は、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースのバージョン 2.4.0 でサポートされます。

![修正された問題](../assets/fix.svg) ソース割り当て、スケーラブルな環境機能のサポート、PHP 7.4、MySQL 8、PHPUNIT 9 との互換性に関する問題を解決するための多くの修正を行いました。

![新規](../assets/new.svg) **店舗での配信方法。** チェックアウト時にピックアップの場所として使用するソースを選択するオプションが追加されました。 詳しくは、 [店内配信](../stores-purchase/shipping-in-store-delivery.md) （内） _セールスおよび購入エクスペリエンスガイド_.

![新規](../assets/new.svg) **マルチソースモード用のバンドル製品のサポート。** 在庫は、複数のソースを持つすべての製品タイプをサポートします。

![新規](../assets/new.svg) **非同期的な在庫のインデックス再作成。** 在庫のインデックスを非同期で再作成する機能と、いくつかの重要なシナリオのパフォーマンスを向上させる機能を追加しました。

![新規](../assets/new.svg) **一括インターフェイス。** 販売性チェック用の新しい一括インターフェイスが導入されました。 `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![新規](../assets/new.svg) **テスト対象の拡大。** 新しい機能は、検出された問題や修正された問題に対する拡張された対象を含む、自動化されたテストでカバーされます。

![既知の問題](../assets/bug.svg) **既知の問題。** この `object_id` 予約メタデータのフィールドが `inventory_cleanup_reservations` cron ジョブが正常に動作しなかった問題を修正しました。 この問題は、 [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**回避策：** 次の MySQL クエリを実行して、予約を手動でクリーンアップします。

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 ( モジュールバージョン： `inventory-composer-metapackage = 1.1.6`) はバージョン 2.3.6 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースのバージョン 2.3.5、2.3.4、2.3.3、2.3.2、2.3.1、2.3.0 と互換性があります。

![修正された問題](../assets/fix.svg) バックオーダー、クレジットメモ、低在庫レポートグリッド、「不整合の解決」CLI ツールと一般的な改善に関連する修正を修正。

![新規](../assets/new.svg) **非同期的な在庫のインデックス再作成。** 在庫のインデックスを非同期で再作成する機能と、いくつかの重要なシナリオのパフォーマンスを向上させる機能を追加しました。

## 1.1.5

[!DNL Inventory Management] 1.1.5 ( モジュールバージョン： `inventory-composer-metapackage = 1.1.5`) は、バージョン 2.3.5 でサポートされ、Adobe Commerce、Adobe Commerce、クラウドインフラストラクチャ上のバージョン、Magento Open Sourceコードベースのバージョン 2.3.4、2.3.3、2.3.2、2.3.1、2.3.0 と互換性があります。

![新規](../assets/new.svg) **製品 SKU が変更されたら、在庫を更新します。** 新しい動作に切り替えるための新しい設定「カタログと同期」が追加されました。

![新規](../assets/new.svg) **機能テスト。** テストカバレッジのギャップを解消する新しい機能テストを導入しました。 テストの安定性と信頼性を高めるために、いくつかの問題を修正しました。

![既知の問題](../assets/bug.svg) 製品のオーバーセル、ストアフロントでの「在庫切れ」製品の表示、スケーラブルな環境サポートとユーザーインターフェイスの改善のための多数の修正を防ぐために修正しました。

## 1.1.4

[!DNL Inventory Management] 1.1.4 ( モジュールバージョン： `inventory-composer-metapackage = 1.1.4`) はバージョン 2.3.4 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Sourceコードベースのバージョン 2.3.3、2.3.2、2.3.1、2.3.0 と互換性があります。

![修正された問題&#x200B;](../assets/fix.svg)**パフォーマンスの向上。** Inventory Reservations CLI コマンドのバンチングロジックが導入され、メモリ使用量を削減し、応答なしでプロセスが停止した場合のケースを回避できます。

![新規&#x200B;](../assets/new.svg)**テスト対象の拡大。** 多くの新しい機能テストが導入されました。 手動の在庫シナリオのほとんどは、自動化されたテストでカバーされます。

![既知の問題](../assets/bug.svg) クレジットメモ、グループ化された製品、ソースおよび在庫の一括処理の問題を解決するための多数の修正を行いました。

## 1.1.3

[!DNL Inventory Management] 1.1.3 ( モジュールバージョン： `inventory-composer-metapackage = 1.1.3`) はバージョン 2.3.3 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Sourceコードベースのバージョン 2.3.2、2.3.1、2.3.0 と互換性があります。

![修正された問題&#x200B;](../assets/fix.svg)**Adobe Commerceおよび B2B 機能との統合が改善されました。** [!DNL Inventory Management] は、デフォルト以外の在庫ソースおよび在庫を使用する Web サイトで、次の機能と正しく連携するようになりました。

- SKU 別の注文 (Adobe Commerce)
- クイックオーダー (B2B)
- 購買依頼リスト (B2B)

![新規&#x200B;](../assets/new.svg)**パフォーマンスの向上。** デフォルトの在庫およびソースを実行する Web サイトのストアフロントカタログの参照パフォーマンスが向上しました。

![新規&#x200B;](../assets/new.svg)**テスト対象の拡大。** 機能および統合の自動テスト対象が大幅に増加しました。

## 1.1.2

[!DNL Inventory Management] 1.1.2 ( モジュールバージョン： `inventory-composer-metapackage = 1.1.2`) は、バージョン 2.3.2 でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Sourceコードベースのバージョン 2.3.1、2.3.0 との互換性があります。

![修正された問題](../assets/fix.svg) 追加済み `source_code` をGETの `/V1/shipments` REST エンドポイント。 <!-- https://github.com/magento/inventory/pull/2142 -->

![修正された問題](../assets/fix.svg) 未発送の注文に対してクレジットメモを発行した後に、予約を正しくクリアし、製品数量を更新する問題を解決しました。 次のオプションを選択した場合： <!-- https://github.com/magento/inventory/pull/2179 -->

![修正された問題](../assets/fix.svg) 製品の作成時に数量を入力する際に、設定可能な製品の子の数量が正しく保存される問題を修正しました。 <!-- https://github.com/magento/inventory/pull/2158 -->

の新しいモジュール [!DNL Inventory Management] 1.1.2 ベータ版には以下が含まれます。

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![新規](../assets/new.svg) **在庫の一部を一括転送エンドポイントとして追加しました。**  — 現在の一括転送エンドポイントでは、割り当てられたすべての数量が接触チャネルから宛先のソースに移動します。 新しい `/rest/V1/inventory/bulk-partial-source-transfer` エンドポイントを使用すると、マーチャントは一括操作として部分的な在庫をソースからソースに転送できます。 特定の量を転送するには、 `sku`, `qty`, `origin_source_code`、および `destination_source_code`. 転送は、ソースが `sku`、転送するのに十分な量などが存在します。 詳しくは、 [在庫一括処理](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} （ REST API ドキュメント）を参照してください。 <!-- https://github.com/magento/inventory/pull/2117 -->

![新規](../assets/new.svg) **予約 CLI を追加しました**  — 新しいコマンドでは、予約の不整合を検出して解決するオプションが提供されます。 注文の送信および変更ステータスに応じて、 [!DNL Inventory Management] は、報酬の予約を通じて初期予約と更新を生成します。 これらのコマンドは、注文 ID、SKU、および Stock ID によって不整合が検出されたリストを返し、解決する予約を作成します。 詳しくは、 [CLI リファレンス](cli.md) を参照してください。 <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![新規](../assets/new.svg) **ソースと SSA オプションのパフォーマンス向上** ★出荷中にソースを並べ替えて選択すると、ソース数の多い在庫のパフォーマンスが低下。 このリリースでは、出荷時の SSA オプションの確認と選択を行う際に、使用可能なソースの一覧表示と並べ替えを大幅に改善しました。 <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![新規](../assets/new.svg) **GraphQLのInventory managementサポートを追加しました。**  — このリリースでは、新しい `magento/module-inventory-graph-ql` モジュール。 ザGraphQL [製品インターフェイス属性](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} にが含まれるようになりました `only_x_left_in_stock` および `stock_status` 属性 [!DNL Inventory Management] サポート。 <!-- https://github.com/magento/inventory/pull/2124 -->

![新規](../assets/new.svg) **割り当てられたソースの簡易 UI**  — 製品ページの「割り当てられたソース」の表では内容が簡素化され、更新が容易になり、多数のソースを表示する際のパフォーマンスが向上しました。 すべてのソースがソース名でリストされます ( `source_code`) をクリックします。

![新規](../assets/new.svg) **集計在庫サービスのエクスポート**  — このリリースでは、Amazon、eBay、Google Shopping Ads などの外部Sales Channelをサポートする新しい書き出し集約型の在庫サービス（システムでの予約を維持）が提供されます。  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 ( モジュールバージョン： `inventory-composer-metapackage = 1.1.0`) は、Adobe Commerceのバージョン 2.3.0、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースとサポートされ、互換性があります。 [!DNL Inventory Management] 1.1.1 は、パッケージ名の更新としてのみリリースされ、バージョン 2.3.1 でサポートされ、Adobe Commerceのバージョン 2.3.0、Adobe Commerce on cloud infrastructure、およびMagento Open Sourceコードベースとの互換性があります。

![修正された問題](../assets/fix.svg) **シングルモードとマルチソースモードのElasticsearchのサポートを追加しました。**  — カスタム在庫のElasticsearchを設定および使用できるようになりました。 詳しくは、 [Elasticsearchサービスの設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} を参照してください。 <!-- PR https://github.com/magento/inventory/pull/1943 -->

![修正された問題](../assets/fix.svg) 多数の操作でパフォーマンスが大幅に向上するように、デフォルトの在庫のパフォーマンスの問題を解決しました。 シングルソースモード、在庫をソースに転送、ストアフロントカテゴリページ、販売可能数量の計算のパフォーマンスが向上しました。

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![修正された問題](../assets/fix.svg) 設定可能な製品およびグループ化された製品で、在庫切れステータスと在庫への一括在庫転送の問題を解決しました。 親製品の選択と一括操作の実行は、製品のステータスには影響しません。 親製品が在庫にある場合、その製品は在庫に残ります。

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![新規](../assets/new.svg) **距離優先度のアルゴリズム** — Distance Priority Algorithm は、距離ベースの出荷レコメンデーション用の、標準の新しいソース選択アルゴリズムです。 このアルゴリズムは、出荷先住所の場所をソースの場所と比較して、出荷を達成するために最も近いソースを決定します。 距離は、読み込んだジオコード位置データまたはGoogleの方向（運転、歩行、自転車）を使用して、物理的な距離またはある場所から別の場所への移動に費やした時間によって決定できます。

![新規](../assets/new.svg) **展開されたソース数量リスト**  — ソース数が多いマーチャントは、製品グリッドを通じて、製品ごとのすべてのソースを簡単に移動し、表示できます。 各製品には、少なくとも 5 つのソースと一致する数量が表示されます。 ソースにカーソルを合わせると、ソースのリスト全体と現在の数量をスクロールできます。

![既知の問題](../assets/bug.svg) Magento Open SourceとAdobe Commerce v2.3.1 に関する既知の問題 — ソース間のデータの非同期移行では、PHP クラスとメソッド名を反映したトピック名を持つ非同期 API の変更が原因で問題が発生します。 同期操作の使用、設定 **[!UICONTROL Run asynchronously]** から `No`、をお勧めします。
