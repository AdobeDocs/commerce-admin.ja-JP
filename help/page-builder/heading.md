---
title: 要素 – 見出し
description: 見出しレベルが H1 から H6 のテキストコンテナをに追加するために使用する見出しコンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# 要素 – 見出し

見出しレベルは、コンテンツを整理し、検索エンジンが各ページのインデックスを作成するのに役立つ階層を確立します。 の使用 _見出し_ 内のコンテンツタイプ [[!DNL Page Builder] ステージ](workspace.md#stage) 見出しレベルが H1 から H6 のテキストコンテナをステージに追加する。 見出しは、現在のテーマに関連付けられているスタイルシートに従って書式設定されます。

この [コンテンツの見出し](workspace.md) のフィールド _[!UICONTROL Content]_セクションを使用すると、ページの上部に H1 見出しを追加できます。 ただし、このフィールドは以前の [!DNL Commerce] およびのバージョンは、古いコンテンツをサポートするために提供されています。 このフィールドは次の利点を生かしません [!DNL Page Builder]の高度な機能。 「コンテンツ見出し」フィールドを空白のままにして、を使用することをお勧めします [!DNL Page Builder] 見出しコンテンツタイプ：任意のレベルの見出しをページに追加します。

次の例では、Luma テーマでフォーマットされている場合に、コンテンツの見出しと見出しのコンテンツタイプがどのように表示されるかを示しています。

![ストアフロントのコンテンツの見出しと見出しレベル](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

から見出しをドラッグできます _要素_ の節 [!DNL Page Builder] ステージ上の行、列またはタブセットにパネルします。 見出しのレベルと配置は、ステージ上のエディターツールバーから、または _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） コントロールします。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 見出しエディター

![ツールバー付き見出しエディター](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## 見出しコンテナツールボックス

すべてのコンテンツコンテナと同様に、コンテナにカーソルを合わせると、ツールボックスが表示されます。

![見出しコンテナツールボックス](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ----------------- | ---------------------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 見出しコンテナをページ上の別の有効な場所に移動します。 |
| （ラベル） | 見出し | 現在のコンテナを見出しとして識別します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 見出しを編集ページを開きます。このページで、コンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 見出しコンテナを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示の見出しコンテナを表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | 見出しコンテナをコピーします。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | 見出しコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 見出しの追加

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をドラッグします。 **[!UICONTROL Heading]** ステージ上の行、列またはタブセットへのプレースホルダー。

   ![見出しをステージにドラッグ](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. エディターで、見出しのテキストを `Edit Heading Text` プレースホルダー。

   既定では、見出しテキストにはレベル 2 （H2）の見出しタイプが割り当てられます。

   ![見出しエディターのプレースホルダー](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. ツールバーで、H1 から H6 までの適切な見出しタイプを選択します。

1. 必要に応じて、配置を変更します。

## ヘッダー設定の編集

1. 見出しコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![見出しツールボックス](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. 見出しコンテンツを更新（**[!UICONTROL Heading Type]** および **[!UICONTROL Heading Text]**&#x200B;必要に応じて）を使用します。

   このコンテンツは、見出しエディターで更新することもできます。

1. を更新 _[!UICONTROL Advanced]_必要に応じて設定します。

   - 親コンテナ内の見出しの位置を制御するには、 **[!UICONTROL Alignment]**:

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | 親コンテナの左罫線に沿ってリストを配置します。指定したパディングはすべて許可されます。 |
     | `Center` | 親コンテナの中央にリストを揃えます。指定したパディングに対する許容値を使用します。 |
     | `Right` | 親コンテナの右端に沿ってブロックを配置します。指定したパディングは許可されます。 |

     {style="table-layout:auto"}

   - を **[!UICONTROL Border]** 見出しコンテナの 4 つの辺すべてに適用されるスタイル：

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

   - 境界線のスタイルを `None`の場合は、次のボーダー表示オプションを入力します。

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション）の名前を指定します **[!UICONTROL CSS classes]** を現在のスタイルシートから取得して、コンテナに適用します。

     複数のクラス名はスペースで区切ります。

   - 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** 見出しコンテナの外側の余白と内側のパディングを決定します。

     対応する値を図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

## 見出しの複製

特定の設定を持つ書式設定された見出しの場合は、新しいプレースホルダーでやり直すよりも、見出しを複製する方が効率的です。

1. 見出しコンテナにカーソルを合わせてツールボックスを表示し、 _複製_ （ ![アイコンを複製](./assets/pb-icon-duplicate.png){width="20"} ） アイコンをクリックします。

   複製は、元の画像のすぐ下に表示されます。

   ![見出しコンテナの複製](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. 新しい見出しコンテナにポインタを合わせてツールボックスを表示し、 _移動_ （ ![移動アイコン](./assets/pb-icon-move.png){width="20"} ） アイコンをクリックします。

   ![見出しの移動](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. 見出しを選択してドラッグし、赤いガイドラインが新しい位置を示すようにします。

   見出しを移動すると、各コンテナの上部と下部の境界線が破線で表示されます。

   ![複製した見出しの位置への移動](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. 見出しレベルを変更する場合は、見出しテキストをクリックし、エディターツールバーで新しいレベルを選択します。

   ![新しい見出しレベルの選択](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}
