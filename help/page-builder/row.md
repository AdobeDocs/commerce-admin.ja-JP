---
title: レイアウト — 行
description: 行のコンテンツタイプについて説明します。行を [!DNL Page Builder] ステージ。
exl-id: 0aa8bf6f-7ae3-4718-9f76-430ed63ba05c
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 0%

---

# レイアウト — 行

以下を使用します。 _行_ 行を [[!DNL Page Builder] ステージ](workspace.md#stage).

{{$include /help/_includes/page-builder-save-timeout.md}}

## 行ツールボックス

行コンテナの上にマウスポインターを置くと、行ツールボックスが表示されます。 ツールボックスには、行の移動、非表示、複製、編集、削除を行うオプションが含まれます。 設定の選択によって、行の外観、背景、レイアウトが決まります。 追加のコンテンツ要素は、 [!DNL Page Builder] パネルが左側に表示されます。

![行ツールボックス](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ---------- | ----------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | ステージ上の他の行に対する別の位置に行を移動します。 |
| （ラベル） | [!UICONTROL Row] | 現在のコンテンツコンテナを行として識別します。 コンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 行を編集ページを開き、コンテナのプロパティを変更できます。 |
| 非表示 | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在の行を非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示の行を表示します。 |
| 複製 | ![複製アイコン](./assets/pb-icon-duplicate.png){width="25"} | 行のコピーを作成します。 |
| 削除 | ![削除アイコン](./assets/pb-icon-remove.png){width="25"} | 行コンテナとその内容をステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 行を追加

1. Adobe Analytics の [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、新しい&#x200B;**[!UICONTROL Row]**最初の行のすぐ下のステージに

1. 行を書式設定するには、行コンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   使用可能な設定の指定について詳しくは、以下のセクションを参照してください。

   ![行の追加](./assets/pb-layout-row-add.png){width="600" zoomable="yes"}

## 行設定の変更

1. 行コンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![行ツールボックス](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. 使用可能な設定の更新について詳しくは、次のセクションを参照してください。

1. 完了したら、「 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。

## 外観

以下を使用します。 _外観_ 行にコンテンツを表示する方法を指定する設定です。

![外観の設定](./assets/pb-row-layout.png){width="600" zoomable="yes"}

- コンテンツ領域のコンテナや幅に対する背景色や背景画像の表示方法を指定するには、配置を選択します。

  | オプション | 説明 |
  | ------ | ----------- |
  | [!UICONTROL Contained] | 背景色または画像は、テーマで定義されるページの最大幅に制限されます。 |
  | [!UICONTROL Full Width] | コンテンツを、テーマで定義されている最大ページ幅に制限します。 背景色や画像は制限されず、行の幅全体に広がります。 |
  | [!UICONTROL Full Bleed] | コンテンツや背景の画像や色は制限されず、行の幅全体を広げます。 フル裁ち落としは、 [テーマ](../content-design/themes.md) それがレイアウトをサポートしています。 |

  {style="table-layout:auto"}

- 次を入力します。 **[!UICONTROL Minimum Height]** 行の。 この値は、任意の有効な CSS 単位 ( `100px`, `50%`, `50em`, `100vh`) または計算 ( `100vh - 237px`) をクリックします。

  例えば、行の最小の高さを設定して、ページの高さを最大限に引き伸ばすことができます。この設定により、ページ全体の背景画像やビデオに対する魅力的なオプションが提供されます。

- を選択します。 **[!UICONTROL Vertical Alignment]** 設定を使用して、行（上、中央、下）に追加されるコンテンツコンテナを整列させます。

## 背景

行の背景表示を定義する多くのオプションがあります。 単純なカラーまたは背景画像を適用し、より高度な効果を管理できます。

### 背景色

スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進値を入力して、背景色を指定します。 この設定は、行の背景色を決定します。 また、カラーの不透明度を調整することもできます。

![色なし（デフォルト）](./assets/pb-settings-background-color-no-color.png){width="200"}

値は、次の 3 つの方法のいずれかで設定できます。

- 事前定義済みの色名（例： ） `White`
- 色の 16 進数カラー値（例： ） `#ffffff`
- 色の rgba 値（不透明度の割合を含む）。次に例を示します。 `rgba(255, 255, 255, 0.75)`

カラーを選択する場合は、 _カラーなし_ ボックス。

![カラースウォッチの選択](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

カラーボックスをクリックしてカラーピッカーを再度開くと、スライダの下のボックスに現在の赤、緑、青、アルファの値 (rgba) が表示されます。 最後の数値は、現在の不透明度の割合を小数で示します。 スライダーを使用して不透明度を調整したり、必要な 10 進数値を入力したりできます。

![不透明度の設定](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] は、透明度レイヤーをサポートしています。 _アルファチャンネル_：様々な不透明度の背景の作成に使用できる背景画像。

### [!UICONTROL Background Type]

背景の種類には、画像またはビデオがあります。 [!DNL Page Builder] デフォルト： `Image` およびは、様々な画像設定を表示します。 次を選択した場合、 `Video`, [!DNL Page Builder] 画像設定をビデオ設定と入れ替えます。 どちらの背景タイプも次のように説明します。

![背景の種類](./assets/pb-background-type.png){width="200"}

### 画像タイプの設定

次の場合、 _[!UICONTROL Background Type]_から `Image`の場合は、次の設定を使用して背景画像表示を定義します。

![背景画像](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]**  — 必要に応じて、提供されているツールを使用して、行に適用する背景画像を選択します。

  | オプション | 説明 |
  | ------ | ----------- |
  | [!UICONTROL Upload] | ローカルコンピューターからギャラリーに画像ファイルをアップロードし、そのファイルを行の背景画像として適用します。 |
  | [!UICONTROL Select from Gallery] | ギャラリーから行の背景画像として既存の画像を選択するように求めるプロンプトが表示されます。 |
  | ![カメラアイコン](./assets/pb-icon-camera.png){width="25"} | 画像をカメラタイルにドラッグするか、ローカルファイルシステム内の画像を参照することができます。 |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]**  — 必要に応じて、同じツールを使用して、モバイルデバイスでの表示に使用する別の背景画像を選択します。

- **[!UICONTROL Background Size]**  — このオプションを設定して、行の幅に対する背景画像の拡大/縮小方法を指定します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Cover` | 背景画像は行の全幅を覆います。 |
  | `Contain` | 背景画像は、コンテンツ領域の幅に制限されます。 |
  | `Auto` | 現在のスタイルシートからサイズを適用します。 |

  {style="table-layout:auto"}

  ![背景サイズ](./assets/pb-layout-row-settings-background-size-cover.png){width="250"}

- **[!UICONTROL Background Position]**  — このオプションを設定して、行に対する背景画像のアンカー方法を指定します。

  | アンカーポイント | 位置 |
  | ------ | ----------- |
  | `Top` | 左/中央/右 |
  | `Center` | 左/中央/右 |
  | `Bottom` | 左/中央/右 |

  {style="table-layout:auto"}

  アンカーポイントは、指定した背景位置の行に画像をアタッチするプッシュピンのようなものです。

- **[!UICONTROL Background Attachment]**  — 添付ファイルのタイプを設定して、背景画像がスクロールページに対してどのように移動するかを指定します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Scroll` | 添付された背景画像は、ページがスクロールするたびに下に移動するように同期されます。 スクロール速度を制御するには、視差の背景を使用します。 |
  | `Fixed` | （モバイルでは使用できません）コンテナが画像をスクロールすると、背景画像は移動せず、指定された背景位置で固定されます。 |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]**  — に設定 `Yes` を繰り返して、行の使用可能なスペースを埋めます。

### ビデオタイプ設定

次の場合、 _背景の種類_ から `Video`の場合は、次の設定を使用して背景画像表示を定義します。

- **[!UICONTROL Video URL]**  — 有効なビデオの URL を入力します。 有効なビデオの URL は次のリンクになります。

   - YouTubeビデオ： `https://youtu.be/CoDhMRUUjeI`
   - Vimeo ビデオ： `https://vimeo.com/190156113`
   - 有効なビデオファイル (`.mp4` をお勧めします )。 `https://myvideos.com/spiral.mp4`

  ![背景ビデオの URL](./assets/pb-video-url.png){width="300"}

- **[!UICONTROL Overlay Color]**  — 色を選択して、ビデオに透明の色合いを適用します。

- **[!UICONTROL Infinite Loop]**  — に設定 `No` ビデオを 1 回再生して停止させる場合。 このオプションが `Yes` （デフォルト）。ビデオは無限ループで繰り返されます。

- **[!UICONTROL Lazy Load]**  — に設定 `No` ページが表示されていない場合でも、ビデオをページと共に読み込む。 このオプションが `Yes` （デフォルト）。ビデオは、画面に表示されている場合にのみ、ソースから読み込まれます。

- **[!UICONTROL Play Only When Visible]**  — に設定 `No` ビデオが表示されているかどうかに関係なく、読み込まれた直後にビデオの再生を開始する場合。 このオプションが `Yes` （デフォルト）。ビデオの再生は表示されているときにのみ開始されます。

- **[!UICONTROL Fallback Image]**  — 必要に応じて、ビデオが読み込まれる前に画面に表示する画像を指定します。また、何らかの理由でビデオが読み込まれない場合も指定します。

## 視差背景

ページのスクロールに関連して、背景画像やビデオをスクロールする速度を制御するには、これらのオプションを使用します。 背景は、スクロールをよりゆっくりに設定して、没入感を作り出すことができます。

- 設定 **視差の背景を有効にする** から `Yes`.
- 次を入力します。 **視差速度** ～間の 10 進数値として `-1.0` および `2.0`.

![視差の背景設定](./assets/pb-settings-parallax-background.png){width="600" zoomable="yes"}

## 詳細

- 行に追加されるコンテンツコンテナの水平方向の位置を制御するには、 **[!UICONTROL Alignment]**:

  | オプション | 説明 |
  | ------ | ----------- |
  | `Default` | 現在のテーマのスタイルシートで指定された位置揃えの既定の設定を適用します。 |
  | `Left` | コンテンツコンテナを行コンテナの左の境界線に沿って揃えます。指定されたパディングに適した値になります。 |
  | `Center` | コンテンツコンテナを行コンテナの中央に揃えます。指定されたパディングの分だけを使用します。 |
  | `Right` | コンテンツコンテナを行コンテナの右側の境界線に沿って揃えます。指定されたパディングの分だけを使用します。 |

  {style="table-layout:auto"}

- を設定します。 **[!UICONTROL Border]** 行コンテナの 4 つの側面すべてに適用されるスタイル：

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

  ![境界線のカラー](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | オプション | 説明 |
  | ------ |------------ |
  | [!UICONTROL Border Color] | スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進値を入力して、カラーを指定します。 |
  | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
  | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各隅を囲むために使用する半径のサイズを定義します。 |

  {style="table-layout:auto"}

  次の例の行の境界線の半径は 15 です。

  ![境界線の半径が 15 の行](./assets/pb-settings-border-radius-15.png){width="500"}

- （オプション） **[!UICONTROL CSS classes]** を現在のスタイルシートから行コンテナに適用します。

  複数のクラス名はスペースで区切ります。

- 次の値をピクセル単位で入力します。 **[!UICONTROL Margins and Padding]** をクリックして、行の外側の余白と内側の余白を指定します。

  行コンテナ図で、対応する各値を入力します。

  | コンテナ領域 | 説明 |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
  | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |

  {style="table-layout:auto"}

  ![余白とパディング](./assets/pb-layout-row-settings-margin-padding-default.png){width="600" zoomable="yes"}
