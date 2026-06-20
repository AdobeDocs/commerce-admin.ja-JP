---
title: 自動リダイレクト
description: Commerce ストアで商品またはカテゴリのURL キーが変更されるたびに生成される自動リダイレクトを設定する方法について説明します。
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/Vscg-TDdLnzKjdi-SMwrcpR-QDPvlHpPzgmcLe63-4Q
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 571
ht-degree: 0%

---

# 自動リダイレクト

ストアは、製品またはカテゴリのURL キーが変更されるたびに、永続的なリダイレクトを自動的に生成するように設定できます。 検索エンジン最適化セクションで、URL キーの下のチェックボックスは、永続的なリダイレクトが有効かどうかを示します。 ストアが既にカタログ URLを自動的にリダイレクトするように設定されている場合、リダイレクトはURL キーへの簡単な更新です。 自動リダイレクトを作成するプロセスは、製品とカテゴリの両方で同じです。

>[!NOTE]
>
>自動リダイレクトが有効になっていて、カテゴリを保存すると、すべての製品およびカテゴリの書き換えがリアルタイムで生成され、デフォルトでデータベーステーブルに保存されます。 これは、多くの製品が割り当てられたカテゴリで、パフォーマンスに大きな問題が発生する可能性があります。 解決策は、このデフォルトを変更し、カテゴリ保存時に製品のカテゴリ/製品URL書き換えの生成をスキップすることです。 この場合、製品の書き換えは、正規の製品URLに対してのみ生成されます。

## 自動リダイレクトの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Search Engine Optimization]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![&#x200B; カタログ設定 – 検索エンジン最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]**&#x200B;を`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。


>[!NOTE]
>
> URLの書き換えは、ストアビューまたはweb サイトのスコープに対して生成できます。 管理者からのURL書き換え範囲を&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;**[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**&#x200B;に設定します。_[!UICONTROL Product URL Rewrite Scope]_ フィールドで範囲を選択します。

## 商品URLを自動的にリダイレクト

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

1. リスト内の製品を見つけて、クリックしてレコードを開きます。

1. **[!UICONTROL Search Engine Optimization]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![製品検索エンジン最適化 – 永続的なリダイレクト &#x200B;](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. **[!UICONTROL URL Key]**&#x200B;に対して、次の操作を行います。

   - 「**[!UICONTROL Create Permanent Redirect for old URL]**」チェックボックスが選択されていることを確認します。 そうでない場合は、[自動リダイレクトを有効にする](url-rewrite.md#configure-url-rewrites)の手順に従ってください。

   - 必要に応じて、**[!UICONTROL URL Key]**&#x200B;を更新します。スペースの代わりに、これらの文字間のすべての小文字と末尾を除くハイフンを使用します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

1. キャッシュの更新を求めるメッセージが表示されたら、ワークスペースの上部にあるメッセージ内のリンクに従います。

   恒久的なリダイレクトは、製品および関連するカテゴリ URLに対して有効になりました。

## カテゴリ URLを自動的にリダイレクト

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. ツリー内のカテゴリを検索し、クリックしてレコードを開きます。

1. **[!UICONTROL Search Engine Optimization]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL URL Key]**&#x200B;に対して、次の操作を行います。

   - 「**[!UICONTROL Create Permanent Redirect for old URL]**」チェックボックスが選択されていることを確認します。 そうでない場合は、[自動リダイレクトを有効にする](url-rewrite.md#configure-url-rewrites)の手順に従ってください。

   - 必要に応じて、**[!UICONTROL URL Key]**&#x200B;を更新します。スペースの代わりに、これらの文字間のすべての小文字と末尾を除くハイフンを使用します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

1. キャッシュの更新を求めるメッセージが表示されたら、ワークスペースの上部にあるメッセージ内のリンクに従います。

   これで、カテゴリと関連する製品URLに対して、永続的なリダイレクトが有効になりました。

## カテゴリ保存の製品URL書き換えの生成をスキップ {#skip-rewrite}

>[!WARNING]
>
>カテゴリ/製品URL書き換えの自動生成をオフにすると、既存のカテゴリ/製品タイプ URL書き換えがすべて永続的に削除され、復元できなくなります。 これにより、未解決のカテゴリ/製品タイプ URLの競合が発生する可能性があり、解決するにはURL キーの手動アップデートが必要です。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Search Engine Optimization]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Generate "category/product" URL Rewrites]**&#x200B;を`No`に設定します。

1. 確認ダイアログで「**[!UICONTROL OK]**」をクリックし、既存のURLの書き換えの変更と削除を確認します。

   ![&#x200B; カテゴリ/製品URLの書き換えをオフにする – 確認](./assets/seo-rewrite-off.png){width="350"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
