---
title: "インストール、更新、削除 [!DNL Inventory Management]"
description: を管理する方法を学ぶ [!DNL Inventory Management] メタパッケージ。
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
source-git-commit: d6c81da4b4e0674d6699e9781921ccb2160b9983
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# インストール、更新、削除 [!DNL Inventory Management]

[!DNL Inventory Management] モジュールは、単一ソースおよび複数ソースのマーチャントが販売チャネルの製品数と在庫を管理するためのすべてのインベントリ機能とオプションを提供します。 これらの機能は、Adobe CommerceとMagento Open Sourceの 2.4.x リリースで使用できます。

これらの機能と拡張機能は、 [在庫プロジェクト](https://github.com/magento/inventory) コミュニティエンジニアリングMagento Open Sourceを通じて。

[!DNL Inventory Management] は、Adobe CommerceおよびMagento Open Sourceの 2.3.x および 2.4.x リリースでインストールされ、すべての機能がデフォルトで有効になっています。 これらのインベントリ機能を有効にするための追加の手順は必要ありません。 v2.1.x または 2.2.x からのアップグレードには、追加の手順が必要な場合があります。 詳しくは、 [Inventory managementをアップグレード](#upgrade-inventory-management).

次に従ったインストール [オンプレミスでの迅速なインストールを開始](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} をお勧めします。 すべてを受け取るには、メタパッケージと共にインストールします [!DNL Inventory Management] モジュール。

次の行は `composer.json` メタパッケージインストール [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

のリスト [!DNL Inventory Management] メタパッケージのバージョンについては、 [リリースノート](release-notes.md).

The [!DNL Inventory Management] インストールプロセスは、すべてのモジュールを `<Magento_installation_directory>/app/etc/config.php` ファイル。 A `1` 値は、対応するモジュールが有効であることを示します。 次のモジュールのリストが追加されます。

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

## 有効にする [!DNL Inventory Management] 機能

インストール、アップグレード、更新時に、 _[!UICONTROL Manage Stock]_」オプションがデフォルトで有効になっています。 このオプションは、在庫の追跡と管理を有効にしますが、モジュールのステータスには影響しません。 モジュールを無効にするには、次の節を参照してください。

設定について詳しくは、 [Inventory managementの設定](configuration.md).

## Inventory managementを無効にする

>[!IMPORTANT]
>
>デフォルトの [!DNL Inventory Management] モジュールを強くお勧めします。 代替案 [!DNL CatalogInventory] 無効なシステムに使用するモジュール [!DNL Inventory Management] モジュールは非推奨（廃止予定）となりました。 の無効化 [!DNL Inventory Management] モジュールは、システムの不安定な原因となり、様々な問題が発生する可能性があります。

以下を無効にする必要があります： [!DNL Inventory Management] モジュール：

* 2.0.x、2.1.x、2.2.x、2.3.x から 2.4.x へのマーチャントのアップグレードプロセスを迅速化します。
* カスタムまたはサードパーティの在庫および注文管理システムモジュールを使用します。

詳しくは、 [モジュールの有効化または無効化](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) ページの _インストールガイド_ を参照してください。

完了すると、システムは、 `<Magento_installation_directory>/app/etc/config.php`、次で始まる：

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>OMS コネクタモジュールがインストールされている場合は、 `Magento_InventoryMessageBus` モジュール。コネクタモジュールです。 OMS でコネクタを使用する必要があります。

## Inventory managementを削除

>[!IMPORTANT]
>
>デフォルトの [!DNL Inventory Management] モジュールを強くお勧めします。 代替案 [!DNL CatalogInventory] 削除されたシステムに使用されるモジュール [!DNL Inventory Management] モジュールは非推奨（廃止予定）となりました。 の削除 [!DNL Inventory Management] モジュールは、システムの不安定な原因となり、様々な問題が発生する可能性があります。

を使用しない場合、 [!DNL Inventory Management] の機能を使用して、これらのモジュールを削除（アンインストール）できます。 コンポーザーファイルを通じてすべてのモジュールを削除するには、以下をに追加します。 `composer.json`:

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

この変更が完了したら、composer install を実行し、これらのInventory managementモジュールを自動的に削除します。

## Inventory managementをアップグレード

### 前へ [!DNL Commerce] versions

既存の 2.1.x、2.2.x、2.3.x のインストールをAdobe CommerceまたはMagento Open Source2.4.x にアップグレードまたは更新する場合 [!DNL Inventory Management] モジュールはデフォルトで無効になっています。 このデフォルト設定は、後方互換性のないアップグレードを防ぎ、Order Management(OMS) をより適切にサポートするための予防措置です。

>[!NOTE]
>
>Order Management はをサポートしていません [!DNL Inventory Management]. アップグレード時に、 [!DNL Inventory Management] OMS と [!DNL Commerce] 2.3.x でシームレスに動作。


有効にするには [!DNL Inventory Management] モジュール：

1. を編集します。 `<Commerce_installation_directory>/app/etc/config.php` ファイル。
1. すべての在庫モジュールを次の場所から変更： `0` から `1` を有効にします。
1. データベースを更新します。

   ```bash
   bin/magento setup:upgrade
   ```

1. キャッシュをクリーンアップします。

   ```bash
   bin/magento cache:clean
   ```

次を使用することをお勧めします。 [予約不整合コマンド](cli.md) アップグレード後 アップグレード時に、すべての製品がデフォルトの在庫に追加されます。 保留中の注文がある場合、コマンドは、販売および注文の受け渡しに対する販売可能数量と予約を正しく更新します。

### 前へ [!DNL Inventory Management] versions

の以前のリリースからアップグレードする場合 [!DNL Inventory Management] を最新バージョンにするには、通常の拡張機能のアップグレード手順に従います。

最新のバージョンについては、メタパッケージのバージョンを更新してください。

```json
        magento/inventory-composer-metapackage = 1.1.3
```

コマースのアップグレードについて詳しくは、次のガイドを参照してください。

* [Commerce 更新ガイド](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [モジュールの有効化または無効化](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
