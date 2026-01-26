---
title: ストアのローカリゼーション
description: ストアまたはストア表示をローカライズする方法について説明します。
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# ストアのローカリゼーション

ストア全体でページにハードコードされているように見えるテキストのほとんどは、表示のロケールを変更することで、すぐに別の言語に変更できます。 ロケールを変更しても、実際には一語一語が翻訳されるわけではなく、ストア全体で使用されるインターフェイステキストを提供する別の翻訳テーブルが参照されるだけです。 変更可能なテキストには、ナビゲーションタイトル、ラベル、ボタン、およびリンク（_買い物かご_ や _マイアカウント_ など）が含まれます。 [ インライン翻訳 ](../configuration-reference/advanced/developer.md) ツールを使用して、インターフェイス内のテキストにタッチ アップすることもできます。

言語パックは、Commerce Marketplaceの [ 翻訳とローカライゼーション ](https://marketplace.magento.com/extensions/content-customizations/translations-localization.html){:target="_blank"} にあります。 新しい拡張機能が Marketplace に継続的に追加されるので、頻繁に確認してください。

## 手順 1：言語パックをインストールする

言語パック拡張機能をインストールするための標準的な手順に従います。 拡張機能のインストールについて詳しくは、『 [ 拡張機能ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) の _一般的な CLI のインストール_ を参照してください。

## 手順 2：言語のストア表示の作成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL All Stores]**に移動します。

1. 「**[!UICONTROL Create Store View]**」をクリックします。

1. 新しいストア表示のオプションを設定します。

   - 「**[!UICONTROL Store]**」 – ビューの親であるストアを選択します。

   - 「**[!UICONTROL Name]**」 – ストア表示の名前を入力します。 例：ポルトガル語

     ストアのヘッダーで、名前が _言語選択_ に表示されます。

   - **[!UICONTROL Code]** - ビューを識別するコードを小文字で入力します。 例：`portuguese`。

   - **[!UICONTROL Status]** - ビューをアクティブにするには、`Enabled` に設定します。

   - 「**[!UICONTROL Sort Order]**」 – （オプション）このビューが他のビューとともにリストされる順序を決定する番号を入力します。

1. 完了したら、「**[!UICONTROL Save Store View]**」をクリックします。

## 手順 3：ストア表示のロケールの変更

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. **[!UICONTROL Scope]** ドロップダウンで、設定するストア表示を選択し、プロンプトが表示されたら「**[!UICONTROL OK]**」をクリックします。

1. *[!UICONTROL General]* 設定ページで、「拡張セレクター ![ の「](../assets/icon-display-expand.png)」セクション **[!UICONTROL Locale Options]** 展開します。

1. 「**[!UICONTROL Use Website]**」チェックボックスをオフにして、ビューに割り当てる言語に **[!UICONTROL Locale]** を設定します。

   言語のバリエーションがいくつかある場合は、特定の地域や方言に合ったものを選択してください。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

   ロケールの言語を変更した後、商品名と説明、カテゴリ、[CMS](../content-design/page-translate.md) ページ、ブロックなど、作成した残りのコンテンツを、ストアビューごとに個別に翻訳する必要があります。

## 製品をローカライズ

ストアが異なる言語で複数のビューを持っている場合、各ストア表示で同じ製品を使用できます。 言語に関係なく、SKU、価格、在庫レベルなど、同じ基本商品情報を使用できます。 次に、各言語で必要に応じて、製品名、説明フィールドおよびメタデータのみを翻訳します。

### 手順 1：製品フィールドの翻訳

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. グリッドで、翻訳する製品を見つけ、編集モードで開きます。

1. 左上隅で翻訳のビューに **[!UICONTROL Store View]** を設定し、確認を求められたら「**[!UICONTROL OK]**」をクリックします。

1. 編集するフィールドごとに、次の操作を行います。

   - フィールドの右側にある「**[!UICONTROL Use Default Value]**」チェックボックスの選択を解除します。

   - 翻訳したテキストをフィールドに貼り付けるか入力します。

   [ 画像 ](../catalog/catalog-images-video.md) ラベルや代替テキスト、[ 検索エンジン最適化 ](../catalog/product-search-engine-optimization.md) フィールドや [ カスタムオプション ](../catalog/settings-advanced-custom-options.md) 情報など、すべてのテキストフィールドが必ず翻訳されるようにしてください。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

### 手順 2：フィールドラベルを翻訳

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**に移動します。

1. リストで、翻訳する属性を見つけ、編集モードで開きます。

1. 左側のパネルで「**[!UICONTROL Manage Labels]**」を選択します。

1. 「_[!UICONTROL Manage Titles]_」セクションで、各ストアビューの翻訳済みラベルを入力します。

   ![ 翻訳済みラベルを入力 ](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。

### 手順 3：すべてのカテゴリを翻訳

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**カテゴリ** に移動します。

1. 左上隅で **[!UICONTROL Store View]** を翻訳のビューに設定し、確認を求められたら「**[!UICONTROL OK]**」をクリックします。

1. ツリー内で翻訳するカテゴリを探し、編集モードで開きます。

1. _基本情報_ については、**[!UICONTROL Category Name]** を翻訳してください。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png) 「_[!UICONTROL Content]_」セクションを展開し、「**[!UICONTROL Description]**を翻訳」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png) 「**[!UICONTROL Search Engine Optimization Settings]**」セクションを展開し、次のフィールドを翻訳します。

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. _[!UICONTROL Search Engine Optimization Settings]_セクションで、次の操作を行って&#x200B;**[!UICONTROL URL Key]**を翻訳します。

   - フィールドの右側にある「**[!UICONTROL Use Default Value]**」チェックボックスをオフにします。

   - 翻訳したテキストを入力します。

   - 「**[!UICONTROL Create Permanent Redirect for old URL]**」チェックボックスが選択されていることを確認します。

   ![URL キーを翻訳 ](./assets/category-translate-url-key.png)

1. 完了したら、「**[!UICONTROL Save Category]**」をクリックします。

1. ストアで使用されているすべてのカテゴリについて、この手順を繰り返します。

### 手順 4：製品属性および属性オプションの翻訳

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**に移動します。

1. 翻訳する属性を選択します。

1. 左側の **[!UICONTROL Manage Labels]** を選択し、**[!UICONTROL Managed Titles]** のオプションを設定して、属性タイトルの翻訳を定義します。

1. 左側の **[!UICONTROL Properties]** を選択し、「**[!UICONTROL Manage Options]**」セクションに翻訳済み属性のオプションを入力します。

   ![ 管理オプション ](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。
