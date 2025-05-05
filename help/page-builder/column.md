---
title: レイアウト – 列
description: ステージ内でページを複数の列に分割するために使用される、列コンテンツタ  [!DNL Page Builder]  プについて説明します。
exl-id: 9701e1b5-3584-4602-9512-051567274f21
feature: Page Builder, Page Content
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '1574'
ht-degree: 0%

---

# レイアウト – 列

_ステージ_ でページを複数の列に分割するには、[[!DNL Page Builder]  列 ](workspace.md#stage) コンテンツタイプを使用します。 列を行、タブ、またはステージに直接追加すると、列グループは最初は同じ幅の 2 つの列に分割されます。 必要に応じて、列を追加または削除できます。 列のサイズを変更するには、2 つの列の間の境界線をドラッグします。 次の列の幅は、行、タブ、ステージ内の使用可能なスペースを埋めるように調整されます。 単一の列は、ステージまたはそのコンテナの全幅を拡張します。

![ 列の追加 ](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 2.4.5 リリースのアップデート

ページビルダーの機能が 2.4.5 リリースで更新され、ユーザーが個々の列の親コンテナとして _[!DNL Columns]_&#x200B;を使用できるようになりました。 この新しいコンテナでは、背景のプロパティもサポートされるようになり、列を一列に折り返す必要がなくなります。 これにより、不要なマークアップを減らし、ストアフロントの表示とエクスペリエンスをより詳細に制御できます。

グループ内の他の列の上または下に列をドラッグして積み重ねることで、[!DNL Columns] コンテナのレイアウトを変更できます。 これにより、開発者がカスタマイズする必要なしに達成できる、新しいさまざまなレイアウトの組み合わせが可能になります。

[!DNL Columns] コンテナを使用してページレイアウトを調整する方法のデモについては、このビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/345828?quality=12&learn=on)

## 列ツールボックス

各列には、コンテナの上にマウスポインターを置くと表示されるオプションのツールボックスがあります。

| ツール | アイコン | 説明 |
|--- |--- |--- |
| 移動 | ![ 移動アイコン ](./assets/pb-icon-move.png){width="25"} | 列とその内容を、他の列と相対的に別の位置に移動します。 |
| （ラベル） | 列 | 現在のコンテナを列として識別します。 列コンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![ 設定アイコン ](./assets/pb-icon-settings.png){width="25"} | 列を編集ページを開きます。このページで、コンテナのプロパティを変更できます。 |
| 複製 | ![ 複製アイコン ](./assets/pb-icon-duplicate.png){width="25"} | 現在の列をコピーします。 |
| 削除 | ![ 削除アイコン ](./assets/pb-icon-remove.png){width="25"} | 現在の列とその内容を削除します。 |

{style="table-layout:auto"}

## 柱通芯

[ グリッド ](workspace.md) を使用すると、コンテンツが一貫して列に配置され、デスクトップとモバイルデバイスの両方でページが正しくレンダリングされるようになります。 詳しくは、[!DNL Page Builder] 設定の [ 詳細なコンテンツツール ](setup.md) の節を参照してください。

![1 つの列を持つ行のグリッド分割 ](./assets/pb-layout-column-one-grid.png){width="500" zoomable="yes"}

次の 2 列の例では、各列コンテナの上部のボーダーの括弧内の数値（6/12）は、各列のグリッド分割数と分割総数を示しています。 この場合、柱は、合計 12 のうち 6 つのグリッド単位の幅です。

![2 列の行のグリッド分割 ](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## 列を追加

1. _[!UICONTROL Layout]_&#x200B;の下の [!DNL Page Builder] パネルで、**[!UICONTROL Column]**&#x200B;をステージにドラッグします。

   ![ 列のステージへのドラッグ ](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

   列グループが同じ幅の 2 つの列に分割されました。 各列は、コンテンツの個別のコンテナであり、独自のツールボックスオプションのセットを持ちます。

   ![2 つの等しい列 ](./assets/pb-layout-columns-two-empty.png){width="600" zoomable="yes"}

1. 列グループの左上隅にある _グリッド_ ツール（![Grid control](./assets/pb-icon-grid-control.png)）をクリックして、必要に応じてグリッドのサイズを調整します。

   コンテンツをグリッドに配置すると、コンテンツを一貫して配置でき、デスクトップとモバイルデバイスの両方でページを正しくレンダリングできます。 詳しくは、[!DNL Page Builder] 設定の [ 詳細なコンテンツツール ](../configuration-reference/general/content-management.md) の節を参照してください。

   ![2 列のグリッド分割 ](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## 列のサイズ変更

1. 2 つの列の境界線にポインタを合わせます。

   境界線がハイライト表示され、選択した列のツールボックスが表示されます。

   ![2 つの列の間のハイライト表示された境界線 ](./assets/pb-column-resize-border.png){width="600" zoomable="yes"}

1. マウス ボタンを押したままにしてグリッドを表示し、グリッド上の新しい位置に境界線をドラッグします。

   両方の列の幅は、変更を反映して調整されます。 各列の新しい幅は、`4/12` （4 out of 12）や `8/12` （8 out of 12）のように、ラベルの後に表示されます。

   ![ サイズ変更された列 ](./assets/pb-columns-resized-grid.png){width="600" zoomable="yes"}

## 列の削除

1. 削除する列の上にマウスポインターを置いてツールボックスを表示し、_削除_ （![ 削除アイコン ](./assets/pb-icon-remove.png){width="20"}）アイコンを選択します。

   ![ 列ツールボックス ](./assets/pb-column-toolbox-remove.png){width="600" zoomable="yes"}

1. 列にコンテンツが含まれている場合は、「**[!UICONTROL OK]**」をクリックして確定します。

   今後のプロセスを高速化するには、「**[!UICONTROL Do not show this again]**」チェックボックスをオンにして、確認ステップをスキップします。

   列グループには、1 つの列（12/12）とグリッドが含まれるようになりました。 グリッドは列に対してのみ使用可能なので、この方法を使用してグリッドを表示できます。

   ![ グリッド付き単一の列 ](./assets/pb-column-single-grid.png){width="600" zoomable="yes"}

1. 列グループを使用して、残りの列を行またはステージの幅いっぱいに拡張する場合：

   - 列の上にマウスポインターを置いてツールボックスを表示し、「_設定_」（![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   - 「_[!UICONTROL Advanced]_」セクションまでスクロールし、4 つの&#x200B;**[!UICONTROL Padding]**&#x200B;値をすべて `0` に設定します。

     ![ ゼロのパディングを使用 ](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

   - 右上隅の「**[!UICONTROL Save]**」をクリックして、_[!UICONTROL Edit Column]_&#x200B;ページを閉じます。

1. ワークスペースの右上隅にある _フルスクリーンを閉じる_ アイコン ![ フルスクリーンアイコンを閉じる ](./assets/pb-icon-reduce.png){width="20"} アイコンをクリックし、右上隅の「**[!UICONTROL Save]**」をクリックします。

## 列設定の変更

1. 列の上にマウスポインターを置いてツールボックスを表示し、「_設定_」（![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![ 列ツールボックス ](./assets/pb-column-toolbox-settings.png){width="600" zoomable="yes"}

1. 必要に応じて、**[!UICONTROL Appearance]** の設定を変更します。

   - コンテナに対する列の位置を決定する整列設定を選択します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Full Height` | 列は、コンテナの高さを最大にします。 |
     | `Top Aligned` | 列はコンテナの一番上に配置されます。 |
     | `Centered` | 列は、コンテナの中央に配置されます。 |
     | `Bottom Aligned` | 列はコンテナの下部に配置されます。 |

     {style="table-layout:auto"}

   - 必要に応じて、列の **[!UICONTROL Minimum Height]** を入力します。 例えば、背景画像の高さに合わせて最小の高さを設定できます。

   - 最小の高さを設定する場合は、**[!UICONTROL Vertical Alignment]** を設定して、列に追加されるコンテンツコンテナの位置（`Top`、`Center`、`Bottom`）を制御します。

1. 列コンテンツの背景を変更します。

   - **[!UICONTROL Background Color]** - カラーを指定するには、見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力します。 この設定により、列の背景色が決まります。

   - **[!UICONTROL Background Image]** – 必要に応じて、用意されているツールを使用して列に適用する背景画像を選択します。

     | ツール | 説明 |
     | ------ | ----------- |
     | [!UICONTROL Upload] | ローカルコンピューターからギャラリーに画像ファイルをアップロードし、列の背景画像として適用します。 |
     | [!UICONTROL Select from Gallery] | 列の背景画像として、ギャラリーから既存の画像を選択するように求めるプロンプトを表示します。 |
     | ![ カメラアイコン ](./assets/pb-icon-camera.png){width="25"} | 画像をカメラタイルにドラッグするか、ローカルファイルシステム内の画像を参照できます。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Mobile Image]** – 必要に応じて、同じツールを使用して、モバイルデバイスでの表示に使用する別の背景画像を選択します。

   - **[!UICONTROL Background Size]** – この設定を変更すると、列の幅に対する背景画像の拡大縮小の方法を指定できます。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Cover` | 背景画像は、列の全幅をカバーしています。 |
     | `Contain` | 背景画像は、コンテンツ領域の幅に制限されます。 |
     | `Auto` | 現在のテーマのスタイルシートで指定されているデフォルトの背景サイズを適用します。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Position]** – この設定を変更して、列に対する画像のアンカーポイントを決定します。 オプション：`Top Left`、`Top Center`、`Top Right`、`Center Left`、`Center`、`Center Right`、`Bottom Left`、`Bottom Center` または `Bottom Right`

   - **[!UICONTROL Background Attachment]** – この設定を変更して、スクロール ページに対する背景画像の移動方法を指定します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Scroll` | 背景画像は、ページがスクロールすると下に移動するように同期されます。 |
     | `Fixed` | （モバイルでは使用できません）コンテナが画像の上をスクロールしても、背景画像は移動せず、指定された背景位置に固定されます。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Repeat]** – 背景画像を繰り返してスペースを埋める場合は、この設定 `Yes` を変更します。

1. 必要に応じて、_[!UICONTROL Advanced]_&#x200B;設定を更新します。

   - 列に追加されるコンテンツコンテナの水平方向の位置を制御するには、**[!UICONTROL Alignment]** のいずれかを選択します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | コンテンツコンテナを列コンテナの左の境界線に沿って配置します。指定したパディングを使用できます。 |
     | `Center` | コンテンツコンテナを列コンテナの中央に揃えます。指定したパディングに余裕があります。 |
     | `Right` | コンテンツコンテナを列コンテナの右端に沿って配置します。指定したパディングに余裕があります。 |

     {style="table-layout:auto"}

   - 列コンテナの 4 つの側面すべてに適用される **[!UICONTROL Border]** スタイルを設定します。

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

   - （オプション）列コンテナに適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

     複数のクラス名はスペースで区切ります。

   - 列の外側の余白と内側のパディングを指定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

     対応する各値を列コンテナ図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション：`Top`/`Right`/`Bottom`/`Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション：`Top`/`Right`/`Bottom`/`Left` |

     {style="table-layout:auto"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。
