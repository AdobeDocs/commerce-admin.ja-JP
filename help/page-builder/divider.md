---
title: 要素 – ディバイダ
description: ' [!DNL Page Builder] 段階のコンテンツのセクション間にルールを視覚的な区切りとして追加するために使用されるディバイダ コンテンツ タイプについて説明します。'
exl-id: e1052170-6d2f-4893-a78b-a845a8b6c0d9
feature: Page Builder, Page Content
TQID: https://experienceleague.adobe.com/6OxxIz3QSkS2S8yRRrnrKj8iF60zp-qM3SGZIyJRTeA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 903
ht-degree: 0%

---

# 要素 – ディバイダ

_Divider_ コンテンツ タイプを使用して、[[!DNL Page Builder]  ステージ ](workspace.md#stage)のコンテンツのセクション間にルールを視覚的な区切りとして追加します。 境界線の色、太さ、幅を指定できます。 また、整列の制御、余白とパディングの設定、コンテナの境界線の形式を行うこともできます。 デフォルトでは、区切り記号は、コンテナの全幅を拡張するヘアライン規則で、パディングを許可します。

![境界線のないコンテナ内のデフォルトの区切り記号](./assets/pb-elements-divider-default.png){width="500" zoomable="yes"}

ほとんどの区切りコンテナは表示されませんが、次の例では、区切り記号、パディング、コンテナ間の関係を確認できるように、コンテナに赤い破線が表示されています。 区切り記号の上下のパディングを調整して、エレメント間の間隔を制御できます。

![境界線が点線のコンテナ内にパディングを持つディバイダー](./assets/pb-elements-divider-default-border-dashed.png){width="500" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 区切りツール ボックス

| ツール | アイコン | 説明 |
| ---- | --------------------| ------------|
| 移動 | ![移動アイコン ](./assets/pb-icon-move.png){width="25"} | 区切りコンテナをページ上の別の有効な場所に移動します。 |
| （ラベル） | 区切り記号 | 現在のコンテナをディバイダ要素として識別します。 |
| 設定 | ![設定アイコン ](./assets/pb-icon-settings.png){width="25"} | ディバイダを編集ページが開き、ディバイダとそのコンテナのプロパティを変更できます。 |
| 非表示 | ![ アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | ディバイダーコンテナを非表示にします。 |
| 表示 | ![ アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示の仕切りコンテナを表示します。 |
| 重複 | ![ アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | ディバイダーコンテナのコピーを作成します。 |
| 削除 | ![ アイコンを削除](./assets/pb-icon-remove.png){width="25"} | 分割コンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 区切り記号を追加

1. [!DNL Page Builder] パネルで、**[!UICONTROL Elements]**&#x200B;を展開し、**[!UICONTROL Divider]** プレースホルダーをステージ上の行、列、またはタブ セットにドラッグします。

   ステージ上の別のコンテンツコンテナの前または後に区切りを配置する場合は、赤いガイドラインを参照してください。

   ![区切りをステージにドラッグする](./assets/pb-elements-divider-drag.png){width="600" zoomable="yes"}

   次の例では、区切り記号はテキストの新しいセクションの先頭をマークします。

   ![ テキストのセクションを区切る](./assets/pb-elements-dividers-multiple-text-row.png){width="500" zoomable="yes"}

1. 新しいディバイダの設定を指定するには、次の手順に従います。

## 区切り記号の設定の変更

1. 分割コンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![ ディバイダーツールボックス ](./assets/pb-elements-divider-toolbox.png){width="500" zoomable="yes"}

1. 次のいずれかの方法を使用して区切り記号&#x200B;**[!UICONTROL Line Color]**&#x200B;を変更します。

   - 有効な[HTML カラー名](https://en.wikipedia.org/wiki/Web_colors)を入力してください。 例：`Teal`。
   - 16進数カラー値を入力します。 例：`#008080`。

   完了したら、**[!UICONTROL Apply]**&#x200B;をクリックします。

   ![線の色を設定しています](./assets/pb-elements-divider-settings-line-color.png){width="600" zoomable="yes"}

1. **[!UICONTROL Line Thickness]**&#x200B;をピクセル単位で入力します。

1. 測定単位を示すには、**[!UICONTROL Line Width]**&#x200B;の後に`px`または`%`を入力します。

   ![線の色、太さ、幅の設定](./assets/pb-elements-divider-settings-line-color-thickness-width.png){width="600" zoomable="yes"}

1. 必要に応じて&#x200B;_[!UICONTROL Advanced]_設定を更新します。

   - 親コンテナ内の区切り記号の位置を制御するには、**[!UICONTROL Alignment]**&#x200B;を選択します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイルシートで指定されている整列のデフォルト設定を適用します。 |
     | `Left` | 親コンテナの左端に沿ってリストを整列させ、指定されたパディングを許可します。 |
     | `Center` | 親コンテナの中央にリストを整列させ、指定された任意のパディングを許可します。 |
     | `Right` | 親コンテナの右端に沿ってブロックを整列させ、指定されたパディングを許可します。 |

     {style="table-layout:auto"}

     次の例では、区切り記号に中央揃えを使用するようにオプションが設定されています。

     ![中央揃えの分割線](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - 分割コンテナのすべての4つの側面に適用される&#x200B;**[!UICONTROL Border]** スタイルを設定します。

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

   - `None`以外の境界線スタイルを設定する場合は、境界線の表示オプションを完了します。

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 色見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の16進数値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | 境界線の各隅を丸めるために使用する半径のサイズを定義するピクセル数を入力します。 |

     {style="table-layout:auto"}

   - （オプション）現在のスタイルシートから&#x200B;**[!UICONTROL CSS classes]**&#x200B;の名前を指定して、コンテナに適用します。

     複数のクラス名はスペースで区切ります。

   - **[!UICONTROL Margins and Padding]**&#x200B;の値をピクセル単位で入力して、区切りコンテナの外側の余白と内側の余白を決定します。

     対応する値をダイアグラムに入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側のエッジに適用される空白スペースの量。 オプション：`Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側エッジに適用される空白スペースの量。 オプション：`Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

   ![行の中央に区切り記号](./assets/pb-elements-divider-settings-2px-centered.png){width="500" zoomable="yes"}

## 区切り記号の複製

特定の設定を持つ書式設定されたディバイダの場合は、新しいプレースホルダーで始めるのではなく、複製を作成する方が効率的です。

1. 分割コンテナにカーソルを合わせてツールボックスを表示し、_複製_ （![複製アイコン ](./assets/pb-icon-duplicate.png){width="20"}）アイコンを選択します。

   重複するディバイダーコンテナが元のコンテナのすぐ下に表示されます。

   ![重複分割](./assets/pb-elements-divider-duplicate.png){width="500" zoomable="yes"}

1. 新しいディバイダーコンテナにカーソルを合わせてツールボックスを表示し、_移動_ （![移動アイコン ](./assets/pb-icon-move.png){width="20"}）アイコンを選択します。

   ![仕切りの移動](./assets/pb-elements-divider-move.png){width="500" zoomable="yes"}

1. 赤いガイドラインが新しい位置を示すまで、区切り記号を選択してドラッグします。

   各コンテナの上下の境界線は、区切り線を移動すると破線として表示されます。

   ![複製された区切り記号を位置に移動](./assets/pb-elements-divider-move-guideline.png){width="500" zoomable="yes"}


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
