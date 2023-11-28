---
title: エレメント — 見出し
description: H1 から H6 までの見出しレベルを持つテキストコンテナを [!DNL Page Builder] ステージ。
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# エレメント — 見出し

見出しレベルは、コンテンツを整理し、検索エンジンが各ページのインデックスを作成するのに役立つ階層を確立します。 以下を使用します。 _見出し_ コンテンツタイプ [[!DNL Page Builder] ステージ](workspace.md#stage) を使用して、見出しレベルが H1 から H6 のテキストコンテナをステージに追加します。 見出しは、現在のテーマに関連付けられているスタイルシートに従って書式設定されます。

The [コンテンツ見出し](workspace.md) フィールド _[!UICONTROL Content]_セクションを使用して、ページの上部に H1 見出しを追加できます。 ただし、このフィールドは以前の [!DNL Commerce] 古いコンテンツをサポートするためのバージョンおよびが提供されています。 このフィールドでは [!DNL Page Builder]の高度な機能。 「コンテンツの見出し」フィールドは空白のままにし、 [!DNL Page Builder] 見出しコンテンツタイプ：任意のレベルの見出しをページに追加します。

次の例では、Luma テーマで書式設定した場合に、「コンテンツの見出し」と「見出し」コンテンツタイプがどのように表示されるかを示します。

![ストアフロントのコンテンツ見出しと見出しレベル](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

見出しは、 _要素_ のセクション [!DNL Page Builder] パネルをステージ上の行、列またはタブセットにドラッグします。 見出しのレベルと整列は、ステージ上のエディターツールバーから、または _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) コントロールを使用します。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 見出しエディター

![ツールバー付きの見出しエディター](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## 見出しコンテナツールボックス

すべてのコンテンツコンテナと同様に、コンテナの上にマウスポインターを置くとツールボックスが表示されます。

![見出しコンテナツールボックス](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ----------------- | ---------------------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 見出しコンテナをページ上の別の有効な場所に移動します。 |
| （ラベル） | 見出し | 現在のコンテナを見出しとして識別します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 「見出しを編集」ページが開き、コンテナのプロパティを変更できます。 |
| 非表示 | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 見出しコンテナを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示の見出しコンテナを表示します。 |
| 複製 | ![複製アイコン](./assets/pb-icon-duplicate.png){width="25"} | 見出しコンテナのコピーを作成します。 |
| 削除 | ![削除アイコン](./assets/pb-icon-remove.png){width="25"} | ステージから見出しコンテナとその内容を削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 見出しを追加

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をクリックし、 **[!UICONTROL Heading]** プレースホルダーをステージ上の行、列またはタブセットに追加します。

   ![見出しのステージへのドラッグ](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. エディターで、 `Edit Heading Text` プレースホルダー。

   デフォルトでは、見出しテキストにはレベル 2(H2) の見出しタイプが割り当てられます。

   ![見出しエディター内のプレースホルダー](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. ツールバーで、H1 と H6 の間の適切な見出しタイプを選択します。

1. 必要に応じて、位置揃えを変更します。

## ヘッダー設定を編集

1. 見出しコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![見出しツールボックス](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. 見出しのコンテンツ (**[!UICONTROL Heading Type]** および **[!UICONTROL Heading Text]**) をクリックします。

   見出しエディターでこのコンテンツを更新することもできます。

1. を更新します。 _[!UICONTROL Advanced]_必要に応じて設定します。

   - 親コンテナ内での見出しの位置を制御するには、 **[!UICONTROL Alignment]**:

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイルシートで指定された位置揃えの既定の設定を適用します。 |
     | `Left` | リストを親コンテナの左側の境界線に沿って揃えます。指定されたパディングの値を使用します。 |
     | `Center` | 指定されたパディングを許容して、親コンテナの中央にリストを揃えます。 |
     | `Right` | 指定されたパディングの値を使用して、親コンテナの右側の境界線に沿ってブロックを揃えます。 |

     {style="table-layout:auto"}

   - を設定します。 **[!UICONTROL Border]** スタイルを見出しコンテナの 4 つの側面すべてに適用します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 関連するスタイルシートで指定された既定の罫線のスタイルを適用します。 |
     | `None` | コンテナの境界線を表示しません。 |
     | `Dotted` | コンテナの境界線は点線で表示されます。 |
     | `Dashed` | コンテナの境界線は破線で表示されます。 |
     | `Solid` | コンテナの境界線は実線で表示されます。 |
     | `Double` | コンテナの境界線は二重線で表示されます。 |
     | `Groove` | コンテナ境界は溝付きの線として表示されます。 |
     | `Ridge` | コンテナの境界線は、稜線として表示されます。 |
     | `Inset` | コンテナの境界線は、挿入線として表示されます。 |
     | `Outset` | コンテナの境界線は、アウトセット行として表示されます。 |

     {style="table-layout:auto"}

   - 次の条件を満たさない境界線のスタイルを設定した場合： `None`、境界線の表示オプションを設定します。

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各隅を囲むために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション） **[!UICONTROL CSS classes]** 現在のスタイルシートからコンテナに適用します。

     複数のクラス名はスペースで区切ります。

   - 次の値をピクセル単位で入力します。 **[!UICONTROL Margins and Padding]** を使用して、見出しコンテナの外側の余白と内側の余白を指定します。

     ダイアグラムに対応する値を入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完了したら、「 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。

## 見出しを複製

特定の設定で書式設定された見出しの場合、新しいプレースホルダーで始め直すよりも、見出しを複製する方が効率的です。

1. 見出しコンテナの上にマウスポインターを置いてツールボックスを表示し、 _複製_ ( ![複製アイコン](./assets/pb-icon-duplicate.png){width="20"} ) アイコンをクリックします。

   複製は元の画像のすぐ下に表示されます。

   ![見出しコンテナの複製](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. 新しい見出しコンテナの上にマウスポインターを置いてツールボックスを表示し、 _移動_ ( ![移動アイコン](./assets/pb-icon-move.png){width="20"} ) アイコンをクリックします。

   ![見出しの移動](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. 見出しを選択し、赤いガイドラインが新しい位置を示すまでドラッグします。

   各コンテナの上と下の境界線は、見出しを移動する際に破線で表示されます。

   ![複製した見出しを位置に移動](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. 見出しレベルを変更する場合は、見出しテキストをクリックし、エディターツールバーで新しいレベルを選択します。

   ![新しい見出しレベルの選択](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}
