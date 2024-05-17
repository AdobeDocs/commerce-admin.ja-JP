---
title: 新製品リストウィジェット
description: 新製品リストウィジェットを使用して、最近追加された製品のリストを表示する方法を説明します。
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# 新製品リストウィジェット

新製品のリストは動的コンテンツの例であり、製品カタログから取得したライブデータで構成されています。 デフォルトでは、 _新製品_ リストには、最近追加された製品の最初の 8 つが含まれます。 ただし、指定した日付範囲内の製品のみを含めるように設定することもできます。

![ストアフロントのホームページに表示される新製品リスト](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## 手順 1：各製品を新規製品として設定

![Magento Open Source](../assets/open-source.svg) この手順は、Magento Open Sourceにのみ適用されます。

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce ストアについては、を参照してください。 [更新のスケジュール設定](content-staging-scheduled-update.md) その後、このページの手順 2 に進みます。

_[!UICONTROL Set Product as New]_日付範囲の設定は、スケジュールされた更新でのみ設定できます。

製品を新規設定すると、製品が「」に追加されます _新製品_ リスト。 リストに含めたくない場合は、いつでも設定を戻すことができます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 機能させる各製品を見つけて、編集モードで開きます。

1. の場合 **[!UICONTROL Set Product as New]**&#x200B;で、製品を新製品として設定するかどうかを切り替えます。

   ![製品を新規として設定](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

1. ページキャッシュを再インデックス化して更新するように求めるプロンプトが表示されたら、ページ上部のリンクをクリックし、指示に従います。

## 手順 2：ウィジェットの作成

新製品リストの内容とストア内での配置を決定するコードは、ウィジェットツールによって生成されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Widget]**.

1. が含まれる _[!UICONTROL Settings]_セクションで、次の操作を行います。

   - を設定 **[!UICONTROL Type]** 対象： `Catalog New Products List`.

   - を選択します。 **[!UICONTROL Design Theme]** それは店で使われます。

1. クリック **[!UICONTROL Continue]**.

   ![新しい製品リストウィジェットの設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. が含まれる _[!UICONTROL Storefront Properties]_セクションで、次の操作を行います。

   - の場合 **[!UICONTROL Widget Title]**、ウィジェットのわかりやすいタイトルを入力します。 （このタイトルは、 _Admin_.）

   - の場合 **[!UICONTROL Assign to Store Views]**&#x200B;で、ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択することも、 `All Store Views`. 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]**&#x200B;を入力し、この項目がページの同じ部分に他のユーザーと表示される順序を決定します。 （`0` =最初、 `1` =秒、 `3` = 3 番目、など）。

   ![レイアウトの更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## 手順 3：場所の選択

1. が含まれる _[!UICONTROL Layout Updates]_セクションで、をクリック&#x200B;**[!UICONTROL Add Layout Update]**.

1. を設定 **[!UICONTROL Display On]** 対象： `Specified Page.`

1. を設定 **[!UICONTROL Page]** 対象： `CMS Home Page`.

1. を設定 **[!UICONTROL Block Reference]** 対象： `Main Content Area`.

1. を設定 **[!UICONTROL Template]** を次のいずれかに変更します。

   - `New Product List Template`
   - `New Products Grid Template`

     ![レイアウトの更新](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save and Continue Edit]**.

   現時点では、メッセージを無視してキャッシュを更新できます。

## 手順 4：リストの設定

1. 左パネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. を設定 **[!UICONTROL Display Products]** を次のいずれかに変更します。

   - `All Products`  – 最後に追加された製品から順に製品を一覧表示します。
   - `New Products`  – として識別された製品のみを一覧表示します _新規_. 製品は、で指定された日付範囲で新規と見なされます。 _[!UICONTROL Set Product As New From/To]_. 新しい製品が定義されずに日付範囲が期限切れになった場合、リストは空になります。

1. 複数ページを含むリストのナビゲーション制御を提供するには、次のように設定します **[!UICONTROL Display Page Control]** 対象： `Yes`.

   の場合 **[!UICONTROL Number of Products per Page]**&#x200B;を入力し、各ページに表示する製品の数を入力します。

1. を **[!UICONTROL Number of Products to Display]** リストに含める新製品の数を指定します。

   デフォルト設定は `10`.

1. の場合 **[!UICONTROL Cache Lifetime (Seconds)]**、新製品のリストを更新する頻度を選択します。

   デフォルトでは、キャッシュは 86,400 秒（24 時間）に設定されています。

   ![ウィジェットオプション](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

1. キャッシュを更新するように求めるプロンプトが表示されたら、ページ上部のメッセージに記載されているリンクをクリックし、指示に従います。

## 手順 5：作業のプレビュー

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. グリッドでページを見つけます。見つける _新製品_ リストが表示されたら、 **[!UICONTROL Preview]** 内のリンク _[!UICONTROL Action]_列。
