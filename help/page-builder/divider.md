---
title: 要素 — ディバイダ
description: 区切りコンテンツタイプについて説明します。区切りコンテンツタイプは、 [!DNL Page Builder] ステージ。
exl-id: e1052170-6d2f-4893-a78b-a845a8b6c0d9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# 要素 — ディバイダ

以下を使用します。 _分周器_ コンテンツタイプ：内のコンテンツのセクション間に視覚的な区切りとしてルールを追加します。 [[!DNL Page Builder] ステージ](workspace.md#stage). 区切りの線の色、太さ、幅を指定できます。 また、コンテナ境界の整列、余白とパディングの設定、形式も制御できます。 デフォルトでは、ディバイダーはコンテナの幅を広げるヘアラインルールで、パディングの許容値を含みます。

![境界線のないコンテナ内のデフォルトの区切り線](./assets/pb-elements-divider-default.png){width="500" zoomable="yes"}

次の例では、ほとんどのディバイダコンテナは非表示ですが、コンテナを赤い破線で表示し、ディバイダ、パディング、コンテナ間の関係を確認できます。 区切りの上下のパディングを調整して、要素間の間隔を制御できます。

![境界線が破線のコンテナ内のパディングを含むディバイダー](./assets/pb-elements-divider-default-border-dashed.png){width="500" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Divider ツールボックス

| ツール | アイコン | 説明 |
| ---- | --------------------| ------------|
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 区切りコンテナをページ上の別の有効な場所に移動します。 |
| （ラベル） | 分周器 | 現在のコンテナをディバイダ要素として識別します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 「ディバイダを編集」ページが開き、ディバイダとそのコンテナのプロパティを変更できます。 |
| 非表示 | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | ディバイダコンテナを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のディバイダコンテナを表示します。 |
| 複製 | ![複製アイコン](./assets/pb-icon-duplicate.png){width="25"} | ディバイダコンテナのコピーを作成します。 |
| 削除 | ![削除アイコン](./assets/pb-icon-remove.png){width="25"} | ステージからディバイダコンテナとその内容を削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## ディバイダーの追加

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をクリックし、 **[!UICONTROL Divider]** プレースホルダーをステージ上の行、列またはタブセットに追加します。

   ステージ上の別のコンテンツコンテナの前または後にディバイダを配置する際は、赤いガイドラインを参照用に使用します。

   ![ステージへのディバイダーのドラッグ](./assets/pb-elements-divider-drag.png){width="600" zoomable="yes"}

   次の例では、区切りはテキストの新しいセクションの先頭を示します。

   ![テキストのセクションを区切る区切り](./assets/pb-elements-dividers-multiple-text-row.png){width="500" zoomable="yes"}

1. 新しいディバイダの設定を指定するには、次の手順に従います。

## ディバイダ設定の変更

1. ディバイダコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![Divider ツールボックス](./assets/pb-elements-divider-toolbox.png){width="500" zoomable="yes"}

1. ディバイダを変更する **[!UICONTROL Line Color]** 次のいずれかの方法を使用します。

   - 有効な [HTMLの色名][1]. 例： `Teal`.
   - 16 進数の色の値を入力します。 例： `#008080`.

   完了したら、「 **[!UICONTROL Apply]**.

   ![線の色の設定](./assets/pb-elements-divider-settings-line-color.png){width="600" zoomable="yes"}

1. 次を入力します。 **[!UICONTROL Line Thickness]** ピクセル単位で指定します。

1. 測定単位を指定するには、 **[!UICONTROL Line Width]** その後に `px` または `%`.

   ![線の色、太さ、幅の設定](./assets/pb-elements-divider-settings-line-color-thickness-width.png){width="600" zoomable="yes"}

1. を更新します。 _[!UICONTROL Advanced]_必要に応じて設定します。

   - 親コンテナ内でのディバイダの位置を制御するには、 **[!UICONTROL Alignment]**:

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイルシートで指定された位置揃えの既定の設定を適用します。 |
     | `Left` | リストを親コンテナの左側の境界線に沿って揃えます。指定されたパディングの値を使用します。 |
     | `Center` | 指定されたパディングを許容して、親コンテナの中央にリストを揃えます。 |
     | `Right` | 指定されたパディングの値を使用して、親コンテナの右側の境界線に沿ってブロックを揃えます。 |

     {style="table-layout:auto"}

     次の例では、区切りの中央の位置を使用するようにオプションが設定されています。

     ![中央揃えのディバイダ](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - を設定します。 **[!UICONTROL Border]** 区切りコンテナの 4 つの側面すべてに適用されるスタイル：

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

   - 次の値をピクセル単位で入力します。 **[!UICONTROL Margins and Padding]** ディバイダコンテナの外側の余白と内側の余白を決定する。

     ダイアグラムに対応する値を入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完了したら、「 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。

   ![行を中央に配置したディバイダ](./assets/pb-elements-divider-settings-2px-centered.png){width="500" zoomable="yes"}

## ディバイダを複製する

特定の設定で書式設定されたディバイダの場合、新しいプレースホルダで始め直すよりも、複製を作成する方が効率的です。

1. ディバイダコンテナの上にマウスポインターを置いてツールボックスを表示し、 _複製_ ( ![複製アイコン](./assets/pb-icon-duplicate.png){width="20"} ) アイコンをクリックします。

   重複したディバイダコンテナは、元のコンテナのすぐ下に表示されます。

   ![重複したディバイダ](./assets/pb-elements-divider-duplicate.png){width="500" zoomable="yes"}

1. 新しいディバイダコンテナの上にマウスポインターを置いてツールボックスを表示し、 _移動_ ( ![移動アイコン](./assets/pb-icon-move.png){width="20"} ) アイコンをクリックします。

   ![ディバイダの移動](./assets/pb-elements-divider-move.png){width="500" zoomable="yes"}

1. 赤いガイドラインが新しい位置を示すまで、ディバイダを選択してドラッグします。

   各コンテナの上と下の境界線は、ディバイダを移動すると破線で表示されます。

   ![複製したディバイダを位置に移動する](./assets/pb-elements-divider-move-guideline.png){width="500" zoomable="yes"}

[1]: https://en.wikipedia.org/wiki/Web_colors
