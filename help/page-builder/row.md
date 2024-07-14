---
title: レイアウト – 行
description: ステージで行を追加するために使用される、行コンテンツタイプについて説明  [!DNL Page Builder]  ます。
exl-id: 0aa8bf6f-7ae3-4718-9f76-430ed63ba05c
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1620'
ht-degree: 0%

---

# レイアウト – 行

_行_ コンテンツタイプを使用して、[[!DNL Page Builder]  ステージ ](workspace.md#stage) に行を追加します。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 行ツールボックス

行のツールボックスは、行コンテナにカーソルを合わせると表示されます。 ツールボックスには、行を移動、非表示、複製、編集または削除するオプションが含まれています。 設定の選択によって、行の外観、背景、レイアウトが決まります。 追加のコンテンツ要素は、左側の [!DNL Page Builder] パネルから行にドラッグできます。

![ 行ツールボックス ](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ---------- | ----------- |
| 移動 | ![ 移動アイコン ](./assets/pb-icon-move.png){width="25"} | 行をステージ上の他の行と相対的に別の位置に移動します。 |
| （ラベル） | [!UICONTROL Row] | 現在のコンテンツコンテナを行として識別します。 コンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![ 設定アイコン ](./assets/pb-icon-settings.png){width="25"} | 行の編集ページが開きます。このページで、コンテナのプロパティを変更できます。 |
| Hide | ![ アイコンを非表示 ](./assets/pb-icon-hide.png){width="25"} | 現在の行を非表示にします。 |
| 表示 | ![ アイコンを表示 ](./assets/pb-icon-show.png){width="25"} | 非表示の行を表示します。 |
| 複製 | ![ 複製アイコン ](./assets/pb-icon-duplicate.png){width="25"} | 行をコピーします。 |
| 削除 | ![ 削除アイコン ](./assets/pb-icon-remove.png){width="25"} | 行コンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 行を追加

1. [!DNL Page Builder] パネルの _[!UICONTROL Layout]_の下で、新しい&#x200B;**[!UICONTROL Row]**をステージの最初の行のすぐ下にドラッグします。

1. 行を書式設定するには、行コンテナの上にマウスポインターを置いてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   使用可能な設定の完了の詳細については、次の節を参照してください。

   ![ 行の追加 ](./assets/pb-layout-row-add.png){width="600" zoomable="yes"}

## 行設定の変更

1. 行コンテナにカーソルを合わせてツールボックスを表示し、「_設定_」（![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![ 行ツールボックス ](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. 使用可能な設定の更新について詳しくは、次の節を参照してください。

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

## 外観

_外観_ 設定を使用して、行にコンテンツを表示する方法を決定します。

![ 外観設定 ](./assets/pb-row-layout.png){width="600" zoomable="yes"}

- コンテンツ領域のコンテナと幅に対する背景色や背景画像の表示方法を決定するには、配置を選択します。

  | オプション | 説明 |
  | ------ | ----------- |
  | [!UICONTROL Contained] | 背景色または画像は、テーマで定義されている最大ページ幅に制限されます。 |
  | [!UICONTROL Full Width] | テーマで定義されているページの幅の最大値にコンテンツを制限します。 背景色や画像に制限はなく、行の全幅を拡張します。 |
  | [!UICONTROL Full Bleed] | コンテンツと背景画像や色は制限されず、行の全幅を拡張します。 フルブリードは、レイアウトをサポートする [ テーマ ](../content-design/themes.md) に対してのみ使用できます。 |

  {style="table-layout:auto"}

- 行の **[!UICONTROL Minimum Height]** を入力します。 この値には、有効な CSS 単位（`100px`、`50%`、`50em`、`100vh` など）または計算（`100vh - 237px` など）を含む数値を指定できます。

  例えば、行の最小の高さを設定して、ページの完全な高さを伸ばすことができ、完全なページの背景画像やビデオに対して魅力的なオプションを提供します。

- **[!UICONTROL Vertical Alignment]** 設定を選択して、行（上、中央または下）に追加されたコンテンツコンテナを整列します。

## 背景

行の背景表示を定義するには、多くのオプションがあります。 シンプルなカラーまたは背景画像を適用し、より高度な効果を管理できます。

### 背景色

スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、背景色を指定します。 この設定により、行の背景色が決まります。 また、カラーの不透明度を調整することもできます。

![ 色なし（デフォルト） ](./assets/pb-settings-background-color-no-color.png){width="200"}

次の 3 つの方法のいずれかで値を設定できます。

- 定義済みのカラー名（`White` など）
- カラーの 16 進数カラー値（例：`#ffffff`）
- カラーの rgba 値（不透明度の割合）（`rgba(255, 255, 255, 0.75)` など）。

カラーを選択する場合は、「カラーなし _ボックスの左側にあるスウォッチをクリックし_ す。

![ カラースウォッチの選択 ](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

カラーボックスをクリックして再度カラーピッカーを開くと、スライダの下のボックスに現在の赤、緑、青、アルファ値（rgba）が表示されます。 最後の数値は、現在の不透明度の割合を小数で示します。 スライダを使用して、不透明度を調整したり、必要な小数値を入力したりできます。

![ 不透明度の設定 ](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] では、背景画像に透明度レイヤー（_アルファチャンネル_ を含めることもできます。このレイヤーを使用して、様々な不透明度の背景を作成できます。

### [!UICONTROL Background Type]

背景の種類は、画像またはビデオです。 デフォルト [!DNL Page Builder]`Image` で、様々な画像設定が表示されます。 `Video` を選択すると、[!DNL Page Builder] は画像設定をビデオ設定にスワップします。 どちらの背景タイプも次のように説明します。

![ 背景の種類 ](./assets/pb-background-type.png){width="200"}

### 画像タイプの設定

_[!UICONTROL Background Type]_を `Image` に設定した場合は、次の設定を使用して背景画像の表示を定義します。

![ 背景画像 ](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** – 必要に応じて、提供されたツールを使用して、行に適用する背景画像を選択します。

  | オプション | 説明 |
  | ------ | ----------- |
  | [!UICONTROL Upload] | ローカルコンピューターからギャラリーに画像ファイルをアップロードし、それを行の背景画像として適用します。 |
  | [!UICONTROL Select from Gallery] | 行の背景画像として、ギャラリーから既存の画像を選択するように求めるプロンプトを表示します。 |
  | ![ カメラアイコン ](./assets/pb-icon-camera.png){width="25"} | 画像をカメラタイルにドラッグするか、ローカルファイルシステム内の画像を参照できます。 |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** – 必要に応じて、同じツールを使用して、モバイルデバイスでの表示に使用する別の背景画像を選択します。

- **[!UICONTROL Background Size]** – 行の幅に対する背景画像の拡大縮小の方法を指定するには、このオプションを設定します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Cover` | 背景画像は、行の全幅をカバーしています。 |
  | `Contain` | 背景画像は、コンテンツ領域の幅に制限されます。 |
  | `Auto` | 現在のスタイル シートからサイズを適用します。 |

  {style="table-layout:auto"}

  ![ 背景サイズ ](./assets/pb-layout-row-settings-background-size-cover.png){width="250"}

- **[!UICONTROL Background Position]** – 行に対する背景画像のアンカー方法を指定するには、このオプションを設定します。

  | アンカーポイント | 位置 |
  | ------ | ----------- |
  | `Top` | 左/中央/右 |
  | `Center` | 左/中央/右 |
  | `Bottom` | 左/中央/右 |

  {style="table-layout:auto"}

  アンカーポイントは、プッシュピンのようなもので、指定した背景位置の行に画像をアタッチします。

- **[!UICONTROL Background Attachment]** – 添付ファイルタイプを設定して、スクロールするページに対する背景画像の移動を指定します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Scroll` | 添付された背景画像は、ページがスクロールすると下に移動するように同期されます。 スクロール速度を制御するには、Parallax Background を使用します。 |
  | `Fixed` | （モバイルでは使用できません）コンテナが画像の上をスクロールし、指定された背景位置に固定されるので、背景画像は移動しません。 |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** - `Yes` に設定すると、行内の使用可能なスペースに背景画像が繰り返し表示されます。

### ビデオタイプの設定

_背景の種類_ を `Video` に設定する場合、次の設定を使用して背景画像の表示を定義します。

- **[!UICONTROL Video URL]** – 有効なビデオ URL を入力します。 有効なビデオ URL は、次へのリンクです。

   - YouTube ビデオ：`https://youtu.be/CoDhMRUUjeI`
   - Vimeo ビデオ：`https://vimeo.com/190156113`
   - 有効なビデオ ファイル （`.mp4` を推奨）: `https://myvideos.com/spiral.mp4`

  ![ 背景ビデオの URL](./assets/pb-video-url.png){width="300"}

- **[!UICONTROL Overlay Color]** - ビデオに透明の濃淡を適用するカラーを選択します。

- **[!UICONTROL Infinite Loop]** - `No` に設定すると、ビデオを 1 回再生して停止します。 このオプションを `Yes` （デフォルト）に設定すると、ビデオは無限ループで繰り返されます。

- **[!UICONTROL Lazy Load]** - `No` に設定すると、非表示の場合でもビデオがページと共に読み込まれます。 このオプションを `Yes` （デフォルト）に設定すると、画面に表示されている場合にのみ、ビデオはソースから読み込まれます。

- **[!UICONTROL Play Only When Visible]** - ビデオが表示されているかどうかに関係なく、ビデオの読み込み直後に再生を開始するには、`No` に設定します。 このオプションが `Yes` （デフォルト）に設定されている場合、ビデオは表示されているときにのみ再生を開始します。

- **[!UICONTROL Fallback Image]** – 必要に応じて、ビデオが読み込まれる前および何らかの理由でビデオが読み込まれない場合に画面に表示する画像を指定します。

## 視差背景

これらのオプションを使用して、ページのスクロールに対する、背景の画像やビデオのスクロールの速度の制御を行います。 背景のスクロール速度を遅くして、没入感を生み出すことができます。

- **Parallax Background を有効にする** を `Yes` に設定します。
- **視差速度** を `-1.0` ～ `2.0` の 10 進数値で入力します。

![Parallax Background settings](./assets/pb-settings-parallax-background.png){width="600" zoomable="yes"}

## 詳細

- 行に追加されるコンテンツコンテナの水平方向の位置を制御するには、**[!UICONTROL Alignment]** のいずれかを選択します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
  | `Left` | コンテンツコンテナを行コンテナの左の境界線に沿って配置します。指定したパディングを使用できます。 |
  | `Center` | コンテンツコンテナを行コンテナの中央に揃えます。指定したパディングに余裕があります。 |
  | `Right` | コンテンツコンテナを行コンテナの右端に沿って配置します。指定したパディングに余裕があります。 |

  {style="table-layout:auto"}

- 行コンテナの 4 つの辺すべてに適用される **[!UICONTROL Border]** スタイルを設定します。

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

  ![ 境界線のカラー ](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | オプション | 説明 |
  | ------ |------------ |
  | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
  | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
  | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

  {style="table-layout:auto"}

  次の例の行の境界線の半径は 15 です。

  ![ 行（境界線の半径が 15 の場合） ](./assets/pb-settings-border-radius-15.png){width="500"}

- （オプション）行コンテナに適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

  複数のクラス名はスペースで区切ります。

- 行の外側の余白と内側のパディングを指定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

  対応する各値を行コンテナ図に入力します。

  | コンテナ領域 | 説明 |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション：`Top`/`Right`/`Bottom`/`Left` |
  | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション：`Top`/`Right`/`Bottom`/`Left` |

  {style="table-layout:auto"}

  ![ 余白とパディング ](./assets/pb-layout-row-settings-margin-padding-default.png){width="600" zoomable="yes"}
