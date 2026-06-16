---
title: '[!UICONTROL Content] メニュー'
description: '[!UICONTROL Content] メニューを使用して、ストア内のコンテンツを管理するための複数の機能にアクセスします。'
exl-id: 4e149836-f13c-4240-8700-882f2fc1619a
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/UTh5IKGTXZUcSXGQvP7rHtja8EnEELc75EPpvPvSD3E
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# [!UICONTROL Content] メニュー

>[!NOTE]
>
>新しい[[!DNL Media Gallery]](media-gallery.md)が有効になると、_[!UICONTROL Media]_&#x200B;セクションが表示され、1つのオプションで[!DNL Media Gallery]にアクセスできます。**[!UICONTROL Enable Old Media Gallery]**&#x200B;オプションを`No`に設定するには、**[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**&#x200B;に移動し、左側のパネルで&#x200B;**[!UICONTROL Advanced]** > **[!UICONTROL System]**&#x200B;を選択します。

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

![管理者](./assets/admin-menu-content.png){width="400" zoomable="yes"}に表示される[!UICONTROL Content] メニュー

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクト（Adobeが管理するSaaS インフラストラクチャ）にのみ適用されます。"}

![管理者](./assets/admin-menu-content-accs.png){width="400" zoomable="yes"}に表示される[!UICONTROL Content] メニュー

>[!ENDTABS]

## [!UICONTROL Content] メニューの表示

_管理者_ サイドバーで、**[!UICONTROL Content]**&#x200B;を選択します。

## [!UICONTROL Elements]

- テキスト、画像、ブロック、変数、ウィジェットを使用して[&#x200B; ページ &#x200B;](pages.md)を作成します。 ページは、ストアのナビゲーションに組み込んだり、他のページにリンクしたりできます。
- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）ナビゲーション機能を使用して、ページを[階層](page-hierarchy.md)に整理します。
- コードを記述せずに、コンテンツの[&#x200B; ブロック &#x200B;](blocks.md)を作成します。 ブロックにはテキスト、画像、動画などを含め、ページレイアウトの任意の部分に割り当てることができます。
- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）動的ブロック [を作成して](dynamic-blocks.md) リッチでインタラクティブなコンテンツを組み込みます。このコンテンツは、[価格ルール &#x200B;](../merchandising-promotions/introduction.md#promotions)および[顧客セグメント &#x200B;](../customers/customer-segments.md)のロジックに基づいています。
- 動的なデータを表示する[&#x200B; ウィジェット &#x200B;](widgets.md)を作成し、ストア内の任意の場所にブロック、リンク、インタラクティブ要素を追加します。
- ページビルダーコンテンツから[&#x200B; テンプレート &#x200B;](../page-builder/templates.md)を作成し、新しいコンテンツを追加（または古いコンテンツを置き換える）する際の時間と労力を節約します。

>[!NOTE]
>
>このメニューの&#x200B;_[!UICONTROL Banners]_&#x200B;オプションは2.3.1で廃止され、削除されました。 その機能はダイナミックブロックに置き換えられます。

## [!UICONTROL Design] {#design-features}

ストアのビジュアルプレゼンテーションを管理します。

- [&#x200B; デザイン設定](configuration.md)を設定して、[!DNL Commerce] インストールでweb サイト、ストア、ビューごとに異なる設定を管理します。

- レイアウトファイル、テンプレートファイル、翻訳ファイル、スキンのコレクションである[&#x200B; テーマ &#x200B;](themes.md)を使用して、ストアの視覚的なプレゼンテーションを決定します。

- [&#x200B; スケジュール &#x200B;](schedule.md)を使用して、シーズンまたはプロモーションのテーマの変更を事前に計画します。

## [!UICONTROL Content Staging]

{{ee-feature}}

[&#x200B; コンテンツのステージング &#x200B;](content-staging.md)を使用すると、ビジネス チームは、ストアの管理者から直接、さまざまなコンテンツの更新を簡単に作成、プレビュー、スケジュールできます。
