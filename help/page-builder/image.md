---
title: メディア – 画像
description: にJPG、GIF、PNG 画像を追加するために使用される画像コンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 0%

---

# メディア – 画像

の使用 _画像_ にJPG、GIF、または PNG 画像を追加するためのコンテンツタイプ [[!DNL Page Builder] ステージ](workspace.md#stage). デフォルトのデスクトップイメージに加えて、モバイルデバイス用のセカンダリイメージを指定できます。 画像の下に表示されるキャプションを追加し、画像を任意の URL、製品、カテゴリまたはページにリンクすることもできます。

>[!TIP]
>
>を使用できます [Adobe Stockの統合](../content-design/adobe-stock.md) 提供される数百万のアセットの中から適切なアセットを見つけて保存するには、次の手順に従います [Adobe Stock](https://stock.adobe.com). 参照： [Adobe Stock画像の使用](../content-design/adobe-stock-manage.md) Adobe Stock アセットを検索、調整およびギャラリーに保存する方法について詳しくは、こちらを参照してください。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 画像ツールボックス

画像コンテナにカーソルを合わせると、画像ツールボックスが表示されます。

![画像ツールボックス](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
|--- |--- |--- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 画像をステージ上の別の位置に移動します。 |
| （ラベル） | 画像 | 現在のコンテンツコンテナを画像として識別します。 画像コンテナにカーソルを合わせると、ツールボックスが表示されます。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | を開きます _画像を編集_ このページで、画像とコンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在の画像を非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示の画像を表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | 画像のコピーを作成します。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | ステージから画像を削除します。 |
| 新しい画像をアップロード |  | ローカルファイルシステムからギャラリーに画像をアップロードします。 |
| ギャラリーから選択 |  | ギャラリーから既存の画像を選択します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 画像を追加

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Media]** をドラッグして **[!UICONTROL Image]** ターゲットコンテナへのプレースホルダー。

   行、列、タブに画像を追加できます。 次の例では、画像を空の列にドラッグします。

   ![画像コンテンツタイプのステージへのドラッグ](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. 次のいずれかの方法を使用して画像アセットを追加します。

   ![画像をアップロードするか、ステージ上のギャラリーツールから選択](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >最大ファイルサイズは 4 MB です。 サポートされているファイルタイプは、JPG、GIF、PNG です。

   - _**新しい画像をアップロード**_：この方法を使用して、システムから新しい画像ファイルをアップロードします。

      - クリック **[!UICONTROL Upload Image]**.

      - 画像を見つけて選択し、ギャラリーとターゲットコンテナに追加します。

     または、画像ファイルをシステムからドラッグして、 _カメラ_ （ ![カメラ アイコン](./assets/pb-icon-camera.png){width="20"} ） アイコンをクリックします。

   - _**既存のアセットを選択**_：メディアストレージ/ギャラリーから既存の画像アセットを選択するには、この方法を使用します。

      - クリック **[!UICONTROL Select from Gallery]**.

      - ツリーを使用して画像に移動します。

      - サムネールをクリックし、 **[!UICONTROL Add Selected]**.

        ![選択した画像の追加](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _**Adobe Stock画像を検索して選択します**_:Adobe Stock内から画像を検索する場合に使用します。

     >[!NOTE]
     >
     >このメソッドには、 [Adobe Stockの統合](../content-design/adobe-stock.md) が管理者用に設定されています。

      - クリック **[!UICONTROL Search Adobe Stock]** で画像を検索します。

      - プレビューまたはライセンス済み画像をギャラリーに保存します。

        参照： [Adobe Stock画像の使用](../content-design/adobe-stock-manage.md) Adobe Stock assets の操作の詳細情報。

      - ギャラリーでアセットサムネールを選択し、をクリックします。 **[!UICONTROL Add Selected]**.

   画像がターゲットコンテナのプレースホルダーの場所に表示されます。 背景画像とは異なり、画像を現在のコンテナ内の別の位置に移動したり、別のコンテナに移動したりできます。

   >[!NOTE]
   >
   >この [バナー](banner.md) および [Slider](slider.md) コンテンツタイプには以下も含まれます _画像をアップロード_ および _ギャラリーから選択_ 画像を追加するためのオプション。

   ![列内の画像](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## 画像設定の変更

1. 画像コンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。
ファイル名、サイズ、およびファイルサイズが現在の画像の下に表示されます。

   ![現在の画像](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. 現在のを変更するには **[!UICONTROL Image]**&#x200B;次のいずれかの操作をおこないます。

   - _**新しい画像をアップロード**_：この方法を使用して、システムから新しい画像ファイルをアップロードします。

      - クリック **[!UICONTROL Upload Image]**.

      - 画像を見つけて選択し、ギャラリーとターゲットコンテナに追加します。

   - _**既存のアセットを選択**_：メディアストレージ/ギャラリーから既存の画像アセットを選択するには、この方法を使用します。

      - クリック **[!UICONTROL Select from Gallery]**.

      - ツリーを使用して画像に移動します。

      - サムネールをクリックし、 **[!UICONTROL Add Selected]**.

        ![選択した画像の追加](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Adobe Stock画像を検索して選択します**:Adobe Stock内から画像を検索する場合に使用します。

     >[!NOTE]
     >
     >このメソッドには、 [Adobe Stockの統合](../content-design/adobe-stock.md) が管理者用に設定されています。

      - クリック **[!UICONTROL Search Adobe Stock]** で画像を検索します。

      - プレビューまたはライセンス済み画像をギャラリーに保存します。

        参照： [Adobe Stock画像の使用](../content-design/adobe-stock-manage.md) Adobe Stock assets の操作の詳細情報。

      - ギャラリーでアセットサムネールを選択し、をクリックします。 **[!UICONTROL Add Selected]**.

1. を追加します **[!UICONTROL Mobile Image]**、前の手順で説明したのと同じ方法を使用して、モバイルデバイスでの表示に使用する画像を選択します。

   ![モバイル画像](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. 必要に応じて、 **[!UICONTROL Link]** 画像の。

   リンクは、顧客が画像をクリックすると表示される宛先ページです。 次の 3 つのリンクタイプのいずれかを使用できます。

   - **[!UICONTROL URL]**  – 相対 URL または完全修飾 URL へのリンク。

   - **[!UICONTROL Product]**  – 製品名または SKU に基づいて宛先ページを識別します。 部分的または完全な名前に基づいて、名前で製品を検索します。 検索結果リストから製品を選択します。

     ![リンクする製品の選択](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]**  – 宛先ページをカテゴリツリー内の特定のカテゴリまたはサブカテゴリとして識別します。 名前の一部または全部に基づいてカテゴリを検索します。 表示されたツリーの展開セクションからカテゴリを選択します。

     ![リンクするカテゴリの選択](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]**  – 宛先ページを特定のコンテンツページとして識別します。 名前の一部または全部に基づいてページを検索します。 検索結果リストからページを選択します。

     ![リンクするページの選択](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   訪問者がストアから移動できないようにするには、 **[!UICONTROL Open in new tab]** チェックボックス。 このチェックボックスをオフにすると、リンクされた宛先は同じブラウザータブで開くので、訪問者をストアから効果的に移動できます。

1. を追加します **[!UICONTROL Image Caption]**&#x200B;で、画像の下に表示するテキストを入力します。

   キャプションの形式は、現在のテーマに関連付けられているスタイルシートによって決まります。

   通常、キャプションは画像の下に表示され、訪問者や検索エンジンに画像に関する情報を提供します。 サイトが複数の言語で使用可能な場合は、同じ画像を使用しても、キャプションは翻訳できます。 HTMLでは、 `<figcaption>` タグが `<figure>` タグ。 `<figcaption>This is the image caption</figcaption>`

1. 必要に応じて、その他の設定を更新します。

   - [検索エンジンの最適化](#search-engine-optimization)
   - [詳細](#advanced)

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

## 画像の移動

1. 画像コンテナにカーソルを合わせてツールボックスを表示し、 _移動_ （![移動アイコン](./assets/pb-icon-move.png){width="20"} ） アイコンをクリックします。

   ![画像の移動](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. 画像を選択して、赤いガイドラインのすぐ下の新しい位置にドラッグします。

   ![赤いガイドラインを使用した画像の配置](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## 画像を削除

1. 画像コンテナにカーソルを合わせてツールボックスを表示し、 _削除_ （ ![アイコンを削除](./assets/pb-icon-remove.png){width="20"} ） アイコンをクリックします。

1. 確認を求められたら、 **[!UICONTROL OK]**.

## 検索エンジンの最適化

これらの設定のテキストは、検索エンジンに表示され、ページのインデックス作成方法が改善されます。

- の場合 **[!UICONTROL Alternative Text]**、を入力 _alt_ 表示するデジタルアクセシビリティツールのテキスト説明。

  代替テキストの使用は、アクセシビリティのベストプラクティスであり、一部のロケールでは法律で義務付けられています。 HTMLでは、 `alt` attribute は、のサブセットです。 `image` タグ : `<image title="tooltip" alt="description" src="image.jpg">`.

- の場合 **[!UICONTROL Title Attribute]**&#x200B;マウスオーバーしたときにツールヒントとして表示するテキストを入力します。

  ベストプラクティスとして、説明的でキーワードの多いタイトルを選択すると、検索エンジンによる画像のインデックス作成方法が改善されます。 HTMLでは、 `title` attribute は、のサブセットです。 `image` タグ : `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- コンテナに追加される画像の水平方向の位置を制御するには、 **[!UICONTROL Alignment]**.

  | オプション | 説明 |
  | ------ | ----------- |
  | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
  | `Left` | 指定したパディングを考慮して、画像コンテナの左境界線に沿って画像コンテンツを配置します。 |
  | `Center` | 指定したパディングを許可して、画像コンテナの中央に画像コンテンツを揃えます。 |
  | `Right` | 指定したパディングを考慮して、画像コンテナの右端に沿って画像コンテンツを配置します。 |

  {style="table-layout:auto"}

- を **[!UICONTROL Border]** 画像コンテナの 4 つの辺すべてに適用されるスタイル：

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

- （オプション）の名前を指定します **[!UICONTROL CSS classes]** 画像コンテナに適用する現在のスタイルシートから。

  複数のクラス名はスペースで区切ります。

- 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** 画像コンテナの外側の余白と内側のパディングを指定します。

  対応する各値を画像コンテナ図に入力します。

  | コンテナ領域 | 説明 |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 |
  | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 |

  {style="table-layout:auto"}
