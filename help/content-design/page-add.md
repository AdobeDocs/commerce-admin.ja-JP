---
title: ページの追加と削除
description: 以下では、 [!DNL Commerce] ストア。
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# ページの追加と削除

コンテンツページをストアに追加するプロセスは、基本的に、作成する可能性のあるどのタイプのページでも同じです。 テキスト、画像、コンテンツのブロック、変数およびウィジェットを含めることができます。 ほとんどのコンテンツページは、最初に検索エンジンで読み取るように設計され、次にユーザーで読むように設計されています。 ページのタイトルと URL を選択する場合、およびメタデータやコンテンツを構成する場合は、これら 2 つの異なるオーディエンスのそれぞれのニーズに注意してください。 ページが完了したら、そのページをストアのナビゲーションに追加したり、他のページにリンクしたり、ストアのフッターからリンクしたり、新しいページとして使用したりできます [ホームページ](page-home-new.md).

![ページグリッド](./assets/pages-grid.png){width="700" zoomable="yes"}

## ページを追加

次の手順では、各手順を実行して基本ページを作成します。 一部の高度な機能はスキップされますが、他のトピックでは説明します。

### 手順 1：ページの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. クリック **[!UICONTROL Add New Page]**.

   ![新しいページ](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. ページをすぐに公開しない場合は、 **[!UICONTROL Enable Page]** から `No`.

1. 次を入力します。 **[!UICONTROL Page Title]**.

   ページタイトルが [パンくず](../catalog/navigation-breadcrumb-trail.md) ナビゲーション。

### 手順 2：コンテンツの完了

次の条件に応じて、 [高度なコンテンツツールの設定](../configuration-reference/general/content-management.md)、ページコンテンツを追加します。

#### ページビルダーコンテンツツールの使用

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Page Builder を使用したコンテンツ](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Content Heading]** 」ボックスに、ページの上部に表示する見出しを入力します。

   有効にした場合、 [Page Builder](../page-builder/introduction.md) ステージとパネルが「コンテンツ見出し」の下に表示されます。 詳しくは、 [Workspace](../page-builder/workspace.md). 次の場合 _Page Builder_ が有効になっていない場合、エディターは WYSIWYG モードで開き、上部にツールバーが表示されます。

1. コンテンツを入力し、必要に応じてテキストを書式設定します。

#### エディターツールバーを使用する

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![コンテンツ](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Content Heading]** 」ボックスに、ページの上部に表示する見出しを入力します。

1. コンテンツを入力し、必要に応じてテキストを書式設定します。

   次の項目を追加できます。 [画像](media-storage.md), [変数](../systems/variables-predefined.md)、および [widgets](widgets.md) 必要に応じて。 詳しくは、 [エディターの使用](editor.md).

### 手順 3:SEO 情報の入力

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![検索エンジンの最適化](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. デフォルトを受け入れるか、別の **[!UICONTROL URL Key]** すべての小文字で構成され、スペースの代わりにハイフンが使用されます。

   デフォルトの URL キーは、ページの保存時に作成され、コンテンツ見出しに基づいています。

1. を入力します。 **[!UICONTROL Meta Title]** を設定します。

   メタタイトルは 70 文字未満で、ブラウザーのタイトルバーおよびタブに表示されます。

1. 高価値の選択肢を入力 **[!UICONTROL Meta Keywords]** 検索エンジンがページのインデックスを作成する際に使用できる

   複数の単語をコンマで区切ります。 メタキーワードは、一部の検索エンジンでは無視され、他の検索エンジンでは使用されます。

1. の場合 **[!UICONTROL Meta Description]**」をクリックし、検索結果リストのページの簡単な説明を入力します。

   理想的には、説明の長さは 150～160 文字で、最大値は 255 文字です。

1. クリック **[!UICONTROL Save]**.

### 手順 4：ページの範囲の指定

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Web サイト内のページ](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Store View]** リストで、ページを使用できる各ビューを選択します。

   インストールに複数の Web サイトがある場合は、各 Web サイトを選択し、ページを使用できる場所にビューを保存します。

### 手順 5：親ページを特定する（該当する場合）

{{ee-feature}}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![階層](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. このページが別のページの子の場合、 **[!UICONTROL Parent page]**.

### 手順 6：デザイン変更の入力（オプション）

1. ページのレイアウトを変更するには、 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![デザイン](./assets/page-design.png){width="600" zoomable="yes"}

1. ページの列のレイアウトを変更するには、 **[!UICONTROL Layout]** を次のいずれかに変更します。

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` （が必要です） [Page Builder](../page-builder/introduction.md))
   - `Category -- Full Width` （Page Builder が必要）
   - `Product -- Full Width` （Page Builder が必要）

1. を適用するには **[!UICONTROL Custom Layout Update]**」で、リストからファイル名を選択します。

   詳しくは、 [レイアウトの更新](layout-updates.md).

1. ページのテーマを変更するには、 **[!UICONTROL New Theme]** を次のいずれかに変更します。

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) デザインの変更をスケジュールするには、 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** 次の操作を実行します。

   ![カスタムデザインの更新](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - カレンダー (![カレンダーアイコン](../assets/icon-calendar.png)) をクリックして、 **[!UICONTROL From]** および **[!UICONTROL To]** 変更を有効にする日付。

   - ページに別のテーマを適用するには、 **[!UICONTROL New Theme]**.

   - ページの列レイアウトを変更するには、 **[!UICONTROL Layout]** 適用する

### 手順 7：ページをプレビューする

1. 次をクリック： **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]** をクリックして、「ページ」グリッドに戻ります。

1. グリッド内のページを探し、「 」を選択します。 **[!UICONTROL View]** （内） _[!UICONTROL Action]_列。

1. グリッドに戻るには、 **[!UICONTROL Back]** をクリックします。

### 手順 8：ページを公開する

1. 選択 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_グリッドの列。

1. 設定 **[!UICONTROL Enable Page]** から `Yes`.

1. 次をクリック： **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

## ページの複製

任意のコンテンツページをテンプレートとして使用し、複製として保存できます。 この時間節約の手法を使用すると、サイト全体のコンテンツページで一貫したデザインを作成できます。 重複したページには元のページのページタイトルが保持されますが、「 URL キー」フィールドと「ステータス」フィールドは更新する必要があります。

![保存して複製](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. グリッドで、複製するページを探し、 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. 次をクリック： **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Duplicate]**.

1. ページが保存および複製されたメッセージが表示されたら、「 」をクリックします。 **[!UICONTROL Back]** をクリックして、グリッドに戻ります。

1. グリッド内で重複するページを見つけ、次の点に注意してください。

   - ページタイトルは元のページと同じです。
   - 一意のが一時的な URL キーが割り当てられます。
   - ページのステータスは `Disabled`.

1. で重複ページを開きます。 _編集_ モードに切り替えて、以下の操作を行います。

   - ページをすぐに公開する場合は、 **[!UICONTROL Enable Page]** から `Yes`.

   - を更新します。 **[!UICONTROL Page Title]**&#x200B;必要に応じて。

   - 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** セクションを開き、一意の **[!UICONTROL URL Key]** を選択します。

     ![一時 URL キー](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - 必要に応じて、残りのページコンテンツを更新します。

1. 次をクリック： **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

   グリッドの重複ページに変更が反映されます。

## 保存メニュー

| コマンド | 説明 |
|--- |--- |
| [!UICONTROL Save] | 現在のページを保存し、作業を続行します。 |
| [!UICONTROL Save & New] | 現在のページを保存して閉じ、新しいページを開始します。 |
| [!UICONTROL Save & Duplicate] | 現在のページを保存して閉じ、新しい複製コピーを開きます。 |
| [!UICONTROL Save & Close] | 現在のページを保存して閉じ、ページグリッドに戻ります。 |

{style="table-layout:auto"}

## ページの削除

作成したページを削除する方法は 2 つあります。 これは、 _[!UICONTROL Pages]_グリッドまたは_[!UICONTROL Edit]_ ページに貼り付けます。

### 方法 1：ページグリッドからページを削除する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. グリッドの上のフィルターを使用してページを見つけ、削除する 1 つ以上のページのチェックボックスをオンにします。

1. リストの左上隅で、 **[!UICONTROL Actions]** から `Delete`.

1. アクションを確定するには、 **[!UICONTROL OK]**.

### 方法 2：編集ページからページを削除する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 削除するページを見つけます。

1. Adobe Analytics の _[!UICONTROL Actions]_列をクリックします。**[!UICONTROL Select]**を選択します。**[!UICONTROL Edit]**.

1. ボタンバーで、 **[!UICONTROL Delete Page]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.
