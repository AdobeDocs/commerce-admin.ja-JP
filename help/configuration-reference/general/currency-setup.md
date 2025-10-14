---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: Commerce Admin の [!UICONTROL General] &gt; [!UICONTROL Currency Setup] ページで設定を確認します。
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>これらの設定について詳しくは、[&#x200B; 通貨の設定 &#x200B;](../../stores-purchase/currency-configuration.md) を参照してください。

## [!UICONTROL Currency Options]

![&#x200B; 通貨の設定/通貨オプション &#x200B;](./assets/currency-setup-currency-options.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Web サイト | すべてのオンライン支払トランザクションに使用される主要通貨。 複数のストアを表示する場合、価格の範囲を [&#x200B; カタログ &#x200B;](../catalog/catalog.md) 設定で設定する必要があります。 |
| [!UICONTROL Default Display Currency] | ストア表示 | 価格の表示に使用される主要通貨。 |
| [!UICONTROL Allowed Currencies] | ストア表示 | ストアが支払いに受け入れる通貨。 |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>2.4.6 リリース以降、[[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨（廃止予定）となり、[[!DNL Fixer API]  （APILayer） &#x200B;](https://apilayer.com/marketplace/fixer-api) サービスに置き換わります。 非推奨の [!DNL Fixer.io] アカウントではなく、APILayer アカウントを使用することを強くお勧めします。

![&#x200B; 通貨設定 > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | [!DNL fixer.io] アカウントを通じて変換サービスにアクセスするために使用されるキー。 詳細は、[[!DNL fixer.io]](https://fixer.io/) を参照してください。 |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | Fixer.io セッションがタイムアウトするまでの非アクティブな時間（秒）を指定します。 デフォルト値：`100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![&#x200B; 通貨設定/Fixer Api （APILayer） &#x200B;](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | [!DNL APILayer] アカウントを通じて変換サービスにアクセスするために使用されるキー。 詳細は、[[!DNL APILayer]](https://apilayer.com/) を参照してください。 |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | [!DNL APILayer] セッションがタイムアウトするまでの非アクティブな時間（秒）を指定します。 デフォルト値は `100` です。 |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![&#x200B; 通貨の設定/通貨換算 API](./assets/currency-setup-converter.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | 変換サービスへのアクセスに使用するキー。 詳しくは、[[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/) を参照してください。 |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | [!DNL Currency Converter] セッションがタイムアウトするまでの非アクティブな時間（秒）を指定します。 デフォルト値：`100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![&#x200B; 通貨設定/予定インポート設定 &#x200B;](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | 通貨レートに対してスケジュール済インポートが有効かどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Service] | ストア表示 | スケジュールされたインポートのデータを提供するサービスを指定します。 デフォルト値は `fixer.io` です |
| [!UICONTROL Start Time] | ストア表示 | 開始時間を時間、分、秒で示します（24 時間形式）。 |
| [!UICONTROL Frequency] | ストア表示 | スケジュールされた読み込みの実行頻度を決定します。 オプション：`Daily`/`Weekly`/`Monthly` |
| [!UICONTROL Error Email Recipient] | ストア表示 | スケジュールされた読み込みエラーについてメールで通知される各ユーザーのメールアドレスを識別します。 受信者が複数の場合は、各エントリをコンマで区切ります。 |
| [!UICONTROL Error Email Sender] | Web サイト | エラーメール通知の送信者として表示される店舗連絡先を識別します。 既定の送信者：`General Contact` |
| [!UICONTROL Error Email Template] | Web サイト | エラーメール通知の基礎として使用するテンプレートを指定します。 既定のテンプレート：`Currency Update Warnings` |

{style="table-layout:auto"}
