---
title: コンテンツを追加 – 動的ブロック
description: 再利用可能な動的ブロックをに追加するために使用される、動的ブロックのコンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: 04c90f47-9e32-4d34-ac0d-a2f2cec95ffc
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# コンテンツを追加 – 動的ブロック

動的ブロック コンテンツタイプを使用して、既存のを追加します [動的ブロック](../content-design/dynamic-blocks.md) に [[!DNL Page Builder] ステージ](workspace.md#stage).

![ストアフロントの動的ブロック](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ダイナミック ブロック ツールボックス

| ツール | アイコン | 説明 |
| --------- | ------------- | ----------------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | ブロックコンテナとその内容をステージ上の別の位置に移動します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | を開きます _ブロックを編集_ このページで、ブロックを選択し、コンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在のブロックコンテナとそのコンテンツを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のブロックコンテナとその内容を表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | ブロックコンテナとその内容のコピーを作成します。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | ブロックコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## ステージに既存のダイナミックブロックを追加

1. に移動します。 [!DNL Page Builder] ターゲットページ、ブロック、製品またはカテゴリのワークスペース。

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Add Content]** をドラッグします。 **[!UICONTROL Dynamic Block]** ステージへのプレースホルダー。

   ![動的ブロックプレースホルダーのステージへのドラッグ](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. 空のダイナミックブロックコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![ダイナミック ブロック ツールボックス](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. 日 _ダイナミック ブロックを編集_ ページ、クリック **[!UICONTROL Select Dynamic Block]** リストを使用して、ブロックを選択します。

   ![ダイナミック ブロックを選択する](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

   リストで、挿入するダイナミック ブロックを探し、をクリックします **[!UICONTROL Select]**. 次に、 **[!UICONTROL Add Selected]**.

   ![リストでダイナミック ブロックを選択する](./assets/pb-add-content-dynamic-block-select-list.png){width="600" zoomable="yes"}

   ダイナミック ブロック情報の概要が下に表示されます。

   ![動的ブロックの概要](./assets/pb-add-content-dynamic-block-summary.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Template]** を次のいずれかに変更します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Dynamic Block Block Template` | スタンドアロン ブロックを追加します。 |
   | `Dynamic Block Inline Template` | ブロックの内容をテキストに挿入します。 |

   {style="table-layout:auto"}

   ![ダイナミック ブロック テンプレート](./assets/pb-add-content-dynamic-block-template.png){width="200"}

1. 必要に応じて、詳細設定を完了します。

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

### 詳細設定

1. 親コンテナ内のダイナミック ブロックの位置をコントロールするには、 **[!UICONTROL Alignment]**:

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
   | `Left` | 親コンテナの左罫線に沿ってリストを配置します。指定したパディングはすべて許可されます。 |
   | `Center` | 親コンテナの中央にリストを揃えます。指定したパディングに対する許容値を使用します。 |
   | `Right` | 親コンテナの右端に沿ってブロックを配置します。指定したパディングは許可されます。 |

   {style="table-layout:auto"}

1. を **[!UICONTROL Border]** ダイナミック ブロック コンテナの 4 つの側面すべてに適用されるスタイル：

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 関連付けられたスタイル シートで指定されている既定の罫線スタイルを適用します。 |
   | `None` | コンテナの境界線の表示はしません。 |
   | `Dotted` | コンテナの境界線は点線で表示されます。 |
   | `Dashed` | コンテナの境界線は破線で表示されます。 |
   | `Solid` | コンテナの境界線は実線で表示されます。 |
   | `Double` | コンテナの境界線は二重線で表示されます。 |
   | `Groove` | コンテナの境界線は溝付き線で表示されます。 |
   | `Ridge` | コンテナの境界線は、境界線として表示されます。 |
   | `Inset` | コンテナの境界線は、インセットされた線として表示されます。 |
   | `Outset` | コンテナの境界線は、先頭行として表示されます。 |

   {style="table-layout:auto"}

1. 境界線のスタイルを `None`の場合は、次のボーダー表示オプションを入力します。

   | オプション | 説明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
   | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
   | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

   {style="table-layout:auto"}

1. （オプション）の名前を指定します **[!UICONTROL CSS classes]** を現在のスタイルシートから取得して、コンテナに適用します。

   複数のクラス名はスペースで区切ります。

1. 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** ダイナミックブロックコンテナの外側の余白と内側のパディングを決定する。

   対応する値を図に入力します。

   | コンテナ領域 | 説明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## ダイナミック ブロック コンテナ設定を編集

1. 動的ブロックコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![ダイナミック ブロック ツールボックス](./assets/pb-add-content-dynamic-block-toolbox.png){width="500" zoomable="yes"}

1. 必要に応じて、次のようにダイナミック ブロックを変更します。

   - クリック **[!UICONTROL Select Dynamic Block]**.

     ![別のダイナミック ブロックを選択する](./assets/pb-add-content-dynamic-block-select.png){width="20"}

   - アクティブなダイナミック ブロックのリストで、 **[!UICONTROL Select]** 追加するブロック用。

1. 必要に応じて、残りの設定を更新します。

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

## ダイナミック ブロックを複製する

1. 動的ブロックコンテナにカーソルを合わせてツールボックスを表示し、 _複製_ （ ![アイコンを複製](./assets/pb-icon-duplicate.png){width="20"} ） アイコンをクリックします。

   複製は、元の画像のすぐ下に表示されます。

   ![ダイナミック ブロックを複製する](./assets/pb-add-content-dynamic-block-duplicate.png){width="500" zoomable="yes"}

1. 新しい動的ブロックを別の位置に移動するには、そのコンテナにカーソルを合わせて選択します。 _移動_ （ ![移動アイコン](./assets/pb-icon-move.png){width="20"} ）を選択します。

1. ダイナミック ブロックを選択し、新しい位置に赤いガイドラインが表示されるまでドラッグします。

   ダイナミック ブロックを移動すると、各コンテナの上部と下部の境界が破線で表示されます。

## ステージからダイナミックブロックを削除

1. 動的ブロックコンテナにカーソルを合わせてツールボックスを表示し、 _削除_ （ ![アイコンを削除](./assets/pb-icon-remove.png){width="20"} ） アイコンをクリックします。

1. 確認を求められたら、 **[!UICONTROL OK]**.
