---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: 次のページで設定を確認します： [!UICONTROL General] &gt; [!UICONTROL Currency Setup] コマース管理のページ。
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 2%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>詳しくは、 [通貨設定](../../stores-purchase/currency-configuration.md) を参照してください。

## [!UICONTROL Currency Options]

![「通貨設定」>「通貨オプション」](./assets/currency-setup-currency-options.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Web サイト | すべてのオンライン支払トランザクションに使用される主要通貨。 複数のストア表示の場合、価格の範囲を [カタログ](../catalog/catalog.md) 設定。 |
| [!UICONTROL Default Display Currency] | ストア表示 | 価格の表示に使用する主要通貨。 |
| [!UICONTROL Allowed Currencies] | ストア表示 | ストアが支払いに受け入れた通貨。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>2.4.6 リリース以降、 [[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨となり、 [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) サービス。 非推奨の [!DNL Fixer.io] アカウント。

![通貨設定 > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | を使用して変換サービスにアクセスするためのキー [!DNL fixer.io] アカウント。 詳しくは、 [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | Fixer.io セッションがタイムアウトするまでの無操作状態の秒数を指定します。 デフォルト値： `100` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Fixer Api (APILayer)]

![通貨設定/修正者 Api (APIayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | を使用して変換サービスにアクセスするためのキー [!DNL APILayer] アカウント。 詳しくは、 [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | 無操作状態が続くまでの時間（秒）を指定します [!DNL APILayer] セッションがタイムアウトしました。 デフォルト値は `100`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Currency Converter API]

![通貨設定/通貨換算 API](./assets/currency-setup-converter.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | 変換サービスへのアクセスに使用するキー。 詳しくは、 [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | 無操作状態が続くまでの時間（秒）を指定します [!DNL Currency Converter] セッションがタイムアウトしました。 デフォルト値：`100` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Scheduled Import Settings]

![「通貨設定」>「予定インポート設定」](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | 予定されているインポートで通貨レートが有効かどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Service] | ストア表示 | スケジュールされたインポートのデータを提供するサービスを指定します。 デフォルト値は です。`fixer.io` |
| [!UICONTROL Start Time] | ストア表示 | 24 時間形式の時計に基づいて、開始時刻を時間、分、秒単位で示します。 |
| [!UICONTROL Frequency] | ストア表示 | スケジュールされたインポートの実行頻度を決定します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | ストア表示 | スケジュールされたインポートエラーに関する電子メールで通知を受け取る各人の電子メールアドレスを識別します。 複数の受信者の場合、各エントリはコンマで区切ります。 |
| [!UICONTROL Error Email Sender] | Web サイト | エラーの E メール通知の送信者として表示されるストアの連絡先を識別します。 デフォルトの送信者： `General Contact` |
| [!UICONTROL Error Email Template] | Web サイト | エラーの電子メール通知の基礎として使用するテンプレートを指定します。 デフォルトのテンプレート： `Currency Update Warnings` |

{:style=&quot;table-layout:auto&quot;}
