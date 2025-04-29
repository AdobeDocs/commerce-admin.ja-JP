---
title: コンテンツのステージングダッシュボード
description: コンテンツのステージングダッシュボードを使用して、アクティブなキャンペーンと今後のすべてのキャンペーンの概要にアクセスします。
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# コンテンツのステージングダッシュボード

{{ee-feature}}

[!UICONTROL Content Staging] ダッシュボードには、アクティブなキャンペーンと今後のすべてのキャンペーンの概要が表示されます。 ダッシュボードの形式は、グリッドからタイムラインに変更できます。 また、フィルターを使用して、キャンペーンの検索、列のレイアウトのカスタマイズ、グリッドの様々なビューの保存を行うこともできます。 ワークスペースコントロールについて詳しくは、「[Admin Workspace](../getting-started/admin-workspace.md)」を参照してください。

![ グリッド表示のステージングダッシュボード ](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## ステージングダッシュボードの表示

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Content Staging]_/**[!UICONTROL Dashboard]**に移動します。

1. ダッシュボードの形式を変更するには、**[!UICONTROL View As]** コントロールを `list`、`Grid`、または `Timeline` に設定します。

   ![ タイムライン表示 ](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   タイムラインを表示するときに、右下隅のスライダーを使用して、1～4 週間のビューを調整できます。 各列は 1 日を表します。

1. タイムラインが表示されている場合は、スライダーを右端の `4w` の位置にドラッグすると、より長い時間を表示できます。

   ![4 週間ビュー ](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. キャンペーンに関する一般的な情報を表示するには、ページの任意の項目をクリックします。

   - キャンペーンを開くには、「**[!UICONTROL View/Edit]**」をクリックします。

   - その日にストア内の顧客に対してキャンペーンがどのように表示されるかを確認するには、[**[!UICONTROL Preview]**] をクリックします。

   ![ キャンペーン情報 ](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## ステージングダッシュボードの列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Status] | キャンペーンのステータス。 `Active` または `Upcoming`。 |
| [!UICONTROL Update Name] | キャンペーンの名前。 |
| [!UICONTROL Includes] | キャンペーンに含めるオブジェクト数を定義します。 |
| [!UICONTROL Start Time] | キャンペーンが開始する日付。 |
| [!UICONTROL End Time] | キャンペーンが終了する日付。 |
| [!UICONTROL Description] | 各キャンペーンの追加の説明。 |
| [!UICONTROL Action] | 個々のレコードに適用できるアクションは次のとおりです。<br/>**[!UICONTROL View/Edit]**- キャンペーンを編集モードで開きます。<br/>**[!UICONTROL Preview]** - キャンペーンをプレビューモードで表示します。 |

{style="table-layout:auto"}

## キャンペーンの編集

終了日のない価格ルールキャンペーンを除き、既存のキャンペーンオブジェクトをステージングダッシュボードから編集できます。

>[!NOTE]
>
>アクティブなキャンペーンが最初に終了日なしで作成された場合、後でキャンペーンを編集して終了日を含めることはできません。 この場合、重複するキャンペーンを作成し、必要な終了日を入力する必要があります。

![ キャンペーンの詳細 ](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

この例のキャンペーンには、2 つのカテゴリと 3 つの個別の製品が含まれています。

このキャンペーン内のオブジェクトを編集するには、次の手順に従います。

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Content Staging]_/**[!UICONTROL Dashboard]**に移動します。

1. 表示されたリストまたはタイムラインでキャンペーンを見つけて、開いて詳細にアクセスします。

   - リストを表示するには、「**[!UICONTROL Select]**」をクリックし、_[!UICONTROL Action]_の列の「**[!UICONTROL View/Edit]**」をクリックします。
   - タイムライン表示の場合、1 回クリックして概要を表示し、「**[!UICONTROL View/Edit]**」をクリックします。

1. 必要に応じて、「_[!UICONTROL General]_」セクションの設定を更新します。

1. 編集する項目を含んだセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

   ![ キャンペーン品目に割り当てられた製品の更新 ](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save]**」をクリックします。
