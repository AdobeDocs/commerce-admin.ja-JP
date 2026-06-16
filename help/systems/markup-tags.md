---
title: マークアップタグ
description: ストア内のオブジェクトを参照するコードのスニペットを含むマークアップタグについて説明します。
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
TQID: https://experienceleague.adobe.com/Is9ZYbe3G4uXGAcoY8KjaaNVvTdHgYpTvmZBpj7SQpU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 5ad33b22f893986a79bbb746f476e8490080fb0d
workflow-type: tm+mt
source-wordcount: 914
ht-degree: 0%

---

# マークアップタグ

マークアップタグは、変数、URL、画像、ブロックなど、ストア内のオブジェクトへの相対参照を持つコードのスニペットを含むディレクティブです。 マークアップタグは、エディターが利用できるあらゆる場所で使用でき、[email](email-templates.md)および[newsletter](../merchandising-promotions/newsletter-template.md) テンプレートのHTMLや、その他の種類の[content](../content-design/introduction.md#content)に組み込むことができます。

マークアップタグは二重中括弧で囲まれ、ウィジェットツールで生成するか、HTML コンテンツに直接入力できます。 例えば、ページへのフルパスをハードコーディングするのではなく、マークアップタグを使用してストア URLを表すことができます。 次の例では、マークアップタグを紹介します。

{{$include /help/_includes/directives-caution.md}}

## カスタム変数

変数マークアップタグを使用すると、メールテンプレート、ブロック、ニュースレター、コンテンツページに[&#x200B; カスタム変数](variables-custom.md)を挿入できます。

`{{CustomVar code= "my_custom_variable"}}`

## ストア URL

Store URL マークアップタグは、web サイトのベース URLを表し、ドメイン名を含む完全なURLの最初の部分の代わりに使用されます。 このマークアップタグには、2つのバージョンがあります。1つはストアに直接送信され、もう1つはパスが追加されたときに使用される末尾にスラッシュ（`/`）が付いています。

`{{store url='apparel/shoes/womens'}}`

## メディア URL

Dynamic Media URL マークアップタグは、コンテンツ配信ネットワーク（CDN）に保存される画像の場所とファイル名を表します。 タグを使用すると、ページ、ブロック、バナー、メールテンプレートに画像を配置できます。

`{{media url='shoe-sale.jpg'}}`

## ブロック ID

ブロック ID マークアップタグは、最も使いやすいもののひとつであり、CMS ページに直接ブロックを配置したり、別のブロック内にネストしたりするために使用できます。 この手法を使用して、様々なプロモーションや言語に合わせてブロックを変更できます。 ブロック ID マークアップ タグは、ブロックを識別子で参照します。

`{{block id='block-id'}}`

## テンプレートタグ

テンプレートタグはPHTML テンプレートファイルを参照し、CMS ページまたは静的ブロックにブロックを表示するために使用できます。 次の例のコードは、ページまたはブロックに追加して、問い合わせフォームを表示できます。

`{{block class="Magento\Contact\Block\ContactForm" name="contactForm" template="Magento_Contact::form.phtml"}}`

次の例のコードをページまたはブロックに追加して、特定のカテゴリの製品のリストをカテゴリ IDで表示できます。

`{{block type="catalog/product_list" category_id="22" template="catalog/product/list.phtml"}}`

## ウィジェットコード

ウィジェットツールを使用すると、製品のリストを表示したり、製品IDに基づいて特定の製品ページに移動するリンクなど、複雑なリンクを挿入したりできます。 生成されるコードには、ブロック参照、コードモジュールの場所、対応するPHTML テンプレートが含まれます。 コードを生成した後、コピーして、ある場所から別の場所に貼り付けることができます。

次の例のコードは、ページまたはブロックに追加して、新製品のリストを表示できます。

`{{widget type="catalog/product_widget_new" display_type="new_products" products_count="10" template="catalog/product/widget/new/content/new_grid.phtml"}}`

次の例のコードは、ページまたはブロックに追加して、特定の製品へのリンクを製品IDで表示できます。

`{{widget type="catalog/product_widget_link" anchor_text="My Product Link" title="My Product Link" template="catalog/product/widgetlink/link_block.phtml" id_path="product/31"}}`

## リンクでのマークアップタグの使用

HTMLのアンカータグでマークアップタグを使用し、ストア内の任意のページに直接リンクできます。 リンクは、コンテンツページ、ブロック、メールやニュースレターのテンプレートに組み込むことができます。 このテクニックを使用して、画像を特定のページにリンクすることもできます。

### 手順1: 宛先URLの特定

可能であれば、リンク先のページに移動し、ブラウザーのアドレスバーから完全なURLをコピーします。 必要なURLの部分は`.com/`の後にあります。 それ以外の場合は、リンク先として使用するCMS ページからURL キーをコピーします。

#### カテゴリーページへの完全なURL

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### 製品ページへの完全なURL

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### CMS ページへの完全なURL

`https://mystore.com/about-us`

### 手順2: URLにマークアップを追加する

Store URL タグは、web サイトのベース URLを表し、ドメイン名と`.com`を含むストア URLのHTTP アドレス部分の代用として使用されます。 タグには2つのバージョンがあり、目的の結果に応じて使用できます。

`store direct_url` - ページに直接リンクします。

`store url` – 末尾にスラッシュを配置して、追加の参照をパスとして追加できるようにします。

次の例では、URL キーは一重引用符で囲まれ、マークアップ タグ全体は二重中括弧で囲まれています。 アンカータグと共に使用する場合、マークアップタグはアンカーの二重引用符の内側に配置されます。 混同を避けるために、ネストされた引用符セットごとに一重引用符と二重引用符を使用して交互に使用できます。

完全なURLで始める場合は、URLのHTTP アドレス （`http://`または`https://`）の部分を削除し、`.com/`を含めます。 その代わりに、「ストア URL マークアップ」タグを入力し、最初の一重引用符を通して入力します。

#### URL マークアップタグを保存

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

それ以外の場合は、ストア URL マークアップタグの最初の部分を入力し、先ほどコピーしたURL キーまたはパスを貼り付けます。

### URL キーを使用したURL マークアップタグの保存

`{{store url=`

マークアップタグを完成させるには、閉じる二重引用符と二重中括弧を入力します。

`{{store url='apparel/shoes/womens'}}`

### 手順3: アンカータグを完成させる

完成したマークアップタグを、ターゲット URLではなくマークアップタグを使用して、アンカータグ内にラップします。 次に、リンクテキストと終了アンカータグを追加します。

#### アンカータグのマークアップ

`<a href="{{markup tag goes here}}">Link Text</a>`

完成したアンカータグを、リンクを表示する任意のCMS ページ、ブロック、バナー、またはメールテンプレートのコードに貼り付けます。

### マークアップ付きの完全リンク

`<a href="{{store url='apparel/shoes'}}">Shoe Sale</a>`

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
