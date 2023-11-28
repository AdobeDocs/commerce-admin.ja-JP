---
title: ストアのローカライゼーション
description: ストア表示またはストア表示をローカライズする方法を説明します。
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# ストアのローカライゼーション

ストア全体でページ上でハードコードされているように見えるテキストのほとんどは、ビューのロケールを変更することで、すぐに別の言語に変更できます。 ロケールを変更しても、実際には word-for-word というテキストが翻訳されるわけではなく、単にストア全体で使用されるインターフェイステキストを提供する別の翻訳テーブルを参照するだけです。 変更できるテキストには、ナビゲーションのタイトル、ラベル、ボタンおよびリンク ( _買い物かご_ および _マイアカウント_. また、 [インライン翻訳](../configuration-reference/advanced/developer.md) ツールを使用して、インターフェイス内のテキストにタッチアップできます。

言語パックは、の下にあります。 [翻訳とローカライゼーション][1]Commerce Marketplaceの {:target=&quot;_blank&quot;}。 新しい拡張機能は Marketplace に継続的に追加されるので、頻繁にご確認ください。

## 手順 1：言語パックのインストール

言語パック拡張機能のインストールに関する標準手順に従います。 拡張機能のインストールについて詳しくは、 [一般的な CLI のインストール][2] （内） _拡張機能ガイド_.

## 手順 2：言語のストア表示を作成する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. クリック **[!UICONTROL Create Store View]**.

1. 新しいストア表示のオプションを設定します。

   - **[!UICONTROL Store]**  — ビューの親であるストアを選択します。

   - **[!UICONTROL Name]**  — ストアビューの名前を入力します。 例：ポルトガル語。

     ストアのヘッダーで、名前が _言語選択_.

   - **[!UICONTROL Code]**  — ビューを識別するコードを小文字で入力します。 例： `portuguese`.

   - **[!UICONTROL Status]**  — ビューをアクティブにするには、をに設定します。 `Enabled`.

   - **[!UICONTROL Sort Order]** - （オプション）このビューが他のビューと共に表示される順序を決定する数値を入力します。

1. 完了したら、「 **[!UICONTROL Save Store View]**.

## 手順 3：ストア表示のロケールを変更する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左上隅で、 **[!UICONTROL Store View]** 設定を適用する特定のビューに追加します。

1. 範囲の切り替えを確認するメッセージが表示されたら、 **[!UICONTROL OK]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Locale Options]** 」セクションに入力します。

1. 次をクリア： **[!UICONTROL Use Website]** チェックボックスとセット **[!UICONTROL Locale]** をビューに割り当てる言語に設定します。

   使用可能な言語に複数のバリエーションがある場合は、特定の地域または言語用の言語を選択するようにしてください。

1. 完了したら、「 **[!UICONTROL Save Config]**.

   ロケールの言語を変更した後、作成した残りのコンテンツ ( 製品名、説明、カテゴリ、 [CMS](../content-design/page-translate.md) ページとブロックは、ストアビューごとに個別に翻訳する必要があります。

## 製品のローカライズ

ストアに異なる言語の複数のビューがある場合、各ストアビューで同じ製品を使用できます。 言語に関係なく、SKU、価格、在庫レベルなど、同じ基本的な製品情報を使用できます。 その後、各言語で必要に応じて、製品名、説明フィールド、メタデータのみを翻訳します。

### 手順 1：製品フィールドの翻訳

1. 次の日： _管理者_ サイドバー、移動  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. グリッドで、翻訳する製品を探し、編集モードで開きます。

1. 左上隅で、 **[!UICONTROL Store View]** 翻訳のビューに移動し、 **[!UICONTROL OK]** 確認するプロンプトが表示されたら、

1. 編集する各フィールドに対して、次の操作を実行します。

   - 選択を解除すると、 **[!UICONTROL Use Default Value]** チェックボックスを使用して、フィールドの右側に表示されます。

   - フィールドに翻訳済みのテキストを貼り付けるか、入力します。

   すべてのテキストフィールド ( [画像](../catalog/catalog-images-video.md) ラベルと代替テキスト [検索エンジンの最適化](../catalog/product-search-engine-optimization.md) フィールドおよび任意の [カスタムオプション](../catalog/settings-advanced-custom-options.md) 情報。

1. 完了したら、「 **[!UICONTROL Save]**.

### 手順 2：フィールドラベルを翻訳する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. リストで、翻訳する属性を見つけ、編集モードで開きます。

1. 左側のパネルで、を選択します。 **[!UICONTROL Manage Labels]**.

1. Adobe Analytics の _[!UICONTROL Manage Titles]_「 」セクションで、各ストアビューの翻訳済みラベルを入力します。

   ![翻訳済みラベルを入力](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Attribute]**.

### 手順 3：すべてのカテゴリを翻訳する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **カテゴリ**.

1. 左上隅で、 **[!UICONTROL Store View]** 翻訳のビューに移動し、 **[!UICONTROL OK]** 確認するプロンプトが表示されたら、

1. ツリーで、翻訳するカテゴリを見つけ、編集モードで開きます。

1. の場合 _基本情報_, translate **[!UICONTROL Category Name]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Content]_セクションと翻訳&#x200B;**[!UICONTROL Description]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization Settings]** セクションで次のフィールドを翻訳します。

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. の下 _[!UICONTROL Search Engine Optimization Settings]_セクションで、以下の操作を行って、**[!UICONTROL URL Key]**:

   - 次をクリア： **[!UICONTROL Use Default Value]** チェックボックスを使用して、フィールドの右側に表示されます。

   - 翻訳されたテキストを入力します。

   - 次を確認します。 **[!UICONTROL Create Permanent Redirect for old URL]** チェックボックスがオンになっている。

   ![URL キーを翻訳](./assets/category-translate-url-key.png)

1. 完了したら、「 **[!UICONTROL Save Category]**.

1. ストアで使用されるすべてのカテゴリに対して、この手順を繰り返します。

### 手順 4：製品属性と属性のオプションを翻訳する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 翻訳する属性を選択します。

1. 選択 **[!UICONTROL Manage Labels]** 左側で、 **[!UICONTROL Managed Titles]** 属性タイトルの翻訳を定義するオプションです。

1. 選択 **[!UICONTROL Properties]** 左側に、翻訳済みの属性オプションを **[!UICONTROL Manage Options]** 」セクションに入力します。

   ![オプションを管理](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
