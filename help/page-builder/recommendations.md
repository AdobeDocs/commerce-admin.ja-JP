---
title: コンテンツを追加 – 製品レコメンデーション
description: レコメンデーションのリストをステージに追加するために使用される、Product Recommendations コンテンツタイプについて説明  [!DNL Page Builder]  ます。
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# コンテンツを追加 – 製品レコメンデーション

_Product Recommendations_ コンテンツタイプを使用して、CMS ページ、ブロック、動的ブロックの [[!DNL Page Builder]  ステージ ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) にアクティブな既存の [ レコメンデーションユニット ](workspace.md#stage) を追加します。

>[!NOTE]
>
>[!DNL Page Builder]_Product Recommendations_ コンテンツタイプは、Adobe Commerce 2.4.4 以降でサポートされ、[Product Recommendations metapackage バージョン 3.0.x 以降 ](https://commercemarketplace.adobe.com/magento-product-recommendations.html) で利用できます。 Product Recommendations のサポートを追加する [!DNL Page Builder] は、[ インストール情報を参照 ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure) してください。 **このコンテンツタイプは、Magento Open Sourceでは使用できません。**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Product Recommendations ツールボックス

| ツール | アイコン | 説明 |
| --- | --| --- |
| 移動 | ![ 移動アイコン ](./assets/pb-icon-move.png){width="25"} | 製品レコメンデーションコンテナとそのコンテンツをステージ上の別の位置に移動します。 |
| 設定 | ![ 設定アイコン ](./assets/pb-icon-settings.png){width="25"} | 製品レコメンデーションを編集ページを開きます。このページで、レコメンデーションユニットを選択し、コンテナのプロパティを変更できます。 |
| Hide | ![ アイコンを非表示 ](./assets/pb-icon-hide.png){width="25"} | 現在の製品レコメンデーションコンテナとそのコンテンツを非表示にします。 |
| 表示 | ![ アイコンを表示 ](./assets/pb-icon-show.png){width="25"} | 非表示の製品レコメンデーションコンテナとそのコンテンツを表示します。 |
| 複製 | ![ 複製アイコン ](./assets/pb-icon-duplicate.png){width="25"} | 製品レコメンデーションコンテナとそのコンテンツの複製を作成します。 |
| 削除 | ![ 削除アイコン ](./assets/pb-icon-remove.png){width="25"} | 製品レコメンデーションコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 既存のレコメンデーションユニットの追加

1. [!DNL Page Builder] ページタイプの [ レコメンデーションユニットの作成 ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) が完了していることを確認します。

>[!NOTE]
>
>[!DNL Page Builder] ページタイプのレコメンデーションユニットは、デフォルトストア表示でのみ作成できます。

1. ページ、ブロック、またはダイナミックブロックを編集モードで開きます。

1. 「_[!UICONTROL Content]_」セクションを展開し、コンテンツプレビュー領域の&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;または内部をクリックして、[!DNL Page Builder] ワークスペースを開きます。

1. [!DNL Page Builder] パネルの _[!UICONTROL Layout]_&#x200B;の下にある&#x200B;**[!UICONTROL Row]**&#x200B;プレースホルダーをステージにドラッグします。

1. [!DNL Page Builder] パネルの _[!UICONTROL Add Content]_&#x200B;の下で、**[!UICONTROL Product Recommendation]**&#x200B;プレースホルダーを行にドラッグします。

   ![ 製品レコメンデーションコンテンツタイプの追加 ](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. 次のいずれかの操作を行います。

   - 「**[!UICONTROL Edit Product Recommendation]**」をクリックします。
   - 空のコンテナの上にマウスポインターを置いてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png)）アイコンをクリックします。

   ![ 製品レコメンデーションを編集 ](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. 「_[!UICONTROL Selection]_」セクションで、「**[!UICONTROL Select]**」をクリックします。

1. アクティブな商品レコメンデーションのリストで、追加するレコメンデーションユニットを含む行を見つけ、最後の列の **[!UICONTROL Select]** をクリックします。

   ![ 選択した製品のレコメンデーション ](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. 右上隅の「**[!UICONTROL Add Selected]**」をクリックします。

   選択した製品レコメンデーションの名前が、_[!UICONTROL Edit Product Recommendation]_&#x200B;のページの「_[!UICONTROL Selection]_」セクションに表示されます。

1. [ 詳細設定 ](#advanced-settings) に必要な変更を加えます。

   ![ 製品レコメンデーションを編集 ](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. 完了したら、次の手順を実行します。

   - 最大化されたブラウザーウィンドウで作業する場合は、ワークスペースの右上隅にある _全画面表示を閉じる_ （![ 全画面表示を閉じるアイコン ](./assets/pb-icon-reduce.png)）アイコンをクリックします。

   - 「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

   ステージに戻ると、製品プレースホルダー画像がコンテナに表示されます。

## レコメンデーションユニット設定の編集

1. レコメンデーションユニットコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png)）アイコンをクリックします。

   ![ レコメンデーションツールボックス ](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. [ 詳細設定 ](#advanced-settings) に必要な変更を加えます。

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

## レコメンデーションユニットの複製

1. レコメンデーションユニットコンテナにカーソルを合わせてツールボックスを表示し、ツールボックスの _複製_ （![ 複製アイコン ](./assets/pb-icon-duplicate.png)）アイコンをクリックします。

   複製は、元の画像のすぐ下に表示されます。

1. 複製されたお勧めユニットを新しい位置に移動するには、コンテナの上にマウスポインターを置いて、ツールボックスの _移動_ （![ 移動アイコン ](./assets/pb-icon-move.png)）アイコンをクリックします。

1. 推奨単位を選択して、新しい位置に赤いガイドラインが表示されるまでドラッグします。

   レコメンデーションユニットを移動すると、各コンテナの上部と下部の境界線が破線で表示されます。

## レコメンデーションユニットをステージから削除

1. レコメンデーションユニットコンテナにマウスポインターを置き、ツールボックスの _削除_ （![ 削除アイコン ](./assets/pb-icon-remove.png)）アイコンをクリックします。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL OK]**」をクリックします。

## 詳細設定

1. 親コンテナ内の Product Recommendations ユニットの位置を制御するには、**[!UICONTROL Alignment]** のいずれかを選択します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
   | `Left` | 親コンテナの左境界に沿って単位を配置します。指定したパディングは許容されます。 |
   | `Center` | 親コンテナの中央に単位を配置します。指定したパディングに対する許容値を使用します。 |
   | `Right` | 親コンテナの右端に沿って単位を配置します。指定したパディングは許容されます。 |

   {style="table-layout:auto"}

1. Product Recommendations ユニットの 4 つの側面すべてに適用される **[!UICONTROL Border]** スタイルを設定します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 関連付けられたスタイル シートで指定されている既定の罫線スタイルを適用します。 |
   | `None` | ユニットの境界の表示は提供されません。 |
   | `Dotted` | 単位の境界線は点線で表示されます。 |
   | `Dashed` | 単位の境界は破線で表示されます。 |
   | `Solid` | 単位の境界は実線で表示されます。 |
   | `Double` | 単位の境界線は二重線で表示されます。 |
   | `Groove` | 単位境界は溝付き線として表示されます。 |
   | `Ridge` | ユニットの境界は稜線として表示されます。 |
   | `Inset` | 単位の境界はインセット線として表示されます。 |
   | `Outset` | 単位の境界線は、先頭行として表示されます。 |

   {style="table-layout:auto"}

1. `None` 以外の境界線のスタイルを設定する場合は、境界線の表示オプションを完了します。

   | オプション | 説明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
   | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
   | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

   {style="table-layout:auto"}

1. （オプション）単位に適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

   複数のクラス名はスペースで区切ります。

1. 単位の外側の余白と内側のパディングを決定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

   対応する値を図に入力します。

   | コンテナ領域 | 説明 |
   | ------ | ----------- |
   | [!UICONTROL Margins] | ユニットのすべての側面の外側の端に適用される空白スペースの量。 オプション：`Top`/`Right`/`Bottom`/`Left` |
   | [!UICONTROL Padding] | ユニットのすべての側面の内側の端に適用される空白スペースの量。 オプション：`Top`/`Right`/`Bottom`/`Left` |

   {style="table-layout:auto"}
