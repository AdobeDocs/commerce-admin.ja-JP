---
title: 自動リダイレクト
description: Commerce ストアで商品またはカテゴリの URL キーが変更された場合に自動的にリダイレクトを生成するように設定する方法を説明します。
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# 自動リダイレクト

製品またはカテゴリの URL キーが変更されるたびに永続的なリダイレクトを自動的に生成するようにストアを設定できます。 「検索エンジンの最適化」セクションで、URL キーの下のチェックボックスは、永続的なリダイレクトが有効かどうかを示します。 カタログ URL を自動的にリダイレクトするようにストアが既に設定されている場合、リダイレクトは URL キーへの簡単な更新です。 自動リダイレクトの作成手順は、製品とカテゴリの両方で同じです。

>[!NOTE]
>
>自動リダイレクトを有効にしてカテゴリを保存すると、すべての製品およびカテゴリの書き換えがリアルタイムで生成され、デフォルトでデータベーステーブルに保存されます。 その結果、製品が多数割り当てられているカテゴリでは、パフォーマンスに関して重大な問題が発生する可能性があります。 解決策は、このデフォルトを変更して、カテゴリの保存時に製品のカテゴリ/製品 URL の書き換えの生成をスキップすることです。 この場合、製品の書き換えは正規の製品 URL に対してのみ生成されます。

## 自動リダイレクトの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Search Engine Optimization]**」セクションを展開します。

   ![ カタログ設定 – 検索エンジンの最適化 ](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。


>[!NOTE]
>
> URL の書き換えは、ストア表示または web サイト範囲に対して生成できます。 **[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;**[!UICONTROL Catalog]**/**[!UICONTROL Catalog]**/**[!UICONTROL Search Engine Optimization]**&#x200B;の管理者から、URL 書き換え範囲を設定します。 「_[!UICONTROL Product URL Rewrite Scope]_」フィールドで範囲を選択します。

## 製品 URL を自動的にリダイレクト

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. リストで製品を見つけ、クリックしてレコードを開きます。

1. 「**[!UICONTROL Search Engine Optimization]**」セクション ![&#128279;](../assets/icon-display-expand.png) 展開セレクター」を展開します。

   ![ 製品検索エンジンの最適化 – 永続的なリダイレクト ](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. **[!UICONTROL URL Key]** の場合は、次の手順を実行します。

   - 「**[!UICONTROL Create Permanent Redirect for old URL]**」チェックボックスが選択されていることを確認します。 表示されない場合は、手順に従って [ 自動リダイレクトを有効にする ](url-rewrite.md#configure-url-rewrites) ください。

   - 必要に応じて **[!UICONTROL URL Key]** を更新し、スペースの代わりにこれらの文字の間に小文字と末尾でないハイフンをすべて使用します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. キャッシュを更新するように求められたら、ワークスペースの上部にあるメッセージのリンクに従います。

   これで、製品および関連するカテゴリ URL に対して、永続的なリダイレクトが有効になります。

## カテゴリ URL を自動的にリダイレクト

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. ツリーでカテゴリを見つけ、クリックしてレコードを開きます。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Search Engine Optimization]**」セクションを展開します。

1. **[!UICONTROL URL Key]** の場合は、次の手順を実行します。

   - 「**[!UICONTROL Create Permanent Redirect for old URL]**」チェックボックスが選択されていることを確認します。 表示されない場合は、手順に従って [ 自動リダイレクトを有効にする ](url-rewrite.md#configure-url-rewrites) ください。

   - 必要に応じて **[!UICONTROL URL Key]** を更新し、スペースの代わりにこれらの文字の間に小文字と末尾でないハイフンをすべて使用します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. キャッシュを更新するように求められたら、ワークスペースの上部にあるメッセージのリンクに従います。

   これで、カテゴリおよび関連する製品 URL に対して、永続的なリダイレクトが有効になります。

## カテゴリ保存の製品 URL 書き換えの生成をスキップ {#skip-rewrite}

>[!WARNING]
>
>カテゴリ/製品の URL 書き換えの自動生成をオフにすると、既存のカテゴリ/製品タイプの URL の書き換えが完全に削除されますが、復元することはできません。 これにより、未解決のカテゴリや製品タイプの URL の競合が発生する可能性があり、解決するために URL キーを手動で更新する必要が生じる場合があります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Search Engine Optimization]**」セクションを展開します。

1. **[!UICONTROL Generate "category/product" URL Rewrites]** を `No` に設定します。

1. 確認ダイアログで、「**[!UICONTROL OK]**」をクリックして、変更と既存の URL の書き換えの削除を確認します。

   ![ カテゴリ/製品 URL の書き換えを無効にする – 確認 ](./assets/seo-rewrite-off.png){width="350"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
