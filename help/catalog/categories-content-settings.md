---
title: カテゴリ – コンテンツ設定
description: '[!UICONTROL Content] 設定を使用して、カテゴリページに表示される追加のコンテンツを定義する方法について説明します。'
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# カテゴリ – コンテンツ設定

_[!UICONTROL Content]_&#x200B;の設定によって、カテゴリページに表示される追加コンテンツが決まります。 カテゴリ製品のリストに加えて、ページには画像、説明、CMS ブロックを含めることができます。 [[!DNL Page Builder]](../page-builder/introduction.md) のコンテンツツールを使用して、カテゴリの説明を定義できます。

## カテゴリの説明を [!DNL Page Builder] に追加します

1. カテゴリを編集モードで開きます。

1. 下にスクロールして、「**[!UICONTROL Content]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

   ![ カテゴリコンテンツ ](./assets/category-content.png){width="600" zoomable="yes"}

1. **[!UICONTROL Description]** 領域の右上にある「**[!UICONTROL Edit with Page Builder]**」をクリックします。

1. [[!DNL Page Builder]](../page-builder/introduction.md) のコンテンツツールを使用して [ 既存のテキストを編集 ](../page-builder/text.md) し、必要に応じて他のコンテンツを追加します。

## [!DNL Page Builder] プレビュー

[!DNL Page Builder] で作成されたコンテンツがある既存のカテゴリの「_コンテンツ_」セクションを展開すると、カテゴリページに表示されるとおりに、**[!UICONTROL Description]** コンテンツのプレビューが表示されます。 コンテンツ領域をクリックすると、[!DNL Page Builder] ワークスペースが開き、必要な更新を行うことができます。

![ 説明プレビュー ](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

このコンテンツプレビューは、製品フォームとカテゴリフォームに対してデフォルトで有効になっています。 プレビューの読み込みが原因でパフォーマンスが低下した場合は、[ コンテンツ管理の設定 ](../configuration-reference/general/content-management.md#advanced-content-tools) でプレビューを無効にすることができます。

## エディターでカテゴリの説明を追加

テキスト ボックスに ASCII 文字のみを入力します。 ワードプロセッサからテキストを貼り付ける場合は、まずプレーンな.TXT ファイルとして保存し、非表示の制御文字を削除します。

詳しくは、[WYSIWYG エディター ](../content-design/editor.md) を参照してください。

1. カテゴリを編集モードで開きます。

1. 下にスクロールして、「**[!UICONTROL Content]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

   ![ カテゴリコンテンツ ](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. カテゴリ **[!UICONTROL Description]** を入力し、[ エディターツールバー ](../content-design/editor.md) を使用して、必要に応じて形式を設定します。

   右下隅をドラッグして、テキストボックスの高さを変更できます。

## カテゴリページへの CMS ブロックの追加

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. カテゴリ ツリーで、編集するカテゴリを選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Content]**」セクションを展開します。

1. **[!UICONTROL Add the CMS block]**：追加するブロックを選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Display Settings]**」セクションを展開します。

1. **[!UICONTROL Display Mode]** を次のいずれかに設定します。

   - `Static block only`
   - `Static block and products`

1. 完了したら、「**[!UICONTROL Save]**」をクリックして、ストアフロントのブロック表示を確認します（キャッシュの更新が必要です）。

## コンテンツ設定リファレンス

| 設定 | [ 範囲 ](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Category Image] | ストア表示 | カテゴリページの上部の画像を指定します。 メソッド：<br/><br/>**[!UICONTROL Upload]**- ローカルコンピューターからギャラリーに画像ファイルをアップロードし、カテゴリ画像として使用します。<br/><br/>**[!UICONTROL Select from Gallery]** - ギャラリーから既存の画像を選択するように求められます。 <br/><br/>![ ページビルダーカメラアイコン ](../assets/icon-camera.png) – 画像ファイルをカメラタイルにドラッグするか、画像を参照してローカルファイルシステムから選択します。 |
| [!UICONTROL Description] | ストア表示 | カテゴリ ページに表示される説明を指定します。 <br/><br/>**[!UICONTROL Edit with Page Builder]**- [[!DNL Page Builder]  ワークスペース ](../page-builder/workspace.md) を開きます。ここで説明を編集できます。<br/><br/>**[!UICONTROL Show / Hide Editor]** - WYSIWYG エディターとHTMLモードの表示を切り替えます。 |
| [!UICONTROL Add CMS Block] | ストア表示 | カテゴリ ページに既存の [CMS ブロック ](../content-design/blocks.md) を追加します。 |

{style="table-layout:auto"}
