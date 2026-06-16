---
title: '[!DNL Google Tag Manager]'
description: Adobe Commerce サイトのマーケティングキャンペーンイベントに関連する多数のタグ（コードのスニペット）を [!DNL Google Tag Manager] を使用して管理する方法について説明します。
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/O6QyIkoGkC1FnCa-8fIjVAhqG4aZwDr-AuAIQqyzdPA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
  - id: bcbf87e7-9b75-4596-bffe-0f376b4c73a7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1500
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager]は、マーケティングキャンペーンイベントに関連するさまざまなタグ （コードのスニペット）を効率的に管理およびデプロイするのに役立つ強力なツールです。 [!DNL Google Tag Manager]を使用すると、トラッキングタグをサイトに追加してオーディエンスを測定したり、検索エンジンマーケティング施策をパーソナライズ、リターゲティング、または実施したりできます。

[!DNL Google Tag Manager]は、データとイベントを[!DNL Google Analytics]、拡張E コマース、その他のサードパーティ分析ソリューションに直接転送し、サイト、製品、プロモーションのパフォーマンスを明確に把握できるようにします。

このプロセスを続行するには、[!DNL Google Analytics]と[!DNL Tag Manager] アカウントが必要です。 次の手順では、Google アカウントの設定、Commerce ストアの設定、タグの作成の手順を説明します。

>[!NOTE]
>
>ビジネスが[一般データ保護規則](../getting-started/compliance-gdpr.md)や[Google州消費者プライバシー法](../getting-started/compliance-ccpa.md)などのプライバシー規制の対象となる場合は、[&#x200B; カリフォルニア州プライバシー設定](google-tools.md#google-privacy-settings)を参照してください。

## 手順1: [!DNL Google Analytics] アカウントの設定

開始に必要な基本については、Google ヘルプの「[&#x200B; サイト検索の設定](https://support.google.com/analytics/answer/1012264)」を参照してください。 [Google Analytics](https://support.google.com/analytics/answer/9304153)および[Google Tag Manager](https://support.google.com/tagmanager/answer/6102821)のGoogle ガイドも参照してください。

1. [!DNL Google Analytics] アカウントにログインします。

1. **[!UICONTROL Internal Site Search Tracking]**&#x200B;を有効にするには、次の操作を行います。

   - **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**&#x200B;に移動します。

   - **[!UICONTROL Site Search Tracking]**&#x200B;を`On`に設定します。

   - **[!UICONTROL Query]** パラメーターを`q`に設定します。

   - 完了したら、設定を&#x200B;**[!UICONTROL Save]**&#x200B;します。

1. 表示機能を有効にするには、次の操作を行います。

   - **[!UICONTROL Property Settings]**&#x200B;を選択してください。

   - _[!UICONTROL Advertising Features]_&#x200B;で、**[!UICONTROL Enable Demographics and Interest Reports]**&#x200B;を`On`に設定します。

   - **[!UICONTROL Save]**&#x200B;設定。

1. E コマースのトラッキングを有効にするには、次の操作を行います。

   - **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**&#x200B;に移動します。

   - **[!UICONTROL Enable Ecommerce]**&#x200B;を`On`に設定します。

   - **[!UICONTROL Enable Enhanced Ecommerce Reporting]**&#x200B;を`On`に設定します。

   - **[!UICONTROL Save]**&#x200B;設定。

1. ページを再読み込みし、すべての設定が`On`のままであることを確認します。

   >[!NOTE]
   >
   >すべての設定が`On`ではない場合は、前の手順を繰り返し、ページを保存して再読み込みします。 すべての設定が`On`に設定されるまで、このプロセスを繰り返します。

## 手順2: [!DNL Google Tag Manager] アカウントの設定

次の手順では、基本設定を使用して新しいコンテナを設定する方法を示します。 サンプル [Composer](https://developer.adobe.com/commerce/php/development/composer/)設定（.json）ファイルを使用してプロセスを簡素化し、読み込んで新しいコンテナにタグを生成します。 この例では、既存のコンテナを変更するのではなく、コンテナを作成することをお勧めします。

>[!NOTE]
>
>詳しくは、「[&#x200B; コンテナの書き出しと読み込み](https://support.google.com/tagmanager/answer/6106997)」のGoogleを参照してください。 これらの手順では、サンプル JSONを新しいコンテナにインポートするための手順を説明します。

1. リンクされたファイル [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)をダウンロードし、エディターでファイルを開いて`GTM_M2_Config.json`として保存します。

   json ファイルが[!DNL Google Tag Manager]に直接アップロードされます。

1. **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**&#x200B;に移動します。

1. **[!UICONTROL Choose container file]**&#x200B;をクリックし、json ファイルを選択します。

1. **[!UICONTROL Choose workspace]**&#x200B;で、**[!UICONTROL New]**&#x200B;をクリックします。

1. タイトルと説明を入力し、**[!UICONTROL Save]**&#x200B;をクリックします。

1. ファイルを読み込むには、次のいずれかの操作を選択します。

   - 新しいコンテナに対して&#x200B;**[!UICONTROL Overwrite]** オプションを選択する必要があります。

   - 既存のコンテナを使用している場合は、**[!UICONTROL Merge]** オプションを選択する必要があります。

1. タグ、トリガー、変数を確認するには、**[!UICONTROL Preview]**&#x200B;をクリックします。

1. 変数で参照されている&#x200B;**[!UICONTROL Google Analytics ID]**&#x200B;を編集するには、次の操作を行います。

   - **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**&#x200B;に移動します。

   - **[!UICONTROL Google Analytics]**&#x200B;を選択し、独自の&#x200B;**[!UICONTROL GA ID]**&#x200B;でプレースホルダー（`UA-xxxxxx-x`）を更新します。

1. 新しいコンテナにタグ、トリガーおよび変数を追加する場合は、Googleの手順に従います。

   使用する別のコンテナに設定がある場合は、新しいコンテナに移動できます。

1. 完了したら、**[!UICONTROL Confirm]**&#x200B;をクリックします。

1. 新しいコンテナを公開するには、Googleの手順に従います。

## 手順3: ストアの設定

{{gtag-api-note}}

1. Commerce ストアの管理者にログインします。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Google API]**&#x200B;を選択します。

1. **[!UICONTROL Google Analytics]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の設定を行います。

   ![営業設定 – Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enable]**&#x200B;を`Yes`に設定します。

   - **[!UICONTROL Account type]**&#x200B;を`Google Tag Manager`に設定します。

   - **[!UICONTROL Container ID]** フィールドにGTM ID （`GTM-xxxxxx`）を入力します。

   - Google Analyticsをコンテンツ実験にも使用している場合は、**コンテンツ実験を有効にする**&#x200B;を`Yes`に設定します。

   - 残りのフィールドにはデフォルト値を使用します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. [!DNL Google Tag Manager]設定をテストし、すべてが正しく機能することを確認します。

>[!NOTE]
>
>各コンテナは1つのweb サイトに関連付けられており、アカウントごとに1つのコンテナのみが必要です。 複数サイトのCommerce インスタンスがある場合は、個別のコンテナが必要です。

## フィールドの説明

| フィールド | 範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | ストアビュー | Google Analytics Enhanced E コマースを使用して、ストアでのアクティビティを分析できるかどうかを判断します。 オプション：`Yes` / `No` |
| [!UICONTROL Account type] | ストアビュー | ストアのアクティビティとトラフィックのモニタリングに使用されるGoogle トラッキングコードを指定します。 オプション：`Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | ストアビュー | Google Analyticsの結果に表示されるIP アドレスから識別情報が削除されるかどうかを指定します。 |
| [!UICONTROL Container Id] | ストアビュー | [!DNL Google Tag Manager]が既にインストールされ、ストア用に設定されている場合、コンテナ IDはこのフィールドに自動的に表示されます。 |
| [!UICONTROL List property for the catalog page] | ストアビュー | カタログページに関連付けられているタグマネージャープロパティを識別します。 デフォルト値：`Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | ストアビュー | クロスセル ブロックに関連付けられているTag Manager プロパティを識別します。 デフォルト値：`Cross-sell` |
| [!UICONTROL List property for the up-sell block] | ストアビュー | アップセルブロックに関連付けられているタグマネージャープロパティを識別します。 デフォルト値：`Up-sell` |
| [!UICONTROL List property for the related products block] | ストアビュー | 関連する製品ブロックに関連付けられているタグマネージャープロパティを識別します。 デフォルト値：`Related Products` |
| [!UICONTROL List property for the search results page] | ストアビュー | 検索結果ページに関連付けられているタグマネージャープロパティを識別します。 デフォルト値：`Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | ストアビュー | 内部プロモーションのラベルに関連付けられているタグマネージャープロパティを識別します。 デフォルト値：`Label` |

{style="table-layout:auto"}

## コンバージョンをトラッキングするためのタグの作成

Google AdWords アカウントをお持ちの場合は、コンバージョンをトラッキングするタグを作成できます。 次の例は、[!DNL Google Tag Manager]と[!DNL Google Analytics]の両方を使用して、ストアのコンバージョン _成功_ ページを起動するタグを作成する方法を示しています。

### 手順1: タグを作成

1. [!DNL Google Tag Manager] アカウントにログインし、ストア用に作成したコンテナのリンクをクリックします。

1. **[!UICONTROL New Tag]** ボックスで、**[!UICONTROL Add a new tag]**&#x200B;をクリックします。

1. AdWords アカウントから次の情報を取得します。

   - コンバージョン ID
   - コンバージョンラベル

   サポートが必要な場合は、Googleの[&#x200B; サポートサイト &#x200B;](https://support.google.com/tagmanager/answer/6105160)にアクセスしてください。

1. [!DNL Google Tag Manager] ダッシュボードで、**[!UICONTROL Google AdWords]**&#x200B;をクリックし、次の操作を行います。

   - タイトルプレースホルダーをクリックし、新しいタグの名前を入力します。

   - **[!UICONTROL Choose Product]**&#x200B;で、**[!UICONTROL Google AdWords]**&#x200B;を選択します。

   - _[!UICONTROL Choose a Tag Type]_&#x200B;で「**[!UICONTROL AdWords Conversion Tracking]**」を選択し、「**[!UICONTROL Continue]**」をクリックします。

1. AdWords アカウントから&#x200B;**[!UICONTROL Conversion ID]**&#x200B;と&#x200B;**[!UICONTROL Conversion Label]**&#x200B;を入力し、**[!UICONTROL Continue]**&#x200B;をクリックします。

### 手順2: ルールの作成

[!DNL Google Tag Manager] ダッシュボードから続く次の手順は、コンバージョンページでタグを起動するルールを作成することです。

1. **[!UICONTROL Fire On]**&#x200B;で、**[!UICONTROL Some Pages]**&#x200B;をクリックします。

1. 「_[!UICONTROL Choose Pages]_」セクションで、次の設定を行います。

   - **[!UICONTROL Name]** - ページの説明の名前を入力します。

   - **[!UICONTROL Variable]** `url`

   - **操作** - `matches RegEx`

     詳しくは、Google タグマネージャーヘルプの[正規表現およびCSS セレクター演算子](https://support.google.com/tagmanager/answer/7679109)を参照してください。

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 緑のチェックボックスを選択し、**[!UICONTROL Save]**&#x200B;をクリックします。

   設定したトリガーは、「Fire On」セクションに青いボタンとして表示されます。

1. 完了したら、**[!UICONTROL Save Tag]**&#x200B;をクリックします。

### 手順3: プレビューと公開

このプロセスの次の手順は、タグをプレビューすることです。 タグがプレビューされるたびに、バージョンのスナップショットが保存されます。 結果に問題がなければ、使用するバージョンに移動し、**[!UICONTROL Publish]**&#x200B;をクリックします。

## JavaScriptを使用したカスタム HTML タグ

この節では、チェックアウトページで実行するカスタム HTML タグ JavaScriptにCSP Nonceを追加し、Content Security Policy （CSP）要件への準拠を確保する方法について説明します。 これにより、不正なスクリプトの実行を防止することで、サイトのセキュリティを強化できます。 詳しくは、[&#x200B; コンテンツセキュリティポリシー](https://developer.adobe.com/commerce/php/development/security/content-security-policies)のドキュメントを参照してください。

>[!NOTE]
>
>Google Tag Managerへの`cspNonce` グローバル変数の読み込みは、Adobe Commerce バージョン 2.4.8以降でのみサポートされています。

>[!WARNING]
>
>ストアに不明なスクリプトを追加すると、データ侵害のリスクが生じる可能性があります。 チェックアウトページで許可されたスクリプトは、支払いの詳細などの機密性の高い顧客情報を盗む可能性があります。 Google Tag Manager アカウントを保護するために、予防策を講じることが重要です。 信頼できるスクリプトのみを追加し、タグを定期的に確認および監査し、2要素認証（2FA）やアクセス制御などの強力なセキュリティ対策を実装できます。

### 手順1: CSP Nonce変数の作成

Google Tag Manager内で使用できるCSP Nonce変数を作成するには、変数設定を読み込むか、手動で設定します。

#### 変数設定のインポート

CSP Nonce変数は、サンプルコンテナ [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)に含まれています。 このコードをワークスペースに読み込むことで、変数を作成できます。

#### 変数を手動で作成する

変数設定を読み込めない場合は、次の手順を実行して作成します。

1. ワークスペースで、サイドバーの&#x200B;**変数** セクションに移動します。
1. 「**ユーザー定義変数**」セクションのページ下部にある「**新規**」ボタンをクリックします。
1. 変数に`gtmNonce`という名前を付けます。
1. 鉛筆アイコンをクリックして、変数を編集します。
1. 「**ページ変数**」セクションから「**JavaScript変数**」を選択します。
1. 「**グローバル変数名**」フィールドに「`window.cspNonce`」と入力します。
1. 変数を保存します。

[Google Tag Manager Variables](https://support.google.com/tagmanager/answer/7683056?hl=en)について詳しくは、Google ドキュメントの[Web](https://support.google.com/tagmanager/answer/7683362?hl=en)のユーザー定義の変数タイプを参照してください。 このドキュメントでは、特定のマーケティングや分析のニーズに合わせてタグ管理をカスタマイズするための、カスタム変数の作成と管理に関する詳細なガイダンスを提供します。

### 手順2: カスタム HTML タグの作成

1. ワークスペースで、サイドバーの&#x200B;**タグ** セクションに移動します。
1. 「**新規**」ボタンをクリックします。
1. **Tag Configuration** セクションで、**カスタム HTML タグ**&#x200B;を選択します。
1. テキスト領域に必要なJavaScriptを入力し、前の手順で作成した変数を指す開始`<script>` タグにnonce属性を追加します。 例：

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. 「**サポート document.write**」を選択します。
1. 「**トリガー**」セクションで、目的のトリガーを選択します。 例えば、**同意初期化 – すべてのページ**&#x200B;です。

Google Tag Managerの[&#x200B; タグ &#x200B;](https://support.google.com/tagmanager/answer/3281060)について詳しくは、Google ドキュメントの[&#x200B; カスタムタグ &#x200B;](https://support.google.com/tagmanager/answer/6107167)を参照してください。
