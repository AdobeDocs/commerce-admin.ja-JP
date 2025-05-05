---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] ページの [!UICONTROL Payment Services] セクションで、設定を確認します。
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



支払いサービスは、堅牢で安全な支払い処理を提供するために、サンドボックステストやシンプルなセットアップを含む、ターンキーのセルフサービスソリューションを提供します。 詳しくは、[_支払いサービスユーザーガイド_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=ja) を参照してください。

支払いサービスの設定にアクセスするには、_管理者_ サイドバーで **[!UICONTROL Sales]**/**[!UICONTROL Payment Services]** に移動し、「**[!UICONTROL Settings]**」をクリックします。

![ 資金決済の設定 ](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>[ 設定 ](https://experienceleague.adobe.com/docs/commerce/payment-services/configure/settings.html?lang=ja) の代わりにレガシー設定を使用するには、[ レガシー設定 ](https://experienceleague.adobe.com/docs/commerce/payment-services/configure/configure-admin.html?lang=ja) を参照してください。

## [!UICONTROL General]

![ 一般設定 ](assets/payments-general-settings.png){width="600" zoomable="yes"}

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---|---|---|
| [!UICONTROL Enable] | web サイト | Web サイトの [!DNL Payment Services] を有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | ストア表示 | ストアのメソッド（環境）を設定します。 オプション：[!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | ストア表示 | サンドボックスオンボーディング中に自動生成されるサンドボックスマーチャント ID。 |
| [!UICONTROL Production Merchant ID] | ストア表示 | サンドボックスのオンボーディング中に自動生成される実稼動マーチャント ID。 |
| [!UICONTROL Soft Descriptor] | web サイトまたはストア表示 | 顧客トランザクションの情報を提供し、ブランド、ストアまたは製品ラインを記述するソフト記述子を web サイトおよびストアビューに追加します。 [!UICONTROL Use website] の切り替えにより、web サイトレベルで追加されたソフト記述子が適用されます。 [!UICONTROL Use default] 切替スイッチは、デフォルトとして追加された任意のソフト記述子を適用します。 |

{style="table-layout:auto"}

## [!UICONTROL Credit card fields]

![ クレジットカードのフィールド設定 ](assets/payments-ccfields-settings.png){width="600" zoomable="yes"}

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---|---|---|
| [!UICONTROL Title] | ストア表示 | チェックアウト時に支払い方法ビューでこの支払いオプションのタイトルとして表示するテキストを追加します。 |
| [!UICONTROL Payment Action] | web サイト | 指定した支払方法の [ 支払アクション ](payment-methods.md#payment-actions)。 オプション：[!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | web サイト | [3DS セキュア認証 ](https://experienceleague.adobe.com/docs/commerce/payment-services/security-compliance/security.html?lang=ja#3ds) を有効または無効にします。 オプション：[!UICONTROL Always]/[!UICONTROL When Required]/[!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | web サイト | チェックアウトページに表示するクレジットカードフィールドを有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | ストア表示 | [ クレジット カードの保管 ](https://experienceleague.adobe.com/docs/commerce/payment-services/payments-checkout/vaulting.html?lang=ja) を有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | ストア表示 | 管理者で、顧客の注文を完了する機能を有効または無効にします [ ボールト支払方法を使用 ](https://experienceleague.adobe.com/docs/commerce/payment-services/payments-checkout/vaulting.html?lang=ja)。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | web サイト | デバッグモードを有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL Payment buttons]

![Paypal 支払いボタンの設定 ](assets/payments-ppbuttons-settings.png){width="600" zoomable="yes"}

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---|---|---|
| [!UICONTROL Title] | ストア表示 | チェックアウト時に支払い方法ビューでこの支払いオプションのタイトルとして表示するテキストを追加します。 |
| [!UICONTROL Payment Action] | web サイト | 指定した支払方法の [ 支払アクション ](payment-methods.md#payment-actions){target="_blank"}。 オプション：[!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | ストア表示 | チェックアウトページで [!DNL PayPal Smart Buttons] を有効または無効にします。 オプション：[!UICONTROL &#x200B; Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | ストア表示 | 製品の詳細ページで [!DNL PayPal Smart Buttons] を有効または無効にします。 オプション：[!UICONTROL &#x200B; Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | ストア表示 | ミニ買い物かごのプレビューで [!DNL PayPal Smart Buttons] を有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | ストア表示 | 買い物かごページの [!DNL PayPal Smart Buttons] を有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | ストア表示 | 支払ボタンが表示される後で支払う支払いオプションの外観を有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | web サイト | 買い物かご、製品ページ、ミニカート、およびチェックアウトフロー中の「後で支払う」メッセージを有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | ストア表示 | 支払ボタンが表示される Venmo 支払オプションを有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | ストア表示 | 支払いボタンが表示される「Apple Pay」支払いオプションを有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | ストア表示 | 支払いボタンが表示されるクレジット カードおよびデビット カードの支払いオプションを有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | web サイト | デバッグモードを有効または無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL PayPal Smart Button Styling]

![Paypal 支払いボタンのスタイル設定 ](assets/payments-buttonstyle-settings.png){width="600" zoomable="yes"}

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Layout] | ストア表示 | 支払いボタンのレイアウトのスタイルを定義します。 オプション：[!UICONTROL Vertical] / [!UICONTROL Horizontal] |
| [!UICONTROL Tagline] | ストア表示 | タグラインを有効/無効にします。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Color] | ストア表示 | 支払いボタンの色を定義します。 オプション：[!UICONTROL Blue] / [!UICONTROL Gold] / [!UICONTROL Silver] / [!UICONTROL White] / [!UICONTROL Black] |
| [!UICONTROL Shape] | ストア表示 | 支払いボタンの形状を定義します。 オプション：[!UICONTROL Rectangular] / [!UICONTROL Pill] |
| [!UICONTROL Responsive Button Height] | ストア表示 | 支払いボタンで既定の高さを使用するかどうかを定義します。 オプション：[!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Height] | ストア表示 | 支払いボタンの高さを定義します。 デフォルト値：なし |
| [!UICONTROL Label] | ストア表示 | 支払いボタンに表示されるラベルを定義します。 オプション：[!UICONTROL PayPal] / [!UICONTROL Checkout] / [!UICONTROL Buynow] / [!UICONTROL Pay] / [!UICONTROL Installment] |

{style="table-layout:auto"}
