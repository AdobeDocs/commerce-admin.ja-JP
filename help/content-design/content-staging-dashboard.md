---
title: コンテンツステージングダッシュボード
description: コンテンツステージングダッシュボードを使用して、アクティブなキャンペーンおよび今後のキャンペーンの概要にアクセスします。
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# コンテンツステージングダッシュボード

{{ee-feature}}

The [!UICONTROL Content Staging] ダッシュボードには、アクティブなキャンペーンと今後のキャンペーンの概要が表示されます。 ダッシュボードの形式は、グリッドからタイムラインに変更できます。 また、フィルターを使用してキャンペーンを検索したり、列のレイアウトをカスタマイズしたり、グリッドの様々な表示を保存したりすることもできます。 ワークスペースのコントロールについて詳しくは、 [管理ワークスペース](../getting-started/admin-workspace.md).

![グリッド表示のステージングダッシュボード](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## ステージングダッシュボードを表示する

1. 次の日： _管理者_ サイドバー、移動  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. ダッシュボードのフォーマットを変更するには、 **[!UICONTROL View As]** ～を制御する `list`, `Grid`または `Timeline`.

   ![タイムライン表示](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   タイムラインが表示されているとき、右下隅のスライダーを使用して表示を 1 週間から 4 週間に調整できます。 各列は 1 日を表します。

1. タイムラインが表示されている場合は、スライダーを `4w` 右端の位置を使用して、長い期間を表示できます。

   ![4 週間表示](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. キャンペーンの一般情報を表示するには、ページ上の任意の項目をクリックします。

   - キャンペーンを開くには、 **[!UICONTROL View/Edit]**.

   - その日のキャンペーンがストア内の顧客にどのように表示されるかを確認するには、 **[!UICONTROL Preview]**.

   ![キャンペーン情報](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## ステージングダッシュボードの列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Status] | キャンペーンのステータス。 `Active` または `Upcoming`. |
| [!UICONTROL Update Name] | キャンペーンの名前。 |
| [!UICONTROL Includes] | キャンペーンに含まれるオブジェクトの数を定義します。 |
| [!UICONTROL Start Time] | キャンペーンが開始する日付。 |
| [!UICONTROL End Time] | キャンペーンが終了する日付。 |
| [!UICONTROL Description] | 各キャンペーンの追加の説明。 |
| [!UICONTROL Action] | 個々のレコードに適用できるアクションには、次のものがあります。<br/>**[!UICONTROL View/Edit]**— キャンペーンを編集モードで開きます。<br/>**[!UICONTROL Preview]**  — キャンペーンをプレビューモードで表示します。 |

{style="table-layout:auto"}

## キャンペーンの編集

終了日のない価格ルールキャンペーンを除き、既存のキャンペーンオブジェクトは、ステージングダッシュボードから編集できます。

>[!NOTE]
>
>価格ルールを含むキャンペーンが終了日なしで最初に作成された場合、キャンペーンを後から編集して終了日を含めることはできません。 その場合は、重複したキャンペーンを作成し、必要な終了日を入力する必要があります。

![キャンペーンの詳細](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

この例のキャンペーンには、2 つのカテゴリと 3 つの個々の製品が含まれています。

このキャンペーンのオブジェクトを編集するには、以下の手順に従います。

1. 次の日： _管理者_ サイドバー、移動  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. 表示されたリストまたはタイムラインでキャンペーンを探し、開いて詳細にアクセスします。

   - リストを表示するには、 **[!UICONTROL Select]** その後 **[!UICONTROL View/Edit]** （内） _[!UICONTROL Action]_列。
   - タイムライン表示の場合、1 回クリックして概要を表示し、 **[!UICONTROL View/Edit]**.

1. の設定を更新します。 _[!UICONTROL General]_セクションを必要に応じて変更します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) 編集する項目を含むセクション。

   ![キャンペーン項目に割り当てられた製品の更新](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.
