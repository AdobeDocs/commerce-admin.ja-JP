---
title: '"インストール、更新、削除 [!DNL Inventory Management]“'
description: の管理方法について説明します [!DNL Inventory Management] メタパッケージ。
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
source-git-commit: d6c81da4b4e0674d6699e9781921ccb2160b9983
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# インストール、更新、削除 [!DNL Inventory Management]

[!DNL Inventory Management] モジュールは、単一ソースおよび複数ソースのマーチャント向けのすべての在庫機能とオプションを提供し、販売チャネル向けの製品数量と在庫を管理します。 これらの機能は、Adobe CommerceおよびMagento Open Sourceの 2.4.x リリースで使用できます。

これらの機能と拡張機能は、 [在庫プロジェクト](https://github.com/magento/inventory) Magento Open Sourceコミュニティエンジニアリングプログラムを通じて。

[!DNL Inventory Management] は 2.3.x および 2.4.x リリースのAdobe CommerceおよびMagento Open Sourceにインストールされます。すべての機能がデフォルトで有効になっています。 これらのインベントリ機能を有効にするために必要な追加手順はありません。 v2.1.x または 2.2.x からのアップグレードでは、追加の手順が必要になる場合があります。 参照： [Inventory managementのアップグレード](#upgrade-inventory-management).

によるインストール [オンプレミスでのクイックスタートのインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} 推奨されます。 すべてのものを受け取るためにメタパッケージでインストール [!DNL Inventory Management] モジュール。

次の行 `composer.json` metapackage インストール [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

のリスト用 [!DNL Inventory Management] メタパッケージのバージョンについては、 [リリースノート](release-notes.md).

この [!DNL Inventory Management] インストールプロセスは、すべてのモジュールをに追加します。 `<Magento_installation_directory>/app/etc/config.php` ファイル。 A `1` 値は、対応するモジュールが有効であることを示します。 次のモジュールのリストが追加されました。

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## Enable （有効） [!DNL Inventory Management] の機能

インストール、アップグレード、更新の際に、 _[!UICONTROL Manage Stock]_管理者のオプションは、デフォルトで有効になっています。 このオプションを使用すると、在庫の追跡と管理が可能になりますが、モジュールのステータスには影響しません。 モジュールを無効にするには、次の節を参照してください。

設定について詳しくは、を参照してください。 [Inventory managementの設定](configuration.md).

## Inventory managementを無効にする

>[!IMPORTANT]
>
>デフォルトの使用 [!DNL Inventory Management] モジュールを使用することを強くお勧めします。 代替手段 [!DNL CatalogInventory] モジュール（無効になっているシステムに使用） [!DNL Inventory Management] モジュールは、非推奨（廃止予定）になりました。 の無効化 [!DNL Inventory Management] モジュールはシステムを不安定にし、様々な問題を引き起こす可能性があります。

無効にすることができます [!DNL Inventory Management] モジュールの目的：

* 2.0.x、2.1.x、2.2.x、または 2.3.x から 2.4.x に移行するマーチャントのアップグレードプロセスを迅速化します。
* カスタムまたはサードパーティの在庫および受注管理システム・モジュールを使用します。

を参照してください。 [モジュールの有効化または無効化](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) 内のページ _インストールガイド_ 該当するモジュールを無効にする方法については、を参照してください。

完了すると、次の場所にモジュールと値のリストが表示されます `<Magento_installation_directory>/app/etc/config.php`で始まる。

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>OMS コネクタモジュールがインストールされている場合は、を無効にしないでください `Magento_InventoryMessageBus` モジュール（コネクタモジュール）。 OMS でコネクタを使用する必要があります。

## Inventory managementを削除

>[!IMPORTANT]
>
>デフォルトの使用 [!DNL Inventory Management] モジュールを使用することを強くお勧めします。 代替手段 [!DNL CatalogInventory] モジュール（削除されたシステムに使用されます） [!DNL Inventory Management] モジュールは、非推奨（廃止予定）になりました。 削除， [!DNL Inventory Management] モジュールはシステムを不安定にし、様々な問題を引き起こす可能性があります。

を使用しないことを選択した場合 [!DNL Inventory Management] 機能を使用すると、これらのモジュールを削除（アンインストール）できます。 composer ファイルを使用してすべてのモジュールを削除するには、次のコマンドをに追加します。 `composer.json`:

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

この変更が完了したら、composer のインストールを実行すると、これらのInventory management モジュールが自動的に削除されます。

## Inventory managementのアップグレード

### 前へ [!DNL Commerce] バージョン

Adobe CommerceまたはMagento Open Source 2.4.x に既存の 2.1.x、2.2.x または 2.3.x をアップグレードまたはアップデートする場合 [!DNL Inventory Management] モジュールはデフォルトで無効になっています。 このデフォルト設定は、後方互換性のないアップグレードを防ぎ、Order Management （OMS）をより適切にサポートするための予防策です。

>[!NOTE]
>
>Order Management はサポートしていません [!DNL Inventory Management]. アップグレード時、 [!DNL Inventory Management] oms および OMS を許可するモジュールは無効です。 [!DNL Commerce] 2.3.x でシームレスに動作


を有効にする [!DNL Inventory Management] モジュール：

1. を編集する `<Commerce_installation_directory>/app/etc/config.php` ファイル。
1. すべての在庫モジュールの変更元 `0` 対象： `1` を有効にします。
1. データベースを更新します。

   ```bash
   bin/magento setup:upgrade
   ```

1. キャッシュのクリーンアップ：

   ```bash
   bin/magento cache:clean
   ```

を使用することをお勧めします [予約の不整合コマンド](cli.md) アップグレード後。 アップグレードすると、すべての製品がデフォルトの在庫に追加されます。 保留中の受注がある場合、受注および受注の履行に対する販売可能数量および予約が正しく更新されます。

### 前へ [!DNL Inventory Management] バージョン

の以前のリリースからアップグレードする場合 [!DNL Inventory Management] 最新バージョンには、通常の拡張機能アップグレード手順に従います。

最新のメタパッケージのバージョンを更新してください。

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Commerceのアップグレードについて詳しくは、次のガイドを参照してください。

* [Commerce アップデートガイド](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [モジュールの有効化または無効化](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
