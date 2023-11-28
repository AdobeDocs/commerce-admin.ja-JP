---
title: 通貨設定
description: 基本通貨の範囲の設定と、受け入れる通貨と価格表示に使用する通貨を指定する方法について説明します。
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# 通貨設定

個々の通貨レートを設定する前に、まず [基準通貨](../configuration-reference/general/currency-setup.md). デフォルトではグローバルに設定され、基本通貨設定が全体に適用されます。 [ストア階層](../getting-started/websites-stores-views.md). マルチサイトのAdobe CommerceまたはMagento Open Sourceがインストールされている場合は、範囲を Web サイトのレベルに設定することで、複数のベース通貨を管理できます。

また、受け入れる通貨と、表示に使用する通貨も指定します [価格](../catalog/catalog-price-scope.md) ストア内で使用できます。 次の図では、ベース通貨の範囲が Web サイトレベルで設定され、各 Web サイトが異なるベース通貨を持つようにできます。

![通貨スコープ図](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## 手順 1：許可された通貨を選択

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左上隅で、 **[!UICONTROL Scope]** を、設定が適用されるストア表示に追加します。

1. の下の左側のパネル _一般_&#x200B;を選択します。 **[!UICONTROL Currency Setup]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Currency Options]** 」セクションで、次のオプションを設定します。

   - **[!UICONTROL Base Currency]**  — オンライントランザクションに使用する主要通貨に設定します。

   - **[!UICONTROL Default Display Currency]**  — ストア表示で価格を表示する際に使用する通貨に設定します。

   - **[!UICONTROL Allowed Currencies]**  — 店舗表示で、支払として受け入れるすべての通貨を選択します。 また、主通貨も必ず選択してください。

     複数の通貨の場合は、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

   ![一般設定 — 通貨オプション](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、 [通貨オプション](../configuration-reference/general/currency-setup.md) （内） _設定リファレンスガイド_.

1. キャッシュを更新するよう求められたら、 _閉じる_ ( ![ボックスを閉じる](../assets/icon-close-x.png) ) をクリックします。

   以下が可能です。 [キャッシュの更新](../systems/cache-management.md) 後で。

1. 基準通貨の範囲を定義します。

   - 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

   - 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Price]** 」セクションに入力します。 ( このセクションは、スコープが **[!UICONTROL Store View:]** _デフォルトの設定_.)

   - 設定 **[!UICONTROL Catalog Price Scope]** 次のいずれかを実行します。 `Global` または `Website`.

   ![カタログ構成 — 価格オプション](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## 手順 2：インポート接続を設定する

1. ページの上部までスクロールします。

1. 左側のパネルで、を展開します。 **[!UICONTROL General]** を選択します。 **[!UICONTROL Currency Setup]**.

1. 通貨サービス接続を設定します。

   次の 3 つのサービスオプションがあります。 _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_、および _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >2.4.6 リリース以降、 [[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨となり、 [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) サービス。 非推奨の [!DNL Fixer.io] アカウント。

   - _に接続するには、以下を実行します。 [fixer.io サービス](https://fixer.io/):_

      - 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Fixer.io]** 」セクションに入力します。

      - fixer.io を入力してください **[!UICONTROL API key]**.

      - の場合 **[!UICONTROL Connection Timeout in Seconds]**&#x200B;に設定されている場合は、無操作状態が続いてから接続がタイムアウトするまでの時間（秒）を入力します。

     ![一般設定 — 通貨設定 — Fixer.io オプション](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _に接続するには、以下を実行します。 [[!DNL Fixer Api (APILayer)] サービス](https://apilayer.com/):_

      - 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Fixer Api (APILayer)]** 」セクションに入力します。

      - を入力します。 [!DNL APILayer] **[!UICONTROL API key]**.

      - の場合 **[!UICONTROL Connection Timeout in Seconds]**&#x200B;に設定されている場合は、無操作状態が続いてから接続がタイムアウトするまでの時間（秒）を入力します。

     ![一般設定 — 通貨の設定 — 固定 API(APILayer) オプション](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _に接続するには、以下を実行します。 [[!DNL Currency Convertor API] サービス](https://free.currencyconverterapi.com/):_

      - 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Currency Convertor API]** 」セクションに入力します。

      - 通貨コンバータを入力 **[!UICONTROL API key]**.

      - の場合 **[!UICONTROL Connection Timeout in Seconds]**&#x200B;に設定されている場合は、無操作状態が続いてから接続がタイムアウトするまでの時間（秒）を入力します。

     ![一般的な設定 — 通貨の設定 — 通貨コンバーター API オプション](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## 手順 3：スケジュールされたインポート設定を指定する

1. 通貨設定を続行し、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Scheduled Import Settings]** 」セクションに入力します。

   ![一般設定 — 通貨予定インポート設定](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. 通貨レートを自動的に更新するには、 **[!UICONTROL Enabled]** から `Yes`.

1. 更新オプションを設定します。

   - **[!UICONTROL Service]**  — レート・プロバイダに設定します。 デフォルト値は `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** ：スケジュールに従って料金が更新される時間、分、秒に設定します。

   - **[!UICONTROL Frequency]**  — レートが更新される頻度を判断するには、次のいずれかに設定します。

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]**  — インポートプロセス中にエラーが発生した場合に電子メール通知を受け取る人の電子メールアドレスを入力します。

     複数の電子メールアドレスを入力する場合は、それぞれをコンマで区切ります。

   - **[!UICONTROL Error Email Sender]**  — に設定します。 [ストア連絡先](../getting-started/store-details.md#store-email-addresses) エラー通知の送信者として表示される

   - **[!UICONTROL Error Email Template]**  — エラー通知に使用する電子メールテンプレートに設定します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** 無効なキャッシュをリンクして更新します。

   ![システムメッセージ — 無効なキャッシュを更新します](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## 手順 4：通貨レートの更新

通貨レートは、有効にする前に、現在の値で更新する必要があります。 [レートの更新](currency-update.md) 手動で、またはレートを自動的にインポートする場合。

## 手順 5：通貨記号のカスタマイズ（オプション）

通貨記号の管理を使用すると、ストアで支払いとして受け入れられる各通貨に関連付けられた記号をカスタマイズできます。

![通貨記号](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   ストアに対して有効になっている各通貨が、 _[!UICONTROL Currency]_リスト。

1. 必要に応じて、リストの設定を変更します。

   - 使用する各通貨のカスタム記号を入力するか、 **[!UICONTROL Use Standard]** チェックボックスをオンにします。

   - 既定のシンボルを上書きするには、 _[!UICONTROL Use Standard]_」チェックボックスにチェックを入れ、使用する記号を入力します。

   >[!NOTE]
   >
   >通貨記号の配置を左から右に変更することはできません。

1. 完了したら、「 **[!UICONTROL Save Currency Symbols]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** 無効なキャッシュをリンクして更新します。
