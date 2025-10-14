---
title: 要素 – HTML コード
description: ステージ内でHTML、CSS、JavaScript コードのスニペットを追加するために使用される、HTML コード コンテンツタイプについて説明  [!DNL Page Builder]  ます。
exl-id: b6e2dff5-ceac-4c7e-a87f-f95a542ada28
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# 要素 – HTML コード

_HTML コード_ コンテンツタイプを使用して、[[!DNL Page Builder]  ステージ &#x200B;](workspace.md#stage) にHTML、CSS、JavaScript コードのスニペットを追加します。 例えば、カスタム HTMLを追加し、ページ上の要素に適用できる CSS クラスを宣言する場合があります。 また、サードパーティのプロバイダーから受け取ったロゴ、ボタン、バナーのコードのスニペットを追加する場合もあります。

## HTML コードツールボックス

![HTML コード ツールボックス &#x200B;](./assets/pb-elements-html-code-toolbox.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ---------- | ----------------- |
| 移動 | ![&#x200B; 移動アイコン &#x200B;](./assets/pb-icon-move.png){width="25"} | HTML コードコンテナをページ上の別の有効な場所に移動します。 |
| 設定 | ![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="25"} | 「HTML コードを編集」ページが開きます。このページで、コンテナのプロパティを変更できます。 |
| Hide | ![&#x200B; アイコンを非表示 &#x200B;](./assets/pb-icon-hide.png){width="25"} | HTML コードコンテナを非表示にします。 |
| 表示 | ![&#x200B; アイコンを表示 &#x200B;](./assets/pb-icon-show.png){width="25"} | 非表示のHTML コードコンテナを表示します。 |
| 複製 | ![&#x200B; 複製アイコン &#x200B;](./assets/pb-icon-duplicate.png){width="25"} | HTML コードコンテナをコピーします。 |
| 削除 | ![&#x200B; 削除アイコン &#x200B;](./assets/pb-icon-remove.png){width="25"} | HTML コードコンテナとそのコンテンツをステージから削除します。 |

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## HTML コードを追加

次の例は、[Google Font][1] コードを埋め込み、現在のスタイルシートを上書きするカスタム見出しクラスを宣言する方法を示しています。

### 手順 1:Google フォントを選択する

1. [Google Fonts][1] サイトにアクセスし、使用するフォントファミリーを選択します。

1. ページの `<head>` セクションに埋め込む生成されたコードをコピーし、一時的にテキストエディターに貼り付けます。

   - 埋め込みフォントコード
   - CSS ルール

1. 見出しクラスを `<style>` タグで囲み、各見出しクラスにフォントファミリルールを追加します。

   このコードは [!DNL Page Builder] に貼り付けられます。

   ```html
   <style>
      h1 {color: teal; font-family: 'Khand', sans-serif; }
      h2 {color: teal; font-family: 'Khand', sans-serif; }
      h3 {color: teal; font-family: 'Khand', sans-serif; }
   </style>
   ```

### 手順 2：ページへのコードの追加

1. ストアの _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Pages]**&#x200B;に移動します。

1. フォントを使用できるページを探し、編集モードで開きます。

1. 下にスクロールして、「**[!UICONTROL Content]**」セクションを展開します。

1. [!DNL Page Builder] パネルで **[!UICONTROL Elements]** を展開し、**[!UICONTROL HTML Code]** プレースホルダーをステージ上の行、列、タブセットにドラッグします。

   赤いガイドラインを使用して、行、列、タブセット内の別のコンテンツコンテナの前または後にディバイダーを配置します。

   ![HTML コードのプレースホルダーのステージへのドラッグ &#x200B;](./assets/pb-elements-html-code-drag.png){width="600" zoomable="yes"}

1. HTML コンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）, アイコンを選びます。

1. テキストボックスに、準備した埋め込みGoogle フォントコードおよびスタイル宣言を貼り付けます。

   読みやすくするために、スペースを 2、3 個入力してコードをインデントできます。

   ![HTMLのコードとスタイル &#x200B;](./assets/pb-elements-html-code-example.png){width="500" zoomable="yes"}

1. 必要に応じて残りの設定を更新します（詳しくは [HTML コード設定の変更 &#x200B;](#html-settings) を参照）。

1. 右上隅にある「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

   新しいフォントは、ブラウザーを使用してページを表示するとレンダリングされます。

### 手順 3：ページのプレビュー

1. _[!UICONTROL Currently Active]_&#x200B;セクションで、**[!UICONTROL Enable Page]**&#x200B;を `Yes` に設定します。

   ![&#x200B; ページの有効化 &#x200B;](./assets/pb-elements-html-code-enable-page.png){width="600" zoomable="yes"}

1. 右上隅の **[!UICONTROL Save]** 矢印をクリックし、「**[!UICONTROL Save & Close]**」を選択します。

1. グリッドでページを見つけ、**[!UICONTROL View]** 列で _[!UICONTROL Actions]_&#x200B;を選択します。

   ![&#x200B; 新しいフォントファミリーでページの見出しをプレビューする &#x200B;](./assets/pb-elements-html-code-preview.png){width="700" zoomable="yes"}

## HTML コードの設定の変更 {#html-settings}

1. HTML コンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

1. テキストボックスで、必要に応じてコードを編集します。

   HTML、CSS、JavaScript コードがサポートされています。 ページの `<head>` セクションに属するコードスニペットは、ここに入力できます。

   エディターには、コードに特殊な要素を挿入するボタンもあります。

   | ボタン | 説明 |
   | ------ | ----------- |
   | ウィジェットを挿入… | クリックすると、「HTML」テキストボックス内のカーソル位置にウィジェットが挿入されます。 |
   | イメージの挿入… | アップロードした画像または Gallery の画像をHTML テキストボックスのカーソル位置に挿入するときにクリックします。 |
   | 変数の挿入… | クリックすると、「HTML」テキストボックス内のカーソル位置に変数が挿入されます。 |

1. 必要に応じて、_[!UICONTROL Advanced]_&#x200B;設定を更新します。

   - 親コンテナ内のコードの位置を制御するには、**[!UICONTROL Alignment]** のいずれかを選択します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | 親コンテナの左罫線に沿ってリストを配置します。指定したパディングはすべて許可されます。 |
     | `Center` | 親コンテナの中央にリストを揃えます。指定したパディングに対する許容値を使用します。 |
     | `Right` | 親コンテナの右端に沿ってブロックを配置します。指定したパディングは許可されます。 |

     次の例では、オプションを設定して、レンダリングされたコードブロックに中央揃えを使用します。

     ![&#x200B; 中央揃えのデバイダー &#x200B;](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - コードコンテナの 4 つの辺すべてに適用する **[!UICONTROL Border]** スタイルを設定します。

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

   - `None` 以外の境界線のスタイルを設定する場合は、境界線の表示オプションを完了します。

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション）コンテナに適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

     複数のクラス名はスペースで区切ります。

   - コードコンテナの外側の余白と内側のパディングを決定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

     対応する値を図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 オプション：`Top`/`Right`/`Bottom`/`Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 オプション：`Top`/`Right`/`Bottom`/`Left` |

[1]: https://fonts.google.com/

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
