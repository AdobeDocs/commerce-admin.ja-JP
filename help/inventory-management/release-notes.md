---
title: '[!DNL Inventory Management] リリースノート'
description: すべての [!DNL Inventory Management]  リリースについて詳しくは、リリースノートを参照してください。
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
TQID: https://experienceleague.adobe.com/UaHQorWcNwDPzAMuV-e27DDH-G5D0k5qENPTINNfiTk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 3533
ht-degree: 0%

---

# [!DNL Inventory Management] リリースノート

これらのリリースノートには、[!DNL Inventory Management]のリリースが記載されており、次のものが含まれます。

![新機能](../assets/new.svg)
![修正された問題](../assets/fix.svg)修正と改善
![既知の問題](../assets/bug.svg)既知の問題

[!DNL Inventory Management]は、Magento Open Source コミュニティ エンジニアリングの特別プロジェクトです。 参加して貢献するには、[GitHub プロジェクト ](https://github.com/magento/inventory) リポジトリと[wiki](https://github.com/magento/inventory/wiki)を参照してください。 プロジェクトについて話し合うには、[Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) チャネル （[ セルフサインアップ ](https://opensource.magento.com/slack)）に参加してください。

サポートされているリリースと互換性のあるリリースについては、[ リリーススケジュール ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"}を参照してください。

## v1.2.7

[!DNL Inventory Management] 1.2.7 リリースノートは、[ コア 2.4.7 リリースノート ](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1)に含まれています。

## v1.2.6

[!DNL Inventory Management] 1.2.6 （モジュールバージョン：`magento/inventory-metapackage = 1.2.6`）は、バージョン 2.4.6でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースのバージョン 2.4.0と互換性があります。

![修正済みの問題](../assets/fix.svg) ストアフロントでは、売り切れた子商品が在庫に戻されたときに、複合商品（設定可能、バンドル、グループ化）が在庫として表示されるようになりました。 以前、ストアフロントは、これらの条件で複合製品の在庫切れを示していました。<!-- ACP2E-1106-->

![修正済みの問題](../assets/fix.svg)数量が0に設定され、**[!UICONTROL Display out-of-stock products]**&#x200B;が有効になっているオプションが作成された場合、ストアフロントで設定可能な製品オプションが在庫切れとして表示されるようになりました。<!-- ACP2E-1148-->

![修正済みの問題](../assets/fix.svg) カテゴリーページのキャッシュは、在庫量が変更され、製品がまだ在庫にある場合に無効化されなくなりました。 Adobe Commerceは、ストアフロントのカテゴリーページの商品数量（他の何も）が変更されたときにページを再生成するのではなく、キャッシュからページを読み込むようになりました。<!-- ACP2E-118-->

![修正された問題](../assets/fix.svg) **[!UICONTROL Display Out-Of-Stock Products]**&#x200B;設定が有効になっているシングルソースモードでインベントリを使用する場合、カテゴリーリストの製品数が正しくなりました。 Adobe Commerceは、商品の数を確認する際に販売可能かどうかを確認するようになりました。<!-- ACP2E-1033-->

![修正された問題](../assets/fix.svg)店舗内配達のカート価格ルールが、在庫が有効になっている場合に想定どおりに機能するようになりました。 以前は、カート価格ルールで生成された割引はこれらの条件では適用されませんでした。<!-- ACP2E-1015-->

![修正済みの問題](../assets/fix.svg)製品インベントリをスケジュール モードで更新すると、すべてのキャッシュがクリアされなくなりました。 以前は、インベントリ インデクサーはすべての設定キャッシュをクリアしていました。<!-- ACP2E-1003-->

![修正された問題](../assets/fix.svg)高度なインベントリの製品の&#x200B;**[!UICONTROL Allow Multiple Boxes for Shipping]**&#x200B;属性の値が期待どおりに保存されるようになりました。<!-- ACP2E-992-->

![修正済みの問題](../assets/fix.svg) Adobe Commerceは、実店舗での受け取りで注文した注文に対する部分的な払い戻しクレジットメモの後、正確な予約報酬を発行するようになりました。 以前は、管理者ユーザーが&#x200B;**[!UICONTROL Return to Stock]** チェックボックスを選択せずにクレジットメモを作成したときに、誤った予約が`inventory_reservation` テーブルに保存されていました。<!-- ACP2E-979-->

![修正済みの問題](../assets/fix.svg) Adobe Commerceでは、マルチソース在庫を実装するデプロイメントで、バリエーションの1つが手動で在庫に戻された場合、ストアフロントで設定可能な商品が在庫切れとして表示されなくなりました。<!-- ACP2E-952-->

![修正された問題](../assets/fix.svg)製品グリッドの列位置（**[!UICONTROL Catalog]** > **[!UICONTROL Products]**）が、複数のインベントリ ソースが設定されたデプロイメントでページが再読み込みされた後、以前の位置に戻らなくなりました。<!-- ACP2E-925-->

**[!UICONTROL Back to stock]** チェックボックスが選択されていない場合に、バーチャル製品に対してクレジットメモが発行された後、![修正された問題](../assets/fix.svg)在庫数量が正しくなりました。<!-- ACP2E-908-->

![修正済みの問題](../assets/fix.svg) デフォルト以外の在庫に割り当てられている商品の自動並べ替えとスコープを使用して、カテゴリを保存できるようになりました。 以前、Adobe Commerceはカテゴリを保存せず、次のエラーが表示されていました：`Something went wrong while saving the category`。<!-- ACP2E-859-->

![修正済みの問題](../assets/fix.svg)すべての在庫切れの設定可能なバリエーションを使用して製品を作成すると、設定可能な製品在庫ステータスが期待どおりに更新されるようになりました。<!-- ACP2E-813-->

![修正済みの問題](../assets/fix.svg)予約非一貫性アナライザーツールが、設定可能、バンドル、グループ化された製品を含む一部が出荷された注文で正しく機能するようになりました。 複合製品タイプが分析されるようになりました。 以前は、キャンセルと返金は親製品にのみ保存され、設定可能なバンドル製品や一緒に出荷するバンドル製品のサブプロダクト注文品目には保存されていませんでした。<!-- ACP2E-924-->

![修正済みの問題](../assets/fix.svg)管理者ユーザーが200以上の在庫ソースを在庫または商品に割り当てようとした場合、Adobe Commerceにエラーが表示されなくなりました。<!-- ACP2E-1180-->

![修正済みの問題](../assets/fix.svg) Adobe Commerceでは、商品が削除された注文に対するクレジットメモの作成がサポートされるようになりました。 以前は、請求書を作成した後に商品が注文から削除された場合、加盟店はクレジットメモを作成できませんでした。 アプリケーションで次のエラーが表示されました：`Following products with requested skus were not found: s00001`。 t. <!-- ACP2E-1138-->

![修正済みの問題](../assets/fix.svg) ストアが、単一のストア IDと複数のストア IDの両方に基づいてフィルタリングされるようになりました。 製品属性コード `event`が予約済み属性コードのリストに追加されました。 以前は、在庫モジュールのインストール時に低在庫報告書が例外をスローしていました。<!-- ACP2E-1017-->

![修正された問題](../assets/fix.svg)階層化されたナビゲーションフィルターが期待どおりに機能し、在庫切れの商品がストアフロントカテゴリの商品リストに追加されるようになりました。 新しい`is_out_of_stock`並べ替え属性は、ストアフロント製品コレクションにElasticsearch動的フィールドマッパーを使用します。<!-- ACP2E-748-->

![修正済みの問題](../assets/fix.svg)複合製品（バンドル、グループ化、設定可能）の在庫ステータスは、REST `POST /rest/V1/inventory/source-items`呼び出しによって子製品の在庫ステータスが変更されたときに、予想どおりに更新されます。<!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 （モジュールバージョン：`magento/inventory-metapackage = 1.2.5`）は、バージョン 2.4.5でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースのバージョン 2.4.0と互換性があります。

![修正済みの問題](../assets/fix.svg)販売者が管理者から出荷を作成すると、バンドルおよびグループ化された製品のデフォルトの在庫在庫状況が予想どおりに更新されるようになりました。 以前は、これらの製品のステータスは、出荷が作成された後も変更されませんでした。<!--- ACP2E-418-->

![修正済みの問題](../assets/fix.svg)次のいずれかの条件を満たした場合、設定可能な製品が再入荷されるようになりました：1。 親製品には、少なくとも1人の保存済みの子が在庫にあります。 2. 設定可能な製品自体が更新され、**在庫**&#x200B;として設定され、少なくとも1人の子が在庫を持っていました。<!--- ACP2E-443-->

![修正済みの問題](../assets/fix.svg) REST APIを通じて実装されたインベントリの変更が、製品詳細ページに期待どおりに反映されるようになりました。 カタログ製品のキャッシュは、最後と現在の在庫状況を比較した後にクリーニングされるようになりました。 以前は、コールバック機能を省略すると、在庫状況の変更が誤って評価され、必要なキャッシュクリーニングがトリガーされませんでした。 そのため、ストアフロントには在庫の変更が反映されていませんでした。<!--- ACP2E-161-->

![修正済みの問題](../assets/fix.svg)以前に在庫切れだったデフォルトの在庫に割り当てられた商品が、`/V1/inventory/source-items`を使用してソース商品を更新した後、ストアフロントに表示されるようになりました。 以前は、このREST API エンドポイントは間違った`stock_status`を設定していました。<!--- ACP2E-562-->

![修正済みの問題](../assets/fix.svg)一括アクション （**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**）を使用して在庫ソースの割り当てを解除すると、先頭のゼロを除く重複しているSKUがソースに含まれている場合に期待どおりに機能するようになりました（例：`01234`と`1234`）。 以前は、アプリケーションは在庫ソースの割り当てを解除せず、エラーをスローしていました。<!--- ACP2E-2641-->

無制限の取り寄せ注文が有効になっていて、商品が取り寄せ注文の数量に関係なくカスタム在庫に割り当てられている場合、ストアフロントで![問題](../assets/fix.svg)商品の在庫状況が常に&#x200B;**在庫**&#x200B;になりました。 以前は、再注文が可能な場合でも商品は在庫切れでした。<!--- ACP2E-664-->

![修正済みの問題](../assets/fix.svg) ソース項目が`POST /V1/inventory/source-items`で更新された後、設定可能な製品の親子製品在庫が正しく更新されるようになりました。 APIを通じて子商品が更新された後、デフォルトの在庫チェック用の新しい在庫プラグインが追加され、設定可能な商品数量とステータスが更新されます。<!--- ACP2E-442-->

![修正済みの問題](../assets/fix.svg)在庫切れのグループ化された商品は、ストアフロントカテゴリーページに表示されなくなりました。<!--- ACP2E-2082-->

![修正済みの問題](../assets/fix.svg) `CatalogInventory` `composer.json`のパッケージ名を修正しました。<!--- ACP2E-2914-->

![修正された問題](../assets/fix.svg)複数元/在庫展開で数量ゼロの製品を注文した後、管理画面にバックオーダーの状態が正しく表示されるようになりました。 [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![修正済みの問題](../assets/fix.svg) バンドル製品が「在庫」セクションから更新されると、ストアフロントカテゴリーページに在庫切れのバンドル製品が表示されなくなりました。<!--- ACP2E-2012-->

![修正済みの問題](../assets/fix.svg) PHP 7.4との互換性の問題が解決されました。<!--- AC-3192-->

![修正済みの問題](../assets/fix.svg)多数のオプション（複数の100）を含むバンドル製品を含む保存操作のパフォーマンスが向上しました。 以前は、これらの大きなバンドル製品を保存するのに数分かかり、在庫サービスを有効にしたデプロイメントでタイムアウトが発生することがありました。 [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![修正済みの問題](../assets/fix.svg)先頭の`0`を除くSKUが重複している場合に複数の製品に在庫ソースを割り当てるときに、製品の一括アクションツール（**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**）が期待どおりに機能するようになりました（例：`01234`と`1234`）。 以前は、在庫ソースに割り当てられた製品はひとつでした。 [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![修正された問題](../assets/fix.svg)在庫が0の場合、`ProductInterface.only_x_left_in_stock` フィールドが0を返すようになりました。 以前はnullが返されていました。 [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![修正済みの問題](../assets/fix.svg)管理者&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**&#x200B;からデフォルトのストックを編集できるようになりました。 以前は、デフォルトのストックにweb サイトを割り当てることができましたが、デフォルトのストックにソースを追加または削除しようとすると、コンソールにJavaScript エラーが表示されていました。<!--- ACP2E-545-->

![修正された問題](../assets/fix.svg) <!--- ACP2E-274--> **[!UICONTROL Display Out-Of-Stock Products]**&#x200B;設定が有効になっているインベントリのシングルソースモードを使用する場合、カテゴリーリストの製品数が正しくなりました。 新しいプラグインでは、`AreProductsSalableInterface`と`StockConfigurationInterface`を使用して、製品の合計数を決定するようになりました。 以前は、カテゴリ製品リストで誤った製品数量が返されていました。

![修正済みの問題](../assets/fix.svg) <!--- ACP2E-322-->設定可能な製品は、**[!UICONTROL Move out of stock to the bottom]**&#x200B;設定が有効になっているときに在庫が更新された後、製品リストの最後の位置に移動されるようになりました。 新しいカスタムデータベースクエリが実装され、Elasticsearch インデックスの並べ替え順序が無効になり、管理者対応の並べ替え順序が無視されます。 以前は、この設定が有効になっている場合、設定可能な製品とその子製品はリストの下部に移動されませんでした。

## v1.2.4

Inventory management 1.2.4 （モジュールバージョン：`magento/inventory-metapackage = 1.2.4`）は、バージョン 2.4.4でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースのバージョン 2.4.0と互換性があります。

![修正済みの問題](../assets/fix.svg) Commerceでは、すべての商品の販売可能な正確な数量の値が管理者商品リストビューに表示されるようになりました。 以前は、特殊文字を含むSKUを含む在庫商品の販売可能数量に対して、空白の値を表示していました。<!--- MC-41936-->

![修正済みの問題](../assets/fix.svg)多くの（約10,000）在庫ソースを使用したデプロイメントで、商品をカートに追加するなど、カートとチェックアウトのアクションのパフォーマンスが向上しました。<!--- MC-42570-->

![修正済みの問題](../assets/fix.svg) [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} データベースから予約が取り消され、キャッシュがクリアされた場合でも、`bin/magento inventory:reservation:list-inconsistencies` コマンドが部分的な出荷を伴う注文を正しく処理するようになりました。 以前、このコマンドが事前にクリアされたキャッシュで実行された場合、Commerceに次のエラーが表示されました：`Area code is not set`。<!--- MC-42142-->


![修正済みの問題](../assets/fix.svg) グループ化された製品の子製品の増分インデックス作成によって、子が共有されたときに他のグループ化された製品のインデックスが誤って作成されなくなりました。<!--- MC-41963-->

![修正された問題](../assets/fix.svg) ストアフロントのカテゴリーページに、カテゴリから製品をAPIで削除した後、正しい製品数が表示されるようになりました。 以前は、インデックス再作成が発生するまで、カテゴリーページの製品数が正しくありませんでした。<!--- MC-42287-->

![修正済みの問題](../assets/fix.svg)設定可能な製品は、**[!UICONTROL Manage Stock]** オプションが無効になっている場合に、クレジットメモを作成するときに在庫に戻せるようになりました。 以前は、このオプションが無効になっている場合、Commerceはクレジットメモ作成ページに「**在庫に戻る**」チェックボックスを表示しませんでした。<!--- MC-42002-->

![修正済みの問題](../assets/fix.svg) 10,000件を超える在庫在庫の管理が改善されました。 以前は、パフォーマンスの問題により、マーチャントがweb サイトを起動する前に管理画面で在庫を編集できないことがありました。<!--- MC-42643-->

![修正済みの問題](../assets/fix.svg)管理者の&#x200B;**[!UICONTROL User Roles]** ページが更新され、管理者に制限された権限を付与して、配信方法の設定にアクセスできるようになります。 _配送方法_ セクションの名前が&#x200B;_[!UICONTROL Delivery methods]_に変更され、_[!UICONTROL In-Store Pickup]_&#x200B;は&#x200B;_[!UICONTROL Delivery methods]_セクションの下に移動されました。 [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![修正済みの問題](../assets/fix.svg) Adobe Commerceでは、クレジットメモがAPIによって更新された後、重複した商品予約が作成されなくなりました。<!--- MC-41757-->

![修正された問題](../assets/fix.svg) チェックアウトワークフローの&#x200B;_[!UICONTROL Pick up in Store]_タブから_[!UICONTROL Shipping]_ タブに切り替えても、実店舗での受け取り配送のみが利用可能な場合に、JavaScript エラーがトリガーされなくなりました。<!--- MC-42808-->

![修正済みの問題](../assets/fix.svg)販売可能な製品数量と在庫のある製品数量が正しく同期されるようになりました。 以前は、キャンセルされた注文に対する在庫予約報酬は再作成されませんでした。<!--- MC-42485-->

![修正済みの問題](../assets/fix.svg) バリデーターのパフォーマンスが最適化され、出荷タイプ `Ship Together`のバンドル製品の子製品に新しいソースを追加できなくなります。<!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 （モジュールバージョン：`magento/inventory-metapackage = 1.2.3`）は、バージョン 2.4.3でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースのバージョン 2.4.0と互換性があります。

![修正済みの問題](../assets/fix.svg) フロントエンドでの複合製品の表示に関するいくつかの問題を修正しました。

![修正済みの問題](../assets/fix.svg)必要最小限の数量でカートページ管理のパフォーマンスを改善しました。

![修正済みの問題](../assets/fix.svg) ソースの作成、在庫切れアイテム、在庫のソーシング、割り当てられたソースの並べ替え、実店舗での配送、および在庫コマンドの問題を解決するために、いくつかの修正を行いました。

![修正済みの問題](../assets/fix.svg) [!DNL Commerce]は、店舗配達で3桁のカナダの郵便番号をサポートするようになりました。 `geonames.org`によって設定された制限により、6桁のコードはサポートされていません。

![修正済みの問題](../assets/fix.svg)管理者は、マルチストア展開の場合、**製品** グリッドと&#x200B;**製品の編集** ページに、無効な製品のデフォルトストックの正しい数量を表示できるようになりました。

![修正された問題](../assets/fix.svg) [!DNL Commerce]は、バンドル製品が再入荷したときに、カテゴリ製品キャッシュを更新するようになりました。

## 1.2.2

[!DNL Inventory Management] 1.2.2 （モジュールバージョン：`magento/inventory-metapackage = 1.2.2`）は、バージョン 2.4.2でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースのバージョン 2.4.0と互換性があります。

![修正済みの問題](../assets/fix.svg) フロントエンドでの複合製品の表示に関するいくつかの問題を修正しました。

![修正された問題](../assets/fix.svg) B2Bでの数量の更新中にカート ページのパフォーマンスが向上しました。

![修正済みの問題](../assets/fix.svg)実店舗での受け取り、一括更新、および在庫しきい値に関する問題を解決することを目的とした修正がいくつかあります。

![新規](../assets/new.svg) **機能テスト。** 新しい機能テストを導入し、既存のテストをより安定させるための修正を行いました。

## 1.2.1

[!DNL Inventory Management] 1.2.1 （モジュールバージョン：`magento/inventory-metapackage = 1.2.1`）は、バージョン 2.4.1でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースのバージョン 2.4.0と互換性があります。

![修正済みの問題](../assets/fix.svg) `inventory_cleanup_reservations` cron ジョブに関する既知の問題を修正し、バンドル製品のストア内ピックアップ機能に関する問題を修正しました。 このアップデートには、在庫計算、バンドル製品サポート、バックオーダー機能の一般的な改善も含まれています。

![新規](../assets/new.svg) **機能テスト。** 実店舗での受け取り機能に追加のカバレッジを提供するために、新機能テストを導入しました。

## 1.2.0

[!DNL Inventory Management] 1.2.0 （モジュールバージョン：`magento/inventory-metapackage = 1.2.0`）は、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Source コードベースのバージョン 2.4.0でサポートされています。

![修正された問題](../assets/fix.svg) ソース割り当て、スケーラブルな環境機能のサポート、PHP 7.4、MySQL 8、およびPHPUNIT 9との互換性に関する問題を解決するための多数の修正。

![新規](../assets/new.svg) **実店舗配達方法。** チェックアウト時に受け取り場所として使用するソースをユーザーが選択するオプションを追加しました。 _販売および購入エクスペリエンスガイド_&#x200B;の「[実店舗配送](../stores-purchase/shipping-in-store-delivery.md)」を参照してください。

![新規](../assets/new.svg) **マルチソースモードのバンドル製品サポート。** 在庫では、複数のソースを持つあらゆる商品タイプをサポートします。

![新規](../assets/new.svg) **非同期ストックのインデックス再作成。** 在庫を非同期でインデックス再作成する機能を追加し、いくつかの重要なシナリオのパフォーマンスを向上させました。

![新規](../assets/new.svg) **バルクインターフェイス。** 販売可能性チェック用の新しいバルクインターフェイスが導入されました：`\Magento\InventorySalesApi\Api\AreProductsSalableInterface`、`\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`。

![新規](../assets/new.svg) **テスト範囲が拡大しました。** 新しい機能は、検出された問題と修正された問題に対する拡張カバレッジを含む、自動化されたテストでカバーされています。

![既知の問題](../assets/bug.svg) **既知の問題。** 予約メタデータに`object_id` フィールドが存在しないため、`inventory_cleanup_reservations` cron ジョブが正常に動作していません。 この問題は、[magento/inventory#3046](https://github.com/magento/inventory/pull/3046)で導入されました。

**回避策：**&#x200B;次のMySQL クエリを実行して、予約を手動でクリーンアップします。

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 （モジュールバージョン：`inventory-composer-metapackage = 1.1.6`）は、バージョン 2.3.6でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Source コードベースのバージョン 2.3.5、2.3.4、2.3.3、2.3.3、2.3.2、2.3.1、および2.3.0と互換性があります。

![修正された問題](../assets/fix.svg)取り消し注文、クレジットメモ、低在庫レポートグリッド、「不整合を解決」 CLI ツールに接続された修正と一般的な改善に関する問題を解決するための修正。

![新規](../assets/new.svg) **非同期ストックのインデックス再作成。** 在庫を非同期でインデックス再作成する機能を追加し、いくつかの重要なシナリオのパフォーマンスを向上させました。

## 1.1.5

[!DNL Inventory Management] 1.1.5 （モジュールバージョン：`inventory-composer-metapackage = 1.1.5`）は、バージョン 2.3.5でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Source コードベースのバージョン 2.3.4、2.3.3、2.3.2、2.3.1、および2.3.0と互換性があります。

![新規](../assets/new.svg) **製品SKUが変更された後に在庫を更新します。** 新しい動作に切り替えるための新しい設定設定が導入されました。「カタログとの同期」

![新規](../assets/new.svg) **機能テスト。** 新しい機能テストを導入し、テスト範囲のギャップを解消。 テストをより安定して信頼性を高めるために、いくつかの問題を修正しました）。

![既知の問題](../assets/bug.svg)製品のオーバーセルを防ぐための修正、ストアフロントでの「在庫切れ」製品の表示、スケーラブルな環境サポートとユーザーインターフェイスの改善に関する多数の修正。

## 1.1.4

[!DNL Inventory Management] 1.1.4 （モジュールバージョン：`inventory-composer-metapackage = 1.1.4`）は、バージョン 2.3.4でサポートされており、バージョン 2.3.3、2.3.2、2.3.1、およびバージョン 2.3.0のAdobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Source コードベースと互換性があります。

![問題を修正&#x200B;](../assets/fix.svg)**パフォーマンスが向上しました。** Inventory Reservations CLI コマンドのバンチロジックを導入して、メモリ使用量を削減し、応答なしでプロセスが停止するケースを回避しました。

![新規&#x200B;](../assets/new.svg)**テスト範囲を拡大しました。** 多くの新機能テストを導入しました。 ほぼすべての手作業による在庫管理シナリオは、自動テストでカバーされています。

![既知の問題](../assets/bug.svg) クレジットメモ、グループ化された製品、ソースおよび在庫の大量アクションに関する問題を解決することを目的とした多数の修正。

## 1.1.3

[!DNL Inventory Management] 1.1.3 （モジュールバージョン：`inventory-composer-metapackage = 1.1.3`）は、バージョン 2.3.3でサポートされており、Adobe Commerce、Adobe Commerce on cloud infrastructure、およびMagento Open Source コードベースのバージョン 2.3.2、2.3.1、および2.3.0と互換性があります。

![修正された問題&#x200B;](../assets/fix.svg)**Adobe CommerceおよびB2B機能との統合の強化** [!DNL Inventory Management]は、デフォルト以外の在庫ソースと在庫を使用しているweb サイトで、次の機能で正しく機能するようになりました。

- SKUで注文（Adobe Commerce）
- クイックオーダー（B2B）
- リクエストリスト（B2B）

![新規&#x200B;](../assets/new.svg)**パフォーマンスが向上しました。** デフォルトの在庫在庫とソースを実行しているweb サイトでは、ストアフロントカタログの閲覧パフォーマンスが向上します。

![新規&#x200B;](../assets/new.svg)**テスト範囲を拡大しました。** 自動化された機能および統合テストのカバレッジが大幅に増加しました。

## 1.1.2

[!DNL Inventory Management] 1.1.2 （モジュールバージョン：`inventory-composer-metapackage = 1.1.2`）は、バージョン 2.3.2でサポートされており、バージョン 2.3.1およびバージョン 2.3.0のAdobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースと互換性があります。

![修正済みの問題](../assets/fix.svg)がGET `/V1/shipments` REST エンドポイントの応答に`source_code`を追加しました。<!-- https://github.com/magento/inventory/pull/2142 -->

![修正済みの問題](../assets/fix.svg)未出荷の注文に対するクレジットメモを発行した後、予約を正しくクリアし、製品数量を更新する問題を解決しました。 オプションを<!-- https://github.com/magento/inventory/pull/2179 -->に選択すると

![修正済みの問題](../assets/fix.svg)製品の作成中に数量を入力する際に、設定可能な製品の子の数量を正しく保存する問題を解決しました。<!-- https://github.com/magento/inventory/pull/2158 -->

[!DNL Inventory Management] 1.1.2 Betaの新しいモジュールは次のとおりです。

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![新規](../assets/new.svg) **一括部分株式転送エンドポイントを追加** – 現在の一括転送エンドポイントは、割り当てられたすべての数量をオリジンから宛先ソースに移動します。 新しい`/rest/V1/inventory/bulk-partial-source-transfer` エンドポイントを使用すると、販売者は一括操作としてソースからソースに部分的な在庫を転送できます。 特定の数量を転送するには、`sku`、`qty`、`origin_source_code`、`destination_source_code`のエンドポイントにリクエストを入力します。 転送では、ソースが`sku`に割り当てられていることや、転送に十分な量が存在することを確認します。 REST API ドキュメントの[ インベントリの一括アクション ](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"}を参照してください。<!-- https://github.com/magento/inventory/pull/2117 -->

![新規](../assets/new.svg) **予約CLI**&#x200B;が追加されました。新しいコマンドを使用すると、予約の不整合を検出して解決するオプションが表示されます。 注文が送信され、ステータスが変更されると、[!DNL Inventory Management]は報酬予約を通じて初期予約と更新を生成します。 これらのコマンドは、注文ID、SKU、Stock IDで検出された不整合のリストを返し、解決する予約を作成します。 詳しくは、[CLI リファレンス ](cli.md)を参照してください。<!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![新規](../assets/new.svg) **ソースとSSA オプションのパフォーマンスが向上しました** – 出荷時にソースを並べ替えて選択すると、ソースの数が多い在庫のパフォーマンスが低下しました。 このリリースでは、出荷時にSSA オプションを確認および選択する際に、使用可能なソースのリストと並べ替えを行う際のパフォーマンスが大幅に改善されました。<!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![新規](../assets/new.svg) **Inventory management**&#x200B;のGraphQL サポートを追加しました。このリリースでは、新しい`magento/module-inventory-graph-ql` モジュールがインストールされます。 GraphQL [ProductInterface属性](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"}に、[!DNL Inventory Management]のサポート用の`only_x_left_in_stock`属性と`stock_status`属性が含まれるようになりました。<!-- https://github.com/magento/inventory/pull/2124 -->

![新規](../assets/new.svg) **割り当て済みソースの簡易UI** – 製品ページの「割り当て済みソース」テーブルで、コンテンツが簡素化され、多くのソースを表示する際の更新が簡単になり、パフォーマンスが向上しました。 すべてのソースがソース名で一覧表示されます（`source_code`にカーソルを合わせます）。

![新規](../assets/new.svg) **集約ストックサービスの書き出し** – このリリースでは、Amazon、eBay、Google Shopping adsなどの外部セールスチャネルをサポートする新しい集約ストックサービス（システム内の予約を保持）が提供されます。 <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 （モジュールバージョン：`inventory-composer-metapackage = 1.1.0`）は、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースのバージョン 2.3.0とサポートされ、互換性があります。[!DNL Inventory Management] 1.1.1は、パッケージ名の更新プログラムとしてのみリリースされ、バージョン 2.3.1でサポートされ、Adobe Commerce、Adobe Commerce on cloud infrastructure、Magento Open Source コードベースのバージョン 2.3.0と互換性があります。

![修正済みの問題](../assets/fix.svg) **シングルソースモードとマルチソースモードに対するElasticsearchのサポートが追加されました** — Elasticsearchをカスタム素材で設定して使用できるようになりました。 インストールについて詳しくは、[Elasticsearch サービスの設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"}を参照してください。<!-- PR https://github.com/magento/inventory/pull/1943 -->

![修正済みの問題](../assets/fix.svg) Default Stockのパフォーマンスの問題を解決し、多数の操作でパフォーマンスを大幅に向上させました。 シングルソースモード、在庫のSourceへの転送、ストアフロントカテゴリページ、および販売可能数量の計算のパフォーマンスが向上しました。

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![修正済みの問題](../assets/fix.svg)構成可能な製品とグループ化された製品の在庫切れステータスと一括在庫転送に関する問題を解決しました。 親製品を選択して一括アクションを実行しても、製品ステータスには影響しません。 親商品が「在庫」の場合は、「在庫」のままです。

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![新規](../assets/new.svg) **Distance Priority Algorithm** – 距離優先アルゴリズムは、距離ベースの配送レコメンデーション用の新しい、すぐに使用できるSource Selection Algorithmです。 このアルゴリズムは、配送先の住所の場所と配送元の場所を比較し、出荷を処理するのに最も近い配送元を決定します。 距離は、読み込まれたジオコードの位置情報またはGoogleの方向（運転、歩行、または自転車）を使用して、物理的な距離または別の場所から別の場所に移動した時間によって決まります。

![新規](../assets/new.svg) **ソース数量リストを拡張** — ソース数が多いマーチャントは、製品グリッドを通じて、製品ごとに簡単にホバーして全ソースを表示できます。 各製品には、最低5つのソースと一致する数量が表示されます。 ソースにカーソルを合わせると、ソースと現在の数量のリスト全体をスクロールできます。

![既知の問題](../assets/bug.svg) Magento Open SourceとAdobe Commerce v2.3.1の既知の問題 – ソース間のデータの非同期マイグレーションで、PHP クラスとメソッド名を反映するトピック名を持つ非同期APIが変更されたために問題が発生します。 同期操作を使用して、**[!UICONTROL Run asynchronously]**&#x200B;を`No`に設定することをお勧めします。
