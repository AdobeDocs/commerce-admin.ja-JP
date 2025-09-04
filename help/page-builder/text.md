---
title: 要素 – テキスト
description: ステージでテキストコンテナを追加するために使用される、テキストコンテンツタイプについて説明  [!DNL Page Builder]  ます。
exl-id: 3f14af35-9c04-4f4b-b3dd-d3406d56a9c0
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# 要素 – テキスト

_テキスト_ コンテンツタイプを使用して、WYSIWYG（「What You See Is What You Get」）エディターを含むテキストコンテナを [[!DNL Page Builder]  ステージ ](workspace.md#stage) に追加します。 また、エディターツールバーからテキストにリンク、画像、[ 変数 ](../systems/variables-predefined.md) およびウィジェットを追加できます。

![ バナー上の書式付きテキスト ](./assets/pb-storefont-banner-with-button.png){width="700"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## テキストエディターツール

テキストエディターには、ステージから直接アクセスすることも、設定ページからアクセスすることもできます。 ステージに直接加えられた変更は、自動的に保存されます。 詳しくは、[ エディターの使用 ](../content-design/editor.md) を参照してください。

![ テキストエディターツール - TinyMCE](./assets/pb-elements-text-editor-tools.png){width="600"}

## テキストコンテナツールボックス

![ テキストコンテナツールボックス ](./assets/pb-elements-text-toolbox.png){width="600"}

| ツール | アイコン | 説明 |
| --------- | --------------------- | -------------- |
| 移動 | ![ 移動アイコン ](./assets/pb-icon-move.png){width="25"} | テキスト コンテナをページ上の別の有効な場所に移動します。 |
| （ラベル） | テキスト | 現在のコンテナをテキスト要素として識別します。 |
| 設定 | ![ 設定アイコン ](./assets/pb-icon-settings.png){width="25"} | テキストコンテナのプロパティを編集モードで開きます。 |
| Hide | ![ アイコンを非表示 ](./assets/pb-icon-hide.png){width="25"} | テキストコンテナを非表示にします。 |
| 表示 | ![ アイコンを表示 ](./assets/pb-icon-show.png){width="25"} | 非表示のテキストコンテナを表示します。 |
| 複製 | ![ 複製アイコン ](./assets/pb-icon-duplicate.png){width="25"} | テキストコンテナをコピーします。 |
| 削除 | ![ 削除アイコン ](./assets/pb-icon-remove.png){width="25"} | テキストコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## テキストを追加

1. [!DNL Page Builder] パネルで **[!UICONTROL Elements]** を展開し、**[!UICONTROL Text]** プレースホルダーをステージ上の行、列またはタブセットにドラッグします。

   ![ テキストプレースホルダーのステージへのドラッグ ](./assets/pb-elements-text-drag.png){width="600" zoomable="yes"}

1. 必要に応じて、エディターを使用してテキストの入力や書式設定を行います。

   詳しくは、[ エディターの使用 ](../content-design/editor.md) を参照してください。

   ![ コンテンツを含むテキストエディター ](./assets/pb-elements-text-editor.png){width="600"}

## リンクの作成

エディターの「リンクを挿入」ボタンを使用すると、ギャラリー内の画像にハイパーリンクを簡単に追加できます。 ただし、事前に URL があれば、テキスト内にインラインリンクを作成する場合にも使用できます。 ウィジェットボタンとは異なり、「リンクを挿入/編集」ボタンは、ストアのページ、製品、カテゴリには統合されません。

電話番号またはメールのリンクを作成するには、[ カスタム変数の追加 ](../systems/variables-custom.md) を参照してください。

1. ストアフロントで、リンクのターゲットにするページに移動し、リンク情報をコピーします。

   完全修飾 URL か、ストアドメインへの参照を省略する相対 URL のいずれかを使用できます。

   完全な URL - `https://mystore.com/women/tops-women/tees-women.html`

   相対 URL - `../women/tops-women/tees-women.html`

1. エディタースペースでテキストを選択し、エディターツールバーの _リンクを挿入/編集_ （![ リンクを挿入/編集ボタン ](./assets/pb-icon-add-link.png){width="20"}）をクリックします。

   ![ 書式設定されたテキストへのリンクの追加 ](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="500" zoomable="yes"}

1. **[!UICONTROL URL]**：準備した相対リンクを入力します。

1. **[!UICONTROL Target]** を `None` に設定します。

   この設定の場合、ページは新しいタブを開かずに同じブラウザーウィンドウで開きます。

1. **[!UICONTROL Title]** には、`Shop Tees` と入力します。

   `Title` リンク属性は、一部のブラウザーでツールヒントとして使用されます。

1. リンクを保存して [!DNL Page Builder] ワークスペースに戻るには、「**[!UICONTROL OK]**」をクリックします。

   ![ リンクの詳細 ](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="500" zoomable="yes"}

## 画像の挿入

1. 画像を挿入するテキスト内の位置にカーソルを置きます。

1. エディターツールバーの _画像を挿入/編集_ （![ 画像を挿入/編集ボタン ](./assets/icon-pb-add-image.png){width="20"}）をクリックします。

1. **[!UICONTROL Source]**：検索アイコンをクリックし、メディア ストレージを使用して画像を検索および選択します。

1. **[!UICONTROL Image Description]**：画像の説明テキストを入力します。

   このテキストは、画像の `alt` リンク属性に設定され、一部のブラウザーでアクセシビリティのために使用されます。

1. ページ上の画像のレンダリングに使用する幅と高さの **[!UICONTROL Dimensions]** をピクセル単位で入力します。

   画像の縦横比を自動的に維持するには、「**[!UICONTROL Constrain proportions]**」チェックボックスをオンのままにします。

1. 画像を挿入して [!DNL Page Builder] ワークスペースに戻るには、[**[!UICONTROL OK]**] をクリックします。

## テキスト設定の変更

1. テキストコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   >[!NOTE]
   >
   >テキストコンテナは別のコンテナ内に密にネストされているので、正しいツールボックスがあることを確認してください。

1. 必要に応じてコンテンツを更新します。

1. 必要に応じて、_[!UICONTROL Advanced]_&#x200B;設定を更新します。

   - 親コンテナ内のテキストの位置を制御するには、**[!UICONTROL Alignment]** のいずれかを選択します。

     | オプション | 説明 |
     | ------ |------------ |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | 親コンテナの左罫線に沿ってリストを配置します。指定したパディングはすべて許可されます。 |
     | `Center` | 親コンテナの中央にリストを揃えます。指定したパディングに対する許容値を使用します。 |
     | `Right` | 親コンテナの右端に沿ってブロックを配置します。指定したパディングは許可されます。 |

     {style="table-layout:auto"}

   - テキストコンテナの 4 つの辺すべてに適用する **[!UICONTROL Border]** スタイルを設定します。

     | オプション | 説明 |
     | ------ |------------ |
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

   - `None` 以外の境界線のスタイルを設定する場合は、境界線の表示オプションを完了します。

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション）コンテナに適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

     複数のクラス名はスペースで区切ります。

   - テキストコンテナの外側の余白と内側のパディングを決定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

     対応する値を図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- |------------ |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション：`Top`/`Right`/`Bottom`/`Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション：`Top`/`Right`/`Bottom`/`Left` |

     {style="table-layout:auto"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
