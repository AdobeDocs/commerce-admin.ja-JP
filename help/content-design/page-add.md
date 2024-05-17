---
title: ページの追加と削除
description: で使用されているコンテンツページを追加および削除する方法を説明します [!DNL Commerce] ストア。
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# ページの追加と削除

コンテンツページをストアに追加するプロセスは、作成する可能性のあるすべてのタイプのページで基本的に同じです。 テキスト、画像、コンテンツブロック、変数およびウィジェットを含めることができます。 ほとんどのコンテンツページは、最初は検索エンジンで、2 番目は人物で読むように設計されています。 ページタイトルや URL を選択する際と、メタデータやコンテンツを構成する際は、これら 2 つの異なるオーディエンスのニーズを念頭に置いてください。 ページが完成したら、ストアのナビゲーションに追加したり、他のページにリンクしたり、ストアのフッターからリンクしたり、新しいページとして使用したりできます [ホームページ](page-home-new.md).

![ページグリッド](./assets/pages-grid.png){width="700" zoomable="yes"}

## ページを追加

以下の手順では、基本的なページを作成するための各手順について説明します。 一部の高度な機能は飛ばされますが、他のトピックで説明しています。

### 手順 1：ページを作成する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. クリック **[!UICONTROL Add New Page]**.

   ![新しいページ](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. ページをすぐに公開しない場合、次のように設定します **[!UICONTROL Enable Page]** 対象： `No`.

1. を入力 **[!UICONTROL Page Title]**.

   にページタイトルが表示されます [パンくず](../catalog/navigation-breadcrumb-trail.md) ナビゲーション。

### 手順 2：コンテンツを完了する

状況によって [高度なコンテンツツールの設定](../configuration-reference/general/content-management.md)ページのコンテンツを追加します。

#### ページビルダーのコンテンツツールの使用

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![ページビルダーを使用したコンテンツ](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. が含まれる **[!UICONTROL Content Heading]** ボックスに、ページの先頭に表示する見出しを入力します。

   有効な場合、 [ページビルダー](../page-builder/introduction.md) ステージとパネルは「コンテンツ」見出しの下に表示されます。 詳しくは、を参照してください [ワークスペース](../page-builder/workspace.md). 次の場合 _ページビルダー_ が有効になっていない場合、エディターは WYSIWYG モードで開き、上部にツールバーが表示されます。

1. コンテンツを完成させ、必要に応じてテキストを書式設定します。

#### エディターツールバーの使用

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![コンテンツ](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. が含まれる **[!UICONTROL Content Heading]** ボックスに、ページの先頭に表示する見出しを入力します。

1. コンテンツを完成させ、必要に応じてテキストを書式設定します。

   次を追加できます [画像](media-storage.md), [変数](../systems/variables-predefined.md)、および [ウィジェット](widgets.md) 必要に応じて。 詳しくは、を参照してください [エディターの使用](editor.md).

### 手順 3:SEO 情報の完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![検索エンジンの最適化](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. デフォルトをそのまま使用するか、別の値を入力します **[!UICONTROL URL Key]** これは、すべての小文字で構成され、スペースの代わりにハイフンを使用します。

   デフォルトの URL キーは、ページの保存時に作成されたもので、コンテンツの見出しに基づいています。

1. を入力 **[!UICONTROL Meta Title]** をページ用に使用します。

   メタタイトルは 70 文字未満で入力する必要があり、ブラウザーのタイトルバーとタブに表示されます。

1. 選択した値の高い値を入力してください **[!UICONTROL Meta Keywords]** この検索エンジンは、を使用してページのインデックスを作成できます。

   複数の単語をコンマで区切ります。 メタキーワードは、一部の検索エンジンでは無視されますが、他の検索エンジンでは使用されます。

1. の場合 **[!UICONTROL Meta Description]**&#x200B;を入力し、検索結果リストのページの簡単な説明を入力します。

   説明の長さは 150～160 文字、上限は 255 にしてください。

1. クリック **[!UICONTROL Save]**.

### 手順 4：ページの範囲を指定

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Web サイトのページ](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. が含まれる **[!UICONTROL Store View]** リストで、ページを使用できる各ビューを選択します。

   インストールに複数の web サイトがある場合は、各 web サイトを選択し、ページを使用できるストア表示を選択します。

### 手順 5：親ページを特定する（該当する場合）

{{ee-feature}}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![階層](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. このページが別のページの子である場合は、のチェックボックスをオンにします **[!UICONTROL Parent page]**.

### 手順 6：デザインの変更を入力（オプション）

1. ページのレイアウトを変更するには、を展開します ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![デザイン](./assets/page-design.png){width="600" zoomable="yes"}

1. ページの列レイアウトを変更するには、次を設定します **[!UICONTROL Layout]** を次のいずれかに変更します。

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` （必須 [ページビルダー](../page-builder/introduction.md)）
   - `Category -- Full Width` （ページビルダーが必要）
   - `Product -- Full Width` （ページビルダーが必要）

1. を適用するには **[!UICONTROL Custom Layout Update]**&#x200B;リストからファイルの名前を選択します。

   詳しくは、を参照してください [レイアウトの更新](layout-updates.md).

1. ページのテーマを変更するには、次を設定します **[!UICONTROL New Theme]** を次のいずれかに変更します。

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）設計変更をスケジュールするには、を展開します ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** 次の手順を実行します。

   ![カスタムデザインの更新](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - カレンダーの使用（![カレンダーアイコン](../assets/icon-calendar.png)）を選択して、 **[!UICONTROL From]** および **[!UICONTROL To]** 変更が有効になる日付。

   - ページに別のテーマを適用するには、ページの名前を **[!UICONTROL New Theme]**.

   - ページの列のレイアウトを変更するには、 **[!UICONTROL Layout]** お申し込みください。

### 手順 7：ページのプレビュー

1. 「」をクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]** をクリックしてページグリッドに戻ります。

1. グリッドでページを見つけて、を選択します。 **[!UICONTROL View]** が含まれる _[!UICONTROL Action]_列。

1. グリッドに戻るには、をクリックします **[!UICONTROL Back]** ブラウザーウィンドウの左上隅

### 手順 8：ページの公開

1. を選択 **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_グリッドの列。

1. を設定 **[!UICONTROL Enable Page]** 対象： `Yes`.

1. 「」をクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

## ページの複製

任意のコンテンツページをテンプレートとして使用し、複製として保存できます。 この時間を節約する手法を使用して、サイト全体のコンテンツページに対して一貫したデザインを作成できます。 複製ページには、元のページのページタイトルが保持されますが、URL キーフィールドとステータスフィールドは更新する必要があります。

![保存して複製](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. グリッドで、複製するページを見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 「」をクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Duplicate]**.

1. ページが保存されて複製されたことを示すメッセージが表示されたら、をクリックします。 **[!UICONTROL Back]** 上部のボタンバーでグリッドに戻ります。

1. グリッドで重複ページを見つけて、次の点に注意してください。

   - ページタイトルは元のタイトルと同じです。
   - 一意の一時 URL キーが割り当てられます。
   - ページのステータスは `Disabled`.

1. で複製ページを開きます。 _編集_ をモードにして、次の手順を実行します。

   - ページをすぐに公開する場合は、次のように設定します **[!UICONTROL Enable Page]** 対象： `Yes`.

   - を更新 **[!UICONTROL Page Title]**、必要に応じて。

   - を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization]** 「」セクションに一意のを入力します **[!UICONTROL URL Key]** 複製したページに使用する。

     ![一時 URL キー](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - 必要に応じて、残りのページコンテンツを更新します。

1. 「」をクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

   グリッド内の複製ページに変更内容が反映されます。

## 保存メニュー

| コマンド | 説明 |
|--- |--- |
| [!UICONTROL Save] | 現在のページを保存し、作業を続行します。 |
| [!UICONTROL Save & New] | 現在のページを保存して閉じ、新しいページを開始します。 |
| [!UICONTROL Save & Duplicate] | 現在のページを保存して閉じ、新しい複製コピーを開きます。 |
| [!UICONTROL Save & Close] | 現在のページを保存して閉じ、ページグリッドに戻ります。 |

{style="table-layout:auto"}

## ページの削除

作成したページを削除する方法は 2 つあります。 から削除できます _[!UICONTROL Pages]_グリッドまたは_[!UICONTROL Edit]_ ページ。

### 方法 1：ページグリッドからページを削除する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. グリッドの上でフィルターを使用してページを見つけ、削除する 1 つ以上のページのチェックボックスを選択します。

1. リストの左上隅にあるを設定します。 **[!UICONTROL Actions]** 対象： `Delete`.

1. アクションを確定するには、 **[!UICONTROL OK]**.

### 方法 2：編集ページからページを削除する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 削除するページを検索します。

1. が含まれる _[!UICONTROL Actions]_ページエンティティの列で、をクリックします&#x200B;**[!UICONTROL Select]**を選択します&#x200B;**[!UICONTROL Edit]**.

1. ボタン バーで、をクリックします **[!UICONTROL Delete Page]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.
