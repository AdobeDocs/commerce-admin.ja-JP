---
title: 検索語句を管理
description: ストアの検索語句を管理し、スペルミスや代替の語句を使用して顧客をリダイレクトする方法を説明します。
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 3851258543ba829a4bdbfdb5d3d053ec4627184a
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# 検索語句を管理

The [ランディングページ](../content-design/pages.md) 検索語句には、コンテンツページ、カテゴリページ、製品の詳細ページ、別のサイト上のページなどがあります。

一般的な誤ったつづりを取り込み、適切なページにリダイレクトするには、検索語句を使用します。 例えば、鍛えた鉄パティオ家具を販売する場合、多くの人がこの用語を誤って「 _棒鉄_&#x200B;または _腐った鉄_. スペルミスのある単語を検索語句として入力し、同義語として _鍛錬鉄_. スペルが間違っていても、検索対象は Irouth Iron のページです。

また、顧客が求めているものを学ぶには、店舗で商品を見つけるために使用する検索語句を調べます。 十分な担当者がカタログにない商品を検索する場合は、販売機会を示している可能性があります。 一方、空のままにするのではなく、カタログ内の別の製品にリダイレクトできます。

## 検索語句の追加

ユーザーがストア内で検索に使用する新しい単語を学ぶ際に、その単語を検索語句のリストに追加して、カタログ内で最も一致する商品に人を誘導できます。

![検索語グリッド](./assets/search-terms.png){width="700" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Search Query] | 検索の実行に使用するクエリ。 |
| [!UICONTROL Store] | 検索クエリが適用されたストア。 |
| [!UICONTROL Results] | クエリで見つかった結果の数。 |
| [!UICONTROL Uses] | 使用数。 |
| [!UICONTROL Redirect URL] | 検索の実行後にユーザーがリダイレクトされたターゲットページの URL。 |
| [!UICONTROL Suggested Terms] | クエリ結果に推奨される用語が表示されるかどうかを決定します。 |
| [!UICONTROL Actions] | 製品を編集モードで開きます。 |

{style="table-layout:auto"}

>[!NOTE]
>
>結果の数は、買い物客がこの検索クエリを使用して検索を実行するたびに更新されます。 いずれかの製品が変更または削除された場合、更新はおこなわれません。

### 検索語句を追加

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. クリック **[!UICONTROL Add New Search Term]**.

   ![検索語句の一般情報](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. の下 _[!UICONTROL General Information]_（内）**[!UICONTROL Search Query]**ボックスに、新しい検索語句として追加する単語または語句を入力します。

1. ストアが複数の言語で利用できる場合は、該当する **[!UICONTROL Store]** 表示。

1. 検索結果をストア内の別のページまたは別の Web サイトにリダイレクトするには、 **[!UICONTROL Redirect URL]** フィールドに入力します。

1. 検索で結果が返されない場合に、この用語を提案として使用できるようにするには、 **[!UICONTROL Display in Suggested Terms]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Search]**.

## 検索語を編集

1. Adobe Analytics の _[!UICONTROL Search Terms]_グリッドで、任意のレコードの行をクリックして、検索語句を編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、「 **[!UICONTROL Save Search]**.

## 検索語句の削除

検索語句を削除する方法は、グリッドからと編集ページでの 2 つです。

**メソッド 1:** Adobe Analytics の _[!UICONTROL Search Terms]_グリッド

1. リストで、削除する用語のチェックボックスを選択します。

1. リストの左上隅で、 **[!UICONTROL Actions]** から `Delete`.

1. 完了したら、「 **[!UICONTROL Submit]**.

**方法 2:** 次の日： _[!UICONTROL Edit a Search Term]_ページ

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. 削除する検索語句を見つけて、編集モードで開きます。

1. クリック **[!UICONTROL Delete Search]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## 人気の高い検索用語

The _検索語句_ ストアのフッターのリンクには、ストアの訪問者が使用する検索用語が、人気度別にランク付けして表示されます。 検索語句は _タグクラウド_ 形式を使用します。テキストのサイズは、その用語の人気度を示します。

デフォルトでは、「人気のある検索用語」は検索エンジン最適化ツールとして有効になっていますが、カタログ検索プロセスに直接接続されていません。 検索キーワードページは検索エンジンによってインデックス付けされるので、ページ上のすべてのキーワードを使用すると、検索エンジンのランク付けとストアの表示性を向上できます。 人気のある検索用語ページの URL は次のとおりです。 `mystore.com/search/term/popular/`

![ストアフロントの例 — 人気の高い検索用語](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_一般的な検索用語を設定するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** 」セクションに入力します。

   ![カタログ設定 — 検索エンジンの最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、 [検索エンジンの最適化](../configuration-reference/catalog/catalog.md#search-engine-optimization) （内） _設定リファレンス_.

1. 設定 **[!UICONTROL Popular Search Terms]** 必要に応じて。

   必要に応じて、 **[!UICONTROL Use system value]** この設定を変更するには、チェックボックスを使用します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

>[!NOTE]
>
>ポピュラーのキャッシュをさらに設定できます [カタログ検索](search-configuration.md).

## シノニムを検索

効果を改善する 1 つの方法 [カタログ検索](search-configuration.md) は、人々が同じ項目を説明する際に使用する様々な用語を含めることを目的としています。 誰かが _ソファ_&#x200B;を検索し、製品が _長椅子_. 検索語句をより幅広くキャプチャするには、 _ソファ_, _ダベンポート_、および _恋人_ ～の同義語として _長椅子_&#x200B;をクリックし、同じランディングページに誘導します。

Adobe Commerceは、2 つの異なるシノニム管理ソリューションをサポートしています。

- ライブ検索 [シノニム](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) 機能は、ライブ検索がインストールされたAdobe Commerceインストールで使用できます。
- 標準の検索シノニム機能（このページで説明）は、すべてのAdobe Commerceインストールで標準で使用できます。

>[!NOTE]
>
>標準の検索シノニム機能（標準でサポート） `name` および `sku` 製品属性 **_のみ_**.

>[!IMPORTANT]
>
>検索のシノニム機能では、全文一致検索方法のみを使用します。

![ストアフロントの例 — 同義語を含む検索結果](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### シノニムグループの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   The _[!UICONTROL Search Synonyms]_グリッドが表示されます。 検索のシノニムを初めて使用した場合、グリッドは空になります。

   ![同義語グリッドを検索](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. クリック **[!UICONTROL New Synonym Group]**.

   ![新しい検索シノニムグループ](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. 設定 **[!UICONTROL Scope]** を追加します。

1. グループ内の各シノニムをコンマで区切って入力します。 検索条件として使用する単語を選択します。 例：

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. これらのシノニムを、同じスコープの他のユーザーとグループに結合するには、 **[!UICONTROL Merge existing synonyms]** チェックボックス。

1. 完了したら、「 **[!UICONTROL Save Synonym Group]**.

### シノニムグループの編集

1. Adobe Analytics の _[!UICONTROL Search Synonyms]_グリッドで、任意のレコードの行をクリックして、シノニム・グループを編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、「 **[!UICONTROL Save Synonym Group]**.

### シノニム・グループの削除

シノニム・グループを削除する方法は、グリッドからと編集ページでの 2 つです。

**メソッド 1:** 「シノニムの検索」グリッド内

1. Adobe Analytics の _[!UICONTROL Search Synonyms]_「グリッド」で、削除するグループのチェックボックスをオンにします。

1. リストの左上隅で、 **[!UICONTROL Actions]** から `Delete`.

1. 完了したら、「 **[!UICONTROL Submit]**.

**方法 2:** 「シノニム・グループの編集」ページで、

1. 「シノニムの検索」グリッドで、任意のレコードの行をクリックし、シノニム・グループを編集モードで開きます。

1. クリック **[!UICONTROL Delete Synonym Group]**.

1. プロンプトが表示されたら、グループの削除を確認します。

## 検索語句レポート

検索語句レポートには、各語句の結果数と、語句が使用された回数（ヒット）が表示されます。 レポートデータは、用語、ストア、結果およびヒットでフィルタリングでき、さらに分析するためにエクスポートできます。

### レポートを表示

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. 必要に応じて、コントロールを使用してレポートをフィルタリングします。

   ![検索語句レポート](./assets/search-terms-report.png){width="700" zoomable="yes"}

## レポートのエクスポート

1. の場合 **[!UICONTROL Export to]**、書き出し形式を選択します。

   - `CSV`  — プレーンテキストデータを含む、値をコンマで区切ったファイル
   - `Excel XML` - XML ベースのスプレッドシートデータ形式

1. クリック **[!UICONTROL Export]**.

   生成されたファイルは、指定されたフォルダーに自動的に保存され、ダウンロード用に保存されます。

### レポート列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 検索語句の入力用に生成された一意の数値 ID |
| [!UICONTROL Search Query] | 検索の実行に使用するクエリ |
| [!UICONTROL Store] | 検索クエリが適用されたストア |
| [!UICONTROL Results] | 結果の数 |
| [!UICONTROL Hits] | 使用数 |

{style="table-layout:auto"}
