---
source-git-commit: a37e67c332140fbba7609db8cc5e22a3625a1c9d
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---
# B2B パッケージのAdobe Commerce

<!-- The 'packages' variable contains the 'packages' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'packages-dev' variable contains the 'packages-dev' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'product' variable contains data of the 'magento/product-enterprise-edition' package
 -->

<!-- The edition variable contains `commerce-b2b` value from the _data/names.yml file
 -->

Adobe Commerce B2B では、Composer を使用して PHP パッケージを管理します。

`composer.json` ファイルはパッケージのリストを宣言します。`composer.lock` ファイルは、Adobe Commerce B2B のインストールのビルドに使用されるパッケージの完全なリスト（各パッケージの完全なバージョンとその依存関係）を格納します。

次のリファレンスドキュメントは `composer.lock` ファイルから生成され、Adobe Commerce B2B 1.5.2 に含まれている必須パッケージをカバーしています。

## 依存関係

`magento/extension-b2b 1.5.2` には次の依存関係があります。

- magento/framework: >=103.0.6 &lt;103.0.9
- magento/magento2-b2b-base:1.5.2
- [magento/module-b2b](https://developer.adobe.com/commerce/php/module-reference/module-b2b/): 100.5.2
- [magento/module-bundle-negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-bundle-negotiable-quote/):100.5.1
- [magento/module-bundle-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list/):100.5.1
- [magento/module-bundle-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list-graph-ql/):1.5.1
- [magento/module-bundle-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-bundle-shared-catalog/):100.5.1
- [magento/module-checkout-address-search-negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-address-search-negotiable-quote/):100.5.1
- [magento/module-checkout-agreements-negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-negotiable-quote/): 100.5.1
- [magento/module-checkout-agreements-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-purchase-order/): 1.5.1
- [magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company/):102.0.2
- [magento/module-company-asynchronous-operations](https://developer.adobe.com/commerce/php/module-reference/module-company-asynchronous-operations/):1.5.1
- [magento/module-company-credit](https://developer.adobe.com/commerce/php/module-reference/module-company-credit/):100.5.2
- [magento/module-company-credit-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-credit-graph-ql/):1.5.1
- [magento/module-company-customer-import-export](https://developer.adobe.com/commerce/php/module-reference/module-company-customer-import-export/):1.5.0
- [magento/module-company-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-graph-ql/):1.5.2
- [magento/module-company-negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote/):1.5.1
- [magento/module-company-negotiable-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote-template/):1.5.1
- [magento/module-company-payment](https://developer.adobe.com/commerce/php/module-reference/module-company-payment/): 100.5.1
- [magento/module-company-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-quote/): 1.5.2
- [magento/module-company-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-quote-graph-ql/):1.5.2
- [magento/module-company-relation](https://developer.adobe.com/commerce/php/module-reference/module-company-relation/):1.5.2
- [magento/module-company-relation-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-company-relation-shared-catalog/):1.5.1
- [magento/module-company-shipping](https://developer.adobe.com/commerce/php/module-reference/module-company-shipping/):1.5.1
- [magento/module-configurable-negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-configurable-negotiable-quote/):100.5.1
- [magento/module-configurable-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list/): 100.5.1
- [magento/module-configurable-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list-graph-ql/):1.5.1
- [magento/module-configurable-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-configurable-shared-catalog/):100.5.1
- [magento/module-downloadable-company](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-company/):1.5.1
- [magento/module-downloadable-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-requisition-list-graph-ql/):1.5.1
- [magento/module-gift-card-negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-negotiable-quote/): 100.5.1
- [magento/module-gift-card-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list/): 100.5.1
- [magento/module-gift-card-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list-graph-ql/):1.5.1
- [magento/module-gift-card-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-shared-catalog/):100.5.1
- [magento/module-grouped-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-grouped-requisition-list/): 100.5.1
- [magento/module-grouped-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-grouped-shared-catalog/):100.5.1
- [magento/module-negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote/): 101.0.2
- [magento/module-negotiable-quote-async-order](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-async-order/): 1.5.1
- [magento/module-negotiable-quote-duplicate](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate/): 1.5.2
- [magento/module-negotiable-quote-duplicate-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate-graph-ql/):1.5.1
- [magento/module-negotiable-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-graph-ql/):1.5.1
- [magento/module-negotiable-quote-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list/): 1.5.1
- [magento/module-negotiable-quote-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list-graph-ql/):1.5.1
- [magento/module-negotiable-quote-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-shared-catalog/):100.5.1
- [magento/module-negotiable-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template/):1.5.2
- [magento/module-negotiable-quote-template-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-graph-ql/):1.5.2
- [magento/module-negotiable-quote-template-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-shared-catalog/):1.5.1
- [magento/module-negotiable-quote-weee](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-weee/): 100.5.1
- [magento/module-order-history-search](https://developer.adobe.com/commerce/php/module-reference/module-order-history-search/): 100.5.2
- [magento/module-paypal-negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-paypal-negotiable-quote/):1.5.1
- [magento/module-paypal-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-paypal-purchase-order/):1.5.1
- [magento/module-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order/): 100.5.2
- [magento/module-purchase-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-graph-ql/):1.5.1
- [magento/module-purchase-order-rule](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule/): 100.5.2
- [magento/module-purchase-order-rule-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule-graph-ql/):1.5.1
- [magento/module-quick-order](https://developer.adobe.com/commerce/php/module-reference/module-quick-order/):100.5.1
- [magento/module-quick-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-quick-order-graph-ql/):1.5.1
- [magento/module-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list/): 100.5.2
- [magento/module-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list-graph-ql/):1.5.1
- [magento/module-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog/):100.5.2
- [magento/module-shared-catalog-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog-graph-ql/):1.5.1
- magento/security-package-b2b: 1.0.6

## サードパーティライセンス

### Apache-2.0、LGPL-2.1-only

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/opensearch-project/opensearch-php">opensearch-project/opensearch-php</a>
    </td>
    <td>ライブラリ</td>
    <td>OpenSearch 用 PHP クライアント</td>
  </tr>
  </tbody>
</table>

### Apache-2.0

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/adobe/stock-api-libphp">astock/stock-api-libphp</a>
    </td>
    <td>ライブラリ</td>
    <td>Adobe Stock API ライブラリ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/awslabs/aws-crt-php">aws/aws-crt-php</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP 用AWS共通ランタイム</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/aws/aws-sdk-php">aws/aws-sdk-php</a>
    </td>
    <td>ライブラリ</td>
    <td>AWS SDK for PHP - PHP プロジェクトでAmazon Web Servicesを使用する</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/api"> オープンテレメトリ/api</a>
    </td>
    <td>ライブラリ</td>
    <td>OpenTelemetry PHP の API です。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/context"> オープンテレメトリ/コンテキスト </a>
    </td>
    <td>ライブラリ</td>
    <td>OpenTelemetry PHP のコンテキスト実装。</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree
    </td>
    <td>メタパッケージ</td>
    <td>BraintreeMagento</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/wikimedia/less.php">wikimedia/less.php</a>
    </td>
    <td>ライブラリ</td>
    <td>LESS プロセッサの PHP ポート</td>
  </tr>
  </tbody>
</table>

### BSD-2 句

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/Bacon/BaconQrCode">bacon/bacon-qr-code</a>
    </td>
    <td>ライブラリ</td>
    <td>BaconQrCode は、PHP 用の QR コードジェネレータです。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/DASPRiD/Enum">dasprid/enum</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP 7.1 列挙実装</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webimpress/safe-writer">webimpress/safe-writer</a>
    </td>
    <td>ライブラリ</td>
    <td>競合状態を避けるため、ファイルを安全に書き込むためのツール</td>
  </tr>
  </tbody>
</table>

### BSD-3 句

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_File">colinmollenhour/cache-backend-file</a>
    </td>
    <td>Magento-module</td>
    <td>ストックの Zend_Cache_Backend_File バックエンドは、タグによるクリーニングのパフォーマンスが非常に悪く、キャッシュされたアイテムの数が増えると使用できなくなります。 このバックエンドは多くの変更を加え、特にタグのクリーニングのパフォーマンスを大幅に向上させます。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/php-redis-session-abstract">colinmollenhour/php-redis-session-abstract</a>
    </td>
    <td>ライブラリ</td>
    <td>楽観的ロックを使用した Redis ベースのセッションハンドラー</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/duosecurity/duo_universal_php">duosecurity/duo_universal_php</a>
    </td>
    <td>ライブラリ</td>
    <td>Duo Universal SDKの PHP 実装。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/firebase/php-jwt">firebase/php-jwt</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP で JSON ウェブトークン（JWT）をエンコードし、デコードするためのシンプルなライブラリ。 現在の仕様に準拠する必要があります。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-captcha">laminas/laminas-captcha</a>
    </td>
    <td>ライブラリ</td>
    <td>置物、画像、ReCaptcha などを使用した CAPTCHA の生成と検証</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-code">laminas/laminas-code</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP Reflection API、静的コードスキャン、およびコード生成の拡張</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-config">laminas/laminas-config</a>
    </td>
    <td>ライブラリ</td>
    <td>アプリケーション コード内でこの構成データにアクセスするための、ネストされたオブジェクト プロパティ ベースのユーザーインターフェイスを提供します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-di"> ラミナス・ラミナス・ディ </a>
    </td>
    <td>ライブラリ</td>
    <td>PSR-11 コンテナの自動依存関係インジェクション</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-escaper"> ラミナス/ラミナスエスケープ </a>
    </td>
    <td>ライブラリ</td>
    <td>安全かつ安全にHTML、HTML属性、JavaScript、CSS および URL をエスケープ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-eventmanager"> ラミナス/ラミナス – イベントマネージャ </a>
    </td>
    <td>ライブラリ</td>
    <td>PHP アプリケーション内のイベントをトリガーしてリッスンする</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-feed"> ラミナス/ラミナス・フィード </a>
    </td>
    <td>ライブラリ</td>
    <td>rss および Atom フィードを作成および使用する機能を提供します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-filter"> ラミナス/ラミナスフィルター </a>
    </td>
    <td>ライブラリ</td>
    <td>データとファイルをプログラムでフィルタリングし、正規化する</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-http">laminas/laminas-http</a>
    </td>
    <td>ライブラリ</td>
    <td>ハイパーテキスト転送プロトコル （HTTP） リクエストを実行するための簡単なインターフェイスを提供します。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-i18n"> ラミナス/ラミナス – i18n</a>
    </td>
    <td>ライブラリ</td>
    <td>アプリケーションの翻訳を提供し、国際化値をフィルタリングおよび検証します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-json">laminas/laminas-json</a>
    </td>
    <td>ライブラリ</td>
    <td>は、ネイティブの PHP を JSON にシリアル化し、JSON をネイティブの PHP にデコードする便利なメソッドを提供します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-loader"> ラミナス/ラミナスローダー </a>
    </td>
    <td>ライブラリ</td>
    <td>自動読み込みとプラグインの読み込み戦略</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-modulemanager"> ラミナス/ラミナス – モジュールマネージャー </a>
    </td>
    <td>ライブラリ</td>
    <td>ラミナス mvc アプリケーション用モジュール式アプリケーションシステム</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-mvc"> ラミナス/ラミナス – mvc</a>
    </td>
    <td>ライブラリ</td>
    <td>Laminas のイベント駆動型 MVC レイヤー（MVC アプリケーション、コントローラ、プラグインを含む）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-permissions-acl">laminas/laminas-permissions-acl</a>
    </td>
    <td>ライブラリ</td>
    <td>権限管理のための軽量で柔軟なアクセス制御リスト（ACL）実装を提供します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-recaptcha">laminas/laminas-recaptcha</a>
    </td>
    <td>ライブラリ</td>
    <td>ReCaptcha web サービスの OOP ラッパー</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-router">laminas/laminas-router</a>
    </td>
    <td>ライブラリ</td>
    <td>HTTP およびコンソールアプリケーション用の柔軟なルーティングシステム</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-server">laminas/laminas-server</a>
    </td>
    <td>ライブラリ</td>
    <td>反射ベースの RPC サーバを作成する</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-servicemanager"> ラミナス/ラミナス – サービスマネガー </a>
    </td>
    <td>ライブラリ</td>
    <td>ファクトリ駆動の依存関係挿入コンテナ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-session">laminas/laminas-session</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP セッションおよびストレージへのオブジェクト指向インタフェース</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-soap"> ラミナス/ラミナス石鹸 </a>
    </td>
    <td>ライブラリ</td>
    <td></td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-stdlib"> ラミナス/ラミナス – stdlib</a>
    </td>
    <td>ライブラリ</td>
    <td>SPL 拡張機能、配列ユーティリティ、エラーハンドラーなど</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-text"> ラミナス/ラミナス テキスト </a>
    </td>
    <td>ライブラリ</td>
    <td>FIGlets とテキストベースのテーブルの作成</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-translator"> ラミナス/ラミナス – トランスレータ </a>
    </td>
    <td>ライブラリ</td>
    <td>Laminas-i18n の Translator コンポーネント用インターフェイス</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-uri"> ラミナス/ラミナス uri</a>
    </td>
    <td>ライブラリ</td>
    <td>操作と検証を支援するコンポーネント » Uniform Resource Identifier （URI）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-validator">laminas/laminas-validator</a>
    </td>
    <td>ライブラリ</td>
    <td>幅広いドメイン向けの検証クラスと、複雑な検証条件を作成するためにバリデータを連結する機能</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-view"> ラミナス/ラミナス ビュー </a>
    </td>
    <td>ライブラリ</td>
    <td>複数のビューレイヤー、ヘルパーなどをサポートおよび提供する柔軟なビューレイヤー</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/marc-mabe/php-enum">marc-mabe/php-enum</a>
    </td>
    <td>ライブラリ</td>
    <td>ネイティブの PHP を使用した定義済みリストのシンプルかつ迅速な実装</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/nikic/PHP-Parser">nikic/php-parser</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP で書かれた PHP パーサ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpfui/recaptcha">phpui/recaptcha</a>
    </td>
    <td>ライブラリ</td>
    <td>Googleの reCAPTCHA 用クライアントライブラリ（PHP 8.4 以降）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tedious/JShrink">tedivm/jshrink</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP に組み込まれた JavaScript 縮小機能</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tubalmartin/YUI-CSS-compressor-PHP-port"> タバルマーティン/cssmin</a>
    </td>
    <td>ライブラリ</td>
    <td>YUI CSS コンプレッサの PHP ポート</td>
  </tr>
  </tbody>
</table>

### BSD-3 句の変更

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_Redis">colinmollenhour/cache-backend-redis</a>
    </td>
    <td>Magento-module</td>
    <td>タグを完全にサポートする Redis を使用した Zend_Cache バックエンド。</td>
  </tr>
  </tbody>
</table>

### ISC

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/paragonie/sodium_compat">paragonie/sodium_compat</a>
    </td>
    <td>ライブラリ</td>
    <td>純粋な PHP の libsodium の実装。存在する場合は PHP の拡張機能を使用します。</td>
  </tr>
  </tbody>
</table>

### LGPL-2.1 以降

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/ezyang/htmlpurifier">ezyang/htmlpurifier</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP で記述された標準準拠のHTML フィルタ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-amqplib/php-amqplib">php-amqplib/php-amqplib</a>
    </td>
    <td>ライブラリ</td>
    <td>以前は videlalvaro/php-amqplib でした。  このライブラリは、AMQP プロトコルを PHP で実装したものです。 RabbitMQ に対してテストされています。</td>
  </tr>
  </tbody>
</table>

### MIT

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/braintree/braintree_php">braintree/braintree_php</a>
    </td>
    <td>ライブラリ</td>
    <td>Braintree PHP クライアントライブラリ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/math"> ブリック/数学 </a>
    </td>
    <td>ライブラリ</td>
    <td>任意精度演算ライブラリ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/varexporter">brick/varexporter</a>
    </td>
    <td>ライブラリ</td>
    <td>var_export （）の代わりとなる強力な関数で、__set_state （）を使用せずにクロージャやオブジェクトをエクスポートすることができます。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ChristianRiesen/base32">christian-riesen/base32</a>
    </td>
    <td>ライブラリ</td>
    <td>RFC 4648 に準拠した Base32 エンコーダー/デコーダー</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/credis"> コリンモレンアワー/クレディ </a>
    </td>
    <td>ライブラリ</td>
    <td>Credis は Redis のキー値ストアへの軽量なインターフェースで、パフォーマンスを向上させるために利用可能な場合は phpredis ライブラリをラップします。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/ca-bundle">composer/ca-bundle</a>
    </td>
    <td>ライブラリ</td>
    <td>システム CA バンドルへのパスを検索し、Mozilla CA バンドルへのフォールバックを含めることができます。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/class-map-generator">composer/class-map-generator</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP コードをスキャンし、クラスマップを生成するためのユーティリティ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/composer">composer/composer</a>
    </td>
    <td>ライブラリ</td>
    <td>Composer を使用すると、PHP プロジェクトの依存関係を宣言、管理、およびインストールできます。 あらゆる場所に適切なスタックを確保できます。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/metadata-minifier">composer/metadata-minifier</a>
    </td>
    <td>ライブラリ</td>
    <td>メタデータの縮小と拡張を処理する小さなユーティリティライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/pcre">composer/pcre</a>
    </td>
    <td>ライブラリ</td>
    <td>タイプセーフな preg_*代替品を提供する PCRE ラッピングライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/semver">composer/semver</a>
    </td>
    <td>ライブラリ</td>
    <td>ユーティリティ、バージョン制約の解析、および検証を提供する Semver ライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/spdx-licenses">composer/spdx-licenses</a>
    </td>
    <td>ライブラリ</td>
    <td>SPDX ライセンスのリストと検証ライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/xdebug-handler">composer/xdebug-handler</a>
    </td>
    <td>ライブラリ</td>
    <td>Xdebug を指定せずにプロセスを再起動する。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/doctrine/lexer"> ドクトリン/レキサー </a>
    </td>
    <td>ライブラリ</td>
    <td>トップダウン、再帰的なディセントリーパーサーで使用できる PHP ドクトリンレクサーパーサーライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/egulias/EmailValidator">egulias/email-validator</a>
    </td>
    <td>ライブラリ</td>
    <td>複数の RFC に対してメールを検証するためのライブラリ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elastic-transport-php"> 弾力性/輸送性 </a>
    </td>
    <td>ライブラリ</td>
    <td>Elastic 製品用の HTTP トランスポート PHP ライブラリ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elasticsearch-php">elasticsearch/elasticsearch</a>
    </td>
    <td>ライブラリ</td>
    <td>Elasticsearch用 PHP クライアント</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/endroid/qr-code">endroid/qr-code</a>
    </td>
    <td>ライブラリ</td>
    <td>Endroid QR コード</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/guzzlestreams">ezimuel/guzzlestreams</a>
    </td>
    <td>ライブラリ</td>
    <td>elasticsearch-php で使用される guzzle/streams のフォーク（放棄）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/ringphp">ezimuel/ringphp</a>
    </td>
    <td>ライブラリ</td>
    <td>Elasticsearch-php で使用される guzzle/RingPHP のフォーク（放棄）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/guzzle">guzzlehttp/guzzle</a>
    </td>
    <td>ライブラリ</td>
    <td>Guzzle は PHP HTTP クライアントライブラリです</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/promises">guzzlehttp/promises</a>
    </td>
    <td>ライブラリ</td>
    <td>Guzzle Promises ライブラリ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/psr7">guzzlehttp/psr7</a>
    </td>
    <td>ライブラリ</td>
    <td>共通のユーティリティメソッドも提供する PSR-7 メッセージ実装</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jsonrainbow/json-schema">justinrainbow/json-schema</a>
    </td>
    <td>ライブラリ</td>
    <td>JSON スキーマを検証するためのライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem">league/flysystem</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP のファイルストレージの抽象化</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-aws-s3-v3">league/flysystem-aws-s3-v3</a>
    </td>
    <td>ライブラリ</td>
    <td>Flysystem 用のAWS S3 ファイルシステムアダプタ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-local">league/flysystem-local</a>
    </td>
    <td>ライブラリ</td>
    <td>Flysystem 用のローカルファイルシステムアダプタ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/mime-type-detection">league/mime-type-detection</a>
    </td>
    <td>ライブラリ</td>
    <td>Flysystem の MIME タイプ検出</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/monolog"> 独白/独白 </a>
    </td>
    <td>ライブラリ</td>
    <td>ファイル、ソケット、受信ボックス、データベース、および様々な web サービスにログを送信します。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jmespath/jmespath.php">mtdowling/jmespath.php</a>
    </td>
    <td>ライブラリ</td>
    <td>JSON ドキュメントから要素を抽出する方法を宣言的に指定します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/constant_time_encoding">paragonie/constant_time_encoding</a>
    </td>
    <td>ライブラリ</td>
    <td>RFC 4648 エンコーディングの定時間実装（Base-64、Base-32、Base-16）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/random_compat">paragonie/random_compat</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP 5.x における random_bytes （）と random_int （）のポリフィルは PHP 7 から提供されています。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/emogrifier"> ペラゴ/顔文字 </a>
    </td>
    <td>ライブラリ</td>
    <td>CSS スタイルをHTML コードのインラインスタイル属性に変換します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/discovery">php-http/discovery</a>
    </td>
    <td>Composer-plugin</td>
    <td>PSR-7、PSR-17、PSR-18 および HTTPlug 実装を検索してインストールします</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/httplug">php-http/httplug</a>
    </td>
    <td>ライブラリ</td>
    <td>HTTPlug、PHP 用の HTTP クライアントの抽象化</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/promise">php-http/promise</a>
    </td>
    <td>ライブラリ</td>
    <td>非同期 HTTP 要求に使用するプロミス</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/CssXPath">phpgt/cssxpath</a>
    </td>
    <td>ライブラリ</td>
    <td>CSS セレクターを XPath クエリに変換します。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/Dom">phpgt/dom</a>
    </td>
    <td>ライブラリ</td>
    <td>最新の DOM API。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/PropFunc">phpgt/propfunc</a>
    </td>
    <td>ライブラリ</td>
    <td>プロパティのアクセサ関数とミューテータ関数。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/mcrypt_compat">phpseclib/mcrypt_compat</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP 5.x-8.x polyfill （mcrypt 拡張モジュール用）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/phpseclib">phpseclib/phpseclib</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP Secure Communications Library - RSA、AES、SSH2、SFTP、X.509 などの純粋な PHP 実装。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/cache">psr/cache</a>
    </td>
    <td>ライブラリ</td>
    <td>ライブラリをキャッシュするための共通インターフェイス</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/clock">psr/clock</a>
    </td>
    <td>ライブラリ</td>
    <td>クロックを読み取るための共通インターフェイス。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/container">psr/container</a>
    </td>
    <td>ライブラリ</td>
    <td>共通コンテナインタフェース （PHP FIG PSR-11）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/event-dispatcher">psr/event-dispatcher</a>
    </td>
    <td>ライブラリ</td>
    <td>イベント処理の標準インターフェイス。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-client">psr/http-client</a>
    </td>
    <td>ライブラリ</td>
    <td>HTTP クライアントの共通インターフェイス</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-factory">psr/http-factory</a>
    </td>
    <td>ライブラリ</td>
    <td>PSR-17:PSR-7 HTTP メッセージファクトリの共通インターフェイス</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-message">psr/http-message</a>
    </td>
    <td>ライブラリ</td>
    <td>HTTP メッセージの共通インターフェイス</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/log">psr/log</a>
    </td>
    <td>ライブラリ</td>
    <td>ライブラリをログに記録するための共通インターフェイス</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ralouphie/getallheaders">ralouphie/getallheaders</a>
    </td>
    <td>ライブラリ</td>
    <td>getallheaders のポリフィル。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/collection"> ラムジー/コレクション </a>
    </td>
    <td>ライブラリ</td>
    <td>コレクションを表現および操作するための PHP ライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/uuid"> ラムジー/uuid</a>
    </td>
    <td>ライブラリ</td>
    <td>ユニバーサル固有識別子（UUID）を生成し、操作するための PHP ライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/reactphp/promise">react/promise</a>
    </td>
    <td>ライブラリ</td>
    <td>CommonJS Promises/A for PHP の軽量実装</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/PHP-CSS-Parser">sabberworm/php-css-parser</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP で書かれた CSS ファイルのパーサ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/jsonlint">seld/jsonlint</a>
    </td>
    <td>ライブラリ</td>
    <td>JSON リンター</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/phar-utils">seld/phar-utils</a>
    </td>
    <td>ライブラリ</td>
    <td>PHAR ファイル形式ユーティリティ（PHP が起動した場合に使用）</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/signal-handler">seld/signal-handler</a>
    </td>
    <td>ライブラリ</td>
    <td>クロスプラットフォーム開発を容易にするためにシグナルがサポートされていない場合にサイレントに失敗するシンプルな Unix シグナルハンドラー</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/aes-key-wrap">spomky-labs/aes-key-wrap</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP 用の AES キーのラップ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/otphp">spomky-labs/otphp</a>
    </td>
    <td>ライブラリ</td>
    <td>RFC 4226 （HOTP アルゴリズム）および RFC 6238 （TOTP アルゴリズム）に従ってワンタイム パスワードを生成し、Google Authenticator と互換性のある PHP ライブラリ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/pki-framework">spomky-labs/pki-framework</a>
    </td>
    <td>ライブラリ</td>
    <td>公開鍵インフラストラクチャを管理するための PHP フレームワーク。 X.509 公開鍵証明書、属性証明書、証明書リクエストおよび証明書パス検証で構成されます。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/config">symfony/config</a>
    </td>
    <td>ライブラリ</td>
    <td>あらゆる種類の設定値を検索、読み込み、組み合わせ、自動入力および検証するのに役立ちます</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/console">symfony/console</a>
    </td>
    <td>ライブラリ</td>
    <td>美しくテスト可能なコマンドラインインターフェイスの作成が容易になります。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/css-selector">symfony/css-selector</a>
    </td>
    <td>ライブラリ</td>
    <td>CSS セレクターを XPath 式に変換</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/dependency-injection">symfony/dependency-injection</a>
    </td>
    <td>ライブラリ</td>
    <td>を使用すると、アプリケーションでのオブジェクトの作成方法を標準化および一元化できます</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/deprecation-contracts">symfony/deprecation-contracts</a>
    </td>
    <td>ライブラリ</td>
    <td>トリガー廃止通知の一般的な関数と規則</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/error-handler">symfony/error-handler</a>
    </td>
    <td>ライブラリ</td>
    <td>エラーを管理し、PHP コードのデバッグを容易にするツールを提供します。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher">symfony/event-dispatcher</a>
    </td>
    <td>ライブラリ</td>
    <td>は、イベントをディスパッチしてリッスンすることで、アプリケーションコンポーネントが相互に通信できるようにするツールを提供します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher-contracts">symfony/event-dispatcher-contracts</a>
    </td>
    <td>ライブラリ</td>
    <td>イベントのディスパッチに関連する一般的な抽象概念</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/filesystem">symfony/filesystem</a>
    </td>
    <td>ライブラリ</td>
    <td>ファイルシステムの基本的なユーティリティを提供します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/finder">symfony/finder</a>
    </td>
    <td>ライブラリ</td>
    <td>直感的な fluent インターフェイスを使用してファイルとディレクトリを検索します。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client">symfony/http-client</a>
    </td>
    <td>ライブラリ</td>
    <td>HTTP リソースを同期または非同期で取得する強力なメソッドを提供</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client-contracts">symfony/http-client-contracts</a>
    </td>
    <td>ライブラリ</td>
    <td>HTTP クライアントに関連する一般的な抽象概念</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-foundation">symfony/http-foundation</a>
    </td>
    <td>ライブラリ</td>
    <td>HTTP 仕様のオブジェクト指向レイヤーを定義します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-kernel">symfony/http-kernel</a>
    </td>
    <td>ライブラリ</td>
    <td>リクエストを応答に変換する構造化されたプロセスを提供します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/intl">symfony/intl</a>
    </td>
    <td>ライブラリ</td>
    <td>ICU ライブラリのローカリゼーションデータへのアクセスを提供します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mailer">symfony/mailer</a>
    </td>
    <td>ライブラリ</td>
    <td>メール送信に役立ちます</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mime">symfony/mime</a>
    </td>
    <td>ライブラリ</td>
    <td>MIME メッセージの操作を許可</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-ctype">symfony/polyfill-ctype</a>
    </td>
    <td>ライブラリ</td>
    <td>ctype 関数のシンボリックリポリ入力</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-grapheme">symfony/polyfill-intl-grapheme</a>
    </td>
    <td>ライブラリ</td>
    <td>intl の grapheme_*関数のシンフォニーポリフィル</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-idn">symfony/polyfill-intl-idn</a>
    </td>
    <td>ライブラリ</td>
    <td>intl の idn_to_ascii 関数と idn_to_utf8 関数に対するシンボリックリポリフィル</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-normalizer">symfony/polyfill-intl-normalizer</a>
    </td>
    <td>ライブラリ</td>
    <td>Intl の Normalizer クラスおよび関連する関数に対する Symfony polyfill</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-mbstring">symfony/polyfill-mbstring</a>
    </td>
    <td>ライブラリ</td>
    <td>Mbstring 拡張機能用のシンボリックポリフィル</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php73">symfony/polyfill-php73</a>
    </td>
    <td>ライブラリ</td>
    <td>Symfony polyfill は、PHP 7.3 以降の機能を下位の PHP バージョンにバックポートします。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php80">symfony/polyfill-php80</a>
    </td>
    <td>ライブラリ</td>
    <td>Symfony polyfill は、PHP 8.0 以降の機能を下位の PHP バージョンにバックポートします。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php81">symfony/polyfill-php81</a>
    </td>
    <td>ライブラリ</td>
    <td>Symfony polyfill は、PHP 8.1 以降の機能を下位の PHP バージョンにバックポートする</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php82">symfony/polyfill-php82</a>
    </td>
    <td>ライブラリ</td>
    <td>Symfony polyfill は、PHP 8.2 以降の機能を下位の PHP バージョンにバックポートする</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php83">symfony/polyfill-php83</a>
    </td>
    <td>ライブラリ</td>
    <td>Symfony polyfill は、PHP 8.3 以降の機能を下位の PHP バージョンにバックポートする</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/process">symfony/process</a>
    </td>
    <td>ライブラリ</td>
    <td>サブプロセスでコマンドを実行します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/service-contracts">symfony/service-contracts</a>
    </td>
    <td>ライブラリ</td>
    <td>サービスの記述に関連する一般的な抽象概念</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/string">symfony/string</a>
    </td>
    <td>ライブラリ</td>
    <td>文字列へのオブジェクト指向 API を提供し、バイト、UTF-8 コードポイントおよび grapheme クラスターを統一された方法で処理します</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-dumper">symfony/var-dumper</a>
    </td>
    <td>ライブラリ</td>
    <td>任意の PHP 変数を参照するためのメカニズムを提供します。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-exporter">symfony/var-exporter</a>
    </td>
    <td>ライブラリ</td>
    <td>シリアライズ可能な PHP データ構造をプレーンな PHP コードにエクスポートする</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/yaml">symfony/yaml</a>
    </td>
    <td>ライブラリ</td>
    <td>YAML ファイルの読み込みとダンプ</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/web-token/jwt-framework">web-token/jwt-framework</a>
    </td>
    <td>Symfony-bundle</td>
    <td>PHP および Symfony バンドル用の JSON オブジェクト署名および暗号化ライブラリ。</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webonyx/graphql-php">webonyx/graphql-php</a>
    </td>
    <td>ライブラリ</td>
    <td>GraphQL参照実装の PHP ポート</td>
  </tr>
  </tbody>
</table>

### OSL-3.0、AFL-3.0

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-customer-balance
    </td>
    <td>Magento2-module</td>
    <td>該当なし</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card
    </td>
    <td>Magento2-module</td>
    <td>該当なし</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card-account
    </td>
    <td>Magento2-module</td>
    <td>該当なし</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-wrapping
    </td>
    <td>Magento2-module</td>
    <td>該当なし</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-graph-ql
    </td>
    <td>Magento2-module</td>
    <td>該当なし</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-reward
    </td>
    <td>Magento2-module</td>
    <td>該当なし</td>
  </tr>
  </tbody>
</table>

### OSL-3.0

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### PHP

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/2tvenom/CBOREncode">2tvenom/cborencode</a>
    </td>
    <td>ライブラリ</td>
    <td>PHP 用 CBOR エンコーダ</td>
  </tr>
  </tbody>
</table>

### 独自の

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### 専有

<table>
  <thead>
    <tr>
      <th>名前</th>
      <th>タイプ</th>
      <th>説明</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-core
    </td>
    <td>Magento2-module</td>
    <td>Magento Braintree 2.2.0 モジュールから PayPal 用に Gene Commerceでフォークします。</td>
  </tr>
  </tbody>
</table>
