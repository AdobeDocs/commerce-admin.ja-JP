---
title: 通貨の設定
description: 基本通貨の範囲の設定、受け入れる通貨の指定方法、価格表示に使用する通貨について説明します。
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# 通貨の設定

個々の通貨レートを設定する前に、まず [基準通貨](../configuration-reference/general/currency-setup.md). デフォルトではグローバルに設定されているので、基本通貨設定が全体に適用されます [ストア階層](../getting-started/websites-stores-views.md). マルチサイト Adobe CommerceまたはMagento Open Sourceのインストールがある場合は、スコープを web サイトレベルに設定することで、複数の基本通貨を管理できます。

また、受け入れる通貨と、の表示に使用する通貨も指定します [価格](../catalog/catalog-price-scope.md) あなたの店で。 次の図では、基本通貨の範囲が web サイトレベルで設定されているので、各 web サイトが異なる基本通貨を持つことができます。

![通貨範囲図](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## 手順 1：使用可能な通貨の選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左上隅にを設定します **[!UICONTROL Scope]** を設定が適用されるストア表示に変更します。

1. の下の左パネルで _一般_、を選択 **[!UICONTROL Currency Setup]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Currency Options]** を選択し、次のオプションを設定します。

   - **[!UICONTROL Base Currency]** - オンライン取引に使用する主要通貨に設定します。

   - **[!UICONTROL Default Display Currency]** — ストア表示で価格を表示するために使用する通貨に設定します。

   - **[!UICONTROL Allowed Currencies]** - ストア表示で支払として受け入れるすべての通貨を選択します。 主要通貨も必ず選択してください。

     複数通貨の場合は、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   ![一般設定 – 通貨オプション](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、を参照してください。 [通貨オプション](../configuration-reference/general/currency-setup.md) が含まれる _設定リファレンスガイド_.

1. キャッシュを更新するように求められたら、 _閉じる_ （ ![クローズボックス](../assets/icon-close-x.png) ）を選択します。

   次のことができます [キャッシュの更新](../systems/cache-management.md) 後で。

1. 基本通貨の範囲を定義します。

   - 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

   - 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Price]** セクション。 （このセクションは、範囲がに設定されている場合にのみ表示されます。 **[!UICONTROL Store View:]** _デフォルトの設定_.）

   - を設定 **[!UICONTROL Catalog Price Scope]** 次のいずれか `Global` または `Website`.

   ![カタログの設定 – 価格オプション](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## 手順 2：読み込み接続の設定

1. ページの先頭までスクロールします。

1. 左側のパネルで、を展開します **[!UICONTROL General]** を選択します **[!UICONTROL Currency Setup]**.

1. 通貨サービス接続の設定：

   次の 3 つのサービスオプションがあります。 _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_、および _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >2.4.6 リリース以降、 [[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨（廃止予定）になり、に置き換えられました [[!DNL Fixer API] （APILayer）](https://apilayer.com/marketplace/fixer-api) サービス。 非推奨（廃止予定）ではなく、APILayer アカウントを使用することを強くお勧めします [!DNL Fixer.io] アカウント。

   - _に接続するには [fixer.io サービス](https://fixer.io/):_

      - を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Fixer.io]** セクション。

      - fixer.io を入力 **[!UICONTROL API key]**.

      - の場合 **[!UICONTROL Connection Timeout in Seconds]**：非アクティブになってから接続がタイムアウトするまでの時間（秒数）を入力します。

     ![一般設定 – 通貨の設定 – Fixer.io オプション](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _に接続するには [[!DNL Fixer Api (APILayer)] サービス](https://apilayer.com/):_

      - を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Fixer Api (APILayer)]** セクション。

      - を入力 [!DNL APILayer] **[!UICONTROL API key]**.

      - の場合 **[!UICONTROL Connection Timeout in Seconds]**：非アクティブになってから接続がタイムアウトするまでの時間（秒数）を入力します。

     ![一般設定 – 通貨の設定 – Fixer API （APILayer）オプション](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _に接続するには [[!DNL Currency Convertor API] サービス](https://free.currencyconverterapi.com/):_

      - を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Currency Convertor API]** セクション。

      - 通貨換算を入力します。 **[!UICONTROL API key]**.

      - の場合 **[!UICONTROL Connection Timeout in Seconds]**：非アクティブになってから接続がタイムアウトするまでの時間（秒数）を入力します。

     ![一般設定 – 通貨の設定 – 通貨換算 API オプション](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## 手順 3：スケジュールされた読み込み設定の指定

1. 通貨の設定を続行し、展開します ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Scheduled Import Settings]** セクション。

   ![一般設定 – 通貨スケジュール済みインポート設定](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. 通貨レートを自動的に更新するには、次のように設定します **[!UICONTROL Enabled]** 対象： `Yes`.

1. 更新オプションを設定します。

   - **[!UICONTROL Service]**  – 料金プロバイダーに設定します。 デフォルト値はです `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** — スケジュールに従ってレートを更新する時、分、秒に設定します。

   - **[!UICONTROL Frequency]** — レートが更新される頻度を決定するには、次のいずれかに設定します。

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]**  – 読み込み処理中にエラーが発生した場合にメール通知を受け取るユーザーのメールアドレスを入力します。

     複数のメールアドレスを入力する場合は、それぞれをコンマで区切ります。

   - **[!UICONTROL Error Email Sender]**  – に設定 [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) エラー通知の送信者として表示されます。

   - **[!UICONTROL Error Email Template]** — エラー通知に使用する電子メールテンプレートに設定します。

1. 完了したら、 **[!UICONTROL Save Config]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** 無効なキャッシュをリンクして更新します。

   ![システムメッセージ – 無効なキャッシュを更新します](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## 手順 4：通貨レートの更新

通貨レートを有効にするには、現在の値で更新する必要があります。 [料率の更新](currency-update.md) 手動で行うか、レートを自動的にインポートします。

## 手順 5：通貨記号のカスタマイズ（オプション）

通貨記号の管理を使用すると、ストアで支払いとして受け入れられる各通貨に関連付けられた記号をカスタマイズできます。

![通貨記号](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   ストアで有効になっている各通貨は、 _[!UICONTROL Currency]_リスト。

1. 必要に応じて、リストの設定を変更します。

   - 使用する各通貨のカスタム記号を入力するか、 **[!UICONTROL Use Standard]** 各通貨のチェックボックス。

   - 既定の記号を優先するには、 _[!UICONTROL Use Standard]_チェックボックスをオンにして、使用する記号を入力します。

   >[!NOTE]
   >
   >通貨記号の配置を左から右に変更することはできません。

1. 完了したら、 **[!UICONTROL Save Currency Symbols]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** 無効なキャッシュをリンクして更新します。
