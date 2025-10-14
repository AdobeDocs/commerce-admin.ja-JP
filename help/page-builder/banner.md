---
title: メディア – バナー
description: ステージにイラストで表示されたインタラクティブコンポーネントを追加する際に使用するバナーコンテンツタ  [!DNL Page Builder]  プについて説明します。
exl-id: 287d866c-8a63-4531-8c1b-40d560a07947
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '2302'
ht-degree: 0%

---

# メディア – バナー

_バナー_ コンテンツタイプを使用して、[[!DNL Page Builder]  ステージ &#x200B;](workspace.md#stage) のcall to actionとボタンでユーザーを引きつけるイラスト付きのインタラクティブコンポーネントを追加します。

>[!NOTE]
>
>以前はコンテンツメニューの _バナー_ オプションでしたが、現在は [&#x200B; 動的ブロック &#x200B;](../content-design/dynamic-blocks.md) になっています。

![&#x200B; ストアフロントのホームページのバナー &#x200B;](./assets/pb-banner-homepage.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## バナーツールボックス

バナーツールボックスは、バナーコンテナにカーソルを合わせると表示されます。

![&#x200B; バナーツールボックス &#x200B;](./assets/pb-tutorial1-banner-toolbox.png){width="600" zoomable="yes"}

| ツール | アイコン | 説明 |
|--- |--- |--- |
| 移動 | ![&#x200B; 移動アイコン &#x200B;](./assets/pb-icon-move.png){width="25"} | バナーをステージ上の別の位置に移動します。 |
| （ラベル） | バナー | 現在のコンテンツコンテナをバナーとして識別します。 コンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="25"} | バナーを編集ページを開きます。このページで、バナーとコンテナのプロパティを変更できます。 |
| Hide | ![&#x200B; アイコンを非表示 &#x200B;](./assets/pb-icon-hide.png){width="25"} | 現在のバナーを非表示にします。 |
| 表示 | ![&#x200B; アイコンを表示 &#x200B;](./assets/pb-icon-show.png){width="25"} | 非表示のバナーを表示します。 |
| 複製 | ![&#x200B; 複製アイコン &#x200B;](./assets/pb-icon-duplicate.png){width="25"} | バナーをコピーします。 |
| 削除 | ![&#x200B; 削除アイコン &#x200B;](./assets/pb-icon-remove.png){width="25"} | ステージからバナーを削除します。 |
| [!UICONTROL Upload New Image] |  | バナーの背景用に、ローカルファイルシステムからギャラリーに画像をアップロードします。 |
| [!UICONTROL Select from Gallery] |  | バナーの背景にギャラリーの既存の画像を使用します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## バナーを追加

1. [!DNL Page Builder] パネルで **[!UICONTROL Media]** を展開し、**[!UICONTROL Banner]** プレースホルダーをステージにドラッグします。

   ![&#x200B; バナーコンテンツタイプのステージへのドラッグ &#x200B;](./assets/pb-tutorial1-banner-drag-to-stage.png){width="600" zoomable="yes"}

   _[!UICONTROL Upload Image]_&#x200B;ボタンと&#x200B;_[!UICONTROL Select from Gallery]_ ボタンが含まれているので、ステージから直接バナーコンテンツをすばやく変更できます。 _[!UICONTROL Edit Banner]_&#x200B;ページのコンテンツを変更することもできます。

1. バナープレースホルダー内をクリックして [&#x200B; テキストエディター &#x200B;](../content-design/editor.md) を表示し、バナーのコンテンツを入力します。

   [&#x200B; コンテンツ &#x200B;](#content) 設定を使用して、より複雑なバナーコンテンツを含めることもできます。

## バナー設定の変更

1. バナーコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png)）アイコンを選択します。

1. 使用可能な設定の更新について詳しくは、次の節を参照してください。

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Advanced]](#advanced)

1. 完了したら、右上隅の「**[!UICONTROL Save]**」をクリックして、_[!UICONTROL Edit Banner]_&#x200B;ページを閉じます。

1. 右上隅にある「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

## [!UICONTROL Appearance]

バナーは、4 つの定義済みテンプレートのいずれかに基づいているので、設定と管理が簡単です。

- 次のいずれかのバナー配置タイプを選択します。

  | プレースメント | 説明 |
  | --------- | ----------- |
  | [!UICONTROL Poster] | コンテンツとボタンをバナーの中央に配置します。 オーバーレイを使用すると、バナーの全幅が拡張されます。 |
  | [!UICONTROL Collage Left] | バナーの左側の定義済み領域に、コンテンツとボタンを配置します。 オーバーレイを使用すると、定義した領域のみがオーバーレイ対象になります。 |
  | [!UICONTROL Collage Center] | バナーの中央にある定義済みの領域にコンテンツとボタンを配置します。 オーバーレイを使用すると、定義した領域のみがオーバーレイ対象になります。 |
  | [!UICONTROL Collage Right] | バナーの右側の定義済み領域にコンテンツとボタンを配置します。 オーバーレイを使用すると、定義した領域のみがオーバーレイ対象になります。 |

  {style="table-layout:auto"}

  ![&#x200B; 外観 – 右のコラージュ &#x200B;](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

- （オプション）行の **[!UICONTROL Minimum Height]** を入力します。

  最小の高さは、有効な CSS 単位（`100px`、`50%`、`50em`、`100vh` など）または計算（`100vh - 237px` など）を含む数値です。

  例えば、バナーの最小の高さを設定して、ページの完全な高さを引き伸ばすことができ、完全なページの背景画像やビデオに対して魅力的なオプションを提供できます。

## [!UICONTROL Background]

バナーの背景表示を定義するオプションは多数あります。 シンプルなカラーまたは背景画像を適用し、より高度な効果を管理できます。

### [!UICONTROL Background Color]

スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、背景色を指定します。 この設定により、行の背景色が決まります。 また、カラーの不透明度を調整することもできます。

![&#x200B; 色なし（デフォルト） &#x200B;](./assets/pb-settings-background-color-no-color.png){width="200"}

次の 3 つの方法のいずれかで値を設定できます。

- 定義済みのカラー名（`White` など）
- カラーの 16 進数カラー値（例：`#ffffff`）
- カラーの rgba 値（不透明度の割合）（`rgba(255, 255, 255, 0.75)` など）。

カラーを選択する場合は、「カラーなし _ボックスの左側にあるスウォッチをクリックし_ す。

![&#x200B; カラースウォッチの選択 &#x200B;](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

カラーボックスをクリックして再度カラーピッカーを開くと、スライダの下のボックスに現在の赤、緑、青、アルファ値（rgba）が表示されます。 最後の数値は、現在の不透明度の割合を小数で示します。 スライダを使用して、不透明度を調整したり、必要な小数値を入力したりできます。

![&#x200B; 不透明度の設定 &#x200B;](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] では、背景画像に透明度レイヤー（_アルファチャンネル_ を含めることもできます。このレイヤーを使用して、様々な不透明度の背景を作成できます。

### [!UICONTROL Background Type]

背景の種類は、画像またはビデオです。 デフォルト [!DNL Page Builder]`Image` で、様々な画像設定が表示されます。 `Video` を選択すると、[!DNL Page Builder] は画像設定をビデオ設定にスワップします。 両方の背景タイプの設定について、次の節で説明します。

![&#x200B; 背景の種類 &#x200B;](./assets/pb-background-type.png){width="200"}

### 画像タイプの設定

_背景の種類_ を `Image` に設定する場合、次の設定を使用して背景画像の表示を定義します。

![&#x200B; 背景画像付きバナー &#x200B;](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** – 必要に応じて、用意されているツールを使用してバナーに適用する背景画像を選択します。

  | ツール | 説明 |
  | ---- | ----------- |
  | [!UICONTROL Upload] | ローカルコンピューターからギャラリーに画像ファイルをアップロードし、それをバナーの背景画像として適用します。 |
  | [!UICONTROL Select from Gallery] | バナーの背景画像として、ギャラリーから既存の画像を選択するように求めるプロンプトを表示します。 |
  | ![&#x200B; カメラアイコン &#x200B;](./assets/pb-icon-camera.png){width="25"} | 画像をカメラタイルにドラッグするか、ローカルファイルシステム内の画像を参照できます。 |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** – 必要に応じて、同じツールを使用して、モバイルデバイスでの表示に使用する別の背景画像を選択します。

- **[!UICONTROL Background Size]** – このオプションを設定して、バナーの幅に対する背景画像の拡大縮小を指定します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Cover` | 背景画像はバナーの全幅をカバーしています。 |
  | `Contain` | 背景画像は、コンテンツ領域の幅に制限されます。 |
  | `Auto` | 現在のスタイル シートからサイズを適用します。 |

  {style="table-layout:auto"}

  ![&#x200B; 背景サイズ &#x200B;](./assets/pb-layout-row-settings-background-size-cover.png){width="200"}

- **[!UICONTROL Background Position]** – このオプションを設定して、背景画像をバナーに対してどのように固定するかを指定します。

  | アンカー | 位置 |
  | ------ | ----------- |
  | `Top` | 左/中央/右 |
  | `Center` | 左/中央/右 |
  | `Bottom` | 左/中央/右 |

  {style="table-layout:auto"}

  アンカーポイントは、プッシュピンのようなもので、指定した背景位置で画像をバナーにアタッチします。

- **[!UICONTROL Background Attachment]** – 添付ファイルタイプを設定して、スクロールするページに対する背景画像の移動を指定します。

  | オプション | 説明 |
  | ------ | ----------- |
  | `Scroll` | 添付された背景画像は、ページがスクロールすると下に移動するように同期されます。 |
  | `Fixed` | （モバイルでは使用できません）コンテナが画像の上をスクロールし、指定された背景位置に固定されるので、背景画像は移動しません。 |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** – 背景画像を繰り返してスペースを埋める場合は、この設定 `Yes` を変更します。

### ビデオタイプの設定

_[!UICONTROL Background Type]_&#x200B;を `Video` に設定した場合は、次の設定を使用して背景画像の表示を定義します。

- **[!UICONTROL Video URL]** – 有効なビデオ URL を入力します。 有効なビデオ URL は、次へのリンクです。

   - YouTube ビデオ：`https://youtu.be/CoDhMRUUjeI`
   - Vimeo ビデオ：`https://vimeo.com/190156113`
   - 有効なビデオ ファイル （`.mp4` を推奨）: `https://myvideos.com/spiral.mp4`

  ![&#x200B; 背景ビデオの URL](./assets/pb-video-url.png){width="200"}

- **[!UICONTROL Overlay Color]** - ビデオに透明の濃淡を適用するカラーを選択します。

- **[!UICONTROL Infinite Loop]** - `No` に設定すると、ビデオを 1 回再生して停止します。 `Yes` （デフォルト）に設定すると、ビデオは無限ループで繰り返されます。

- **[!UICONTROL Lazy Load]** - `No` に設定すると、非表示の場合でもビデオがページと共に読み込まれます。 `Yes` （デフォルト）に設定されている場合、ビデオは画面に表示されているときにのみソースから読み込まれます。

- **[!UICONTROL Play Only When Visible]** - ビデオが表示されているかどうかに関係なく、ビデオの読み込み直後に再生を開始するには、`No` に設定します。 `Yes` （デフォルト）に設定されている場合、ビデオは表示されているときにのみ再生を開始します。

- **[!UICONTROL Fallback Image]** – 必要に応じて、ビデオが読み込まれる前および何らかの理由でビデオが読み込まれない場合に画面に表示する画像を指定します。

## [!UICONTROL Content]

バナーコンテンツは、ステージ上で直接変更することも、設定を変更する場合に変更することもできます。 設定では、バナーリンク、ボタン、オーバーレイなど、より複雑なコンテンツ機能が提供されます。 コンテンツの位置は、[&#x200B; アピアランス &#x200B;](#appearance) の配置設定を反映します。

### ステージ上のシンプルなコンテンツ

1. プレースホルダーテキストをクリックし、バナーに表示するテキストを入力します。

   テキストボックスの上にエディターツールバーが表示されます。

   ![&#x200B; ステージ上でのコンテンツの編集 &#x200B;](./assets/pb-tutorial1-banner-stage-text.png){width="600" zoomable="yes"}

1. エディターツールバーを使用して、テキストの入力や書式設定のほか、リンク、画像、ウィジェットなどの要素を挿入します。

   ![&#x200B; 書式設定されたテキストを使用したステージ &#x200B;](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="600" zoomable="yes"}

### 設定の複雑なコンテンツ

1. バナーコンテナの上にマウスポインターを置くと、ツールボックスが表示されます。次に、_設定_ （![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="25"}）アイコンを選択します。

1. 「_[!UICONTROL Content]_」セクションまでスクロールし、**[!UICONTROL Message Text]**&#x200B;エディターを使用してバナーテキストを入力および書式設定します。

   テキストリンク、画像、ウィジェットなどの要素を挿入することもできます。

   ![&#x200B; メッセージテキストエディター &#x200B;](./assets/pb-tutorial1-banner-settings-content-message-text.png){width="600" zoomable="yes"}

1. 必要に応じて、バナー **[!UICONTROL Link]** を指定します。

   リンクは、顧客がバナーボタンまたは領域をクリックすると表示される宛先ページです。 次の 3 つのリンクタイプのいずれかを使用できます。

   - **[!UICONTROL URL]** – 相対 URL または完全修飾 URL へのリンク。
   - **[!UICONTROL Product]** – 製品名または SKU に基づいて宛先ページを識別します。 部分的または完全な名前に基づいて、名前で製品を検索します。 検索結果リストから製品を選択します。
   - **[!UICONTROL Category]** - カテゴリツリー内の特定のカテゴリまたはサブカテゴリとして宛先ページを識別します。 名前の一部または全部に基づいてカテゴリを検索します。 表示されたツリーの展開セクションからカテゴリを選択します。
   - **[!UICONTROL Page]** – 宛先ページを特定のコンテンツページとして識別します。 名前の一部または全部に基づいてページを検索します。 検索結果リストからページを選択します。

   >[!NOTE]
   >
   >2.4.1 リリース以降、ストアフロントの表示に関する問題により、[!DNL Page Builder] はバナーとネストされたテキスト内のリンクのリンクをサポートしなくなりました。 _[!UICONTROL Message Text]_&#x200B;でリンクを使用している場合、「_[!UICONTROL Link]_」オプションを設定することはできません。 バナー全体に 1 つのリンクを使用する場合は、テキストからすべてのリンクを削除できます。<br/>
   >
   >![&#x200B; リンク設定がブロックされています &#x200B;](./assets/pb-nested-link-blocked.png){width="200"}


1. 必要に応じて、リンクをたどるように顧客に促すボタンを追加します。

   バナーの外観を設定すると、テキストの下に 1 つのリンクまたはボタンが配置されます。 追加するリンクまたはボタンのプロパティを入力します。

   ![&#x200B; テキストおよびボタン（またはリンク）を使用した外観 &#x200B;](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >バナーに [&#x200B; ブロック &#x200B;](block.md) を追加して、複数のボタンやリンクを使用することもできます。 競合を避けるために、すべてのリンクまたはボタンを個別のブロックに保持し、リンクまたはボタンをバナーに直接追加しないでください。

   - **[!UICONTROL Show Button]** を次のいずれかに設定します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Always` | ボタンは常にバナーに表示されます。 |
     | `On Hover` | ボタンは、マウスポインターを置いたときにのみバナーに表示されます。 |
     | `Never Show` | ボタンがバナーに表示されない。 |

     {style="table-layout:auto"}

   - ボタンに表示する **[!UICONTROL Button Text]** を入力します。

   - **[!UICONTROL Button Type]** を次のいずれかに設定します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Primary` | 現在のスタイル シートからプライマリ ボタン スタイルを適用します。 |
     | `Secondary` | 現在のスタイル シートからセカンダリ ボタン スタイルを適用します（該当する場合）。 |
     | `Link` | ボタンではなくハイパーリンクを作成します。 |

     {style="table-layout:auto"}

     現在のテーマのボタンのスタイルによって、ボタンの形式が決まります。 通常、プライマリボタンの背景色は、セカンダリボタンの背景色よりも目立ちます。

1. **[!UICONTROL Show Overlay]** を次のいずれかに設定します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Always` | オーバーレイは常に表示されます。 |
   | `On Hover` | オーバーレイは、カーソルを合わせたときにのみ表示されます。 |
   | `Never Show` | オーバーレイが表示されません。 |

   {style="table-layout:auto"}

   オーバーレイを使用して、[!UICONTROL Appearance] 設定で定義されたアクティブなコンテンツ領域に背景色を適用することができます。 バナーの背景画像は、バナーの全幅に対して表示されたままになります。

   オーバーレイの表示を選択した場合は、**[!UICONTROL Overlay Color]** を設定します。

   - **カラーなし** スウォッチをクリックし、スウォッチを選択します。
   - **カラーなし** フィールドに、有効なカラー名または 16 進数値を入力します。

   ![&#x200B; オーバーレイカラー &#x200B;](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}

1. 右上隅にある「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

   ![&#x200B; テキストメッセージとボタンを含むバナー &#x200B;](./assets/pb-tutorial1-banner-stage-background-color.png){width="600" zoomable="yes"}


## [!UICONTROL Search Engine Optimization] {#seo}

これらの設定のテキストは、検索エンジンに表示され、ページのインデックス作成方法が改善されます。

- **[!UICONTROL Alternative Text]** しくは、表示するデジタルアクセシビリティツールの _alt_ テキストの説明を入力します。

  代替テキストの使用は、アクセシビリティのベストプラクティスであり、一部のロケールでは法律で義務付けられています。 HTMLでは、`alt` 属性は `image` タグのサブセットです（`<image title="tooltip" alt="description" src="image.jpg">`）。

- **[!UICONTROL Title Attribute]**：マウスオーバーしたときにツールヒントとして表示するテキストを入力します。

  ベストプラクティスとして、説明的でキーワードの多いタイトルを選択すると、検索エンジンによる画像のインデックス作成方法が改善されます。 HTMLでは、`title` 属性は `image` タグのサブセットです（`<image title="tooltip" alt="description" src="image.jpg">`）。

## [!UICONTROL Advanced]

1. バナーに追加されるコンテンツコンテナの水平方向の位置を制御するには、**[!UICONTROL Alignment]** のいずれかを選択します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
   | `Left` | 指定したパディングを許可して、バナーコンテナの左境界線に沿ってコンテンツコンテナを揃えます。 |
   | `Center` | コンテンツコンテナをバナーコンテナの中央に揃え、指定したパディングを許容します。 |
   | `Right` | 指定したパディングを考慮して、コンテンツコンテナをバナーコンテナの右端に沿って配置します。 |

   {style="table-layout:auto"}

1. バナーコンテナの 4 つの側面すべてに適用する **[!UICONTROL Border]** スタイルを設定します。

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

1. `None` 以外の境界線のスタイルを設定する場合は、境界線の表示オプションを完了します。

   - **[!UICONTROL Border Color]** - カラーを指定するには、見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力します。

     ![&#x200B; 境界線のカラー &#x200B;](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

   - **[!UICONTROL Border Width]** – 境界線の幅のピクセル数を入力します。

   - **[!UICONTROL Border Radius]** – 境界線の各コーナーを丸めるために使用する半径のサイズを定義するピクセル数を入力します。

1. （オプション）バナーコンテナに適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

   複数のクラス名はスペースで区切ります。

1. バナーの外側の余白と内側のパディングを指定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

   対応する各値をバナーコンテナ図に入力します。

   | オプション | 説明 |
   | ------ | ----------- |
   | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 |
   | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 |

   {style="table-layout:auto"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
