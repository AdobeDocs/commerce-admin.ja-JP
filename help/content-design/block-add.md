---
title: コンテンツブロックを追加
description: コンテンツのカスタムブロックを作成し、任意のページで、または別のブロック内で再利用できます。
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# コンテンツブロックを追加

コンテンツのカスタムブロックを作成して、任意のページ、ページのグループまたは別のブロックに追加できます。 例えば、ブロック内に画像スライダーを配置し、そのブロックをホームページ上に配置します。 ブロックワークスペースは同じ [基本的なコントロール](pages-workspace.md) として _ページ_ workspace を使用して、使用可能なブロックを見つけ、定期的なメンテナンスを実行できます。 ブロックが完了したら、 [Widget](widget-static-block.md) ツールを使用して、ストア内の特定のページに配置できます。

![[ ブロック ] ページには、既存のブロックのグリッドが表示されます](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## ブロックを作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 右上隅で、 **新しいブロックを追加**.

   ![新しいブロックページには、オプションとコンテンツスペースが表示されます](./assets/block-detail.png){width="500" zoomable="yes"}

1. 新しいブロックの既定の有効状態を変更する場合は、 **ブロックを有効にする** から `No`.

1. 割り当て： **ブロックタイトル** 内部参照用。

1. ユニークを割り当て **識別子** ブロックに対して。

   スペースの代わりに、アンダースコアを含むすべての小文字を使用します。

1. それぞれ選択 **[!UICONTROL Store View]** ブロックを使用できる場所です。

1. 表示されるコンテンツツールセットを使用して、ブロックのコンテンツを追加します。

   - 次の場合 [Page Builder](../page-builder/introduction.md) が有効な場合は、「 **[!UICONTROL Edit with Page Builder]** コンテンツでページビルダーツールを使用するには [workspace](../page-builder/workspace.md).

     ![Page Builder ワークスペース](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Page Builder でのブロックの追加について詳しくは、 [チュートリアル 2：ブロック](../page-builder/2-blocks.md).

   - 以下を使用します。 [編集者](editor.md) テキストを書式設定し、リンクを作成し、テーブル、画像、ビデオ、オーディオを追加します。

     HTMLコードを使用する場合は、 **エディターを表示/非表示**.

     ![ブロックエディタ（非表示）](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

   新しいブロックが、[ ブロック ] グリッドのリストの下部に表示されます。

1. 以下を使用します。 [Widget](widget-static-block.md) ツールを使用して、完了したブロックをストアの特定のページに配置できます。

## ブロックを削除する

カスタムブロックを削除する方法は 2 つあります。 これは、 _ブロック_ グリッド、またはブロックを編集ページから。

### 方法 1：ブロックグリッドからブロックを削除する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. グリッドの上のフィルタを使用してブロックを見つけ、削除する 1 つ以上のブロックのチェックボックスをオンにします。
1. リストの左上隅で、 **[!UICONTROL Actions]** から `Delete`.
1. アクションを確定するには、 **[!UICONTROL OK]**.

### 方法 2：編集ページからブロックを削除する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. 削除するブロックを見つけます。
1. Adobe Analytics の _アクション_ ブロックの列で、 **[!UICONTROL Select]** を選択します。 **[!UICONTROL Edit]**.
1. メニューバーで、 **[!UICONTROL Delete Block]**.
1. アクションを確定するには、 **[!UICONTROL OK]**.

## 保存メニュー

| コマンド | 説明 |
|----------|----------- |
| [!UICONTROL Save] | 現在のブロックを保存し、作業を続行します。 |
| [!UICONTROL Save & Duplicate] | 現在のブロックを保存して閉じ、新しい複製コピーを開きます。 |
| [!UICONTROL Save & Close] | 現在のブロックを保存して閉じ、[ ブロック ] グリッドに戻ります。 |

{style="table-layout:auto"}

## Lightbox またはスライダーの追加

- 追加が簡単です。 [スライダー](../page-builder/slider.md) ～と一緒にあなたの店に [[!DNL Page Builder]](../page-builder/introduction.md). スライダーは、自動的に再生するように設定するか、ナビゲーションボタンを使用して手動で制御することができます。

  ![Page Builder スライダー](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  また、jQuery ベースの画像ライトボックスの幅広い種類もできます。 [[!DNL Commerce Marketplace]][1]そして、いくつかは無料です。

- また、拡張機能は、 [!DNL Commerce Marketplace]. 詳しくは、拡張機能の開発者が提供するドキュメントを参照してください。

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
