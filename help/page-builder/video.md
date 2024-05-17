---
title: メディア – ビデオ
description: YouTubeまたは Vimeo でホストされているビデオをに追加するために使用される、ビデオコンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 0%

---

# メディア – ビデオ

の使用 _ビデオ_ ホストされているビデオを追加するためのコンテンツタイプ [YouTube][1] または [Vimeo][2] に [[!DNL Page Builder] ステージ](workspace.md#stage). ページやブロック、または製品やカテゴリの説明にビデオを簡単に埋め込むことができます。

![ストアフロントのホームページのビデオ](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ビデオツールボックス

![ビデオツールボックス](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| ツール | アイコン | 説明 |
|--- |--- |--- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | ビデオをステージ上の別の位置に移動します。 |
| （ラベル） | [!UICONTROL Video] | 現在のコンテンツコンテナをビデオとして識別します。 画像コンテナにカーソルを合わせると、ツールボックスが表示されます。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | を開きます _[!UICONTROL Edit Video]_このページで、ビデオとコンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在のビデオを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のビデオを表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | ビデオをコピーします。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | ステージからビデオを削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## ビデオを追加

1. 開始する前に、 [YouTube][1] または [Vimeo][2] 埋め込むビデオで、リンクをコピーします。

   または、有効なビデオファイルへの直接リンクをコピーすることもできます。 参照： [基本的なビデオ設定](#basic-video-settings) 有効なリンク用。

1. が含まれる [!DNL Commerce] 管理者、に戻る [!DNL Page Builder] ビデオを追加するワークスペース。

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Media]** をドラッグします。 **[!UICONTROL Video]** ステージへのプレースホルダー。

   ![ビデオプレースホルダーのステージへのドラッグ](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. ビデオコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

1. の場合 **[!UICONTROL Video URL]**、コピーしたビデオの URL をペーストします。

   の URL [!DNL Page Builder] この例で使用するビデオは次のとおりです。 `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. を制限するには **[!UICONTROL Maximum Width]** ビデオの最大幅をピクセル単位で入力します。

   空白の場合、ビデオの幅はコンテナで許可されている幅になり、余白とパディングを使用できます。

1. 右上隅のをクリックします。 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

## ビデオ設定の変更

1. ビデオコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

1. 次の節に従って、設定を変更します。

   - [基本](#basic-video-settings)
   - [詳細](#advanced)

1. 右上隅のをクリックします。 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

### 基本的なビデオ設定

1. 現在のビデオを変更するには、 **[!UICONTROL Video URL]**.

   有効なビデオ URL を入力します。 有効なビデオ URL は、次へのリンクです。

   - YouTube ビデオ： `https://youtu.be/CoDhMRUUjeI`
   - Vimeo 動画： `https://vimeo.com/190156113`
   - 有効なビデオファイル （`.mp4` 推奨）: `https://myvideos.com/spiral.mp4`

1. ストアフロントのビデオに許可される幅を変更するには、新しいを入力します **[!UICONTROL Maximum Width]** ピクセル単位。

   空白の場合、ビデオはコンテナの全幅を拡大し、余白とパディングの許容値を減らします。

1. ページの読み込み後にビデオを自動開始するには、次のように設定します **[!UICONTROL Autoplay]** 対象： `Yes`.

   自動再生が次のように設定されている場合： `Yes`の場合、ビデオはポリシーに従って再生時にミュートされます。 ただし、この設定を使用しても、モバイルデバイスでビデオを自動再生することはできません。 これらのポリシーについて詳しくは、次の開発者向けリソースを参照してください。

   - [Vimeo の自動再生ポリシー](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Googleからの自動再生ポリシー（Chrome/YouTube）](https://developer.chrome.com/blog/autoplay/)
   - [ローカルビデオの自動再生ポリシー](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   自動再生が次のように設定されている場合： `No`このビデオは、ユーザーの要求に応じてのみ再生されます。

### [!UICONTROL Advanced]

1. コンテナ内のビデオの水平方向の位置を制御するには、 **[!UICONTROL Alignment]**:

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
   | `Left` | 指定したパディングを考慮して、ビデオコンテナの左境界線に沿ってコンテンツを配置します。 |
   | `Center` | 指定したパディングを許容して、ビデオコンテナの中央にコンテンツを揃えます。 |
   | `Right` | 指定したパディングを考慮して、ビデオコンテナの右端に沿ってコンテンツを配置します。 |

   {style="table-layout:auto"}

- を **[!UICONTROL Border]** ビデオコンテナの 4 つの辺すべてに適用されるスタイル：

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

- （オプション）の名前を指定します **[!UICONTROL CSS classes]** ビデオコンテナに適用する現在のスタイルシートから。

  複数のクラス名はスペースで区切ります。

- 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** ビデオコンテナの外側の余白と内側のパディングを指定します。

  対応する各値をビデオコンテナ図に入力します。

  | コンテナ領域 | 説明 |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 |
  | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 |

  {style="table-layout:auto"}

## ビデオの移動

1. ビデオコンテナにカーソルを合わせてツールボックスを表示し、 _移動_ （ ![移動アイコン](./assets/pb-icon-move.png){width="20"} ） アイコンをクリックします。

   ![ビデオの移動](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. ビデオを選択して、赤いガイドラインのすぐ下の新しい位置にドラッグします。

   ![赤いガイドラインを使用したビデオの配置](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## ステージからビデオを削除

1. ビデオコンテナにカーソルを合わせてツールボックスを表示し、 _削除_ （![アイコンを削除](./assets/pb-icon-remove.png)） アイコンをクリックします。

1. 確認を求められたら、 **[!UICONTROL OK]**.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
