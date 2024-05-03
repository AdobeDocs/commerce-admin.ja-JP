---
title: ページワークスペースコントロール
description: コンテンツページの検索と更新に使用する Workspace ツールについて説明します。
exl-id: c53e3e70-9f88-46ec-b44d-133a2ff5d0d5
feature: Page Content, Admin Workspace
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 0%

---

# ページワークスペースコントロール

ページワークスペースには、必要なページをすばやく見つけるのに役立つツールや、個々のページまたは複数のページで日常的なメンテナンスを実行するコマンドが含まれています。 また、グリッドからページプロパティをすばやく更新することもできます。

![ページグリッド](./assets/pages-grid.png){width="700" zoomable="yes"}

## ページプロパティをすばやく更新

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.
1. グリッドの任意の行をクリックします。

   ![ページプロパティは、ページグリッドで編集できます](./assets/page-grid-properties-update.png){width="600" zoomable="yes"}

   複数のレコードを選択するには、更新する各行のチェックボックスをオンにします。

1. 次のいずれかのプロパティを更新します。

   - **[!UICONTROL Title]**
   - **[!UICONTROL URL Key]**
   - **[!UICONTROL Status]**
   - **[!UICONTROL Layout]**

1. 完了したら、 **[!UICONTROL Save]**.

## ワークスペースコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL Add New Page] | ページを追加します。 |
| [!UICONTROL Search] | 現在のフィルターに基づいてカタログ検索を開始します。 |
| [!UICONTROL Actions] | リスト内の選択した項目に適用できるすべてのアクションをリストします。 1 つのページまたは複数のページにアクションを適用するには、アクションの対象となる各レコードの最初の列にあるチェックボックスを選択します。 オプション： `Delete` / `Disable` / `Enable` / `Edit` |
| [!UICONTROL Select] | 最初の列のヘッダーにあるコントロールを使用すると、アクションのターゲットとして複数のレコードを選択できます。 選択する各レコードの最初の列のチェックボックスをオンにします。 オプション： `Select All` / `Deselect All` |
| [!UICONTROL Save Edits] | 選択したレコードに現在のアクションを適用します。 |
| [!UICONTROL Edit] | レコードを編集モードで開きます。 行の任意の場所をクリックして、同じことを達成できます。 |

{style="table-layout:auto"}

## 列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Select] | 最初の列のチェックボックスは、複数のレコードを選択するために使用されます。 オプション： `Select All` / `Deselect All` |
| [!UICONTROL ID] | この ID は、各ページに割り当てられる増分数です。 |
| [!UICONTROL Title] | ページの上部に表示されるタイトル。 |
| [!UICONTROL URL Key] | URL キーはファイル名に似ており、URL 内のページを識別します。 |
| [!UICONTROL Layout] | ページのメインコンテンツ領域の右側にサイドバーを表示するか、左側にサイドバーを表示するかを指定します。 オプション： `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` |
| [!UICONTROL Store View] | ページを特定のストア表示に関連付けるために使用されます。 |
| [!UICONTROL Status] | ページがオンラインかオフラインかを示します。 オプション： `Enabled` / `Disabled` |
| [!UICONTROL Created] | ページが作成された日付。 |
| [!UICONTROL Modified] | ページが最後に変更された日付。 |
| [!UICONTROL Action] | 個々のレコードに適用できるアクションを以下に示します。<br/>**[!UICONTROL Edit]**- ページを編集モードで開きます。<br/>**[!UICONTROL Delete]** - ページを削除します。<br/>**[!UICONTROL View]**- ページをプレビューモードで表示します。 |

{style="table-layout:auto"}

## その他の列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Custom design from/to] | 選択したデザインがページに適用される開始日と終了日を指定します。 ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）。 |
| [!UICONTROL Custom Theme] | ページにカスタムテーマを適用します |
| [!UICONTROL Custom Layout] | ページのカスタムレイアウトを決定します |
| [!UICONTROL Meta Title] | ページのメタタイトル |
| [!UICONTROL Meta Keywords] | ページのメタキーワード |
| [!UICONTROL Meta Description] | ページのメタ説明 |

{style="table-layout:auto"}

## ページ検索

の左上にある検索ボックス _[!UICONTROL Pages]_grid を使用すると、キーワードで特定のページを検索できます。 より高度な検索では、次のことができます [フィルター](../getting-started/admin-grid-controls.md) 複数のパラメーターによる検索。

### キーワードで検索

1. ページ検索ボックスに検索語句を入力します。

1. 結果を表示するには、検索（![虫眼鏡アイコン](../assets/icon-magnify-search.png)） アイコンをクリックします。

   結果には、キーワードを含むすべてのページが含まれます。

### 検索結果のフィルタリング

1. 必要に応じて、 **[!UICONTROL Clear All]** 直前の検索条件をクリアします。

1. 検索フィルターの選択を表示するには、をクリックします **[!UICONTROL Filters]** !（[ファネルアイコン](../assets/icon-filter-search.png)） タブを選択します。

1. 検索するページを説明するために、必要な数のフィルターを入力します。

1. クリック **[!UICONTROL Apply Filters]** をクリックして結果を表示します。

### フィルターを検索

| フィルター | 説明 |
|--- |--- |
| [!UICONTROL ID] | ページレコード ID で検索をフィルタリングします。 |
| [!UICONTROL Title] | ページタイトルに基づいて検索をフィルタリングします。 |
| [!UICONTROL URL Key] | URL キーで検索をフィルタリングします。 |
| [!UICONTROL Created] | ページを作成した日付で検索をフィルタリングします。 |
| [!UICONTROL Modified] | ページが最後に変更された日付に基づいて検索をフィルタリングします。 |
| [!UICONTROL Store View] | ストア表示に基づいて検索をフィルタリングします。 オプション： `All available` / `Store Views` |
| [!UICONTROL Layout] | ページレイアウトに基づいて検索をフィルタリングします。 オプション： `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` |
| [!UICONTROL Status] | ページステータスで検索をフィルタリングします。 オプション： `Disabled` / `Published` |
| [!UICONTROL Custom design from / to] | 選択したデザインがページに適用された場合は、開始日と終了日で検索をフィルタリングします。 ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）。 |
| [!UICONTROL Asset] | ページタイトルアセットで検索をフィルタリングします |
| [!UICONTROL Custom Layout] | カスタムレイアウトに基づいて検索をフィルタリングします。 オプション： `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` / `Page -- Full Width` / `Category -- Full Width` / `Product -- Full Width` |
| [!UICONTROL Custom Theme] | カスタムテーマに基づいて検索をフィルタリングします。 デフォルトのオプション： `Magento Blank` / `Magento Luma` |
| [!UICONTROL Meta Keywords] | ページのメタキーワードに基づいて検索をフィルタリングします。 |
| [!UICONTROL Meta Title] | ページのメタタイトルに基づいて検索をフィルタリングします。 |
| [!UICONTROL Meta Description] | ページのメタ説明に基づいて検索をフィルタリングします。 |

{style="table-layout:auto"}

### 検索ツール

| ツール | 説明 |
|--- |--- |
| [!UICONTROL Apply Filters] | すべてのフィルターを検索結果に適用します。 |
| [!UICONTROL Cancel] | 現在の検索をキャンセルします。 |
| [!UICONTROL Clear All] | すべての検索フィルターをクリアします。 |

{style="table-layout:auto"}

## ページアクション

ページの編集、無効化、有効化および削除が可能です。 個々のページにアクションを適用するには、最初の列のチェックボックスを選択します。 すべてのページを選択または選択解除するには、列の上部にある選択コントロールを使用します。

![ページアクション](./assets/pages-select.png){width="400" zoomable="yes"}

### 単一アクション

の使用 _[!UICONTROL Action]_右端の列：個々のページに次のアクションのいずれかを適用します。

- [!UICONTROL Edit]  – 編集モードでページを開きます
- [!UICONTROL Delete] - ページを削除します（確認が必要）
- [!UICONTROL View] - ストアフロントで直接ページを開きます

![単一ページアクション](./assets/page-grid-actions.png){width="600" zoomable="yes"}

### 一括アクション

を使用して、選択した複数のページに対して、次のアクションのいずれかを同時に適用します。 _[!UICONTROL Action]_左上隅のセレクター：

- [!UICONTROL Delete] - ページを削除します（確認が必要）
- [!UICONTROL Disable] - ストアフロントでページを無効にします
- [!UICONTROL Enable] - ストアフロントでページを有効にします
- [!UICONTROL Edit]  – 編集モードでグリッドの列を開きます（**[!UICONTROL Title]**, **[!UICONTROL URL Key]**, **[!UICONTROL Layout]**、および **[!UICONTROL Status]**）

## ページグリッドレイアウト

列の選択とグリッド内の順序は、必要に応じて変更できます。 新しい列の配置を保持するには、これをビューとして保存します。

### 列の選択の変更

右上隅のをクリックします _列_ （![列アイコン](../assets/icon-columns.png)）を制御し、次の操作を行います。

- グリッドに追加する任意の列のチェックボックスをオンにします。

- グリッドから削除する列のチェックボックスをオフにします。

### 列の移動

1. 列のヘッダーをクリックしてホールドします。

1. 列を新しい位置にドラッグして、マウスボタンを放します。

### ビューの保存

1. 「」をクリックします _表示_ （![目のアイコン](../assets/icon-view-eye.png)） コントロールし、 **[!UICONTROL Save View As]**.

1. ビューの名前を入力します。

1. ビューを保存するには、 _矢印_ （![矢印アイコン](../assets/icon-arrow-save.png)）に設定します。

   ビューの名前が現在のビューとして表示されます。

### ビューの変更

「」をクリックします _表示_ （![目のアイコン](../assets/icon-view-eye.png)）を制御し、次のいずれかの操作を行います。

- 使用するビューを選択します。

- 編集（）をクリックして、ビューの名前を変更する![鉛筆アイコン](../assets/icon-edit-pencil.png)）アイコンで表示され、名前を更新します。

  ![保存したビューは、編集アイコンとともにビューコントロールに表示されます](./assets/pages-default-grid-control.png){width="600" zoomable="yes"}

## スケジュールされた変更

{{ee-feature}}

ページの変更はスケジュールに従って適用でき、他のコンテンツの変更と共にグループ化できます。 ページに対してスケジュールされた変更に基づいてキャンペーンを作成したり、既存のキャンペーンに変更を適用したりできます。 詳しくは、を参照してください [コンテンツのステージング](content-staging.md).

>[!NOTE]
>
>この [!UICONTROL Custom Design Update] タブがで削除されました ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceであり、ページ上で直接変更することはできません。 これらのアクティベーションに対して、スケジュールされた更新を作成する必要があります。

>[!NOTE]
>
>スケジュールされた更新はすべて連続して適用されます。つまり、どのエンティティも、1 つのポイントで 1 つのスケジュールされた更新しか持つことができません。 スケジュールされた更新は、その期間内のすべてのストアビューに適用されます。 その結果、1 つのエンティティに対して、異なるストア表示の異なるスケジュールされた更新を同時に行うことはできません。 現在スケジュールされている更新の影響を受けないすべてのストアビュー内のすべてのエンティティ属性値は、前回スケジュールされた更新ではなく、デフォルト値から取得されます。

![ホームページの上部に、スケジュールされた変更が表示されます](./assets/page-scheduled-change.png){width="600" zoomable="yes"}

>[!NOTE]
>
>キャンペーン開始日と終了日は、を使用して定義する必要があります **_default_** 各 web サイトのローカルタイムゾーンから変換される管理タイムゾーン。 異なるタイムゾーンに複数の web サイトがあり、米国のタイムゾーンに基づいてキャンペーンを開始する例を考えてみましょう。 この場合、ローカルタイムゾーンごとに個別の更新をスケジュールし、を設定する必要があります **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** 各ローカル Web サイトのタイムゾーンからデフォルトの管理者のタイムゾーンに変換されました。

また、製品アップデートの変更をスケジュールおよびプレビューすることもできます。 詳しくは、を参照してください [更新のスケジュール設定](content-staging-scheduled-update.md).
