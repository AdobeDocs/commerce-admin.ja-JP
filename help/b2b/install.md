---
title: 拡張機能のイ  [!DNL Adobe Commerce B2B]  ストール
description: メタパッケージのインストール方法  [!DNL Adobe Commerce B2B]  説明します。
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 25964363ca5c4ec849e231d4eccb5f60b682a499
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# [!DNL Adobe Commerce B2B] 拡張機能のインストール

Adobe Commerce B2B 拡張機能は、サポートされてい `magento/extension-b2b`Adobe Commerceのすべてのバージョンで使用できます。 Adobe Commerceのインストール後にインストールされます。


## 要件

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html)、サポートされているすべてのバージョン
- PHP 8.1、8.2、8.3 （B2B 1.5.0 が必要）
- [!DNL Composer]

>[!IMPORTANT]
>
>Adobe Commerce B2B バージョン 1.4.2 以降は、PHP 8.3 と互換性がありません。Commerce インスタンスをCommerce バージョン 2.4.7 以降にアップグレードする場合は、B2B 1.4.2 以降との互換性を維持するために、インスタンスにインストールされている PHP のバージョンが PHP 8.2 であることを確認します。

## サポートされるプラットフォーム

- クラウドインフラストラクチャー上のAdobe Commerce（ECE）
- Adobe Commerce オンプレミス（EE）

## インストール手順

>[!BEGINSHADEBOX]

**前提条件**

- [repo.magento.com](https://repo.magento.com/) にアクセスして、拡張機能をダウンロードします。 キーの生成と必要な権限の取得については、[ 認証キーの取得 ](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) を参照してください。

  [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) ディレクトリでグローバルに定義することにより、インストール用に認証キーを保存します。 または、Adobe Commerce アプリケーションのルートディレクトリにある [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) ファイルに保存します。

- [B2B 拡張機能のサポート対象バージョン ](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability)- デプロイ済みのAdobe Commerce バージョンでサポートされている B2B 拡張機能の最新バージョンを特定します。

- インストールまたはアップグレードの要件に影響を与える可能性のある、バージョンの互換性、アップデート、変更に関する最新の情報については、リリースノートを参照してください。

   - [B2B リリースノート](release-notes.md)
   - [Adobe Commerce リリースノート ](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Composer を使用して B2B 拡張機能（`magento/b2b-extension`）をインストールします。 拡張機能は、Adobe Commerce インスタンスの B2B 機能を有効にするモジュールのコレクションを含む composer メタパッケージです。 含まれているモジュールのリストについては、[B2B パッケージ ](packages.md) を参照してください。

>[!BEGINTABS]

>[!TAB  クラウドインフラストラクチャ ]

>[!TIP]
>
>Adobeでは、クラウドインフラストラクチャにAdobe Commerce B2B をインストールする場合、開始前にAdobe Commerce アプリケーションを統合環境またはステージング環境にデプロイすることをお勧めします。

Adobeでは、B2B 拡張機能をプロジェクトに追加する際に、開発ブランチで作業することをお勧めします。 ブランチがない場合は、[ 開発用のブランチの作成 ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) を参照してください。 B2B 拡張機能をインストールする場合、`Magento_B2b` 拡張機能名が `app/etc/config.php` ファイルに自動的に挿入されます。 ファイルを直接編集する必要はありません。

**B2B 拡張機能をインストールするには**:

1. ローカルワークステーションで、をプロジェクトディレクトリに変更します。

1. 開発ブランチを作成またはチェックアウトします。

1. `composer.json` ファイルの `require` セクションに B2B 拡張機能を追加します。

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
   >更新をクラウド環境にプッシュすると、Commerce クラウドのデプロイメントプロセスが開始されて、変更が適用されます。 [ デプロイメントログ ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) からデプロイメントステータスを確認します。 デプロイメントエラーが発生した場合は、[ コンポーネントの障害からの回復 ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment) を参照してください。

1. ビルドおよびデプロイが完了したら、SSH を使用してリモート環境にログインし、B2B 拡張機能がインストールされ、有効になっていることを確認します。

   ```bash
   bin/magento module:status Magento_B2b
   ```

   拡張機能名には、`<VendorName>_<ComponentName>` の形式を使用します。

   応答の例：

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB  オンプレミス ]

1. Adobe Commerce アプリケーションのルートディレクトリから、`composer.json` を更新して B2B 拡張機能の依存関係を追加します。

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   エラーが発生した場合、例えば次のようになります。

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   パッケージのスペル、バージョンの制約、パッケージが使用可能で、最小安定性（安定）の要件に一致していることを確認します。

1. プロンプトが表示されたら、[ 認証キー ](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) を入力します。

   _公開鍵_ はユーザー名で、_秘密鍵_ はパスワードです。 公開鍵と秘密鍵を `auth.json` に保存している場合は、認証を求められません。

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
   >実稼動モードでは、`Please rerun Magento compile command` へのメッセージが表示される場合があります。 コマンドを入力して、インストールを完了します。 Adobe Commerceでは、開発者モードでコンパイルコマンドを実行するように求められることはありません。

>[!ENDTABS]

インストールが完了したら、メッセージコンシューマーを設定して起動します。

## メッセージコンシューマー

Adobe Commerce B2B 拡張機能は、メッセージキューの管理に MySQL を使用します。 次の表に、B2B 機能をサポートするメッセージコンシューマーを示します。 拡張機能をインストールしたら、Commerce ストアフロントに必要な B2B 機能について、メッセージコンシューマーを開始します。

| 消費者 | 説明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 共有カタログ内の各製品の価格を更新します。 管理システムの設定で「[**[!UICONTROL Shared Catalogs]**](catalog-shared.md)」オプションが有効になっている場合は必須です。 |
| `sharedCatalogUpdateCategoryPermissions` | 共有カタログ カテゴリに割り当てられているカテゴリを更新します。 管理システムの設定で「[**[!UICONTROL Shared Catalogs]**](catalog-shared.md)」オプションが有効になっている場合は必須です。 |
| `negotiableQuotePriceUpdate` | 交渉可能な見積の価格を更新します。 管理システムの設定で「[**[!UICONTROL Quotes]**](quotes.md)」オプションが有効になっている場合は必須です。 |
| `purchaseorder.toorder` | 発注書を注文に変換します。 管理システムの設定で「[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)」オプションが有効になっている場合は必須です。 |
| `purchaseorder.transactional.email` | 発注書 E メールを送信します。 管理システムの設定で「[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)」オプションが有効になっている場合は必須です。 |
| `purchaseorder.validation` | 関連する [ 承認ルール ](account-dashboard-approval-rules.md) に対して発注書を検証します。 管理システムの設定で「[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)」オプションが有効になっている場合は必須です。 |
| `quoteItemCleaner` | 商品がカタログから削除された場合、または買い物かごから削除された場合に、無効または非アクティブな価格見積を削除します。 管理システムの設定で「[**[!UICONTROL Quotes]**](quotes.md)」オプションが有効になっている場合は必須です。 |
| `inventoryQtyCounter` | 注文または製品の削除後に、在庫インデックスを非同期で修正します。 Admin 設定でInventory managementに対して「[**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options)」オプションが有効になっている場合は必須です。 [ パフォーマンスのベストプラクティス ](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update) を参照してください。 |
| `async.operations.all` | 品目のインポートまたはエクスポート、一括スケールでの価格の変更、倉庫への製品の割り当てなど [&#128279;](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) 一括操作  の個々のタスクごとにメッセージを作成します。 [!DNL Inventory Management] の [**管理者の一括操作**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) オプションが管理システムの設定で **非同期で実行** に設定されている場合に必要です。 |

{style="table-layout:auto"}

>[!NOTE]
>
>すべてのAdobe Commerce メッセージコンシューマーのリストについては、『 [ 設定ガイド ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) の _メッセージキューコンシューマー_ を参照してください。

### メッセージコンシューマーの設定

B2B 機能について [ メッセージコンシューマーを開始 ](#start-message-consumers) する際に、次のパラメーターを追加して、処理の問題や遅延の可能性を防ぎます。

- `--max-messages <value>` – 各消費者が終了するまでに処理する必要があるメッセージの最大数を指定します（デフォルトは 10000）。 Adobeでは推奨しませんが、0 を使用して、コンシューマーが終了しないようにできます。 PHP アプリケーションのベストプラクティスは、長時間実行されているプロセスを再起動して、メモリリークの可能性を防ぐことです。

- `--batch-size <value>` - コンシューマーが使用するシステムリソースを制限できます（CPU、メモリ）。 より小さなバッチを使用すると、リソースの使用量が減少します。その結果、処理が遅くなります。  指定した場合、キュー内のメッセージが各 `<value>` のバッチで消費されます。 このオプションは、バッチコンシューマーにのみ適用できます。 `--batch-size` が定義されていない場合、バッチコンシューマーはキュー内の使用可能なすべてのメッセージを受け取ります。

その他の設定オプションについて詳しくは、[ 特定の設定 ](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration) を参照してください。

### メッセージコンシューマーの開始

B2B 機能の非同期操作を有効にするには、複数のメッセージコンシューマーを開始する必要があります。

1. 使用可能なメッセージコンシューマーのリストを表示します。

   ```bash
   bin/magento queue:consumers:list
   ```

   このコマンドは、すべての [B2B メッセージコンシューマー ](#message-consumers) を含む、使用可能なメッセージコンシューマーを返します。

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
>バックグラウンドで実行するには、コマンドに `&` を追加し、プロンプトに戻ってコマンドを実行し続けます。 例：`bin/magento queue:consumers:start sharedCatalogUpdatePrice &`。

詳しくは、『 _設定ガイド_ の [ メッセージキューの管理 ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) を参照してください。

### Cron へのメッセージコンシューマーの追加

cron 設定ファイル [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management) にスケジュールを追加することで、`SharedCatalogUpdateCategoryPermissions` および `SharedCatalogUpdatePrice` メッセージコンシューマーの実行スケジュールを自動化できます。

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

また、管理者の [ ストア設定 ](../systems/cron.md) から、メッセージコンシューマーのスケジュールを設定することもできます。

## 管理者で B2B 機能を有効にする

Adobe Commerce B2B 拡張機能をインストールしてメッセージコンシューマーを開始した後、[ 管理者で B2B 機能を有効にする ](enable-basic-features.md) 必要もあります。

