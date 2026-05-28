---
title: '[!UICONTROL General] > [!UICONTROL Currency Setup]'
description: Commerce管理者の[!UICONTROL General] > [!UICONTROL Currency Setup] ページで設定を確認します。
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>これらの設定について詳しくは、[通貨設定](../../stores-purchase/currency-configuration.md)を参照してください。

## [!UICONTROL Currency Options]

![通貨設定/通貨オプション ](./assets/currency-setup-currency-options.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Base Currency] | web サイト | すべてのオンライン決済トランザクションに使用される主要通貨。 複数のストアビューの場合、価格の範囲は[ カタログ ](../catalog/catalog.md)設定で設定する必要があります。 |
| [!UICONTROL Default Display Currency] | ストアビュー | 価格の表示に使用される主要通貨。 |
| [!UICONTROL Allowed Currencies] | ストアビュー | 支払いのためにストアが受け入れた通貨。 |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>2.4.6 リリース以降、[[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨となり、[[!DNL Fixer API]  （APILayer） ](https://apilayer.com/marketplace/fixer-api) サービスに置き換えられます。 非推奨の[!DNL Fixer.io] アカウントの代わりにAPILayer アカウントを使用することを強くお勧めします。

![通貨設定> Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | [!DNL fixer.io] アカウントを介してコンバージョンサービスにアクセスするために使用されるキー。 詳しくは、[[!DNL fixer.io]](https://fixer.io/)を参照してください。 |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | Fixer.io セッションがタイムアウトするまでの非アクティブな時間の秒数を指定します。 デフォルト値：`100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![通貨設定/Fixer Api （APILayer） ](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | [!DNL APILayer] アカウントを介してコンバージョンサービスにアクセスするために使用されるキー。 詳しくは、[[!DNL APILayer]](https://apilayer.com/)を参照してください。 |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | [!DNL APILayer] セッションがタイムアウトするまでの非アクティブな時間の秒数を指定します。 デフォルト値は`100`です。 |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![通貨設定/通貨変換API](./assets/currency-setup-converter.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API key] | グローバル | コンバージョンサービスへのアクセスに使用されるキー。 詳しくは、[[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/)を参照してください。 |
| [!UICONTROL Connection Timeout in Seconds] | グローバル | [!DNL Currency Converter] セッションがタイムアウトするまでの非アクティブな時間の秒数を指定します。 デフォルト値：`100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![通貨設定/スケジュールされた読み込み設定](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストアビュー | 通貨レートに対してスケジュールされた読み込みが有効かどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Service] | ストアビュー | スケジュールされた読み込み用のデータを提供するサービスを指定します。 デフォルト値は`fixer.io`です |
| [!UICONTROL Start Time] | ストアビュー | 24時間の時計に基づいて、開始時間を時間、分、秒で示します。 |
| [!UICONTROL Frequency] | ストアビュー | スケジュールされた読み込みが実行される頻度を指定します。 オプション：`Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | ストアビュー | スケジュールされたインポートエラーについて電子メールで通知される各人物の電子メールアドレスを識別します。 複数の受信者の場合は、各エントリをコンマで区切ります。 |
| [!UICONTROL Error Email Sender] | web サイト | エラー電子メール通知の送信者として表示されるストア連絡先を識別します。 既定の送信者：`General Contact` |
| [!UICONTROL Error Email Template] | web サイト | エラーメール通知の基として使用されるテンプレートを指定します。 既定のテンプレート：`Currency Update Warnings` |

{style="table-layout:auto"}
