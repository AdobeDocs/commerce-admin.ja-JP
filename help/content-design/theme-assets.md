---
title: テーマアセット
description: CSS、フォント、画像、JavaScript ファイルなど、テーマアセットの管理方法について説明します。
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# テーマアセット

この _静的ファイル_ は、テーマで使用される CSS、フォント、画像、JavaScript などのアセットのコレクションです。 静的ファイルの場所は、で指定します。 [ベース URL](../stores-purchase/store-urls.md) 設定。 各静的ファイルの URL にデジタル署名を追加して、ブラウザーが新しいバージョンが使用可能かどうかを検出できるようにします。 署名がブラウザーキャッシュに保存されている署名と異なる場合は、ファイルの新しいバージョンが使用されます。

標準インストールの場合、テーマに関連付けられたアセットは以下のように整理されます。 `web` の下の次の場所にあるフォルダー [!DNL Commerce] ルート。

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## 静的ファイル URL へのデジタル署名の追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Static Files Settings]** セクション。

   ![静的ファイルの設定](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. を設定 **[!UICONTROL Sign Static Files]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

| ファイルタイプ | 説明 |
|--- |--- |
| CSS | スキンに関連付けられている視覚的なスタイル設定をコントロールします。 サーバー上の場所の例： `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| フォント | テーマで使用できるフォントを指定します。 サーバー上の場所： `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| 画像 | ボタン、背景テクスチャなど、テーマで使用されるグラフィカルアセットを提供します。 サーバー上の場所の例： `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | テーマ固有の JavaScript ルーチンと呼び出し可能な関数。 サーバー上の場所の例： `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## CSS ファイルの結合

サイトを最適化しページの読み込み時間を短縮する取り組みの一環として、別々の CSS ファイルを 1 つの圧縮ファイルに結合することで、それらのファイルの数を減らすことができます。 結合された CSS ファイルを開くと、1 つの連続したテキストストリームが表示され、改行が削除されます。 結合ファイルは編集できないので、開発モードが終了し、CSS に頻繁に変更を加えなくなるまで待つことをお勧めします。

>[!NOTE]
>
>CSS ファイルは、 _Admin_ で作業しているときにのみパネルに表示される [開発者モード](../systems/developer-tools.md#operation-modes).

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左のパネルで、 **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL CSS Settings]** セクション。

   ![CSS 設定](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   これらの構成オプションの詳細については、を参照してください [CSS 設定](../configuration-reference/advanced/developer.md#css-settings) が含まれる _設定リファレンス_.

1. を設定 **[!UICONTROL Merge CSS Files]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

## JavaScript ファイルの結合

複数の JavaScript ファイルを 1 つの圧縮ファイルに結合して、ページの読み込み時間を短縮できます。 結合された JavaScript ファイルを開くと、1 つの連続したテキストストリームが表示され、改行が削除されます。 開発プロセスが完了し、コードにエラーが含まれていない場合は、ファイルの結合を検討してください。

>[!NOTE]
>
>JavaScript ファイルは、 _Admin_ で作業しているときにのみパネルに表示される [開発者モード](../systems/developer-tools.md#operation-modes).

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左のパネルで、 **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL JavaScript Settings]** セクション。

   ![JavaScript 設定](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   これらの構成オプションの詳細については、を参照してください [JavaScript 設定](../configuration-reference/advanced/developer.md#javascript-settings) が含まれる _設定リファレンス_.

1. を設定 **[!UICONTROL Merge JavaScript Files]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.
