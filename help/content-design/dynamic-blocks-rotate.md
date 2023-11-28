---
title: 回転ダイナミックブロックを追加する
description: 複数のダイナミックブロックをローテーターに追加して、ストアフロントにインタラクティブコンテンツのスライドショーを表示します。
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# 回転ダイナミックブロックを追加する

{{ee-feature}}

インタラクティブコンテンツのスライドショーを表示するには、複数の [動的ブロック](dynamic-blocks.md) 回転体に対して。 The [widget](widgets.md) ツールは、ローテーターを単一のページ上の特定の場所、またはストア全体の複数のページに配置するために使用します。

![ダイナミックブロックローテーター](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## 手順 1：個々のダイナミックブロックを作成する

宛先 [ダイナミックブロックの作成](dynamic-blocks.md) ローテーターに配置する手順は、次のとおりです。

## 手順 2：ダイナミックブロックローテーターウィジェットを追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅で、 **[!UICONTROL Add Widget]**.

1. の下 _設定_，設定 **[!UICONTROL Type]** から `Dynamic Blocks Rotator`.

1. 現在の **[!UICONTROL Design Theme]** ストアの。

   この設定は、現在のパッケージを識別します。 [テーマ](themes.md) ストアのページレイアウトを決定します。

1. クリック **[!UICONTROL Continue]**.

   ![ダイナミックブロックローテーターの設定](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## 手順 3：オプションを設定します。

1. の下 _ストアフロントのプロパティ_、次のオプションを設定します。

   - を入力します。 **[!UICONTROL Title]** 回転体に対して。

   - Adobe Analytics の **[!UICONTROL Assign to Store Views]** リストで、 [ストア表示](../getting-started/websites-stores-views.md) 回転体が使用可能な場所。

   - （オプション） **[!UICONTROL Sort Order]** ターゲットコンテナ内でのローテーターの位置を決定する数値。 同じコンテナに割り当てられている可能性のある他のウィジェットとの相対位置です。

   ![Rotator ストアフロントのプロパティ](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. の下 _レイアウトオプション_&#x200B;をクリックし、 **[!UICONTROL Add Layout Update]** 次の操作を実行します。

   - 設定 **[!UICONTROL Display on]** ローテーターを表示するページまたはページのタイプに追加します。

      - `Categories`  — 回転子を次のいずれかに表示します。 [アンカー](../catalog/navigation-layered.md) アンカーのないカテゴリページのいずれかです。 オプション：アンカーのカテゴリ/アンカーなしのカテゴリ
      - `Products`  — 特定のタイプの製品ページまたはすべての製品ページのローテーターを表示します。 オプション：すべての製品タイプ/ [シンプルな製品](../catalog/product-create-simple.md) /  [仮想製品](../catalog/product-create-virtual.md) / [バンドル製品](../catalog/product-create-bundle.md) / [ダウンロード可能な製品](../catalog/product-create-downloadable.md) / [ギフトカード](../catalog/product-gift-card-create.md) / [設定可能な製品](../catalog/product-create-configurable.md) / [グループ化された製品](../catalog/product-create-grouped.md)
      - `Generic Pages`  — すべてのページ、特定のページ、または特定のレイアウトを持つページでのみローテーターを表示します。 オプション： `All Pages` / `Specified Page` / `Page Layouts`

     この例では、回転子は `Specified Page`.

   - 特定の **[!UICONTROL Page]** 回転体が現れる場所。

   - 設定 **[!UICONTROL Container]** の一部に [ページレイアウト](page-layout.md#standard-page-layouts) 回転体が現れる場所。

     他のウィジェットが同じコンテナに割り当てられている場合は、並べ替え順に従って順番に表示されます。

   - 確定 `Dynamic Block Template` をデフォルトとして **[!UICONTROL Template]**.

     この設定は、ローテーターを単独で使用するか、既存のテキスト内に配置するかに基づいて、ローテーターのフォーマットに使用するテンプレートを決定します。

     ![ローテーターレイアウトの更新](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - クリック **[!UICONTROL Save and Continue Edit]**.

1. 左側のパネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. の **[!UICONTROL Dynamic Blocks to Display]**, accept `Specified Dynamic Blocks`.

   この設定は、回転子に含まれるダイナミックブロックの種類を決定します。

   - `Specified Dynamic Blocks`  — 特定の動的ブロックのみが含まれます。
   - `Cart Price Rule Related`  — 買い物かごの価格ルールに関連付けられている動的ブロックのみが含まれます。
   - `Catalog Price Rule Related`  — カタログ価格ルールに関連付けられている動的ブロックのみが含まれます。

1. 宛先 **[!UICONTROL Restrict the Dynamic Block Types]** ウィジェットで使用できるものを選択し、 `Content Area`.

   この設定は、バナーをページレイアウトの特定の部分に限定します。

   - `Content Area`  — 動的ブロックをページのメインコンテンツ領域に配置します。
   - `Footer`  — ページフッターにダイナミックブロックを配置します。
   - `Header`  — 動的ブロックをページヘッダーに配置します。
   - `Left Column`  — 動的ブロックをページレイアウトの左列に配置します（可能な場合）。
   - `Right Column`  — 動的ブロックをページレイアウトの右列に配置します（可能な場合）。

1. 設定 **[!UICONTROL Rotation Mode]** を次のいずれかに変更します。

   - `Display all instead of rotating`  — すべての動的ブロックが表示される、動的ブロックのスタックを表示します。
   - `One at a time, Random`  — 指定したダイナミックブロックをランダムな順序で表示します。 ページが更新されると、別の（ランダムな）動的ブロックが表示されます。
   - `One at the time, Series`  — 追加されたシーケンス内の指定された動的ブロックを表示します。 ページが更新されると、シーケンス内の次の動的ブロックが表示されます。
   - `One at the time, Shuffle`  — 一度に 1 つのダイナミックブロックをシャッフル順に表示します。 このオプションは、 `One at a time, Random` 」オプションを使用します。ただし、同じダイナミックブロックは繰り返されません。

     ![ローテーターウィジェットオプション](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Specify Dynamic Blocks]** グリッドで、ローテーターに含める各ダイナミックブロックのチェックボックスをオンにします。

1. 完了したら、「 **[!UICONTROL Save]**.
