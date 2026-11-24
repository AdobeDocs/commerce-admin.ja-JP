---
title: エンリッチメント設定
description: AI Product DiscoveryでCatalog EnrichmentとPDP enrichmentが共有する配信、月次エージェント型トラフィックジョブ、適格なAI エージェントを設定します。
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# エンリッチメント設定

AI Product Discovery ワークスペースの「**[!UICONTROL Settings]**」タブを使用して、Adobe Commerce インスタンスを設定します。 設定すると、カタログとPDPのエンリッチメントがAI製品発見ワークスペースに表示されます。

このタブのフィールドは、AI Product Discoveryが接続する[!DNL Adobe Commerce]環境とストアビューを識別します。 IMSのログインと組織の要件については、[AI製品検出の前提条件](prerequisites.md)を参照してください。

1. 管理画面で、**[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**&#x200B;または&#x200B;**[!UICONTROL Product Details Page Enrichment]**&#x200B;に移動します。
1. ページの上部にある&#x200B;**[!UICONTROL Scope]** リストで、設定するストアビューを選択するか、**[!UICONTROL All Store Views]**&#x200B;のままにして、ストアビュー全体の設定を管理します。
1. 「**[!UICONTROL Settings]**」タブを開きます。
1. **[!UICONTROL Commerce Configuration]**&#x200B;で、URLがラベル付きのストアビューパネルを展開します。

   AI製品検出サービスと監査ワークフローを有効にするための[!DNL Adobe Commerce]環境の詳細を指定します。

   ![&#x200B; カタログエンリッチメント設定タブのCommerce設定](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. ストアビューに必要な接続の詳細を入力します。

   - **[!UICONTROL Store View URL]**: ストアビューに対応するURL （例：`https://brand.example.com/fr/`）。
   - **[!UICONTROL Environment ID]**：接続がアクセスする[!DNL Adobe Commerce]環境の一意の識別子。
   - **[!UICONTROL Website Code]**、**[!UICONTROL Store Code]**&#x200B;および&#x200B;**[!UICONTROL Store View Code]**: Commerce web サイトのWeb サイト、ストア、およびストアの表示コード。 これらの値は、Commerce管理者のコードと一致する必要があります。
   - **[!UICONTROL Host Name]**: [!DNL Adobe Commerce] インスタンスのホスト名。
   - **（オプション – カタログの強化のみ）** **[!UICONTROL Catalog field limits]**&#x200B;の下の&#x200B;**[!UICONTROL Limit maximum characters for product name]**&#x200B;を選択し、生成された製品名の文字制限を指定します。 **[!UICONTROL Limit maximum characters for product description]**&#x200B;を選択し、生成される製品説明の文字数制限を指定します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

保存した後、最初の同期ジョブまたは検証ジョブが完了するのを待ってから、そのストアビューのカタログまたは監査結果に頼ります。 商品の提案が&#x200B;**[!UICONTROL Catalog Enrichment]** ページに表示されるまでに、最大で24時間かかる場合があります。

ストアビュー設定を削除するには、そのエントリを展開し、**[!UICONTROL Delete]**&#x200B;をクリックします。

## フィールドの説明 {#commerce-connection-fields}

必須フィールドには、**[!UICONTROL Commerce Configuration]** フォームにアスタリスク （*）が付いています。

| フィールド | 必須 | 説明 |
| --- | --- | --- |
| ストアビューURL | はい | ストアビューに対応するURL （例：`https://brand.example.com/fr/`）。 |
| 環境ID | はい | 接続がアクセスする[!DNL Adobe Commerce]環境の一意の識別子。 |
| Web サイトコード | はい | CommerceのWeb サイトのWeb サイトのコード。 |
| ストアコード | はい | Commerce Web サイトのストアコード。 |
| ストアビューコード | はい | Commerce web サイトのストアビュー。 |
| ホスト名 | はい | [!DNL Adobe Commerce] インスタンスのホスト名。 |
| カタログフィールドの制限（カタログエンリッチメントのみ） | いいえ | 生成される製品名と説明に対して文字制限を定義します。 |
