---
title: コンテンツを追加 – 動的ブロック
description: 再利用可能な動的ブロックを [!DNL Page Builder] 段階に追加するために使用される動的ブロック コンテンツ タイプについて説明します。
exl-id: 04c90f47-9e32-4d34-ac0d-a2f2cec95ffc
feature: Page Builder, Page Content
TQID: https://experienceleague.adobe.com/5M3Pz-NB6CdERDJj8lhHzj6ibsR0NJ-bVgpfUG7cdPw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 827
ht-degree: 0%

---

# コンテンツを追加 – 動的ブロック

動的ブロックのコンテンツタイプを使用して、既存の[動的ブロック ](../content-design/dynamic-blocks.md)を[[!DNL Page Builder]  ステージ ](workspace.md#stage)に追加します。

![ ストアフロントの動的ブロック ](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 動的ブロックツールボックス

| ツール | アイコン | 説明 |
| --------- | ------------- | ----------------- |
| 移動 | ![移動アイコン ](./assets/pb-icon-move.png){width="25"} | ブロックコンテナとそのコンテンツをステージ上の別の位置に移動します。 |
| 設定 | ![設定アイコン ](./assets/pb-icon-settings.png){width="25"} | _ブロックを編集_ ページを開きます。このページでは、ブロックを選択してコンテナのプロパティを変更できます。 |
| 非表示 | ![ アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在のブロックコンテナとそのコンテンツを非表示にします。 |
| 表示 | ![ アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のブロックコンテナとそのコンテンツを表示します。 |
| 重複 | ![ アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | ブロックコンテナとそのコンテンツのコピーを作成します。 |
| 削除 | ![ アイコンを削除](./assets/pb-icon-remove.png){width="25"} | ブロックコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 既存のダイナミックブロックをステージに追加

1. 対象ページ、ブロック、製品、またはカテゴリの[!DNL Page Builder] ワークスペースに移動します。

1. [!DNL Page Builder] パネルで、**[!UICONTROL Add Content]**&#x200B;を展開し、**[!UICONTROL Dynamic Block]** プレースホルダーをステージにドラッグします。

   ![動的ブロックプレースホルダーをステージにドラッグする](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. 空の動的ブロックコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![動的ブロックツールボックス ](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. _動的ブロックを編集_ ページで、**[!UICONTROL Select Dynamic Block]**&#x200B;をクリックし、リストを使用してブロックを選択します。

   ![動的ブロックの選択](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

   リストで、挿入する動的ブロックを見つけて、**[!UICONTROL Select]**&#x200B;をクリックします。 次に、**[!UICONTROL Add Selected]**&#x200B;をクリックします。

   ![ リスト内の動的ブロックの選択](./assets/pb-add-content-dynamic-block-select-list.png){width="600" zoomable="yes"}

   ダイナミックブロック情報の概要を以下に示します。

   ![動的ブロックの概要](./assets/pb-add-content-dynamic-block-summary.png){width="600" zoomable="yes"}

1. **[!UICONTROL Template]**&#x200B;を次のいずれかに設定します：

   | オプション | 説明 |
   | ------ | ----------- |
   | `Dynamic Block Block Template` | スタンドアロンブロックを追加します。 |
   | `Dynamic Block Inline Template` | ブロックの内容をテキストに挿入します。 |

   {style="table-layout:auto"}

   ![動的ブロックテンプレート ](./assets/pb-add-content-dynamic-block-template.png){width="200"}

1. 必要に応じて、詳細設定を行います。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

### 詳細設定

1. 親コンテナ内の動的ブロックの位置を制御するには、**[!UICONTROL Alignment]**&#x200B;を選択します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイルシートで指定されている整列のデフォルト設定を適用します。 |
   | `Left` | 親コンテナの左端に沿ってリストを整列させ、指定されたパディングを許可します。 |
   | `Center` | 親コンテナの中央にリストを整列させ、指定された任意のパディングを許可します。 |
   | `Right` | 親コンテナの右端に沿ってブロックを整列させ、指定されたパディングを許可します。 |

   {style="table-layout:auto"}

1. 動的ブロックコンテナのすべての4つの側面に適用される&#x200B;**[!UICONTROL Border]** スタイルを設定します。

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

1. **[!UICONTROL Margins and Padding]**&#x200B;の値をピクセル単位で入力して、ダイナミックブロックコンテナの外側の余白と内側の余白を決定します。

   対応する値をダイアグラムに入力します。

   | コンテナ領域 | 説明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | コンテナのすべての側面の外側のエッジに適用される空白スペースの量。 オプション：`Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | コンテナのすべての側面の内側エッジに適用される空白スペースの量。 オプション：`Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## 動的ブロックコンテナ設定の編集

1. 動的ブロックコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![動的ブロックツールボックス ](./assets/pb-add-content-dynamic-block-toolbox.png){width="500" zoomable="yes"}

1. 必要に応じて、ダイナミックブロックを変更します。

   - **[!UICONTROL Select Dynamic Block]**&#x200B;をクリックします。

     ![別の動的ブロックを選択しています](./assets/pb-add-content-dynamic-block-select.png){width="20"}

   - アクティブな動的ブロックのリストで、追加するブロックの&#x200B;**[!UICONTROL Select]**&#x200B;をクリックします。

1. 必要に応じて、残りの設定を更新します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

## 動的ブロックの複製

1. 動的ブロックコンテナにカーソルを合わせてツールボックスを表示し、_複製_ （![複製アイコン ](./assets/pb-icon-duplicate.png){width="20"}）アイコンを選択します。

   複製はオリジナルのすぐ下に表示されます。

   ![動的ブロックの複製](./assets/pb-add-content-dynamic-block-duplicate.png){width="500" zoomable="yes"}

1. 新しいダイナミックブロックを別の位置に移動するには、そのコンテナにカーソルを合わせ、ツールボックスで&#x200B;_移動_ （![移動アイコン ](./assets/pb-icon-move.png){width="20"}）を選択します。

1. 新しい位置に赤いガイドラインが表示されるまで、ダイナミックブロックを選択してドラッグします。

   各コンテナの上下の境界線は、ダイナミックブロックを移動すると破線で表示されます。

## ステージからダイナミックブロックを削除

1. 動的ブロックコンテナにカーソルを合わせてツールボックスを表示し、_削除_ （![削除アイコン ](./assets/pb-icon-remove.png){width="20"}）アイコンを選択します。

1. 確認を求められたら、**[!UICONTROL OK]**&#x200B;をクリックします。

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
