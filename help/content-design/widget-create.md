---
title: ウィジェットの作成と管理
description: ストア全体でコンテンツを自動的に更新するウィジェットを作成および管理する方法について説明します。
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# ウィジェットの作成と管理

ウィジェットは再利用可能なコンポーネントです。 ストア全体でウィジェットを簡単に作成し、既存のウィジェットを変更してコンテンツを自動的に更新することができます。 また、使用されなくなったウィジェットを削除することもできます。

![ウィジェット](./assets/widgets.png){width="700" zoomable="yes"}

## ウィジェットを作成

ウィジェットの作成プロセスは、それぞれでほぼ同じです [ウィジェットの種類](widgets.md#widget-types). 手順の最初の部分に従って、必要な特定のタイプのウィジェットの最後の部分を完了できます。

### 手順 1：タイプの選択

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. クリック **[!UICONTROL Add Widget]**.

1. Adobe Analytics の _[!UICONTROL Settings]_セクション：

   - 設定 **[!UICONTROL Type]** を、作成するウィジェットタイプに追加します。

   - 次を確認します。 **[!UICONTROL Design Theme]** が現在のテーマに設定されている。

     ![ウィジェット設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Continue]**.

### 手順 2：ストアフロントのプロパティとレイアウトの指定

1. Adobe Analytics の _[!UICONTROL Storefront Properties]_セクション：

   - の場合 **[!UICONTROL Widget Title]**」で、ウィジェットの説明的なタイトルを入力します。

     このタイトルは管理者からのみ表示されます。

   - の場合 **[!UICONTROL Assign to Store Views]**」で、ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択するか、 `All Store Views`. 複数のビューを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

   - （オプション）の場合 **[!UICONTROL Sort Order]**」、数値を入力して、この項目がページの同じ部分に他の項目と共に表示される順序を決定します。 (`0` =最初 `1` =秒 `3` = 3 番目、など )

     ![ストアフロントのプロパティ](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. Adobe Analytics の _[!UICONTROL Layout Updates]_セクションで、**[!UICONTROL Add Layout Update]**.

1. 設定 **[!UICONTROL Display On]** を、表示するページのタイプに設定します。

1. Adobe Analytics の **[!UICONTROL Container]** リストで、ページレイアウトを配置する領域を選択します。

   ![レイアウトの更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. ウィジェットがリンクの場合は、 **[!UICONTROL Template]** を次のいずれかに変更します。

   - `Block Template`  — ページ上にスタンドアロン単位として配置できるようにコンテンツをフォーマットします。
   - `Inline Template`  — コンテンツを他のコンテンツ内に配置できるようにフォーマットします。 例えば、テキストの段落内に移動するリンクなどです。

### 手順 3：ウィジェットオプションの設定

各ウィジェットタイプのオプションは若干異なりますが、基本的に同じ処理です。 次の使用例は、特定のカテゴリの製品リストを、ページネーションコントロールと共に表示します。

1. 左側のパネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. クリック **[!UICONTROL Select Block]**.

1. を入力します。 **[!UICONTROL Title]** リストの上に表示する `Featured Products`.

1. ページネーションコントロールの場合、 **[!UICONTROL Display Page Control]** から `Yes`  次の操作を実行します。

   - 次を入力します。 **[!UICONTROL Number of Products per Page]**.

   - 合計を入力 **[!UICONTROL Number of Products to Display]**.

   - 設定 **[!UICONTROL Condition]** を、取り上げる製品のカテゴリに追加します。

     この手順は、 [価格ルール](../merchandising-promotions/price-rules-catalog.md).

### 手順 4：保存して結果を確認する

1. 完了したら、「 **[!UICONTROL Save]**.

1. 必要に応じて、ワークスペースの上部に表示される指示に従ってキャッシュを更新します。

1. ストアフロントに戻り、ウィジェットが正しく機能していることを確認します。

   別の場所に移動するには、ウィジェットを再度開いて、別のページまたはブロック参照を試すことができます。

## ウィジェット作成のデモ

ウィジェットの作成について詳しくは、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12)

## ウィジェットを編集する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. グリッドの上のフィルターを使用してウィジェットを探し、ウィジェット名をクリックします。

1. 必要な変更を加えます。

   ウィジェットのオプションについて詳しくは、ウィジェットの作成手順を確認してください。

1. 次をクリック： **[!UICONTROL Save]**.

## ウィジェットの削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. グリッドの上のフィルターを使用してウィジェットを見つけ、削除するウィジェットのチェックボックスをオンにします。

1. リストの左上隅で、 **[!UICONTROL Actions]** から `Delete`.

1. 完了したら、「 **[!UICONTROL Submit]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.
