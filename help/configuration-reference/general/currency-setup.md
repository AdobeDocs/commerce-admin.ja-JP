---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: の設定を確認します。 [!UICONTROL General] &gt; [!UICONTROL Currency Setup] コマース管理者のページ。
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
>参照： [通貨の設定](../../stores-purchase/currency-configuration.md) これらの設定について詳しくは、こちらを参照してください。

## [!UICONTROL Currency Options]

![通貨の設定/通貨オプション](./assets/currency-setup-currency-options.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Web サイト | すべてのオンライン支払トランザクションに使用される主要通貨。 複数のストア表示の場合、価格の範囲はで設定する必要があります。 [カタログ](../catalog/catalog.md) 設定。 |
| [!UICONTROL Default Display Currency] | ストア表示 | 価格の表示に使用される主要通貨。 |
| [!UICONTROL Allowed Currencies] | ストア表示 | ストアが支払いに受け入れる通貨。 |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>2.4.6 リリース以降、 [[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨（廃止予定）になり、に置き換えられました [[!DNL Fixer API] （APILayer）](https://apilayer.com/marketplace/fixer-api) サービス。 非推奨（廃止予定）ではなく、APILayer アカウントを使用することを強くお勧めします [!DNL Fixer.io] アカウント。

![通貨設定 > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | を通じて変換サービスにアクセスするために使用されるキー [!DNL fixer.io] アカウント。 詳しくは、を参照してください [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | Fixer.io セッションがタイムアウトするまでの非アクティブな時間（秒）を指定します。 デフォルト値 `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![通貨設定/Fixer Api （APILayer）](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | を通じて変換サービスにアクセスするために使用されるキー [!DNL APILayer] アカウント。 詳しくは、を参照してください [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | 次の時間（前に非アクティブであった秒数）を決定します [!DNL APILayer] セッションがタイムアウトします。 デフォルト値は `100`. |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![通貨の設定/通貨換算 API](./assets/currency-setup-converter.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | 変換サービスへのアクセスに使用するキー。 詳しくは、を参照してください [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | 次の時間（前に非アクティブであった秒数）を決定します [!DNL Currency Converter] セッションがタイムアウトします。 デフォルト値`100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![通貨設定/予定インポート設定](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | 通貨レートに対してスケジュール済インポートが有効かどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Service] | ストア表示 | スケジュールされたインポートのデータを提供するサービスを指定します。 デフォルト値は `fixer.io` |
| [!UICONTROL Start Time] | ストア表示 | 開始時間を時間、分、秒で示します（24 時間形式）。 |
| [!UICONTROL Frequency] | ストア表示 | スケジュールされた読み込みの実行頻度を決定します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | ストア表示 | スケジュールされた読み込みエラーについてメールで通知される各ユーザーのメールアドレスを識別します。 受信者が複数の場合は、各エントリをコンマで区切ります。 |
| [!UICONTROL Error Email Sender] | Web サイト | エラーメール通知の送信者として表示される店舗連絡先を識別します。 既定の送信者： `General Contact` |
| [!UICONTROL Error Email Template] | Web サイト | エラーメール通知の基礎として使用するテンプレートを指定します。 デフォルトのテンプレート： `Currency Update Warnings` |

{style="table-layout:auto"}
