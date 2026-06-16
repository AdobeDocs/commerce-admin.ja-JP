---
title: カテゴリ – コンテンツ設定
description: '[!UICONTROL Content]設定を使用して、カテゴリーページに表示される追加コンテンツを定義する方法について説明します。'
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/PKCKw4i-EDB10X3AU-daMiyVMT96naqRLF8vrVBp24s
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 450
ht-degree: 0%

---

# カテゴリ – コンテンツ設定

_[!UICONTROL Content]_の設定により、追加コンテンツがカテゴリーページに表示されるかどうかが決まります。 このページには、カテゴリ商品のリストに加えて、画像、説明、CMS ブロックを含めることができます。 [[!DNL Page Builder]](../page-builder/introduction.md) コンテンツ ツールを使用して、カテゴリの説明を定義できます。

## [!DNL Page Builder]にカテゴリの説明を追加

1. カテゴリを編集モードで開きます。

1. 下にスクロールして、**[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![ カテゴリーコンテンツ ](./assets/category-content.png){width="600" zoomable="yes"}

1. **[!UICONTROL Description]** エリアの右上にある「**[!UICONTROL Edit with Page Builder]**」をクリックします。

1. [[!DNL Page Builder]](../page-builder/introduction.md) コンテンツツールを使用して、既存のテキスト ](../page-builder/text.md)を[編集し、他のコンテンツを（必要に応じて）追加します。

## [!DNL Page Builder] プレビュー

[!DNL Page Builder]で作成されたコンテンツがある既存のカテゴリの&#x200B;_コンテンツ_ セクションを展開すると、カテゴリーページに表示されるコンテンツの&#x200B;**[!UICONTROL Description]**&#x200B;のプレビューが表示されます。 コンテンツ領域をクリックすると、[!DNL Page Builder] ワークスペースが開き、必要な更新を行うことができます。

![説明プレビュー](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

このコンテンツプレビューは、デフォルトで製品フォームとカテゴリーフォームに対して有効になっています。 プレビューの読み込みに伴いパフォーマンスが低下する場合は、[ コンテンツ管理設定](../configuration-reference/general/content-management.md#advanced-content-tools)でプレビューを無効にできます。

## エディターでのカテゴリの説明の追加

テキストボックスにプレーン ASCII文字のみを入力します。 ワードプロセッサーからテキストをペーストする場合は、最初にプレーンな.TXT ファイルとして保存して、目に見えないコントロール文字を削除します。

詳しくは、[WYSIWYG エディター](../content-design/editor.md)を参照してください。

1. カテゴリを編集モードで開きます。

1. 下にスクロールして、**[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![ カテゴリーコンテンツ ](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. カテゴリ **[!UICONTROL Description]**&#x200B;を入力し、[ エディターツールバー](../content-design/editor.md)を使用して、必要に応じて書式設定します。

   右下隅をドラッグして、テキストボックスの高さを変更できます。

## カテゴリーページへのCMS ブロックの追加

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. カテゴリーツリーで、編集するカテゴリを選択します。

1. **[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Add the CMS block]**&#x200B;で、追加するブロックを選択します。

1. **[!UICONTROL Display Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Display Mode]**&#x200B;を次のいずれかに設定します。

   - `Static block only`
   - `Static block and products`

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックし、ストアフロントでのブロック表示を確認します（キャッシュの更新が必要です）。

## コンテンツ設定リファレンス

| 設定 | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Category Image] | ストアビュー | カテゴリ ページの先頭の画像を指定します。 方法：<br/><br/>**[!UICONTROL Upload]**- ローカルコンピューターからギャラリーに画像ファイルをアップロードし、それをカテゴリ画像として使用します。<br/><br/>**[!UICONTROL Select from Gallery]** - ギャラリーから既存の画像を選択するよう求めるメッセージが表示されます。 <br/><br/>![ ページビルダーのカメラアイコン ](../assets/icon-camera.png) – 画像ファイルをカメラタイルにドラッグするか、画像を参照してローカルファイルシステムから選択します。 |
| [!UICONTROL Description] | ストアビュー | カテゴリ ページに表示される説明を指定します。<br/><br/>**[!UICONTROL Edit with Page Builder]**- [[!DNL Page Builder]  ワークスペース ](../page-builder/workspace.md)を開き、説明を編集できます。<br/><br/>**[!UICONTROL Show / Hide Editor]** - WYSIWYG エディターとHTML モードの表示を切り替えます。 |
| [!UICONTROL Add CMS Block] | ストアビュー | 既存の[CMS ブロック ](../content-design/blocks.md)をカテゴリーページに追加します。 |

{style="table-layout:auto"}
