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
>このページでは、[ ライブサーチ ](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) とは異なる可能性のある標準の検索機能について説明します。

_検索結果_ リストには、「クイック検索」ボックスまたは「詳細検索」フォームに入力した検索条件に一致するすべての製品が表示されます。 カタログ内のすべての製品リストには、基本的に同じコントロールがあります。 唯一の違いは、1 つは検索クエリの結果であり、もう 1 つは [ ナビゲーション ](navigation.md) の結果であることです。

結果は、グリッドまたはリストとして書式設定でき、属性の選択で並べ替えることができます。 ページに収まらない商品がある場合は、ページネーションコントロールが表示されます。 これらのコントロールを使用して、ページ間を移動します。 ページあたりのレコード数は、カタログフロントエンド設定によって決定されます。 詳しくは、[ 製品リスト ](navigation-product-listings.md) を参照してください。

**Elasticsearch**:

- サフィックスによる検索は標準ではサポートされていません。 例えば、キーワードに SKU の最後の部分のみが含まれている場合、SKU で検索しても期待した結果が返されない場合があります。
- `name` と `sku` の製品属性のみをプレフィックスで検索（部分キーワード検索）する機能は、すぐにサポートされています。 その他のすべての製品属性は、キーワード全体で検索され、完全に一致します。
- `name` と `sku` の製品属性の検索結果は、完全一致ではなく関連度に基づいています。 最も関連性の高い一致（完全に一致した _製品名_ や _SKU_ など）が最初に表示されます。 完全一致を検索するには、検索クエリで二重引用符を使用します。 例えば、`WSH12-32-Red` 検索クエリは、関連度で並べ替えられた、複数の製品を返す場合があります。 ただし、`"WSH12-32-Red"` 検索クエリは、「完全に **_一致する `sku` を持つ製品を 1 つだけ返_** ます。

![ ページネーションコントロールを使用した検索結果 ](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>2023 年 8 月のElasticsearch 7 のサポート終了のお知らせに伴い、Adobe Commerceのお客様はすべて OpenSearch 2.x 検索エンジンに移行することをお勧めします。 製品のアップグレード中に検索エンジンを移行する方法については、[ アップグレード ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) の _OpenSearch への移行_ を参照してください。

## 検索結果を拡張するキーワードマッピング

この手法では、属性を使用して 2 つの製品間にキーワードベースの関連付けを作成し、どちらかの製品を検索すると両方の製品の結果が返されるようにします。 キーワードマッピングを使用すると、検索結果で表示されない製品を昇格させることができます。

![ キーワードマッピングを使用した検索結果 ](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

次の例では、SKU に基づくキーワードマッピングを使用しています。 検索ボックスにいずれかの SKU を入力すると、両方の製品が結果に表示されます。 次の設定可能な製品の SKU が、製品バリエーションの SKU ではなく、マッピングされます。

- Montana ウィンドジャケット （MJ03）
- チャズカンガルー・フーディー（MH01）

### 手順 1：属性の作成

1. _[!UICONTROL Products]_リストで、`Montana Wind Jacket` （MJ03）を編集モードで開きます。
1. 右上隅の「**[!UICONTROL Add Attribute]**」をクリックします。
1. _属性を選択_ ページで「**[!UICONTROL Create New Attribute]**」をクリックします。
1. 属性プロパティを次のように設定します。

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label] - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` （デフォルト）
   - [!UICONTROL Use in Filter Options] - `Yes` （デフォルト）

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。

   属性が製品の属性セットに追加されます。

### 手順 2：最初の製品をマッピングする

1. 製品設定ページで、下にスクロールして「_[!UICONTROL Attributes]_」セクションを展開します。
1. 「**[!UICONTROL Search Keywords]**」フィールドに、この製品にマッピングする SKU `MH01` を入力します。

   「検索キーワード」フィールドでは、複数の SKU をスペースで区切って入力できます。 この例では、1 つのみ入力されます。

   ![ 検索キーワードを含む属性セクション ](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。
1. **[!UICONTROL System]**/_[!UICONTROL Tools]_/**[!UICONTROL Cache Management]**に移動し、**[!UICONTROL Page Cache]**を更新します。

### 手順 3:2 番目の製品のマッピング

1. _[!UICONTROL Products]_リストで、`Chaz Kangaroo Hoodie` （MH01）を編集モードで開きます。
1. 下にスクロールして、「**[!UICONTROL Attributes]**」セクションを展開します。
1. 「**[!UICONTROL Search Keywords]**」フィールドに、他の製品の SKU`MJ03` を入力します。
1. 「**[!UICONTROL Save]**」をクリックします。
1. **[!UICONTROL System]**/_[!UICONTROL Tools]_/**[!UICONTROL Cache Management]**に移動し、**[!UICONTROL Page Cache]**を更新します。

### 手順 4：ストアフロントでテストする

1. ストアフロントに移動し、「クイック検索 _ボックスに `MJ03` と入力し_ す。
1. 両方の製品が検索結果リストに返されることを確認します。

## 重み付け検索

カタログ検索が有効な製品属性には、重み付けを割り当てて、検索結果の価値を高めることができます。 重み付けが大きい属性は、重み付けが小さい属性より先に返されます。 例えば、システムに 2 つの属性がある場合、_color_ の検索重み付けは 3 で、_description_ の検索重み付けは 1 です。 _red_ という単語を検索すると、検索結果の先頭に色属性値 `red` が付いた商品の一覧が返され、検索結果の末尾に _red_ という単語を含む説明を持つ商品が返されます。 この例では、`color` 属性の重み付けは `description` 属性よりも大きくなります。

>[!IMPORTANT]
>
>関連度による並べ替えは、**_複数_** の条件およびそれらの間の関係 **_同時_** の影響を受けます。 [!UICONTROL Search Weight] れはその基準の一つにすぎない。 つまり、検索重み付けが小さい属性が、検索重み付けが大きい属性よりも関連性が高い場合があります。 その他の条件には、任意の属性の一致数、見つかった検索語句の位置、検索語句の前後の全体的なテキスト構造などがあります。

**_属性の検索の重み付けプロパティを設定するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**に移動します。

1. リストで属性を見つけ、編集モードで開きます。

1. 左側のパネルで「**[!UICONTROL Storefront Properties]**」を選択し、次の操作を実行します。

   - 検索クエリに属性を含めるには、**[!UICONTROL Use in Search]** を `Yes` に設定します。

   - 属性の検索値を確立するには、**[!UICONTROL Search Weight]** を 1～10 の数値に設定します。`10` が最も優先度が高くなります。 値を入力しない場合、すべての属性のデフォルトの検索重み付けは `1` になります。

   ![Search Weight](./assets/search-weight.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。
