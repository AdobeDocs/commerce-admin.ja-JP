---
title: 自動リダイレクト
description: Commerce ストアで商品またはカテゴリの URL キーが変更された場合に自動的にリダイレクトを生成するように設定する方法を説明します。
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: d088d5833b9c61e7b1c90a0839fdf38527929ce5
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# 自動リダイレクト

製品またはカテゴリの URL キーが変更されるたびに永続的なリダイレクトを自動的に生成するようにストアを設定できます。 「検索エンジンの最適化」セクションで、URL キーの下のチェックボックスは、永続的なリダイレクトが有効かどうかを示します。 If your store is already configured to automatically redirect catalog URLs, a redirect is a simple update to the URL key. 自動リダイレクトの作成手順は、製品とカテゴリの両方で同じです。

>[!NOTE]
>
>自動リダイレクトを有効にしてカテゴリを保存すると、すべての製品およびカテゴリの書き換えがリアルタイムで生成され、デフォルトでデータベーステーブルに保存されます。 その結果、製品が多数割り当てられているカテゴリでは、パフォーマンスに関して重大な問題が発生する可能性があります。 解決策は、このデフォルトを変更して、カテゴリの保存時に製品のカテゴリ/製品 URL の書き換えの生成をスキップすることです。 この場合、製品の書き換えは正規の製品 URL に対してのみ生成されます。

## 自動リダイレクトの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. In left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Search Engine Optimization]**」セクションを展開します。

   ![Catalog configuration - search engine optimization](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。


>[!NOTE]
>
> URL の書き換えは、ストア表示または web サイト範囲に対して生成できます。 Set the URL rewrite scope from the Admin at **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]****[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Select the scope in the_[!UICONTROL Product URL Rewrite Scope]_ field.

## Automatically redirect product URLs

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. Find the product in the list and click to open the record.

1. Expand ![Expansion selector ](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Optimization]** section.

   ![ 製品検索エンジンの最適化 – 永続的なリダイレクト ](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. **[!UICONTROL URL Key]** の場合は、次の手順を実行します。

   - 「**[!UICONTROL Create Permanent Redirect for old URL]**」チェックボックスが選択されていることを確認します。 表示されない場合は、手順に従って [ 自動リダイレクトを有効にする ](url-rewrite.md#configure-url-rewrites) ください。

   - Update the **[!UICONTROL URL Key]** as needed, using all lowercase characters and non-trailing hyphens between these characters instead of spaces.

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. キャッシュを更新するように求められたら、ワークスペースの上部にあるメッセージのリンクに従います。

   これで、製品および関連するカテゴリ URL に対して、永続的なリダイレクトが有効になります。

## カテゴリ URL を自動的にリダイレクト

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. ツリーでカテゴリを見つけ、クリックしてレコードを開きます。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Search Engine Optimization]**」セクションを展開します。

1. **[!UICONTROL URL Key]** の場合は、次の手順を実行します。

   - 「**[!UICONTROL Create Permanent Redirect for old URL]**」チェックボックスが選択されていることを確認します。 表示されない場合は、手順に従って [ 自動リダイレクトを有効にする ](url-rewrite.md#configure-url-rewrites) ください。

   - Update the **[!UICONTROL URL Key]** as needed, using all lowercase characters and non-trailing hyphens between these characters instead of spaces.

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. キャッシュを更新するように求められたら、ワークスペースの上部にあるメッセージのリンクに従います。

   The permanent redirect is now in effect for the category and any associated product URLs.

## Skip generation of product URL rewrites for category save {#skip-rewrite}

>[!WARNING]
>
>Turning off automatic generation of category/products URL rewrites results in permanent removal of all existing category/product type URL rewrites, which cannot be restored. This could potentially cause unresolved category/product type URL conflicts that require a manual update of the URL key to resolve.

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. In left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Search Engine Optimization]**」セクションを展開します。

1. **[!UICONTROL Generate "category/product" URL Rewrites]** を `No` に設定します。

1. 確認ダイアログで、「**[!UICONTROL OK]**」をクリックして、変更と既存の URL の書き換えの削除を確認します。

   ![Turn off category/product URL rewrites - confirm](./assets/seo-rewrite-off.png){width="350"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
