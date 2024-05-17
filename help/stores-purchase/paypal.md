---
title: PayPal 支払いソリューション
description: ストアで使用できる PayPal 支払いソリューションの統合について説明します。
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1230'
ht-degree: 0%

---

# PayPal 支払いソリューション

PayPal は、オンライン決済のグローバルリーダーであり、顧客がオンラインで支払う迅速かつ安全な方法です。 利用可能な PayPal ソリューションの選択は、マーチャントの場所によって異なります。 PayPal Express Checkout と PayPal Payments Standard は、世界中のすべての地域で使用できます。 詳しくは、 [国別 PayPal ソリューション](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日以降、ヨーロッパの銀行は満たさない支払いを拒否する可能性があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件 ほとんどの PayPal ソリューションでは、PSD2 の要件は PayPal で処理されるので、これらの要件に準拠するための対応は必要ありません。

## PayPal ビジネスアカウント

PayPal をストアの支払い方法として提供するには、PayPal が必要です [ビジネス アカウント][1] および/または [PayPal Payflow アカウント][2]. アカウント要件は、各 PayPal ソリューションの説明で指定されています。 PayPal マーチャントアカウントは、以下の管理にも使用されます [不正フィルター](#paypal-fraud-management-filters) これは、ストアからの購入に適用されます。

PayPal Express Checkout または Payflow Pro の Express Checkout を使用するお客様は、PayPal のバイヤーアカウントを持っている必要があります。 PayPal Payments Standard （一部の国では Website Payments Standard）は、マーチャントが有効にしている場合、直接または購入者アカウントを通じて使用できます _PayPal アカウント オプション_. デフォルトでは、このパラメータは有効になっており、顧客はクレジットカード情報を入力するか、PayPal でバイヤーアカウントを作成するかを選択できます。 無効にした場合、お客様は購入を行う前に、まず PayPal バイヤーアカウントを作成する必要があります。

Website Payments Pro、Website Payments Pro Payflow Edition、Payflow Pro Gateway、Payflow Link では、チェックアウト時にクレジットカード情報を入力する必要があります。

## PayPal クレジットと PayLater

PayPal PayLater は、顧客が資金調達にすばやくアクセスできるようにし、追加費用なしで今すぐ購入して時間の経過と共に支払うことができます。 お客様が PayPal Credit オプションを選択した場合は課金されず、通常の PayPal 取引手数料のみを支払います。 詳しくは、 [PayPal web サイト][3].

資金調達を宣伝する際に、売り上げを伸ばしましょう。 PayPal は、PayPal PayLater を使用した資金調達でブラウザーをバイヤーに変えるのに役立ちます。 顧客は時間の経過と共に料金を支払うことができますが、追加費用なしで事前に支払いを受けられます。 お客様が PayPal でチェックアウトする際に、PayPal の無料バナー広告を使用して、支払いオプションとして PayPal の資金調達を宣伝します。 PayPal 広告プログラムは、追加の購入を生み出し、平均購入サイズを 15% 以上増加させることが示されています。

無料の既製バナー広告をサイトのページや _PayPal クレジット_ チェックアウト中に買い物かごにボタンを押して、資金調達がすぐに利用できることを顧客に思い出させます。

>[!NOTE]
>
>2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能により、買い物客は購入時に全額を支払うのではなく、隔週の分割払いで注文の支払いを行うことができます。 PayPal クレジットエクスペリエンスは非推奨（廃止予定）となりました。

米国のマーチャントの場合、 [PayPal Express チェックアウト](paypal-express-checkout.md) 支払いオプション。 この支払い方法を無効にするには、 _機能_ セクション [PayPal Express チェックアウト設定](paypal-express-checkout.md#features).

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

![PayPal オールインワン決済ソリューション](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

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

![PayPal 支払いゲートウェイの設定](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## PayPal 不正管理フィルター

PayPal の不正管理フィルターを使用すると、不正な取引を検出して対応しやすくなり、フラグを立てる、確認のために保留する、またはリスクの高い支払いを拒否するように設定できます。 Commerceに関連するアクション [注文ステータス](order-status.md) 不正フィルターの設定に従って変更された値：

| アクション | 結果 |
| --- | --- |
| [!UICONTROL Review] | 疑わしい注文がステータスを受け取る _支払いの確認_ 注文する場合。 注文を確認して承認するか、管理者または PayPal 側で支払いをキャンセルすることができます。 クリックした場合 **[!UICONTROL Accept Payment]** または **[!UICONTROL Deny Payment]**&#x200B;注文の新しいトランザクションは作成されません。 <br/><br/>PayPal サイトで取引のステータスを変更する場合は、 **[!UICONTROL Get Payment Update]** 管理者の「順序」ページで変更を適用します。 クリックした場合 **[!UICONTROL Accept Payment]** または **[!UICONTROL Deny Payment]**&#x200B;を選択すると、PayPal サイトで行われた変更が適用されます。 |
| [!UICONTROL Deny] | 対応する取引は PayPal によって拒否されるため、疑わしい注文を顧客が行うことはできません。 <br/><br/>管理者から支払いを拒否するには、 **[!UICONTROL Deny Payment]** をページの右上隅に表示します。 注文のステータスが「」に変わります `Canceled`、トランザクションが取り消され、資金が顧客アカウントでリリースされます。 対応する情報が _[!UICONTROL Comments History]_注文ビューのセクション。 |
| [!UICONTROL Flag] | 疑わしい注文がステータスを取得 `Processing` 置かれるとき。 該当する取引は、商社勘定の取引のリスト内でフラグ付きでマークされます。 |

{style="table-layout:auto"}

## 国別 PayPal ソリューション

| 国 | PayPal 支払いソリューション |
|--- |--- |
| オーストラリア | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| カナダ | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) （高速チェックアウトを含む）<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| フランス | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| ドイツ | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 香港特別行政区 | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| イタリア | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 日本 | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| ニュージーランド | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| スペイン | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 英国 | [!DNL PayPal Payments Pro Hosted Solution] （高速チェックアウトを含む）<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 米国 | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) （高速チェックアウトを含む）<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) （高速チェックアウトを含む）<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) （高速チェックアウトを含む）<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) （高速チェックアウトを含む）<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

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
