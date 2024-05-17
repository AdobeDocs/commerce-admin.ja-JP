---
title: カテゴリ – コンテンツ設定
description: の使用について説明します [!UICONTROL Content] カテゴリページに表示される追加のコンテンツを定義するための設定。
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# カテゴリ – コンテンツ設定

この _[!UICONTROL Content]_設定によって、カテゴリページに表示される追加コンテンツが決まります。 カテゴリ製品のリストに加えて、ページには画像、説明、CMS ブロックを含めることができます。 を使用できます [[!DNL Page Builder]](../page-builder/introduction.md) カテゴリの説明を定義するコンテンツツール。

## カテゴリの説明をに追加します。 [!DNL Page Builder]

1. カテゴリを編集モードで開きます。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** セクション。

   ![カテゴリコンテンツ](./assets/category-content.png){width="600" zoomable="yes"}

1. の右上 **[!UICONTROL Description]** エリア、クリック **[!UICONTROL Edit with Page Builder]**.

1. の使用 [[!DNL Page Builder]](../page-builder/introduction.md) コンテンツツールから [既存のテキストを編集](../page-builder/text.md) を選択し、必要に応じて他のコンテンツを追加します。

## [!DNL Page Builder] プレビュー

を展開すると、 _コンテンツ_ で作成されたコンテンツが存在する既存のカテゴリのセクション [!DNL Page Builder]を選択すると、のプレビューが表示されます **[!UICONTROL Description]** カテゴリページに表示されるコンテンツ。 コンテンツ領域をクリックすると、が開きます [!DNL Page Builder] ワークスペース（必要な更新を加えることができます）。

![説明プレビュー](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

このコンテンツプレビューは、製品フォームとカテゴリフォームに対してデフォルトで有効になっています。 プレビューの読み込みが原因でパフォーマンスが低下した場合は、でプレビューを無効にできます [コンテンツ管理の設定](../configuration-reference/general/content-management.md#advanced-content-tools) 設定。

## エディターでカテゴリの説明を追加

テキスト ボックスに ASCII 文字のみを入力します。 ワードプロセッサからテキストを貼り付ける場合は、まずプレーンな.TXT ファイルとして保存し、非表示の制御文字を削除します。

詳しくは、を参照してください [WYSIWYG エディター](../content-design/editor.md).

1. カテゴリを編集モードで開きます。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** セクション。

   ![カテゴリコンテンツ](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. カテゴリを入力 **[!UICONTROL Description]** を使用する [エディターツールバー](../content-design/editor.md) を必要に応じて書式設定します。

   右下隅をドラッグして、テキストボックスの高さを変更できます。

## カテゴリページへの CMS ブロックの追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリ ツリーで、編集するカテゴリを選択します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** セクション。

1. の場合 **[!UICONTROL Add the CMS block]**&#x200B;で、追加するブロックを選択します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Display Settings]** セクション。

1. を **[!UICONTROL Display Mode]** を次のいずれかに変更します。

   - `Static block only`
   - `Static block and products`

1. 完了したら、 **[!UICONTROL Save]** および、ストアフロントでのブロック表示を確認します（キャッシュの更新が必要です）。

## コンテンツ設定リファレンス

| 設定 | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Category Image] | ストア表示 | カテゴリページの上部の画像を指定します。 メソッド： <br/><br/>**[!UICONTROL Upload]**- ローカルコンピューターからギャラリーに画像ファイルをアップロードし、カテゴリ画像として使用します。<br/><br/>**[!UICONTROL Select from Gallery]** - ギャラリーから既存の画像を選択するように求められます。 <br/><br/>![ページビルダーのカメラアイコン](../assets/icon-camera.png)  – 画像ファイルをカメラタイルにドラッグするか、画像を参照してローカルファイルシステムから選択します。 |
| [!UICONTROL Description] | ストア表示 | カテゴリ ページに表示される説明を指定します。 <br/><br/>**[!UICONTROL Edit with Page Builder]**– を開きます [[!DNL Page Builder] workspace](../page-builder/workspace.md)：説明を編集できます。<br/><br/>**[!UICONTROL Show / Hide Editor]** - WYSIWYG エディターとHTMLモードの表示を切り替えます。 |
| [!UICONTROL Add CMS Block] | ストア表示 | 既存のを追加 [CMS ブロック](../content-design/blocks.md) をカテゴリページに追加します。 |

{style="table-layout:auto"}
