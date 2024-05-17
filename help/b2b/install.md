---
title: のインストール [!DNL B2B for Adobe Commerce] 拡張子
description: のインストール方法を説明します [!DNL B2B for Adobe Commerce] メタパッケージ。
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: e57aa4e8919c2de5341c4b8363197d6380bbb0f6
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---


# のインストール [!DNL B2B for Adobe Commerce] 拡張子

B2B for Adobe Commerce拡張機能は、Adobe Commerce v2.2.0 以降でのみ使用できます。 Adobe Commerceのインストール後にインストールされます。

デプロイされたAdobe Commerceバージョンでサポートされている最新バージョンの B2B 拡張機能をインストールします。

>[!NOTE]
>
>これらのインストール手順は、オンプレミスにデプロイされたAdobe Commerceに適用されます。 クラウドインフラストラクチャにデプロイされたCommerce プロジェクト用の B2B 拡張機能をインストールするには、以下を参照してください [Commerce Cloudインフラストラクチャガイド](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## 要件

- Adobe Commerce バージョン 2.3.x 以降
- [B2B 拡張機能のサポートされているバージョン](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- 有効 [認証キー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) Adobe Commerce Extensions をダウンロードします。

  で認証キーをグローバルに定義して、インストール用に保存します。 [COMPOSER_ホーム](https://getcomposer.org/doc/03-cli.md#composer-home) ディレクトリ。 または、に保存します [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) ファイル（Adobe Commerce アプリケーションのルートディレクトリ内）。

B2B 拡張機能をインストールまたはアップグレードする前に、リリースノートを参照して、インストールまたはアップグレードの要件に影響を与える可能性のあるバージョンの互換性、更新、変更に関する最新情報を確認してください。

- [B2B リリースノート](release-notes.md)
- [Adobe Commerce リリースノート](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## インストール手順

1. Adobe Commerce アプリケーションのルートディレクトリから、を更新します `composer.json` b2B 拡張機能の依存関係を追加するには：

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   エラーが発生した場合、例えば次のようになります。

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   パッケージのスペル、バージョンの制約、パッケージが使用可能で、最小安定性（安定）の要件に一致していることを確認します。

1. プロンプトが表示されたら、 [認証キー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   あなたの _公開鍵_ はユーザー名、は _秘密鍵_ はパスワードです。 公開鍵と秘密鍵をに保存している場合は、次の手順を実行します `auth.json`の場合、認証を求めるプロンプトは表示されません。

1. Composer がモジュールの更新を完了した後で、次のコマンドを実行します。

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >実稼動モードでは、に対するメッセージを受信する場合があります。 `Please rerun Magento compile command`. コマンドを入力して、インストールを完了します。 Adobe Commerceでは、開発者モードでコンパイルコマンドを実行するように求められることはありません。

インストールが完了したら、メッセージコンシューマーを設定して開始します。以下が含まれます [メッセージコンシューマーのパラメーターの指定](#configure-message-consumers).

## メッセージコンシューマー

Adobe Commerce用 B2B 拡張機能は、メッセージキューの管理に MySQL を使用します。 次の表に、B2B 機能をサポートするメッセージコンシューマーを示します。 拡張機能をインストールしたら、Commerce ストアフロントに必要な B2B 機能について、メッセージコンシューマーを開始します。

| 消費者 | 説明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 共有カタログ内の各製品の価格を更新します。 次の場合に必須： [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 管理システムの設定で、オプションが有効になっている。 |
| `sharedCatalogUpdateCategoryPermissions` | 共有カタログ カテゴリに割り当てられているカテゴリを更新します。 次の場合に必須： [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 管理システムの設定で、オプションが有効になっている。 |
| `negotiableQuotePriceUpdate` | 交渉可能な見積の価格を更新します。 次の場合に必須： [**[!UICONTROL Quotes]**](quotes.md) 管理システムの設定で、オプションが有効になっている。 |
| `purchaseorder.toorder` | 発注書を注文に変換します。 次の場合に必須： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 管理システムの設定で、オプションが有効になっている。 |
| `purchaseorder.transactional.email` | 発注書 E メールを送信します。 次の場合に必須： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 管理システムの設定で、オプションが有効になっている。 |
| `purchaseorder.validation` | 関連する発注を検証します。 [承認ルール](account-dashboard-approval-rules.md). 次の場合に必須： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 管理システムの設定で、オプションが有効になっている。 |
| `quoteItemCleaner` | 商品がカタログから削除された場合、または買い物かごから削除された場合に、無効または非アクティブな価格見積を削除します。 次の場合に必須： [**[!UICONTROL Quotes]**](quotes.md) 管理システムの設定で、オプションが有効になっている。 |
| `inventoryQtyCounter` | 注文または製品の削除後に、在庫インデックスを非同期で修正します。 次の場合に必須： [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) 「」オプションが、Admin Configuration Settings のInventory managementに対して有効になっている。 参照： [パフォーマンスのベストプラクティス](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | の個々のタスクごとにメッセージを作成します [一括操作](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)品目のインポートまたはエクスポート、一括スケールでの価格の変更、倉庫への製品の割当てなど。 次の場合に必須： [**管理の一括操作**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) オプション [!DNL Inventory Management] はに設定されています。 **非同期で実行** 管理システムの設定で行います。 |

{style="table-layout:auto"}

>[!NOTE]
>
>すべてのAdobe Commerce メッセージコンシューマーのリストについては、以下を参照してください [メッセージキューコンシューマー](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) が含まれる _設定ガイド_.

### メッセージコンシューマーの設定

次のパラメーターを追加して、発生する可能性のある処理の問題や遅延を防ぎます [メッセージコンシューマーの開始](#start-message-consumers) （B2B 機能用）。

- `--max-messages <value>` – 各消費者が終了するまでに処理する必要があるメッセージの最大数を指定します（デフォルトは 10000）。 推奨はしませんが、0 を使用して消費者が終了するのを防ぐことができます。 PHP アプリケーションのベストプラクティスは、長時間実行されているプロセスを再起動して、メモリリークの可能性を防ぐことです。

- `--batch-size <value>`- コンシューマーが消費するシステムリソース （CPU、メモリ）を制限できます。 より小さなバッチを使用すると、リソースの使用量が減少します。その結果、処理が遅くなります。  指定した場合、キュー内のメッセージが次のバッチで消費されます `<value>` 各。 このオプションは、バッチコンシューマーにのみ適用できます。 次の場合 `--batch-size` が定義されていない場合、バッチコンシューマーはキュー内の使用可能なすべてのメッセージを受け取ります。

その他の設定オプションについては、を参照してください。 [特定の設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### メッセージコンシューマーの開始

B2B 機能の非同期操作を有効にするには、複数のメッセージコンシューマーを開始する必要があります。

1. 使用可能なメッセージコンシューマーのリストを表示します。

   ```bash
   bin/magento queue:consumers:list
   ```

   このコマンドは、使用可能なメッセージコンシューマー（すべてを含む）を返します [B2B メッセージコンシューマー](#message-consumers).

1. 各消費者を個別に起動します。

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   例：

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>バックグラウンドで実行するには、次を追加します `&` コマンドを実行するには、プロンプトに戻り、コマンドの実行を続行します。 例： `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

詳しくは、を参照してください [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) が含まれる _設定ガイド_.

### Cron へのメッセージコンシューマーの追加

の実行スケジュールを自動化することもできます `SharedCatalogUpdateCategoryPermissions` および `SharedCatalogUpdatePrice` cron 設定ファイルにスケジュールを追加してメッセージコンシューマーに送信 [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

また、からメッセージコンシューマーのスケジュールを設定することもできます [ストアの設定](../systems/cron.md) admin.

## 管理者で B2B 機能を有効にする

B2B for Adobe Commerce拡張機能をインストールしてメッセージコンシューマーを開始した後、次の手順も実行する必要があります [管理者で B2B 機能を有効にする](enable-basic-features.md).
