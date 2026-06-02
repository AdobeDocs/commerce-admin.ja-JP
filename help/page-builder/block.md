---
title: コンテンツを追加 – ブロック
description: 再利用可能なブロックを [!DNL Page Builder]  ステージに追加するために使用されるブロック コンテンツ タイプについて説明します。
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '794'
ht-degree: 0%

---

# コンテンツを追加 – ブロック

_ブロック_ コンテンツタイプを使用して、既存のアクティブな[&#x200B; ブロック &#x200B;](../content-design/blocks.md)を[[!DNL Page Builder]  ステージ &#x200B;](workspace.md#stage)に追加します。 次の例では、最初の列にページのサイドメニューを含むブロックが含まれています。 2番目の列には画像が含まれています。

![&#x200B; サイドメニュー付きブロック &#x200B;](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ツールボックスをブロック

| ツール | アイコン | 説明 |
| --------- | -------- | ------------- |
| 移動 | ![移動アイコン &#x200B;](./assets/pb-icon-move.png) | ブロックコンテナとそのコンテンツをステージ上の別の位置に移動します。 |
| 設定 | ![設定アイコン &#x200B;](./assets/pb-icon-settings.png) | ブロックを選択し、コンテナのプロパティを変更できる「ブロックを編集」ページを開きます。 |
| 非表示 | ![&#x200B; アイコンを非表示](./assets/pb-icon-hide.png) | 現在のブロックコンテナとそのコンテンツを非表示にします。 |
| 表示 | ![&#x200B; アイコンを表示](./assets/pb-icon-show.png) | 非表示のブロックコンテナとそのコンテンツを表示します。 |
| 重複 | ![&#x200B; アイコンを複製](./assets/pb-icon-duplicate.png) | ブロックコンテナとそのコンテンツのコピーを作成します。 |
| 削除 | ![&#x200B; アイコンを削除](./assets/pb-icon-remove.png) | ブロックコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 既存のブロックを追加

1. 対象ページ、ブロック、ダイナミックブロック、製品、またはカテゴリの[!DNL Page Builder] ワークスペースに移動します。

1. [!DNL Page Builder] パネルで、**[!UICONTROL Add Content]**&#x200B;を展開し、**[!UICONTROL Block]** プレースホルダーをステージにドラッグします。

   ![&#x200B; ブロックをステージにドラッグする](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. 空のブロックコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="25"}）アイコンを選択します。

1. **[!UICONTROL Select Block]**&#x200B;をクリックします。

   ![&#x200B; ブロックの選択](./assets/pb-add-content-block-select.png){width="200"}

1. 追加するブロックの行で、最後の列の&#x200B;**[!UICONTROL Select]**&#x200B;をクリックします。

   ![選択したブロック &#x200B;](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   選択したブロックの名前がページに表示されます。

   ![&#x200B; ブロック名](./assets/pb-add-content-block-name.png){width="200"}

1. 必要に応じて、このページの最後にあるフィールドの説明を参照して、残りの設定を完了します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

### 詳細設定

1. 親コンテナ内のブロックの位置を制御するには、**[!UICONTROL Alignment]**&#x200B;を選択します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイルシートで指定されている整列のデフォルト設定を適用します。 |
   | `Left` | 親コンテナの左端に沿ってリストを整列させ、指定されたパディングを許可します。 |
   | `Center` | 親コンテナの中央にリストを整列させ、指定された任意のパディングを許可します。 |
   | `Right` | 親コンテナの右端に沿ってブロックを整列させ、指定されたパディングを許可します。 |

   {style="table-layout:auto"}

1. ブロックコンテナのすべての4つの側面に適用される&#x200B;**[!UICONTROL Border]** スタイルを設定します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 関連付けられたスタイルシートで指定されたデフォルトの境界線スタイルを適用します。 |
   | `None` | コンテナの境界を表示しません。 |
   | `Dotted` | コンテナの境界線が点線で表示されます。 |
   | `Dashed` | コンテナの境界線が破線で表示されます。 |
   | `Solid` | コンテナの境界線が実線として表示されます。 |
   | `Double` | コンテナの境界線が2行で表示されます。 |
   | `Groove` | コンテナの境界線は、溝付き線として表示されます。 |
   | `Ridge` | コンテナの境界線は、うね付きの線として表示されます。 |
   | `Inset` | コンテナの境界線がインセット線として表示されます。 |
   | `Outset` | コンテナの境界線がアウトセット線として表示されます。 |

   {style="table-layout:auto"}

1. `None`以外の境界線スタイルを設定する場合は、境界線の表示オプションを完了します。

   | オプション | 説明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 色見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の16進数値を入力して、カラーを指定します。 |
   | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
   | [!UICONTROL Border Radius] | 境界線の各隅を丸めるために使用する半径のサイズを定義するピクセル数を入力します。 |

   {style="table-layout:auto"}

1. （オプション）現在のスタイルシートから&#x200B;**[!UICONTROL CSS classes]**&#x200B;の名前を指定して、コンテナに適用します。

   複数のクラス名はスペースで区切ります。

1. **[!UICONTROL Margins and Padding]**&#x200B;の値をピクセル単位で入力して、ブロックコンテナの外側の余白と内側の余白を決定します。

   対応する値をダイアグラムに入力します。

   | コンテナ領域 | 説明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | コンテナのすべての側面の外側のエッジに適用される空白スペースの量。 オプション：`Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | コンテナのすべての側面の内側エッジに適用される空白スペースの量。 オプション：`Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## ブロック設定の編集

1. ブロックコンテナにカーソルを合わせ、ツールボックスで&#x200B;_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="25"}）アイコンを選択します。

   ![&#x200B; ツールボックスをブロック &#x200B;](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. 別のブロックを選択するには、**[!UICONTROL Select Block]**&#x200B;をクリックします。

   - アクティブなブロックのリストで、追加するブロックの&#x200B;**[!UICONTROL Select]**&#x200B;をクリックします。
   - **[!UICONTROL Add Selected]**&#x200B;をクリックします。

1. 必要に応じて、このページの最後にあるフィールドの説明を参照して、残りの設定を更新します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

## ブロックの複製

1. ブロックコンテナにカーソルを合わせてツールボックスを表示し、_複製_ （![複製アイコン &#x200B;](./assets/pb-icon-duplicate.png)）アイコンを選択します。

   複製はオリジナルのすぐ下に表示されます。

1. 新しいブロックを新しい位置に移動するには、コンテナにカーソルを合わせ、ツールボックスの&#x200B;_移動_ （![移動アイコン &#x200B;](./assets/pb-icon-move.png)）をクリックします。

1. 新しい位置に赤いガイドラインが表示されるまで、ブロックを選択してドラッグします。

   各コンテナの上下の境界線は、ブロックの移動中に破線として表示されます。

## ステージからブロックを削除する

1. ブロックコンテナにカーソルを合わせてツールボックスを表示し、_削除_ （![削除アイコン &#x200B;](./assets/pb-icon-remove.png)）アイコンを選択します。

1. 確認を求められたら、**[!UICONTROL OK]**&#x200B;をクリックします。

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
