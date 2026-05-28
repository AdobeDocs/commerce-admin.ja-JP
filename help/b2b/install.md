---
title: ' [!DNL Adobe Commerce B2B] 拡張機能のインストール'
description: ' [!DNL Adobe Commerce B2B]  メタパッケージのインストール方法について説明します。'
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: 25964363ca5c4ec849e231d4eccb5f60b682a499
workflow-type: tm+mt
source-wordcount: '1320'
ht-degree: 0%

---


# [!DNL Adobe Commerce B2B]拡張機能のインストール

Adobe Commerce B2B拡張機能`magento/extension-b2b`は、サポートされているすべてのバージョンのAdobe Commerceで使用できます。 Adobe Commerceのインストール後にインストールされます。


## 要件定義

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html)、サポートされているすべてのバージョン
- PHP 8.1、8.2、および8.3 （B2B 1.5.0が必要）
- [!DNL Composer]

>[!IMPORTANT]
>
>Adobe Commerce B2B バージョン 1.4.2以降は、PHP 8.3と互換性がありません。 Commerce インスタンスをCommerce バージョン 2.4.7以降にアップグレードする場合は、B2B 1.4.2以降との互換性を維持するために、インスタンスにインストールされているPHP バージョンがPHP 8.2であることを確認してください。

## サポートされているプラットフォーム

- Adobe Commerce on cloud infrastructure （ECE）
- Adobe Commerce オンプレミス（EE）

## インストール手順

>[!BEGINSHADEBOX]

**前提条件**

- 拡張機能をダウンロードするには、[repo.magento.com](https://repo.magento.com/)にアクセスしてください。 キーの生成と必要な権限の取得については、[認証キーの取得](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)を参照してください。

  認証キーを[COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) ディレクトリでグローバルに定義して、インストール用に保存します。 または、Adobe Commerce アプリケーションルートディレクトリの[auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) ファイルに保存します。

- [&#x200B; サポートされているB2B拡張機能のバージョン &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability) – デプロイされたAdobe CommerceのバージョンでサポートされているB2B拡張機能の最新バージョンを確認します。

- リリースノートを参照して、インストールやアップグレードの要件に影響を与える可能性のあるバージョンの互換性、アップデート、変更に関する最新の情報を確認してください。

   - [B2B リリースノート](release-notes.md)
   - [Adobe Commerce リリースノート](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Composerを使用してB2B拡張機能（`magento/b2b-extension`）をインストールします。 拡張機能は、Adobe Commerce インスタンスのB2B機能を有効にするモジュールのコレクションを含むコンポーザーメタパッケージです。 含まれるモジュールの一覧については、[B2B パッケージ &#x200B;](packages.md)を参照してください。

>[!BEGINTABS]

>[!TAB  クラウド インフラストラクチャ ]

>[!TIP]
>
>クラウドインフラストラクチャにAdobe Commerce B2Bをインストールする場合、Adobeでは、開始する前にAdobe Commerce アプリケーションを統合環境またはステージング環境にデプロイすることをお勧めします。

Adobeでは、B2B拡張機能をプロジェクトに追加する際に、開発ブランチで作業することをお勧めします。 分岐がない場合は、[開発用の分岐の作成](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)を参照してください。 B2B拡張機能をインストールすると、`Magento_B2b`拡張機能の名前が`app/etc/config.php` ファイルに自動的に挿入されます。 ファイルを直接編集する必要はありません。

**B2B拡張機能をインストールするには**:

1. ローカル ワークステーションで、プロジェクト ディレクトリに移動します。

1. 開発ブランチを作成またはチェックアウトします。

1. B2B拡張機能を`composer.json` ファイルの`require` セクションに追加します。

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. プロジェクトの依存関係を更新します。

   ```bash
   composer update
   ```

1. コードの変更を追加、コミット、プッシュします。

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
   >クラウド環境に更新をプッシュすると、Commerce クラウドデプロイメントプロセスが開始され、変更が適用されます。 [&#x200B; デプロイ ログ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)のデプロイメント ステータスを確認します。 デプロイメントエラーが発生した場合は、[&#x200B; コンポーネントエラーからの回復](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment)を参照してください。

1. ビルドとデプロイが完了したら、SSHを使用してリモート環境にログインし、B2B拡張機能がインストールされ、有効になっていることを確認します。

   ```bash
   bin/magento module:status Magento_B2b
   ```

   拡張機能の名前では、次の形式が使用されています：`<VendorName>_<ComponentName>`。

   回答サンプル：

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB  オンプレミス ]

1. Adobe Commerce アプリケーションのルートディレクトリから`composer.json`を更新して、B2B拡張機能の依存関係を追加します。

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   エラーが発生した場合、例：

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   パッケージのスペル、バージョンの制約、およびパッケージが使用可能で、最小安定性（安定）要件に一致することを確認します。

1. プロンプトが表示されたら、[認証キー](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)を入力します。

   _公開鍵_&#x200B;はユーザー名、秘密鍵&#x200B;_はパスワードです。_&#x200B;公開鍵と秘密鍵を`auth.json`に保存している場合、認証を求めるメッセージは表示されません。

1. Composerでモジュールの更新が完了したら、次のコマンドを実行します。

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
   >実稼動モードでは、`Please rerun Magento compile command`へのメッセージが表示される場合があります。 コマンドを入力して、インストールを完了します。 Adobe Commerceでは、開発者モードでコンパイルコマンドを実行するプロンプトは表示されません。

>[!ENDTABS]

インストールが完了したら、メッセージコンシューマーを設定して開始します。

## メッセージコンシューマー

Adobe Commerce B2B拡張機能は、メッセージキュー管理にMySQLを使用します。 次の表に、B2B機能をサポートするメッセージコンシューマーを示します。 拡張機能をインストールしたら、Commerce ストアフロントに必要なB2B機能のメッセージコンシューマーを開始します。

| 消費者 | 説明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 共有カタログ内の各製品の価格を更新します。 管理者システム構成設定で[**[!UICONTROL Shared Catalogs]**](catalog-shared.md) オプションが有効になっている場合は必須です。 |
| `sharedCatalogUpdateCategoryPermissions` | 共有カタログ カテゴリに割り当てられたカテゴリを更新します。 管理者システム構成設定で[**[!UICONTROL Shared Catalogs]**](catalog-shared.md) オプションが有効になっている場合は必須です。 |
| `negotiableQuotePriceUpdate` | 交渉可能な見積の価格を更新します。 管理者システム構成設定で[**[!UICONTROL Quotes]**](quotes.md) オプションが有効になっている場合は必須です。 |
| `purchaseorder.toorder` | 発注書を発注書に変換します。 管理者システム構成設定で[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションが有効になっている場合は必須です。 |
| `purchaseorder.transactional.email` | 発注書のメールを送信する。 管理者システム構成設定で[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションが有効になっている場合は必須です。 |
| `purchaseorder.validation` | 関連する[承認ルール &#x200B;](account-dashboard-approval-rules.md)に対して発注書を検証します。 管理者システム構成設定で[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) オプションが有効になっている場合は必須です。 |
| `quoteItemCleaner` | 商品がカタログから削除されたり、買い物かごから削除されたりすると、無効または非アクティブな価格見積もりを削除します。 管理者システム構成設定で[**[!UICONTROL Quotes]**](quotes.md) オプションが有効になっている場合は必須です。 |
| `inventoryQtyCounter` | 注文または商品が削除された後に、在庫指数を非同期で修正します。 管理者設定で[**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) オプションがInventory managementに対して有効になっている場合に必要です。 [&#x200B; パフォーマンスのベストプラクティス &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update)を参照してください。 |
| `async.operations.all` | 品目のインポートまたはエクスポート、大規模な価格変更、倉庫への製品の割り当てなど、[一括操作](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)の各タスクに対するメッセージを作成します。 [!DNL Inventory Management]の&#x200B;[**管理者一括操作**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) オプションが&#x200B;**管理者システム構成設定で非同期実行**&#x200B;に設定されている場合に必要です。 |

{style="table-layout:auto"}

>[!NOTE]
>
>すべてのAdobe Commerce メッセージコンシューマーの一覧については、_設定ガイド_&#x200B;の[&#x200B; メッセージキューコンシューマー](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers)を参照してください。

### メッセージコンシューマーの設定

B2B機能のメッセージ コンシューマー[&#128279;](#start-message-consumers)を開始する際に次のパラメーターを追加することで、処理の問題や遅延が発生する可能性を防ぎます。

- `--max-messages <value>` – 各コンシューマーが終了する前に処理する必要があるメッセージの最大数を指定します（デフォルト = 10000）。 Adobeではお勧めしませんが、0を使用すると、コンシューマーが終了するのを防ぐことができます。 PHP アプリケーションのベストプラクティスは、メモリのリークを防ぐために、長時間実行しているプロセスを再起動することです。

- `--batch-size <value>` - コンシューマー（CPU、メモリ）が消費するシステム リソースを制限できます。 バッチを小さくすると、リソース使用量が減少するため、処理が遅くなります。  指定した場合、キュー内のメッセージは、それぞれ`<value>`個のバッチで消費されます。 このオプションは、バッチコンシューマーにのみ適用されます。 `--batch-size`が定義されていない場合、バッチコンシューマーはキュー内のすべての利用可能なメッセージを受信します。

追加の設定オプションについて詳しくは、[特定の設定](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration)を参照してください。

### メッセージ消費者を開始

B2B機能の非同期操作を有効にするには、複数のメッセージコンシューマーを開始する必要があります。

1. 使用可能なメッセージコンシューマーのリスト：

   ```bash
   bin/magento queue:consumers:list
   ```

   このコマンドは、すべての[B2B メッセージコンシューマー](#message-consumers)を含む、使用可能なメッセージコンシューマーを返します。

1. 各コンシューマーを個別に開始：

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   例：

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>バックグラウンドで実行するには、コマンドに`&`を追加し、プロンプトに戻ってコマンドを実行し続けます。 例：`bin/magento queue:consumers:start sharedCatalogUpdatePrice &`。

詳しくは、_設定ガイド_&#x200B;の「[&#x200B; メッセージキューの管理](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues)」を参照してください。

### cronへのメッセージコンシューマーの追加

スケジュールをcron設定ファイル [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management)に追加することで、`SharedCatalogUpdateCategoryPermissions`および`SharedCatalogUpdatePrice` メッセージ コンシューマーの実行スケジュールを自動化できます。

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

また、管理者の[&#x200B; ストア設定設定](../systems/cron.md)から、メッセージコンシューマーのスケジュールを設定することもできます。

## 管理者でB2B機能を有効にする

Adobe Commerce B2B拡張機能をインストールし、メッセージコンシューマーを開始したら、Admin[&#128279;](enable-basic-features.md)でB2B機能を有効にする必要があります。

