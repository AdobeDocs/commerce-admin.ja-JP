---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: の設定を確認します。 [!UICONTROL Sales] &gt; [!UICONTROL Google API] コマース管理者のページ。
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | ストア表示 | 有効 [!DNL Google Analytics] あなたの店のために。 オプション： `Yes` / `No` |
| [!UICONTROL Account Type] | ストア表示 | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）Google Analytics アカウントの種類に応じて設定オプションを決定します。 オプション：ユニバーサルアナリティクス（デフォルト）/Google Tag Manager |
| [!UICONTROL Account Number] | ストア表示 | の作成時に割り当てられたアカウント番号またはトラッキングコード [!DNL Google Analytics] アカウント。 |
| [!UICONTROL Anonymize IP] | ストア表示 | に表示される IP アドレスから識別情報を削除するかどうかを決定します [!DNL Google Analytics] 件の結果。 |
| [!UICONTROL Enable Content Experiments] | ストア表示 | アクティブ化 [Google コンテンツ実験](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207)を使用して、同じページの最大 10 個の異なるバージョンをテストできます。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Google Tag Manager アカウントタイプ](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

条件 **[!UICONTROL Account Type]** はに設定されています。 `Google Tag Manager`を選択すると、追加のフィールドが表示されます。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | ストア表示 | の一意の ID [!DNL Google Tag Manager] コンテナ。 この値は通常、で始まります `GTM-`. この ID [!DNL Google Tag Manager] アカウント。 次の場合 [!DNL Google Tag Manager] はストアに対して既にインストールおよび設定されており、コンテナ ID はこのフィールドに自動的に表示されます。 |
| [!UICONTROL List property for the catalog page] | ストア表示 | は、 [!DNL Google Tag Manager] カタログページに関連付けられたプロパティ。 デフォルト値 `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | ストア表示 | は、 [!DNL Google Tag Manager] クロスセル ブロックに関連付けられたプロパティです。 デフォルト値 `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | ストア表示 | は、 [!DNL Google Tag Manager] アップセル ブロックに関連付けられたプロパティです。 デフォルト値 `Up-sell` |
| [!UICONTROL List property for the related products block] | ストア表示 | は、 [!DNL Google Tag Manager] 関連製品ブロックに関連付けられたプロパティです。 デフォルト値 `Related Products` |
| [!UICONTROL List property for the search results page] | ストア表示 | は、 [!DNL Google Tag Manager] 検索結果ページに関連付けられたプロパティ。 デフォルト値 `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | ストア表示 | は、 [!DNL Google Tag Manager] 内部販促のラベルに関連付けられたプロパティ。 デフォルト値 `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | ストア表示 | ストアのGoogle AdWords を有効にします。 オプション： `Yes` / `No` |
| [!UICONTROL Conversion ID] | ストア表示 | Google AdWords アカウントの ID。 |
| [!UICONTROL Conversion Language] | ストア表示 | AdWords の変換に使用される言語です。 オプション： `All available languages` |
| [!UICONTROL Conversion Format] | ストア表示 | の形式を決定します [!DNL Google Site Stats] 変換ページに表示される通知。 通知は、訪問の追跡に使用される Cookie について訪問者に通知するページにリンクしています。 この数値は、に割り当てられます `google_conversion_format` adwords スクリプトの変数。 詳しくは、 [コンバージョントラッキングについて](https://support.google.com/google-ads/answer/1722022?hl=en) （Google web サイト上） オプション： <br/>**`1`**- 1 行の通知を表示します。<br/>**`2`** - （デフォルト） 2 行の通知を表示します。 <br/>**`3`**– 顧客通知が表示されません。 |
| [!UICONTROL Conversion Color] | ストア表示 | 変換ラベルの色を決定します。 を使用 [カラーピッカー](https://www.w3schools.com/colors/colors_picker.asp) 16 進数値を選択します。 この 16 進数値は、 `google_conversion_color` adwords スクリプトの変数。 例：ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | ストア表示 | と共に表示されるテキストラベル [!DNL Google Site Stats] 通知。 このテキスト文字列は、 `~` adwords スクリプトの変数。 例：「お買い物ありがとうございます。」 |
| [!UICONTROL Conversion Value Type] | ストア表示 | 変換を行うタイミングを決定するために使用する値のタイプを指定します。 オプション： <br/>**`Dynamic`**– 動的な注文金額に基づいてコンバージョンが発生したことを判断します。<br/>**`Constant`**  – 入力された値に基づいて、コンバージョンが発生したことを判別します。 |
| [!UICONTROL Conversion Value] | ストア表示 | に使用する値を指定します。 _[!UICONTROL Constant]_コンバージョン値タイプ。 |
| [!UICONTROL Send Order Currency] | ストア表示 | （基本通貨の異なる Web サイト用に） AdWords でトランザクション固有の通貨換算値を有効にします。 |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![GOOGLE ANALYTICS4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | ストア表示 | ストアのGoogle Analytics 4 を有効にします。 オプション： `Yes` / `No` |
| [!UICONTROL Account Type] | ストア表示 | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）Google Analytics アカウントの種類に応じて設定オプションを決定します。 オプション： `Google Analytics4` （デフォルト） / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | ストア表示 | Google Analytics アカウントの作成時に割り当てられたアカウント番号またはトラッキングコード。 |
| [!UICONTROL Anonymize IP] | ストア表示 | Google Analyticsの結果に表示される IP アドレスから識別情報を削除するかどうかを指定します。 |
| [!UICONTROL Enable Content Experiments] | ストア表示 | アクティブ化 [Google コンテンツ実験](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207)を使用して、同じページの最大 10 個の異なるバージョンをテストできます。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Google Tag Manager アカウントタイプ](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

条件 **[!UICONTROL Account Type]** はに設定されています。 `Google Tag Manager`を選択すると、追加のフィールドが表示されます。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | ストア表示 | の一意の ID [!DNL Google Tag Manager] コンテナ。 この値は通常、で始まります `GTM-`. この ID はGoogle Tab Manager アカウントに含まれています。 次の場合 [!DNL Google Tag Manager] はストアに対して既にインストールおよび設定されており、コンテナ ID はこのフィールドに自動的に表示されます。 |
| [!UICONTROL List property for the catalog page] | ストア表示 | は、 [!DNL Google Tag Manager] カタログページに関連付けられたプロパティ。 デフォルト値 `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | ストア表示 | は、 [!DNL Google Tag Manager] クロスセル ブロックに関連付けられたプロパティです。 デフォルト値 `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | ストア表示 | は、 [!DNL Google Tag Manager] アップセル ブロックに関連付けられたプロパティです。 デフォルト値 `Up-sell` |
| [!UICONTROL List property for the related products block] | ストア表示 | は、 [!DNL Google Tag Manager] 関連製品ブロックに関連付けられたプロパティです。 デフォルト値 `Related Products` |
| [!UICONTROL List property for the search results page] | ストア表示 | は、 [!DNL Google Tag Manager] 検索結果ページに関連付けられたプロパティ。 デフォルト値 `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | ストア表示 | は、 [!DNL Google Tag Manager] 内部販促のラベルに関連付けられたプロパティ。 デフォルト値 `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | ストア表示 | ストアのGoogle AdWords を有効にします。 オプション： `Yes` / `No` |
| [!UICONTROL Conversion ID] | ストア表示 | Google AdWords アカウントの ID。 |
| [!UICONTROL Conversion Language] | ストア表示 | AdWords の変換に使用される言語です。 オプション：使用可能なすべての言語 |
| [!UICONTROL Conversion Format] | ストア表示 | コンバージョンページに表示されるGoogle サイトの統計情報に関する通知の形式を指定します。 通知は、訪問の追跡に使用される Cookie について訪問者に通知するページにリンクしています。 この数値は、に割り当てられます `google_conversion_format` adwords スクリプトの変数。 詳しくは、 [コンバージョントラッキングについて](https://support.google.com/google-ads/answer/1722022?hl=en) （Google web サイト上） オプション： <br/>**`1`**- 1 行の通知を表示します。<br/>**`2`** - （デフォルト） 2 行の通知を表示します。 <br/>**`3`**– 顧客通知が表示されません。 |
| [!UICONTROL Conversion Color] | ストア表示 | 変換ラベルの色を決定します。 を使用 [カラーピッカー](https://www.w3schools.com/colors/colors_picker.asp) 16 進数値を選択します。 この 16 進数値は、 `google_conversion_color` adwords スクリプトの変数。 例：ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | ストア表示 | Google サイト統計の通知と共に表示されるテキストラベルです。 このテキスト文字列は、 `~` adwords スクリプトの変数。 例：「お買い物ありがとうございます。」 |
| [!UICONTROL Conversion Value Type] | ストア表示 | 変換を行うタイミングを決定するために使用する値のタイプを指定します。 オプション： <br/>**`Dynamic`**– 動的な注文金額に基づいてコンバージョンが発生したことを判断します。<br/>**`Constant`**  – 入力された値に基づいて、コンバージョンが発生したことを判別します。 |
| [!UICONTROL Conversion Value] | ストア表示 | に使用する値を指定します。 _[!UICONTROL Constant]_コンバージョン値タイプ。 |
| [!UICONTROL Send Order Currency] | ストア表示 | （基本通貨の異なる Web サイト用に） AdWords でトランザクション固有の通貨換算値を有効にします。 |

{style="table-layout:auto"}
