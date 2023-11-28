---
title: をインストールします。 [!DNL B2B for Adobe Commerce] 拡張
description: をインストールする方法を説明します。 [!DNL B2B for Adobe Commerce] メタパッケージ。
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: e57aa4e8919c2de5341c4b8363197d6380bbb0f6
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 0%

---


# をインストールします。 [!DNL B2B for Adobe Commerce] 拡張

Adobe Commerce拡張機能の B2B は、Adobe Commerce v2.2.0 以降でのみ使用できます。 Adobe Commerceのインストール後にインストールされます。

デプロイ済みのAdobe Commerceバージョンでサポートされている B2B 拡張機能の最新バージョンをインストールします。

>[!NOTE]
>
>これらのインストール手順は、オンプレミスにデプロイされたAdobe Commerceに適用されます。 クラウドインフラストラクチャにデプロイされたコマースプロジェクト用の B2B 拡張機能をインストールするには、 [Commerce Cloudインフラストラクチャガイド](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## 要件

- Adobe Commerceバージョン 2.3.x 以降
- [B2B 拡張機能のサポートされているバージョン](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- 有効 [認証キー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) をクリックして、Adobe Commerce拡張機能をダウンロードします。

  認証キーをインストール用に保存するには、認証キーを [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) ディレクトリ。 または、 [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) ファイルをAdobe Commerceアプリケーションのルートディレクトリに配置します。

B2B 拡張機能をインストールまたはアップグレードする前に、リリースノートを調べて、インストールまたはアップグレードの要件に影響を与える可能性のあるバージョンの互換性、更新、変更に関する最新情報を確認してください。

- [B2B リリースノート](release-notes.md)
- [Adobe Commerceリリースノート](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## インストール手順

1. Adobe Commerceアプリケーションのルートディレクトリで、 `composer.json` B2B 拡張機能の依存関係を追加するには、次の手順を実行します。

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   次のようなエラーが発生した場合：

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   パッケージのスペル、バージョンの制約、およびパッケージが使用可能で、最小安定性（安定性）要件に一致していることを確認します。

1. プロンプトが表示されたら、 [認証キー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   お使いの _公開鍵_ はユーザー名です。 _秘密鍵_ はお客様のパスワードです。 公開鍵と秘密鍵を `auth.json`認証を求めるメッセージは表示されません。

1. Composer がモジュールの更新を完了したら、次のコマンドを実行します。

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
   >実稼動モードでは、次の宛てのメッセージを受け取る場合があります。 `Please rerun Magento compile command`. コマンドを入力して、インストールを完了します。 Adobe Commerceでは、開発者モードでコンパイルコマンドを実行するように求められません。

インストールが完了したら、次を含むメッセージコンシューマーを設定して開始します。 [メッセージコンシューマー用のパラメーターの指定](#configure-message-consumers).

## メッセージ消費者

B2B for Adobe Commerce拡張機能は、メッセージキュー管理に MySQL を使用します。 次の表に、B2B 機能をサポートするメッセージコンシューマーを示します。 拡張機能をインストールしたら、コマースストアフロントに必要な B2B 機能に関するメッセージコンシューマーを起動します。

| 消費者 | 説明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 共有カタログ内の各製品の価格を更新します。 必須 [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) オプションが有効になっている場合は、管理システム設定で有効になります。 |
| `sharedCatalogUpdateCategoryPermissions` | 共有カタログカテゴリに割り当てられたカテゴリを更新します。 必須 [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) オプションが有効になっている場合は、管理システム設定で有効になります。 |
| `negotiableQuotePriceUpdate` | ネゴシエーション可能な見積もりの価格を更新します。 必須 [**[!UICONTROL Quotes]**](quotes.md) オプションが有効になっている場合は、管理システム設定で有効になります。 |
| `purchaseorder.toorder` | 発注書を注文に変換します。 必須 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションが有効になっている場合は、管理システム設定で有効になります。 |
| `purchaseorder.transactional.email` | 発注書の電子メールを送信します。 必須 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションが有効になっている場合は、管理システム設定で有効になります。 |
| `purchaseorder.validation` | 関連するに対して発注を検証します [承認ルール](account-dashboard-approval-rules.md). 必須 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションが有効になっている場合は、管理システム設定で有効になります。 |
| `quoteItemCleaner` | 商品がカタログから削除されたり、買い物かごから削除されたりした場合に、無効または非アクティブな価格見積もりを削除します。 必須 [**[!UICONTROL Quotes]**](quotes.md) オプションが有効になっている場合は、管理システム設定で有効になります。 |
| `inventoryQtyCounter` | 注文が行われた後、または製品が削除された後に、在庫指数を非同期で修正します。 必須 [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) オプションがInventory managementに対して有効になっている場合は、管理者設定を使用します。 詳しくは、 [パフォーマンスのベストプラクティス](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | の個々のタスクにメッセージを作成します [バルク操作](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)（品目のインポートまたはエクスポート、一括価格での価格変更、倉庫への製品の割り当てなど）。 必須 [**管理の一括操作**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) のオプション [!DNL Inventory Management] が **非同期で実行** 」をクリックします。 |

{style="table-layout:auto"}

>[!NOTE]
>
>すべてのAdobe Commerce Message Consumer のリストについては、 [メッセージキューコンシューマー](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) （内） _設定ガイド_.

### メッセージコンシューマーの設定

次のパラメーターを追加して、処理の問題や遅延を防ぐ： [メッセージ消費者を起動](#start-message-consumers) B2B 機能用。

- `--max-messages <value>` — 各コンシューマーが処理する必要がある最大メッセージ数を指定します ( デフォルトは10000)。 お勧めしませんが、0 を使用して、消費者が終了するのを防ぐことができます。 PHP アプリケーションのベストプラクティスは、長時間実行されるプロセスを再起動して、メモリリークを防ぐことです。

- `--batch-size <value>` — コンシューマーが消費するシステムリソース（CPU、メモリ）を制限できます。 小さいバッチを使用すると、リソースの使用量が削減されるので、処理が遅くなります。  指定した場合、キュー内のメッセージは `<value>` それぞれ このオプションは、バッチコンシューマーにのみ適用されます。 次の場合 `--batch-size` が定義されていない場合、バッチコンシューマーは、使用可能なすべてのメッセージをキューで受け取ります。

その他の設定オプションについて詳しくは、 [特定の設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### メッセージコンシューマーを開始

B2B 機能の非同期操作を有効にするには、複数のメッセージコンシューマーを開始する必要があります。

1. 使用可能なメッセージコンシューマーをリストします。

   ```bash
   bin/magento queue:consumers:list
   ```

   このコマンドは、使用可能なメッセージコンシューマー ( すべての [B2B メッセージ消費者](#message-consumers).

1. 各消費者を個別に開始します。

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   例：

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>バックグラウンドで実行するには、「 `&` コマンドに戻り、プロンプトに戻り、コマンドの実行を続けます。 例： `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

詳しくは、 [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) （内） _設定ガイド_.

### cron にメッセージコンシューマーを追加

実行スケジュールを自動化するオプションがあります。 `SharedCatalogUpdateCategoryPermissions` および `SharedCatalogUpdatePrice` cron 設定ファイルにスケジュールを追加してコンシューマーにメッセージを送信 [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

また、 [ストアの設定](../systems/cron.md) 」と入力します。

## 管理での B2B 機能の有効化

B2B for Adobe Commerce拡張機能をインストールし、メッセージコンシューマーを起動した後も、 [管理者での B2B 機能の有効化](enable-basic-features.md).
