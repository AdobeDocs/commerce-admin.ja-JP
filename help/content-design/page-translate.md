---
title: コンテンツページの翻訳
description: 特定のストアビューから使用できる各ページの翻訳版を作成する方法を説明します。
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/9jox-v5fCEhPsaex70yQod--qH-Xnp9dkgmuxJGTZd0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 368
ht-degree: 0%

---

# コンテンツページの翻訳

ストアに異なる[言語](../stores-purchase/store-localize.md)の複数のビューがあり、各ビューのロケールを異なる言語に設定した場合、結果は部分的に翻訳されたサイトになります。 次の手順では、各ページの翻訳版を作成し、特定のストアビューで使用できるようにします。 _[!UICONTROL Manage Pages]_&#x200B;リストの[!UICONTROL Store View]列には、ページの翻訳バージョンを持つ各ビューが表示されます。

コンテンツページを翻訳するには、元のURL キーと同じURL キーを持つが、特定のストアビューに割り当てられている別のページを作成する必要があります。 次に、翻訳されたテキストを使用して、特定のビューのページを更新します。 次の例は、スペインのストアビュー用に&#x200B;_About Us_ ページの翻訳版を作成する方法を示しています。

## 手順1：翻訳するページのURL キーをコピーする

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**&#x200B;に移動します。

1. グリッドで、翻訳するページを見つけ、_編集_ モードで開きます。

1. **[!UICONTROL Search Engine Optimization]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、**[!UICONTROL URL Key]**&#x200B;をクリップボードにコピーします。

1. _[!UICONTROL Pages]_&#x200B;グリッドに戻るには、上部のボタンバーの&#x200B;**[!UICONTROL Back]**&#x200B;をクリックします。

## 手順2：翻訳されたコンテンツのページを追加する

1. **[!UICONTROL Add New Page]**&#x200B;をクリックします。

1. 翻訳済み&#x200B;**[!UICONTROL Page Title]**&#x200B;を入力します。

1. **[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、ページの翻訳テキストを完成させます。

1. **[!UICONTROL Search Engine Optimization]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - 元のページからコピーした&#x200B;**[!UICONTROL URL Key]**&#x200B;を貼り付けます。

   - **[!UICONTROL Meta Title]**、**[!UICONTROL Meta Keywords]**、**[!UICONTROL Meta Description]**&#x200B;の翻訳済みテキストを入力します。

1. **[!UICONTROL Page in Websites]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、**[!UICONTROL Store View]**&#x200B;をページが使用可能なストアビューに設定します。

1. **[!UICONTROL Design]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、ページの列&#x200B;**[!UICONTROL Layout]**&#x200B;を設定します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. プロンプトが表示されたら、無効な[&#x200B; キャッシュ &#x200B;](../systems/cache-management.md)を更新します。

## 手順3：翻訳の確認

翻訳を確認するには、ストアフロントに移動し、言語選択ツールを使用してストアビューを変更します。

会社のフッターリンク [&#x200B; ブロック &#x200B;](block-add.md)、[&#x200B; ウェルカムメッセージ &#x200B;](../getting-started/storefront-branding.md#change-the-welcome-message)、[製品情報](../stores-purchase/store-localize.md#localize-products)など、翻訳する必要がある要素がページ上にまだ存在することに注意してください。
