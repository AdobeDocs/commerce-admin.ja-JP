---
title: ストアのローカリゼーション
description: ストアまたはストア表示をローカライズする方法について説明します。
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# ストアのローカリゼーション

ストア全体でページにハードコードされているように見えるテキストのほとんどは、表示のロケールを変更することで、すぐに別の言語に変更できます。 ロケールを変更しても、実際には一語一語が翻訳されるわけではなく、ストア全体で使用されるインターフェイステキストを提供する別の翻訳テーブルが参照されるだけです。 変更可能なテキストには、ナビゲーションのタイトル、ラベル、ボタン、次のようなリンクがあります _自分のカート_ および _マイアカウント_. を使用することもできます [インライン翻訳](../configuration-reference/advanced/developer.md) インターフェイスのテキストをタッチアップするツール。

言語パックはの下にあります。 [翻訳とローカライゼーション][1]Commerce Marketplaceの {:target=&quot;_blank&quot;}。 新しい拡張機能が Marketplace に継続的に追加されるので、頻繁に確認してください。

## 手順 1：言語パックをインストールする

言語パック拡張機能をインストールするための標準的な手順に従います。 拡張機能のインストールについて詳しくは、を参照してください [一般的な CLI のインストール][2] が含まれる _拡張機能ガイド_.

## 手順 2：言語のストア表示の作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. クリック **[!UICONTROL Create Store View]**.

1. 新しいストア表示のオプションを設定します。

   - **[!UICONTROL Store]** — ビューの親であるストアを選択します。

   - **[!UICONTROL Name]** — ストア ビューの名前を入力します。 例：ポルトガル語

     ストアのヘッダーでは、名前がに表示されます。 _言語選択_.

   - **[!UICONTROL Code]** - ビューを識別するコードを小文字で入力します。 例： `portuguese`.

   - **[!UICONTROL Status]** — ビューをアクティブにするには、をに設定します。 `Enabled`.

   - **[!UICONTROL Sort Order]** — （オプション）このビューを他のビューとともに一覧表示する順序を決定する番号を入力します。

1. 完了したら、 **[!UICONTROL Save Store View]**.

## 手順 3：ストア表示のロケールの変更

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左上隅にを設定します **[!UICONTROL Store View]** ：設定を適用する特定のビューに移動します。

1. 範囲の切り替えを確認するプロンプトが表示されたら、 **[!UICONTROL OK]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Locale Options]** セクション。

1. をクリア **[!UICONTROL Use Website]** チェックボックスとセット **[!UICONTROL Locale]** を、ビューに割り当てる言語に変更します。

   言語のバリエーションがいくつかある場合は、特定の地域や方言に合ったものを選択してください。

1. 完了したら、 **[!UICONTROL Save Config]**.

   ロケールの言語を変更した後、製品名と説明、カテゴリなど、作成した残りのコンテンツ [CMS](../content-design/page-translate.md) ページおよびブロックは、ストア表示ごとに個別に翻訳する必要があります。

## 製品をローカライズ

ストアが異なる言語で複数のビューを持っている場合、各ストア表示で同じ製品を使用できます。 言語に関係なく、SKU、価格、在庫レベルなど、同じ基本商品情報を使用できます。 次に、各言語で必要に応じて、製品名、説明フィールドおよびメタデータのみを翻訳します。

### 手順 1：製品フィールドの翻訳

1. 日 _Admin_ サイドバー、に移動  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. グリッドで、翻訳する製品を見つけ、編集モードで開きます。

1. 左上隅にを設定します **[!UICONTROL Store View]** をクリックして翻訳を表示し、 **[!UICONTROL OK]** 確認を求めるプロンプトが表示されたら、

1. 編集するフィールドごとに、次の操作を行います。

   - の選択を解除 **[!UICONTROL Use Default Value]** フィールドの右側にあるチェックボックス。

   - 翻訳したテキストをフィールドに貼り付けるか入力します。

   次に示すすべてのテキストフィールドを必ず翻訳してください。 [画像](../catalog/catalog-images-video.md) ラベルと代替テキスト [検索エンジンの最適化](../catalog/product-search-engine-optimization.md) フィールドと任意 [カスタムオプション](../catalog/settings-advanced-custom-options.md) 情報。

1. 完了したら、 **[!UICONTROL Save]**.

### 手順 2：フィールドラベルを翻訳

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. リストで、翻訳する属性を見つけ、編集モードで開きます。

1. 左パネルで、を選択します。 **[!UICONTROL Manage Labels]**.

1. が含まれる _[!UICONTROL Manage Titles]_セクションで、各ストア表示の翻訳済みラベルを入力します。

   ![翻訳済みラベルを入力](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Attribute]**.

### 手順 3：すべてのカテゴリを翻訳

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **カテゴリ**.

1. 左上隅にを設定します **[!UICONTROL Store View]** をクリックして翻訳を表示し、 **[!UICONTROL OK]** 確認を求めるプロンプトが表示されたら、

1. ツリー内で翻訳するカテゴリを探し、編集モードで開きます。

1. の場合 _基本情報_、翻訳 **[!UICONTROL Category Name]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Content]_セクションと翻訳&#x200B;**[!UICONTROL Description]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization Settings]** を選択して、次のフィールドを翻訳してください。

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. の下 _[!UICONTROL Search Engine Optimization Settings]_セクションで、次の手順を実行して翻訳します&#x200B;**[!UICONTROL URL Key]**:

   - をクリア **[!UICONTROL Use Default Value]** フィールドの右側にあるチェックボックス。

   - 翻訳したテキストを入力します。

   - 次のことを確認します **[!UICONTROL Create Permanent Redirect for old URL]** チェックボックスが選択されています。

   ![URL キーを翻訳](./assets/category-translate-url-key.png)

1. 完了したら、 **[!UICONTROL Save Category]**.

1. ストアで使用されているすべてのカテゴリについて、この手順を繰り返します。

### 手順 4：製品属性および属性オプションの翻訳

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 翻訳する属性を選択します。

1. を選択 **[!UICONTROL Manage Labels]** 左側のを設定し、 **[!UICONTROL Managed Titles]** 属性タイトルの翻訳を定義するためのオプション。

1. を選択 **[!UICONTROL Properties]** 左側で、翻訳済み属性オプションを内に入力 **[!UICONTROL Manage Options]** セクション。

   ![オプションを管理](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
