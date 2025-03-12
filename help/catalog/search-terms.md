---
title: 検索語句の管理
description: スペルミスや代替用語を使用して顧客をリダイレクトするために、ストアの検索用語を管理する方法を説明します。
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# 検索語句の管理

検索語句の [ ランディングページ ](../content-design/pages.md) は、コンテンツページ、カテゴリページ、製品詳細ページのほか、別のサイトのページにすることもできます。

検索用語を使用すると、一般的なスペルミスを取り込み、適切なページにリダイレクトすることができます。 例えば、鍛造の鉄のパティオ家具を販売する場合、多くの人が用語を _ロッド鉄_、さらには _腐った鉄_ と誤字することがわかります。 スペルミスした各単語を検索語句として入力し、「鍛造鉄 _の同義語にするこ_ ができます。 その単語のスペルが間違っているにもかかわらず、検索は鍛造された鉄のページに向けられます。

また、ストア内の製品を検索するために顧客が使用する検索用語を調べることで、顧客が探しているものを把握することもできます。 カタログにない商品を探すユーザーが十分にある場合は、販売機会を示している可能性があります。 その間、手ぶらにするのではなく、カタログの別の製品にリダイレクトできます。

## 検索語句を追加

ストアでユーザーが検索に使用する新しい単語を学習したら、その単語を検索用語リストに追加して、カタログ内で最も一致する製品をユーザーに示すことができます。

![ 検索用語グリッド ](./assets/search-terms.png){width="700" zoomable="yes"}

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

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL SEO & Search]_/**[!UICONTROL Search Terms]**に移動します。

1. 「**[!UICONTROL Add New Search Term]**」をクリックします。

   ![ 検索語句の一般情報 ](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. [_[!UICONTROL General Information]_] の [**[!UICONTROL Search Query]**] ボックスに、新しい検索語として追加する単語または語句を入力します。

1. ストアが複数の言語で使用可能な場合は、該当する **[!UICONTROL Store]** ビューを選択します。

1. 検索結果をストア内の別のページまたは別の web サイトにリダイレクトするには、「リダイレク **[!UICONTROL Redirect URL]**」フィールドにターゲットページの完全な URL を入力します。

1. 検索で結果が返されない場合にこの用語を提案として使用する場合は、**[!UICONTROL Display in Suggested Terms]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Search]**」をクリックします。

## 検索語句を編集

1. _[!UICONTROL Search Terms]_グリッドで、レコードの行をクリックして、検索語句を編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、「**[!UICONTROL Save Search]**」をクリックします。

## 検索語句を削除する

検索語句を削除する方法には、グリッドからの方法と編集ページでの方法の 2 つがあります。

**方法 1:** _[!UICONTROL Search Terms]_グリッド内

1. リストで、削除する用語のチェックボックスを選択します。

1. リストの左上隅にある **[!UICONTROL Actions]** を `Delete` に設定します。

1. 完了したら、「**[!UICONTROL Submit]**」をクリックします。

**方法 2:**_[!UICONTROL Edit a Search Term]_ページで

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL SEO & Search]_/**[!UICONTROL Search Terms]**に移動します。

1. 削除する検索語句を見つけ、編集モードで開きます。

1. 「**[!UICONTROL Delete Search]**」をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。

## 一般的な検索用語

ストアのフッターにある _検索語句_ リンクには、ストアの訪問者が使用した検索語句が人気度の高い順に表示されます。 検索用語は _タグクラウド_ 形式で表示されます。テキストのサイズは、この用語の普及度を示します。

デフォルトでは、人気検索用語は検索エンジン最適化ツールとして有効になっていますが、カタログ検索プロセスに直接接続されていません。 検索用語ページは検索エンジンによってインデックス化されるので、ページ上の用語はすべて検索エンジンのランキングとストアの表示を向上させるのに役立ちます。 一般的な検索用語ページの URL は `mystore.com/search/term/popular/` です。

![ ストアフロントの例 – よく使用される検索用語 ](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_一般的な検索用語を設定するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Search Engine Optimization]**」セクションを展開します。

   ![ カタログ設定 – 検索エンジンの最適化 ](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、[ 設定リファレンス ](../configuration-reference/catalog/catalog.md#search-engine-optimization) の _検索エンジンの最適化_ を参照してください。

1. 必要に応じて **[!UICONTROL Popular Search Terms]** を設定します。

   必要に応じて、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、この設定を変更します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

>[!NOTE]
>
>一般的な [ カタログ検索 ](search-configuration.md) のキャッシュをさらに設定できます。

## シノニムの検索

[ カタログ検索 ](search-configuration.md) の効果を高める 1 つの方法は、同じ項目を説明するために使用できる別の用語を含めることです。 誰かが _ソファ_ を探していて、あなたの製品が _ソファ_ としてリストされているという理由だけで販売を失いたくない。 _ソファ_、_ダベンポート_ および _ロベサート_ を _ソファ_ の同義語として入力することで、より幅広い検索用語を取り込み、それらを同じランディングページに誘導できます。

Adobe Commerceでは、次の 2 つの異なるシノニム管理ソリューションをサポートしています。

- Live Search[ 同義語 ](https://experienceleague.adobe.com/docs/commerce/live-search/live-search-admin/synonyms/synonyms.html) 機能は、Live Search がインストールされているAdobe Commerceのインストールで使用できます。
- 標準のシノニム検索機能（このページで説明）は、すべてのAdobe Commerce インストールでそのまま使用できます。

>[!NOTE]
>
>標準の検索シノニム機能は、すぐに使用できる機能で、`name` および `sku` の製品属性 **_のみ_** をサポートしています。

>[!IMPORTANT]
>
>同義語検索機能では、全文一致の検索方法のみが使用されます。

![ ストアフロントの例 – 同義語を使用した検索結果 ](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### シノニム・グループの作成

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL SEO & Search]_/**[!UICONTROL Search Synonyms]**に移動します。

   _[!UICONTROL Search Synonyms]_グリッドが表示されます。 同義語の検索を初めて使用した場合、グリッドは空になります。

   ![ シノニム グリッドの検索 ](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. 「**[!UICONTROL New Synonym Group]**」をクリックします。

   ![ 新しい検索同義語グループ ](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. シノニムが適用されるストア表示に **[!UICONTROL Scope]** を設定します。

1. グループ内の各シノニムをコンマで区切って入力します。 検索条件として使用する可能性のある単語を選択します。 例：

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. これらの同義語を同じ範囲を持つ他の同義語グループにマージするには、「**[!UICONTROL Merge existing synonyms]**」チェックボックスを選択します。

1. 完了したら、「**[!UICONTROL Save Synonym Group]**」をクリックします。

### シノニム・グループの編集

1. _[!UICONTROL Search Synonyms]_グリッドで、レコードの行をクリックして、シノニム グループを編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、「**[!UICONTROL Save Synonym Group]**」をクリックします。

### シノニム・グループの削除

シノニム・グループを削除するには、グリッドから削除する方法と編集ページで削除する方法の 2 つがあります。

**方法 1:** 類義語検索グリッド

1. _[!UICONTROL Search Synonyms]_グリッドで、削除するグループのチェックボックスを選択します。

1. リストの左上隅にある **[!UICONTROL Actions]** を `Delete` に設定します。

1. 完了したら、「**[!UICONTROL Submit]**」をクリックします。

**方法 2:** シノニム・グループの編集ページ

1. シノニムの検索グリッドで、レコードの行をクリックして、シノニム・グループを編集モードで開きます。

1. 「**[!UICONTROL Delete Synonym Group]**」をクリックします。

1. プロンプトが表示されたら、グループの削除を確認します。

## 検索語句レポート

検索用語レポートには、各用語の結果数と、その用語が使用された回数（ヒット数）が表示されます。 レポートデータは、用語、ストア、結果およびヒットでフィルタリングしたり、さらなる分析のために書き出したりできます。

### レポートを表示

1. _管理者_ サイドバーで、**[!UICONTROL Reports]**/_[!UICONTROL Marketing]_/**[!UICONTROL Search Terms]**に移動します。

1. 必要に応じてコントロールを使用してレポートをフィルタリングします。

   ![ 検索語句レポート ](./assets/search-terms-report.png){width="700" zoomable="yes"}

## レポートのエクスポート

1. **[!UICONTROL Export to]** の場合は、書き出し形式を選択します。

   - `CSV` - プレーンテキストデータを含む、コンマ区切りの値ファイル
   - `Excel XML` - XML ベースのスプレッドシートデータ形式

1. 「**[!UICONTROL Export]**」をクリックします。

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
