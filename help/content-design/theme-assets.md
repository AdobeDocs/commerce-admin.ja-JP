---
title: テーマアセット
description: CSS、フォント、画像、JavaScript ファイルなどのテーマアセットの管理方法について説明します。
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/8dH6Wuc49gsiL1rIFW-CqJmuqYNqawwearfbgq73Mug
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---

# テーマアセット

_静的ファイル_&#x200B;は、テーマで使用されるCSS、フォント、画像、JavaScriptなどのアセットのコレクションです。 静的ファイルの場所は、[ ベース URL](../stores-purchase/store-urls.md)設定で指定します。 各静的ファイルのURLにデジタル署名を追加して、ブラウザーが新しいバージョンを使用できるタイミングを検出できるようにすることができます。 署名がブラウザーキャッシュに保存されているものと異なる場合は、新しいバージョンのファイルが使用されます。

標準インストールの場合、テーマに関連付けられたアセットは、[!DNL Commerce] ルートの下の次の場所にある`web` フォルダーに整理されます。

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## 静的ファイル URLへのデジタル署名の追加

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL Developer]**&#x200B;を選択します。

1. **[!UICONTROL Static Files Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![静的ファイル設定](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. **[!UICONTROL Sign Static Files]**&#x200B;を`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

| ファイルタイプ | 説明 |
|--- |--- |
| CSS | スキンに関連付けられているビジュアルスタイルを制御します。 サーバー上の場所の例：`[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| フォント | テーマで使用できるフォントを指定します。 サーバー上の場所：`[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| 画像 | ボタンや背景のテクスチャなど、テーマで使用されるグラフィカルアセットを指定します。 サーバー上の場所の例：`[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | テーマ固有のJavaScript ルーチンと呼び出し可能な関数。 サーバー上の場所の例：`[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## CSS ファイルを結合

サイトを最適化し、ページ読み込み時間を短縮する取り組みの一環として、個別のCSS ファイルを単一の凝縮ファイルに結合することで、その数を減らすことができます。 結合されたCSS ファイルを開くと、改行が削除されたテキストの連続したストリームが1つ表示されます。 結合されたファイルは編集できないので、開発モードから抜け出し、CSSを頻繁に変更しなくなるまで待つことをお勧めします。

>[!NOTE]
>
>CSS ファイルは、[開発者モード ](../systems/developer-tools.md#operation-modes)で作業している場合にのみ、_管理者_ パネルから結合できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を選択し、**[!UICONTROL Developer]**&#x200B;を選択します。

1. **[!UICONTROL CSS Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![CSS設定](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   これらの設定オプションについて詳しくは、_設定リファレンス_&#x200B;の[CSS設定](../configuration-reference/advanced/developer.md#css-settings)を参照してください。

1. **[!UICONTROL Merge CSS Files]**&#x200B;を`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## JavaScript ファイルの結合

複数のJavaScriptファイルを、ひとつのファイルに統合することで、ページの読み込み時間を短縮できます。 結合されたJavaScript ファイルを開くと、改行が削除された1つの連続したテキストストリームが表示されます。 開発プロセスが終了し、コードにエラーが含まれていない場合は、ファイルをマージすることを検討してください。

>[!NOTE]
>
>JavaScript ファイルは、[ デベロッパーモード ](../systems/developer-tools.md#operation-modes)で作業している場合にのみ、_管理者_ パネルから結合できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を選択し、**[!UICONTROL Developer]**&#x200B;を選択します。

1. **[!UICONTROL JavaScript Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![JavaScript設定](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   これらの設定オプションについて詳しくは、_設定リファレンス_&#x200B;の[JavaScript Settings](../configuration-reference/advanced/developer.md#javascript-settings)を参照してください。

1. **[!UICONTROL Merge JavaScript Files]**&#x200B;を`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
