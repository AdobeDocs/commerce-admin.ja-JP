---
title: ウィジェット
description: さまざまなコンテンツを表示し、ストア内の特定のブロック参照に配置できるコードスニペットを提供するウィジェットについて説明します。
exl-id: 993ba2ca-a8de-4f7e-8cab-7ba7d16eebe7
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/ov5Wt8dIf--1UoXqFtv-NiAaEVL97UaQodxU4bGe8zo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 671
ht-degree: 0%

---

# ウィジェット

ウィジェットとは、幅広いコンテンツを表示し、ストア内の特定のブロック参照に配置できるようにする、コードのスニペットのことです。 多くのウィジェットは、リアルタイムの動的データを表示し、顧客がストアと対話する機会を生み出します。 ウィジェットツールを使用すると、画像やテキストを含むブロックや、ストア内の任意の場所にあるインタラクティブな要素など、既存のコンテンツ内にウィジェットを簡単に配置できます。

ウィジェットを使用して、マーケティングキャンペーン用のランディングページを作成したり、ストア全体の特定の場所にプロモーションコンテンツを表示したりできます。 ウィジェットは、外部レビューシステム、ビデオチャット、投票、購読フォームのインタラクティブ要素やアクションブロックを追加したり、タグクラウドや画像スライダーのナビゲーション要素を提供したりするためにも使用できます。

{{$include /help/_includes/directives-caution.md}}

![新製品リストウィジェット &#x200B;](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## ウィジェットタイプ

ウィジェットを[作成する場合](widget-create.md)は、タイプを設定する必要があります。 このタイプは、ウィジェットの機能を決定します。

| タイプ | 説明 |
|--- |--- |
| [!UICONTROL CMS Hierarchy Node Link] | このオプションを使用すると、他のコンテンツに組み込むことができるページ階層内の特定のノードへのリンクを表示できます。 |
| [!UICONTROL CMS Page Link] | カスタムテキストと、特定のCMS ページにリンクするタイトルを指定するには、このオプションを使用します。 リンクが完了したら、コンテンツページやブロックで使用できます。 |
| [!UICONTROL CMS Static Block] | ページ上の特定の場所にコンテンツブロックを表示するには、このオプションを使用します。 |
| [!UICONTROL Catalog Category Link] | 選択したカタログ カテゴリへのインライン リンクまたはブロック スタイル リンクを表示するには、このオプションを使用します。 リンクが完了したら、コンテンツページやブロックで使用できます。 |
| [!UICONTROL Catalog Events Carousel] | 今後のカタログイベントのリストを表示するには、このオプションを使用します。 |
| [!UICONTROL Catalog New Products List] | このオプションを使用すると、製品レコードで指定された時間内に、新規製品として指定された製品ブロックを表示できます。 |
| [!UICONTROL Catalog Product Link] | このオプションを使用すると、選択したカタログ商品へのインラインリンクまたはブロックスタイルのリンクを表示できます。 リンクが完了したら、コンテンツページやブロックで使用できます。 |
| [!UICONTROL Catalog Products List] | このオプションを使用して、カタログの商品のリストを表示します。 |
| [!UICONTROL Dynamic Blocks Rotator] | このオプションを使用すると、1つの動的ブロック、または一連の動的ブロックの並べ替え、ランダムな順序、またはシャッフルを表示できます。 ダイナミックブロックは、価格ルールによってトリガーされ、特定のページと場所に配置されるか、すべてのページに表示されるように設定できます。 |
| [!UICONTROL Gift Registry Search] | このオプションを使用すると、買い物客は名前またはレジストリ IDでパブリックギフトレジストリを検索できます。 |
| [!UICONTROL Order by SKU] | SKUによる注文は、すべての買い物客の利便性としてストアに表示されるか、特定の顧客グループでのみ利用可能になります。 顧客は、SKUおよび数量情報を直接注文SKU ブロックに入力するか、顧客アカウントからCSV ファイルをアップロードできます。 |
| [!UICONTROL Orders and Returns] | このオプションを使用すると、ゲストは注文のステータスを確認し、商品を返品するリクエストを送信できます。 ウィジェットは、アカウントにログインしていないゲストと顧客にのみ表示されます。 |
| [!UICONTROL Recently Compared Products] | 最近比較した商品のブロックを表示します。 含まれる製品数を指定し、リストまたは製品グリッドとして書式設定できます。 |
| [!UICONTROL Recently Viewed Products] | 最近閲覧した商品のブロックを表示するには、このオプションを使用します。 含まれる製品数を指定し、リストまたは製品グリッドとして書式設定できます。 ウィジェットにリアルタイムの価格更新が表示されない場合があります。 顧客が製品をクリックすると、製品ページで現在の価格を確認する必要があります。 |
| [!UICONTROL Wish List Search] | このオプションを使用すると、お客様はウィッシュリストの所有者の名前またはメールアドレスで公開されているウィッシュリストを検索できます。 店舗のお客様は、他のお客様に属するウィッシュリストを検索したり、それらを表示して商品を注文したり、自分のウィッシュリストに商品を追加したりできます。 |

{style="table-layout:auto"}

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
