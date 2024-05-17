---
title: ページ階層
description: ページ階層システムを使用して、コンテンツページを整理し、ページネーション、ナビゲーション、メニューを追加する機能を提供する方法を説明します。
exl-id: 2ce79b85-1420-4640-a4f7-0143a608a71a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# ページ階層

{{ee-feature}}

ストアページ階層システムを使用すると、コンテンツページを整理し、ページネーション、ナビゲーションおよびメニューを追加できます。 サンプルデータのプライバシーポリシーページは、左側にメニューがあるページの例です。 大量のコンテンツを定期的に公開する場合は、ページ階層を使用してコンテンツを整理し、関心のある記事をユーザーが簡単に見つけられるようにすることができます。

ページ階層システムは、ノードを使用して、関連するコンテンツ部分を識別し、コンテンツページを親子関係に整理します。 親ノードは、子ノードおよびページを含む可能性のあるフォルダーに似ています。 階層内の各ノードとページの相対位置は、次のように表示されます _ツリー_ 構造。 ノードには、他のノードやコンテンツページが含まれ、1 つのコンテンツページが、親/子または近隣の関係の複数のノードや他のコンテンツページに関連付けられる場合があります。

![左側にナビゲーションを使用したページ](./assets/storefront-privacy-policy.png){width="600" zoomable="yes"}

## ページ階層の設定

構成設定により、ページ階層システムおよびメタデータがアクティブ化され、デフォルトのメニューレイアウトが決定されます。

![CMS ページ階層](./assets/content-management-cms-page-hierarchy.png){width="600" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Content Management]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL CMS Page Hierarchy]**  必要な変更を加えます。

1. 完了したら、 **[!UICONTROL Save Config]**.

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | コンテンツページに対してページ階層の使用をアクティベートします。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | このオプションを有効にすると、メタデータを階層内のページに関連付けることができます。 オプション： `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | 既定のメニュースタイルを決定します。 オプション： `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## 階層ノードの追加

次の例では、関連するコンテンツページへの簡単なナビゲーションを使用してノードを作成する方法を示しています。 ノードにはコンテンツページが関連付けられていませんが、サイトの他の場所で参照できる URL キーがあります。

例えば、というノードを作成できます。 _プレスリリース_ 個々のプレスリリースへのナビゲーションが可能です。 次に、 _会社情報_ ノードに移動します。 または、ニュースレターのバックイシューのコレクション用のノードを作成することもできます。

ノードにリンクするには、を使用します [ウィジェット](widgets.md) cms 階層ノードリンクを作成し、コンテンツブロックまたはページにウィジェットを配置するためのツール。

![会社概要ページのナビゲーションメニューの例](./assets/page-navigation-storefront.png){width="600" zoomable="yes"}

### 手順 1：ノードを作成する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Hierarchy]**.

   ![CMS ページグリッド](./assets/page-hierarchy-cms-pages.png){width="600" zoomable="yes"}

1. グリッドの上で、をクリックします **[!UICONTROL Add Node...]**.

1. 次の下 _[!UICONTROL Page Properties]_、a と入力します&#x200B;**[!UICONTROL Title]**ノードおよび適切な&#x200B;**[!UICONTROL URL Key]**.

   URL キーは、ノードの一意の web アドレスを提供します。 スペースではなくハイフンを使用して単語を区切り、すべて小文字にする必要があります。

   ![ページプロパティ](./assets/page-hierarchy-add-node-page-properties.png){width="500" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.

   ノードは、ページの左側のツリーにフォルダーとして表示されます。

### 手順 2：ノードへのページの追加

1. 階層ツリーで、ノードをクリックして選択します。

1. クリック **[!UICONTROL Add Selected Pages(s) to Tree]**.

   上にスクロールすると、選択した各ページがノードフォルダーの下のツリーに表示されます。

### 手順 3：構造の定義

1. 必要に応じて、ページをメニューに表示する順序を反映する位置にドラッグします。

   ![ページをドラッグして配置](./assets/page-hierarchy-drag-to-position.png){width="500" zoomable="yes"}

1. 階層の最上位にあるノードをクリックします。

   この _[!UICONTROL Page Properties]_ノードに関する情報がセクションに表示されるようになりました。

1. 次の下 **[!UICONTROL Render Metadata in HTML Head]**、次の手順を実行します。

   ![メタデータ設定のレンダリング](./assets/page-hierarchy-render-metadata.png){width="400" zoomable="yes"}

   - ノードを階層の最上位として識別するには、を設定します **[!UICONTROL First]** 対象： `Yes`.

   - ページネーションコントロールを表示するには、を設定します **[!UICONTROL Next/Previous]** 対象： `Yes`.

   - 階層内のページをブックとして整理するには、次のように設定します **[!UICONTROL Enable Chapter/Section]** 対象： `Yes`.

     ノードをブックの一部として含めない場合は、デフォルトのままにします `No`.

   - ノードをブックの特定の部分に割り当てるには、次のように設定します **[!UICONTROL Chapter/Section]** を次のいずれかに変更します。

      - `No` - ノードをチャプター/セクションとして定義しません。
      - `Chapter`  – 現在のノードをチャプターとして割り当てます。
      - `Section`  – 現在のノードをセクションとして割り当てます。
      - `Both`  – 現在のノードをチャプターとセクションの両方として割り当てます。

### 手順 4：ページネーションコントロールの追加

1. 次の下 _ネストされたページのページネーションオプション_、設定 **[!UICONTROL Enable Pagination]** 対象： `Yes`.

1. の場合 **[!UICONTROL Frame]**&#x200B;で、ページネーションコントロールに含めるページリンクの数を入力します。

   ページネーションコントロールに含めることができるページが階層内にまだある場合。

1. の場合 **[!UICONTROL Frame Skip]**&#x200B;で、次のページネーションリンクのセットのために前にスキップ（または後ろにスキップ）するページ数を入力します。

### 手順 5：メニューレイアウトの選択

メニューにノードを表示する場合は、次の操作を行います。

1. 次の下 _ページナビゲーションメニューオプション_、設定 **[!UICONTROL Show in navigation menu]** 対象： `Yes`.

   この設定により、ページ階層にナビゲーションメニューを生成するかどうかが決まります。

   ![ページナビゲーションメニューオプション](./assets/page-hierarchy-page-navigation-menu-options.png){width="300" zoomable="yes"}

1. コンテンツに関連するメニューの場所を指定するには、 **[!UICONTROL Menu Layout]**:

   - `Content` - メニューレイアウトがコンテンツ内にある。
   - `Use Default`  – で指定されたメニュースタイルを使用します。 [設定](../configuration-reference/general/content-management.md).
   - `Left Column` - メニューがコンテンツの左側に表示されます。
   - `Right Column` - メニューがコンテンツの右側に表示されます。

1. メニューに含める詳細を指定するには、を設定します **[!UICONTROL Menu Detalization]** を次のいずれかに変更します。

   - `Only Children` - メニューにサブページのみを含めます。
   - `Neighbours and Children`  – 階層内の同じレベルにあるサブページとその他のページを含みます。

1. メニューの深さを決定するには、 **[!UICONTROL Maximal Depth]** 含めるレベルの最大数。

1. メニューをフォーマットするには、 **[!UICONTROL List Type]**:

   - `Unordered` - メニューオプションには番号が付けられておらず、箇条書きまたは箇条書きなしで書式設定できます。 順不同リストタイプのオプション：デフォルト/円/ディスク/正方形
   - `Ordered` - メニューオプションには番号が付けられ、大文字または小文字の数字、アルファベット、またはローマ数字の形式を設定できます。

1. を設定 **[!UICONTROL List Style]** を次のいずれかに変更します。

   - `Circle`
   - `Disc`
   - `Square`

1. ノードをナビゲーションメニューにも表示する場合は、にスクロールします。 _メインナビゲーションメニューオプション_ およびを設定 **[!UICONTROL Show in Navigation menu]** 対象： `Yes`.

   ![メインナビゲーションメニューオプション](./assets/page-hierarchy-main-navigation-menu-options.png){width="250" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.
