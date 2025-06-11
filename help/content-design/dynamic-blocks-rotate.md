---
title: 回転するダイナミック ブロックを追加する
description: 複数の動的ブロックをロテータに追加して、インタラクティブ コンテンツのスライド ショーをストアフロントに表示します。
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# 回転するダイナミック ブロックを追加する

{{ee-feature}}

インタラクティブコンテンツのスライドショーを表示するには、ロテーターに複数の [ 動的ブロック ](dynamic-blocks.md) を追加します。 [ ウィジェット ](widgets.md) ツールを使用すると、ローテーターを単一ページまたはストア全体の複数ページの特定の場所に配置できます。

![ ダイナミック ブロック ローテータ ](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## 手順 1：個々のダイナミック ブロックを作成する

ロテータに配置する [ ダイナミック ブロックを作成する ](dynamic-blocks.md) には、次の手順に従います。

## 手順 2：動的ブロックローテータウィジェットの追加

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Widgets]**に移動します。

1. 右上隅の「**[!UICONTROL Add Widget]**」をクリックします。

1. _設定_ で、**[!UICONTROL Type]** を `Dynamic Blocks Rotator` に設定します。

1. ストアの現在の **[!UICONTROL Design Theme]** を選択します。

   この設定は、ストアのページレイアウトを決定する現在のパッケージまたは [ テーマ ](themes.md) を識別します。

1. 「**[!UICONTROL Continue]**」をクリックします。

   ![ ダイナミック ブロック回転子設定 ](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## 手順 3：オプションの完了

1. _ストアフロントのプロパティ_ で、次のオプションを設定します。

   - ロテータの **[!UICONTROL Title]** を入力します。

   - **[!UICONTROL Assign to Store Views]** リストで、ロテータが使用可能な [ ストア ビュー ](../getting-started/websites-stores-views.md) を選択します。

   - （オプション）ターゲットコンテナ内のローテータの位置を決定する **[!UICONTROL Sort Order]** 数を入力します。 これは、同じコンテナに割り当てられる可能性のある他のウィジェットに対する相対パスです。

   ![Rotator ストアフロントのプロパティ ](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. _レイアウトオプション_ の下の「**[!UICONTROL Add Layout Update]**」をクリックして、次の操作を実行します。

   - ローテータを表示するページまたはページの種類に **[!UICONTROL Display on]** を設定します。

      - `Categories` - [ アンカー ](../catalog/navigation-layered.md) またはアンカー以外のカテゴリページにローテータを表示します。 オプション：アンカーカテゴリ/アンカー以外のカテゴリ
      - `Products` – 特定のタイプの製品ページ、またはすべての製品ページにロテータを表示します。 オプション：すべての製品タイプ/[ シンプル製品 ](../catalog/product-create-simple.md)/[ バーチャル製品 ](../catalog/product-create-virtual.md)/[ バンドル製品 ](../catalog/product-create-bundle.md)/[ ダウンロード可能製品 ](../catalog/product-create-downloadable.md)/[ ギフトカード ](../catalog/product-gift-card-create.md)/[ 設定可能な製品 ](../catalog/product-create-configurable.md)/[ グループ化された製品 ](../catalog/product-create-grouped.md)
      - `Generic Pages` – すべてのページ、特定のページ、または特定のレイアウトを持つページにのみローテーターを表示します。 オプション：`All Pages`/`Specified Page`/`Page Layouts`

     この例では、ロテータを `Specified Page` に配置します。

   - ロテータを表示する特定の **[!UICONTROL Page]** を選択します。

   - ローテータを表示する [ ページレイアウト ](page-layout.md#standard-page-layouts) の部分に **[!UICONTROL Container]** を設定します。

     他のウィジェットが同じコンテナに割り当てられている場合、並べ替え順に従って順番に表示されます。

   - `Dynamic Block Template` をデフォルトの **[!UICONTROL Template]** として使用します。

     この設定により、回転子を単独で配置するか、既存のテキスト内に配置するかに基づいて、回転子の書式設定に使用するテンプレートが決定されます。

     ![ ローテーターレイアウトの更新 ](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - 「**[!UICONTROL Save and Continue Edit]**」をクリックします。

1. 左側のパネルで「**[!UICONTROL Widget Options]**」を選択します。

1. **[!UICONTROL Dynamic Blocks to Display]** の場合、`Specified Dynamic Blocks` を受け入れます。

   この設定により、ロテータに含まれるダイナミック ブロックのタイプが決まります。

   - `Specified Dynamic Blocks` – 特定のダイナミックブロックのみが含まれます。
   - `Cart Price Rule Related` – 買い物かごの価格ルールに関連付けられた動的ブロックのみを含めます。
   - `Catalog Price Rule Related` - カタログ価格ルールに関連付けられている動的ブロックのみが含まれます。

1. ウィジェットで使用できるを **[!UICONTROL Restrict the Dynamic Block Types]** すには、「`Content Area`」を選択します。

   この設定では、バナーをページレイアウトの特定の部分に制限します。

   - `Content Area` - ページのメインコンテンツ領域に動的ブロックを配置します。
   - `Footer` - ページフッターに動的ブロックを配置します。
   - `Header` - ページヘッダーに動的ブロックを配置します。
   - `Left Column` – 可能な場合は、動的ブロックをページレイアウトの左側の列に配置します。
   - `Right Column` - ダイナミックブロックがページレイアウトの右側の列に配置されます（使用可能な場合）。

1. **[!UICONTROL Rotation Mode]** を次のいずれかに設定します。

   - `Display all instead of rotating` - ダイナミック ブロックのスタックを表示します。ここで、すべてが表示されます。
   - `One at a time, Random` – 指定したダイナミック ブロックをランダムに表示します。 ページを更新すると、別の（ランダムな）ダイナミックブロックが表示されます。
   - `One at the time, Series` – 指定したダイナミック ブロックが追加された順序で表示されます。 ページが更新されると、シーケンス内の次の動的ブロックが表示されます。
   - `One at the time, Shuffle` – 一度に 1 つのダイナミック ブロックを入れ替えて表示します。 このオプションは、同じダイナミック ブロックが繰り返されないことを除いて、`One at a time, Random` のオプションに似ています。

     ![Rotator ウィジェットのオプション ](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Specify Dynamic Blocks]** グリッドで、ロテータに含める各ダイナミック ブロックのチェックボックスをオンにします。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。
