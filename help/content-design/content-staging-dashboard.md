---
title: コンテンツのステージングダッシュボード
description: コンテンツのステージングダッシュボードを使用して、アクティブなキャンペーンと今後のキャンペーンの概要にアクセスできます。
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/Hwrb3dYdJlggWN-Z-nUKxVBhsejFMZR-yWIgRzfJifQ
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# コンテンツのステージングダッシュボード

{{ee-feature}}

[!UICONTROL Content Staging] ダッシュボードには、アクティブなすべてのキャンペーンと今後のキャンペーンの概要が表示されます。 ダッシュボードの形式は、グリッドからタイムラインに変更できます。 また、フィルターを使用してキャンペーンを検索したり、列レイアウトをカスタマイズしたり、グリッドの様々なビューを保存したりすることもできます。 ワークスペース制御について詳しくは、[管理者ワークスペース ](../getting-started/admin-workspace.md)を参照してください。

![ グリッドビューでのステージングダッシュボード ](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## ステージングダッシュボードを見る

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**に移動します。

1. ダッシュボードの形式を変更するには、**[!UICONTROL View As]** コントロールを`list`、`Grid`、または`Timeline`に設定します。

   ![ タイムラインビュー](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   タイムラインが表示されている場合、右下隅のスライダーを使用して、1週間から4週間のビューを調整できます。 各列は1日を表します。

1. タイムラインが表示されている場合は、スライダーを右端の`4w`位置までドラッグして、長いスパンを表示します。

   ![4週間のビュー](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. キャンペーンに関する一般的な情報を表示するには、ページ上の任意の項目をクリックします。

   - キャンペーンを開くには、**[!UICONTROL View/Edit]**&#x200B;をクリックします。

   - その日にストアの顧客にキャンペーンがどのように表示されるかを確認するには、**[!UICONTROL Preview]**&#x200B;をクリックします。

   ![ キャンペーン情報](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## ステージングダッシュボードの列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Status] | キャンペーンのステータス： `Active`または`Upcoming`。 |
| [!UICONTROL Update Name] | キャンペーンの名前。 |
| [!UICONTROL Includes] | キャンペーンに含めるオブジェクトの数を定義します。 |
| [!UICONTROL Start Time] | キャンペーンが開始される日付。 |
| [!UICONTROL End Time] | キャンペーンが終了する日付。 |
| [!UICONTROL Description] | 各キャンペーンの追加説明。 |
| [!UICONTROL Action] | 個々のレコードに適用できるアクションは次のとおりです。<br/>**[!UICONTROL View/Edit]**- キャンペーンを編集モードで開きます。<br/>**[!UICONTROL Preview]** - キャンペーンをプレビューモードで表示します。 |

{style="table-layout:auto"}

## キャンペーンの編集

既存のキャンペーンオブジェクトは、終了日のない価格ルールキャンペーンを除き、ステージングダッシュボードから編集できます。

>[!NOTE]
>
>アクティブなキャンペーンが最初に終了日なしで作成された場合、そのキャンペーンを後で編集して終了日を含めることはできません。 この場合、重複する施策を作成し、必要な終了日を入力する必要があります。

![ キャンペーンの詳細](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

この例のキャンペーンには、2つのカテゴリと3つの個別の製品が含まれています。

このキャンペーンのオブジェクトを編集するには、次の手順に従います。

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**に移動します。

1. 表示されたリストまたはタイムラインでキャンペーンを見つけ、それを開いて詳細にアクセスします。

   - リストを表示するには、**[!UICONTROL Select]**&#x200B;をクリックし、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL View/Edit]**をクリックします。
   - タイムライン表示の場合は、1回クリックして概要を表示し、**[!UICONTROL View/Edit]**&#x200B;をクリックします。

1. 必要に応じて、_[!UICONTROL General]_セクションのいずれかの設定を更新します。

1. ![拡張セレクター](../assets/icon-display-expand.png)を展開して、編集対象の項目を含む任意のセクションを展開します。

   ![ キャンペーン項目に割り当てられた製品を更新しています](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save]**&#x200B;をクリックします。
