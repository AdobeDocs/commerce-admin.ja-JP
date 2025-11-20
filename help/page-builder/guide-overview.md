---
title: '[!DNL Page Builder] ユーザーガイド'
description: Adobe CommerceおよびMagento Open Source [!DNL Page Builder]  管理者向けの包括的な情報です。
seo-title: Adobe Commerce [!DNL Page Builder] User Guide
seo-description: Describes how to use the [!DNL Page Builder] module in Adobe Commerce or Magento Open Source.
exl-id: 983ef3a8-b803-40ff-a9f5-07eb895df31c
source-git-commit: dbc0057f02bddf681d769bdaebfaf6b526c8dbd2
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# [!DNL Page Builder] ユーザーガイド

このガイドは、Adobe CommerceおよびMagento Open Source Admin で作業する管理者を対象としています。 基本的なコンテンツコンポーネントの構築を 3 つのパートで [!DNL Page Builder] うウォークスルーなど、の機能に関する詳細情報を提供します。 ここでは、コア [!DNL Commerce] の設定と機能に関する基本的な知識を前提としています。

[!DNL Page Builder] には、ストア管理者用の次の 2 つの領域があります。

- 管理者：この領域を使用して設定 UI にアクセスし、ページビルダーツールを操作します。
- コマンドラインインターフェイス：このツールを使用して、インストールタスクとバックエンド設定タスクを実行します。

このガイドでは、次の内容について説明します。

| 件名 | 説明 |
| ------- | ----------- |
| [&#x200B; はじめに &#x200B;](introduction.md) | [!DNL Page Builder] とは また、Adobe CommerceとMagento Open Sourceのサイトでのコンテンツ作成をどのように強化するのでしょうか。 |
| [&#x200B; リリースノート &#x200B;](release-notes.md) | 各 [!DNL Page Builder] モジュールリリースで提供されるアップデートを確認します。 |
| [&#x200B; 設定 &#x200B;](setup.md) | デフォルトの設定を更新するには、デフォルトのページレイアウトを変更し、より高度な [!DNL Page Builder] 機能を有効にします。 また、[!DNL Google Maps] を統合して、場所のコンテンツをページに組み込むこともできます。 |
| [Workspace](workspace.md) | [!DNL Page Builder] Workspace のコンポーネントと、それらを使用してストア向けの魅力的なコンテンツを作成する方法を確認します。 |
| ガイド | [!DNL Page Builder] を使い始めたばかりの場合は、チュートリアルの演習を完了することで、すばやく作業を開始できます。<br>[1 - サンプルページ &#x200B;](1-simple-page.md)<br>[2 – 再利用可能なコンテンツブロック &#x200B;](2-blocks.md)<br>[3 – 製品名用のカタログページ &#x200B;](3-catalog-content.md) |
| [Workspace](workspace.md) | 基本ページ、製品およびカタログ ページ、ブロック、動的ブロックを作成する際に、[!DNL Page Builder] ワークスペースで使用できるツールを確認します。 |
| レイアウト | _パネルの_ レイアウト [!DNL Page Builder] セクションと、これらのツールを使用して [!DNL Page Builder] ステージにレイアウトコンポーネントを追加する方法を確認します。<br>[&#x200B; 行 &#x200B;](row.md)<br>[&#x200B; 列 &#x200B;](column.md)<br>[&#x200B; タブ &#x200B;](tabs.md) |
| 要素 | _パネルの_ 要素 [!DNL Page Builder] セクションと、これらのツールを使用して [!DNL Page Builder] ステージの任意のレイアウトコンテナに基本要素を追加する方法を確認します。<br>[&#x200B; テキスト &#x200B;](text.md)<br>[&#x200B; 見出し &#x200B;](heading.md)<br>[&#x200B; ボタン &#x200B;](buttons.md)<br>[&#x200B; デバイダー &#x200B;](divider.md)<br>[HTML コード &#x200B;](html-code.md) |
| メディア | _ントロールパネルの「_ メディア [!DNL Page Builder]」セクションと、これらのツールを使用して [!DNL Page Builder] ステージ上の任意のレイアウトコンテナにメディアアイテムを追加する方法を確認します。<br>[images](image.md)<br>[video](video.md)<br>[banners](banner.md)<br>[slider](slider.md)<br>[[!DNL Google Maps]](map.md) |
| コンテンツを追加 | コンテン _パネルの_ コンテンツを追加 [!DNL Page Builder] セクションと、[!DNL Page Builder] ステージにコンテンツコンポーネントを追加する方法を確認します。<br>[&#x200B; ブロック &#x200B;](block.md)<br>[&#x200B; 動的ブロック &#x200B;](dynamic-block.md)<br>[&#x200B; 製品 &#x200B;](products.md)<br>[&#x200B; 製品レコメンデーション &#x200B;](recommendations.md) （Adobe Commerceのみ） |
| [&#x200B; テンプレート &#x200B;](templates.md) | 既存の [!DNL Page Builder] コンテンツをテンプレートとして保存し、そのテンプレートを別の領域に適用して、コンテンツをすばやく一貫して作成できるようにします。 |

{style="table-layout:auto"}

Adobe CommerceおよびMagento Open Sourceのコア機能については説明しません。

## 追加ドキュメント

{{docs-links}}

## [!DNL Page Builder] 開発者情報

[!DNL Page Builder] はAdobe Commerce 2.4.x およびMagento Open Source 2.4.3 以降と共にインストールされ、すべての機能がデフォルトで有効になっています。 モジュールリリースに含まれる変更点について詳しくは、[[!DNL Page Builder]  リリースノート &#x200B;](release-notes.md) を参照してください。 [[!DNL Page Builder]  開発者ガイド &#x200B;](https://developer.adobe.com/commerce/frontend-core/page-builder/) には、モジュールのアーキテクチャとカスタマイズの詳細が記載されています。

## リソースのトラブルシューティング

[!DNL Page Builder] の問題のトラブルシューティングについて詳しくは、[!DNL Commerce] サポートナレッジベースの次の記事を参照してください。

- [DotDigital [!DNL Page Builder] form を保存した際の空のページ &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/magento-2.4.1-empty-page-when-dotdigital-page-builder-form-saved.html)
