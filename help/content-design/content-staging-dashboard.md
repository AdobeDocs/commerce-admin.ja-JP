---
title: コンテンツのステージングダッシュボード
description: コンテンツのステージングダッシュボードを使用して、アクティブなキャンペーンと今後のすべてのキャンペーンの概要にアクセスします。
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# コンテンツのステージングダッシュボード

{{ee-feature}}

この [!UICONTROL Content Staging] ダッシュボードには、アクティブなキャンペーンと今後のすべてのキャンペーンの概要が表示されます。 ダッシュボードの形式は、グリッドからタイムラインに変更できます。 また、フィルターを使用して、キャンペーンの検索、列のレイアウトのカスタマイズ、グリッドの様々なビューの保存を行うこともできます。 ワークスペース コントロールの詳細については、を参照してください。 [管理ワークスペース](../getting-started/admin-workspace.md).

![グリッド表示のステージングダッシュボード](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## ステージングダッシュボードの表示

1. 日 _Admin_ サイドバー、に移動  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. ダッシュボードの形式を変更するには、 **[!UICONTROL View As]** コントロール先 `list`, `Grid`、または `Timeline`.

   ![タイムライン表示](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   タイムラインを表示するときに、右下隅のスライダーを使用して、1～4 週間のビューを調整できます。 各列は 1 日を表します。

1. タイムラインが表示されている場合は、スライダーをにドラッグします `4w` 右端に移動すると、表示される時間が長くなります。

   ![4 週間ビュー](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. キャンペーンに関する一般的な情報を表示するには、ページの任意の項目をクリックします。

   - キャンペーンを開くには、をクリックします **[!UICONTROL View/Edit]**.

   - その日にストア内の顧客に対してキャンペーンがどのように表示されるかを確認するには、次をクリックします **[!UICONTROL Preview]**.

   ![キャンペーン情報](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## ステージングダッシュボードの列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Status] | キャンペーンのステータス。 `Active` または `Upcoming`. |
| [!UICONTROL Update Name] | キャンペーンの名前。 |
| [!UICONTROL Includes] | キャンペーンに含めるオブジェクト数を定義します。 |
| [!UICONTROL Start Time] | キャンペーンが開始する日付。 |
| [!UICONTROL End Time] | キャンペーンが終了する日付。 |
| [!UICONTROL Description] | 各キャンペーンの追加の説明。 |
| [!UICONTROL Action] | 個々のレコードに適用できるアクションを以下に示します。<br/>**[!UICONTROL View/Edit]**– 編集モードでキャンペーンを開きます。<br/>**[!UICONTROL Preview]** - キャンペーンをプレビューモードで表示します。 |

{style="table-layout:auto"}

## キャンペーンの編集

終了日のない価格ルールキャンペーンを除き、既存のキャンペーンオブジェクトをステージングダッシュボードから編集できます。

>[!NOTE]
>
>価格ルールを含むキャンペーンが最初に終了日なしで作成された場合、後でキャンペーンを編集して終了日を含めることはできません。 この場合、重複するキャンペーンを作成し、必要な終了日を入力する必要があります。

![キャンペーンの詳細](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

この例のキャンペーンには、2 つのカテゴリと 3 つの個別の製品が含まれています。

このキャンペーン内のオブジェクトを編集するには、次の手順に従います。

1. 日 _Admin_ サイドバー、に移動  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. 表示されたリストまたはタイムラインでキャンペーンを見つけて、開いて詳細にアクセスします。

   - リストを表示するには、 **[!UICONTROL Select]** その後 **[!UICONTROL View/Edit]** が含まれる _[!UICONTROL Action]_列。
   - タイムライン表示の場合、1 回クリックして概要を表示し、次にクリックします **[!UICONTROL View/Edit]**.

1. の設定を更新します。 _[!UICONTROL General]_必要に応じて、「」を選択します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) 編集する項目を含むセクション。

   ![キャンペーン項目に割り当てられた製品の更新](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.
