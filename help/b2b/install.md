---
title: のインストール [!DNL Adobe Commerce B2B] 拡張子
description: のインストール方法を説明します [!DNL Adobe Commerce B2B] メタパッケージ。
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# のインストール [!DNL Adobe Commerce B2B] 拡張子

Adobe Commerce B2B 拡張機能 `magento/extension-b2b` は、サポートされているすべてのバージョンのAdobe Commerceで使用できます。 Adobe Commerceのインストール後にインストールされます。


## 要件

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html)、サポートされているすべてのバージョン
- PHP 8.1 / 8.2 / 8.3
- [!DNL Composer]

## サポートされるプラットフォーム

- クラウドインフラストラクチャー上のAdobe Commerce（ECE）
- Adobe Commerce オンプレミス（EE）

## インストール手順

>[!BEGINSHADEBOX]

**前提条件**

- アクセス先 [repo.magento.com](https://repo.magento.com/) から拡張機能をダウンロードします。 キーの生成と必要な権限の取得については、を参照してください。 [認証キーの取得](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  で認証キーをグローバルに定義して、インストール用に保存します。 [COMPOSER_ホーム](https://getcomposer.org/doc/03-cli.md#composer-home) ディレクトリ。 または、に保存します [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) ファイル（Adobe Commerce アプリケーションのルートディレクトリ内）。

- [B2B 拡張機能のサポートされているバージョン](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability) – デプロイされているAdobe Commerceのバージョンでサポートされている B2B 拡張機能の最新バージョンを確認します。

- インストールまたはアップグレードの要件に影響を与える可能性のある、バージョンの互換性、アップデート、変更に関する最新の情報については、リリースノートを参照してください。

   - [B2B リリースノート](release-notes.md)
   - [Adobe Commerce リリースノート](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

B2B 拡張機能のインストール （`magento/b2b-extension`）を使用します。 拡張機能は、Adobe Commerce インスタンスの B2B 機能を有効にするモジュールのコレクションを含む composer メタパッケージです。 含まれているモジュールのリストについては、を参照してください。 [B2B パッケージ](packages.md).

>[!BEGINTABS]

>[!TAB クラウドインフラストラクチャ]

>[!TIP]
>
>Adobeでは、クラウドインフラストラクチャにAdobe Commerce B2B をインストールする場合、開始前にAdobe Commerce アプリケーションを統合環境またはステージング環境にデプロイすることをお勧めします。

Adobeでは、B2B 拡張機能をプロジェクトに追加する際に、開発ブランチで作業することをお勧めします。 ブランチがない場合は、 [開発用のブランチの作成](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). B2B 拡張機能をインストールする場合、 `Magento_B2b` 拡張機能名はに自動的に挿入されます。 `app/etc/config.php` ファイル。 ファイルを直接編集する必要はありません。

**B2B 拡張機能をインストールするには**:

1. ローカルワークステーションで、をプロジェクトディレクトリに変更します。

1. 開発ブランチを作成またはチェックアウトします。

1. に B2B 拡張機能を追加 `require` の節 `composer.json` ファイル。

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. プロジェクトの依存関係を更新します。

   ```bash
   composer update
   ```

1. コードの変更を追加、コミットおよびプッシュします。

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >更新をクラウド環境にプッシュすると、Commerce クラウドのデプロイメントプロセスが開始されて、変更が適用されます。 からデプロイメントステータスを確認します。 [ログをデプロイ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). デプロイメントエラーが発生した場合は、を参照してください。 [コンポーネント障害からのリカバリ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. ビルドおよびデプロイが完了したら、SSH を使用してリモート環境にログインし、B2B 拡張機能がインストールされ、有効になっていることを確認します。

   ```bash
   bin/magento module:status Magento_B2b
   ```

   拡張機能名には、次の形式を使用します。 `<VendorName>_<ComponentName>`.

   応答の例：

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB オンプレミス]

1. Adobe Commerce アプリケーションのルートディレクトリから、を更新します `composer.json` b2B 拡張機能の依存関係を追加するには：

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   エラーが発生した場合、例えば次のようになります。

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   パッケージのスペル、バージョンの制約、パッケージが使用可能で、最小安定性（安定）の要件に一致していることを確認します。

1. プロンプトが表示されたら、 [認証キー](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

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

>[!ENDTABS]

インストールが完了したら、メッセージコンシューマーを設定して起動します。

## メッセージコンシューマー

Adobe Commerce B2B 拡張機能は、メッセージキューの管理に MySQL を使用します。 次の表に、B2B 機能をサポートするメッセージコンシューマーを示します。 拡張機能をインストールしたら、Commerce ストアフロントに必要な B2B 機能について、メッセージコンシューマーを開始します。

| 消費者 | 説明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 共有カタログ内の各製品の価格を更新します。 次の場合に必須： [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) オプションは、「管理システム」設定で有効になっています。 |
| `sharedCatalogUpdateCategoryPermissions` | 共有カタログ カテゴリに割り当てられているカテゴリを更新します。 次の場合に必須： [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) オプションは、「管理システム」設定で有効になっています。 |
| `negotiableQuotePriceUpdate` | 交渉可能な見積の価格を更新します。 次の場合に必須： [**[!UICONTROL Quotes]**](quotes.md) オプションは、「管理システム」設定で有効になっています。 |
| `purchaseorder.toorder` | 発注書を注文に変換します。 次の場合に必須： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションは、「管理システム」設定で有効になっています。 |
| `purchaseorder.transactional.email` | 発注書 E メールを送信します。 次の場合に必須： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションは、「管理システム」設定で有効になっています。 |
| `purchaseorder.validation` | 関連する発注を検証します。 [承認ルール](account-dashboard-approval-rules.md). 次の場合に必須： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションは、「管理システム」設定で有効になっています。 |
| `quoteItemCleaner` | 商品がカタログから削除された場合、または買い物かごから削除された場合に、無効または非アクティブな価格見積を削除します。 次の場合に必須： [**[!UICONTROL Quotes]**](quotes.md) オプションは、「管理システム」設定で有効になっています。 |
| `inventoryQtyCounter` | 注文または製品の削除後に、在庫インデックスを非同期で修正します。 次の場合に必須： [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) 「」オプションが、Admin Configuration Settings のInventory managementに対して有効になっている。 参照： [パフォーマンスのベストプラクティス](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | の個々のタスクごとにメッセージを作成します [一括操作](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) 品目のインポートまたはエクスポート、一括スケールでの価格変更、倉庫への製品の割当てなど。 次の場合に必須： [**管理の一括操作**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) オプション [!DNL Inventory Management] はに設定されています。 **非同期で実行** 管理システムの設定で行います。 |

{style="table-layout:auto"}

>[!NOTE]
>
>すべてのAdobe Commerce メッセージコンシューマーのリストについては、以下を参照してください [メッセージキューコンシューマー](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) が含まれる _設定ガイド_.

### メッセージコンシューマーの設定

次のパラメーターを追加して、発生する可能性のある処理の問題や遅延を防ぎます [メッセージコンシューマーの開始](#start-message-consumers) （B2B 機能用）。

- `--max-messages <value>` – 各消費者が終了するまでに処理する必要があるメッセージの最大数を指定します（デフォルトは 10000）。 Adobeでは推奨しませんが、0 を使用して、コンシューマーが終了しないようにできます。 PHP アプリケーションのベストプラクティスは、長時間実行されているプロセスを再起動して、メモリリークの可能性を防ぐことです。

- `--batch-size <value>`- コンシューマーが消費するシステムリソース （CPU、メモリ）を制限できます。 より小さなバッチを使用すると、リソースの使用量が減少します。その結果、処理が遅くなります。  指定した場合、キュー内のメッセージが次のバッチで消費されます `<value>` 各。 このオプションは、バッチコンシューマーにのみ適用できます。 次の場合 `--batch-size` が定義されていない場合、バッチコンシューマーはキュー内の使用可能なすべてのメッセージを受け取ります。

その他の設定オプションについては、を参照してください。 [特定の設定](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

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

詳しくは、を参照してください [メッセージキューの管理](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) が含まれる _設定ガイド_.

### Cron へのメッセージコンシューマーの追加

の実行スケジュールを自動化できます `SharedCatalogUpdateCategoryPermissions` および `SharedCatalogUpdatePrice` cron 設定ファイルにスケジュールを追加してメッセージコンシューマーに送信 [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

また、からメッセージコンシューマーのスケジュールを設定することもできます [ストアの設定](../systems/cron.md) admin.

## 管理者で B2B 機能を有効にする

Adobe Commerce B2B 拡張機能をインストールしてメッセージコンシューマーを開始した後、次の手順も実行する必要があります [管理者で B2B 機能を有効にする](enable-basic-features.md).

