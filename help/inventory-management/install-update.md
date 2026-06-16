---
title: ' [!DNL Inventory Management]のインストール、更新、削除'
description: ' [!DNL Inventory Management]  メタパッケージの管理方法について説明します。'
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/-koENBfshZ7WkXih0dee4geUb2Mnx-mtTxUxt-s6yUo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 683
ht-degree: 0%

---

# [!DNL Inventory Management]のインストール、更新、削除

[!DNL Inventory Management]個のモジュールは、販売店の商品の数量と在庫を管理するために、単一およびマルチソースの販売店のすべての在庫機能とオプションを提供します。 これらの機能は、Adobe CommerceおよびMagento Open Sourceの2.4.x リリースで使用できます。

これらの機能と拡張機能は、Magento Open Source コミュニティエンジニアリングプログラムを通じて[Inventory プロジェクト &#x200B;](https://github.com/magento/inventory)の一部として開発されました。

[!DNL Inventory Management]は、Adobe CommerceおよびMagento Open Sourceの2.3.xおよび2.4.x リリースにインストールされ、すべての機能がデフォルトで有効になっています。 これらのインベントリ機能を有効にするための追加ステップは必要ありません。 v2.1.xまたは2.2.xからのアップグレードには、追加の手順が必要になる場合があります。 [Inventory managementのアップグレード &#x200B;](#upgrade-inventory-management)を参照してください。

[&#x200B; クイックスタートオンプレミスのインストール &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=ja){target="_blank"}に従ったインストールをお勧めします。 すべての[!DNL Inventory Management] モジュールを受け取るには、メタパッケージをインストールしてください。

`composer.json` メタパッケージの次の行は、[!DNL Inventory Management]をインストールします。

```json
        magento/inventory-composer-metapackage = 1.1.3
```

[!DNL Inventory Management]個のメタパッケージのバージョンの一覧については、[&#x200B; リリースノート &#x200B;](release-notes.md)を参照してください。

[!DNL Inventory Management]のインストール プロセスでは、すべてのモジュールが`<Magento_installation_directory>/app/etc/config.php` ファイルに追加されます。 `1`値は、対応するモジュールが有効であることを示します。 次のモジュールのリストが追加されます。

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

## [!DNL Inventory Management]機能を有効にする

インストール、アップグレード、または更新すると、管理者の&#x200B;_[!UICONTROL Manage Stock]_&#x200B;オプションがデフォルトで有効になります。 このオプションは、在庫の追跡と管理を有効にしますが、モジュールのステータスには影響しません。 モジュールを無効にするには、次の節を参照してください。

設定について詳しくは、[Inventory managementの設定](configuration.md)を参照してください。

## Inventory managementを無効にする

>[!IMPORTANT]
>
>既定の[!DNL Inventory Management] モジュールを使用することを強くお勧めします。 無効な[!DNL Inventory Management] モジュールを持つシステムに使用される代替[!DNL CatalogInventory] モジュールは非推奨（廃止予定）になりました。 [!DNL Inventory Management] モジュールを無効にすると、システムが不安定になり、様々な問題が発生する可能性があります。

[!DNL Inventory Management] モジュールを無効にして、次の操作を行うことができます。

* 2.0.x、2.1.x、2.2.x、または2.3.xから2.4.xに移行するマーチャントのアップグレードプロセスを高速化します。
* カスタムまたはサードパーティの在庫管理および注文管理システムモジュールを使用します。

該当するモジュールを無効にする方法について詳しくは、_インストールガイド_&#x200B;の「[&#x200B; モジュールを有効または無効にする](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=ja)」ページを参照してください。

完了すると、次で始まる`<Magento_installation_directory>/app/etc/config.php`のモジュールと値のリストが表示されます。

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>OMS Connector モジュールがインストールされている場合は、Connector モジュールである`Magento_InventoryMessageBus` モジュールを無効にしないでください。 OMSでコネクタを使用する必要があります。

## Inventory managementを削除

>[!IMPORTANT]
>
>既定の[!DNL Inventory Management] モジュールを使用することを強くお勧めします。 削除された[!DNL Inventory Management] モジュールを含むシステムに使用される代替[!DNL CatalogInventory] モジュールは非推奨（廃止予定）になりました。 [!DNL Inventory Management] モジュールを削除すると、システムが不安定になり、様々な問題が発生する可能性があります。

[!DNL Inventory Management]機能を使用しない場合は、これらのモジュールを削除（アンインストール）できます。 コンポーザーのファイルを使用してすべてのモジュールを削除するには、次を`composer.json`に追加します。

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

この変更が完了したら、composer installを実行すると、これらのInventory management モジュールが自動的に削除されます。

## Inventory managementのアップグレード

### 以前の[!DNL Commerce] バージョン

既存の2.1.x、2.2.x、または2.3.x インストールをAdobe CommerceまたはMagento Open Source 2.4.xにアップグレードまたはアップデートする場合、デフォルトで[!DNL Inventory Management] モジュールは無効になります。 このデフォルト設定は、後方互換性のないアップグレードを防ぎ、Order Management（OMS）をより適切にサポートするための予防策です。

>[!NOTE]
>
>Order Managementは[!DNL Inventory Management]をサポートしていません。 アップグレード時に、[!DNL Inventory Management] モジュールは無効になり、OMSと[!DNL Commerce] 2.3.xがシームレスに動作するようになります。


[!DNL Inventory Management] モジュールを有効にするには：

1. `<Commerce_installation_directory>/app/etc/config.php` ファイルを編集します。
1. `0`から`1`までのすべての在庫モジュールを変更して有効にします。
1. データベースを更新します。

   ```bash
   bin/magento setup:upgrade
   ```

1. キャッシュをクリーニングします。

   ```bash
   bin/magento cache:clean
   ```

アップグレード後は、[予約不整合コマンド &#x200B;](cli.md)を使用することをお勧めします。 アップグレード時には、すべての製品がデフォルトのStockに追加されます。 保留中の注文がある場合、コマンドは販売可能な数量と販売注文と注文フルフィルメントの予約を正しく更新します。

### 以前の[!DNL Inventory Management] バージョン

以前のリリースの[!DNL Inventory Management]から最新バージョンにアップグレードする場合は、通常の拡張機能のアップグレード手順に従います。

最新の場合は、メタパッケージのバージョンを更新します。

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Commerceのアップグレードについて詳しくは、次のガイドを参照してください。

* [Commerce アップデートガイド](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html?lang=ja){target="_blank"}
* [モジュールを有効または無効にする](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=ja){target="_blank"}
