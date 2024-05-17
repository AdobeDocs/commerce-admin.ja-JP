---
title: コンテンツを追加 – 製品Recommendations
description: にレコメンデーションのリストを追加するために使用される、Product Recommendations コンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 2f86421311b218d39c1abebaf117b8af0be5ea5d
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# コンテンツを追加 – 製品Recommendations

の使用 _製品のRecommendations_ 既存のアクティブなコンテンツ タイプを追加 [レコメンデーションユニット](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) に [[!DNL Page Builder] ステージ](workspace.md#stage) CMS ページ、ブロック、またはダイナミックブロックの場合。

>[!NOTE]
>
>この [!DNL Page Builder] _製品のRecommendations_ コンテンツタイプはAdobe Commerce 2.4.4 以降でサポートされており、で利用できます。 [Product Recommendations metapackage バージョン 3.0.x 以降](https://commercemarketplace.adobe.com/magento-product-recommendations.html). 追加 [!DNL Page Builder] 製品Recommendationsのサポート [インストール情報を参照してください](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure). **このコンテンツ タイプはMagento Open Sourceに使用できません。**

{{$include /help/_includes/page-builder-save-timeout.md}}

## 製品Recommendationsツールボックス

| ツール | アイコン | 説明 |
| --- | --| --- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | 製品レコメンデーションコンテナとそのコンテンツをステージ上の別の位置に移動します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 製品レコメンデーションを編集ページを開きます。このページで、レコメンデーションユニットを選択し、コンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在の製品レコメンデーションコンテナとそのコンテンツを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示の製品レコメンデーションコンテナとそのコンテンツを表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | 製品レコメンデーションコンテナとそのコンテンツの複製を作成します。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | 製品レコメンデーションコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 既存のレコメンデーションユニットの追加

1. 既にしていることを確認します [レコメンデーションユニットの作成](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) の場合 [!DNL Page Builder] ページタイプ。

>[!NOTE]
>
>のレコメンデーションユニットを作成できます [!DNL Page Builder] デフォルトストア表示のページタイプのみ。

1. ページ、ブロック、またはダイナミックブロックを編集モードで開きます。

1. を展開します。 _[!UICONTROL Content]_セクションでクリック&#x200B;**[!UICONTROL Edit with Page Builder]**またはコンテンツプレビュー領域内で、を開きます。 [!DNL Page Builder] ワークスペース。

1. が含まれる [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、ドラッグ：**[!UICONTROL Row]**ステージへのプレースホルダー。

1. が含まれる [!DNL Page Builder] 下のパネル _[!UICONTROL Add Content]_、ドラッグ：**[!UICONTROL Product Recommendation]**行のプレースホルダー。

   ![製品レコメンデーションコンテンツタイプの追加](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. 次のいずれかの操作を行います。

   - クリック **[!UICONTROL Edit Product Recommendation]**.
   - 空のコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （![設定アイコン](./assets/pb-icon-settings.png)） アイコンをクリックします。

   ![製品レコメンデーションを編集](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. が含まれる _[!UICONTROL Selection]_セクションで、をクリック&#x200B;**[!UICONTROL Select]**.

1. アクティブな商品レコメンデーションのリストで、追加するレコメンデーションユニットを含む行を見つけて、クリックします **[!UICONTROL Select]** 最後の列

   ![選択済みの製品レコメンデーション](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. 右上隅のをクリックします。 **[!UICONTROL Add Selected]**.

   選択した製品レコメンデーションの名前がに表示されます _[!UICONTROL Selection]_の節_[!UICONTROL Edit Product Recommendation]_ ページ。

1. に必要な変更を加えます [詳細設定](#advanced-settings).

   ![製品レコメンデーションを編集](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. 完了したら、次の手順を実行します。

   - 完全に最大化されたブラウザーウィンドウを使用する場合は、 _全画面表示を閉じる_ （![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png)） アイコンでワークスペースの右上隅に表示されます。

   - クリック **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

   ステージに戻ると、製品プレースホルダー画像がコンテナに表示されます。

## レコメンデーションユニット設定の編集

1. レコメンデーションユニットコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （![設定アイコン](./assets/pb-icon-settings.png)） アイコンをクリックします。

   ![推奨ツールボックス](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. に必要な変更を加えます [詳細設定](#advanced-settings).

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

## レコメンデーションユニットの複製

1. レコメンデーションユニットコンテナにカーソルを合わせてツールボックスを表示し、 _複製_ （![アイコンを複製](./assets/pb-icon-duplicate.png)） アイコンをクリックします。

   複製は、元の画像のすぐ下に表示されます。

1. 複製したレコメンデーションユニットを新しい位置に移動するには、コンテナの上にマウスポインターを置いて、 _移動_ （![移動アイコン](./assets/pb-icon-move.png)） アイコンをクリックします。

1. 推奨単位を選択して、新しい位置に赤いガイドラインが表示されるまでドラッグします。

   レコメンデーションユニットを移動すると、各コンテナの上部と下部の境界線が破線で表示されます。

## レコメンデーションユニットをステージから削除

1. レコメンデーションユニットコンテナにマウスポインターを置いて、 _削除_ （ ![アイコンを削除](./assets/pb-icon-remove.png)） アイコンをクリックします。

1. 確認を求められたら、 **[!UICONTROL OK]**.

## 詳細設定

1. 親コンテナ内の商品Recommendationsユニットの位置を制御するには、 **[!UICONTROL Alignment]**:

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
   | `Left` | 親コンテナの左境界に沿って単位を配置します。指定したパディングは許容されます。 |
   | `Center` | 親コンテナの中央に単位を配置します。指定したパディングに対する許容値を使用します。 |
   | `Right` | 親コンテナの右端に沿って単位を配置します。指定したパディングは許容されます。 |

   {style="table-layout:auto"}

1. を **[!UICONTROL Border]** product Recommendationsユニットの 4 つの側面すべてに適用されるスタイル：

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

1. 境界線のスタイルを `None`の場合は、次のボーダー表示オプションを入力します。

   | オプション | 説明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
   | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
   | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

   {style="table-layout:auto"}

1. （オプション）の名前を指定します **[!UICONTROL CSS classes]** 単位に適用する現在のスタイルシートから。

   複数のクラス名はスペースで区切ります。

1. 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** ユニットの外側の余白と内側のパディングを決定します。

   対応する値を図に入力します。

   | コンテナ領域 | 説明 |
   | ------ | ----------- |
   | [!UICONTROL Margins] | ユニットのすべての側面の外側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | ユニットのすべての側面の内側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
