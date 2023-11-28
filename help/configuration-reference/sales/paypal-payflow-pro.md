---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt;  [!UICONTROL PayPal Payflow Pro]'
description: 設定を確認するには、 [!UICONTROL PayPal Payflow Pro] のセクション [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] コマース管理のページ。
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日現在、ヨーロッパの銀行は、満たさない支払いを辞退する可能性があります [PSD2](../../getting-started/compliance-payment-services-directive.md) 要件。 PSD2 に準拠するには [!DNL PayPal Payflow Pro] は、と統合されている必要があります [!DNL Cardinal Commerce]. 詳しくは、 [3-D セキュア（ペイフロー用）](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![必須設定](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Web サイト | （オプション） PayPal マーチャントアカウントに関連付けられている電子メールアドレス。 電子メールアドレスでは大文字と小文字が区別され、アカウント内のアドレスと完全に一致する必要があります。 |
| [!UICONTROL Partner] | Web サイト | PayPal パートナー ID（該当する場合）。 |
| [!UICONTROL Vendor] | Web サイト | PayPal ユーザーのログイン名。 |
| ユーザー | Web サイト | PayPal アカウント上の別のユーザーの ID。 |
| [!UICONTROL Password] | Web サイト | PayPal マーチャントアカウントに関連付けられたパスワード。 |
| [!UICONTROL Test Mode] | Web サイト | 有効にすると、はテスト環境で PayPal Payflow Pro を実行します。 実稼働モードで「運用開始」の準備が整ったら、テストモードをオフにします。 オプション： `Yes` / `No` |
| [!UICONTROL Use Proxy] | Web サイト | プロキシは、サーバーファイアウォールが PayPal サーバーへの直接アクセスを禁止している場合に、トラフィックをリダイレクトするために使用できます。 該当する場合は、PayPal サーバーとの接続を確立するために使用されるプロキシサーバーを識別します。 オプション： `Yes` / `No` <br/><br/>有効にした場合は、プロキシオプションを設定します。 <br/>**`Proxy Host`**— プロキシホストの IP アドレス。<br/>**`Proxy Port`**  — プロキシポートの番号。 |
| [!UICONTROL Enable this Solution] | Web サイト | PayPal Payflow Pro をお客様が支払い方法として利用できるかどうかを指定します。 |
| [!UICONTROL Enable PayPal Credit] | Web サイト | PayPal クレジットをお客様が支払いオプションとして利用できるかどうかを指定します。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advertise PayPal Credit]

![PayPal クレジットの宣伝](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Web サイト | PayPal クレジットアカウントに関連付けられた発行者 ID です。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | PayPal から Publisher ID を取得します。 |
| [!UICONTROL Home Page] | Web サイト | の位置とサイズを決定します。 [!DNL PayPal Credit] バナーをホームページに表示します。 オプション： <br/>**`Display`**— 次の条件を満たすかどうかを決定します。[!DNL PayPal Credit] バナーがストアのホームページに表示されます。 オプション： `Yes` / `No`<br/>**`Position`** - [!DNL PayPal Credit] バナーをホームページに表示します。 オプション：ヘッダー（中央）/サイドバー（右） <br/>**`Size`**— サイズを決定します [!DNL PayPal Credit] バナーをホームページに表示します。 オプション： `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Web サイト | の位置とサイズを決定します。 [!DNL PayPal Credit] カテゴリページのバナー。 オプション： （の場合と同じ） [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Web サイト | の位置とサイズを決定します。 [!DNL PayPal Credit] 製品ページのバナー。 オプション： （の場合と同じ） [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Web サイト | の位置とサイズを決定します。 [!DNL PayPal Credit] 買い物かごページのバナー。 オプション： （の場合と同じ） [!UICONTROL Home Page]) |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![基本設定](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストア表示 | チェックアウト時の支払い方法として PayPal Payflow Pro を識別する名前。 |
| [!UICONTROL Sort Order] | ストア表示 | チェックアウト時に他の支払い方法と共に PayPal Payflow Pro が表示される順序を決定する数値です。 |
| [!UICONTROL Payment Action] | Web サイト | 注文が送信されたときに PayPal が実行するアクションを決定します。 オプション： <br/>**`Authorization`**・買い付けを承認するが、資金を保留する。 その金額は、商人によって「取り込まれる」まで引き落とされません。<br/>**`Sale`**  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。 |
| **[!UICONTROL Credit Card Settings]** |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Web サイト | 顧客がチェックアウト時に使用できるクレジットカードを決定します。 サポートされている各カードを選択します。 オプション： `American Express` （追加の契約が必要） / `Visa` / `MasterCard` / `Discover` / `JCB` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Settings]

![詳細設定](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| 買い物かごに表示 | ストア表示 | PayPal Express Checkout が買い物かごの支払いオプションとして表示されるかどうかを指定します。 オプション：はい（推奨）/いいえ |
| [!UICONTROL Payment Action Applicable From] | Web サイト | 適用可能な国の選択範囲を決定します。 オプション：すべての許可された国/特定の国 |
| [!UICONTROL Countries Payment Applicable From] | Web サイト | 支払が受け入れられた国を識別します。 選択した国の請求先住所を持つ顧客のみが、この支払い方法で購入を行うことができます。 |
| [!UICONTROL Debug Mode] | Web サイト | ストアと PayPal 支払いシステム間で送信されたメッセージをログファイルに記録します。 オプション： `Yes` / `No` <br/><br/>**_注意：_**ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI データセキュリティ基準に従って、クレジットカード情報はログファイルに記録されません。 |
| [!UICONTROL Enable SSL Verification] | Web サイト | ホストセキュリティ証明書の検証を有効にします。 オプション： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Web サイト | PayPal サイト上の顧客の買い物かごからの行項目の完全な概要を表示します。 オプション： `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Web サイト | 顧客が PayPal サイトからトランザクションを完了できるか、またはストアに戻って注文を送信する前に注文の確認手順を完了する必要があるかを指定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
