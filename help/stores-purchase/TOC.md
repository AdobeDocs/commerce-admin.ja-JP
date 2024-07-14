---
user-guide-title: 店舗および購入エクスペリエンスガイド
user-guide-description: Adobe CommerceおよびMagento Open Sourceで作業するサイト管理者、カスタマーサービスエージェント、およびセールスマネージャーを対象とした包括的な情報です。
breadcrumb-title: 店舗と購入エクスペリエンス
role: Admin, User
feature: Storefront
recommendations: noDisplay
source-git-commit: 2bf5b95b89439196f9db4af0908ff27434472df8
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 3%

---


# 店舗および購入エクスペリエンスガイド {#stores-sales}

+ [店舗および購入エクスペリエンスガイド](guide-overview.md)
+ [ストアと購入体験の概要](introduction.md)
+ サイトおよびストアの管理 {#site-store}
   + [ストアメニュー](stores-menu.md)
   + [ストアとサイトの構造](stores.md)
   + [ビューを保存](store-views.md)
   + [ストアのローカリゼーション](store-localize.md)
   + [URL を格納](store-urls.md)
   + 税 {#taxes}
      + [概要](taxes.md)
      + [税の構成設定](tax-settings-general.md)
      + [価格の表示設定](display-settings.md)
      + [税務処理基準](tax-rules.md)
      + [税クラス](tax-class.md)
      + [固定製品税](fixed-product-tax.md)
      + [非表示の税計算](hidden-tax-calculation.md)
      + [税ゾーンと税率](tax-zones-rates.md)
      + [付加価値税（VAT）](vat.md)
      + [国別の税金ガイドライン](international-tax-guidelines.md)
   + 通貨 {#currency}
      + [概要](currency.md)
      + [通貨の設定](currency-configuration.md)
      + [通貨レートを更新](currency-update.md)
   + [販売メール](sales-email.md)
   + [販売ドキュメント](sales-documents.md)
+ POI （購入 {#point-of-purchase}）
   + [即時購入](checkout-instant-purchase.md)
   + 買い物かご {#cart}
      + [概要](cart.md)
      + [買い物かご設定](cart-configuration.md)
      + [買い物かごの永続性](cart-persistent.md)
      + [SKU で並べ替え](order-by-sku.md)
   + 買い物支援 {#assist}
      + [買い物かごの管理](shopping-assisted-cart-manage.md)
      + [オーダーの作成](customer-account-create-order.md)
      + [顧客注文の更新](order-update.md)
   + チェックアウト {#checkout}
      + [概要](checkout-process.md)
      + [1 ページのチェックアウト](checkout-one-page.md)
      + [ゲストのチェックアウト](checkout-guest.md)
      + [利用条件](terms-and-conditions.md)
      + [アドレス検索](checkout-address-search.md)
      + [支払い失敗通知](checkout-payment-failed-emails.md)
      + [チェックアウト合計の並べ替え順序](checkout-totals-sort-order.md)
   + ギフト カード {#gift-cards}
      + [ギフト カードの購入と引き換え](product-gift-card-workflow.md)
      + [ギフト カード アカウント](product-gift-card-accounts.md)
+ 買い物客ツール {#shopper-tools}
   + [友達にメールを送信](email-a-friend.md)
   + 欲しい物のリスト {#wish-lists}
      + [概要](wishlists.md)
      + [ウィッシュリストの設定](wishlist-configuration.md)
      + [ウィッシュリストのストアフロントの経験](wishlist-storefront.md)
   + [製品の比較](product-compare.md)
   + [最近表示または比較](products-viewed-compared.md)
   + [並べ替えを許可](reorders-allow.md)
   + [注文のキャンセルを許可](cancel-allow.md)
+ 支払い {#payments}
   + [概要](payments.md)
   + PayPal 支払いソリューション {#paypal}
      + [PayPal ソリューションの概要](paypal.md)
      + [PayPal Express チェックアウト](paypal-express-checkout.md)
      + [PayPal 支払い詳細](paypal-payments-advanced.md)
      + [PayPal ペイメントプロ](paypal-payments-pro.md)
      + [PayPal 支払い標準](paypal-payments-standard.md)
      + [PayPal Payflow Pro](paypal-payflow-pro.md)
      + [PayPal ペイフローリンク](paypal-payflow-link.md)
      + [PayPal 請求契約](paypal-billing-agreements.md)
      + [PayPal 決済レポート](paypal-settlement-reports.md)
   + [Braintree](braintree.md)
   + [保存されている支払い方法](stored-payment-methods.md)
   + オフライン支払方法 {#offline}
      + [小切手注文とマネーオーダー](check-money-order.md)
      + [代金引換払い](cash-on-delivery.md)
      + [銀行振込](bank-transfer.md)
      + [発注書](purchase-order.md)
      + [小計ゼロのチェックアウト](zero-subtotal-checkout.md)
+ 注文フロー {#order-management} の管理
   + [販売メニュー](sales-menu.md)
   + 受注 {#orders}
      + [概要](orders.md)
      + [ワークフローと処理](order-processing.md)
      + [注文の発送](order-ship.md)
      + [注文ステータス](order-status.md)
      + [スケジュール済み注文操作](order-scheduled-operations.md)
      + [注文のアーカイブ](order-archive.md)
      + [ストアフロントの注文管理](orders-storefront.md)
   + [請求書](invoices.md)
   + [出荷](shipments.md)
   + クレジットメモ {#credit-memos}
      + [概要](credit-memos.md)
      + [クレジットメモを発行する](credit-memo-create.md)
   + {#returns} を返します
      + [概要](returns.md)
      + [戻り値の設定](rma-configure.md)
      + [属性を返す](attributes-returns.md)
      + [ストアフロントのエクスペリエンスを返します](rma-customer-experience.md)
   + [トランザクション](transactions.md)
+ 配信 {#delivery}
   + [概要](delivery.md)
   + [発送設定](shipping-settings.md)
   + の基本的な配信方法 {#basic-methods}
      + [送料無料](shipping-free.md)
      + [定額料金](shipping-flat-rate.md)
      + [テーブル率](shipping-table-rate.md)
      + [店舗での配信](shipping-in-store-delivery.md)
   + 配送業者 {#shipping-carriers}
      + [配送業者の設定](carriers.md)
      + [UPS](ups.md)
      + [USPS](usps.md)
      + [FedEx](fedex.md)
      + [DHL](dhl.md)
   + 配送ラベル {#shipping-labels}
      + [出荷ラベルの概要](shipping-labels.md)
      + [配送ラベルの設定](shipping-label-configure.md)
      + [配送ラベルの作成](shipping-label-create.md)
+ [ マーチャントガイドに戻る ](https://experienceleague.adobe.com/en/docs/commerce-admin/user-guides/home)

