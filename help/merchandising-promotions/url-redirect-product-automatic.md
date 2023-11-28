---
title: 自動リダイレクト
description: 商品やカテゴリの URL キーがコマースストアで変更された場合に常に自動リダイレクトが生成されるように設定する方法を説明します。
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# 自動リダイレクト

ストアは、製品やカテゴリの URL キーが変更されるたびに、永続的なリダイレクトを自動的に生成するように設定できます。 「検索エンジンの最適化」セクションの URL キーの下にあるチェックボックスは、永続的なリダイレクトが有効になっているかどうかを示します。 ストアが既にカタログ URL を自動的にリダイレクトするように設定されている場合、リダイレクトは URL キーに対する簡単な更新です。 自動リダイレクトの作成手順は、製品とカテゴリの両方で同じです。

>[!NOTE]
>
>自動リダイレクトを有効にしてカテゴリを保存すると、製品とカテゴリのすべての書き換えがリアルタイムで生成され、デフォルトでデータベーステーブルに保存されます。 これにより、多くの製品が割り当てられたカテゴリのパフォーマンスが大幅に低下する可能性があります。 解決策は、このデフォルトを変更し、カテゴリの保存時に製品に対して書き換えるカテゴリ/製品 URL の生成をスキップすることです。 この場合、製品の書き換えは、正規の製品 URL に対してのみ生成されます。

## 自動リダイレクトの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** 」セクションに入力します。

   ![カタログ設定 — 検索エンジンの最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 製品 URL を自動的にリダイレクト

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. リスト内の製品を探し、をクリックしてレコードを開きます。

1. 展開 ![拡張セレクター ](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** 」セクションに入力します。

   ![製品検索エンジンの最適化 — 永続的なリダイレクト](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL URL Key]**、次の操作を実行します。

   - 次を確認します。 **[!UICONTROL Create Permanent Redirect for old URL]** チェックボックスがオンになっている。 そうでない場合は、次の手順に従います。 [自動リダイレクトを有効にする](url-rewrite.md#configure-url-rewrites).

   - を更新します。 **[!UICONTROL URL Key]** 必要に応じて、スペースの代わりに、すべての小文字と末尾にハイフン以外を使用します。

1. 完了したら、「 **[!UICONTROL Save]**.

1. キャッシュを更新するように求められたら、ワークスペースの上部にあるメッセージ内のリンクに従います。

   製品と関連するカテゴリ URL に対して、永続的なリダイレクトが有効になりました。

## カテゴリ URL を自動的にリダイレクト

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. ツリー内のカテゴリを探し、クリックしてレコードを開きます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** 」セクションに入力します。

1. の場合 **[!UICONTROL URL Key]**、次の操作を実行します。

   - 次を確認します。 **[!UICONTROL Create Permanent Redirect for old URL]** チェックボックスがオンになっている。 そうでない場合は、次の手順に従います。 [自動リダイレクトを有効にする](url-rewrite.md#configure-url-rewrites).

   - を更新します。 **[!UICONTROL URL Key]** 必要に応じて、スペースの代わりに、すべての小文字と末尾にハイフン以外を使用します。

1. 完了したら、「 **[!UICONTROL Save]**.

1. キャッシュを更新するように求められたら、ワークスペースの上部にあるメッセージ内のリンクに従います。

   カテゴリと関連する製品 URL に対して、永続的なリダイレクトが有効になりました。

## カテゴリの保存に対する製品 URL の書き換えの生成をスキップ {#skip-rewrite}

>[!WARNING]
>
>カテゴリ/製品の URL の書き換えの自動生成をオフにすると、既存のカテゴリ/製品タイプの URL の書き換えがすべて完全に削除され、復元できなくなります。 これにより、解決する URL キーを手動で更新する必要がある、未解決のカテゴリ/製品タイプの URL の競合が発生する可能性があります。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** 」セクションに入力します。

1. 設定 **[!UICONTROL Generate "category/product" URL Rewrites]** から `No`.

1. 確認ダイアログで、 **[!UICONTROL OK]** をクリックして、既存の URL の書き換えの変更と削除を確認します。

   ![カテゴリ/製品 URL の書き換えをオフにする — 確認](./assets/seo-rewrite-off.png){width="350"}

1. 完了したら、「 **[!UICONTROL Save Config]**.
