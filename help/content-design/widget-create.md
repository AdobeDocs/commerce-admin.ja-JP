---
title: ウィジェットの作成と管理
description: ストア全体のコンテンツを自動的に更新するウィジェットを作成および管理する方法について説明します。
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# ウィジェットの作成と管理

ウィジェットは再利用可能なコンポーネントです。 ウィジェットを簡単に作成し、既存のウィジェットを変更して、ストア全体のコンテンツを自動的に更新できます。 使用されなくなったウィジェットを削除することもできます。

![ウィジェット](./assets/widgets.png){width="700" zoomable="yes"}

## ウィジェットを作成

ウィジェットの作成手順は、それぞれのウィジェットでほぼ同じです [ウィジェットタイプ](widgets.md#widget-types). 手順の最初の部分に従ってから、必要な特定のタイプのウィジェットの最後の部分を完了できます。

### 手順 1：タイプの選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. クリック **[!UICONTROL Add Widget]**.

1. が含まれる _[!UICONTROL Settings]_セクション：

   - を設定 **[!UICONTROL Type]** 作成するウィジェットタイプに変更します。

   - を確認します **[!UICONTROL Design Theme]** 現在のテーマに設定されます。

     ![ウィジェット設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Continue]**.

### 手順 2：ストアフロントのプロパティとレイアウトを指定する

1. が含まれる _[!UICONTROL Storefront Properties]_セクション：

   - の場合 **[!UICONTROL Widget Title]**、ウィジェットのわかりやすいタイトルを入力します。

     このタイトルは、管理者からのみ表示されます。

   - の場合 **[!UICONTROL Assign to Store Views]**&#x200B;で、ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択することも、 `All Store Views`. 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]**&#x200B;を入力し、この項目がページの同じ部分に他のユーザーと表示される順序を決定します。 （`0` =最初、 `1` =秒、 `3` = 3 番目、など）。

     ![ストアフロントのプロパティ](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. が含まれる _[!UICONTROL Layout Updates]_セクションで、をクリック&#x200B;**[!UICONTROL Add Layout Update]**.

1. を設定 **[!UICONTROL Display On]** を選択します。を選択して、ページを表示するページのタイプに変更できます。

1. が含まれる **[!UICONTROL Container]** リストから、ページレイアウトを配置する領域を選択します。

   ![レイアウトの更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. ウィジェットがリンクの場合は、 **[!UICONTROL Template]** を次のいずれかに変更します。

   - `Block Template` - ページ上にスタンドアロンの単位として配置できるように、コンテンツをフォーマットします。
   - `Inline Template` - コンテンツを他のコンテンツ内に配置できるようにフォーマットします。 例えば、テキストの段落内に入るリンクなどです。

### 手順 3：ウィジェットオプションの完了

各ウィジェットタイプのオプションはわずかに異なりますが、プロセスは基本的に同じです。 次の例では、ページネーションコントロールを使用して、特定のカテゴリの製品リストを表示します。

1. 左パネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. クリック **[!UICONTROL Select Block]**.

1. を入力 **[!UICONTROL Title]** 次のようにリストの上に表示されます `Featured Products`.

1. ページネーションコントロールの場合、を設定します **[!UICONTROL Display Page Control]** 対象： `Yes`  次の手順を実行します。

   - を入力 **[!UICONTROL Number of Products per Page]**.

   - 合計を入力 **[!UICONTROL Number of Products to Display]**.

   - を設定 **[!UICONTROL Condition]** 特集する商品のカテゴリーに。

     プロセスは、の条件を設定する場合と同じです。 [価格ルール](../merchandising-promotions/price-rules-catalog.md).

### 手順 4：結果を保存して確認

1. 完了したら、 **[!UICONTROL Save]**.

1. プロンプトが表示されたら、ワークスペースの上部にある手順に従って、必要に応じてキャッシュを更新します。

1. ストアフロントに戻り、ウィジェットが正しく動作していることを確認します。

   別の場所に移動するには、ウィジェットを再度開き、別のページまたはブロック参照を試します。

## ウィジェット作成のデモ

ウィジェットの作成について詳しくは、次のビデオを参照してください。

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12)

## ウィジェットの編集

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. グリッドの上にあるフィルターを使用してウィジェットを見つけ、ウィジェット名をクリックします。

1. 必要な変更を加えます。

   ウィジェットオプションについては、ウィジェットの作成手順を確認してください。

1. 「」をクリックします **[!UICONTROL Save]**.

## ウィジェットの削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. グリッドの上にあるフィルターを使用してウィジェットを見つけ、削除するウィジェットのチェックボックスを選択します。

1. リストの左上隅にあるを設定します。 **[!UICONTROL Actions]** 対象： `Delete`.

1. 完了したら、 **[!UICONTROL Submit]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.
