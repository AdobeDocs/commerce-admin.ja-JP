---
title: メディア — 画像
description: 画像、GIF、または PNG の画像を [!DNL Page Builder] ステージ。
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# メディア — 画像

以下を使用します。 _画像_ JPG、GIFまたは PNG 画像を [[!DNL Page Builder] ステージ](workspace.md#stage). デフォルトのデスクトップイメージに加えて、モバイルデバイス用のセカンダリイメージを指定できます。 また、画像の下に表示されるキャプションを追加して、画像を URL、製品、カテゴリまたはページにリンクすることもできます。

>[!TIP]
>
>以下を使用すると、 [Adobe Stock統合](../content-design/adobe-stock.md) ～が提供する百万人の中から適切な資産を見つけて保存する [Adobe Stock](https://stock.adobe.com). 詳しくは、 [Adobe Stock Images の使用](../content-design/adobe-stock-manage.md) を参照して、Adobe Stockのアセットを検索、絞り込み、ギャラリーに保存する方法について詳しく説明します。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 画像ツールボックス

画像コンテナの上にマウスポインターを置くと、画像ツールボックスが表示されます。

![画像ツールボックス](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
|--- |--- |--- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 画像をステージ上の別の位置に移動します。 |
| （ラベル） | 画像 | 現在のコンテンツコンテナを画像として識別します。 画像コンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | を開きます。 _画像を編集_ ページに表示されます。このページで、画像とコンテナのプロパティを変更できます。 |
| 非表示 | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在の画像を非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 隠し画像を表示します。 |
| 複製 | ![複製アイコン](./assets/pb-icon-duplicate.png){width="25"} | 画像のコピーを作成します。 |
| 削除 | ![削除アイコン](./assets/pb-icon-remove.png){width="25"} | ステージから画像を削除します。 |
| 新しい画像をアップロード |  | ローカルファイルシステムからギャラリーに画像をアップロードします。 |
| ギャラリーから選択 |  | ギャラリーから既存の画像を選択します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 画像を追加

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Media]** をクリックし、 **[!UICONTROL Image]** プレースホルダーをターゲットコンテナに追加します。

   画像を行、列またはタブに追加できます。 次の例では、画像は空の列にドラッグされます。

   ![画像コンテンツタイプのステージへのドラッグ](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. 次のいずれかの方法を使用して、画像アセットを追加します。

   ![ステージ上のギャラリーツールから画像をアップロードまたは選択](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >最大ファイルサイズは 4 MB です。 サポートされるファイルタイプは、JPG、GIF、PNG です。

   - _**新しい画像をアップロード**_：この方法を使用して、新しい画像ファイルをシステムからアップロードします。

      - クリック **[!UICONTROL Upload Image]**.

      - 画像を探して選択し、ギャラリーとターゲットのコンテナに追加します。

     別の方法として、システムから画像ファイルをドラッグし、 _カメラ_ ( ![カメラアイコン](./assets/pb-icon-camera.png){width="20"} ) アイコンをクリックします。

   - _**既存のアセットを選択**_：このメソッドを使用して、メディアストレージ/ギャラリーから既存の画像アセットを選択します。

      - クリック **[!UICONTROL Select from Gallery]**.

      - ツリーを使用して画像に移動します。

      - サムネールをクリックし、 **[!UICONTROL Add Selected]**.

        ![選択した画像の追加](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _**Adobe Stock画像を検索して選択**_：このメソッドを使用して、Adobe Stockから画像を検索します。

     >[!NOTE]
     >
     >このメソッドには、 [Adobe Stock統合](../content-design/adobe-stock.md) 管理者に設定されている必要があります。

      - クリック **[!UICONTROL Search Adobe Stock]** 画像を検索します。

      - プレビューまたはライセンスが必要な画像をギャラリーに保存します。

        詳しくは、 [Adobe Stock Images の使用](../content-design/adobe-stock-manage.md) Adobe Stock assets の操作について詳しくは、

      - ギャラリーでアセットのサムネールを選択し、 **[!UICONTROL Add Selected]**.

   ターゲットコンテナのプレースホルダーの場所に画像が表示されます。 背景画像とは異なり、画像を現在のコンテナ内の別の位置に移動したり、別のコンテナに移動したりできます。

   >[!NOTE]
   >
   >The [バナー](banner.md) および [スライダー](slider.md) コンテンツタイプには次も含まれます _画像をアップロード_ および _ギャラリーから選択_ 画像を追加するためのオプション。

   ![列内の画像](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## 画像設定の変更

1. 画像コンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ (![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。
ファイル名、サイズ、およびファイルサイズは、現在の画像の下に表示されます。

   ![現在の画像](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. 現在の **[!UICONTROL Image]**、次のいずれかの操作を行います。

   - _**新しい画像をアップロード**_：この方法を使用して、新しい画像ファイルをシステムからアップロードします。

      - クリック **[!UICONTROL Upload Image]**.

      - 画像を探して選択し、ギャラリーとターゲットのコンテナに追加します。

   - _**既存のアセットを選択**_：このメソッドを使用して、メディアストレージ/ギャラリーから既存の画像アセットを選択します。

      - クリック **[!UICONTROL Select from Gallery]**.

      - ツリーを使用して画像に移動します。

      - サムネールをクリックし、 **[!UICONTROL Add Selected]**.

        ![選択した画像の追加](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Adobe Stock画像を検索して選択**：このメソッドを使用して、Adobe Stockから画像を検索します。

     >[!NOTE]
     >
     >このメソッドには、 [Adobe Stock統合](../content-design/adobe-stock.md) 管理者に設定されている必要があります。

      - クリック **[!UICONTROL Search Adobe Stock]** 画像を検索します。

      - プレビューまたはライセンスが必要な画像をギャラリーに保存します。

        詳しくは、 [Adobe Stock Images の使用](../content-design/adobe-stock-manage.md) Adobe Stock assets の操作について詳しくは、

      - ギャラリーでアセットのサムネールを選択し、 **[!UICONTROL Add Selected]**.

1. を追加するには、以下を実行します。 **[!UICONTROL Mobile Image]**&#x200B;の場合は、前の手順と同じ方法を使用して、モバイルデバイスでの表示に使用する画像を選択します。

   ![モバイル画像](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. 必要に応じて、 **[!UICONTROL Link]** 画像の。

   リンクとは、顧客が画像をクリックすると表示される宛先ページです。 次の 3 つのリンクタイプのいずれかを使用できます。

   - **[!UICONTROL URL]**  — 相対 URL または完全修飾 URL へのリンク。

   - **[!UICONTROL Product]**  — 製品名または SKU に基づいて宛先ページを識別します。 部分的または完全な名前に基づいて、製品を名前で検索します。 検索結果のリストから製品を選択します。

     ![リンクする製品の選択](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]**  — リンク先のページを、カテゴリツリー内の特定のカテゴリまたはサブカテゴリとして識別します。 名前の一部または完全に一致するものに基づいてカテゴリを検索します。 表示されたツリーの展開済みのセクションからカテゴリを選択します。

     ![リンクするカテゴリの選択](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]**  — リンク先のページを特定のコンテンツページとして識別します。 名前の一部または完全などに基づいてページを検索します。 検索結果のリストからページを選択します。

     ![リンクするページの選択](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   訪問者がストアから離れないようにするには、 **[!UICONTROL Open in new tab]** チェックボックス。 このチェックボックスをオフにすると、リンクされた宛先が同じブラウザータブで開き、訪問者を効果的にストアから移動できます。

1. 次の手順で **[!UICONTROL Image Caption]**&#x200B;に設定し、画像の下に表示するテキストを入力します。

   キャプションの形式は、現在のテーマに関連付けられているスタイルシートによって決まります。

   キャプションは通常、画像の下に表示され、訪問者と検索エンジンに関する画像に関する情報を提供します。 サイトが複数の言語で利用できる場合は、同じ画像を使用し、キャプションを翻訳します。 HTMLでは、 `<figcaption>` タグは、 `<figure>` タグを使用します。 `<figcaption>This is the image caption</figcaption>`

1. 必要に応じて、その他の設定を更新します。

   - [検索エンジンの最適化](#search-engine-optimization)
   - [詳細](#advanced)

1. 完了したら、「 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。

## 画像の移動

1. 画像コンテナの上にマウスポインターを置いてツールボックスを表示し、 _移動_ (![移動アイコン](./assets/pb-icon-move.png){width="20"} ) アイコンをクリックします。

   ![画像の移動](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. 画像を選択し、赤いガイドラインのすぐ下の新しい位置にドラッグします。

   ![赤いガイドラインを使用した画像の配置](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## 画像の削除

1. 画像コンテナの上にマウスポインターを置いてツールボックスを表示し、 _削除_ ( ![削除アイコン](./assets/pb-icon-remove.png){width="20"} ) アイコンをクリックします。

1. 確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.

## 検索エンジンの最適化

これらの設定のテキストは検索エンジンで表示され、ページのインデックス付け方法が改善されます。

- の場合 **[!UICONTROL Alternative Text]**、 _alt_ 表示するデジタルアクセシビリティツールのテキスト説明。

  代替テキストの使用はアクセシビリティのベストプラクティスであり、一部のロケールでは法律で必須となっています。 HTMLでは、 `alt` 属性は、 `image` タグ： `<image title="tooltip" alt="description" src="image.jpg">`.

- の場合 **[!UICONTROL Title Attribute]**&#x200B;に値を入力する場合は、マウスオーバー時にツールチップとして表示するテキストを入力します。

  ベストプラクティスとしては、説明的でキーワードが豊富なタイトルを選択し、検索エンジンによる画像のインデックス作成方法を改善します。 HTMLでは、 `title` 属性は、 `image` タグ： `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- コンテナに追加する画像の水平方向の位置を制御するには、 **[!UICONTROL Alignment]**.

  | オプション | 説明 |
  | ------ | ----------- |
  | `Default` | 現在のテーマのスタイルシートで指定された位置揃えの既定の設定を適用します。 |
  | `Left` | 画像コンテンツを画像コンテナの左の境界線に沿って揃えます。指定されたパディングの値を使用します。 |
  | `Center` | 画像コンテンツを画像コンテナの中央に揃えます。指定されたパディングの分だけ大きくします。 |
  | `Right` | 画像コンテナの右の境界線に沿って画像コンテンツを揃えます。指定されたパディングの値を使用します。 |

  {style="table-layout:auto"}

- を設定します。 **[!UICONTROL Border]** 画像コンテナの 4 つの側面すべてに適用されるスタイル：

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

- （オプション） **[!UICONTROL CSS classes]** 現在のスタイルシートから画像コンテナに適用します。

  複数のクラス名はスペースで区切ります。

- 次の値をピクセル単位で入力します。 **[!UICONTROL Margins and Padding]** ：画像コンテナの外側の余白と内側のパディングを指定します。

  画像コンテナ図で、対応する各値を入力します。

  | コンテナ領域 | 説明 |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白の量。 |
  | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白の量。 |

  {style="table-layout:auto"}
