---
title: 要素 —HTMLコード
description: HTML、CSS、JavaScript コードのスニペットを [!DNL Page Builder] ステージ。
exl-id: b6e2dff5-ceac-4c7e-a87f-f95a542ada28
feature: Page Builder, Page Content
source-git-commit: 556394327a6eff9282acb09bdd16777dd3fee360
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 0%

---

# 要素 —HTMLコード

以下を使用します。 _HTMLコード_ HTML、CSS および JavaScript コードのスニペットを [[!DNL Page Builder] ステージ](workspace.md#stage). 例えば、カスタムHTMLを追加し、ページ上の要素に適用できる CSS クラスを宣言するとします。 または、サードパーティのプロバイダーから受け取ったロゴ、ボタン、バナーのコードのスニペットを追加することもできます。

## HTMLコードツールボックス

![HTMLコードツールボックス](./assets/pb-elements-html-code-toolbox.png){width="500" zoomable="yes"}

| ツール | アイコン | 説明 |
| --------- | ---------- | ----------------- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | HTMLコードコンテナをページ上の別の有効な場所に移動します。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | コンテナのプロパティを変更できるHTMLコードを編集ページを開きます。 |
| 非表示 | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 「HTMLコード」コンテナを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のHTMLコードコンテナを表示します。 |
| 複製 | ![複製アイコン](./assets/pb-icon-duplicate.png){width="25"} | 「HTMLコード」コンテナのコピーを作成します。 |
| 削除 | ![削除アイコン](./assets/pb-icon-remove.png){width="25"} | ステージからHTMLコードコンテナとその内容を削除します。 |

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## HTMLコードを追加

次の例は、 [Google Font][1] 現在のスタイルシートを上書きするカスタム見出しクラスをコード化して宣言します。

### 手順 1:Googleフォントの選択

1. 次にアクセス： [Google Fonts][1] サイトを開き、使用するフォントファミリを選択します。

1. 埋め込むコードを `<head>` 」セクションに貼り付け、一時的にテキストエディターに貼り付けます。

   - 埋め込みフォントコード
   - CSS ルール

1. 各見出しクラスにフォントファミリ規則を追加し、見出しクラスを `<style>` タグを使用します。

   このコードは、 [!DNL Page Builder].

   ```html
   <style>
      h1 {color: teal; font-family: 'Khand', sans-serif; }
      h2 {color: teal; font-family: 'Khand', sans-serif; }
      h3 {color: teal; font-family: 'Khand', sans-serif; }
   </style>
   ```

### 手順 2：ページにコードを追加する

1. Adobe Analytics の _管理者_ ストアのサイドバー、に移動します。 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. フォントを使用できるページを見つけ、編集モードで開きます。

1. 下にスクロールして、 **[!UICONTROL Content]** 」セクションに入力します。

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をクリックし、 **[!UICONTROL HTML Code]** プレースホルダーをステージ上の行、列またはタブセットに追加します。

   赤いガイドラインを使用して、行、列またはタブセット内の別のコンテンツコンテナの前または後にディバイダを配置します。

   ![「HTMLコード」プレースホルダーのステージへのドラッグ](./assets/pb-elements-html-code-drag.png){width="600" zoomable="yes"}

1. HTMLコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} )、アイコン。

1. テキストボックスに、用意した埋め込みGoogle Fonts コードとスタイル宣言を貼り付けます。

   読みやすくするために、スペースを少し入力してコードをインデントできます。

   ![HTMLのコードとスタイル](./assets/pb-elements-html-code-example.png){width="500" zoomable="yes"}

1. 必要に応じて、残りの設定を更新します ( [HTMLコード設定の変更](#html-settings) を参照 )。

1. 右上隅で、 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。

   ページがブラウザー経由で表示されると、新しいフォントがレンダリングされます。

### 手順 3：ページをプレビューする

1. Adobe Analytics の _[!UICONTROL Currently Active]_セクション、設定&#x200B;**[!UICONTROL Enable Page]**から `Yes`.

   ![ページの有効化](./assets/pb-elements-html-code-enable-page.png){width="600" zoomable="yes"}

1. 右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

1. グリッド内のページを探し、「 」を選択します。 **[!UICONTROL View]** （内） _[!UICONTROL Actions]_列。

   ![新しいフォントファミリでページ見出しをプレビューする](./assets/pb-elements-html-code-preview.png){width="700" zoomable="yes"}

## HTMLコード設定の変更 {#html-settings}

1. HTMLコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

1. テキストボックスで、必要に応じてコードを編集します。

   HTML、CSS、JavaScript コードがサポートされています。 に属するコードスニペット `<head>` セクションをここに入力できます。

   エディターには、コードに特殊な要素を挿入するためのボタンも用意されています。

   | ボタン | 説明 |
   | ------ | ----------- |
   | ウィジェットの挿入… | をクリックして、「ウィジェット」テキストボックス内のカーソル位置にHTMLを挿入します。 |
   | 画像の挿入… | クリックすると、アップロードされた画像または画像がギャラリーから、「HTML」テキストボックス内のカーソルの位置に挿入されます。 |
   | 変数の挿入… | をクリックして、「HTML」テキストボックス内のカーソル位置に変数を挿入します。 |

1. を更新します。 _[!UICONTROL Advanced]_必要に応じて設定します。

   - 親コンテナ内でのコードの位置を制御するには、 **[!UICONTROL Alignment]**:

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイルシートで指定された位置揃えの既定の設定を適用します。 |
     | `Left` | リストを親コンテナの左側の境界線に沿って揃えます。指定されたパディングの値を使用します。 |
     | `Center` | 指定されたパディングを許容して、親コンテナの中央にリストを揃えます。 |
     | `Right` | 指定されたパディングの値を使用して、親コンテナの右側の境界線に沿ってブロックを揃えます。 |

     次の例では、レンダリングされたコードブロックの中央の位置揃えを使用するようにオプションが設定されています。

     ![中央揃えのディバイダ](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - を設定します。 **[!UICONTROL Border]** スタイルがコードコンテナの 4 つの側面すべてに適用されるようになりました。

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

   - 次の条件を満たさない境界線のスタイルを設定した場合： `None`、境界線の表示オプションを設定します。

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | スウォッチを選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各隅を囲むために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション） **[!UICONTROL CSS classes]** 現在のスタイルシートからコンテナに適用します。

     複数のクラス名はスペースで区切ります。

   - 次の値をピクセル単位で入力します。 **[!UICONTROL Margins and Padding]** を使用して、コードコンテナの外側の余白と内側の余白を指定します。

     ダイアグラムに対応する値を入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白の量。 オプション： `Top` / `Right` / `Bottom` / `Left` |

[1]: https://fonts.google.com/
