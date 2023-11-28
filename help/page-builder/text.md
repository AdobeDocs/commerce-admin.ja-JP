---
title: 要素 — テキスト
description: テキストコンテンツタイプについて説明します。このタイプは、 [!DNL Page Builder] ステージ。
exl-id: 3f14af35-9c04-4f4b-b3dd-d3406d56a9c0
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# 要素 — テキスト

以下を使用します。 _テキスト_ コンテンツタイプ：WYSIWYG(「What You See Is You Get」) エディターを使用してテキストコンテナを追加する場合 [[!DNL Page Builder] ステージ](workspace.md#stage). さらに、リンク、画像、 [変数](../systems/variables-predefined.md)エディターのツールバーからテキストにウィジェットを追加します。

![バナー上の書式付きテキスト](./assets/pb-storefont-banner-with-button.png){width="700"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## テキストエディターツール

テキストエディターには、ステージまたは設定ページから直接アクセスできます。 ステージに直接加えた変更は、自動的に保存されます。 詳しくは、 [エディターの使用](../content-design/editor.md).

![テキストエディターツール — TinyMCE](./assets/pb-elements-text-editor-tools.png){width="600"}

## テキストコンテナツールボックス

![テキストコンテナツールボックス](./assets/pb-elements-text-toolbox.png){width="600"}

| ツール | アイコン | 説明 |
| --------- | --------------------- | -------------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | テキストコンテナをページ上の別の有効な場所に移動します。 |
| （ラベル） | テキスト | 現在のコンテナをテキスト要素として識別します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | テキストコンテナのプロパティを編集モードで開きます。 |
| 非表示 | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | テキストコンテナを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のテキストコンテナを表示します。 |
| 複製 | ![複製アイコン](./assets/pb-icon-duplicate.png){width="25"} | テキストコンテナのコピーを作成します。 |
| 削除 | ![削除アイコン](./assets/pb-icon-remove.png){width="25"} | ステージからテキストコンテナとその内容を削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## テキストを追加

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をクリックし、 **[!UICONTROL Text]** プレースホルダーをステージ上の行、列またはタブセットに追加します。

   ![テキストプレースホルダーのステージへのドラッグ](./assets/pb-elements-text-drag.png){width="600" zoomable="yes"}

1. 必要に応じて、エディターを使用してテキストを入力し、書式設定します。

   詳しくは、 [エディターの使用](../content-design/editor.md).

   ![コンテンツを含むテキストエディター](./assets/pb-elements-text-editor.png){width="600"}

## リンクの作成

エディターの「リンクを挿入」ボタンを使用すると、ギャラリー内の画像にハイパーリンクを簡単に追加できます。 ただし、URL が事前にある場合は、テキスト内にインラインリンクを作成するために使用することもできます。 「ウィジェット」ボタンとは異なり、「リンクを挿入/編集」ボタンは、ストア内のページ、製品またはカテゴリとは統合されていません。

電話番号や電子メールのリンクを作成するには、 [カスタム変数の追加](../systems/variables-custom.md).

1. ストアフロントで、リンクのターゲットとなるページに移動し、リンク情報をコピーします。

   完全修飾 URL またはストアドメインへの参照を省略する相対 URL を使用できます。

   完全な URL - `https://mystore.com/women/tops-women/tees-women.html`

   相対 URL - `../women/tops-women/tees-women.html`

1. エディタースペースでテキストを選択し、「 _リンクを挿入/編集_ ( ![リンクの挿入/編集ボタン](./assets/pb-icon-add-link.png){width="20"} ) をクリックします。

   ![書式設定されたテキストへのリンクの追加](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="500" zoomable="yes"}

1. の場合 **[!UICONTROL URL]**」と入力し、準備した相対リンクを入力します。

1. 設定 **[!UICONTROL Target]** から `None`.

   この設定により、新しいタブを開くのではなく、同じブラウザーウィンドウでページが開きます。

1. の場合 **[!UICONTROL Title]**，と入力します。 `Shop Tees`.

   The `Title` リンク属性は、一部のブラウザーでツールチップとして使用されます。

1. リンクを保存してに戻るには、以下を実行します。 [!DNL Page Builder] ワークスペース、クリック **[!UICONTROL OK]**.

   ![リンクの詳細](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="500" zoomable="yes"}

## 画像を挿入

1. テキスト内で画像を挿入する位置にカーソルを置きます。

1. クリック _画像の挿入/編集_ ( ![画像の挿入/編集ボタン](./assets/icon-pb-add-image.png){width="20"} ) をクリックします。

1. の場合 **[!UICONTROL Source]**&#x200B;をクリックし、メディアストレージを使用して画像を検索および選択します。

1. の場合 **[!UICONTROL Image Description]**、画像の説明テキストを入力します。

   このテキストは、 `alt` 画像のリンク属性。一部のブラウザーでアクセシビリティのために使用されます。

1. 幅と高さを入力 **[!UICONTROL Dimensions]**（ピクセル単位）。ページに画像をレンダリングするために使用します。

   キープ **[!UICONTROL Constrain proportions]** チェックボックスをオンにすると、画像の縦横比が自動的に維持されます。

1. 画像を挿入してから、 [!DNL Page Builder] ワークスペース、クリック **[!UICONTROL OK]**.

## テキスト設定の変更

1. テキストコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   >[!NOTE]
   >
   >テキストコンテナは別のコンテナ内に緊密にネストされているので、正しいツールボックスがあることを確認してください。

1. 必要に応じて、コンテンツを更新します。

1. を更新します。 _[!UICONTROL Advanced]_必要に応じて設定します。

   - 親コンテナ内でのテキストの位置を制御するには、 **[!UICONTROL Alignment]**:

     | オプション | 説明 |
     | ------ |------------ |
     | `Default` | 現在のテーマのスタイルシートで指定された位置揃えの既定の設定を適用します。 |
     | `Left` | リストを親コンテナの左側の境界線に沿って揃えます。指定されたパディングの値を使用します。 |
     | `Center` | 指定されたパディングを許容して、親コンテナの中央にリストを揃えます。 |
     | `Right` | 指定されたパディングの値を使用して、親コンテナの右側の境界線に沿ってブロックを揃えます。 |

     {style="table-layout:auto"}

   - を設定します。 **[!UICONTROL Border]** テキストコンテナの 4 つの側面すべてに適用されるスタイル：

     | オプション | 説明 |
     | ------ |------------ |
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

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各隅を囲むために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション） **[!UICONTROL CSS classes]** 現在のスタイルシートからコンテナに適用します。

     複数のクラス名はスペースで区切ります。

   - 次の値をピクセル単位で入力します。 **[!UICONTROL Margins and Padding]** を使用して、テキストコンテナの外側の余白と内側のパディングを指定します。

     ダイアグラムに対応する値を入力します。

     | コンテナ領域 | 説明 |
     | -------------- |------------ |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完了したら、「 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。
