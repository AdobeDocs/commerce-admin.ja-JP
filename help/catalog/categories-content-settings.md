---
title: カテゴリ — コンテンツ設定
description: の使用について [!UICONTROL Content] 設定を使用して、カテゴリページに表示される追加のコンテンツを定義します。
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# カテゴリ — コンテンツ設定

The _[!UICONTROL Content]_設定によって、カテゴリページに表示される追加のコンテンツが決まります。 カテゴリ製品のリストに加えて、画像、説明、CMS ブロックを含めることができます。 以下を使用すると、 [[!DNL Page Builder]](../page-builder/introduction.md) カテゴリの説明を定義するコンテンツツール。

## カテゴリの説明をに追加します。 [!DNL Page Builder]

1. カテゴリを編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 」セクションに入力します。

   ![カテゴリコンテンツ](./assets/category-content.png){width="600" zoomable="yes"}

1. の右上 **[!UICONTROL Description]** 領域、クリック **[!UICONTROL Edit with Page Builder]**.

1. 以下を使用します。 [[!DNL Page Builder]](../page-builder/introduction.md) コンテンツツール [既存のテキストを編集](../page-builder/text.md) 他のコンテンツを追加します（必要に応じて）。

## [!DNL Page Builder] プレビュー

を展開すると、 _コンテンツ_ コンテンツが作成される既存のカテゴリのセクション [!DNL Page Builder]をクリックすると、 **[!UICONTROL Description]** カテゴリページに表示される内容 コンテンツ領域をクリックすると、 [!DNL Page Builder] ワークスペースで、必要な更新を行うことができます。

![説明のプレビュー](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

このコンテンツプレビューは、製品フォームとカテゴリフォームに対してデフォルトで有効になっています。 プレビューの読み込みによってパフォーマンスが低下した場合は、 [コンテンツ管理の設定](../configuration-reference/general/content-management.md#advanced-content-tools) 設定。

## エディターでカテゴリの説明を追加します。

テキストボックスには、プレーン ASCII 文字のみを入力します。 ワープロからテキストを貼り付ける場合は、まずプレーン.TXT ファイルとして保存し、非表示の制御文字を削除します。

詳しくは、 [WYSIWYG エディタ](../content-design/editor.md).

1. カテゴリを編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 」セクションに入力します。

   ![カテゴリコンテンツ](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. カテゴリを入力 **[!UICONTROL Description]** また、 [エディターツールバー](../content-design/editor.md) 必要に応じて形式を設定します。

   右下隅をドラッグして、テキストボックスの高さを変更できます。

## カテゴリページに CMS ブロックを追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーで、編集するカテゴリを選択します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 」セクションに入力します。

1. の場合 **[!UICONTROL Add the CMS block]**、追加するブロックを選択します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Display Settings]** 」セクションに入力します。

1. を設定します。 **[!UICONTROL Display Mode]** を次のいずれかに変更します。

   - `Static block only`
   - `Static block and products`

1. 完了したら、「 **[!UICONTROL Save]** ストアフロントでのブロック表示を確認します（キャッシュの更新が必要です）。

## コンテンツ設定リファレンス

| 設定 | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Category Image] | ストア表示 | カテゴリページの先頭の画像を指定します。 メソッド： <br/><br/>**[!UICONTROL Upload]**— ローカルコンピューターからギャラリーに画像ファイルをアップロードし、カテゴリ画像として使用します。<br/><br/>**[!UICONTROL Select from Gallery]**  — ギャラリーから既存の画像を選択するように求められます。 <br/><br/>![Page Builder のカメラアイコン](../assets/icon-camera.png)  — 画像ファイルをカメラタイルにドラッグするか、画像を参照してローカルファイルシステムから選択します。 |
| [!UICONTROL Description] | ストア表示 | カテゴリページに表示する説明を指定します。 <br/><br/>**[!UICONTROL Edit with Page Builder]**— を開きます。 [[!DNL Page Builder] workspace](../page-builder/workspace.md)：説明を編集できます。<br/><br/>**[!UICONTROL Show / Hide Editor]** - WYSIWYG エディタとHTML・モードの表示を切り替えます。 |
| [!UICONTROL Add CMS Block] | ストア表示 | 既存の [CMS ブロック](../content-design/blocks.md) をカテゴリページに追加します。 |

{style="table-layout:auto"}
