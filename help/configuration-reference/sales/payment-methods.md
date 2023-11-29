---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: 次のページで設定を確認します： [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] コマース管理のページ。
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Adobe CommerceおよびMagento Open Source向けの支払いサービスは、堅牢で安全な支払い処理を提供するために、サンドボックステストや簡単な設定を含む自動セルフサービスソリューションを提供します。 この強力なツールセットと、購入者に最適なエクスペリエンスを作成するために必要なインサイトと制御を提供する方法について詳しくは、 [_支払サービスユーザーガイド_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

![商社の場所](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://docs.magento.com/user-guide/payment/merchant-location.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Web サイト | 商人がビジネスを行うために登録されている国を識別します。 |

{style="table-layout:auto"}

## 推奨されるソリューション

PayPal アカウントまたはクレジットカードによるオンライン支払いを受け入れ始めた商人には、以下の支払いソリューションを簡単な方法としてお勧めします。 ビジネスが成長するにつれ、これらを追加の PayPal 支払いソリューションと組み合わせることができます。

- [PayPal Express チェックアウト](paypal-express-checkout.md)
- [Braintree](braintree.md)
- [支払いサービス](payment-services.md)

>[!NOTE]
>
>一部の支払い統合とバンドルされた拡張機能は、2.4.x リリースで削除され、Commerce Marketplaceに移行しました。 最新の正式な支払い統合の拡張については、 [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}。
><br/>
>**Amazon Pay** および **クラルナ**:Adobe CommerceおよびMagento Open Sourceリリース 2.4.0 ～ 2.4.3 には、これらのベンダー開発の拡張機能が含まれていました。 2.4.4 リリース以降、これらの拡張機能はコアリリースにバンドルされなくなり、Commerce Marketplaceからインストールおよび更新する必要があります。 また、Marketplace では、拡張機能の開発者が提供する最新のドキュメントにアクセスできます。
><br/>
>これらのバンドルされた拡張機能のいずれかを有効にして設定済みの場合は、 `composer.json` ファイルを作成し、今後の拡張機能の更新を管理するための手順を説明します。 詳しくは、 [モジュールのアップグレード](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) （内） _アップグレードガイド_ を参照してください。<br/>
><br/>
>**Worldpay**, **エウェイ**, **CyberSource**、および **Authorize.Net**：これらの支払い統合からの安全な移行について詳しくは、 [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}。

## その他の PayPal メソッド

PayPal は、あらゆる規模のビジネスのニーズを満たし、世界中のビジネスに関わる様々な支払いソリューションを提供します。 PayPal は、すべての主要なデビットカードとクレジットカードから支払いを受け入れる機能を提供します。 PayPal アカウントを持っていない顧客でも PayPal での購入に対して支払うことができるので、PayPal は余分な手間をかけずに追加の利便性を提供します。

### PayPal のオールインワン方式

- [PayPal 支払いの詳細](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal 支払い標準](paypal-payments-standard.md)

### PayPal 支払いゲートウェイ

- [PayPal Payflow Pro](paypal-payflow-pro.md) （速達チェックアウトを含む）
- [PayPal ペイフローリンク](paypal-payflow-link.md) （速達チェックアウトを含む）

## 基本的な支払い方法

次の支払い方法は、Commerce に組み込まれており、サードパーティの支払いプロバイダーを使用してトランザクションを処理しません。 基本的な支払い方法の多くは、オンラインではなく、オフラインで管理されています。

### [!UICONTROL Check / Money Order]

![小切手/通貨注文](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://docs.magento.com/user-guide/payment/check-money-order.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 顧客が小切手または送金で支払えるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示される、この支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 初期値を決定 [注文ステータス](../../stores-purchase/order-status.md) 小切手または通貨注文で支払われた注文に割り当てられます。 デフォルト値： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 小切手または送金で支払いを受け入れる国を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 小切手または送金で支払いを受け入れる国を特定します。 |
| [!UICONTROL Make Check Payable to] | ストア表示 | 小切手と注文を支払うエンティティの名前。 |
| [!UICONTROL Send Check to] | ストア表示 | 小切手と送金を送信する必要がある番地または発注書箱。 |
| [!UICONTROL Minimum Order Total] | Web サイト | 小切手または送金で支払える最小の注文額。 |
| [!UICONTROL Maximum Order Total] | Web サイト | 小切手または送金で支払うことができる最大の注文額。 <br/><br/>**_注意：_**合計が最小または最大の注文合計の間にあるか、一致する場合に、注文が評価されます。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法と共にリストされた場合に、小切手または送金による支払いが表示される順序を決定する数値。 入力 `0` をクリックして、リストの一番上に配置します。 |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![銀行振替支払](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://docs.magento.com/user-guide/payment/bank-transfer.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 顧客が銀行からお客様のマーチャントアカウントに直接支払いを移行することで、お客様が支払いを行えるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示される、この支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 銀行振替で支払われた注文に割り当てられる初期注文ステータスを決定します。 デフォルト値： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 銀行振込による支払いを受け入れる国を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 銀行振込による支払いを受け入れる国を特定します。 |
| [!UICONTROL Minimum Order Total] | Web サイト | 銀行振替で支払える最小注文額。 |
| [!UICONTROL Maximum Order Total] | Web サイト | 銀行振替で支払える最大注文額。 <br/><br/>**_注意：_**合計が最小または最大の注文合計の間にあるか、一致する場合に、注文が評価されます。 |
| [!UICONTROL Sort Order] | Web サイト | 銀行振替による支払が、チェックアウト時に他の支払方法と共にリストされた場合に表示される順序を決定する数値。 入力 `0` をクリックして、リストの一番上に配置します。 |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![アカウントでの支払い](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://docs.magento.com/user-guide/payment/payment-on-account.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 会社が会社のクレジットを使用して購入を行えるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示される、この支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 会社アカウントに請求された新規注文のステータスを決定します。 オプション： `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 会社が自分のアカウントに対して購入を請求できる国を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 会社が自分のアカウントに対して購入を請求できる国を特定します。 |
| [!UICONTROL Minimum Order Total] | Web サイト | 会社アカウントに請求できる最小の注文額を指定します。 |
| [!UICONTROL Maximum Order Total] | Web サイト | 会社アカウントに請求できる最大の注文額。 <br/><br/>**_注意：_**合計が最小または最大の注文合計の間にあるか、一致する場合に、注文が評価されます。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法と共に一覧表示された場合に、勘定で支払が表示される順序を決定する数値。 入力 `0` をクリックして、リストの一番上に配置します。 |

{style="table-layout:auto"}

>[!NOTE]
>
>アカウントでの支払いは、次の条件を持つ注文ではサポートされていません： [複数の配送先住所](../../stores-purchase/shipping-settings.md#multiple-addresses) とは、支払いオプションには表示されません。

### [!UICONTROL Cash On Delivery Payment]

![現金引渡支払](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 顧客が銀行からお客様のマーチャントアカウントに直接支払いを移行することで、お客様が支払いを行えるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示される、この支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 銀行振替で支払われた注文に割り当てられる初期注文ステータスを決定します。 デフォルト値： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 銀行振込による支払いを受け入れる国を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 銀行振込による支払いを受け入れる国を特定します。 |
| [!UICONTROL Minimum Order Total] | Web サイト | 銀行振替で支払える最小注文額を指定します。 |
| [!UICONTROL Maximum Order Total] | Web サイト | 銀行振替で支払える最大注文額。 <br/><br/>**_注意：_**合計が最小または最大の注文合計の間にあるか、一致する場合に、注文が評価されます。 |
| [!UICONTROL Sort Order] | Web サイト | 銀行振替による支払が、チェックアウト時に他の支払方法と共にリストされた場合に表示される順序を決定する数値。 入力 `0` をクリックして、リストの一番上に配置します。 |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![小計ゼロのチェックアウト](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストア表示 | チェックアウト時にこの支払い方法に使用される名前。 デフォルト値：支払情報は不要 |
| [!UICONTROL Enabled] | Web サイト | 店舗管理者が、課税済みの注文など、小計がゼロの注文を管理できるかどうかを決定します。ただし、割引は、金額をゼロに減らしました。 オプション： `Yes` / `No` |
| [!UICONTROL New Order Status] | Web サイト | 「小計チェックアウトなし」で処理された受注に割り当てられる初期受注ステータスを決定します。 デフォルト値： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | ゼロ小計チェックアウトを適用できる国を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | ゼロ小計チェックアウトを適用できる特定の国を識別します。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法と共に表示される場合に、タイトル（「支払い情報は不要です」など）が表示される順序を決定する数値です。 入力 `0` をクリックして、リストの一番上に配置します。 |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

支払いアクションが設定されています _支払方法ごと_. 支払い処理は、資金が取り込まれるタイミングと、販売注文に対して請求書が作成されるタイミングを決定します。

個々の設定オプションの包括的なリストについては、各支払い方法のトピックの「基本設定」の節を参照してください。

| 支払いアクション | 説明 |
|--- |---|
| [!UICONTROL Authorization] | 購入を承認しますが、資金を保留します。 金額は商人が取り込むまで引き落とされない。 |
| [!UICONTROL Authorize] | 注文の合計に対する購入者のアカウントを許可しますが、支払いは取り込まれません。 請求書を作成して支払をキャプチャします。 認証済みのオーダーを無効またはキャンセルできます。 |
| [!UICONTROL Authorize and Capture] | 注文の合計に対する購入者のアカウントを承認し、支払いをキャプチャします。 請求書が自動的に作成されます。 クレジットメモを使用して、取り込んだ資金を返金できます。 支払がキャプチャされた後は注文をキャンセルできません。 |
| [!UICONTROL Charge on shipment] | Amazonは、Commerce で請求書が作成されたときに取得要求を受け取り、顧客に請求します。 |
| [!UICONTROL Charge on order] | Amazonは請求書を作成し、注文が行われたときに顧客に請求します。 |
| [!UICONTROL Not Capture] | 請求書が発行されると、システムは支払をキャプチャしません。 後でコマースを通じて支払いをキャプチャすると想定されます。 完了した請求書には「取得」ボタンが表示されます。 取り込む前に、請求書を取り消すことができます。 取得後、クレジットメモを作成し、請求書を無効にすることができます。 |
| [!UICONTROL Order] | 定義された期間（最大 29 日）内に、マーチャントが顧客の購入者アカウントから 1 つ以上の注文の合計を取得できるようにする PayPal との契約を表します。 |
| [!UICONTROL Sale] | 購入金額は、承認され、顧客のアカウントから直ちに取り下げられます。 |

{style="table-layout:auto"}

>[!NOTE]
>
>次を選択しないでください： _[!UICONTROL Not Capture]_オプションを使用できます。 「取得」ボタンを使用して支払が取り込まれるまで、クレジット・メモを作成できません。

## [!UICONTROL Purchase Order]

![発注書](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 顧客が発注 (PO) で支払えるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示される、この支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 初期値を決定 [注文ステータス](../../stores-purchase/order-status.md) 発注によって支払われた注文に割り当てられました。 デフォルト値：保留 |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | PO による支払いを受け入れる国を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | PO による支払いを受け入れる国を特定します。 |
| [!UICONTROL Minimum Order Total] | Web サイト | PO が支払える最小の注文額。 |
| [!UICONTROL Maximum Order Total] | Web サイト | PO が支払える最大注文額。 <br/><br/>**_注意：_**合計が最小または最大の注文合計の間にあるか、一致する場合に、注文が評価されます。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払方法と共にリストされた場合に、発注による支払が表示される順序を決定する数値。 入力 `0` をクリックして、リストの一番上に配置します。 |

{style="table-layout:auto"}
