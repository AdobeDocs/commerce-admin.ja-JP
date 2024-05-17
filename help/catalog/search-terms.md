---
title: 検索語句の管理
description: スペルミスや代替用語を使用して顧客をリダイレクトするために、ストアの検索用語を管理する方法を説明します。
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 3851258543ba829a4bdbfdb5d3d053ec4627184a
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# 検索語句の管理

この [ランディングページ](../content-design/pages.md) 検索語句としては、コンテンツページ、カテゴリページ、製品詳細ページのほか、別のサイトのページも使用できます。

検索用語を使用すると、一般的なスペルミスを取り込み、適切なページにリダイレクトすることができます。 例えば、鍛造の鉄のパティオ家具を販売する場合、多くの人がその用語を間違って入力していることを知っています _棒状鉄_、または _鉄を腐らせる_. スペルミスした各単語を検索語句として入力し、次の同義語にすることができます。 _鍛錬鉄_. その単語のスペルが間違っているにもかかわらず、検索は鍛造された鉄のページに向けられます。

また、ストア内の製品を検索するために顧客が使用する検索用語を調べることで、顧客が探しているものを把握することもできます。 カタログにない商品を探すユーザーが十分にある場合は、販売機会を示している可能性があります。 その間、手ぶらにするのではなく、カタログの別の製品にリダイレクトできます。

## 検索語句を追加

ストアでユーザーが検索に使用する新しい単語を学習したら、その単語を検索用語リストに追加して、カタログ内で最も一致する製品をユーザーに示すことができます。

![検索語句グリッド](./assets/search-terms.png){width="700" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Search Query] | 検索の実行に使用するクエリ。 |
| [!UICONTROL Store] | 検索クエリが適用されたストア。 |
| [!UICONTROL Results] | クエリで見つかった結果の数。 |
| [!UICONTROL Uses] | 使用回数。 |
| [!UICONTROL Redirect URL] | 検索の実行後にユーザーがリダイレクトされたターゲットページの URL。 |
| [!UICONTROL Suggested Terms] | クエリ結果に推奨用語を表示するかどうかを決定します。 |
| [!UICONTROL Actions] | 製品を編集モードで開きます。 |

{style="table-layout:auto"}

>[!NOTE]
>
>結果の数は、買い物客がこの検索クエリを使用して検索を実行するたびに更新されます。 製品が変更または削除されても、更新されません。

### 検索語句を追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. クリック **[!UICONTROL Add New Search Term]**.

   ![検索用語の一般情報](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. 次の下 _[!UICONTROL General Information]_が含まれる&#x200B;**[!UICONTROL Search Query]**ボックスに、新しい検索語として追加する単語または語句を入力します。

1. ストアが複数の言語で使用可能な場合は、該当するを選択します **[!UICONTROL Store]** 表示。

1. 検索結果をストア内の別のページまたは別の web サイトにリダイレクトするには、ターゲット ページの完全な URL を **[!UICONTROL Redirect URL]** フィールド。

1. 検索で結果が返されなかった場合に、この用語を提案として使用できるようにする場合は、次のように設定します **[!UICONTROL Display in Suggested Terms]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Search]**.

## 検索語句を編集

1. が含まれる _[!UICONTROL Search Terms]_グリッドで、レコードの行をクリックして、検索語句を編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、 **[!UICONTROL Save Search]**.

## 検索語句を削除する

検索語句を削除する方法には、グリッドからの方法と編集ページでの方法の 2 つがあります。

**メソッド 1:** が含まれる _[!UICONTROL Search Terms]_グリッド

1. リストで、削除する用語のチェックボックスを選択します。

1. リストの左上隅にあるを設定します。 **[!UICONTROL Actions]** 対象： `Delete`.

1. 完了したら、 **[!UICONTROL Submit]**.

**メソッド 2:** 日 _[!UICONTROL Edit a Search Term]_ページ

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. 削除する検索語句を見つけ、編集モードで開きます。

1. クリック **[!UICONTROL Delete Search]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## 一般的な検索用語

この _検索語句_ ストアのフッターにあるリンクには、ストアの訪問者が使用した検索用語が人気度でランク付けされて表示されます。 検索用語がに表示される _タグクラウド_ テキストのサイズが用語の人気を示す形式。

デフォルトでは、人気検索用語は検索エンジン最適化ツールとして有効になっていますが、カタログ検索プロセスに直接接続されていません。 検索用語ページは検索エンジンによってインデックス化されるので、ページ上の用語はすべて検索エンジンのランキングとストアの表示を向上させるのに役立ちます。 一般的な検索用語ページの URL: `mystore.com/search/term/popular/`

![ストアフロントの例 – よく使用される検索用語](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_一般的な検索用語を設定するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization]** セクション。

   ![カタログ設定 – 検索エンジンの最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、を参照してください [検索エンジンの最適化](../configuration-reference/catalog/catalog.md#search-engine-optimization) が含まれる _設定リファレンス_.

1. を設定 **[!UICONTROL Popular Search Terms]** 必要に応じて。

   必要に応じて、 **[!UICONTROL Use system value]** この設定を変更するには、チェックボックスをオンにします。

1. 完了したら、 **[!UICONTROL Save Config]**.

>[!NOTE]
>
>さらに、人気のキャッシュを設定できます [カタログ検索](search-configuration.md).

## シノニムの検索

～の有効性を改善する方法の一つ [カタログ検索](search-configuration.md) は、ユーザーが同じ項目を説明するために使用できる別の用語を含めることです。 あなたは誰かが探しているからといってセールを失いたくありません _ソファ_&#x200B;を選択すると、製品がとして表示されます。 _ソファ_. を入力することで、より幅広い検索用語を取り込むことができます _ソファ_, _ダベンポート_、および _ラブサート_ の同義語として _ソファ_&#x200B;を選択し、同じランディングページに移動します。

Adobe Commerceでは、次の 2 つの異なるシノニム管理ソリューションをサポートしています。

- Live Search [同義語](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) 機能は、Live Search がインストールされたAdobe Commerceのインストールで使用できます。
- 標準のシノニム検索機能（このページで説明）は、すべてのAdobe Commerce インストールでそのまま使用できます。

>[!NOTE]
>
>標準の検索シノニム機能は、すぐに使用できる機能です `name` および `sku` 製品属性 **_のみ_**.

>[!IMPORTANT]
>
>同義語検索機能では、全文一致の検索方法のみが使用されます。

![ストアフロントの例 – 同義語を使用した検索結果](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### シノニム・グループの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   この _[!UICONTROL Search Synonyms]_グリッド表示 同義語の検索を初めて使用した場合、グリッドは空になります。

   ![シノニム グリッドの検索](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. クリック **[!UICONTROL New Synonym Group]**.

   ![新しい検索同義語グループ](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. を設定 **[!UICONTROL Scope]** をシノニムが適用されるストア・ビューに移動します。

1. グループ内の各シノニムをコンマで区切って入力します。 検索条件として使用する可能性のある単語を選択します。 例：

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. これらのシノニムを同じスコープを持つ他のシノニムとグループにマージするには、 **[!UICONTROL Merge existing synonyms]** チェックボックス。

1. 完了したら、 **[!UICONTROL Save Synonym Group]**.

### シノニム・グループの編集

1. が含まれる _[!UICONTROL Search Synonyms]_グリッドで、レコードの行をクリックして、シノニム・グループを編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、 **[!UICONTROL Save Synonym Group]**.

### シノニム・グループの削除

シノニム・グループを削除するには、グリッドから削除する方法と編集ページで削除する方法の 2 つがあります。

**メソッド 1:** シノニムの検索グリッドで、次の操作を行います

1. が含まれる _[!UICONTROL Search Synonyms]_グリッドで、削除するグループのチェックボックスを選択します。

1. リストの左上隅にあるを設定します。 **[!UICONTROL Actions]** 対象： `Delete`.

1. 完了したら、 **[!UICONTROL Submit]**.

**メソッド 2:** シノニム・グループの編集ページ

1. シノニムの検索グリッドで、レコードの行をクリックして、シノニム・グループを編集モードで開きます。

1. クリック **[!UICONTROL Delete Synonym Group]**.

1. プロンプトが表示されたら、グループの削除を確認します。

## 検索語句レポート

検索用語レポートには、各用語の結果数と、その用語が使用された回数（ヒット数）が表示されます。 レポートデータは、用語、ストア、結果およびヒットでフィルタリングしたり、さらなる分析のために書き出したりできます。

### レポートを表示

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. 必要に応じてコントロールを使用してレポートをフィルタリングします。

   ![検索語句レポート](./assets/search-terms-report.png){width="700" zoomable="yes"}

## レポートのエクスポート

1. の場合 **[!UICONTROL Export to]**&#x200B;で、書き出し形式を選択します。

   - `CSV` - プレーンテキストデータを含む、コンマ区切りの値ファイル
   - `Excel XML` - XML ベースのスプレッドシートデータ形式

1. クリック **[!UICONTROL Export]**.

   生成されたファイルは、指定したフォルダーに自動的に保存されてダウンロードされます。

### レポート列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 検索語句エントリ用に生成された一意の数値 ID |
| [!UICONTROL Search Query] | 検索の実行に使用するクエリ |
| [!UICONTROL Store] | 検索クエリが適用されたストア |
| [!UICONTROL Results] | 結果数 |
| [!UICONTROL Hits] | 使用数 |

{style="table-layout:auto"}
