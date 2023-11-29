---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: 設定を確認するには、 [!UICONTROL Payment Services] のセクション [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] コマース管理のページ。
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: bf166c1debd7f10a4d988d231a1a47f32c4cea9e
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



支払いサービスは、堅牢で安全な支払い処理を提供するために、サンドボックステストや簡単な設定を含む自動セルフサービスソリューションを提供します。 詳しくは、 [_支払サービスユーザーガイド_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

支払サービスの構成設定にアクセスするには、 _管理者_ サイドバーに移動 **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** をクリックします。 **[!UICONTROL Settings]**.

![支払いサービス設定](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>の代わりにレガシー設定を使用するには [設定](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/settings.html)を参照してください。 [従来の設定](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/configure-admin.html).

## [!UICONTROL General]

![一般設定](assets/payments-general-settings.png){width="600" zoomable="yes"}

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---|---|---|
| [!UICONTROL Enable] | web サイト | 有効または無効 [!DNL Payment Services] を設定します。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | ストア表示 | ストアのメソッドまたは環境を設定します。 オプション： [!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | ストア表示 | サンドボックスマーチャント ID。サンドボックスのオンボーディング中に自動生成されます。 |
| [!UICONTROL Production Merchant ID] | ストア表示 | サンドボックスのオンボーディング中に自動生成される、実稼動マーチャント ID。 |
| [!UICONTROL Soft Descriptor] | web サイトまたはストア表示 | ソフト記述子を Web サイトに追加し、顧客トランザクションの情報を提供し、ブランド、店舗、または製品ラインを説明するビューを保存します。 The [!UICONTROL Use website] toggle は、web サイトレベルに追加されたソフト記述子を適用します。 The [!UICONTROL Use default] toggle は、デフォルトとして追加されたソフト記述子を適用します。 |

{style="table-layout:auto"}

## [!UICONTROL Credit card fields]

![クレジットカードフィールドの設定](assets/payments-ccfields-settings.png){width="600" zoomable="yes"}

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---|---|---|
| [!UICONTROL Title] | ストア表示 | チェックアウト時に「支払い方法」ビューで、この支払いオプションのタイトルとして表示するテキストを追加します。 |
| [!UICONTROL Payment Action] | web サイト | The [支払手続](payment-methods.md#payment-actions) 指定した支払い方法の オプション： [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | web サイト | 有効または無効 [3DS セキュア認証](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/security-compliance/security.html#3ds). オプション： [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | web サイト | チェックアウトページに表示するクレジットカードフィールドを有効または無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | ストア表示 | 有効または無効 [クレジットカードの保管](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | ストア表示 | 管理者で顧客の注文を完了する機能を有効または無効にします [跳ね上げ式の支払い方法を使用する](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | web サイト | デバッグモードを有効または無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL Payment buttons]

![Paypal の支払いボタンの設定](assets/payments-ppbuttons-settings.png){width="600" zoomable="yes"}

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---|---|---|
| [!UICONTROL Title] | ストア表示 | チェックアウト時に「支払い方法」ビューで、この支払いオプションのタイトルとして表示するテキストを追加します。 |
| [!UICONTROL Payment Action] | web サイト | The [支払手続](payment-methods.md#payment-actions){target="_blank"} 指定した支払い方法の オプション： [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | ストア表示 | 有効または無効 [!DNL PayPal Smart Buttons] を「チェックアウト」ページに追加します。 オプション： [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | ストア表示 | 有効または無効 [!DNL PayPal Smart Buttons] 製品の詳細ページに表示されます。 オプション： [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | ストア表示 | 有効または無効 [!DNL PayPal Smart Buttons] をクリックします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | ストア表示 | 有効または無効 [!DNL PayPal Smart Buttons] を買い物かごページに追加します。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | ストア表示 | 支払いボタンが表示される後払いオプションの外観を有効または無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | web サイト | 買い物かご、製品ページ、ミニ買い物かごおよびチェックアウトフローの「後で支払う」メッセージを有効または無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | ストア表示 | 支払いボタンが表示される Venmo 支払いオプションを有効または無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | ストア表示 | 支払いボタンが表示される「Apple支払」支払いオプションを有効または無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | ストア表示 | 支払いボタンが表示される「クレジット」および「デビット」カードの支払いオプションを有効または無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | web サイト | デバッグモードを有効または無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL PayPal Smart Button Styling]

![Paypal の支払いボタンのスタイル設定](assets/payments-buttonstyle-settings.png){width="600" zoomable="yes"}

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Layout] | ストア表示 | 支払いボタンのレイアウトのスタイルを定義します。 オプション： [!UICONTROL Vertical] / [!UICONTROL Horizontal] |
| [!UICONTROL Tagline] | ストア表示 | タグラインを有効/無効にします。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Color] | ストア表示 | 支払いボタンの色を定義します。 オプション： [!UICONTROL Blue] / [!UICONTROL Gold] / [!UICONTROL Silver] / [!UICONTROL White] / [!UICONTROL Black] |
| [!UICONTROL Shape] | ストア表示 | 支払いボタンの形状を定義します。 オプション： [!UICONTROL Rectangular] / [!UICONTROL Pill] |
| [!UICONTROL Responsive Button Height] | ストア表示 | 支払いボタンが既定の高さを使用するかどうかを定義します。 オプション： [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Height] | ストア表示 | 支払いボタンの高さを定義します。 デフォルト値：なし |
| [!UICONTROL Label] | ストア表示 | 支払いボタンに表示されるラベルを定義します。 オプション： [!UICONTROL PayPal] / [!UICONTROL Checkout] / [!UICONTROL Buynow] / [!UICONTROL Pay] / [!UICONTROL Installment] |

{style="table-layout:auto"}
