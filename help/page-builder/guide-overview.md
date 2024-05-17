---
title: '[!DNL Page Builder] ユーザーガイド'
description: ～に関する包括的な情報 [!DNL Page Builder] （Adobe Commerce管理者とMagento Open Source管理者の場合）。
seo-title: Adobe Commerce [!DNL Page Builder] User Guide
seo-description: Describes how to use the [!DNL Page Builder] module in Adobe Commerce or Magento Open Source.
exl-id: 983ef3a8-b803-40ff-a9f5-07eb895df31c
source-git-commit: fa4030d391fc9a3b21cf8fb6f681df9e9165157d
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# [!DNL Page Builder] ユーザーガイド

このガイドは、Adobe CommerceとMagento Open Sourceの管理者を対象としています。 以下に関する詳細情報が提供されます [!DNL Page Builder] 機能（基本的なコンテンツコンポーネントを構築するための 3 つのパートのチュートリアルを含む）。 ここでは、コア部分の基本的な理解を前提としています [!DNL Commerce] 設定と機能。

[!DNL Page Builder] には、ストア管理者用の次の 2 つの領域があります。

- 管理者：この領域を使用して設定 UI にアクセスし、ページビルダーツールを操作します。
- コマンドラインインターフェイス：このツールを使用して、インストールタスクとバックエンド設定タスクを実行します。

このガイドでは、次の内容について説明します。

| 件名 | 説明 |
| ------- | ----------- |
| [はじめに](introduction.md) | について [!DNL Page Builder]? また、Adobe CommerceとMagento Open Sourceサイトのコンテンツ制作をどのように強化するのでしょうか。 |
| [リリースノート](release-notes.md) | 各で提供されるアップデートを確認します [!DNL Page Builder] モジュールリリース。 |
| [設定](setup.md) | デフォルト設定を更新するには、デフォルトのページレイアウトを変更し、さらに詳細を有効にします [!DNL Page Builder] 機能。 を統合することもできます [!DNL Google Maps] ：ページに場所のコンテンツを組み込みます。 |
| [ワークスペース](workspace.md) | のコンポーネントをレビューする [!DNL Page Builder] ワークスペースと、それらを使用してストアの魅力的なコンテンツを作成する方法。 |
| ガイド | を使い始めたばかりの場合 [!DNL Page Builder]チュートリアルの演習を完了することで、すばやく作業を開始できます。<br>[1 - サンプルページ](1-simple-page.md)<br>[2 – 再利用可能なコンテンツブロック](2-blocks.md)<br>[3 – 製品リストのカタログページ](3-catalog-content.md) |
| [ワークスペース](workspace.md) | で利用できるツールを確認する [!DNL Page Builder] 基本ページ、製品およびカタログのページ、ブロック、ダイナミック ブロックを作成する場合のワークスペース。 |
| レイアウト | を参照 _レイアウト_ の節 [!DNL Page Builder] パネルと、これらのツールを使用してレイアウトコンポーネントをに追加する方法 [!DNL Page Builder] ステージ： <br>[行](row.md)<br>[列](column.md)<br>[タブ](tabs.md) |
| 要素 | を参照 _要素_ の節 [!DNL Page Builder] パネルと、これらのツールを使用して上のレイアウトコンテナに基本要素を追加する方法 [!DNL Page Builder] ステージ： <br>[text](text.md)<br>[見出し](heading.md)<br>[ボタン](buttons.md)<br>[デバイダ](divider.md)<br>[HTMLコード](html-code.md) |
| メディア | を参照 _メディア_ の節 [!DNL Page Builder] パネルと、これらのツールを使用して上の任意のレイアウトコンテナにメディア項目を追加する方法 [!DNL Page Builder] ステージ： <br>[画像](image.md)<br>[ビデオ](video.md)<br>[バナー](banner.md)<br>[スライダー](slider.md)<br>[[!DNL Google Maps]](map.md) |
| コンテンツを追加 | を参照 _コンテンツを追加_ の節 [!DNL Page Builder] パネル、およびコンテンツコンポーネントをに追加する方法 [!DNL Page Builder] ステージ： <br>[ブロック](block.md)<br>[動的ブロック](dynamic-block.md)<br>[製品](products.md)<br>[製品のRecommendations](recommendations.md) （Adobe Commerceのみ） |
| [テンプレート](templates.md) | 既存のものを保存 [!DNL Page Builder] コンテンツをテンプレートとして作成し、そのテンプレートを別の領域に適用して、コンテンツをすばやく一貫して作成できるようにします。 |

{style="table-layout:auto"}

Adobe CommerceとMagento Open Sourceのコア機能については説明しません。

## 追加ドキュメント

{{docs-links}}

## [!DNL Page Builder] 開発者情報

[!DNL Page Builder] はAdobe Commerce 2.4.x およびMagento Open Source 2.4.3 以降と共にインストールされ、すべての機能がデフォルトで有効になっています。 モジュールリリースに含まれる変更点について詳しくは、次を参照してください [[!DNL Page Builder] リリースノート](release-notes.md). この [[!DNL Page Builder] 開発者ガイド](https://developer.adobe.com/commerce/frontend-core/page-builder/) モジュールのアーキテクチャとカスタマイズの詳細を説明します。

## リソースのトラブルシューティング

トラブルシューティングのヘルプ [!DNL Page Builder] 問題については、次を参照してください [!DNL Commerce] サポートナレッジベース記事：

- [DotDigital の場合にページが空になる [!DNL Page Builder] フォームを保存しました](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/magento-2.4.1-empty-page-when-dotdigital-page-builder-form-saved.html)
- [[!DNL Page Builder] メディアギャラリーを読み込まない](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-12/mdva-32133-magento-patch-page-builder-doesn-t-load-media-gallery.html)
- [[!DNL Page Builder] プレビュー分岐の製品価格はサイト間で異なります](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-16/mdva-33453-page-builder-preview-breaks-product-price-differs-across-sites.html)
- [用語ページを保存できません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-19/mdva-33614-magento-patch-can-t-save-terms-page.html)
