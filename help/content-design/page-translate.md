---
title: コンテンツページの翻訳
description: 特定のストア表示から使用可能な各ページの翻訳済みバージョンを作成する方法を説明します。
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# コンテンツページの翻訳

ストアに異なる [&#x200B; 言語 &#x200B;](../stores-purchase/store-localize.md) の複数のビューがあり、各ビューのロケールを異なる言語に設定した場合、その結果、部分翻訳されたサイトになります。 次に、特定のストア表示から使用可能な各ページの翻訳済みバージョンを作成します。 _[!UICONTROL Manage Pages]_&#x200B;リストの [!UICONTROL Store View] 列には、翻訳されたバージョンのページを持つ各ビューが表示されます。

コンテンツページを翻訳するには、元のページと同じ URL キーを持ち、特定のストア表示に割り当てられている別のページを作成する必要があります。 次に、翻訳されたテキストで特定のビューのページを更新します。 次の例では、スペイン語店表示用の _会社概要_ ページの翻訳版を作成する方法を示します。

## 手順 1：翻訳するページの URL キーをコピーする

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Pages]**&#x200B;に移動します。

1. グリッドで、翻訳するページを見つけ、_編集_ モードで開きます。

1. 「![&#x200B; 拡張セレクター &#x200B;](../assets/icon-display-expand.png)**[!UICONTROL Search Engine Optimization]** セクションを展開して、**[!UICONTROL URL Key]** をクリップボードにコピーします。

1. _[!UICONTROL Pages]_&#x200B;のグリッドに戻るには、上部のボタン バーの [**[!UICONTROL Back]**] をクリックします。

## 手順 2：翻訳済みコンテンツのページを追加

1. 「**[!UICONTROL Add New Page]**」をクリックします。

1. 翻訳済み **[!UICONTROL Page Title]** を入力します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) 「**[!UICONTROL Content]**」セクションを展開し、ページの翻訳済みテキストを入力します。

1. **[!UICONTROL Search Engine Optimization]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - 元のページからコピーした **[!UICONTROL URL Key]** を貼り付けます。

   - **[!UICONTROL Meta Title]**、**[!UICONTROL Meta Keywords]**、**[!UICONTROL Meta Description]** の翻訳済みテキストを入力します。

1. ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) 「**[!UICONTROL Page in Websites]**」セクションを展開し、ページを使用可能にするストア表示に **[!UICONTROL Store View]** を設定します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) 「**[!UICONTROL Design]**」セクションを展開し、ページの列 **[!UICONTROL Layout]** を設定します。

1. 「**[!UICONTROL Save]**」をクリックします。

1. プロンプトが表示されたら、無効な [&#x200B; キャッシュ &#x200B;](../systems/cache-management.md) を更新します。

## 手順 3：翻訳を検証

翻訳を確認するには、ストアフロントに移動し、言語選択を使用してストア表示を変更します。

会社のフッターリンク [&#x200B; ブロック &#x200B;](block-add.md)、[&#x200B; ようこそメッセージ &#x200B;](../getting-started/storefront-branding.md#change-the-welcome-message)、[&#x200B; 製品情報 &#x200B;](../stores-purchase/store-localize.md#localize-products) など、翻訳が必要な要素がページ上にまだ存在しています。
