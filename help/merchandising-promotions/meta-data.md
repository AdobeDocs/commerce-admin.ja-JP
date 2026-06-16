---
title: Meta data
description: キーワードが豊富なメタデータを入力して、検索エンジンがCommerce サイトをインデックス化する方法を改善する方法について説明します。
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/hl0i6mlFJY5r5bIWNG6gQMGlWQMmaWOWBnt8pCpKT50
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 747
ht-degree: 0%

---

# Meta data

>[!TIP]
>
>Adobe Commerce as a Cloud Serviceについては、Commerce Storefront ドキュメントの[&#x200B; メタデータガイドライン &#x200B;](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/metadata/)を参照してください

ストアには、キーワードが豊富なメタデータを入力できる場所がロードされており、検索エンジンがサイトをインデックス作成する方法を改善できます。 ストアの設定中に、後で完了するために予備のメタデータを入力することもできます。 時間の経過とともにメタデータを微調整し、顧客の購入パターンや嗜好をターゲットにすることができます。

![製品設定 – 検索エンジン最適化](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Meta タイトル

メタタイトルは、ブラウザーと検索結果リストのタイトルバーとタブに表示されます。 メタタイトルは、ページに固有で、長さが70文字未満である必要があります。

![&#x200B; ストアフロントの例 – メタタイトル &#x200B;](./assets/storefront-home-page-meta-title.png){width="600"}

## Meta キーワード

メタキーワードを無視する検索エンジンもありますが、そのまま使用している検索エンジンもあります。 現在のベストプラクティスは、メタタイトルとメタディスクリプションに価値の高いキーワードを組み込むことです。

![Web ブラウザー検索 – メタキーワード &#x200B;](./assets/storefront-meta-description.png){width="500"}

## Metaの説明

Metaの説明では、検索結果リストのページの概要を説明します。 メタ説明は150～160文字の長さが理想的ですが、フィールドには255文字まで入力できます。

## リッチスニペット

リッチスニペットは、検索結果リストやその他のアプリケーションの詳細な情報を提供します。 デフォルトでは、[schema.org](https://schema.org/)標準に基づく構造化データマークアップが、ストアの製品テンプレートに追加されます。 その結果、検索エンジンが商品リストに&#x200B;_リッチスニペット_&#x200B;として含める場合は、より多くの情報を利用できます。

## 正規メタタグ

一部の検索エンジンは、同じコンテンツを指す複数のURLを持つweb サイトにペナルティを課します。 規範的なメタタグは、複数のURLに同一または類似のコンテンツがある場合に、インデックスを作成するページを検索エンジンに伝えます。 規範的なメタタグを使用することで、サイトのランキングを向上させ、ページビューを集約できます。 正規メタタグは、製品ページまたはカテゴリーページの`<head>` ブロックに配置されます。 好みのURLへのリンクが提供されるため、検索エンジンの重みが増します。

### 例1：カテゴリーパスで重複URLが作成される

例えば、カタログが商品URLにカテゴリーパスを含めるように設定されている場合、ストアは同じ商品ページを指す複数のURLを生成します。

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### 例2：カテゴリーページの完全なURL

カテゴリの正規メタタグが有効になっている場合、ストアのカテゴリーページには、カテゴリ全体のURLへの正規のURLが含まれます。

    http://mystore.com/gear/bags/

### 例3：製品ページのフル URL

製品の正規メタタグが有効になっている場合、製品URL キーはグローバルに一意であるため、製品ページにはdomain-name/product-url-keyへの正規URLが含まれます。

    http://mystore.com/driven-backpack.html

商品URLにカテゴリーパスも含める場合、正規URLはdomain-name/product-url-keyのままです。 ただし、製品には、カテゴリを含む完全なURLを使用してアクセスすることもできます。 例えば、製品のURL キーが`driven-backpack`で、ギア/バッグ カテゴリに割り当てられている場合、製品にはURLを使用してアクセスできます。

URLからカテゴリを省略するか、正規のメタタグを使用して、検索エンジンが製品またはカテゴリでインデックスを作成するように誘導することで、検索エンジンによるペナルティを回避できます。 ベストプラクティスとして、カテゴリと製品の両方に正規メタタグを有効にすることをお勧めします。

### 正規メタタグを有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **検索エンジン最適化** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   フィールド値を変更するには、最初に各フィールドの後ろに「**システム値を使用**」チェックボックスをオフにする必要があります。

   ![&#x200B; カタログ設定 – 検索エンジン最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. 完全なカテゴリパスを使用して、検索エンジンでカテゴリページのみをインデックス化する場合は、次の操作を行います。

   - **カテゴリに正規リンクのMeta タグを使用**&#x200B;から`Yes`に設定します。

   - **製品に正規リンクのMeta タグを使用**&#x200B;から`No`に設定します。

1. 検索エンジンにdomain-name/product-url-key形式のみを使用して製品ページをインデックス化させる場合は、次の操作を行います。

   - **製品に正規リンクのMeta タグを使用**&#x200B;から`Yes`に設定します。

   - **カテゴリに正規リンクのMeta タグを使用**&#x200B;から`No`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## Meta data demo

SEO メタデータの管理について詳しくは、次の動画をご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12&learn=on)
