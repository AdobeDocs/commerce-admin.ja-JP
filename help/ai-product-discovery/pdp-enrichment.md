---
title: 製品詳細ページの強化
description: '[!DNL Adobe Commerce]個の製品詳細ページのエンリッチメントを使用して、AIが提案した製品コピーをレビューし、エンリッチメントジョブを作成し、LLMとAIの発見用に承認済みの更新をデプロイします。'
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%
---

# 製品詳細ページの強化

商品詳細ページ（PDP）のエンリッチメント人間の目に見える体験に何も変更を加えることなく、構造化された商品データを使用して、あらゆるPDPのLLMのクロール可能性を最大化します。 この機能は、製品カタログを読み取り、LLMが簡単に読み取り、解析できる各PDPの構造化データペイロードを作成します。

## 仕組み {#how-it-works}

Adobe Commerceのカタログには、属性、バリエーション、カテゴリー、価格、在庫状況などの商品情報が含まれます。 PDP エンリッチメントジョブでは、AI エージェントが利用できるように、製品ページとカタログファクトのグループを選択します。 情報は、ストアフロントの体験を変更することなく、エージェント向けに整理されています。

PDP エンリッチメントを利用することで、次のことが可能になります。

- ライブ製品ページを持つ特定の有効な製品を選択します。
- ジョブを保存または実行する前に、選択したページとファクトの概要を確認します。
- エンリッチメントに含まれる製品情報をプレビューします。

| 方向 | 目的 |
| --- | --- |
| Commerce カタログ -> エンリッチメントジョブ | ライブ商品ページと、含めるカタログファクトを選択します。 |
| エンリッチメントジョブ -> AI エージェント | 選択した既存の製品情報を構造化フォームで使用できるようにします。 人間が目にするストアフロントは変わりません。 |

## PDPの強化へのアクセス

開始する前に、デプロイメント固有の[AI製品検出の前提条件](prerequisites.md)を確認してください。 Commerce プラットフォームの設定が完了したら、管理者で&#x200B;**[!UICONTROL AI Product Discovery]**&#x200B;を開き、**[!UICONTROL Product Details Page Enrichment]**&#x200B;を選択します。

## PDP強化の2つの道筋

PDP エンリッチメントを受け取るには、次の2つのパスがあります。

- **エージェンティックトラフィック** – このタイプのエンリッチメントは、Commerce インスタンスを設定してから24 ～ 48時間後に自動的に開始され、**最適化** タブに結果が表示されます。
- **Enrichment Manager** – これらのエンリッチメントは、販売者が&#x200B;**[!UICONTROL Create enrichment]** ボタンをクリックし、エンリッチするSKUを手動で選択したときに設定されます。 [ エンリッチメントマネージャー](#create-an-enrichment-job)の詳細をご覧ください。

## PDP エンリッチメントアクティビティの確認

PDP エンリッチメントページが開き、**[!UICONTROL Optimizations]** タブが表示されます。 ダッシュボードを使用して、エンリッチメントの範囲、求人活動、注意が必要な求人を確認できます。 「**[!UICONTROL Settings]**」タブを使用して、Commerce インスタンスを[ リンク ](settings.md)し、AI Product Discoveryにリンクします。

### 注意が必要な仕事を見つける

**[!UICONTROL Needs your attention]** セクションでは、アクションが必要なジョブを強調表示します。 カードには、ジョブ名、製品の選択方法、製品ページ数、ジョブのステータス、進行状況が表示されます。 カードで使用可能なアクションを使用して、ジョブを続行します。

### すべてのジョブを検索

テーブルを使用してジョブを検索および追跡します。 ジョブの詳細で検索するか、**[!UICONTROL Generating]**、**[!UICONTROL Ready to review]**、**[!UICONTROL Deployed]**、**[!UICONTROL Queued]**&#x200B;または&#x200B;**[!UICONTROL Failed]**&#x200B;などのステータスでフィルタリングします。 この表には、各ジョブのID、名前、オリジン、製品ページ数、開始日、ステータス、使用可能なアクションが一覧表示されます。

## エンリッチメントジョブの作成

この節では、製品詳細ページのエンリッチメントを作成する方法について説明します。

![PDP エンリッチメントの作成](./assets/create-cat-enrich.png)

1. **[!UICONTROL Optimizations]**&#x200B;で、**[!UICONTROL Create enrichment]**&#x200B;をクリックします。
1. 「Black Friday 2026」など、**エンリッチメント名**&#x200B;を入力します。
1. 「コーヒー」など、**カテゴリ**&#x200B;を選択します。
1. 「アクセサリ」など、**属性セット**&#x200B;を選択します。
1. 「シンプルな製品」など、**製品タイプ**&#x200B;を選択します。
1. **価格帯**&#x200B;を選択します。
1. **[!UICONTROL Apply filters]**&#x200B;をクリックします。

   エンリッチメント条件に一致する製品をプレビューし、**カスタマイズ**&#x200B;をクリックして、エンリッチメントする製品をさらに範囲で表示できます。

1. エンリッチする特定の製品を確認するには、**[!DNL Next]**&#x200B;をクリックします。
1. **[!DNL Run enrichment]**&#x200B;をクリックします。

   エンリッチメントジョブが実行され、**最適化** テーブルに表示されます。 実行が完了したら、最適化を[ レビューして](#review-and-deploy-an-enrichment-job) デプロイできます。

### エンリッチメントジョブの確認 {#review-and-deploy-an-enrichment-job}

エンリッチメントジョブを開きます。

![PDP エンリッチメント URLのリスト ](./assets/pdp-enrich-urls.png)

候補&#x200B;**付き** URL テーブルには、エンリッチメントの機会を持つすべての製品が一覧表示されます。 各製品について、次のことができます。

- **AI分析と提案されたエンリッチメントを表示するには、行**&#x200B;を展開します。
- **ブランドボイスとマーチャンダイジングガイドラインに合わせて、提案された製品名または説明を適用前に**&#x200B;編集します。
- **エンリッチメントする商品の最適化**&#x200B;をデプロイし、Adobe Commerce ストアフロントに直接公開します。
- エンリッチメントがレビューおよび適用されたら、**修正済みとしてマーク**&#x200B;します。
- カタログ戦略に関連しない提案を&#x200B;**無視**&#x200B;します。

提案は、**現在の提案**、**修正提案**、**無視された提案**&#x200B;の3つのビューに整理されます。 エンリッチメントが適用されると、ステータスが&#x200B;**Applied**&#x200B;の&#x200B;**修正候補**&#x200B;に移動します。 適用されたエンリッチメントは、いつでもロールバックできます。

### 最適化のデプロイ

推奨事項を確認し、最適化する製品ページを選択したら、**最適化をデプロイ**&#x200B;をクリックして、Edgeで最適化を使用してエンリッチメントを公開します。 「**Edgeにデプロイ**&#x200B;の確認」ダイアログに、選択した商品URL、最適化タイプ、適用されているエンリッチメントが表示されます。 デプロイメント後、確認画面により、どの製品ページが正常に最適化されたかが確認されます。

最適化は、[Optimize at Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)を通じて、AI ユーザーエージェントにのみ配信されます。 訪問者は、PDPのデザイン、ページのパフォーマンス、ブランド体験に変更を加えることなく、既存のストアフロント体験を以前とまったく同じように確認し続けることができます。

## 制限と考慮事項 {#limits}

- ライブ製品ページを持つ有効な製品のみを選択できます。
- エンリッチメントは、カタログに既に存在する事実を整理します。新しい製品情報は追加されません。
- PDP エンリッチメントワークフローは、ストアフロントを変更しません。
- PDP エンリッチメントジョブとカタログエンリッチメントジョブには、目的とワークフローが異なります。
- PDP最適化では、Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)で[最適化を使用します。

## ベストプラクティス {#best-practices}

- 製品グループや施策を特定するための明確なジョブ名を使用できます。
- ジョブに含まれる事実をプレビューし、AI エージェントにとって正確かつ適切であることを確認します。
- 製品が既にエンリッチされているかどうかを確認してから、製品をスキップするか上書きするかを決定します。
- カタログの同期と製品ファクトの所有権を、それらのレコードを担当するチームと調整します。

## 例：製品のバリエーションと仕様のエンリッチメント

一般的に、商品ページには、AIが処理できる以上のカタログ情報が含まれています。 例えば、小売企業が防水ハイキングブーツを販売しているとします。 サイズ、幅、カラーのオプションは、JavaScriptで読み込まれるバリアントセレクターに配置されます。 資料、防水、ケア手順は「詳細」タブに表示され、フィットのガイダンスはポップアップで表示されます。 買い物客はこれらすべてを開くことができますが、ページを最初に読み込むAIweb クローラーには、商品名、価格、簡単な説明しか表示されない場合があります。

エンリッチメントジョブがこの製品で実行されると、属性とバリエーションを含む製品のすべてのカタログデータを取り込み、AI エージェントが読み取れる構造化された形式でパッケージ化します。 AI アシスタントは、「このブーツはサイズ 11の広いサイズで利用できますか？」などの質問に答えることができます。 または「それは完全に防水ですか？」 データからカスタム情報を取り込むことができます。

エンリッチメントジョブでは、カタログに既に存在する情報のみを使用します。 新しい商品事実を生み出すことも、買い物客が目にする商品ページを変更することもありません。
