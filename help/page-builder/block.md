---
title: コンテンツを追加 – ブロック
description: 再利用可能なブロックをに追加するために使用されるブロックコンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# コンテンツを追加 – ブロック

の使用 _ブロック_ 既存のアクティブなコンテンツ タイプを追加 [ブロック](../content-design/blocks.md) に [[!DNL Page Builder] ステージ](workspace.md#stage). 次の例では、最初の列にページのサイドメニューを含むブロックが含まれています。 2 番目の列には画像が含まれます。

![サイドメニュー付きブロック](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ブロック ツールボックス

| ツール | アイコン | 説明 |
| --------- | -------- | ------------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png) | ブロックコンテナとその内容をステージ上の別の位置に移動します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png) | 「ブロックの編集」ページが開きます。このページでブロックを選択し、コンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png) | 現在のブロックコンテナとそのコンテンツを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png) | 非表示のブロックコンテナとその内容を表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png) | ブロックコンテナとその内容のコピーを作成します。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png) | ブロックコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 既存のブロックを追加

1. に移動します。 [!DNL Page Builder] ターゲットページ、ブロック、動的ブロック、製品またはカテゴリのワークスペース。

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Add Content]** をドラッグします。 **[!UICONTROL Block]** ステージへのプレースホルダー。

   ![ステージ上へのブロックのドラッグ](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. 空のブロックコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="25"} ） アイコンをクリックします。

1. クリック **[!UICONTROL Select Block]**.

   ![ブロックの選択](./assets/pb-add-content-block-select.png){width="200"}

1. 追加するブロックの行で、をクリックします **[!UICONTROL Select]** 最後の列

   ![選択したブロック](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   選択したブロックの名前がページに表示されます。

   ![ブロック名](./assets/pb-add-content-block-name.png){width="200"}

1. 必要に応じて、このページの最後にあるフィールドの説明を参考にして、残りの設定を完了します。

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

### 詳細設定

1. 親コンテナ内のブロックの位置をコントロールするには、 **[!UICONTROL Alignment]**:

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
   | `Left` | 親コンテナの左罫線に沿ってリストを配置します。指定したパディングはすべて許可されます。 |
   | `Center` | 親コンテナの中央にリストを揃えます。指定したパディングに対する許容値を使用します。 |
   | `Right` | 親コンテナの右端に沿ってブロックを配置します。指定したパディングは許可されます。 |

   {style="table-layout:auto"}

1. を設定 **[!UICONTROL Border]** ブロックコンテナの 4 つの側面すべてに適用されるスタイル：

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

1. 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** ブロックコンテナの外側の余白と内側のパディングを決定する。

   対応する値を図に入力します。

   | コンテナ領域 | 説明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## ブロック設定を編集

1. ブロックコンテナにポインタを合わせて、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="25"} ） アイコンをクリックします。

   ![ブロック ツールボックス](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. 別のブロックを選択するには、 **[!UICONTROL Select Block]**.

   - アクティブなブロックのリストで、 **[!UICONTROL Select]** 追加するブロック。
   - クリック **[!UICONTROL Add Selected]**.

1. 必要に応じて、このページの最後にあるフィールドの説明を参照して、残りの設定を更新します。

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

## ブロックの複製

1. ブロックコンテナにカーソルを合わせてツールボックスを表示し、 _複製_ （![アイコンを複製](./assets/pb-icon-duplicate.png)） アイコンをクリックします。

   複製は、元の画像のすぐ下に表示されます。

1. 新しいブロックを新しい位置に移動するには、コンテナの上にマウスポインターを置いてから、 _移動_ （![移動アイコン](./assets/pb-icon-move.png)）を選択します。

1. 新しい位置に赤いガイドラインが表示されるまで、ブロックを選択してドラッグします。

   各コンテナの上部と下部の境界線は、ブロックを移動すると破線で表示されます。

## ステージからブロックを削除

1. ブロックコンテナにカーソルを合わせてツールボックスを表示し、 _削除_ （![アイコンを削除](./assets/pb-icon-remove.png)） アイコンをクリックします。

1. 確認を求められたら、 **[!UICONTROL OK]**.
