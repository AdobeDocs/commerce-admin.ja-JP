---
title: 要素 – HTMLコード
description: でHTML、CSS、JavaScript コードのスニペットを追加するために使用される、HTMLコードのコンテンツタイプについて説明します [!DNL Page Builder] ステージ。
exl-id: b6e2dff5-ceac-4c7e-a87f-f95a542ada28
feature: Page Builder, Page Content
source-git-commit: 556394327a6eff9282acb09bdd16777dd3fee360
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# 要素 – HTMLコード

の使用 _HTMLコード_ HTML、CSS、JavaScript コードのスニペットをに追加するコンテンツタイプ [[!DNL Page Builder] ステージ](workspace.md#stage). 例えば、ページ上の要素に適用できるカスタムHTMLを追加し、CSS クラスを宣言することができます。 また、サードパーティのプロバイダーから受け取ったロゴ、ボタン、バナーのコードのスニペットを追加する場合もあります。

## HTMLコード ツールボックス

![HTMLコード ツールボックス](./assets/pb-elements-html-code-toolbox.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ---------- | ----------------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | HTMLコードコンテナをページ上の別の有効な場所に移動します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | 「HTMLコードを編集」ページが開きます。このページで、コンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | HTMLコードコンテナを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のHTMLコードコンテナを表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | HTMLコードコンテナをコピーします。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | HTMLコードコンテナとそのコンテンツをステージから削除します。 |

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## HTMLコードを追加

次の例は、埋め込み方法を示しています [Google フォント][1] 現在のスタイルシートを上書きするカスタム見出しクラスをコーディングし、宣言します。

### 手順 1:Google フォントを選択する

1. にアクセスします [Google フォント][1] サイトを選択し、使用するフォントファミリーを選択します。

1. に埋め込む生成されたコードをコピーします。 `<head>` ページの「」セクションを選択し、一時的にテキストエディターに貼り付けます。

   - 埋め込みフォントコード
   - CSS ルール

1. 各見出しクラスにフォントファミリルールを追加し、見出しクラスを `<style>` タグ。

   このコードはに貼り付けられます [!DNL Page Builder].

   ```html
   <style>
      h1 {color: teal; font-family: 'Khand', sans-serif; }
      h2 {color: teal; font-family: 'Khand', sans-serif; }
      h3 {color: teal; font-family: 'Khand', sans-serif; }
   </style>
   ```

### 手順 2：ページへのコードの追加

1. が含まれる _Admin_ ストアのサイドバー、に移動します **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. フォントを使用できるページを探し、編集モードで開きます。

1. 下にスクロールして、 **[!UICONTROL Content]** セクション。

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をドラッグして **[!UICONTROL HTML Code]** ステージ上の行、列またはタブセットへのプレースホルダー。

   赤いガイドラインを使用して、行、列、タブセット内の別のコンテンツコンテナの前または後にディバイダーを配置します。

   ![HTMLコードプレースホルダーのステージへのドラッグ](./assets/pb-elements-html-code-drag.png){width="600" zoomable="yes"}

1. HTMLコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ）、アイコンです。

1. テキストボックスに、準備した埋め込みGoogle フォントコードおよびスタイル宣言を貼り付けます。

   読みやすくするために、スペースを 2、3 個入力してコードをインデントできます。

   ![HTMLコードとスタイル](./assets/pb-elements-html-code-example.png){width="500" zoomable="yes"}

1. 必要に応じて、残りの設定を更新します（を参照）。 [HTMLコード設定の変更](#html-settings) （詳細はこちら）。

1. 右上隅のをクリックします。 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

   新しいフォントは、ブラウザーを使用してページを表示するとレンダリングされます。

### 手順 3：ページのプレビュー

1. が含まれる _[!UICONTROL Currently Active]_セクション、設定&#x200B;**[!UICONTROL Enable Page]**対象： `Yes`.

   ![ページの有効化](./assets/pb-elements-html-code-enable-page.png){width="600" zoomable="yes"}

1. 右上隅のをクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

1. グリッドでページを見つけて、を選択します。 **[!UICONTROL View]** が含まれる _[!UICONTROL Actions]_列。

   ![新しいフォントファミリーでページ見出しをプレビュー](./assets/pb-elements-html-code-preview.png){width="700" zoomable="yes"}

## HTMLコード設定の変更 {#html-settings}

1. HTMLコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

1. テキストボックスで、必要に応じてコードを編集します。

   HTML、CSS、JavaScript コードがサポートされています。 に属するコードスニペット `<head>` ページのセクションは、ここに入力できます。

   エディターには、コードに特殊な要素を挿入するボタンもあります。

   | ボタン | 説明 |
   | ------ | ----------- |
   | ウィジェットを挿入… | クリックすると、HTMLテキストボックス内のカーソル位置にウィジェットが挿入されます。 |
   | イメージの挿入… | アップロードした画像または Gallery の画像をHTML テキスト ボックスのカーソル位置に挿入するときにクリックします。 |
   | 変数の挿入… | クリックすると、HTMLテキストボックス内のカーソル位置に変数が挿入されます。 |

1. を更新 _[!UICONTROL Advanced]_必要に応じて設定します。

   - 親コンテナ内のコードの位置を制御するには、 **[!UICONTROL Alignment]**:

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | 親コンテナの左罫線に沿ってリストを配置します。指定したパディングはすべて許可されます。 |
     | `Center` | 親コンテナの中央にリストを揃えます。指定したパディングに対する許容値を使用します。 |
     | `Right` | 親コンテナの右端に沿ってブロックを配置します。指定したパディングは許可されます。 |

     次の例では、オプションを設定して、レンダリングされたコードブロックに中央揃えを使用します。

     ![中央揃えのディバイダー](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - を **[!UICONTROL Border]** コードコンテナの 4 つの辺すべてに適用されるスタイル：

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

   - 境界線のスタイルを `None`の場合は、次のボーダー表示オプションを入力します。

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション）の名前を指定します **[!UICONTROL CSS classes]** を現在のスタイルシートから取得して、コンテナに適用します。

     複数のクラス名はスペースで区切ります。

   - 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** コードコンテナの外側の余白と内側のパディングを決定します。

     対応する値を図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション： `Top` / `Right` / `Bottom` / `Left` |

[1]: https://fonts.google.com/
