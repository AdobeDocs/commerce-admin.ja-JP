---
title: PayPal 支払いソリューション
description: ストアで使用できる PayPal 支払いソリューションの統合について説明します。
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# PayPal 支払いソリューション

PayPal は、オンライン決済のグローバルリーダーであり、顧客がオンラインで支払う迅速かつ安全な方法です。 利用可能な PayPal ソリューションの選択は、マーチャントの場所によって異なります。 PayPal Express Checkout と PayPal Payments Standard は、世界中のすべての地域で使用できます。 詳しくは、[ 国別 PayPal ソリューション ](#paypal-solutions-by-country) を参照してください。

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日以降、ヨーロッパの銀行は、[PSD2](../getting-started/compliance-payment-services-directive.md) の要件を満たさない支払いを拒否する場合があります。 ほとんどの PayPal ソリューションでは、PSD2 の要件は PayPal で処理されるので、これらの要件に準拠するための対応は必要ありません。

## PayPal ビジネスアカウント

PayPal をストアの支払い方法として提供するには、PayPal[ ビジネスアカウント ][1] および/または [PayPal Payflow アカウント ][2] が必要です。 アカウント要件は、各 PayPal ソリューションの説明で指定されています。 PayPal のマーチャントアカウントは、ストアからの購入に適用される [ 不正フィルター ](#paypal-fraud-management-filters) の管理にも使用されます。

PayPal Express Checkout または Payflow Pro の Express Checkout を使用するお客様は、PayPal のバイヤーアカウントを持っている必要があります。 PayPal Payments Standard （一部の国では Website Payments Standard）は、マーチャントが有効にしている場合、直接または購入者アカウントを通じて使用できます _PayPal アカウント オプション_。 デフォルトでは、このパラメータは有効になっており、顧客はクレジットカード情報を入力するか、PayPal でバイヤーアカウントを作成するかを選択できます。 無効にした場合、お客様は購入を行う前に、まず PayPal バイヤーアカウントを作成する必要があります。

Website Payments Pro、Website Payments Pro Payflow Edition、Payflow Pro Gateway、Payflow Link では、チェックアウト時にクレジットカード情報を入力する必要があります。

## PayPal クレジットと PayLater

PayPal PayLater は、顧客が資金調達にすばやくアクセスできるようにし、追加費用なしで今すぐ購入して時間の経過と共に支払うことができます。 お客様が PayPal Credit オプションを選択した場合は課金されず、通常の PayPal 取引手数料のみを支払います。 詳しくは、[PayPal web サイト ][3] を参照してください。

資金調達を宣伝する際に、売り上げを伸ばしましょう。 PayPal は、PayPal PayLater を使用した資金調達でブラウザーをバイヤーに変えるのに役立ちます。 顧客は時間の経過と共に料金を支払うことができますが、追加費用なしで事前に支払いを受けられます。 お客様が PayPal でチェックアウトする際に、PayPal の無料バナー広告を使用して、支払いオプションとして PayPal の資金調達を宣伝します。 PayPal Advertisingプログラムは、追加購入を生み出し、平均購入サイズを 15% 以上増やすことが示されています。

サイトのページに無料の既製のバナー広告を簡単に追加したり、チェックアウト中にショッピングカートに _PayPal クレジット_ ボタンを追加して、融資がすぐに利用可能であることを顧客に思い出させることができます。

>[!NOTE]
>
>2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能により、買い物客は購入時に全額を支払うのではなく、隔週の分割払いで注文の支払いを行うことができます。 PayPal クレジットエクスペリエンスは非推奨（廃止予定）となりました。

米国のマーチャントの場合、[PayPal Express Checkout](paypal-express-checkout.md) 支払いオプションでは PayPal クレジットがデフォルトで有効になっています。 この支払い方法を無効にするには、_PayPal Express Checkout 設定 [ の_ 機能 ](paypal-express-checkout.md#features) の節を参照してください。

PayPal クレジットは、他の PayPal 支払いソリューションではデフォルトで無効になっていますが、サポートソリューションの支払い方法の設定では有効にすることができます。

- [支払の前払い](paypal-payments-advanced.md)
- [支払いプロ](paypal-payments-pro.md)
- [支払い標準](paypal-payments-standard.md)
- [ペイフロープロ](paypal-payflow-pro.md)
- [ペイフローリンク](paypal-payflow-link.md)

>[!IMPORTANT]
>
>ストアの PayPal クレジットまたは PayPal PayLater を設定する前に、PayPal マーチャントアカウントで有効になっていることを確認してください。

## 統合 PayPal ソリューション

PayPal とAdobe Commerceを使用すると、すべての主要なデビットカードとクレジットカードから支払いを受け入れることができます。 PayPal アカウントをお持ちでないお客様でも PayPal で購入の支払いを行うことができるので、PayPal は余分な手間をかけずに追加の利便性を提供します。

>[!NOTE]
>
>PayPal Express Checkout を除き、ストアで一度に複数の PayPal メソッドを有効にすることはできません。 PayPal Express チェックアウトは、PayPal Payments Standard を除く他の PayPal 支払い方法で使用できます。 支払いソリューションを変更すると、以前の方法は無効になります。

### PayPal Express チェックアウト

[PayPal Express チェックアウト](paypal-express-checkout.md)

### PayPal オールインワン決済ソリューション

米国では、PayPal は、成長するビジネスのニーズに対応するために、次の PCI 準拠のソリューションを提供しています。

- [PayPal 支払い詳細](paypal-payments-advanced.md)
- [PayPal ペイメントプロ](paypal-payments-pro.md)
- [PayPal 支払い標準](paypal-payments-standard.md)

![PayPal オールインワン支払いソリューション ](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### PayPal 支払いゲートウェイ

支払いゲートウェイは、クレジットカードまたは直接支払い処理を承認する e コマースアプリケーションサービスプロバイダーが提供するマーチャントサービスです。 彼らは顧客と銀行の間の仲介者として働いています。

支払いゲートウェイは、オンライン環境とオフライン環境で利用できます。 支払いは、電話、オンライン、またはモバイルアプリを通じて受け付けることができます。 トランザクションはサービスプロバイダーの処理システムに送信され、確認のためにお客様の銀行に送信されます。 確認された場合、マーチャントは顧客の銀行口座と直接連絡することなく支払いを受け取ります。

支払いゲートウェイには、直接とホストの 2 種類があります。

- 直接支払いゲートウェイを使用すると、ユーザーは店舗の web サイトでカードの詳細を入力できます。
- ホストされた支払いゲートウェイは、ストアの web サイトの外部にあるホストされた支払いページにユーザーをリダイレクトします。

支払いゲートウェイは、取引に関与するすべての関係者にセキュリティと保護を提供します。

PayPal は、お客様のビジネスに合わせて 2 つの支払いゲートウェイソリューションを選択できます。 PayPal に安全な支払いサイトでチェックアウトをホストさせるか、カスタマイズ可能なソリューションで支払いエクスペリエンス全体を制御することができます。

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal ペイフローリンク](paypal-payflow-link.md)

![PayPal 支払いゲートウェイの設定 ](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## PayPal 不正管理フィルター

PayPal の不正管理フィルターを使用すると、不正な取引を検出して対応しやすくなり、フラグを立てる、確認のために保留する、またはリスクの高い支払いを拒否するように設定できます。 不正フィルターの設定に従って変更された、Commerce[ 注文ステータス ](order-status.md) 値に関連するアクション：

| アクション | 結果 |
| --- | --- |
| [!UICONTROL Review] | 疑わしい注文は、注文が行われると、ステータス _支払いレビュー_ を受け取ります。 注文を確認して承認するか、管理者または PayPal 側で支払いをキャンセルすることができます。 **[!UICONTROL Accept Payment]** または **[!UICONTROL Deny Payment]** をクリックすると、注文の新しいトランザクションは作成されません。 <br/><br/>PayPal サイトで取引のステータスを変更する場合は、管理者の注文ページの **[!UICONTROL Get Payment Update]** をクリックして変更を適用する必要があります。 **[!UICONTROL Accept Payment]** または **[!UICONTROL Deny Payment]** をクリックすると、PayPal サイトで行われた変更が適用されます。 |
| [!UICONTROL Deny] | 対応する取引は PayPal によって拒否されるため、疑わしい注文を顧客が行うことはできません。 <br/><br/> 管理者から支払いを拒否するには、ページの右上隅にある「**[!UICONTROL Deny Payment]**」をクリックします。 注文ステータスが `Canceled` に変わり、トランザクションが取り消され、資金が顧客口座でリリースされます。 対応する情報が注文表示の _[!UICONTROL Comments History]_&#x200B;セクションに追加されます。 |
| [!UICONTROL Flag] | 注文が行われると、疑わしい注文がステータス `Processing` を取得します。 該当する取引は、商社勘定の取引のリスト内でフラグ付きでマークされます。 |

{style="table-layout:auto"}

## 国別 PayPal ソリューション

| 国 | PayPal 支払いソリューション |
|--- |--- |
| オーストラリア | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| カナダ | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) （高速チェックアウトを含む） <br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| フランス | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| ドイツ | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 香港特別行政区 | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| イタリア | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 日本 | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| ニュージーランド | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| スペイン | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 英国 | [!DNL PayPal Payments Pro Hosted Solution] （高速チェックアウトを含む） <br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 米国 | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) （エクスプレスチェックアウトを含む） <br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) （エクスプレスチェックアウトを含む） <br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) （エクスプレスチェックアウトを含む） <br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) （エクスプレスチェックアウトを含む） <br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### その他の国

PayPal Express Checkout および PayPal Website Payments Standard は、次の国で利用できます。

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
- ルクセンブルク
- マレーシア
- マルタ
- マルチニーク
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
