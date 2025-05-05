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

個々の通貨レートを設定する前に、まず [ 基本通貨 ](../configuration-reference/general/currency-setup.md) の範囲を設定する必要があります。 デフォルトではグローバルに設定されており、基本通貨設定が [ ストア階層 ](../getting-started/websites-stores-views.md) 全体に適用されます。 マルチサイト Adobe CommerceまたはMagento Open Sourceのインストールがある場合は、スコープを web サイトレベルに設定することで、複数の基本通貨を管理できます。

また、受け入れる通貨と、ストアでの [ 価格 ](../catalog/catalog-price-scope.md) の表示に使用する通貨も指定します。 次の図では、基本通貨の範囲が web サイトレベルで設定されているので、各 web サイトが異なる基本通貨を持つことができます。

![ 通貨スコープ図 ](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## 手順 1：使用可能な通貨の選択

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左上隅の **[!UICONTROL Scope]** を、設定が適用されるストア表示に設定します。

1. 左側のパネルの _一般_ で、「**[!UICONTROL Currency Setup]**」を選択します。

1. **[!UICONTROL Currency Options]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、次のオプションを設定します。

   - **[!UICONTROL Base Currency]**：オンライン取引に使用する主要通貨に設定します。

   - **[!UICONTROL Default Display Currency]**：ストア表示で価格を表示するために使用する通貨に設定します。

   - **[!UICONTROL Allowed Currencies]** - ストア表示で支払いとして受け入れるすべての通貨を選択します。 主要通貨も必ず選択してください。

     複数通貨の場合は、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   ![ 一般設定 – 通貨オプション ](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、『 [ 設定リファレンスガイド _の ](../configuration-reference/general/currency-setup.md) 通貨オプション_ を参照してください。

1. キャッシュを更新するように求められたら、システムメッセージの右上隅にある _閉じる_ （![ 閉じるボックス ](../assets/icon-close-x.png)）をクリックします。

   後で [ キャッシュを更新 ](../systems/cache-management.md) できます。

1. 基本通貨の範囲を定義します。

   - 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

   - 下にスクロールして、「**[!UICONTROL Price]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。 （このセクションは、範囲が **[!UICONTROL Store View:]** _デフォルト設定_ に設定されている場合にのみ表示されます。

   - **[!UICONTROL Catalog Price Scope]** を `Global` または `Website` に設定します。

   ![ カタログの設定 – 価格オプション ](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## 手順 2：読み込み接続の設定

1. ページの先頭までスクロールします。

1. 左側のパネルで「**[!UICONTROL General]**」を展開し、「**[!UICONTROL Currency Setup]**」を選択します。

1. 通貨サービス接続の設定：

   サービスオプションには、_[!UICONTROL Fixer.io (legacy)]_、_[!UICONTROL Fixer Api (APILayer)]_、_[!UICONTROL Currency Converter API]_&#x200B;の 3 つがあります

   >[!IMPORTANT]
   >
   >2.4.6 リリース以降、[[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨（廃止予定）となり、[[!DNL Fixer API]  （APILayer） ](https://apilayer.com/marketplace/fixer-api) サービスに置き換わります。 非推奨の [!DNL Fixer.io] アカウントではなく、APILayer アカウントを使用することを強くお勧めします。

   - _[fixer.io サービスに接続するには ](https://fixer.io/):_

      - 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Fixer.io]**」セクションを展開します。

      - fixer.io **[!UICONTROL API key]** を入力します。

      - **[!UICONTROL Connection Timeout in Seconds]**：非アクティブになってから接続がタイムアウトになるまでの時間（秒数）を入力します。

     ![ 一般設定 – 通貨の設定 – Fixer.io オプション ](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _[[!DNL Fixer Api (APILayer)]  サービス ](https://apilayer.com/) に接続するには：_

      - 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Fixer Api (APILayer)]**」セクションを展開します。

      - [!DNL APILayer] **[!UICONTROL API key]** を入力します。

      - **[!UICONTROL Connection Timeout in Seconds]**：非アクティブになってから接続がタイムアウトになるまでの時間（秒数）を入力します。

     ![ 一般設定 – 通貨の設定 – Fixer API （APILayer）オプション ](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _[[!DNL Currency Convertor API]  サービス ](https://free.currencyconverterapi.com/) に接続するには：_

      - 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Currency Convertor API]**」セクションを展開します。

      - 通貨換算 **[!UICONTROL API key]** を入力します。

      - **[!UICONTROL Connection Timeout in Seconds]**：非アクティブになってから接続がタイムアウトになるまでの時間（秒数）を入力します。

     ![ 一般設定 – 通貨の設定 – 通貨換算 API オプション ](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## 手順 3：スケジュールされた読み込み設定の指定

1. 通貨の設定を続行して、**[!UICONTROL Scheduled Import Settings]** のセクションの ![ 拡張セレクター ](../assets/icon-display-expand.png) を展開します。

   ![ 一般設定 – 通貨スケジュール済みインポート設定 ](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. 通貨レートを自動的に更新するには、**[!UICONTROL Enabled]** を `Yes` に設定します。

1. 更新オプションを設定します。

   - 「**[!UICONTROL Service]**」 – 評価プロバイダに設定します。 デフォルト値は `Fixer.io (legacy)` です。

   - **[!UICONTROL Start Time]**：スケジュールに従ってレートを更新する時間、分、秒に設定します。

   - **[!UICONTROL Frequency]**：レートの更新頻度を決定するには、次のいずれかに設定します。

      - `Daily`
      - `Weekly`
      - `Monthly`

   - 「**[!UICONTROL Error Email Recipient]**」 – 読み込みプロセス中にエラーが発生した場合にメール通知を受け取るユーザーのメールアドレスを入力します。

     複数のメールアドレスを入力する場合は、それぞれをコンマで区切ります。

   - **[!UICONTROL Error Email Sender]** - エラー通知の送信者として表示される [ ストア連絡先 ](../getting-started/store-details.md#store-email-addresses) に設定します。

   - 「**[!UICONTROL Error Email Template]**」 – エラー通知に使用するメールテンプレートに設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. キャッシュを更新するように求められたら、**[!UICONTROL Cache Management]** のリンクをクリックして無効なキャッシュを更新します。

   ![ システムメッセージ – 無効なキャッシュを更新します ](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## 手順 4：通貨レートの更新

通貨レートを有効にするには、現在の値で更新する必要があります。 [ 料率を更新 ](currency-update.md) 手動で、または料率を自動的にインポートします。

## 手順 5：通貨記号のカスタマイズ（オプション）

通貨記号の管理を使用すると、ストアで支払いとして受け入れられる各通貨に関連付けられた記号をカスタマイズできます。

![ 通貨記号 ](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Currency]_/**[!UICONTROL Currency Symbols]**&#x200B;に移動します。

   ストアで有効になっている各通貨が _[!UICONTROL Currency]_&#x200B;リストに表示されます。

1. 必要に応じて、リストの設定を変更します。

   - 使用する各通貨のカスタム記号を入力するか、各通貨の「**[!UICONTROL Use Standard]**」チェックボックスを選択します。

   - デフォルトのシンボルをオーバーライドするには、「_[!UICONTROL Use Standard]_」チェックボックスをオフにして、使用するシンボルを入力します。

   >[!NOTE]
   >
   >通貨記号の配置を左から右に変更することはできません。

1. 完了したら、「**[!UICONTROL Save Currency Symbols]**」をクリックします。

1. キャッシュを更新するように求められたら、**[!UICONTROL Cache Management]** のリンクをクリックして無効なキャッシュを更新します。
