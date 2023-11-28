---
title: マークアップタグ
description: ストア内のオブジェクトを参照するコードのスニペットを含むマークアップタグについて説明します。
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# マークアップタグ

マークアップタグは、変数、URL、画像、ブロックなど、ストア内のオブジェクトへの相対参照を持つコードのスニペットを含むディレクティブです。 マークアップタグは、エディターが使用可能な場所であればどこでも使用でき、 [電子メール](email-templates.md) および [ニュースレター](../merchandising-promotions/newsletter-template.md) テンプレート、およびその他のタイプの [コンテンツ](../content-design/introduction.md#content).

マークアップタグは、中括弧で囲み、ウィジェットツールで生成するか、HTMLコンテンツに直接入力することができます。 例えば、ページへのフルパスをハードコーディングする代わりに、マークアップタグを使用してストアの URL を表すことができます。 次の例に示すマークアップタグは次のとおりです。

{{$include /help/_includes/directives-caution.md}}

## カスタム変数

変数マークアップタグを使用して、 [カスタム変数](variables-custom.md) を e メールテンプレート、ブロック、ニュースレター、コンテンツページに変換します。

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## ストア URL

Store URL マークアップタグは、Web サイトのベース URL を表し、完全な URL の最初の部分（ドメイン名を含む）の代わりに使用されます。 このマークアップタグには 2 つのバージョンがあります。1 つはストアに直接送られ、もう 1 つはスラッシュ (`/`) で終わり、パスが追加されたときに使用されます。

\{{store url=&#39;apparel/shoes/womens&#39;}}

## メディア URL

Dynamic Media の URL マークアップタグは、コンテンツ配信ネットワーク (CDN) に保存される画像の場所とファイル名を表します。 タグを使用して、ページ、ブロック、バナーまたは電子メールテンプレートに画像を配置できます。

\{{media url=&#39;shoe-sale.jpg&#39;}}

## ブロック ID

ブロック ID マークアップタグは、最も使いやすいタグの 1 つで、CMS ページに直接ブロックを配置したり、別のブロック内にネストしたりする場合に使用できます。 この方法を使用すると、様々なプロモーションや言語のブロックを変更できます。 ブロック ID マークアップタグは、その識別子でブロックを参照します。

\{\{block id=&#39;block-id&#39;}}

## テンプレートタグ

テンプレートタグは、PHTML テンプレートファイルを参照し、CMS ページまたは静的ブロックにブロックを表示するのに使用できます。 次の例のコードは、「Contact Us」フォームを表示するページまたはブロックに追加できます。

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_連絡先：:form.phtml&quot;}}

次の例のコードは、特定のカテゴリに属する製品のリストをカテゴリ ID 別に表示するために、ページまたはブロックに追加できます。

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## ウィジェットコード

ウィジェットツールを使用して、製品のリストを表示したり、製品 ID に基づいて特定の製品ページに移動するリンクなど、複雑なリンクを挿入したりできます。 生成されるコードには、ブロック参照、コードモジュールの場所、および対応する PHTML テンプレートが含まれます。 コードが生成されたら、コピーして貼り付けることができます。

次の例のコードは、新しい製品のリストを表示するページまたはブロックに追加できます。

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

次の例のコードは、特定の製品へのリンクを製品 ID で表示するために、ページまたはブロックに追加できます。

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;マイ製品リンク&quot; title=&quot;マイ製品リンク&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## リンクでのマークアップタグの使用

マークアップタグとHTMLアンカータグを使用し、ストア内の任意のページに直接リンクできます。 リンクは、コンテンツページ、ブロック、電子メールおよびニュースレターのテンプレートに組み込むことができます。 また、この方法を使用して、画像を特定のページにリンクすることもできます。

### 手順 1. 宛先 URL の識別

可能であれば、リンク先のページに移動し、ブラウザーのアドレスバーから完全な URL をコピーします。 必要な URL の部分は、 `.com/`. それ以外の場合は、リンク先として使用する CMS ページから URL キーをコピーします。

#### カテゴリページへの完全な URL

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### 製品ページへの完全な URL

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### CMS ページへの完全な URL

`https://mystore.com/about-us`

### 手順 2. URL にマークアップを追加する

Store URL タグは、Web サイトのベース URL を表し、ストア URL の HTTP アドレス部分の代わりに使用されます ( ドメイン名や `.com`. タグには 2 つのバージョンがあり、達成すべき結果に応じて使用できます。

`store direct_url`  — ページに直接リンクします。

`store url`  — 末尾にスラッシュを配置し、追加の参照をパスとして追加できます。

次の例では、URL キーは一重引用符で囲み、マークアップタグ全体を二重中括弧で囲みます。 アンカータグと共に使用すると、マークアップタグはアンカーの二重引用符の内側に配置されます。 混乱を避けるために、ネストされた引用符の各セットに対して、一重引用符と二重引用符を使用して代替することができます。

をフル URL で始める場合は、HTTP アドレス (`http://` または `https://`) を含め、URL の（を含む） `.com/`. その代わりに、開始一重引用符を通して上に Store URL マークアップタグを入力します。

#### URL マークアップタグを保存

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

それ以外の場合は、「 URL を保存」マークアップタグの最初の部分を入力し、前にコピーした URL キーまたはパスを貼り付けます。

### URL キーを使用して URL マークアップタグを保存

`{{store url=`

マークアップタグを完了するには、終わりの二重引用符と二重括弧を入力します。

`{{store url='apparel/shoes/womens'}}`

### 手順 3. アンカータグを完了する

ターゲット URL の代わりにマークアップタグを使用して、完成したマークアップタグをアンカータグ内にラップします。 次に、リンクテキストと終了アンカータグを追加します。

#### アンカータグ内のマークアップ

\リ&lt;a href=&quot;\{\{markup tag goes here}}&quot;>ンクテキスト\&lt;/a>

完了したアンカータグを、リンクを表示する CMS ページ、ブロック、バナー、電子メールテンプレートのコードに貼り付けます。

### マークアップを含む完全なリンク

\&lt;a href=&quot;\{\{store url=&amp;#39;apparel/shoes&amp;#39;}}&quot;>靴の販売\&lt;/a>
