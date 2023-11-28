---
title: '[!DNL Google Tag Manager]'
description: 使用方法を学ぶ [!DNL Google Tag Manager] :Adobe Commerceサイトのマーケティングキャンペーンイベントに関連する様々なタグ（コードスニペット）を管理します。
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] は、マーケティングキャンペーンイベントに関連する様々なタグ（コードスニペット）の管理に役立ちます。 [!DNL Google Tag Manager] を使用すると、サイトにトラッキングタグを追加して、オーディエンスを測定したり、検索エンジンのマーケティング戦略をパーソナライズ、再ターゲット化または実行したりできます。

[!DNL Google Tag Manager] データとイベントをに直接転送する [!DNL Google Analytics]を使用して、e コマースやその他のサードパーティの分析ソリューションを強化し、サイト、製品、プロモーションのパフォーマンスを明確に把握できます。

次のアクティビティが必要です： [!DNL Google Analytics] および [!DNL Tag Manager] アカウントを使用してこのプロセスを続行します。 以下の手順では、Googleアカウントの設定、コマースストアの設定、タグの作成のプロセスについて説明します。

>[!NOTE]
>
>お客様のビジネスが [EU 一般データ保護規則](../getting-started/compliance-gdpr.md) および/または [カリフォルニア州消費者プライバシー法](../getting-started/compliance-ccpa.md)を参照してください。 [Google Privacy Settings](google-tools.md#google-privacy-settings).

## 手順 1. を設定します。 [!DNL Google Analytics] アカウント

詳しくは、 [サイト検索の設定](https://support.google.com/analytics/answer/1012264) Googleヘルプで、を使い始めるために必要な基本事項を確認できます。 詳しくは、 Googleガイド ( [Google Analytics](https://support.google.com/analytics/answer/9304153) および [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. ログイン先： [!DNL Google Analytics] アカウント。

1. 有効にするには **[!UICONTROL Internal Site Search Tracking]**、次の操作を実行します。

   - に移動します。 **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - 設定 **[!UICONTROL Site Search Tracking]** から `On`.

   - 設定 **[!UICONTROL Query]** パラメーター `q`.

   - 完了したら、 **[!UICONTROL Save]** 設定を指定します。

1. 表示機能を有効にするには、次の操作を行います。

   - 選択 **[!UICONTROL Property Settings]**.

   - の下 _[!UICONTROL Advertising Features]_，設定&#x200B;**[!UICONTROL Enable Demographics and Interest Reports]**から `On`.

   - **[!UICONTROL Save]** 設定を指定します。

1. e コマーストラッキングを有効にするには、以下の手順を実行します。

   - に移動します。 **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - 設定 **[!UICONTROL Enable Ecommerce]** から `On`.

   - 設定 **[!UICONTROL Enable Enhanced Ecommerce Reporting]** から `On`.

   - **[!UICONTROL Save]** 設定を指定します。

1. ページを再読み込みし、すべての設定が残っていることを確認します。 `On`.

   >[!NOTE]
   >
   >一部の設定が `On`、前の手順を繰り返し、保存して、ページを再読み込みします。 すべての設定がに設定されるまで、この手順を繰り返します。 `On`.

## 手順 2. を設定します。 [!DNL Google Tag Manager] アカウント

以下の手順は、基本設定を使用して新しいコンテナを設定する方法を示しています。 サンプル [コンポーザー](https://developer.adobe.com/commerce/php/development/composer/) 設定 (.json) ファイルを使用してプロセスを簡略化し、読み込んで新しいコンテナにタグを生成します。 この例では、既存のコンテナを変更するのではなく、コンテナを作成することをお勧めします。

>[!NOTE]
>
>詳しくは、「 Googleの使用」を参照してください。 [コンテナのエクスポートとインポート](https://support.google.com/tagmanager/answer/6106997). これらの手順では、新しいコンテナにサンプル JSON を読み込むための手順を示します。

1. リンクされたファイルをダウンロード [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)をクリックし、エディターでファイルを開き、 `GTM_M2_Config.json`.

   JSON ファイルは次に直接アップロードされます： [!DNL Google Tag Manager].

1. に移動します。 **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. クリック **[!UICONTROL Choose container file]** json ファイルを選択します。

1. の下 **[!UICONTROL Choose workspace]**&#x200B;をクリックし、 **[!UICONTROL New]**.

1. タイトルと説明を入力し、「 **[!UICONTROL Save]**.

1. ファイルをインポートするには、次のいずれかの操作を選択します。

   - The **[!UICONTROL Overwrite]** 新しいコンテナに対してオプションを選択する必要があります。

   - The **[!UICONTROL Merge]** 既存のコンテナを使用する場合は、オプションを選択する必要があります。

1. クリック **[!UICONTROL Preview]** をクリックして、タグ、トリガー、変数を確認します。

1. 次の手順で **[!UICONTROL Google Analytics ID]** 変数で参照されるを、以下の手順に従います。

   - に移動します。 **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - 選択 **[!UICONTROL Google Analytics]** プレースホルダーを更新 (`UA-xxxxxx-x`) を使用して、独自の **[!UICONTROL GA ID]**.

1. Googleの新しいコンテナにタグ、トリガー、変数を追加する手順に従います。

   使用する別のコンテナに設定がある場合は、その設定を新しいコンテナに移動できます。

1. クリック **[!UICONTROL Confirm]** 完了したら、

1. Googleでの新しいコンテナの公開手順に従います。

## 手順 3. ストアを設定

{{gtag-api-note}}

1. コマースストアの管理者にログインします。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Google API]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Google Analytics]** セクションで、以下を設定します。

   ![販売構成 —Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Enable]** から `Yes`.

   - 設定 **[!UICONTROL Account type]** から `Google Tag Manager`.

   - Adobe Analytics の **[!UICONTROL Container ID]** フィールドに、GTM ID を入力します (`GTM-xxxxxx`) をクリックします。

   - コンテンツ実験にもGoogle Analyticsを使用する場合は、 **Content Experiment を有効にする** から `Yes`.

   - 残りのフィールドにはデフォルト値を使用します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. テストする [!DNL Google Tag Manager] を設定し、すべてが正しく動作することを確認します。

>[!NOTE]
>
>各コンテナは 1 つの Web サイトに関連付けられ、アカウントごとに 1 つのコンテナのみが必要です。 マルチサイトコマースインスタンスがある場合は、別々のコンテナが必要です。

## 手順 4. GTM コードをAdobe Commerceストアに追加する

1. GTM コードをコピーするには、に移動します。 **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   コマースサイトに追加する GTM コードスニペットは 2 つあります。最初のスニペットは、 `<head>` タグと、2 つ目のタグが `<body>` タグを使用します。

1. コマース管理で、に移動します。 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**をクリックし、編集モードでストア表示を開きます。

1. の下 _[!UICONTROL Other Settings]_、展開&#x200B;**[!UICONTROL HTML Head]**GTM からコピーしたコードを、 `<head>` タグを&#x200B;**[!UICONTROL Scripts and Style Sheets]**フィールドに入力します。

   ![HTMLヘッドへのコードの挿入](./assets/head-tag.png){width="600" zoomable="yes"}

1. 展開 **[!UICONTROL Footer]** の GTM コードを貼り付けます。 `<body>` （内） **[!UICONTROL Miscellaneous HTML]** フィールドに入力します。

   ![フッターへのコードの挿入](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Configuration]**.

## フィールドの説明

| フィールド | 範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | ストア表示 | 拡張 e コマースGoogle Analyticsをストア内のアクティビティの分析に使用できるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Account type] | ストア表示 | ストアのアクティビティとトラフィックの監視に使用するGoogleトラッキングコードを決定します。 オプション： `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | ストア表示 | [Google Analytics] の結果に表示される IP アドレスから識別情報を削除するかどうかを指定します。 |
| [!UICONTROL Enable Content Experiments] | ストア表示 | Google Content Experiment をアクティベートします。この実験を使用して、同じページの最大 10 個の異なるバージョンのテストをおこなうことができます。 オプション： `Yes` / `No` |
| [!UICONTROL Container Id] | ストア表示 | 次の場合 [!DNL Google Tag Manager] が既にインストールされ、お使いのストア用に設定されている場合は、コンテナ ID がこのフィールドに自動的に表示されます。 |
| [!UICONTROL List property for the catalog page] | ストア表示 | カタログページに関連付けられているタグマネージャープロパティを識別します。 デフォルト値： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | ストア表示 | クロス販売ブロックに関連付けられた Tag Manager プロパティを識別します。 デフォルト値： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | ストア表示 | アップセルブロックに関連付けられているタグマネージャープロパティを識別します。 デフォルト値： `Up-sell` |
| [!UICONTROL List property for the related products block] | ストア表示 | 関連する products ブロックに関連付けられている Tag Manager プロパティを識別します。 デフォルト値： `Related Products` |
| [!UICONTROL List property for the search results page] | ストア表示 | 検索結果ページに関連付けられているタグマネージャープロパティを識別します。 デフォルト値： `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | ストア表示 | 内部プロモーションのラベルに関連付けられているタグマネージャープロパティを識別します。 デフォルト値： `Label` |

{style="table-layout:auto"}

## コンバージョンを追跡するためのタグの作成

Google AdWords アカウントを持っている場合は、コンバージョンを追跡するタグを作成できます。 次の例は、 [!DNL Google Tag Manager] および [!DNL Google Analytics] ストアのコンバージョン時に実行されるタグを作成するには、以下を実行します。 _成功_ ページに貼り付けます。

### 手順 1. タグの作成

1. にログインします。 [!DNL Google Tag Manager] アカウントに移動し、ストア用に作成したコンテナのリンクをクリックします。

1. Adobe Analytics の **[!UICONTROL New Tag]** ボックス、 **[!UICONTROL Add a new tag]**.

1. AdWords アカウントから次の情報を取得します。

   - コンバージョン ID
   - コンバージョンラベル

   不明な点がある場合は、Googleの [サポートサイト](https://support.google.com/tagmanager/answer/6105160).

1. 次から： [!DNL Google Tag Manager] ダッシュボードで、 **[!UICONTROL Google AdWords]** 次の操作を実行します。

   - タイトルプレースホルダーをクリックし、新しいタグの名前を入力します。

   - の下 **[!UICONTROL Choose Product]**&#x200B;を選択します。 **[!UICONTROL Google AdWords]**.

   - の下 _[!UICONTROL Choose a Tag Type]_を選択します。**[!UICONTROL AdWords Conversion Tracking]**をクリックします。**[!UICONTROL Continue]**.

1. 次を入力します。 **[!UICONTROL Conversion ID]** および **[!UICONTROL Conversion Label]** をクリックし、 **[!UICONTROL Continue]**.

### 手順 2. ルールの作成

次から続行： [!DNL Google Tag Manager] ダッシュボードを使用する場合、次の手順では、コンバージョンページ上のタグを実行するルールを作成します。

1. の下 **[!UICONTROL Fire On]**&#x200B;をクリックし、 **[!UICONTROL Some Pages]**.

1. Adobe Analytics の _[!UICONTROL Choose Pages]_セクションで、次の設定を実行します。

   - **[!UICONTROL Name]**  — ページの説明の名前を入力します。

   - **[!UICONTROL Variable]** `url`

   - **操作** - `matches RegEx`

     詳しくは、 [正規表現と CSS セレクターの演算子](https://support.google.com/tagmanager/answer/7679109) ( Google Tag Manager ヘルプ ) を参照してください。

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 緑のチェックボックスを選択し、 **[!UICONTROL Save]**.

   設定したトリガーは、「火の場所」セクションに青いボタンで表示されます。

1. 完了したら、「 **[!UICONTROL Save Tag]**.

### 手順 3. プレビューと公開

プロセスの次の手順は、タグをプレビューすることです。 タグがプレビューされるたびに、バージョンのスナップショットが保存されます。 満足できる結果が得られたら、使用するバージョンに移動し、 **[!UICONTROL Publish]**.
