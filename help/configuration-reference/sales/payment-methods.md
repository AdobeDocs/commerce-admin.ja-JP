---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] ページで設定を確認します。
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Adobe CommerceおよびMagento Open Source向け支払いサービスは、堅牢で安全な支払い処理を実現するために、サンドボックステストやシンプルなセットアップなどのターンキーセルフサービスソリューションを提供します。 この強力なツールセットの詳細と、購入者にとって最適なエクスペリエンスを実現するために必要なinsightと制御を提供する方法については、[_支払いサービスユーザーガイド_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html) を参照してください。

{{config}}

## [!UICONTROL Merchant Location]

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

![ 販売者の所在地 ](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/en/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Web サイト | 営業を行うために商人が登録されている国を識別します。 |

{style="table-layout:auto"}

## 推奨されるソリューション

PayPal アカウントまたはクレジットカードによるオンライン支払いを始めたばかりのマーチャントにとって、以下の支払いソリューションは簡単な方法としてお勧めします。 ビジネスが成長するにつれて、これらを追加の PayPal 支払いソリューションと組み合わせることができます。

- [支払いサービス](payment-services.md)
- [!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"} [PayPal Express Checkout](paypal-express-checkout.md)
- [!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"} [Braintree](braintree.md)

>[!NOTE]
>
>一部の支払い統合およびバンドルされた拡張機能は、2.4.x リリースで削除され、Commerce Marketplaceに移行されました。 最新の公式の支払い統合拡張機能については、[Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"} を参照してください。
><br/>
>**Amazon Pay** および **Klarna**:Adobe CommerceおよびMagento Open Source リリース 2.4.0 から 2.4.3 には、これらのベンダーが開発した拡張機能が含まれています。 2.4.4 リリース以降、これらの拡張機能はコアリリースにバンドルされなくなり、Commerce Marketplaceからインストールして更新する必要があります。 また、Marketplace では、拡張機能開発者が提供する最新のドキュメントにもアクセスできます。
><br/>
>これらのバンドルされた拡張機能のいずれかが有効になって設定済みの場合は、2.4.4 アップグレードプロセスの一環として `composer.json` ファイルを更新し、今後、拡張機能の更新を管理する必要があります。 詳しくは、『 [ アップグレードガイド _の ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) アップグレードモジュール_ を参照してください。<br/>
><br/>
>**Worldpay**、**Eway**、**CyberSource**、および **Authorize.Net**：これらの支払い統合から安全に移行する方法については、[DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"} を参照してください。

## その他の PayPal メソッド

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

PayPal は、あらゆる規模の企業のニーズに対応し、世界中でビジネスに従事している様々な支払いソリューションを提供しています。 PayPal は、すべての主要なデビットカードとクレジットカードから支払いを受け入れる機能を提供します。 PayPal アカウントをお持ちでないお客様でも PayPal で購入の支払いが可能であるため、PayPal は追加の手間をかけずに利便性を高めます。

### PayPal オールインワンメソッド

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

- [PayPal 支払い詳細](paypal-payments-advanced.md)
- [PayPal ペイメントプロ](paypal-payments-pro.md)
- [PayPal 支払い標準](paypal-payments-standard.md)

### PayPal 支払いゲートウェイ

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

- [PayPal Payflow Pro](paypal-payflow-pro.md) （高速チェックアウトを含む）
- [PayPal ペイフローリンク ](paypal-payflow-link.md) （高速チェックアウトを含む）

## 基本的な支払い方法

次の支払い方法はCommerceに組み込まれており、サードパーティの支払いプロバイダーを使用して取引を処理することはありません。 基本的な支払い方法の多くは、オンラインではなくオフラインで管理されています。

### [!UICONTROL Check / Money Order]

![ 小切手/送金 ](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 顧客が小切手または送金で支払うことができるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示されるこの支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 小切手またはマネーオーダーによって支払われた注文に割り当てられる最初の [ 注文ステータス ](../../stores-purchase/order-status.md) を決定します。 デフォルト値：`Pending` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 小切手またはマネーオーダーによる支払いを受け入れる国を決定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 小切手またはマネーオーダーによる支払いを受け入れる特定の国を識別します。 |
| [!UICONTROL Make Check Payable to] | ストア表示 | 小切手および為替を支払う必要があるエンティティの名前。 |
| [!UICONTROL Send Check to] | ストア表示 | 小切手および送金が送信される住所または私書箱。 |
| [!UICONTROL Minimum Order Total] | Web サイト | 小切手またはマネーオーダーで支払うことができる最小の注文金額。 |
| [!UICONTROL Maximum Order Total] | Web サイト | 小切手またはマネーオーダーで支払うことができる最大の注文金額。 <br/><br/>**_注意：_**&#x200B;注文は、合計が最小注文合計と最大注文合計の間にあるか、合計と一致するかを検証します。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法でリストされたときに、小切手または送金による支払いが表示される順序を決定する数値です。 `0` と入力して、リストの先頭に配置します。 |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![ 振替支払 ](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 顧客が支払いを銀行から販売者の口座に直接送金して支払うことができるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示されるこの支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 銀行振込で支払われた注文に割り当てられた最初の注文ステータスを決定します。 デフォルト値：`Pending` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 銀行振込による支払いを受け入れる国を決定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 銀行振込による支払いを受け入れる特定の国を識別します。 |
| [!UICONTROL Minimum Order Total] | Web サイト | 銀行振込で支払うことができる最小の注文金額。 |
| [!UICONTROL Maximum Order Total] | Web サイト | 銀行振込で支払うことができる最大の注文金額。 <br/><br/>**_注意：_**&#x200B;注文は、合計が最小注文合計と最大注文合計の間にあるか、合計と一致するかを検証します。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法でリストされた場合に、銀行振込による支払いが表示される順序を決定する数値です。 `0` と入力して、リストの先頭に配置します。 |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![ 分割払 ](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 会社が会社クレジットを使用して購入できるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示されるこの支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 会社アカウントに請求される新規注文のステータスを決定します。 オプション：`Pending (default)`/`Processing`/`Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 会社がアカウントに購入を請求できる国を決定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 企業がアカウントに購入を請求できる特定の国を識別します。 |
| [!UICONTROL Minimum Order Total] | Web サイト | 会社の口座に請求できる最小の注文金額を指定します。 |
| [!UICONTROL Maximum Order Total] | Web サイト | 会社の口座に請求できる最大注文金額。 <br/><br/>**_注意：_**&#x200B;注文は、合計が最小注文合計と最大注文合計の間にあるか、合計と一致するかを検証します。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法と一緒にリストされた場合に、分割払いが表示される順序を決定する数値です。 `0` と入力して、リストの先頭に配置します。 |

{style="table-layout:auto"}

>[!NOTE]
>
>[ 複数の配送先住所 ](../../stores-purchase/shipping-settings.md#multiple-addresses) を含む注文については、アカウントでのお支払いはサポートされておらず、お支払いオプションには表示されません。

### [!UICONTROL Cash On Delivery Payment]

![ 代金交付金 ](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 顧客が支払いを銀行から販売者の口座に直接送金して支払うことができるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示されるこの支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | 銀行振込で支払われた注文に割り当てられた最初の注文ステータスを決定します。 デフォルト値：`Pending` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 銀行振込による支払いを受け入れる国を決定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 銀行振込による支払いを受け入れる特定の国を識別します。 |
| [!UICONTROL Minimum Order Total] | Web サイト | 銀行振込で支払うことができる最小の注文金額を指定します。 |
| [!UICONTROL Maximum Order Total] | Web サイト | 銀行振込で支払うことができる最大の注文金額。 <br/><br/>**_注意：_**&#x200B;注文は、合計が最小注文合計と最大注文合計の間にあるか、合計と一致するかを検証します。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法でリストされた場合に、銀行振込による支払いが表示される順序を決定する数値です。 `0` と入力して、リストの先頭に配置します。 |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![ 小計ゼロのチェックアウト ](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストア表示 | チェックアウト時にこの支払い方法に使用される名前。 デフォルト値：支払情報は不要 |
| [!UICONTROL Enabled] | Web サイト | 小計ゼロの小計チェックアウトを店舗管理者が使用できるかどうかを決定します。小計ゼロの注文（課税済みの注文など）を管理できますが、割引によって金額がゼロに減らされています。 オプション：`Yes` / `No` |
| [!UICONTROL New Order Status] | Web サイト | ゼロ小計チェックアウトとして処理された注文に割り当てられた最初の注文ステータスを決定します。 デフォルト値：`Pending` |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | ゼロ小計チェックアウトを適用できる国を決定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | ゼロ小計チェックアウトを適用できる特定の国を識別します。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法と一緒にリストされた場合に、「支払い情報が必要ありません」などのタイトルが表示される順序を決定する数値です。 `0` と入力して、リストの先頭に配置します。 |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

支払いアクションは _支払い方法ごとに_ 設定されます。 支払処理では、資金が取得される時期と、受注に対する請求書が作成される時期が決定されます。

個々の設定オプションの包括的なリストについては、個々の支払い方法のトピックの基本設定の節を参照してください。

| 支払いアクション | 説明 |
|--- |---|
| [!UICONTROL Authorization] | 購入を承認しますが、資金を保留します。 この金額は、商人によってキャプチャされるまで引き出されません。 |
| [!UICONTROL Authorize] | 注文合計に対する購入者の口座を承認しますが、支払いはキャプチャしません。 請求書を作成して支払をキャプチャします。 許可された注文は無効またはキャンセルできます。 |
| [!UICONTROL Authorize and Capture] | 注文合計に対する購入者の口座を承認し、支払いをキャプチャします。 請求書が自動的に作成されます。 取得した資金は、クレジット・メモを使用して払い戻すことができます。 支払いがキャプチャされた後は、注文をキャンセルすることはできません。 |
| [!UICONTROL Charge on shipment] | Amazonは、Commerceで請求書を作成すると、取得リクエストを受け取り、顧客に請求します。 |
| [!UICONTROL Charge on order] | Amazonによって請求書が作成され、注文の際に顧客に請求されます。 |
| [!UICONTROL Not Capture] | 請求書が送信されると、システムは支払をキャプチャしません。 後でCommerceを通じて支払いをキャプチャすることを想定しています。 完了した請求書に「Capture」（キャプチャ）ボタンが表示されます。 キャプチャする前に、請求書をキャンセルできます。 取得後、クレジット・メモを作成し、請求書を無効にできます。 |
| [!UICONTROL Order] | PayPal との契約を表します。これにより、マーチャントは、定義された期間（最大 29 日）内に、顧客のバイヤーアカウントから注文合計までの 1 つ以上の金額を取得できます。 |
| [!UICONTROL Sale] | 購入金額は承認され、すぐにお客様のアカウントから引き出されます。 |

{style="table-layout:auto"}

>[!NOTE]
>
>後でCommerceを通じて支払いをキャプチャすることが確実でない限り、「_[!UICONTROL Not Capture]_」オプションを選択しないでください。 「取得」ボタンを使用して支払を取得するまでは、クレジット・メモを作成できません。

## [!UICONTROL Purchase Order]

![ 注文書 ](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 顧客が発注書（PO）で支払うことができるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に表示されるこの支払い方法の名前。 |
| [!UICONTROL New Order Status] | Web サイト | PO によって支払われた注文に割り当てられる最初の [ 注文ステータス ](../../stores-purchase/order-status.md) を決定します。 デフォルト値：保留中 |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | 発注による支払を受け入れる国を決定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 発注による支払を受け入れる特定の国を識別します。 |
| [!UICONTROL Minimum Order Total] | Web サイト | PO で支払うことができる最小の注文金額。 |
| [!UICONTROL Maximum Order Total] | Web サイト | PO で支払うことができる最大注文金額。 <br/><br/>**_注意：_**&#x200B;注文は、合計が最小注文合計と最大注文合計の間にあるか、合計と一致するかを検証します。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法と一緒にリストされたときに発注による支払いが表示される順序を決定する数値です。 `0` と入力して、リストの先頭に配置します。 |

{style="table-layout:auto"}
