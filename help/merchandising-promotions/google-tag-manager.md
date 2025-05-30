---
title: '[!DNL Google Tag Manager]'
description: を使用して  [!DNL Google Tag Manager] Adobe Commerce サイトのマーケティングキャンペーンイベントに関連する多数のタグ（コードスニペット）を管理する方法を説明します。
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 22a619db0b0673dc520b9bdc5d6cd0c8ffecdf08
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] は、マーケティングキャンペーンイベントに関連付けられた様々なタグ（コードスニペット）を効率的に管理およびデプロイするのに役立つ強力なツールです。 [!DNL Google Tag Manager] を使用すると、サイトにトラッキングタグを追加し、オーディエンスを測定したり、検索エンジンのマーケティング戦略をパーソナライズ、リターゲティング、実施したりできます。

[!DNL Google Tag Manager] は、データとイベントを [!DNL Google Analytics]、Enhanced Ecommerce、その他のサードパーティの分析ソリューションに直接転送して、サイト、製品、プロモーションのパフォーマンスを明確に把握します。

このプロセスを続行するには、[!DNL Google Analytics] と [!DNL Tag Manager] アカウントが必要です。 以下の手順に従って、Google アカウントの設定、Commerce ストアの設定およびタグの作成を行います。

>[!NOTE]
>
>[EU 一般データ保護規則 ](../getting-started/compliance-gdpr.md) や [ カリフォルニア州消費者プライバシー法 ](../getting-started/compliance-ccpa.md) などのプライバシー規制の対象となるビジネスの場合は、[Googleのプライバシー設定 ](google-tools.md#google-privacy-settings) を参照してください。

## 手順 1. [!DNL Google Analytics] アカウントの設定

開始するために必要な基本については、Google ヘルプの [ サイト検索の設定 ](https://support.google.com/analytics/answer/1012264) を参照してください。 [Google Analytics](https://support.google.com/analytics/answer/9304153) および [Google Tag Manager&rbrace; のGoogle ガイドも参照してくだ ](https://support.google.com/tagmanager/answer/6102821) い。

1. [!DNL Google Analytics] アカウントにログインします。

1. **[!UICONTROL Internal Site Search Tracking]** を有効にするには、次の手順を実行します。

   - **[!UICONTROL Select View]**/**[!UICONTROL View Settings]** に移動します。

   - **[!UICONTROL Site Search Tracking]** を `On` に設定します。

   - パラメ **[!UICONTROL Query]** ターを `q` に設定します。

   - 完了したら、設定を **[!UICONTROL Save]** 定します。

1. 表示機能を有効にするには、次の手順を実行します。

   - 「**[!UICONTROL Property Settings]**」を選択します。

   - _[!UICONTROL Advertising Features]_&#x200B;で、**[!UICONTROL Enable Demographics and Interest Reports]**&#x200B;を `On` に設定します。

   - 設定を **[!UICONTROL Save]** 定します。

1. E コマーストラッキングを有効にするには、以下を行います。

   - **[!UICONTROL Select View]**/**[!UICONTROL Ecommerce Settings]** に移動します。

   - **[!UICONTROL Enable Ecommerce]** を `On` に設定します。

   - **[!UICONTROL Enable Enhanced Ecommerce Reporting]** を `On` に設定します。

   - 設定を **[!UICONTROL Save]** 定します。

1. ページを再読み込みし、すべての設定が `On` しいことを確認します。

   >[!NOTE]
   >
   >すべての設定が `On` 定されていない場合は、前の手順を繰り返し、ページを保存してリロードします。 すべての設定が `On` に設定されるまで、この手順を繰り返します。

## 手順 2. [!DNL Google Tag Manager] アカウントの設定

次の手順は、基本設定を使用して新しいコンテナを設定する方法を示しています。 サンプルの [Composer](https://developer.adobe.com/commerce/php/development/composer/) 設定（.json）ファイルを使用してプロセスを簡略化し、読み込んで新しいコンテナにタグを生成します。 この例では、既存のコンテナを変更するのではなく、コンテナを作成することをお勧めします。

>[!NOTE]
>
>詳しくは、Googleの [ コンテナのエクスポートとインポート ](https://support.google.com/tagmanager/answer/6106997) を参照してください。 これらの手順では、サンプル JSON を新しいコンテナに読み込む手順を説明します。

1. リンクされたファイル [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt) をダウンロードし、エディターでファイルを開いて、`GTM_M2_Config.json` として保存します。

   JSON ファイルは [!DNL Google Tag Manager] に直接アップロードされます。

1. **[!UICONTROL Admin]**/**[!UICONTROL Container]**/**[!UICONTROL Import Container]** に移動します。

1. 「**[!UICONTROL Choose container file]**」をクリックし、json ファイルを選択します。

1. [**[!UICONTROL Choose workspace]**] で、[**[!UICONTROL New]**] をクリックします。

1. タイトルと説明を入力し、「**[!UICONTROL Save]**」をクリックします。

1. ファイルをインポートするには、次のいずれかのアクションを選択します。

   - 新しいコンテナには、「**[!UICONTROL Overwrite]**」オプションを選択する必要があります。

   - 既存のコンテナを使用している場合は、「**[!UICONTROL Merge]**」オプションを選択する必要があります。

1. 「**[!UICONTROL Preview]**」をクリックして、タグ、トリガー、変数を確認します。

1. 変数で参照される **[!UICONTROL Google Analytics ID]** を編集するには、次の手順を実行します。

   - **[!UICONTROL Variables]**/**[!UICONTROL User-Defined Variables]** に移動します。

   - **[!UICONTROL Google Analytics]** を選択し、独自の **[!UICONTROL GA ID]** でプレースホルダー（`UA-xxxxxx-x`）を更新します。

1. タグ、トリガーおよび変数を新しいコンテナに追加するには、Googleの手順に従います。

   別のコンテナ内に使用する設定がある場合は、それらを新しいコンテナに移動できます。

1. 完了したら「**[!UICONTROL Confirm]**」をクリックします。

1. 新しいコンテナを公開するには、Googleの手順に従います。

## 手順 3. ストアの設定

{{gtag-api-note}}

1. Commerce ストアの管理者にログインします。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Google API]**」を選択します。

1. **[!UICONTROL Google Analytics]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を設定します。

   ![ セールス構成：Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enable]** を `Yes` に設定します。

   - **[!UICONTROL Account type]** を `Google Tag Manager` に設定します。

   - 「**[!UICONTROL Container ID]**」フィールドに GTM ID （`GTM-xxxxxx`）を入力します。

   - Google Analyticsを使用してコンテンツ実験も行う場合は、「**コンテンツ実験を有効にする**」を「`Yes`」に設定します。

   - 残りのフィールドにはデフォルト値を使用します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. [!DNL Google Tag Manager] 設定をテストし、すべてが正しく動作することを確認します。

>[!NOTE]
>
>各コンテナは 1 つの web サイトに関連付けられ、アカウントごとに必要なコンテナは 1 つだけです。 マルチサイト Commerce インスタンスがある場合は、個別のコンテナが必要です。

## フィールドの説明

| フィールド | 対象範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | ストア表示 | Google Analytics Enhanced Ecommerce を使用して、ストア内のアクティビティを分析できるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Account type] | ストア表示 | ストアのアクティビティとトラフィックを監視するために使用されるGoogle トラッキングコードを決定します。 オプション：`Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | ストア表示 | Google Analyticsの結果に表示される IP アドレスから識別情報を削除するかどうかを指定します。 |
| [!UICONTROL Enable Content Experiments] | ストア表示 | Google コンテンツ実験をアクティブ化します。同じページの異なる 10 バージョンまでテストするために使用できます。 オプション：`Yes` / `No` |
| [!UICONTROL Container Id] | ストア表示 | [!DNL Google Tag Manager] が既にストアにインストールされて設定されている場合は、このフィールドにコンテナ ID が自動的に表示されます。 |
| [!UICONTROL List property for the catalog page] | ストア表示 | カタログページに関連付けられているタグマネージャープロパティを識別します。 デフォルト値：`Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | ストア表示 | クロスセルブロックに関連付けられたタグマネージャープロパティを識別します。 デフォルト値：`Cross-sell` |
| [!UICONTROL List property for the up-sell block] | ストア表示 | アップセル ブロックに関連付けられたタグ マネージャ プロパティを識別します。 デフォルト値：`Up-sell` |
| [!UICONTROL List property for the related products block] | ストア表示 | 関連する製品ブロックに関連付けられているタグマネージャープロパティを識別します。 デフォルト値：`Related Products` |
| [!UICONTROL List property for the search results page] | ストア表示 | 検索結果ページに関連付けられたタグマネージャープロパティを識別します。 デフォルト値：`Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | ストア表示 | 内部プロモーションのラベルに関連付けられたタグマネージャープロパティを識別します。 デフォルト値：`Label` |

{style="table-layout:auto"}

## コンバージョンを追跡するためのタグの作成

Google AdWords アカウントをお持ちの場合は、コンバージョンを追跡するタグを作成できます。 次の例では、[!DNL Google Tag Manager] と [!DNL Google Analytics] の両方を使用して、ストアのコンバージョン _成功_ ページで実行されるタグを作成する方法を示しています。

### 手順 1. タグの作成

1. [!DNL Google Tag Manager] アカウントにログインし、ストア用に作成したコンテナのリンクをクリックします。

1. [**[!UICONTROL New Tag]**] ボックスの [**[!UICONTROL Add a new tag]**] をクリックします。

1. AdWords アカウントから次の情報を取得します。

   - コンバージョン ID
   - コンバージョンラベル

   サポートが必要な場合は、Google[ サポートサイト ](https://support.google.com/tagmanager/answer/6105160) を参照してください。

1. [!DNL Google Tag Manager] ダッシュボードで「**[!UICONTROL Google AdWords]**」をクリックし、次の手順を実行します。

   - タイトルプレースホルダーをクリックして、新しいタグの名前を入力します。

   - 「**[!UICONTROL Choose Product]**」で、「**[!UICONTROL Google AdWords]**」を選択します。

   - 「_[!UICONTROL Choose a Tag Type]_」で「**[!UICONTROL AdWords Conversion Tracking]**」を選択し、「**[!UICONTROL Continue]**」をクリックします。

1. AdWords アカウントの **[!UICONTROL Conversion ID]** と **[!UICONTROL Conversion Label]** を入力し、「**[!UICONTROL Continue]**」をクリックします。

### 手順 2. ルールの作成

[!DNL Google Tag Manager] ダッシュボードから続いて、次の手順では、コンバージョンページでタグを実行するルールを作成します。

1. [**[!UICONTROL Fire On]**] で、[**[!UICONTROL Some Pages]**] をクリックします。

1. _[!UICONTROL Choose Pages]_&#x200B;セクションで、次の設定を行います。

   - **[!UICONTROL Name]** - ページの説明の名前を入力します。

   - **[!UICONTROL Variable]** `url`

   - **操作** - `matches RegEx`

     詳しくは、Google Tag Manager ヘルプの [ 正規表現と CSS セレクターの演算子 ](https://support.google.com/tagmanager/answer/7679109) を参照してください。

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 「緑」チェックボックスをオンにして、「**[!UICONTROL Save]**」をクリックします。

   設定したトリガーは、[ 火の種 ] セクションに青いボタンとして表示されます。

1. 完了したら、「**[!UICONTROL Save Tag]**」をクリックします。

### 手順 3. プレビューと公開

プロセスの次の手順では、タグをプレビューします。 タグをプレビューするたびに、バージョンのスナップショットが保存されます。 結果に満足したら、使用するバージョンに移動し、[**[!UICONTROL Publish]**] をクリックします。

## JavaScriptを使用したカスタム HTML タグ

この節では、コンテンツセキュリティポリシー（CSP）の要件に準拠するために、チェックアウトページで実行するためにカスタム HTML タグJavaScriptに CSP Nonce を追加する方法について説明します。 この追加により、許可されていないスクリプトの実行が防がれ、サイトのセキュリティが強化されます。 詳しくは、[ コンテンツセキュリティポリシー ](https://developer.adobe.com/commerce/php/development/security/content-security-policies) ドキュメントを参照してください。

>[!NOTE]
>
>`cspNonce` グローバル変数のGoogle Tag Manager への読み込みは、Adobe Commerce バージョン 2.4.8 以降でのみサポートされています。

>[!WARNING]
>
>なじみのないスクリプトをストアに追加すると、データが危険に晒される可能性があります。 チェックアウトページで許可されたスクリプトが、支払いの詳細など、機密性の高い顧客情報を盗む可能性があります。 Google Tag Manager アカウントを保護するための予防策を講じることが不可欠です。 信頼できるスクリプトのみを追加し、タグを定期的に確認および監査し、二要素認証（2FA）やアクセス制御などの強力なセキュリティ対策を実装してください。

### 手順 1. CSP Nonce 変数の作成

変数設定を読み込むか手動で設定することで、Google Tag Manager 内で使用できる CSP Nonce 変数を作成できます。

#### 変数設定の読み込み

CSP Nonce 変数は、サンプルコンテナ [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt) に含まれています。 このコードをワークスペースに読み込むことで、変数を作成できます。

#### 変数を手動で作成

変数設定を読み込めない場合は、次の手順を実行して作成します。

1. ワークスペースで、サイドバーの **変数** セクションに移動します。
1. ページの下部にある「**ユーザー定義変数**」セクションの **新規** ボタンをクリックします。
1. 変数に `gtmNonce` という名前を付けます。
1. 変数を編集するには、鉛筆アイコンをクリックします。
1. 「**ページ変数**」セクションから **0&rbrace;JavaScript変数」を選択します。**
1. 「**グローバル変数名**」フィールドに「`window.cspNonce`」と入力します。
1. 変数を保存します。

[Google Tag Manager 変数について詳しくは ](https://support.google.com/tagmanager/answer/7683056?hl=en)Google ドキュメントの [Web 用のユーザー定義変数タイプ ](https://support.google.com/tagmanager/answer/7683362?hl=en) を参照してください。 このドキュメントでは、特定のマーケティングおよび分析のニーズに合わせてタグ管理をカスタマイズするカスタム変数の作成と管理に関する詳細なガイダンスを提供します。

### 手順 2. カスタム HTML タグの作成

1. ワークスペースで、サイドバーの **タグ** セクションに移動します。
1. 「**新規** ボタンをクリックします。
1. 「**タグ設定**」セクションで、「**カスタム HTML タグ**」を選択します。
1. テキスト領域に必要なJavaScriptを入力し、前の手順で作成した変数を指す nonce 属性を開始 `<script>` タグに追加します。 例：

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. **Support document.write** を選択します。
1. 「**トリガー**」セクションで、目的のトリガーを選択します。 例えば、**同意の初期化 – すべてのページ** などです。

Google Tag Manager の [ タグ ](https://support.google.com/tagmanager/answer/3281060) について詳しくは、Google ドキュメントの [ カスタムタグ ](https://support.google.com/tagmanager/answer/6107167) を参照してください。
