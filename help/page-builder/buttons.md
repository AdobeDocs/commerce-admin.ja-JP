---
title: 要素 – ボタン
description: ステージ内の個々のボタンまたは一連のボタンを追加するために使用される、ボタンコンテンツタイプについて説明  [!DNL Page Builder]  ます。
exl-id: 9f1681c5-04b0-4259-aaf6-5d8081bd8cdb
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1586'
ht-degree: 0%

---

# 要素 – ボタン

_ボタン_ コンテンツタイプを使用して、[[!DNL Page Builder]  ステージ ](workspace.md#stage) に個々のボタンまたは一連のボタンを追加します。 ボタンは水平方向または垂直方向に配置でき、ステージの行、列、タブ、バナーに直接追加できます。

![ 店頭にボタンが設置されているバナー ](./assets/pb-storefont-banner-with-button.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ツールボックス

ボタン コンテンツ タイプを使用する場合は、個々のボタンと、1 つ以上のボタンを保持するボタン コンテナを追加および編集します。 それぞれに独自のツールボックスがあり、[!DNL Page Builder] のステージでボタンのデザインに使用します。

### 個々のボタンのツールボックス

![ ボタンツールボックス ](./assets/pb-elements-button-settings.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | -------- | -------------- |
| 設定 | ![ 設定アイコン ](./assets/pb-icon-settings.png){width="25"} | 「編集ボタン」ページが開きます。このページで、ボタンのプロパティを変更できます。 |
| 複製 | ![ 複製アイコン ](./assets/pb-icon-duplicate.png){width="25"} | ボタンをコピーします。 |
| 削除 | ![ 削除アイコン ](./assets/pb-icon-remove.png){width="25"} | ステージからボタンを削除します。 |

{style="table-layout:auto"}

### ボタンコンテナツールボックス

![ ボタンコンテナツールボックス ](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ----------------- | ----------- |
| 移動 | ![ 移動アイコン ](./assets/pb-icon-move.png){width="25"} | ボタンコンテナをページ上の別の有効な場所に移動します。 |
| 追加 | ![ 追加アイコン ](./assets/pb-icon-add-button.png){width="25"} | コンテナにボタンを追加します。 |
| （ラベル） | ボタン | 現在のコンテナをボタン要素として識別します。 |
| 設定 | ![ 設定アイコン ](./assets/pb-icon-settings.png){width="25"} | 編集ボタン ページを開きます。このページで、コンテナのプロパティを変更できます。 |
| Hide | ![ アイコンを非表示 ](./assets/pb-icon-hide.png){width="25"} | ボタンコンテナを非表示にします。 |
| 表示 | ![ アイコンを表示 ](./assets/pb-icon-show.png){width="25"} | 非表示のボタンコンテナを表示します。 |
| 複製 | ![ 複製アイコン ](./assets/pb-icon-duplicate.png){width="25"} | ボタンコンテナをコピーします。 |
| 削除 | ![ 削除アイコン ](./assets/pb-icon-remove.png){width="25"} | ボタンコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 個々のボタンの追加

1. [!DNL Page Builder] パネルで **[!UICONTROL Elements]** を展開し、**[!UICONTROL Buttons]** プレースホルダーをステージ上の行、列またはタブセットにドラッグします。

   ![ ボタンのステージへのドラッグ ](./assets/pb-elements-button-drag.png){width="500" zoomable="yes"}

1. ボタンにカーソルを合わせてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png)）アイコンを選択します。

1. ボタンに表示する **[!UICONTROL Button Text]** を入力します。

   ![ 基本ボタンの設定 ](./assets/pb-elements-button-settings-button-text.png){width="600" zoomable="yes"}

1. **[!UICONTROL Button Type]** を次のいずれかに設定します。

   | タイプ | 説明 |
   | ------ | ----------- |
   | `Primary` | 現在のスタイル シートからプライマリ ボタン スタイルを適用します。 |
   | `Secondary` | 現在のスタイル シートからセカンダリ ボタン スタイルを適用します（該当する場合）。 |
   | `Link` | ボタンではなくハイパーリンクを作成します。 |

   {style="table-layout:auto"}

   ![プライマリおよびセカンダリボタンの例 ](./assets/pb-elements-button-settings-button-primary-secondary.png){width="500" zoomable="yes"}

1. 次のいずれかのタイプを使用して **[!UICONTROL Button Link]** を設定します。

   - **[!UICONTROL URL]** - リンクの宛先 URL を入力します。

     URL は、ストア内の製品またはページへの相対リンク、または完全修飾 URL にすることができます。

     相対 URL の例 – `../luma-analog-watch.html`

     完全修飾 URL の例 – `http://mystore.com/luma-analog-watch.html`

     リンクが別の web サイトに移動する場合は、新しいブラウザータブでリンクを開くことで、現在のページをストアで開いたままにすることができます。

     訪問者がストアから移動しないようにするには、「**[!UICONTROL Open in new tab]**」チェックボックスを選択します。

   - **[!UICONTROL Product]** – 製品名（一部または全部）または SKU を入力し、リストで製品名を選択します。

     >[!NOTE]
     >
     >製品は、「在庫切れの製品を表示 _設定に従ってリストに表示さ_ ます。 [Inventory management](../inventory-management/introduction.md) を使用しているマルチ Source マーチャントの場合、商品リストは、デフォルト web サイトにのみ割り当てられたソースによって制限されます。

     ![ ボタンリンクの製品の選択 ](./assets/pb-elements-button-settings-button-link-product-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - カテゴリ名（一部または全部）を入力するか、空白フィールドをクリックしてカテゴリツリーを表示します。 次に、ツリーでカテゴリ名を選択します。

     ![ ボタンリンクのカテゴリの選択 ](./assets/pb-elements-button-settings-button-link-category-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - CMS ページの名前（一部または全部）を入力するか、空白フィールドをクリックして完全なリストを表示します。 次に、検索結果リストでページの名前を選択します。

     ![ ボタンリンクの CMS ページを選択 ](./assets/pb-elements-button-settings-button-link-page-search.png){width="600" zoomable="yes"}

1. 必要に応じて [ 詳細設定 ][advanced-settings] を完了します。

1. 完了したら、右上隅の **[!UICONTROL Save]** をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

## 一連のボタンの追加

次のセクションでは、個々のボタンから開始して、ボタンコンテナ内に 3 つのボタンのセットを作成する一連の手順について説明します。 個々のボタンがまだない場合は、前の手順に従って、個々のボタンをステージに追加します。

### 手順 1:2 番目のボタンの作成

1. ボタンコンテナにカーソルを合わせてツールボックスを表示し、「_追加_ （![ 追加アイコン ](./assets/pb-icon-add-button.png){width="20"}）」アイコンを選択します。

   ![ 別のボタンの追加 ](./assets/pb-elements-buttons-toolbox-add.png){width="500" zoomable="yes"}

1. 2 番目のボタンに表示するテキストを入力します。

1. 新規ボタンをクリックしてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![ ボタンの編集 ](./assets/pb-elements-button-set-edit-button2-toolbox.png){width="500" zoomable="yes"}

1. **[!UICONTROL Button Type]** を `Secondary` に設定します。

1. 必要に応じて **[!UICONTROL Button Link]** を設定します。

   次の例では、リンクは、「お問い合わせ [ ページに移動する相対 URL で ](../getting-started/store-details.md#contact-us-form)。

   ![ お問い合わせボタンの設定 ](./assets/pb-elements-button-set-edit-button2-toolbox-settings.png){width="600" zoomable="yes"}

1. 必要に応じて [ 詳細設定 ][advanced-settings] を完了します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

### 手順 2:3 番目のボタンの作成

1. ステージの 2 番目のボタンを再度クリックし、「_複製_」（![ 複製アイコン ](./assets/pb-icon-duplicate.png){width="20"}）アイコンを選択します。

   ![ ボタンの複製 ](./assets/pb-elements-button-set-contact-us-toolbox-duplicate.png){width="500" zoomable="yes"}

1. 3 番目のボタンに表示するテキストを入力します。

1. 3 番目のボタンをクリックしてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![3 番目のボタンのツールボックス ](./assets/pb-elements-button-set-find-us-toolbox-settings.png){width="500" zoomable="yes"}

1. 必要に応じて **[!UICONTROL Button Link]** を更新します。

1. 右上隅にある「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

### 手順 3：ボタンコンテナの更新

1. ボタンコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![ ボタンコンテナツールボックス ](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

1. 「_[!UICONTROL Appearance]_」で、「**[!UICONTROL Stacked]**」を選択します。

1. **[!UICONTROL All Buttons are same size]** を `Yes` に設定します。

   ![ 同じサイズの積み重ねボタン ](./assets/pb-elements-buttons-settings-appearance-stacked.png){width="300"}

1. 必要に応じて、「ボタンコンテナの設定の変更 [ の説明を使用して残りの設定を更新し ][button-container] す。

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

   完全な積み重ねボタンセットがステージに表示され、1 つのプライマリボタンと 2 つのセカンダリボタンが表示されます。

   ![ ステージ上の積み重ねボタン ](./assets/pb-elements-buttons-stacked.png){width="500" zoomable="yes"}

## ボタンの移動

1. 移動するボタンをクリックします。

1. ボタンテキストの直前に表示される「移動」（![ 移動アイコン ](./assets/pb-icon-move.png){width="20"}）アイコンを選択して、ボタンコンテナ内のボタンの新しい位置にドラッグします。

   ![ ボタンの移動 ](./assets/pb-elements-button-set-move-button.png){width="500" zoomable="yes"}

## ボタンの設定の変更

1. ステージ上のボタンをクリックしてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![ ボタンツールボックス ](./assets/pb-elements-button-toolboxes.png){width="500" zoomable="yes"}

1. 必要に応じて標準設定を更新します。

   - **[!UICONTROL Button Text]** - ボタンに表示するテキストを入力します（ステージから直接更新することもできます）。

   - **[!UICONTROL Button Type]** - ボタンの形式を決定します。

     | タイプ | 説明 |
     | ------ | ----------- |
     | `Primary` | 現在のスタイル シートからプライマリ ボタン スタイルを適用します。 |
     | `Secondary` | 現在のスタイル シートからセカンダリ ボタン スタイルを適用します（該当する場合）。 |
     | `Link` | ボタンではなくハイパーリンクを作成します。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Button Link]** - ボタンがクリックされたときに提供される宛先ページを決定します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `URL` | 宛先ページの識別に相対 URL または完全修飾 URL を使用します。 |
     | `Product` | 製品名または SKU に基づいて宛先ページを識別します。 製品名は、部分的または完全な名前に基づいて検索できます。 検索結果のリストから製品が選択されます。 |
     | `Category` | 宛先ページをカテゴリツリー内の特定のカテゴリまたはサブカテゴリとして識別します。 |
     | `Page` | 宛先ページを特定の CMS ページとして識別します。 |

     {style="table-layout:auto"}

1. 必要に応じて [ 詳細設定 ][advanced-settings] を完了します。

1. 設定を保存して [!DNL Page Builder] ワークスペースに戻るには、右上隅の「**[!UICONTROL Save]**」をクリックします。

## ボタンコンテナの設定の変更

1. ボタンコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

1. 必要に応じて、**[!UICONTROL Appearance]** 設定を更新します。

   - 配置オプションを使用して、コンテナ内のボタンを水平または垂直に表示します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Inline` | ボタンを水平方向に配置します。 |
     | `Stacked` | ボタンを垂直方向に配置します。 |

     {style="table-layout:auto"}

   - 必要に応じて「**[!UICONTROL All buttons are same size]**」オプションを設定します。

     `Yes` に設定すると、コンテナ内のすべてのボタンは、最長のボタンテキストの長さに基づいて一定のサイズになります。

1. 必要に応じて [ 詳細設定 ][advanced-settings] を入力します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

## 詳細設定の変更

個々のボタンおよびボタンコンテナの _[!UICONTROL Advanced]_&#x200B;設定を変更できます。

1. 親コンテナ内の位置を制御するには、**[!UICONTROL Alignment]** のオプションを選択します。

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
   | `Left` | 指定したパディングに対する許容値を使用して、親コンテナの左境界線に沿ってコンテンツを配置します。 |
   | `Center` | 親コンテナの中央にコンテンツを配置します。指定したパディングに対する許容値を使用します。 |
   | `Right` | 親コンテナの右端に沿ってコンテンツを配置します。指定したパディングは許容されます。 |

   {style="table-layout:auto"}

1. ボタンコンテナまたはボタンコンテナの 4 つの辺すべてに適用する **[!UICONTROL Border]** スタイルを設定します。

   | オプション | 説明 |
   | ------ | ----------- |
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

1. `None` 以外の境界線のスタイルを設定する場合は、境界線の表示オプションを完了します。

   | オプション | 説明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
   | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
   | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

   {style="table-layout:auto"}

1. （オプション）ボタンまたはボタンコンテナに適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

   複数のクラス名はスペースで区切ります。

1. ボタンまたはボタンコンテナの外側の余白と内側のパディングを決定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

   対応する値を図に入力します。

   | コンテナ領域 | 説明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション：`Top`/`Right`/`Bottom`/`Left` |
   | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション：`Top`/`Right`/`Bottom`/`Left` |

   {style="table-layout:auto"}

[advanced-settings]: #change-advanced-settings
[button-container]: #change-settings-for-a-button-container
