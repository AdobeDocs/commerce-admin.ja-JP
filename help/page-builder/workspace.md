---
title: '''[!DNL Page Builder] ワークスペース`'
description: で使用できるツールについて説明します。 [!DNL Page Builder] workspace を使用して、基本ページ、商品ページ、カタログページ、ブロック、動的ブロックを作成する場合。
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# [!DNL Page Builder] Workspace

条件 [[!DNL Page Builder] が有効になっている](setup.md)、 _[!UICONTROL Content]_セクションとコンテンツ作成プロセスは、高度な [!DNL Page Builder] CMS 用ツール [ページ](../content-design/page-add.md), [製品](../catalog/product-content.md) および [カテゴリ](../catalog/categories-content-settings.md) ページ、 [ブロック](../content-design/block-add.md)、および [動的ブロック](../content-design/dynamic-blocks.md). この節では、_&#x200B;コンテンツ見出し&#x200B;_フィールド、コンテンツのプレビュー、フルスクリーンへの簡単なアクセス [!DNL Page Builder] ワークスペース。

![次を含むコンテンツセクション [!DNL Page Builder] プレビュー](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## コンテンツ見出し

検索エンジンではレベル 1(H1) の見出しを探すので、レベル 1 の見出しを追加すると、ページのインデックスが正しく作成されるのを簡単に確認できます。

>[!NOTE]
>
>The _[!UICONTROL Content Heading]_ページの上部に表示されるフィールドは、以前に作成されたコンテンツをサポートする従来のフィールドです。 [!DNL Commerce] リリース。 しかし、それはの一部ではありません [!DNL Page Builder]. The [!UICONTROL Content Heading] は、現在のテーマに関連付けられているスタイルシートに従って H1 見出しとして書式設定されます。 これは、 [!DNL Page Builder] ステージ。

すべてのレベルの見出しの位置と形式を最適に制御するには、 _[!UICONTROL Content Heading]_フィールドが空の場合は、 [!DNL Page Builder] [見出し](heading.md) コンテンツタイプ。

![コンテンツの見出しおよび他の見出し](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## プレビュー

を展開すると、 _[!UICONTROL Content]_セクションと、 [!DNL Page Builder]をクリックすると、ページと同じようにコンテンツのプレビューが表示されます。 クリック&#x200B;**[!UICONTROL Edit with Page Builder]**または、コンテンツプレビュー領域内で [!DNL Page Builder] ワークスペースで、必要な更新を行うことができます。

![製品の説明のプレビュー](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>製品フォームおよびカテゴリフォームの場合、このコンテンツプレビューはデフォルトで有効になっていますが、無効にすることができます。 プレビューの読み込みによってパフォーマンスが低下した場合は、 [コンテンツ管理の設定](../configuration-reference/general/content-management.md#advanced-content-tools) 設定。

## ステージ

を開くと、 [!DNL Page Builder] プレビューのワークスペースでは、ステージは、コンテンツの作成と書式設定を行うことができ、ライブコンテンツをすばやく編集することもできる主要な作業領域です。 ステージは最初は空で、左のパネルから行、列およびタブをドラッグできるデザインサーフェスが表示されます。

>[!NOTE]
>
>2.4.1 リリース以降、で制御されるすべての領域で、コンテンツ編集がフルスクリーンになりました。 [!DNL Page Builder]- CMS ページ、製品およびカテゴリページ、ブロック、動的ブロック。 フルスクリーン編集により、コンテンツにフォーカスが置かれ、ストアフロントのユーザーエクスペリエンスに合った表示が提供されます。

![ページコンテンツを含むステージ](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ビューポート

A _viewport_ は、ユーザーに表示される Web ページの表示領域です。 フルスクリーンデザインモードでは、ビューポートボタンは [!DNL Page Builder] ステージを開き、サイトユーザーがストアフロントでコンテンツを見たときに表示することができます。

![ビューポートボタン](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] また、ビューポートのブレークポイントも定義します。 ブレークポイントでは、特定のスタイルが適用される最小幅と最大幅を定義します。 The [!DNL Page Builder] ビューポートには次のコンテンツのブレークポイントが設定されます。

- **デスクトップのブレークポイント**—`min-width: 1024px`. このブレークポイントは、1024 ピクセル以上の範囲を測定するビューポートの幅に対して定義されたスタイルを適用します。
- **モバイルのブレークポイント**—`max-width: 768px, min-width: 640px`. これらのブレークポイントでは、768 ～ 640 ピクセルの表示域の幅に対して定義されたスタイルが適用されます。

[!DNL Page Builder] ビューポートには次の 2 つの機能があります。 **_コンテンツプレビュー_** および **_ブレークポイント設定_**.

### コンテンツのプレビュー

デフォルトでは、 [!DNL Page Builder] には、2 つのビューポートプレビューが用意されています。

- **デスクトップ**  — 事前に定義された幅を持たずに、コンテンツのプレビューを表示します。 デスクトップ定義のスタイル（1,024 ピクセルのブレークポイント最小幅を使用）は、引き続きページに適用されます。 ただし、デスクトップビューポートの幅は、「行」などのコンテナコンテンツタイプの設定で定義されます。 デスクトップビューポートを選択すると、ブラウザーページの幅が 1,024 ピクセル以上の場合に、コンテンツがストアフロントでどのようにスタイル設定されているかが表示されます。

  ![幅 1024 ピクセル以上のデスクトップビューポートプレビュー](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **モバイル**  — コンテンツのプレビューを、事前に定義された幅（768 ピクセル）で表示します。 デスクトップビューポートとは異なり、モバイルビューポートでは、ページコンテンツの幅が 768 ピクセルになり、ブレークポイントの幅が 768 ピクセル（最大）と 640 ピクセル（最小）に定義されたスタイルが表示されます。

  ![幅が 768 ピクセル以上のモバイルビューポートプレビュー](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### ブレークポイントの設定

ビューポートボタンには、選択したビューポートに基づいてコンテンツタイプに異なるブレークポイントスタイルを適用するオプションも用意されています。 デフォルトでは、 [!DNL Page Builder] ブレークポイント設定を提供 _[!UICONTROL Minimum Height]_「行」、「列」、「タブ」、「タブ項目」、「バナー」、「スライダー」、「スライド」のフィールド。 モバイルビューポートを選択し、これらのコンテンツタイプの 1 つに対してエディターを開くと、モバイルビューポートのブレークポイントに固有のフィールド値を入力できます。 特定のブレークポイント設定を許可するコンテンツタイプフィールドには、行の例と同様に、フィールドの右側にアイコンが表示されます。

![ブレークポイント設定のアイコンインジケーター](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## パネル

The [!DNL Page Builder] パネルはステージの左側にあり、ステージにドラッグできるコンテンツタイプが含まれます。 次に、コンテンツタイプに固有のコンテナが、オプションのツールボックスと共に表示されます。 コンテンツタイプは、パネル内で次のように整理されます。

### レイアウト

The _[!UICONTROL Layout]_のセクション [!DNL Page Builder] パネルは、行、列またはタブをステージに追加するために使用します。 コンテンツタイプをパネルからステージにドラッグすると、コンテナが表示され、コンテンツタイプに固有のオプションのツールボックスが表示されます。

デフォルトでは、 [!DNL Page Builder] ステージが空です。 レイアウトコンテンツタイプをパネルからステージにドラッグすると、ページ上の他のレイアウトコンテナの上、下または内に配置できます。 行はステージに直接のみ追加できます。

![[!DNL Page Builder] レイアウトコンテンツタイプとステージを含むパネル](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| レイアウトコンテンツタイプ | 説明 |
| ------------------- |------------ |
| [行](row.md) | 新しい行は、パネルからステージにのみドラッグでき、別の行、タブまたは列グループの上または下に配置できます。 「複製」オプションを使用して、既存の行のコピーを作成することもできます。 |
| [列](column.md) | 列は、パネルからステージに、または行とタブにドラッグできます。 追加できる列の最大数は、 [設定](setup.md). |
| [タブ](tabs.md) | 単一のタブは、パネルからステージに、または行と列にドラッグできます。 ツールボックスからタブを追加できます。 |

{style="table-layout:auto"}

### 要素

以下を使用します。 _[!UICONTROL Elements]_のセクション [!DNL Page Builder] パネルを使用して、テキスト、見出し、ボタン、区切り、HTMLコードを、レイアウトコンテナ上の任意のレイアウトコンテナに追加します。 [[!DNL Page Builder] ステージ](workspace.md#stage). コンテンツタイプをパネルから行または列にドラッグしたり、ステージ上のタブセットにドラッグすると、コンテナが表示されます。 コンテンツタイプツールボックスを使用して、そのタイプに固有の設定にアクセスします。

![[!DNL Page Builder] 要素コンテンツタイプを持つパネル](./assets/pb-elements.png){width="600" zoomable="yes"}

| 要素のコンテンツタイプ | 説明 |
| -------------------- | ----------- |
| [テキスト](text.md) | テキストコンテナとエディターをステージに追加します。 |
| [見出し](heading.md) | ステージに見出しコンテナを追加します。 |
| [ボタン](buttons.md) | 個々のボタンまたはボタンのセットのコンテナをステージに追加します。 |
| [分周器](divider.md) | ステージにディバイダのコンテナを追加します。 |
| [HTMLコード](html-code.md) | ステージにHTMLコードのコンテナを追加します。 |

{style="table-layout:auto"}

### メディア

以下を使用します。 _[!UICONTROL Media]_のセクション [!DNL Page Builder] 画像、ビデオ、バナー、スライダー、およびを追加するためのパネル [!DNL Google Maps] を [[!DNL Page Builder] ステージ](workspace.md#stage). メディアコンテンツタイプがパネルからステージにドラッグされると、コンテナが表示され、コンテンツタイプに固有のオプションのツールボックスが表示されます。

![[!DNL Page Builder] メディアコンテンツタイプを持つパネル](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| メディアコンテンツタイプ | 説明 |
| ------------------- | ------------------------------------------ |
| [画像](image.md) | 画像コンテナをステージに追加します。 |
| [ビデオ](video.md) | ステージにビデオコンテナを追加します。 |
| [バナー](banner.md) | バナーコンテナをステージに追加します。 |
| [スライダー](slider.md) | スライダーコンテナをステージに追加します。 |
| [マップ](map.md) | を追加します。 [!DNL Google Maps] コンテナをステージに追加します。 |

{style="table-layout:auto"}

### コンテンツを追加

以下を使用します。 _[!UICONTROL Add Content]_のセクション [!DNL Page Builder] 既存のコンテンツを [[!DNL Page Builder] ステージ](workspace.md#stage). メディアコンテンツタイプをパネルからステージにドラッグすると、コンテナが表示されます。 コンテンツタイプツールボックスを使用して、_&#x200B;設定&#x200B;_タイプに固有の。

![[!DNL Page Builder] コンテンツタイプを追加するパネル](./assets/pb-add-content.png){width="600" zoomable="yes"}

| コンテンツタイプ | 説明 |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [ブロック](block.md) | 既存のブロックをステージに追加します。 |
| [ダイナミックブロック](dynamic-block.md) | 既存のダイナミックブロックをステージに追加します。 |
| [製品](products.md) | ステージに製品のリストを追加します。 |
| ![Adobe Commerceのみ](../assets/adobe-logo.svg) [製品Recommendations](recommendations.md) | レコメンデーション単位をステージに追加します。 |

{style="table-layout:auto"}

## Toolbox

ステージ上の各コンテンツコンテナには、オプションのツールボックスがあります。 オプションはコンテンツタイプによって異なりますが、通常は移動、設定、非表示/表示、複製、削除が含まれます。

### ツールボックスを表示

コンテナの上にマウスポインターを置いてツールボックスを表示し、オプションを選択します。

![行ツールボックスのオプション](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Toolbox オプション

| オプション | アイコン | 説明 |
| --------- | ---------------------------------------- | ------------ |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 現在のコンテンツコンテナをステージ上の別の位置に移動します。 |
| 追加 | ![追加アイコン](./assets/pb-icon-add.png){width="25"} | ボタン、スライド、タブなどの子要素を追加します。 |
| （ラベル） |           | コンテナのコンテンツタイプを識別します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | コンテンツコンテナのプロパティを編集モードで開きます。 |
| 非表示 | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在のコンテンツコンテナを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 現在のコンテンツコンテナを表示します。 |
| 複製 | ![複製アイコン](./assets/pb-icon-duplicate.png){width="25"} | 現在のコンテンツコンテナのコピーを作成します。 |
| 削除 | ![削除](./assets/pb-icon-remove.png){width="25"} | 現在のコンテンツコンテナをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}
