---
title: 自動リダイレクト
description: Commerce ストアで商品またはカテゴリの URL キーが変更された場合に自動的にリダイレクトを生成するように設定する方法を説明します。
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# 自動リダイレクト

製品またはカテゴリの URL キーが変更されるたびに永続的なリダイレクトを自動的に生成するようにストアを設定できます。 「検索エンジンの最適化」セクションで、URL キーの下のチェックボックスは、永続的なリダイレクトが有効かどうかを示します。 カタログ URL を自動的にリダイレクトするようにストアが既に設定されている場合、リダイレクトは URL キーへの簡単な更新です。 自動リダイレクトの作成手順は、製品とカテゴリの両方で同じです。

>[!NOTE]
>
>自動リダイレクトを有効にしてカテゴリを保存すると、すべての製品およびカテゴリの書き換えがリアルタイムで生成され、デフォルトでデータベーステーブルに保存されます。 その結果、製品が多数割り当てられているカテゴリでは、パフォーマンスに関して重大な問題が発生する可能性があります。 解決策は、このデフォルトを変更して、カテゴリの保存時に製品のカテゴリ/製品 URL の書き換えの生成をスキップすることです。 この場合、製品の書き換えは正規の製品 URL に対してのみ生成されます。

## 自動リダイレクトの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization]** セクション。

   ![カタログ設定 – 検索エンジンの最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

## 製品 URL を自動的にリダイレクト

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. リストで製品を見つけ、クリックしてレコードを開きます。

1. を展開 ![展開セレクター ](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization]** セクション。

   ![製品検索エンジンの最適化 – 永続的なリダイレクト](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL URL Key]**、次の手順を実行します。

   - 次のことを確認します **[!UICONTROL Create Permanent Redirect for old URL]** チェックボックスが選択されています。 そうでない場合は、次の手順に従います。 [自動リダイレクトを有効にする](url-rewrite.md#configure-url-rewrites).

   - を更新 **[!UICONTROL URL Key]** 必要に応じて、スペースの代わりにこれらの文字の間にすべての小文字と末尾でないハイフンを使用します。

1. 完了したら、 **[!UICONTROL Save]**.

1. キャッシュを更新するように求められたら、ワークスペースの上部にあるメッセージのリンクに従います。

   これで、製品および関連するカテゴリ URL に対して、永続的なリダイレクトが有効になります。

## カテゴリ URL を自動的にリダイレクト

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. ツリーでカテゴリを見つけ、クリックしてレコードを開きます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization]** セクション。

1. の場合 **[!UICONTROL URL Key]**、次の手順を実行します。

   - 次のことを確認します **[!UICONTROL Create Permanent Redirect for old URL]** チェックボックスが選択されています。 そうでない場合は、次の手順に従います。 [自動リダイレクトを有効にする](url-rewrite.md#configure-url-rewrites).

   - を更新 **[!UICONTROL URL Key]** 必要に応じて、スペースの代わりにこれらの文字の間にすべての小文字と末尾でないハイフンを使用します。

1. 完了したら、 **[!UICONTROL Save]**.

1. キャッシュを更新するように求められたら、ワークスペースの上部にあるメッセージのリンクに従います。

   これで、カテゴリおよび関連する製品 URL に対して、永続的なリダイレクトが有効になります。

## カテゴリ保存の製品 URL 書き換えの生成をスキップ {#skip-rewrite}

>[!WARNING]
>
>カテゴリ/製品の URL 書き換えの自動生成をオフにすると、既存のカテゴリ/製品タイプの URL の書き換えが完全に削除されますが、復元することはできません。 これにより、未解決のカテゴリや製品タイプの URL の競合が発生する可能性があり、解決するために URL キーを手動で更新する必要が生じる場合があります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization]** セクション。

1. を設定 **[!UICONTROL Generate "category/product" URL Rewrites]** 対象： `No`.

1. 確認ダイアログで、 **[!UICONTROL OK]** 既存の URL の書き換えの変更と削除を確認します。

   ![カテゴリ/製品 URL の書き換えを無効にする – 確認](./assets/seo-rewrite-off.png){width="350"}

1. 完了したら、 **[!UICONTROL Save Config]**.
