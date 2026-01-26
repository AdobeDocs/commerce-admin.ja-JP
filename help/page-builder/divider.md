---
title: 要素 – 区切り線
description: ステージ内のコンテンツのセクション間の視覚的な区切りとしてルールを追加するために使用される、ディバイダー  [!DNL Page Builder]  コンテンツタイプについて説明します。
exl-id: e1052170-6d2f-4893-a78b-a845a8b6c0d9
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# 要素 – 区切り線

_ディバイダー_ コンテンツタイプを使用して、[[!DNL Page Builder]  ステージ &#x200B;](workspace.md#stage) 内のコンテンツのセクション間の視覚的な区切りとしてルールを追加します。 分割線の色、太さ、幅を指定できます。 また、整列の制御、余白とパディングの設定、コンテナの境界線の形式の設定を行うこともできます。 デフォルトでは、区切りはコンテナの全幅を拡張するヘアーラインルールで、パディングに余裕があります。

![&#x200B; 境界線のないコンテナ内のデフォルトの区切り文字 &#x200B;](./assets/pb-elements-divider-default.png){width="500" zoomable="yes"}

ほとんどのディバイダーコンテナは非表示ですが、次の例では、コンテナを赤い破線で囲み、ディバイダー、パディング、コンテナの関係を確認できます。 区切り線の上下のパディングを調整して、要素間の間隔を制御できます。

![&#x200B; コンテナ内のパディングを破線の境界線で区切る &#x200B;](./assets/pb-elements-divider-default-border-dashed.png){width="500" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ディバイダーツールボックス

| ツール | アイコン | 説明 |
| ---- | --------------------| ------------|
| 移動 | ![&#x200B; 移動アイコン &#x200B;](./assets/pb-icon-move.png){width="25"} | ディバイダーコンテナをページ上の別の有効な場所に移動します。 |
| （ラベル） | デバイダ | 現在のコンテナを分割要素として識別します。 |
| 設定 | ![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="25"} | ディバイダーを編集ページが開きます。このページで、ディバイダーとそのコンテナのプロパティを変更できます。 |
| Hide | ![&#x200B; アイコンを非表示 &#x200B;](./assets/pb-icon-hide.png){width="25"} | ディバイダーコンテナを非表示にします。 |
| 表示 | ![&#x200B; アイコンを表示 &#x200B;](./assets/pb-icon-show.png){width="25"} | 非表示のディバイダーコンテナを表示します。 |
| 複製 | ![&#x200B; 複製アイコン &#x200B;](./assets/pb-icon-duplicate.png){width="25"} | ディバイダーコンテナをコピーします。 |
| 削除 | ![&#x200B; 削除アイコン &#x200B;](./assets/pb-icon-remove.png){width="25"} | ディバイダーコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## ディバイダーの追加

1. [!DNL Page Builder] パネルで **[!UICONTROL Elements]** を展開し、**[!UICONTROL Divider]** プレースホルダーをステージ上の行、列またはタブセットにドラッグします。

   赤いガイドラインを参考にして、ステージ上の別のコンテンツコンテナの前または後にディバイダーを配置します。

   ![&#x200B; ディバイダーのステージへのドラッグ &#x200B;](./assets/pb-elements-divider-drag.png){width="600" zoomable="yes"}

   次の使用例では、区切り記号を使用して文字列の新しいセクションの先頭を指定します。

   ![&#x200B; テキストのセクションを区切る区切り記号 &#x200B;](./assets/pb-elements-dividers-multiple-text-row.png){width="500" zoomable="yes"}

1. 新しいディバイダーの設定を指定するには、次の手順に従います。

## ディバイダー設定の変更

1. ディバイダーコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![&#x200B; ディバイダーツールボックス &#x200B;](./assets/pb-elements-divider-toolbox.png){width="500" zoomable="yes"}

1. 次のいずれかの方法を使用して、ディバイダー **[!UICONTROL Line Color]** を変更します。

   - 有効な [HTML カラー名 &#x200B;](https://en.wikipedia.org/wiki/Web_colors) を入力してください。 例：`Teal`。
   - 16 進数のカラー値を入力します。 例：`#008080`。

   完了したら、「**[!UICONTROL Apply]**」をクリックします。

   ![&#x200B; 線の色の設定 &#x200B;](./assets/pb-elements-divider-settings-line-color.png){width="600" zoomable="yes"}

1. **[!UICONTROL Line Thickness]** をピクセル単位で入力します。

1. 測定単位を指定するには、**[!UICONTROL Line Width]** に続いて `px` または `%` を入力します。

   ![&#x200B; 線の色、太さ、幅の設定 &#x200B;](./assets/pb-elements-divider-settings-line-color-thickness-width.png){width="600" zoomable="yes"}

1. 必要に応じて、_[!UICONTROL Advanced]_&#x200B;設定を更新します。

   - 親コンテナ内のディバイダーの位置を制御するには、**[!UICONTROL Alignment]** のオプションを選択します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | 親コンテナの左罫線に沿ってリストを配置します。指定したパディングはすべて許可されます。 |
     | `Center` | 親コンテナの中央にリストを揃えます。指定したパディングに対する許容値を使用します。 |
     | `Right` | 親コンテナの右端に沿ってブロックを配置します。指定したパディングは許可されます。 |

     {style="table-layout:auto"}

     次の例では、ディバイダーに中央揃えを使用するようにオプションを設定しています。

     ![&#x200B; 中央揃えのデバイダー &#x200B;](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - ディバイダーコンテナの 4 つの辺すべてに適用する **[!UICONTROL Border]** スタイルを設定します。

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

   - `None` 以外の境界線のスタイルを設定する場合は、境界線の表示オプションを完了します。

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション）コンテナに適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

     複数のクラス名はスペースで区切ります。

   - ディバイダーコンテナの外側の余白と内側のパディングを決定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

     対応する値を図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション：`Top`/`Right`/`Bottom`/`Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション：`Top`/`Right`/`Bottom`/`Left` |

     {style="table-layout:auto"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

   ![&#x200B; 行内で中央に配置されるディバイダー &#x200B;](./assets/pb-elements-divider-settings-2px-centered.png){width="500" zoomable="yes"}

## ディバイダーの複製

特定の設定を持つフォーマットされたディバイダーの場合は、新しいプレースホルダーでやり直すよりも、複製を作成する方が効率的です。

1. ディバイダーコンテナにカーソルを合わせてツールボックスを表示し、「_複製_」（![&#x200B; 複製アイコン &#x200B;](./assets/pb-icon-duplicate.png){width="20"}）アイコンを選択します。

   重複したディバイダーコンテナは、オリジナルのすぐ下に表示されます。

   ![&#x200B; 重複除算器 &#x200B;](./assets/pb-elements-divider-duplicate.png){width="500" zoomable="yes"}

1. 新しいディバイダーコンテナにカーソルを合わせてツールボックスを表示し、_移動_ （![&#x200B; 移動アイコン &#x200B;](./assets/pb-icon-move.png){width="20"}）アイコンを選択します。

   ![&#x200B; 分周器の移動 &#x200B;](./assets/pb-elements-divider-move.png){width="500" zoomable="yes"}

1. ディバイダーを選択してドラッグし、赤いガイドラインが新しい位置を示すようにします。

   分割線を移動すると、各コンテナの上下の境界が破線で表示されます。

   ![&#x200B; 複製したデバイダーの位置への移動 &#x200B;](./assets/pb-elements-divider-move-guideline.png){width="500" zoomable="yes"}


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
