---
title: コンテンツを追加 — 動的ブロック
description: 再利用可能な動的ブロックを [!DNL Page Builder] ステージ。
exl-id: 04c90f47-9e32-4d34-ac0d-a2f2cec95ffc
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# コンテンツを追加 — 動的ブロック

既存のコンテンツを追加するには、ダイナミックブロックコンテンツタイプを使用します [動的ブロック](../content-design/dynamic-blocks.md) から [[!DNL Page Builder] ステージ](workspace.md#stage).

![ストアフロントのダイナミックブロック](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ダイナミックブロックツールボックス

| ツール | アイコン | 説明 |
| --------- | ------------- | ----------------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | ブロックコンテナとそのコンテンツをステージ上の別の位置に移動します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | を開きます。 _ブロックを編集_ ページに表示されます。このページでは、ブロックを選択し、コンテナのプロパティを変更できます。 |
| 非表示 | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在のブロックコンテナとそのコンテンツを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のブロックコンテナとそのコンテンツを表示します。 |
| 複製 | ![複製アイコン](./assets/pb-icon-duplicate.png){width="25"} | ブロックコンテナとそのコンテンツのコピーを作成します。 |
| 削除 | ![削除アイコン](./assets/pb-icon-remove.png){width="25"} | ステージからブロックコンテナとそのコンテンツを削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 既存のダイナミックブロックをステージに追加

1. 次に移動： [!DNL Page Builder] ワークスペース（ターゲットページ、ブロック、製品、カテゴリ）。

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Add Content]** をクリックし、 **[!UICONTROL Dynamic Block]** プレースホルダーをステージに追加します。

   ![ダイナミックブロックプレースホルダーのステージへのドラッグ](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. 空のダイナミックブロックコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![ダイナミックブロックツールボックス](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. 次の日： _ダイナミックブロックを編集_ ページ、クリック **[!UICONTROL Select Dynamic Block]** をクリックし、リストを使用してブロックを選択します。

   ![ダイナミックブロックの選択](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

   リストで、挿入するダイナミックブロックを探し、 **[!UICONTROL Select]**. 次に、「 **[!UICONTROL Add Selected]**.

   ![リスト内のダイナミックブロックの選択](./assets/pb-add-content-dynamic-block-select-list.png){width="600" zoomable="yes"}

   ダイナミックブロック情報の概要は、次のとおりです。

   ![ダイナミックブロックの概要](./assets/pb-add-content-dynamic-block-summary.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Template]** を次のいずれかに変更します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Dynamic Block Block Template` | スタンドアロンブロックを追加します。 |
   | `Dynamic Block Inline Template` | ブロックコンテンツをテキストに挿入します。 |

   {style="table-layout:auto"}

   ![ダイナミックブロックテンプレート](./assets/pb-add-content-dynamic-block-template.png){width="200"}

1. 必要に応じて、詳細設定を実行します。

1. 完了したら、「 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。

### 詳細設定

1. 親コンテナ内でのダイナミックブロックの位置を制御するには、 **[!UICONTROL Alignment]**:

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイルシートで指定された位置揃えの既定の設定を適用します。 |
   | `Left` | リストを親コンテナの左側の境界線に沿って揃えます。指定されたパディングの値を使用します。 |
   | `Center` | 指定されたパディングを許容して、親コンテナの中央にリストを揃えます。 |
   | `Right` | 指定されたパディングの値を使用して、親コンテナの右側の境界線に沿ってブロックを揃えます。 |

   {style="table-layout:auto"}

1. を設定します。 **[!UICONTROL Border]** ダイナミックブロックコンテナの 4 つの側面すべてに適用されるスタイル：

   | オプション | 説明 |
   | ------ | ----------- |
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

1. 次の条件を満たさない境界線のスタイルを設定した場合： `None`、境界線の表示オプションを設定します。

   | オプション | 説明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進値を入力して、カラーを指定します。 |
   | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
   | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各隅を囲むために使用する半径のサイズを定義します。 |

   {style="table-layout:auto"}

1. （オプション） **[!UICONTROL CSS classes]** 現在のスタイルシートからコンテナに適用します。

   複数のクラス名はスペースで区切ります。

1. 次の値をピクセル単位で入力します。 **[!UICONTROL Margins and Padding]** ダイナミックブロックコンテナの外側の余白と内側の余白を決定します。

   ダイアグラムに対応する値を入力します。

   | コンテナ領域 | 説明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## ダイナミックブロックコンテナ設定を編集

1. ダイナミックブロックコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![ダイナミックブロックツールボックス](./assets/pb-add-content-dynamic-block-toolbox.png){width="500" zoomable="yes"}

1. 必要に応じて、ダイナミックブロックを変更します。

   - クリック **[!UICONTROL Select Dynamic Block]**.

     ![別のダイナミックブロックの選択](./assets/pb-add-content-dynamic-block-select.png){width="20"}

   - アクティブな動的ブロックの一覧で、 **[!UICONTROL Select]** を追加するブロックに対して使用します。

1. 必要に応じて、残りの設定を更新します。

1. 完了したら、「 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。

## ダイナミックブロックを複製

1. ダイナミックブロックコンテナの上にマウスポインターを置いてツールボックスを表示し、 _複製_ ( ![複製アイコン](./assets/pb-icon-duplicate.png){width="20"} ) アイコンをクリックします。

   複製は元の画像のすぐ下に表示されます。

   ![ダイナミックブロックの複製](./assets/pb-add-content-dynamic-block-duplicate.png){width="500" zoomable="yes"}

1. 新しいダイナミックブロックを別の位置に移動するには、そのコンテナの上にマウスポインターを置いて、 _移動_ ( ![移動アイコン](./assets/pb-icon-move.png){width="20"} ) をツールボックスに追加します。

1. ダイナミックブロックを選択し、赤いガイドラインが新しい位置に表示されるまでドラッグします。

   各コンテナの上と下の境界線は、ダイナミックブロックを移動する際に破線で表示されます。

## ステージからダイナミックブロックを削除する

1. ダイナミックブロックコンテナの上にマウスポインターを置いてツールボックスを表示し、 _削除_ ( ![削除アイコン](./assets/pb-icon-remove.png){width="20"} ) アイコンをクリックします。

1. 確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.
