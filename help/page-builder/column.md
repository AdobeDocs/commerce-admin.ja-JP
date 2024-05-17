---
title: レイアウト – 列
description: でページを複数の列に分割するために使用される、列コンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: 9701e1b5-3584-4602-9512-051567274f21
feature: Page Builder, Page Content
source-git-commit: 63b620f2af106108c672a9a91cb66923c5231c53
workflow-type: tm+mt
source-wordcount: '1574'
ht-degree: 0%

---

# レイアウト – 列

の使用 _列_ コンテンツタイプ：でページを複数の列に分割します。 [[!DNL Page Builder] ステージ](workspace.md#stage). 列を行、タブ、またはステージに直接追加すると、列グループは最初は同じ幅の 2 つの列に分割されます。 必要に応じて、列を追加または削除できます。 列のサイズを変更するには、2 つの列の間の境界線をドラッグします。 次の列の幅は、行、タブ、ステージ内の使用可能なスペースを埋めるように調整されます。 単一の列は、ステージまたはそのコンテナの全幅を拡張します。

![列の追加](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 2.4.5 リリースのアップデート

ページビルダー機能が 2.4.5 リリースで更新され、ユーザーはを使用できるようになりました _[!DNL Columns]_個々の列の親コンテナとして。 この新しいコンテナでは、背景のプロパティもサポートされるようになり、列を一列に折り返す必要がなくなります。 これにより、不要なマークアップを減らし、ストアフロントの表示とエクスペリエンスをより詳細に制御できます。

のレイアウトを変更することができます [!DNL Columns] コンテナで、グループ内の他の列の上または下に列をドラッグして積み重ねます。 これにより、開発者がカスタマイズする必要なしに達成できる、新しいさまざまなレイアウトの組み合わせが可能になります。

このビデオでは、方法を説明します [!DNL Columns] コンテナを使用してページレイアウトを調整することができます。

>[!VIDEO](https://video.tv.adobe.com/v/345828?quality=12)

## 列ツールボックス

各列には、コンテナの上にマウスポインターを置くと表示されるオプションのツールボックスがあります。

| ツール | アイコン | 説明 |
|--- |--- |--- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 列とその内容を、他の列と相対的に別の位置に移動します。 |
| （ラベル） | 列 | 現在のコンテナを列として識別します。 列コンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 列を編集ページを開きます。このページで、コンテナのプロパティを変更できます。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | 現在の列をコピーします。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | 現在の列とその内容を削除します。 |

{style="table-layout:auto"}

## 柱通芯

この [グリッド](workspace.md) コンテンツを一貫して列に配置し、デスクトップとモバイルデバイスの両方でページが正しくレンダリングされるようにします。 詳しくは、 [高度なコンテンツツール](setup.md) の節 [!DNL Page Builder] 設定。

![1 つの列を持つ行のグリッド分割](./assets/pb-layout-column-one-grid.png){width="500" zoomable="yes"}

次の 2 列の例では、各列コンテナの上部のボーダーの括弧内の数値（6/12）は、各列のグリッド分割数と分割総数を示しています。 この場合、柱は、合計 12 のうち 6 つのグリッド単位の幅です。

![2 列の行のグリッド分割](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## 列を追加

1. が含まれる [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、ドラッグ：**[!UICONTROL Column]**ステージに移動します。

   ![列をステージにドラッグ](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

   列グループが同じ幅の 2 つの列に分割されました。 各列は、コンテンツの個別のコンテナであり、独自のツールボックスオプションのセットを持ちます。

   ![2 つの等しい列](./assets/pb-layout-columns-two-empty.png){width="600" zoomable="yes"}

1. 列グループの左上隅の「」をクリックします _グリッド_ ツール （![グリッドコントロール](./assets/pb-icon-grid-control.png)）を選択し、必要に応じてグリッドサイズを調整します。

   コンテンツをグリッドに配置すると、コンテンツを一貫して配置でき、デスクトップとモバイルデバイスの両方でページを正しくレンダリングできます。 詳しくは、 [高度なコンテンツツール](../configuration-reference/general/content-management.md) の節 [!DNL Page Builder] 設定。

   ![2 列のグリッド分割](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## 列のサイズ変更

1. 2 つの列の境界線にポインタを合わせます。

   境界線がハイライト表示され、選択した列のツールボックスが表示されます。

   ![2 つの列の間のハイライト表示された境界線](./assets/pb-column-resize-border.png){width="600" zoomable="yes"}

1. マウス ボタンを押したままにしてグリッドを表示し、グリッド上の新しい位置に境界線をドラッグします。

   両方の列の幅は、変更を反映して調整されます。 次のように、各列の新しい幅がラベルの後に表示されます `4/12` （12 個中 4 個）と `8/12` （8/12）。

   ![サイズ変更された列](./assets/pb-columns-resized-grid.png){width="600" zoomable="yes"}

## 列の削除

1. 削除する列の上にマウスポインターを置いてツールボックスを表示し、 _削除_ （ ![アイコンを削除](./assets/pb-icon-remove.png){width="20"} ） アイコンをクリックします。

   ![列ツールボックス](./assets/pb-column-toolbox-remove.png){width="600" zoomable="yes"}

1. 列にコンテンツが含まれている場合は、 **[!UICONTROL OK]** を確認します。

   今後プロセスを高速化するには、を選択して確認ステップをスキップできます **[!UICONTROL Do not show this again]** チェックボックス。

   列グループには、1 つの列（12/12）とグリッドが含まれるようになりました。 グリッドは列に対してのみ使用可能なので、この方法を使用してグリッドを表示できます。

   ![グリッド付き単一列](./assets/pb-column-single-grid.png){width="600" zoomable="yes"}

1. 列グループを使用して、残りの列を行またはステージの幅いっぱいに拡張する場合：

   - 列の上にマウスポインターを置いてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   - にスクロール ダウンします。 _[!UICONTROL Advanced]_を選択し、4 つすべてを設定します&#x200B;**[!UICONTROL Padding]**値：至 `0`.

     ![ゼロのパディングの使用](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

   - 右上隅のをクリックします。 **[!UICONTROL Save]** を閉じるには _[!UICONTROL Edit Column]_ページ。

1. 「」をクリックします _全画面表示を閉じる_ （ ![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png){width="20"} ） アイコンをクリックし、をクリックします。 **[!UICONTROL Save]** 右上隅

## 列設定の変更

1. 列の上にマウスポインターを置いてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![列ツールボックス](./assets/pb-column-toolbox-settings.png){width="600" zoomable="yes"}

1. 変更： **[!UICONTROL Appearance]** 必要に応じて設定します。

   - コンテナに対する列の位置を決定する整列設定を選択します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Full Height` | 列は、コンテナの高さを最大にします。 |
     | `Top Aligned` | 列はコンテナの一番上に配置されます。 |
     | `Centered` | 列は、コンテナの中央に配置されます。 |
     | `Bottom Aligned` | 列はコンテナの下部に配置されます。 |

     {style="table-layout:auto"}

   - 必要に応じて、を入力します **[!UICONTROL Minimum Height]** を列に追加します。 例えば、背景画像の高さに合わせて最小の高さを設定できます。

   - 最小高さを設定した場合は、 **[!UICONTROL Vertical Alignment]**  列に追加されるコンテンツコンテナの位置を制御するには、以下を行います（`Top`, `Center`、または `Bottom`）に設定します。

1. 列コンテンツの背景を変更します。

   - **[!UICONTROL Background Color]** - スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 この設定により、列の背景色が決まります。

   - **[!UICONTROL Background Image]**  – 必要に応じて、用意されているツールを使用して列に適用する背景画像を選択します。

     | ツール | 説明 |
     | ------ | ----------- |
     | [!UICONTROL Upload] | ローカルコンピューターからギャラリーに画像ファイルをアップロードし、列の背景画像として適用します。 |
     | [!UICONTROL Select from Gallery] | 列の背景画像として、ギャラリーから既存の画像を選択するように求めるプロンプトを表示します。 |
     | ![カメラアイコン](./assets/pb-icon-camera.png){width="25"} | 画像をカメラタイルにドラッグするか、ローカルファイルシステム内の画像を参照できます。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Mobile Image]**  – 必要に応じて、同じツールを使用して、モバイルデバイスでの表示に使用する別の背景画像を選択します。

   - **[!UICONTROL Background Size]**  – この設定を変更すると、列の幅を基準にして背景画像を拡大/縮小する方法を指定できます。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Cover` | 背景画像は、列の全幅をカバーしています。 |
     | `Contain` | 背景画像は、コンテンツ領域の幅に制限されます。 |
     | `Auto` | 現在のテーマのスタイルシートで指定されているデフォルトの背景サイズを適用します。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Position]**  – この設定を変更して、列に対する画像のアンカーポイントを決定します。 オプション： `Top Left`, `Top Center`, `Top Right`, `Center Left`, `Center`, `Center Right`, `Bottom Left`, `Bottom Center`、または `Bottom Right`

   - **[!UICONTROL Background Attachment]**  – この設定を変更して、スクロール ページに対する背景画像の移動方法を指定します：

     | オプション | 説明 |
     | ------ | ----------- |
     | `Scroll` | 背景画像は、ページがスクロールすると下に移動するように同期されます。 |
     | `Fixed` | （モバイルでは使用できません）コンテナが画像の上をスクロールしても、背景画像は移動せず、指定された背景位置に固定されます。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Repeat]**  – 背景画像をスペースいっぱいに繰り返す場合は、この設定を変更します `Yes`.

1. を更新 _[!UICONTROL Advanced]_必要に応じて設定します。

   - 列に追加されるコンテンツコンテナの水平方向の位置を制御するには、次のいずれかを選択します **[!UICONTROL Alignment]**:

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | コンテンツコンテナを列コンテナの左の境界線に沿って配置します。指定したパディングを使用できます。 |
     | `Center` | コンテンツコンテナを列コンテナの中央に揃えます。指定したパディングに余裕があります。 |
     | `Right` | コンテンツコンテナを列コンテナの右端に沿って配置します。指定したパディングに余裕があります。 |

     {style="table-layout:auto"}

   - を **[!UICONTROL Border]** 列コンテナの 4 つの側面すべてに適用されるスタイル。

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

   - （オプション）の名前を指定します **[!UICONTROL CSS classes]** 列コンテナに適用する現在のスタイルシートから。

     複数のクラス名はスペースで区切ります。

   - 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** 列の外側の余白と内側のパディングを指定します。

     対応する各値を列コンテナ図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。
