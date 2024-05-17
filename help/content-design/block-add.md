---
title: コンテンツブロックを追加
description: 任意のページや別のブロック内で再利用できる、コンテンツのカスタムブロックを作成します。
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# コンテンツブロックを追加

コンテンツのカスタムブロックを作成して、任意のページ、ページのグループ、または別のブロックに追加できます。 たとえば、ブロックに画像スライダーを配置し、そのブロックをホーム ページに配置できます。 ブロック ワークスペースでも同じ機能を使用できます [基本コントロール](pages-workspace.md) as the _ページ_ ワークスペースは、使用可能なブロックを見つけ、日常のメンテナンスを実行するのに役立ちます。 ブロックが完了したら、 [ウィジェット](widget-static-block.md) ストアの特定のページに配置するためのツール。

![ブロック ページには、既存のブロックのグリッドが表示されます](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## ブロックの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 右上隅のをクリックします。 **新規ブロックを追加**.

   ![新しいブロック ページには、オプションとコンテンツ スペースが表示されます](./assets/block-detail.png){width="500" zoomable="yes"}

1. 新しいブロックの既定の有効ステータスを変更する場合は、次のように設定します **ブロックを有効にする** 対象： `No`.

1. を割り当て **ブロックのタイトル** 内部参照用。

1. 一意のを割り当て **識別子** をブロックに使用します。

   スペースの代わりにアンダースコアを含む小文字をすべて使用します。

1. 各を選択 **[!UICONTROL Store View]** ブロックを使用可能にする場所。

1. 表示されたコンテンツツールセットを使用してブロックのコンテンツを追加します。

   - 次の場合 [ページビルダー](../page-builder/introduction.md) 有効にする、を選択します **[!UICONTROL Edit with Page Builder]** コンテンツでページビルダーツールを使用するには [workspace](../page-builder/workspace.md).

     ![ページビルダーワークスペース](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >ページビルダーを使用してブロックを追加する方法については、を参照してください。 [チュートリアル 2: ブロック](../page-builder/2-blocks.md).

   - の使用 [エディター](editor.md) テキストの書式設定、リンクの作成、表、画像、ビデオおよびオーディオの追加を行います。

     HTMLコードを使用するには、 **エディターを表示/非表示**.

     ![ブロック エディタ（非表示）](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

   新しいブロックが、[ ブロック ] グリッドのリストの一番下に表示されます。

1. の使用 [ウィジェット](widget-static-block.md) 完成したブロックをストアの特定のページに配置するツール。

## ブロックの削除

カスタムブロックを削除する方法は 2 つあります。 から削除できます _ブロック_ グリッド、またはブロックを編集ページから。

### 方法 1: ブロック グリッドからブロックを削除する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. グリッドの上でフィルタを使用してブロックを見つけ、削除する 1 つまたは複数のブロックのチェックボックスをオンにします。
1. リストの左上隅にあるを設定します。 **[!UICONTROL Actions]** 対象： `Delete`.
1. アクションを確定するには、 **[!UICONTROL OK]**.

### 方法 2：編集ページからブロックを削除する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. 削除するブロックを検索します。
1. が含まれる _アクション_ ブロックの列で、をクリックします **[!UICONTROL Select]** を選択します **[!UICONTROL Edit]**.
1. メニューバーで、 **[!UICONTROL Delete Block]**.
1. アクションを確定するには、 **[!UICONTROL OK]**.

## 保存メニュー

| コマンド | 説明 |
|----------|----------- |
| [!UICONTROL Save] | 現在のブロックを保存し、作業を続行します。 |
| [!UICONTROL Save & Duplicate] | 現在のブロックを保存して閉じ、新しい複製コピーを開きます。 |
| [!UICONTROL Save & Close] | 現在のブロックを保存して閉じ、[ ブロック ] グリッドに戻ります。 |

{style="table-layout:auto"}

## ライトボックスまたはスライダーの追加

- を追加するのは簡単です [slider](../page-builder/slider.md) 次を使用してストアに移動 [[!DNL Page Builder]](../page-builder/introduction.md). スライダーは、自動的に再生するように設定することも、ナビゲーションボタンを使用して手動で制御することもできます。

  ![ページビルダーのスライダー](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  また、で利用できる jQuery ベースの画像ライトボックスも幅広く揃えています [[!DNL Commerce Marketplace]][1]無料のコンテンツもあります。

- から拡張機能をダウンロードすることもできます。 [!DNL Commerce Marketplace]. その他のヘルプについては、拡張機能開発者が提供するドキュメントを参照してください。

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
