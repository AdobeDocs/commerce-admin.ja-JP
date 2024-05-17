---
title: '[!DNL Google Tag Manager]'
description: の使用方法を学ぶ [!DNL Google Tag Manager] Adobe Commerce サイト内のマーケティングキャンペーンイベントに関連する多数のタグ（コードスニペット）を管理します。
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1142'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] マーケティングキャンペーンイベントに関連する多数のタグ（コードスニペット）を管理するのに役立ちます。 [!DNL Google Tag Manager] を使用すると、サイトにトラッキングタグを追加して、オーディエンスを測定したり、検索エンジンのマーケティング施策をパーソナライズ、リターゲティング、実施したりできます。

[!DNL Google Tag Manager] データとイベントをに直接転送します [!DNL Google Analytics]、Enhanced E コマース、その他のサードパーティの分析ソリューションを使用して、サイト、製品、プロモーションのパフォーマンスを明確に把握できます。

以下が必要です。 [!DNL Google Analytics] および [!DNL Tag Manager] このプロセスを続行する場合は、「」をクリックします。 以下の手順に従って、Google アカウントの設定、Commerce ストアの設定およびタグの作成を行います。

>[!NOTE]
>
>ビジネスが、次のようなプライバシー規制の対象となる場合 [EU 一般データ保護規則](../getting-started/compliance-gdpr.md) および/または [カリフォルニア消費者プライバシー法](../getting-started/compliance-ccpa.md)を参照してください [Google プライバシー設定](google-tools.md#google-privacy-settings).

## 手順 1. の設定 [!DNL Google Analytics] アカウント

参照： [サイト検索の設定](https://support.google.com/analytics/answer/1012264) Google ヘルプで、基礎知識を習得する必要があります。 のGoogle ガイドも参照してください [Google Analytics](https://support.google.com/analytics/answer/9304153) および [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. にログイン [!DNL Google Analytics] アカウント。

1. を有効にする **[!UICONTROL Internal Site Search Tracking]**、次の手順を実行します。

   - に移動します。 **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - を設定 **[!UICONTROL Site Search Tracking]** 対象： `On`.

   - を設定 **[!UICONTROL Query]** パラメーター先 `q`.

   - 完了すると、 **[!UICONTROL Save]** 設定。

1. 表示機能を有効にするには、次の手順を実行します。

   - を選択 **[!UICONTROL Property Settings]**.

   - 次の下 _[!UICONTROL Advertising Features]_、設定&#x200B;**[!UICONTROL Enable Demographics and Interest Reports]**対象： `On`.

   - **[!UICONTROL Save]** 設定。

1. E コマーストラッキングを有効にするには、以下を行います。

   - に移動します。 **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - を設定 **[!UICONTROL Enable Ecommerce]** 対象： `On`.

   - を設定 **[!UICONTROL Enable Enhanced Ecommerce Reporting]** 対象： `On`.

   - **[!UICONTROL Save]** 設定。

1. ページをリロードし、すべての設定が残っていることを確認します `On`.

   >[!NOTE]
   >
   >すべての設定が次に該当するわけではない場合： `On`ここまでの手順を繰り返し、ページを保存して再読み込みします。 すべての設定がに設定されるまで、この手順を繰り返します。 `On`.

## 手順 2. の設定 [!DNL Google Tag Manager] アカウント

次の手順は、基本設定を使用して新しいコンテナを設定する方法を示しています。 サンプル [コンポーザー](https://developer.adobe.com/commerce/php/development/composer/) 設定（.json）ファイルを使用すると、新しいコンテナにタグを生成するための読み込みによってプロセスを簡略化できます。 この例では、既存のコンテナを変更するのではなく、コンテナを作成することをお勧めします。

>[!NOTE]
>
>詳しくは、Googleの説明を参照してください。 [コンテナの書き出しと読み込み](https://support.google.com/tagmanager/answer/6106997). これらの手順では、サンプル JSON を新しいコンテナに読み込む手順を説明します。

1. リンクされたファイルをダウンロードします [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)をクリックし、ファイルをエディターで開き、名前を付けて保存します `GTM_M2_Config.json`.

   JSON ファイルはに直接アップロードされます。 [!DNL Google Tag Manager].

1. に移動します。 **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. クリック **[!UICONTROL Choose container file]** json ファイルを選択します。

1. 次の下 **[!UICONTROL Choose workspace]**&#x200B;を選択し、 **[!UICONTROL New]**.

1. タイトルと説明を入力し、をクリックします **[!UICONTROL Save]**.

1. ファイルをインポートするには、次のいずれかのアクションを選択します。

   - この **[!UICONTROL Overwrite]** 新しいコンテナの場合は、オプションを選択する必要があります。

   - この **[!UICONTROL Merge]** 既存のコンテナを使用している場合は、オプションを選択する必要があります。

1. クリック **[!UICONTROL Preview]** をクリックして、タグ、トリガー、変数を確認します。

1. を編集するには **[!UICONTROL Google Analytics ID]** 変数で参照されるものを使用して、次の操作を行います。

   - に移動します。 **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - を選択 **[!UICONTROL Google Analytics]** プレースホルダーを更新します（`UA-xxxxxx-x`）と独自の **[!UICONTROL GA ID]**.

1. タグ、トリガーおよび変数を新しいコンテナに追加するには、Googleの手順に従います。

   別のコンテナ内に使用する設定がある場合は、それらを新しいコンテナに移動できます。

1. クリック **[!UICONTROL Confirm]** 完了すると、

1. 新しいコンテナを公開するには、Googleの手順に従います。

## 手順 3. ストアの設定

{{gtag-api-note}}

1. Commerce ストアの管理者にログインします。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Google API]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Google Analytics]** を選択して、以下を設定します。

   ![Sales configuration - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Enable]** 対象： `Yes`.

   - を設定 **[!UICONTROL Account type]** 対象： `Google Tag Manager`.

   - が含まれる **[!UICONTROL Container ID]** フィールドに、GTM ID （`GTM-xxxxxx`）に設定します。

   - Google Analyticsを使用してコンテンツ実験も行う場合は、次のように設定します **コンテンツ実験の有効化** 対象： `Yes`.

   - 残りのフィールドにはデフォルト値を使用します。

1. 完了したら、 **[!UICONTROL Save Config]**.

1. のテスト [!DNL Google Tag Manager] 設定し、すべてが正しく機能することを確認します。

>[!NOTE]
>
>各コンテナは 1 つの web サイトに関連付けられ、アカウントごとに必要なコンテナは 1 つだけです。 マルチサイト Commerce インスタンスがある場合は、個別のコンテナが必要です。

## 手順 4. Adobe Commerce ストアに GTM コードを追加します。

1. GTM コードをコピーするには、次に移動します。 **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   Commerce サイトに追加する GTM コードスニペットは 2 つあります。1 つ目はです。 `<head>` タグと、の 2 番目 `<body>` タグ。

1. Commerce Admin で、に移動します。 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**ストア表示を編集モードで開きます。

1. 次の下 _[!UICONTROL Other Settings]_、を展開&#x200B;**[!UICONTROL HTML Head]**に、GTM からコピーしたコードをペーストします。 `<head>` 内のタグ&#x200B;**[!UICONTROL Scripts and Style Sheets]**フィールド。

   ![HTMLヘッドへのコードの挿入](./assets/head-tag.png){width="600" zoomable="yes"}

1. を展開 **[!UICONTROL Footer]** に GTM コードをペーストします。 `<body>` が含まれる **[!UICONTROL Miscellaneous HTML]** フィールド。

   ![フッターへのコードの挿入](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Configuration]**.

## フィールドの説明

| フィールド | 範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | ストア表示 | Google Analyticsの E コマース強化機能を使用して、ストア内のアクティビティを分析できるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Account type] | ストア表示 | ストアのアクティビティとトラフィックを監視するために使用されるGoogle トラッキングコードを決定します。 オプション： `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | ストア表示 | Google Analyticsの結果に表示される IP アドレスから識別情報を削除するかどうかを指定します。 |
| [!UICONTROL Enable Content Experiments] | ストア表示 | Google コンテンツ実験をアクティブ化します。同じページの異なる 10 バージョンまでテストするために使用できます。 オプション： `Yes` / `No` |
| [!UICONTROL Container Id] | ストア表示 | 次の場合 [!DNL Google Tag Manager] はストアに対して既にインストールおよび設定されており、コンテナ ID はこのフィールドに自動的に表示されます。 |
| [!UICONTROL List property for the catalog page] | ストア表示 | カタログページに関連付けられているタグマネージャープロパティを識別します。 デフォルト値 `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | ストア表示 | クロスセルブロックに関連付けられたタグマネージャープロパティを識別します。 デフォルト値 `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | ストア表示 | アップセル ブロックに関連付けられたタグ マネージャ プロパティを識別します。 デフォルト値 `Up-sell` |
| [!UICONTROL List property for the related products block] | ストア表示 | 関連する製品ブロックに関連付けられているタグマネージャープロパティを識別します。 デフォルト値 `Related Products` |
| [!UICONTROL List property for the search results page] | ストア表示 | 検索結果ページに関連付けられたタグマネージャープロパティを識別します。 デフォルト値 `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | ストア表示 | 内部プロモーションのラベルに関連付けられたタグマネージャープロパティを識別します。 デフォルト値 `Label` |

{style="table-layout:auto"}

## コンバージョンを追跡するためのタグの作成

Google AdWords アカウントをお持ちの場合は、コンバージョンを追跡するタグを作成できます。 次の例は、両方の使用方法を示しています [!DNL Google Tag Manager] および [!DNL Google Analytics] ストアのコンバージョンで実行されるタグを作成するには _成功_ ページ。

### 手順 1. タグの作成

1. にログイン [!DNL Google Tag Manager] アカウントを作成し、ストア用に作成したコンテナのリンクをクリックします。

1. が含まれる **[!UICONTROL New Tag]** ボックス、クリック **[!UICONTROL Add a new tag]**.

1. AdWords アカウントから次の情報を取得します。

   - コンバージョン ID
   - コンバージョンラベル

   サポートが必要な場合は、Googleをご覧ください [サポートサイト](https://support.google.com/tagmanager/answer/6105160).

1. から [!DNL Google Tag Manager] ダッシュボード、クリック **[!UICONTROL Google AdWords]** 次の手順を実行します。

   - タイトルプレースホルダーをクリックして、新しいタグの名前を入力します。

   - 次の下 **[!UICONTROL Choose Product]**&#x200B;を選択 **[!UICONTROL Google AdWords]**.

   - 次の下 _[!UICONTROL Choose a Tag Type]_を選択&#x200B;**[!UICONTROL AdWords Conversion Tracking]**をクリックして、**[!UICONTROL Continue]**.

1. を入力 **[!UICONTROL Conversion ID]** および **[!UICONTROL Conversion Label]** を AdWords アカウントからクリックします **[!UICONTROL Continue]**.

### 手順 2. ルールの作成

からの続行 [!DNL Google Tag Manager] ダッシュボードで次に、コンバージョンページでタグを実行するルールを作成します。

1. 次の下 **[!UICONTROL Fire On]**&#x200B;を選択し、 **[!UICONTROL Some Pages]**.

1. が含まれる _[!UICONTROL Choose Pages]_セクションで、次の設定を行います。

   - **[!UICONTROL Name]** - ページ説明の名前を入力します。

   - **[!UICONTROL Variable]** `url`

   - **操作** - `matches RegEx`

     詳しくは、 [正規表現および CSS セレクター演算子](https://support.google.com/tagmanager/answer/7679109) Google Tag Manager のヘルプで以下を行います。

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 「緑」チェックボックスをオンにし、 **[!UICONTROL Save]**.

   設定したトリガーは、[ 火の種 ] セクションに青いボタンとして表示されます。

1. 完了したら、 **[!UICONTROL Save Tag]**.

### 手順 3. プレビューと公開

プロセスの次の手順では、タグをプレビューします。 タグをプレビューするたびに、バージョンのスナップショットが保存されます。 結果に満足したら、使用するバージョンに移動し、をクリックします **[!UICONTROL Publish]**.
