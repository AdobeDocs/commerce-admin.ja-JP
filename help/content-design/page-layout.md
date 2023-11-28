---
title: ページレイアウト
description: ページレイアウトセクションとデフォルトレイアウトの設定方法について説明します。
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# ページレイアウト

ストア内の各ページのレイアウトは、ページのヘッダー、フッター、コンテンツ領域を定義する個別のセクションまたはコンテナで構成されます。 レイアウトによっては、各ページに 1 列、2 列、3 列以上が含まれる場合があります。 レイアウトは、 _平面図_ 」をクリックし、CMS、製品、カテゴリの各ページのデフォルトとして使用する特定のレイアウトを割り当てます。

ページ上で、コンテンツブロックはフロート形式で、 [ページレイアウト](layout-updates.md) 表示する場所に割り当てられます。 レイアウトを 3 列から 2 列のレイアウトに変更すると、メイン領域のコンテンツが拡張され、使用可能なスペースが埋められます。 また、未使用のサイドバーに関連付けられているブロックが消えているように見えることにも注意してください。 ただし、3 列のレイアウトに戻すと、ブロックが再び表示されます。 この流体のアプローチ、または _液体配置_&#x200B;を使用すると、コンテンツを再作業することなく、ページレイアウトを変更できます。 個々のHTMLページの操作に慣れている場合は、このモジュラー型の _構築ブロック_ アプローチには違う考え方が必要です

![標準の 2 列（左側のバーのページレイアウトを含む）](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## デフォルトレイアウトの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Default Layouts]** 」セクションに入力します。

   ![デフォルトのレイアウト](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL Default Product Layout]** 製品ページに使用する

   この設定は、製品ページでデフォルトで使用されるレイアウトを決定します。

   - `No layout updates`  — 製品ページのレイアウトの更新は利用できません。
   - `Empty`  — 製品ページで空のレイアウトを使用します。
   - `1 column`  — 製品ページで単一列のレイアウトを使用します。
   - `2 columns with left bar`  — 製品ページの左側にサイドバーがある 2 列のレイアウトを使用します。
   - `2 columns with right bar`  — 製品ページの右側にサイドバーがある 2 列のレイアウトを使用します。
   - `3 columns`  — 商品ページの左右にサイドバーがある 3 列のレイアウトを使用します。

   条件 [Page Builder](../page-builder/introduction.md) が有効な場合、追加の全幅オプションを使用できます。 その後、ページビルダーのコンテンツツールを使用して、製品ページのレイアウトをデザインできます。

   - `Page -- Full Width`  — を使用します。 _ページ — 全幅_  製品ページのレイアウト。
   - `Category -- Full Width`  — を使用します。 _カテゴリ — 全幅_ 製品ページのレイアウト。
   - `Product -- Full Width` - （推奨） _製品 — 全幅_ 製品ページのレイアウト。

1. を選択します。 **[!UICONTROL Default Category Layout]** をカテゴリページに使用します。

   この設定は、カテゴリページでデフォルトで使用されるレイアウトを決定します。

   - `No layout updates`  — カテゴリページのレイアウトの更新は利用できません。
   - `Empty`  — カテゴリページで空のレイアウトを使用します。
   - `1 column`  — カテゴリページで単一列のレイアウトを使用します。
   - `2 columns with left bar`  — カテゴリページの左側にサイドバーがある 2 列のレイアウトを使用します。
   - `2 columns with right bar`  — カテゴリページの右側にサイドバーがある 2 列のレイアウトを使用します。
   - `3 columns`  — カテゴリページの左右にサイドバーがある 3 列のレイアウトを使用します。

   条件 [Page Builder](../page-builder/introduction.md) が有効な場合、追加の全幅オプションを使用できます。 その後、ページビルダーのコンテンツツールを使用して、カテゴリページのレイアウトをデザインできます。

   - `Page -- Full Width`  — を使用します。 _ページ — 全幅_ カテゴリページのレイアウト。
   - `Category -- Full Width` - （推奨） _カテゴリ — 全幅_ カテゴリページのレイアウト。
   - `Product -- Full Width`  — を使用します。 _製品 — 全幅_ カテゴリページのレイアウト。

1. を選択します。 **[!UICONTROL Default Page Layout]** を CMS ページに使用する

   この設定は、CMS ページでデフォルトで使用されるレイアウトを決定します。

   - `No layout updates` - CMS ページではレイアウトの更新は使用できません。
   - `Empty` - CMS ページで空のレイアウトを使用します。
   - `1 column` - CMS ページで単一列レイアウトを使用します。
   - `2 columns with left bar` - CMS ページでは、左側にサイドバーが付いた 2 列のレイアウトを使用します。
   - `2 columns with right bar` - CMS ページでは、右側にサイドバーが付いた 2 列のレイアウトを使用します。
   - `3 columns` - CMS ページでは、左右にサイドバーが付いた 3 列のレイアウトを使用します。

   条件 [Page Builder](../page-builder/introduction.md) が有効な場合、追加の全幅オプションを使用できます。 次に、ページビルダーのコンテンツツールを使用して、CMS ページのレイアウトをデザインできます。

   - `Page -- Full Width` - （推奨） _ページ — 全幅_ CMS ページのレイアウト。
   - `Category - Full Width`  — を使用します。 _カテゴリ — 全幅_ CMS ページのレイアウト。
   - `Product - Full Width`  — を使用します。 _製品 — 全幅_ CMS ページのレイアウト。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 標準ページレイアウト

### 1 列

![図 — 1 列のレイアウト](./assets/layout-1-col-th.png){zoomable=&quot;yes&quot;}

The _[!UICONTROL 1 Column]_レイアウトを使用して、大きな画像や焦点を持つ劇的なホームページを作成できます。 また、ランディングページや、テキスト、画像、ビデオを組み合わせたその他のページにも適しています。

### 左バー付きの 2 列

![図 — 左バー付き 2 列レイアウト](./assets/layout-2-col-lft-bar-th.png){zoomable=&quot;yes&quot;}

The _[!UICONTROL 2 Columns with Left Bar]_レイアウトは、多くの場合、カタログや検索結果ページのレイヤーナビゲーションなど、左側にナビゲーションがあるページに使用されます。 また、左側に追加のナビゲーションやサポートコンテンツのブロックが必要なホームページにも最適です。

### 右バー付きの 2 列

![図 — 右バー付き 2 列レイアウト](./assets/layout-2-col-rt-bar-th.png){zoomable=&quot;yes&quot;}

を使用 _[!UICONTROL 2 Columns with Right Bar]_レイアウトの場合、メインコンテンツ領域は目を引く画像やバナーに十分な大きさになります。 このレイアウトは、右側にサポートコンテンツのブロックがある製品ページでもよく使用されます。

### 3 列

![図 — 3 列レイアウト](./assets/layout-3-col-th.png){zoomable=&quot;yes&quot;}

The _[!UICONTROL 3 Column]_レイアウトには、ページのメインテキストに十分な幅の中央の列があり、各辺には追加のナビゲーション用のスペースと、サポートするコンテンツのブロックが用意されています。

### 空

![図 — 空のレイアウト](./assets/layout-blank-th.png){zoomable=&quot;yes&quot;}

The _[!UICONTROL Empty]_レイアウトを使用して、カスタムのページレイアウトを定義できます。
