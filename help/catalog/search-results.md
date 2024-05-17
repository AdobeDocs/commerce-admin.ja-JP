---
title: 検索結果
description: 製品が「クイック検索」ボックスまたは「詳細検索」フォームに入力された検索条件に一致する方法を設定する方法を説明します。
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 4b2e1dd87a39c9be1adc49d867e44d306a969854
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# 検索結果

>[!NOTE]
>
>このページでは、とは異なる可能性のある標準の検索機能について説明します [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

この _検索結果_ リストには、「クイック検索」ボックスまたは「詳細検索」フォームに入力した検索条件に一致するすべての製品が含まれます。 カタログ内のすべての製品リストには、基本的に同じコントロールがあります。 唯一の違いは、1 つは検索クエリの結果であり、もう 1 つは次の結果であることです [ナビゲーション](navigation.md).

結果は、グリッドまたはリストとして書式設定でき、属性の選択で並べ替えることができます。 ページに収まらない商品がある場合は、ページネーションコントロールが表示されます。 これらのコントロールを使用して、ページ間を移動します。 ページあたりのレコード数は、カタログフロントエンド設定によって決定されます。 詳しくは、を参照してください [製品リスト](navigation-product-listings.md).

（を使用） **Elasticsearch**:

- サフィックスによる検索は標準ではサポートされていません。 例えば、キーワードに SKU の最後の部分のみが含まれている場合、SKU で検索しても期待した結果が返されない場合があります。
- のプレフィックスによる検索（部分キーワード検索）は、すぐにサポートされます。 `name` および `sku` 製品属性のみ。 その他のすべての製品属性は、キーワード全体で検索され、完全に一致します。
- の検索結果 `name` および `sku` 製品属性は、完全一致ではなく関連度に基づいています。 最も関連性の高い一致（完全一致など） _製品名_ または _SKU_、が最初に表示されます。 完全一致を検索するには、検索クエリで二重引用符を使用します。 例： `WSH12-32-Red` 検索クエリは、関連度で並べ替えられた、複数の製品を返す場合があります。 しかし、 `"WSH12-32-Red"` 検索クエリは、を持つ 1 つの製品のみを返します **_正確に_** matched `sku`.

![ページネーションコントロールを使用した検索結果](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>2023 年 8 月のElasticsearch 7 のサポート終了のお知らせに伴い、Adobe Commerceのお客様はすべて OpenSearch 2.x 検索エンジンに移行することをお勧めします。 製品のアップグレード中に検索エンジンを移行する方法については、を参照してください。 [OpenSearch への移行](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) が含まれる _アップグレードガイド_.

## 検索結果を拡張するキーワードマッピング

この手法では、属性を使用して 2 つの製品間にキーワードベースの関連付けを作成し、どちらかの製品を検索すると両方の製品の結果が返されるようにします。 キーワードマッピングを使用すると、検索結果で表示されない製品を昇格させることができます。

![キーワードマッピングを使用した検索結果](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

次の例では、SKU に基づくキーワードマッピングを使用しています。 検索ボックスにいずれかの SKU を入力すると、両方の製品が結果に表示されます。 次の設定可能な製品の SKU が、製品バリエーションの SKU ではなく、マッピングされます。

- Montana ウィンドジャケット （MJ03）
- チャズカンガルー・フーディー（MH01）

### 手順 1：属性の作成

1. が含まれる _[!UICONTROL Products]_リストで、を開きます `Montana Wind Jacket` （MJ03）を編集モードで使用します。
1. 右上隅のをクリックします。 **[!UICONTROL Add Attribute]**.
1. 日 _属性を選択_ ページ、クリック **[!UICONTROL Create New Attribute]**.
1. 属性プロパティを次のように設定します。

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label]  - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` （デフォルト）
   - [!UICONTROL Use in Filter Options] - `Yes` （デフォルト）

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. 完了したら、 **[!UICONTROL Save Attribute]**.

   属性が製品の属性セットに追加されます。

### 手順 2：最初の製品をマッピングする

1. 製品設定ページで、下にスクロールして _[!UICONTROL Attributes]_セクション。
1. が含まれる **[!UICONTROL Search Keywords]** SKU を入力してください `MH01` それをこの商品にマッピングします。

   「検索キーワード」フィールドでは、複数の SKU をスペースで区切って入力できます。 この例では、1 つのみ入力されます。

   ![検索キーワードを含む属性セクション](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.
1. に移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**を更新します&#x200B;**[!UICONTROL Page Cache]**.

### 手順 3:2 番目の製品のマッピング

1. が含まれる _[!UICONTROL Products]_リストで、を開きます `Chaz Kangaroo Hoodie` （MH01）を編集モードにします。
1. 下にスクロールして、 **[!UICONTROL Attributes]** セクション。
1. が含まれる **[!UICONTROL Search Keywords]** フィールドに、他の製品の SKU を入力します。 `MJ03`.
1. クリック **[!UICONTROL Save]**.
1. に移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**を更新します&#x200B;**[!UICONTROL Page Cache]**.

### 手順 4：ストアフロントでテストする

1. ストアフロントに移動し、次の場所に入力します `MJ03` が含まれる _クイック検索_ ボックス。
1. 両方の製品が検索結果リストに返されることを確認します。

## 重み付け検索

カタログ検索が有効な製品属性には、重み付けを割り当てて、検索結果の価値を高めることができます。 重み付けが大きい属性は、重み付けが小さい属性より先に返されます。 例えば、システムに 2 つの属性がある場合、 _色_ 検索重み付けが 3 の場合、 _説明_ 検索の重み付けが 1 の場合。 単語の検索 _赤_ color 属性値がの商品のリストを返します `red` 検索結果の上部に、という単語を含む説明を含む製品が返されます _赤_ 検索結果の下部 この例では、 `color` 属性の重み付けは、 `description` 属性。

>[!IMPORTANT]
>
>関連度による並べ替えは、次の場合に影響を受けます **_複数_** 条件とユーザー間の関係 **_同時に_**. [!UICONTROL Search Weight] は、その基準の 1 つにすぎません。 つまり、検索重み付けが小さい属性が、検索重み付けが大きい属性よりも関連性が高い場合があります。 その他の条件には、任意の属性の一致数、見つかった検索語句の位置、検索語句の前後の全体的なテキスト構造などがあります。

**_属性の検索の重み付けプロパティを設定するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. リストで属性を見つけ、編集モードで開きます。

1. 左パネルで、を選択します。 **[!UICONTROL Storefront Properties]** 次の手順を実行します。

   - 検索クエリに属性を含めるには、次を設定します **[!UICONTROL Use in Search]** 対象： `Yes`.

   - 属性の検索値を設定するには、を設定します **[!UICONTROL Search Weight]** 1 から 10 の範囲の数値に変換します。 `10` が最も優先順位が高くなります。 値を入力しない場合、すべての属性はデフォルトで次の検索重み付けになります `1`.

   ![検索の重み付け](./assets/search-weight.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Attribute]**.
