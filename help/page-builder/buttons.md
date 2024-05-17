---
title: 要素 – ボタン
description: で個々のボタンまたは一連のボタンを追加するために使用される、ボタンコンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: 9f1681c5-04b0-4259-aaf6-5d8081bd8cdb
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1586'
ht-degree: 0%

---

# 要素 – ボタン

の使用 _ボタン_ 個々のボタンまたは一連のボタンを [[!DNL Page Builder] ステージ](workspace.md#stage). ボタンは水平方向または垂直方向に配置でき、ステージの行、列、タブ、バナーに直接追加できます。

![店先にボタンが付いたバナー](./assets/pb-storefont-banner-with-button.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## ツールボックス

ボタン コンテンツ タイプを使用する場合は、個々のボタンと、1 つ以上のボタンを保持するボタン コンテナを追加および編集します。 それぞれに独自のツールボックスがあり、ボタンのデザインに使用します [!DNL Page Builder] ステージ。

### 個々のボタンのツールボックス

![ボタンツールボックス](./assets/pb-elements-button-settings.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | -------- | -------------- |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 「編集ボタン」ページが開きます。このページで、ボタンのプロパティを変更できます。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | ボタンをコピーします。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | ステージからボタンを削除します。 |

{style="table-layout:auto"}

### ボタンコンテナツールボックス

![ボタンコンテナツールボックス](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ----------------- | ----------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | ボタンコンテナをページ上の別の有効な場所に移動します。 |
| 追加 | ![アイコンを追加](./assets/pb-icon-add-button.png){width="25"} | コンテナにボタンを追加します。 |
| （ラベル） | ボタン | 現在のコンテナをボタン要素として識別します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 編集ボタン ページを開きます。このページで、コンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | ボタンコンテナを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のボタンコンテナを表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | ボタンコンテナをコピーします。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | ボタンコンテナとそのコンテンツをステージから削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 個々のボタンの追加

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をドラッグします。 **[!UICONTROL Buttons]** ステージ上の行、列またはタブセットへのプレースホルダー。

   ![ボタンのステージへのドラッグ](./assets/pb-elements-button-drag.png){width="500" zoomable="yes"}

1. ボタンにカーソルを合わせてツールボックスを表示し、 _設定_ （![設定アイコン](./assets/pb-icon-settings.png)） アイコンをクリックします。

1. を入力 **[!UICONTROL Button Text]** をボタンに表示します。

   ![ボタンの基本設定](./assets/pb-elements-button-settings-button-text.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Button Type]** を次のいずれかに変更します。

   | タイプ | 説明 |
   | ------ | ----------- |
   | `Primary` | 現在のスタイル シートからプライマリ ボタン スタイルを適用します。 |
   | `Secondary` | 現在のスタイル シートからセカンダリ ボタン スタイルを適用します（該当する場合）。 |
   | `Link` | ボタンではなくハイパーリンクを作成します。 |

   {style="table-layout:auto"}

   ![プライマリとセカンダリボタンの例](./assets/pb-elements-button-settings-button-primary-secondary.png){width="500" zoomable="yes"}

1. を **[!UICONTROL Button Link]** 次のいずれかのタイプを使用します。

   - **[!UICONTROL URL]** - リンクの宛先 URL を入力します。

     URL は、ストア内の製品またはページへの相対リンク、または完全修飾 URL にすることができます。

     相対 URL の例 –  `../luma-analog-watch.html`

     完全修飾 URL の例 –  `http://mystore.com/luma-analog-watch.html`

     リンクが別の web サイトに移動する場合は、新しいブラウザータブでリンクを開くことで、現在のページをストアで開いたままにすることができます。

     訪問者がストアから移動しないようにするには、 **[!UICONTROL Open in new tab]** チェックボックス。

   - **[!UICONTROL Product]**  – 製品名（一部または全部）または SKU を入力し、リストで製品名を選択します。

     >[!NOTE]
     >
     >製品は、次に従ってリストに表示されます _在庫切れ商品の表示_ 設定。 を使用したマルチソースマーチャントの場合 [Inventory management](../inventory-management/introduction.md)ただし、製品のリストは、デフォルトの web サイトにのみ割り当てられたソースによって制限されます。

     ![ボタンリンクの製品の選択](./assets/pb-elements-button-settings-button-link-product-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - カテゴリ名（一部または全部）を入力するか、空白フィールドをクリックしてカテゴリツリーを表示します。 次に、ツリーでカテゴリ名を選択します。

     ![ボタンリンクのカテゴリの選択](./assets/pb-elements-button-settings-button-link-category-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - CMS ページの名前（一部または全部）を入力するか、空白フィールドをクリックして完全なリストを表示します。 次に、検索結果リストでページの名前を選択します。

     ![ボタンリンク用の CMS ページを選択](./assets/pb-elements-button-settings-button-link-page-search.png){width="600" zoomable="yes"}

1. を完了する [詳細設定][advanced-settings] 必要に応じて。

1. 完了したら、 **[!UICONTROL Save]** 右上隅で設定を適用し、に戻ります [!DNL Page Builder] ワークスペース。

## 一連のボタンの追加

次のセクションでは、個々のボタンから開始して、ボタンコンテナ内に 3 つのボタンのセットを作成する一連の手順について説明します。 個々のボタンがまだない場合は、前の手順に従って、個々のボタンをステージに追加します。

### 手順 1:2 番目のボタンの作成

1. ボタンコンテナにカーソルを合わせてツールボックスを表示し、 _追加_ （ ![アイコンを追加](./assets/pb-icon-add-button.png){width="20"} ） アイコンをクリックします。

   ![別のボタンの追加](./assets/pb-elements-buttons-toolbox-add.png){width="500" zoomable="yes"}

1. 2 番目のボタンに表示するテキストを入力します。

1. 新規ボタンをクリックしてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![ボタンの編集](./assets/pb-elements-button-set-edit-button2-toolbox.png){width="500" zoomable="yes"}

1. を設定 **[!UICONTROL Button Type]** 対象： `Secondary`.

1. の設定 **[!UICONTROL Button Link]** 必要に応じて。

   次の例では、リンクは、に移動する相対 URL です。 [お問い合わせ](../getting-started/store-details.md#contact-us-form) ページ。

   ![Contact Us ボタンの設定](./assets/pb-elements-button-set-edit-button2-toolbox-settings.png){width="600" zoomable="yes"}

1. を完了する [詳細設定][advanced-settings] 必要に応じて。

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

### 手順 2:3 番目のボタンの作成

1. ステージで 2 番目のボタンをもう一度クリックし、 _複製_ （ ![アイコンを複製](./assets/pb-icon-duplicate.png){width="20"} ） アイコンをクリックします。

   ![ボタンの複製](./assets/pb-elements-button-set-contact-us-toolbox-duplicate.png){width="500" zoomable="yes"}

1. 3 番目のボタンに表示するテキストを入力します。

1. 3 番目のボタンをクリックしてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![3 番目のボタンのツールボックス](./assets/pb-elements-button-set-find-us-toolbox-settings.png){width="500" zoomable="yes"}

1. を更新 **[!UICONTROL Button Link]** 必要に応じて。

1. 右上隅のをクリックします。 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

### 手順 3：ボタンコンテナの更新

1. ボタンコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![ボタンコンテナツールボックス](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

1. 次の下 _[!UICONTROL Appearance]_、を選択&#x200B;**[!UICONTROL Stacked]**.

1. を設定 **[!UICONTROL All Buttons are same size]** 対象： `Yes`.

   ![同じサイズの積み重ねボタン](./assets/pb-elements-buttons-settings-appearance-stacked.png){width="300"}

1. 必要に応じて、の説明を使用して残りの設定を更新します。 [ボタンコンテナの設定の変更][button-container].

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

   完全な積み重ねボタンセットがステージに表示され、1 つのプライマリボタンと 2 つのセカンダリボタンが表示されます。

   ![ステージ上の積み重ねボタン](./assets/pb-elements-buttons-stacked.png){width="500" zoomable="yes"}

## ボタンの移動

1. 移動するボタンをクリックします。

1. 「移動」を選択してドラッグします（ ![移動アイコン](./assets/pb-icon-move.png){width="20"} ）アイコンをクリックすると、ボタンコンテナ内のボタンの新しい位置まで移動します。このアイコンは、ボタンテキストの直前に表示されます。

   ![ボタンの移動](./assets/pb-elements-button-set-move-button.png){width="500" zoomable="yes"}

## ボタンの設定の変更

1. ステージ上のボタンをクリックしてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![ボタンツールボックス](./assets/pb-elements-button-toolboxes.png){width="500" zoomable="yes"}

1. 必要に応じて標準設定を更新します。

   - **[!UICONTROL Button Text]** - ボタンに表示するテキストを入力します（ステージから直接更新することもできます）。

   - **[!UICONTROL Button Type]** - ボタンの形式を決定します。

     | タイプ | 説明 |
     | ------ | ----------- |
     | `Primary` | 現在のスタイル シートからプライマリ ボタン スタイルを適用します。 |
     | `Secondary` | 現在のスタイル シートからセカンダリ ボタン スタイルを適用します（該当する場合）。 |
     | `Link` | ボタンではなくハイパーリンクを作成します。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Button Link]** - ボタンがクリックされた際に提供される宛先ページを決定します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `URL` | 宛先ページの識別に相対 URL または完全修飾 URL を使用します。 |
     | `Product` | 製品名または SKU に基づいて宛先ページを識別します。 製品名は、部分的または完全な名前に基づいて検索できます。 検索結果のリストから製品が選択されます。 |
     | `Category` | 宛先ページをカテゴリツリー内の特定のカテゴリまたはサブカテゴリとして識別します。 |
     | `Page` | 宛先ページを特定の CMS ページとして識別します。 |

     {style="table-layout:auto"}

1. を完了する [詳細設定][advanced-settings] 必要に応じて。

1. 設定を保存し、に戻るには [!DNL Page Builder] ワークスペース、クリック **[!UICONTROL Save]** 右上隅

## ボタンコンテナの設定の変更

1. ボタンコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

1. を更新 **[!UICONTROL Appearance]** 必要に応じて設定します。

   - 配置オプションを使用して、コンテナ内のボタンを水平または垂直に表示します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Inline` | ボタンを水平方向に配置します。 |
     | `Stacked` | ボタンを垂直方向に配置します。 |

     {style="table-layout:auto"}

   - を **[!UICONTROL All buttons are same size]** 好みに応じてオプションを選択します。

     に設定されている場合 `Yes`では、コンテナ内のすべてのボタンは、最長のボタンテキストの長さに基づいて、一定のサイズになります。

1. を完了する [詳細設定][advanced-settings] 必要に応じて。

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

## 詳細設定の変更

を変更できます _[!UICONTROL Advanced]_個々のボタンの設定とボタンコンテナの設定。

1. 親コンテナ内の位置を制御するには、 **[!UICONTROL Alignment]**:

   | オプション | 説明 |
   | ------ | ----------- |
   | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
   | `Left` | 指定したパディングに対する許容値を使用して、親コンテナの左境界線に沿ってコンテンツを配置します。 |
   | `Center` | 親コンテナの中央にコンテンツを配置します。指定したパディングに対する許容値を使用します。 |
   | `Right` | 親コンテナの右端に沿ってコンテンツを配置します。指定したパディングは許容されます。 |

   {style="table-layout:auto"}

1. を **[!UICONTROL Border]** ボタンまたはボタンコンテナの 4 つの辺すべてに適用されるスタイル：

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

1. 境界線のスタイルを `None`の場合は、次のボーダー表示オプションを入力します。

   | オプション | 説明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
   | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
   | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

   {style="table-layout:auto"}

1. （オプション）の名前を指定します **[!UICONTROL CSS classes]** 現在のスタイルシートから、ボタンまたはボタンコンテナに適用します。

   複数のクラス名はスペースで区切ります。

1. 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** ボタンまたはボタンコンテナの外側の余白と内側のパディングを決定します。

   対応する値を図に入力します。

   | コンテナ領域 | 説明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

[advanced-settings]: #change-advanced-settings
[button-container]: #change-settings-for-a-button-container
