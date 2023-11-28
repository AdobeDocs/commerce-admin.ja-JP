---
title: PayPal の支払いソリューション
description: お客様のストアで利用可能な PayPal 支払いソリューションの統合について説明します。
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# PayPal の支払いソリューション

PayPal は、オンラインでの支払いにおける世界的なリーダーであり、顧客がオンラインで支払う迅速で安全な方法です。 利用可能な PayPal ソリューションの選択は、マーチャントの所在地によって異なります。 PayPal Express Checkout と PayPal Payments Standard は、世界中の全ての地域で使用できます。 詳しくは、 [PayPal ソリューション（国別）](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日以降、ヨーロッパの銀行は、満たさない支払いを辞退する場合があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件。 ほとんどの PayPal ソリューションでは、PSD2 に準拠するためのアクションは必要ありません。これらの要件は PayPal で処理されるからです。

## PayPal ビジネスアカウント

お客様のストアで PayPal を支払い方法として提供するには、PayPal が必要です [ビジネスアカウント][1] および/または a [PayPal Payflow アカウント][2]. アカウント要件は、各 PayPal ソリューションの説明に記載されています。 PayPal マーチャントアカウントは、 [詐欺フィルター](#paypal-fraud-management-filters) これは、お客様のストアで行われた購入に適用されます。

PayPal Express Checkout または Payflow Pro の Express Checkout を使用するお客様は、PayPal の購入者アカウントを持っている必要があります。 PayPal 支払い基準（一部の国では Web サイト支払い基準）は、商人が有効にする場合に、直接または購入者アカウントを通じて使用できます _PayPal アカウントオプション_. デフォルトでは、このパラメーターは有効になっており、顧客がクレジットカード情報の入力や PayPal での購入者アカウントの作成を選択できます。 無効にした場合、顧客はまず PayPal の購入者アカウントを作成してから購入する必要があります。

Website Payments Pro、Website Payments Pro Payflow Edition、Payflow Pro Gateway、Payflow Link は、お客様がチェックアウト時にクレジットカード情報を入力する必要があります。

## PayPal クレジットと PayLater

PayPal PayLater は、お客様に対して迅速な資金調達を提供し、お客様が今すぐ購入し、時間とともに、追加費用なしで支払うことができます。 お客様が PayPal クレジットオプションを選択した場合、課金されず、通常の PayPal 取引料のみを支払います。 詳しくは、 [PayPal Web サイト][3].

資金調達を宣伝する際に、セールスを押し上げます。 PayPal は、PayPal PayLater を使用した資金調達でブラウザーを購入者に変えるのに役立ちます。 お客様は時間の経過と共に、前払いを受ける一方で、追加費用はかかりません。 PayPal の無料バナー広告を使用して、顧客が PayPal でチェックアウトする際に、支払いオプションとして PayPal の融資を宣伝します。 PayPal Advertising Program は、追加購入を生成し、平均購入サイズを 15%以上増やすことを示しています。

サイトのページや _PayPal クレジット_ ボタンをクリックして、顧客に対してすぐにファイナンスを提供できることを通知します。

>[!NOTE]
>
>2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能を使用すると、買い物客は購入時に全額を支払う代わりに、隔週の分割払いで注文に対して支払うことができます。 PayPal Credit エクスペリエンスは廃止されました。

米国の商人の場合、PayPal クレジットはデフォルトで [PayPal Express チェックアウト](paypal-express-checkout.md) 支払いオプション。 この支払い方法に対して無効にするには、 _機能_ のセクション [PayPal Express チェックアウト設定](paypal-express-checkout.md#features).

PayPal クレジットは、他の PayPal 支払いソリューションではデフォルトで無効になっていますが、次のソリューションをサポートする支払い方法の設定で有効にすることができます。

- [支払いの詳細](paypal-payments-advanced.md)
- [Payments Pro](paypal-payments-pro.md)
- [支払い標準](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [ペイフローリンク](paypal-payflow-link.md)

>[!IMPORTANT]
>
>ストアに PayPal Credit または PayPal PayLater を設定する前に、PayPal マーチャントアカウントで有効になっていることを確認してください。

## 統合 PayPal ソリューション

PayPal とAdobe Commerceでは、すべての主要なデビットカードとクレジットカードから支払いを受け付けることができます。 PayPal アカウントを持っていないお客様でも、PayPal での購入に対して支払うことができるので、PayPal は余分な手間をかけずに追加の利便性を提供します。

>[!NOTE]
>
>PayPal Express Checkout を除き、一度に複数の PayPal メソッドをストアで有効にすることはできません。 PayPal Express Checkout は、PayPal Payments Standard 以外の他の PayPal 支払い方法で使用できます。 支払い方法を変更すると、以前の方法は無効になります。

### PayPal Express チェックアウト

[PayPal Express チェックアウト](paypal-express-checkout.md)

### PayPal のオールインワン決済ソリューション

米国では、PayPal は、成長するビジネスのニーズに合わせて、次の PCI 準拠のソリューションを提供しています。

- [PayPal 支払いの詳細](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal 支払い標準](paypal-payments-standard.md)

![PayPal のオールインワン決済ソリューション](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### PayPal 支払いゲートウェイ

支払いゲートウェイは、e コマースアプリケーションサービスプロバイダーが提供するマーチャントサービスで、クレジットカードや直接支払い処理を許可します。 顧客と銀行との間の仲介業を行っています。

支払いゲートウェイは、オンライン環境とオフライン環境で使用できます。 支払いは、電話、オンライン、またはモバイルアプリで受け入れることができます。 トランザクションは、サービスプロバイダーの処理システムに送信され、確認と確認のために顧客の銀行に送信されます。 確認された場合、商人は顧客の銀行口座と直接連絡を取ることなく支払を受け取ります。

支払いゲートウェイには、直接とホストの 2 種類があります。

- 直接支払いゲートウェイを使用すると、ユーザーは店舗の Web サイトにカードの詳細を入力できます。
- ホスト型支払いゲートウェイは、ユーザーを、店舗の Web サイトの外部にあるホスト型支払いページにリダイレクトします。

支払いゲートウェイは、トランザクションに関わるすべての関係者に対してセキュリティと保護を提供します。

PayPal は、お客様のビジネスに対して 2 つの支払いゲートウェイソリューションを提供します。 PayPal が安全な支払いサイトでチェックアウトをホストすることも、カスタマイズ可能なソリューションを使用して支払い体験全体を管理することもできます。

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal ペイフローリンク](paypal-payflow-link.md)

![PayPal 支払いゲートウェイの設定](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## PayPal 不正管理フィルター

PayPal 不正管理フィルターを使用すると、不正なトランザクションの検出と対応が容易になり、フラグ設定、保留レビュー、またはリスクの高い支払いの拒否を設定できます。 コマースに関連するアクション [注文ステータス](order-status.md) 不正フィルタの設定に従って変更された値：

| アクション | 結果 |
| --- | --- |
| [!UICONTROL Review] | 疑わしい注文がステータスを受け取ります _支払いレビュー_ 注文が行われた時点で。 注文を確認し、承認したり、支払いをキャンセルしたりするには、Admin または PayPal 側を使用します。 クリック時 **[!UICONTROL Accept Payment]** または **[!UICONTROL Deny Payment]**&#x200B;の場合、注文の新しいトランザクションは作成されません。 <br/><br/>PayPal サイト上のトランザクションのステータスを変更する場合は、 **[!UICONTROL Get Payment Update]** （管理者の「順序」ページ）を開き、変更を適用します。 次をクリックした場合： **[!UICONTROL Accept Payment]** または **[!UICONTROL Deny Payment]**&#x200B;に設定されている場合、PayPal サイトでおこなわれた変更が適用されます。 |
| [!UICONTROL Deny] | 対応するトランザクションが PayPal によって拒否されたので、疑わしい注文を顧客が行うことはできません。 <br/><br/>管理者からの支払いを拒否するには、 **[!UICONTROL Deny Payment]** をクリックします。 オーダーのステータスが「 」に変わります。 `Canceled`に設定すると、トランザクションが元に戻され、資金が顧客アカウントで解放されます。 対応する情報が _[!UICONTROL Comments History]_「 」セクションに表示されます。 |
| [!UICONTROL Flag] | 疑わしい注文がステータスを取得します `Processing` 配置されたとき 対応するトランザクションは、マーチャントアカウントトランザクションのリストでフラグでマークされます。 |

{style="table-layout:auto"}

## PayPal ソリューション（国別）

| 国 | PayPal 支払いソリューション |
|--- |--- |
| オーストラリア | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| カナダ | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) （速達チェックアウトを含む）<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| フランス | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| ドイツ | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 中華人民共和国香港特別行政区 | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| イタリア | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 日本 | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| ニュージーランド | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| スペイン | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 英国 | [!DNL PayPal Payments Pro Hosted Solution] （速達チェックアウトを含む）<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 米国 | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) （速達チェックアウトを含む）<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) （速達チェックアウトを含む）<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) （速達チェックアウトを含む）<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) （速達チェックアウトを含む）<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### その他の国

PayPal Express Checkout と PayPal Website Payments Standard は、以下の国でご利用いただけます。

- アルゼンチン
- オーストリア
- ベルギー
- ブラジル
- ブルガリア
- チリ
- コスタリカ
- キプロス
- チェコ共和国
- デンマーク
- ドミニカ共和国
- エクアドル
- エストニア
- フィンランド
- フランス領ギアナ
- ジブラルタル
- ギリシャ
- グアドループ
- ハンガリー
- アイスランド
- インド
- インドネシア
- アイルランド
- イスラエル
- ジャマイカ
- ラトビア
- リヒテンシュタイン
- リトアニア
- ルクセンブルグ
- マレーシア
- マルタ
- マルティニーク
- メキシコ
- オランダ
- ノルウェー
- フィリピン
- ポーランド
- ポルトガル
- レユニオン
- ルーマニア
- サンマリノ
- シンガポール
- スロバキア
- スロベニア
- 南アフリカ
- 韓国
- スウェーデン
- スイス
- 台湾
- タイ
- トルコ
- アラブ首長国連邦
- ウルグアイ
- ベネズエラ
- ベトナム


[1]: https://manager.paypal.com/
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later
