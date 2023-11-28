---
title: '[!DNL Page Builder] ユーザーガイド'
description: に関する包括的な情報 [!DNL Page Builder] (Adobe CommerceおよびMagento Open Source管理者向け )
seo-title: Adobe Commerce [!DNL Page Builder] User Guide
seo-description: Describes how to use the [!DNL Page Builder] module in Adobe Commerce or Magento Open Source.
exl-id: 983ef3a8-b803-40ff-a9f5-07eb895df31c
source-git-commit: fa4030d391fc9a3b21cf8fb6f681df9e9165157d
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# [!DNL Page Builder] ユーザーガイド

このガイドは、Adobe CommerceとMagento Open Sourceの管理者を対象としています。 以下に関する詳細な情報が記載されています。 [!DNL Page Builder] 基本的なコンテンツコンポーネントを構築するための 3 つのパートから成るチュートリアルを含む機能 コアに関する基本的な理解を前提としています。 [!DNL Commerce] 設定、機能に関する情報です。

[!DNL Page Builder] には、ストア管理者向けの次の 2 つの領域があります。

- 管理者：この領域を使用して設定 UI にアクセスし、ページビルダーツールを操作します。
- コマンドラインインターフェイス：このツールを使用して、インストールおよびバックエンドの設定タスクを実行します。

このガイドでは、以下について説明します。

| 件名 | 説明 |
| ------- | ----------- |
| [はじめに](introduction.md) | 説明 [!DNL Page Builder]? また、Adobe CommerceやMagento Open Sourceサイトのコンテンツ作成をどのように強化しますか。 |
| [リリースノート](release-notes.md) | 各ページで提供された更新を確認します [!DNL Page Builder] モジュールのリリース。 |
| [設定](setup.md) | デフォルト設定を更新するには、デフォルトのページレイアウトを変更し、より詳細な設定を有効にします [!DNL Page Builder] 機能。 また、 [!DNL Google Maps] を使用して、ページに場所のコンテンツを組み込みます。 |
| [Workspace](workspace.md) | のコンポーネントを確認する [!DNL Page Builder] ワークスペースと、ストアに魅力的なコンテンツを作成する方法を説明します。 |
| 順を追う | を使い始めたばかりの場合は、 [!DNL Page Builder]では、チュートリアルの演習を完了することで、すばやく習得できます。<br>[1 — サンプルページ](1-simple-page.md)<br>[2 — 再利用可能なコンテンツブロック](2-blocks.md)<br>[3 — 商品リストのカタログページ](3-catalog-content.md) |
| [Workspace](workspace.md) | で使用できるツールの詳細 [!DNL Page Builder] workspace を使用して、基本ページ、商品ページ、カタログページ、ブロック、動的ブロックを作成する場合。 |
| レイアウト | 関連トピック _レイアウト_ のセクション [!DNL Page Builder] パネルおよびこれらのツールを使用してレイアウトコンポーネントを [!DNL Page Builder] ステージ： <br>[行](row.md)<br>[列](column.md)<br>[タブ](tabs.md) |
| 要素 | 関連トピック _要素_ のセクション [!DNL Page Builder] パネルおよびこれらのツールを使用して、基本要素をレイアウトコンテナ上の任意のレイアウトコンテナに追加する方法を説明します。 [!DNL Page Builder] ステージ： <br>[テキスト](text.md)<br>[見出し](heading.md)<br>[ボタン](buttons.md)<br>[配当者](divider.md)<br>[HTMLコード](html-code.md) |
| メディア | 関連トピック _メディア_ のセクション [!DNL Page Builder] パネルおよびこれらのツールを使用して、メディア項目をレイアウトコンテナ上に追加する方法を説明します。 [!DNL Page Builder] ステージ： <br>[画像](image.md)<br>[ビデオ](video.md)<br>[バナー](banner.md)<br>[スライダ](slider.md)<br>[[!DNL Google Maps]](map.md) |
| コンテンツを追加 | 関連トピック _コンテンツを追加_ のセクション [!DNL Page Builder] パネル、およびコンテンツコンポーネントを [!DNL Page Builder] ステージ： <br>[ブロック](block.md)<br>[ダイナミックブロック](dynamic-block.md)<br>[製品](products.md)<br>[製品Recommendations](recommendations.md) (Adobe Commerceのみ ) |
| [テンプレート](templates.md) | 既存の [!DNL Page Builder] テンプレートとしてコンテンツを作成し、そのテンプレートを別の領域に適用して、コンテンツをすばやく一貫性のあるコンテンツを作成します。 |

{style="table-layout:auto"}

Adobe CommerceとMagento Open Sourceの主な機能は取り上げていません。

## その他のドキュメント

{{docs-links}}

## [!DNL Page Builder] 開発者情報

[!DNL Page Builder] は、Adobe Commerce 2.4.x およびMagento Open Source2.4.3 以降でインストールされ、すべての機能がデフォルトで有効になっています。 モジュールリリースに含まれる変更点については、 [[!DNL Page Builder] リリースノート](release-notes.md). The [[!DNL Page Builder] 開発者ガイド](https://developer.adobe.com/commerce/frontend-core/page-builder/) モジュールのアーキテクチャとカスタマイズの詳細を説明します。

## リソースのトラブルシューティング

トラブルシューティングに関するヘルプ [!DNL Page Builder] 問題：次を参照してください。 [!DNL Commerce] サポートに関するナレッジベース記事：

- [DotDigital の場合は空のページ [!DNL Page Builder] フォームが保存されました](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/magento-2.4.1-empty-page-when-dotdigital-page-builder-form-saved.html)
- [[!DNL Page Builder] メディアギャラリーを読み込みません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-12/mdva-32133-magento-patch-page-builder-doesn-t-load-media-gallery.html)
- [[!DNL Page Builder] プレビューブレーク製品価格がサイト間で異なる](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-16/mdva-33453-page-builder-preview-breaks-product-price-differs-across-sites.html)
- [キーワードページを保存できません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-19/mdva-33614-magento-patch-can-t-save-terms-page.html)
