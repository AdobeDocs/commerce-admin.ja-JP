---
title: テーマアセット
description: CSS、フォント、画像、JavaScript ファイルなど、テーマアセットを管理する方法について説明します。
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# テーマアセット

The _静的ファイル_ は、テーマで使用される CSS、フォント、画像、JavaScript などのアセットのコレクションです。 静的ファイルの場所は、 [ベース URL](../stores-purchase/store-urls.md) 設定。 各静的ファイルの URL にデジタル署名を追加して、ブラウザーが新しいバージョンが利用可能かどうかを検出できるようにすることができます。 署名がブラウザーのキャッシュに保存されている署名と異なる場合は、新しいバージョンのファイルが使用されます。

標準インストールの場合、テーマに関連付けられたアセットは、 `web` 以下の場所にあるフォルダー ( [!DNL Commerce] ルートを使用します。

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## 静的ファイル URL への電子署名の追加

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Developer]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Static Files Settings]** 」セクションに入力します。

   ![静的ファイル設定](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. 設定 **[!UICONTROL Sign Static Files]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

| ファイルタイプ | 説明 |
|--- |--- |
| CSS | スキンに関連付けられた視覚的なスタイルを制御します。 サーバー上の場所の例： `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| フォント | テーマで使用できるフォントを指定します。 サーバー上の場所： `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| 画像 | ボタン、背景テクスチャなど、テーマで使用されるグラフィカルなアセットを提供します。 サーバー上の場所の例： `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | テーマ固有の JavaScript ルーチンと呼び出し可能な関数。 サーバー上の場所の例： `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## CSS ファイルを結合

サイトの最適化とページ読み込み時間の短縮の取り組みの一環として、CSS ファイルを単一の縮小されたファイルに結合することで、個別の CSS ファイルの数を減らすことができます。 結合された CSS ファイルを開くと、テキストの連続したストリームが 1 つ表示され、改行が削除されます。 結合されたファイルは編集できないので、開発モードが終了し、CSS を頻繁に変更しなくなるまで待つことをお勧めします。

>[!NOTE]
>
>CSS ファイルは _管理者_ パネルは、 [開発者モード](../systems/developer-tools.md#operation-modes).

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Developer]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL CSS Settings]** 」セクションに入力します。

   ![CSS 設定](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   これらの設定オプションについて詳しくは、 [CSS 設定](../configuration-reference/advanced/developer.md#css-settings) （内） _設定リファレンス_.

1. 設定 **[!UICONTROL Merge CSS Files]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## JavaScript ファイルの結合

複数の JavaScript ファイルを 1 つの縮小されたファイルに結合して、ページ読み込み時間を短縮できます。 結合された JavaScript ファイルを開くと、1 つの連続したテキストストリームが表示され、改行が削除されます。 開発プロセスが完了し、コードにエラーがない場合は、ファイルを結合することを検討してください。

>[!NOTE]
>
>JavaScript ファイルは _管理者_ パネルは、 [開発者モード](../systems/developer-tools.md#operation-modes).

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Developer]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL JavaScript Settings]** 」セクションに入力します。

   ![JavaScript 設定](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   これらの設定オプションについて詳しくは、 [JavaScript 設定](../configuration-reference/advanced/developer.md#javascript-settings) （内） _設定リファレンス_.

1. 設定 **[!UICONTROL Merge JavaScript Files]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.
