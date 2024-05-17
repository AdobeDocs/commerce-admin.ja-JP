---
title: レイアウト – 行
description: で行を追加するために使用される、行コンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: 0aa8bf6f-7ae3-4718-9f76-430ed63ba05c
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1620'
ht-degree: 0%

---

# レイアウト – 行

の使用 _行_ 行を追加するコンテンツタイプ [[!DNL Page Builder] ステージ](workspace.md#stage).

{{$include /help/_includes/page-builder-save-timeout.md}}

## 行ツールボックス

行のツールボックスは、行コンテナにカーソルを合わせると表示されます。 ツールボックスには、行を移動、非表示、複製、編集または削除するオプションが含まれています。 設定の選択によって、行の外観、背景、レイアウトが決まります。 追加のコンテンツ要素は、 [!DNL Page Builder] 左側のパネル。

![行ツールボックス](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ---------- | ----------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 行をステージ上の他の行と相対的に別の位置に移動します。 |
| （ラベル） | [!UICONTROL Row] | 現在のコンテンツコンテナを行として識別します。 コンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 行の編集ページが開きます。このページで、コンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在の行を非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示の行を表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | 行をコピーします。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | 行コンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 行を追加

1. が含まれる [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、新規ドラッグ&#x200B;**[!UICONTROL Row]**ステージの最初の行のすぐ下に。

1. 行を書式設定するには、行コンテナにカーソルを合わせてツールボックスを表示し、次の中から _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   使用可能な設定の完了の詳細については、次の節を参照してください。

   ![行の追加](./assets/pb-layout-row-add.png){width="600" zoomable="yes"}

## 行設定の変更

1. 行コンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![行ツールボックス](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. 使用可能な設定の更新について詳しくは、次の節を参照してください。

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

## 外観

の使用 _外観_ 行にコンテンツを表示する方法を決定するための設定。

![外観設定](./assets/pb-row-layout.png){width="600" zoomable="yes"}

- コンテンツ領域のコンテナと幅に対する背景色や背景画像の表示方法を決定するには、配置を選択します。

  | オプション | 説明 |
  | ------ | ----------- |
  | [!UICONTROL Contained] | 背景色または画像は、テーマで定義されている最大ページ幅に制限されます。 |
  | [!UICONTROL Full Width] | テーマで定義されているページの幅の最大値にコンテンツを制限します。 背景色や画像に制限はなく、行の全幅を拡張します。 |
  | [!UICONTROL Full Bleed] | コンテンツと背景画像や色は制限されず、行の全幅を拡張します。 フル ブリードアウトは以下の場合にのみ使用できます。 [テーマ](../content-design/themes.md) レイアウトをサポートする。 |

  {style="table-layout:auto"}

- を入力 **[!UICONTROL Minimum Height]** 行に使用します。 この値には、有効な CSS 単位（など）を含む数値を指定できます `100px`, `50%`, `50em`, `100vh`）または計算（など `100vh - 237px`）に設定します。

  例えば、行の最小の高さを設定して、ページの完全な高さを伸ばすことができ、完全なページの背景画像やビデオに対して魅力的なオプションを提供します。

- を選択 **[!UICONTROL Vertical Alignment]** 行（上、中央または下）に追加されたコンテンツコンテナを揃えるための設定。

## 背景

行の背景表示を定義するには、多くのオプションがあります。 シンプルなカラーまたは背景画像を適用し、より高度な効果を管理できます。

### 背景色

スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、背景色を指定します。 この設定により、行の背景色が決まります。 また、カラーの不透明度を調整することもできます。

![カラーなし（デフォルト）](./assets/pb-settings-background-color-no-color.png){width="200"}

次の 3 つの方法のいずれかで値を設定できます。

- 事前定義済みのカラー名（など） `White`
- カラーの 16 進数値（例：） `#ffffff`
- 次のような、不透明度のパーセントを使用したカラーの rgba 値 `rgba(255, 255, 255, 0.75)`

カラーを選択する場合は、の左側にあるスウォッチをクリックします _カラーなし_ ボックス。

![カラースウォッチの選択](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

カラーボックスをクリックして再度カラーピッカーを開くと、スライダの下のボックスに現在の赤、緑、青、アルファ値（rgba）が表示されます。 最後の数値は、現在の不透明度の割合を小数で示します。 スライダを使用して、不透明度を調整したり、必要な小数値を入力したりできます。

![不透明度の設定](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] では、透明度レイヤーもサポートされています。 _アルファチャネル_：様々な不透明度の背景を作成するために使用できる背景画像。

### [!UICONTROL Background Type]

背景の種類は、画像またはビデオです。 [!DNL Page Builder] デフォルトは `Image` 様々な画像設定を表示します。 を選択する場合 `Video`, [!DNL Page Builder] 画像設定をビデオ設定にスワップします。 どちらの背景タイプも次のように説明します。

![背景タイプ](./assets/pb-background-type.png){width="200"}

### 画像タイプの設定

を設定した場合 _[!UICONTROL Background Type]_対象： `Image`以下の設定を使用して、背景画像の表示を定義します。

![背景画像](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]**  – 必要に応じて、提供されたツールを使用して、行に適用する背景画像を選択します。

  | オプション | 説明 |
  | ------ | ----------- |
  | [!UICONTROL Upload] | ローカルコンピューターからギャラリーに画像ファイルをアップロードし、それを行の背景画像として適用します。 |
  | [!UICONTROL Select from Gallery] | 行の背景画像として、ギャラリーから既存の画像を選択するように求めるプロンプトを表示します。 |
  | ![カメラアイコン](./assets/pb-icon-camera.png){width="25"} | 画像をカメラタイルにドラッグするか、ローカルファイルシステム内の画像を参照できます。 |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]**  – 必要に応じて、同じツールを使用して、モバイルデバイスでの表示に使用する別の背景画像を選択します。

- **[!UICONTROL Background Size]**  – 行の幅に対して背景画像をどのように拡大/縮小するかを指定するには、このオプションを設定します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Cover` | 背景画像は、行の全幅をカバーしています。 |
  | `Contain` | 背景画像は、コンテンツ領域の幅に制限されます。 |
  | `Auto` | 現在のスタイル シートからサイズを適用します。 |

  {style="table-layout:auto"}

  ![背景サイズ](./assets/pb-layout-row-settings-background-size-cover.png){width="250"}

- **[!UICONTROL Background Position]**  – このオプションを設定して、背景画像を行に対してどのように固定するかを指定します。

  | アンカーポイント | 位置 |
  | ------ | ----------- |
  | `Top` | 左/中央/右 |
  | `Center` | 左/中央/右 |
  | `Bottom` | 左/中央/右 |

  {style="table-layout:auto"}

  アンカーポイントは、プッシュピンのようなもので、指定した背景位置の行に画像をアタッチします。

- **[!UICONTROL Background Attachment]**  – 添付ファイルタイプを設定して、スクロールするページに対する背景画像の移動を指定します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Scroll` | 添付された背景画像は、ページがスクロールすると下に移動するように同期されます。 スクロール速度を制御するには、Parallax Background を使用します。 |
  | `Fixed` | （モバイルでは使用できません）コンテナが画像の上をスクロールし、指定された背景位置に固定されるので、背景画像は移動しません。 |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]**  – に設定 `Yes` 行内の空きスペースを埋めるために背景画像を繰り返します。

### ビデオタイプの設定

を設定した場合 _背景の種類_ 対象： `Video`以下の設定を使用して、背景画像の表示を定義します。

- **[!UICONTROL Video URL]**  – 有効なビデオ URL を入力します。 有効なビデオ URL は、次へのリンクです。

   - YouTube ビデオ： `https://youtu.be/CoDhMRUUjeI`
   - Vimeo 動画： `https://vimeo.com/190156113`
   - 有効なビデオファイル （`.mp4` 推奨）: `https://myvideos.com/spiral.mp4`

  ![背景ビデオ URL](./assets/pb-video-url.png){width="300"}

- **[!UICONTROL Overlay Color]** - ビデオに透明な色合いを適用するカラーを選択します。

- **[!UICONTROL Infinite Loop]**  – に設定 `No` ビデオを一度再生して停止します。 このオプションを `Yes` （デフォルト）ビデオは無限ループで繰り返されます。

- **[!UICONTROL Lazy Load]**  – に設定 `No` 表示されていない場合でも、ビデオをページと共に読み込むことができるようにする。 このオプションを `Yes` （デフォルト）ソースからビデオが読み込まれるのは、画面に表示されている場合のみです。

- **[!UICONTROL Play Only When Visible]**  – に設定 `No` ビデオが表示されているかどうかに関係なく、ビデオの読み込み直後に再生を開始します。 このオプションを `Yes` （デフォルト）ビデオは、表示されている場合にのみ再生を開始します。

- **[!UICONTROL Fallback Image]**  – 必要に応じて、ビデオが読み込まれる前および何らかの理由でビデオが読み込まれない場合に、画面に表示する画像を指定します。

## 視差背景

これらのオプションを使用して、ページのスクロールに対する、背景の画像やビデオのスクロールの速度の制御を行います。 背景のスクロール速度を遅くして、没入感を生み出すことができます。

- を設定 **視差の背景を有効にする** 対象： `Yes`.
- を入力 **視差速度** 間の小数値として `-1.0` および `2.0`.

![Parallax Background 設定](./assets/pb-settings-parallax-background.png){width="600" zoomable="yes"}

## 詳細

- 行に追加されるコンテンツコンテナの水平方向の位置を制御するには、次のいずれかを選択します **[!UICONTROL Alignment]**:

  | オプション | 説明 |
  | ------ | ----------- |
  | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
  | `Left` | コンテンツコンテナを行コンテナの左の境界線に沿って配置します。指定したパディングを使用できます。 |
  | `Center` | コンテンツコンテナを行コンテナの中央に揃えます。指定したパディングに余裕があります。 |
  | `Right` | コンテンツコンテナを行コンテナの右端に沿って配置します。指定したパディングに余裕があります。 |

  {style="table-layout:auto"}

- を **[!UICONTROL Border]** 行コンテナの 4 つの辺すべてに適用されるスタイル：

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

  ![境界線のカラー](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | オプション | 説明 |
  | ------ |------------ |
  | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
  | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
  | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

  {style="table-layout:auto"}

  次の例の行の境界線の半径は 15 です。

  ![行（境界線の半径 15）](./assets/pb-settings-border-radius-15.png){width="500"}

- （オプション）の名前を指定します **[!UICONTROL CSS classes]** 行コンテナに適用する現在のスタイルシートから。

  複数のクラス名はスペースで区切ります。

- 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** 行の外側の余白と内側のパディングを指定します。

  対応する各値を行コンテナ図に入力します。

  | コンテナ領域 | 説明 |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
  | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション： `Top` / `Right` / `Bottom` / `Left` |

  {style="table-layout:auto"}

  ![余白とパディング](./assets/pb-layout-row-settings-margin-padding-default.png){width="600" zoomable="yes"}
