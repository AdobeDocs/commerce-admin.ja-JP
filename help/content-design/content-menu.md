---
title: '[!UICONTROL Content] メニュー'
description: '[!UICONTROL Content] メニューを使用して、ストア内のコンテンツを管理するための複数の機能にアクセスします。'
exl-id: 4e149836-f13c-4240-8700-882f2fc1619a
source-git-commit: c036fffe602593a801f9cf1361fdb44f1f7e1d5f
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# [!UICONTROL Content] メニュー

>[!NOTE]
>
>新しい [[!DNL Media Gallery]](media-gallery.md) が有効になると、「_[!UICONTROL Media]_」セクションが表示され、[!DNL Media Gallery] にアクセスするための単一のオプションが表示されます。**[!UICONTROL Enable Old Media Gallery]**&#x200B;オプションを `No` に設定するには、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]** に移動し、左パネルの **[!UICONTROL Advanced]**/**[!UICONTROL System]** を選択します。

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

![ 管理者に表示される [!UICONTROL Content] メニュー ](./assets/admin-menu-content.png){width="400" zoomable="yes"}

>[!TAB Adobe Commerceas a Cloud Service]

[!BADGE SaaS のみ &#x200B;]{type=Positive url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクトにのみ適用されます（Adobeで管理される SaaS インフラストラクチャ）。"}

![ 管理者に表示される [!UICONTROL Content] メニュー ](./assets/admin-menu-content-accs.png){width="400" zoomable="yes"}

>[!ENDTABS]

## [!UICONTROL Content] メニューの表示

_管理者_ サイドバーで「**[!UICONTROL Content]**」を選択します。

## [!UICONTROL Elements]

- テキスト、画像、ブロック、変数およびウィジェットを使用して [ ページ ](pages.md) を作成します。 ページは、ストアのナビゲーションに組み込んだり、他のページにリンクしたりできます。
- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）ナビゲーションを使用して、ページを [ 階層 ](page-hierarchy.md) に整理します。
- コードを記述せずにコンテンツの [ ブロック ](blocks.md) を作成します。 ブロックには、テキスト、画像、さらにはビデオを含めることができ、ページレイアウトの任意の部分に割り当てることができます。
- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） [ 動的ブロック ](dynamic-blocks.md) を作成して、[ 価格ルール ](../merchandising-promotions/introduction.md#promotions) および [ 顧客セグメント ](../customers/customer-segments.md) のロジックによって駆動されるリッチでインタラクティブなコンテンツを組み込みます。
- 動的データを表示し、ストア内のどこにでもブロック、リンク、インタラクティブ要素を追加できる [ ウィジェット ](widgets.md) を作成します。
- ページビルダーコンテンツから [ テンプレート ](../page-builder/templates.md) を作成し、新しいコンテンツを追加（または古いコンテンツを置き換え）する際の時間と労力を節約します。

>[!NOTE]
>
>このメニューの _[!UICONTROL Banners]_&#x200B;オプションは、2.3.1 で非推奨（廃止予定）となり、現在は削除されています。 その機能はダイナミック ブロックに置き換えられています。

## [!UICONTROL Design] {#design-features}

ストアの視覚的な表示を管理します。

- [ デザイン設定 ](configuration.md) を設定して、[!DNL Commerce] インストールで web サイト、ストア、表示ごとに異なる設定を維持します。

- レイアウトファイル、テンプレートファイル、翻訳ファイル、スキンの集まりである [ テーマ ](themes.md) を使用して、ストアの視覚的な表示を決定します。

- [ スケジュール ](schedule.md) を使用して、シーズンやプロモーションに合わせてテーマの変更を事前に計画します。

## [!UICONTROL Content Staging]

{{ee-feature}}

[ コンテンツのステージング ](content-staging.md) を使用すると、ビジネスチームは、ストアの管理者から直接様々なコンテンツの更新を簡単に作成、プレビュー、スケジュールできます。
