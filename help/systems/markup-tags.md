---
title: マークアップタグ
description: ストア内のオブジェクトを参照するコードのスニペットを含むマークアップタグについて説明します。
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# マークアップタグ

マークアップタグは、ストア内のオブジェクト（変数、URL、画像、ブロックなど）への相対参照を持つコードのスニペットを含むディレクティブです。 マークアップタグは、エディターが使用可能な任意の場所で使用でき、[ メール ](email-templates.md) テンプレート、[ ニュースレター ](../merchandising-promotions/newsletter-template.md) テンプレートおよびその他の種類の [ コンテンツ ](../content-design/introduction.md#content) のHTMLに組み込むことができます。

マークアップタグは、二重の中括弧で囲まれ、ウィジェットツールで生成することも、HTMLコンテンツに直接入力することもできます。 例えば、ページへのフルパスをハードコーディングする代わりに、マークアップタグを使用してストア URL を表すことができます。 次の例に示すマークアップタグは次のとおりです。

{{$include /help/_includes/directives-caution.md}}

## カスタム変数

変数マークアップタグを使用すると、メールテンプレート、ブロック、ニュースレターおよびコンテンツページに [ カスタム変数 ](variables-custom.md) を挿入できます。

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## ストア URL

Store URL markup タグは、web サイトのベース URL を表し、ドメイン名を含む完全な URL の最初の部分の代わりに使用されます。 このマークアップタグには 2 つのバージョンがあります。1 つはストアに直接送信し、もう 1 つはパスの追加時に使用されるスラッシュ（`/`）を末尾に付加したものです。

\{\{store url=&#39;apparel/shoes/womens&#39;}}

## メディア URL

Dynamic media URL マークアップタグは、コンテンツ配信ネットワーク（CDN）に保存された画像の場所とファイル名を表します。 タグを使用すると、ページ、ブロック、バナー、メールテンプレートに画像を配置できます。

\{\{media url=&#39;shoe-sale.jpg&#39;}}

## ブロック ID

ブロック ID マークアップタグは、最も簡単に使用できるタグの 1 つで、CMS ページに直接ブロックを配置したり、別のブロック内にネストしたりするために使用できます。 この方法を使用して、異なるプロモーションや言語に合わせてブロックを変更できます。 ブロック ID マークアップ タグは、識別子でブロックを参照します。

\{\{block id=&#39;block-id&#39;}}

## テンプレートタグ

テンプレートタグは、PHTML テンプレートファイルを参照し、CMS ページまたは静的ブロックにブロックを表示するために使用できます。 次の例のコードは、お問い合わせフォームを表示するページまたはブロックに追加できます。

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_連絡先：:form.phtml&quot;}}

次の例のコードは、ページまたはブロックに追加して、カテゴリ ID ごとに特定のカテゴリに含まれる製品のリストを表示することができます。

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## ウィジェットコード

ウィジェットツールを使用すると、製品のリストを表示したり、製品 ID に基づいて特定の製品ページに移動するような複雑なリンクを挿入したりできます。 生成されるコードには、ブロック参照、コードモジュールの場所、対応する PHTML テンプレートが含まれます。 コードを生成した後、ある場所から別の場所にコピーして貼り付けることができます。

次の例のコードは、ページまたはブロックに追加して、新製品のリストを表示できます。

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

次の例のコードは、ページまたはブロックに追加して、特定の製品へのリンクを製品 ID で表示することができます。

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;My Product Link&quot; title=&quot;My Product Link&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## リンクでのマークアップタグの使用

マークアップタグとHTMLアンカータグを使用すると、ストア内の任意のページに直接リンクできます。 リンクは、コンテンツページ、ブロック、メールテンプレートおよびニュースレターテンプレートに組み込むことができます。 この方法を使用して、画像を特定のページにリンクすることもできます。

### 手順 1. 宛先 URL の特定

可能であれば、リンク先のページに移動し、ブラウザーのアドレスバーから完全な URL をコピーします。 URL のうち、必要な部分は `.com/` の後に配置されます。 そうでない場合は、リンク先として使用する URL キーを CMS ページからコピーします。

#### カテゴリページの完全な URL

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### 製品ページの完全な URL

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### CMS ページの完全な URL

`https://mystore.com/about-us`

### 手順 2. URL へのマークアップの追加

ストア URL タグは、web サイトのベース URL を表し、ドメイン名や `.com` など、ストア URL の HTTP アドレス部分の代わりに使用されます。 タグには 2 つのバージョンがあり、実行する結果に応じて使用できます。

`store direct_url` - ページに直接リンクします。

`store url` – 末尾にスラッシュを配置して、参照をパスとして追加できるようにします。

次の例では、URL キーは一重引用符で囲まれ、マークアップ タグ全体は二重中括弧で囲まれています。 アンカータグと共に使用すると、マークアップタグはアンカーの二重引用符の内側に配置されます。 混乱を避けるために、ネストされた引用符セットごとに一重引用符と二重引用符を使用して代替できます。

完全な URL から始める場合は、URL の HTTP アドレス（`http://` または `https://`）の部分（`.com/` まで）を削除します。 その代わりに、URL マークアップタグをストアに入力します。このタグの先頭には一重引用符を使用します。

#### URL マークアップタグの保存

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

それ以外の場合は、URL マークアップタグを格納の最初の部分を入力し、以前にコピーした URL キーまたはパスを貼り付けます。

### URL キーを含む URL マークアップタグを保存

`{{store url=`

マークアップ タグを完成するには、閉じる二重引用符と二重中括弧を入力します。

`{{store url='apparel/shoes/womens'}}`

### 手順 3. アンカータグの入力

ターゲット URL の代わりにマークアップタグを使用して、完成したマークアップタグをアンカータグの中に含めます。 次に、リンクテキストと終了アンカータグを追加します。

#### アンカータグ内のマークアップ

\&lt;a href=&quot;\{\{markup tag goes here}}&quot;> リンクテキスト\&lt;/a>

完成したアンカータグを、リンクを表示する任意の CMS ページ、ブロック、バナーまたはメールテンプレートのコードに貼り付けます。

### マークアップ付きの完全リンク

\&lt;a href=&quot;\{\{store url=&#39;apparel/shoes&#39;}}&quot;> 靴の販売\&lt;/a>
