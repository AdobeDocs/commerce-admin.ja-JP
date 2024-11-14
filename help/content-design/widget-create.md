---
title: ウィジェットの作成と管理
description: ストア全体のコンテンツを自動的に更新するウィジェットを作成および管理する方法について説明します。
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# ウィジェットの作成と管理

ウィジェットは再利用可能なコンポーネントです。 ウィジェットを簡単に作成し、既存のウィジェットを変更して、ストア全体のコンテンツを自動的に更新できます。 使用されなくなったウィジェットを削除することもできます。

![ ウィジェット ](./assets/widgets.png){width="700" zoomable="yes"}

## ウィジェットを作成

ウィジェットの作成プロセスは、[ ウィジェットタイプ ](widgets.md#widget-types) ごとに同じです。 手順の最初の部分に従ってから、必要な特定のタイプのウィジェットの最後の部分を完了できます。

### 手順 1：タイプの選択

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Widgets]**に移動します。

1. 「**[!UICONTROL Add Widget]**」をクリックします。

1. _[!UICONTROL Settings]_のセクションで以下を実行します。

   - 作成するウィジェットのタイプに **[!UICONTROL Type]** を設定します。

   - **[!UICONTROL Design Theme]** が現在のテーマに設定されていることを確認します。

     ![ ウィジェット設定 ](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Continue]**」をクリックします。

### 手順 2：ストアフロントのプロパティとレイアウトを指定する

1. _[!UICONTROL Storefront Properties]_のセクションで以下を実行します。

   - **[!UICONTROL Widget Title]** しくは、ウィジェットのわかりやすいタイトルを入力します。

     このタイトルは、管理者からのみ表示されます。

   - **[!UICONTROL Assign to Store Views]**：ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択することも、`All Store Views` を選択することもできます。 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]** の場合は、数字を入力して、この項目がページの同じ部分に他の項目と共に表示される順序を決定します。 （`0` = 1 番目、`1` = 2 番目、`3` = 3 番目など）。

     ![ ストアフロントのプロパティ ](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. 「_[!UICONTROL Layout Updates]_」セクションで、「**[!UICONTROL Add Layout Update]**」をクリックします。

1. ページの表示タイプに **[!UICONTROL Display On]** を設定します。

1. **[!UICONTROL Container]** リストで、ページレイアウトを配置する領域を選択します。

   ![ レイアウトの更新 ](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. ウィジェットがリンクの場合は、**[!UICONTROL Template]** を次のいずれかに設定します。

   - `Block Template` - ページ上にスタンドアロンの単位として配置できるように、コンテンツをフォーマットします。
   - `Inline Template` – 他のコンテンツの中に配置できるようにコンテンツを書式設定します。 例えば、テキストの段落内に入るリンクなどです。

### 手順 3：ウィジェットオプションの完了

各ウィジェットタイプのオプションはわずかに異なりますが、プロセスは基本的に同じです。 次の例では、ページネーションコントロールを使用して、特定のカテゴリの製品リストを表示します。

1. 左側のパネルで「**[!UICONTROL Widget Options]**」を選択します。

1. 「**[!UICONTROL Select Block]**」をクリックします。

1. リストの上に表示する **[!UICONTROL Title]** を入力します（例：`Featured Products`）。

1. ページネーションコントロールの場合は、**[!UICONTROL Display Page Control]** を `Yes` に設定して、次の操作を行います。

   - **[!UICONTROL Number of Products per Page]** を入力します。

   - 合計 **[!UICONTROL Number of Products to Display]** を入力します。

   - **[!UICONTROL Condition]** を、取り上げる製品のカテゴリに設定します。

     プロセスは、[ 価格ルール ](../merchandising-promotions/price-rules-catalog.md) の条件を設定する場合と同じです。

### 手順 4：結果を保存して確認

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. プロンプトが表示されたら、ワークスペースの上部にある手順に従って、必要に応じてキャッシュを更新します。

1. ストアフロントに戻り、ウィジェットが正しく動作していることを確認します。

   別の場所に移動するには、ウィジェットを再度開き、別のページまたはブロック参照を試します。

## ウィジェット作成のデモ

ウィジェットの作成について詳しくは、次のビデオを参照してください。

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12&learn=on)

## ウィジェットの編集

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Widgets]**に移動します。

1. グリッドの上にあるフィルターを使用してウィジェットを見つけ、ウィジェット名をクリックします。

1. 必要な変更を加えます。

   ウィジェットオプションについては、ウィジェットの作成手順を確認してください。

1. **[!UICONTROL Save]** をクリックします。

## ウィジェットの削除

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Widgets]**に移動します。

1. グリッドの上にあるフィルターを使用してウィジェットを見つけ、削除するウィジェットのチェックボックスを選択します。

1. リストの左上隅にある **[!UICONTROL Actions]** を `Delete` に設定します。

1. 完了したら、「**[!UICONTROL Submit]**」をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。
