---
title: メタデータ
description: 検索エンジンによるCommerce サイトのインデックス作成方法を改善するために、キーワードの多いメタデータを入力する方法について説明します。
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# メタデータ

>[!TIP]
>
>Adobe Commerce as a Cloud Serviceについては、Commerce ストアフロントドキュメントの [ メタデータガイドライン ](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/metadata/?lang=ja) を参照してください

ストアには、検索エンジンによるサイトのインデックス作成方法を改善するために、キーワードが豊富なメタデータを入力できる場所が多数用意されています。 ストアを設定する際に、後で終了する目的で、予備のメタデータを入力する場合があります。 時間の経過と共に、メタデータを微調整して、顧客の購入パターンや好みをターゲットに設定できます。

![ 製品設定 – 検索エンジンの最適化 ](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## メタタイトル

メタタイトルは、ブラウザーと検索結果のリストのタイトルバーとタブに表示されます。 メタタイトルは、ページに固有で、長さが 70 文字未満である必要があります。

![ ストアフロントの例 – メタタイトル ](./assets/storefront-home-page-meta-title.png){width="600"}

## メタキーワード

メタキーワードを無視する検索エンジンもあれば、メタキーワードを使用し続ける検索エンジンもあります。 現在のベストプラクティスは、価値の高いキーワードをメタタイトルおよびメタ説明に組み込むことです。

![Web ブラウザー検索 – メタキーワード ](./assets/storefront-meta-description.png){width="500"}

## メタ説明

メタ記述は、検索結果リストのページの概要を説明します。 フィールドの受け入れ文字数は 255 文字ですが、メタ記述の長さは 150～160 文字が理想的です。

## 豊富なスニペット

豊富なスニペットにより、検索結果のリストやその他のアプリケーションに関する詳細情報が提供されます。 デフォルトでは、[schema.org][1] 標準に基づく構造化データマークアップがストアの製品テンプレートに追加されます。 その結果、検索エンジンで製品リストに _リッチ スニペット_ として含める情報が増えます。

## 正規メタタグ

一部の検索エンジンでは、同じコンテンツを指す複数の URL を持つ web サイトにペナルティを課します。 正規メタタグは、複数の URL のコンテンツが同一または類似している場合に、どのページをインデックス化するかを検索エンジンに指示します。 正規のメタタグを使用すると、サイトのランキングとページビューの集計を向上できます。 正規メタタグは、製品ページまたはカテゴリページの `<head>` ブロックに配置されます。 指定した URL へのリンクが提供されるので、検索エンジンを使用すると URL により大きな重み付けが与えられます。

### 例 1：カテゴリパスで重複した URL が作成される

例えば、製品 URL にカテゴリパスを含めるようにカタログが設定されている場合、ストアは同じ製品ページを指す複数の URL を生成します。

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### 例 2：カテゴリページの完全な URL

カテゴリの正規メタタグが有効になっている場合、ストアのカテゴリページには、完全なカテゴリ URL への正規 URL が含まれます。

    http://mystore.com/gear/bags/

### 例 3：製品ページの完全 URL

製品の正規メタタグが有効になっている場合、製品 URL キーはグローバルに一意なので、製品ページには domain-name/product-url-key への正規 URL が含まれます。

    http://mystore.com/driven-backpack.html

製品 URL にカテゴリパスも含める場合、正規 URL は domain-name/product-url-key のままになります。 ただし、カテゴリを含む完全な URL を使用して製品にアクセスすることもできます。 例えば、プロダクトの URL キーが `driven-backpack` で、ギア/バッグ カテゴリに割り当てられている場合、プロダクトはどちらの URL を使用してもアクセスできます。

URL からカテゴリを省略するか、正規のメタタグを使用して検索エンジンが製品またはカテゴリ別にインデックスを作成するように指示すれば、検索エンジンによってペナルティを科されることを回避できます。 ベストプラクティスとして、カテゴリと製品の両方で正規メタタグを有効にすることをお勧めします。

### 正規メタタグの有効化

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. ![ 拡張セレクター ](../assets/icon-display-expand.png) 「**検索エンジンの最適化**」セクションを展開します。

   フィールド値を変更するには、まず各フィールドの後にある **システム値を使用** チェックボックスをオフにする必要があります。

   ![ カタログ設定 – 検索エンジンの最適化 ](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. 検索エンジンで、完全なカテゴリパスを使用してカテゴリページのみのインデックスを作成する場合は、次の操作を行います。

   - **カテゴリに正規リンクメタタグを使用** を `Yes` に設定します。

   - **製品に正規リンクメタタグを使用** を `No` に設定します。

1. 検索エンジンで、domain-name/product-url-key 形式のみを使用して製品ページのインデックスを作成する場合は、次の手順を実行します。

   - **製品に正規リンクメタタグを使用** を `Yes` に設定します。

   - **カテゴリに正規リンクメタタグを使用** を `No` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## メタデータデモ

SEO メタデータの管理については、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/3410176?quality=12&learn=on&captions=jpn)

[1]: https://schema.org/
