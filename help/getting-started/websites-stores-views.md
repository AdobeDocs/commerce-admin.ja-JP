---
title: サイト、ストア、ビューの範囲
description: 顧客にショッピングエクスペリエンスを提供するために使用できる web サイト、ストア、ストアビューの階層について説明します。
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# サイト、ストア、ビューの範囲

すべてのAdobe CommerceとMagento Open Sourceのインストールには、web サイト、ストア、ストアビューの [ 階層 ](../stores-purchase/stores.md) があります。 _範囲_ という用語は、製品、属性、カテゴリなどのデータベースエンティティ、コンテンツ要素、構成設定が適用される階層内の場所を決定します。 Web サイト、ストア、ストアビューには、1 対多の親子関係があります。 1 つのインストールに複数の web サイトを含めることができ、各 web サイトに複数のストアやストア表示を含めることができます。

>[!NOTE]
>
>詳しくは、[!DNL Commerce] 開発者向けドキュメントの [ 複数の web サイトまたはストア ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=ja) を参照してください。

## Web サイト

インストールは、単一の [Web サイト ](../stores-purchase/stores.md#add-websites) から始まります。これは、デフォルトでは _メイン Web サイト_ と呼ばれます。 また、1 つのインストールに対して、独自の IP アドレスとドメインを持つ複数の web サイトを設定することもできます。

## ストア

1 つの web サイトに複数の [ ストア ](../stores-purchase/stores.md#add-stores) を含めることができ、それぞれに独自のメインメニューを持たせることができます。 店舗は商品カタログを共有しますが、異なる商品とデザインを選択できます。 同じ web サイト下のすべてのストアで、管理とチェックアウトが共有されます。

## ビューを保存

顧客が使用できる各ストアは、特定の _[表示](../stores-purchase/store-views.md)_ に従って表示されます。 最初は、ストアには単一のデフォルト表示があります。 別の言語をサポートするために、またはその他の目的のために、追加のストアビューを追加できます。 ユーザーは、ヘッダーの言語選択を使用して、ストア表示を変更できます。

Web サイト、ストア、ストアビューを使用する場合は、次の点に注意してください。

- Commerce インスタンスにはカスケードモデルがあります。グローバル → web サイト → ストア→ストアビュー。
- 各 web サイトには、デフォルトのストアとストア表示が少なくとも 1 つあります。
- 各ストア表示には、異なるベース URL を含めることができます。
- Web サイトの主な機能は、トップレベルの機能設定です。
- ストアの主な機能は、ルートカテゴリ設定です。
- ストア表示の主な機能は、翻訳情報と通貨記号の設定です。

## 範囲設定

Adobe CommerceまたはMagento Open Sourceのインストールに Web サイト、ストア、ビューの階層がある場合は、設定のコンテキストまたは _範囲_ を設定できます。 また、多くのデータベースエンティティのコンテキストに特定の範囲を割り当てて、ストア階層での使用方法を決定することもできます。 詳しくは、[ 製品範囲 ](../catalog/introduction.md#product-scope) と [ 価格範囲 ](../catalog/catalog-price-scope.md) を参照してください。

郵便番号などの一部の設定は、システム全体で同じ値が使用されるので、グローバル範囲を持ちます。 [web サイト ](../stores-purchase/stores.md#add-websites) の範囲は、階層内のそのレベルより下のすべてのストア（すべてのストアとそのビューを含む）に適用されます。 [ ストア表示 ](../stores-purchase/store-views.md) の範囲を持つ項目は、ストア表示ごとに異なる設定が可能です。これは通常、複数の言語をサポートするために使用されます。 構成設定のデフォルト値を上書きする方法については、[ 範囲の設定 ](../configuration-reference/scope-change.md#set-the-scope) を参照してください。

ストアが [ 単一ストアモード ](#single-store-mode) で実行されていない限り、各設定の範囲は、フィールドラベルの下に小さなテキストで表示されます。 インストールに複数の web サイト、ストアまたはビューが含まれている場合は、変更を加える前に設定が適用される [ ストア表示 ](../stores-purchase/store-views.md) を選択します。

![Web サイト、ストア、ストアビューの階層 ](./assets/scope-multisite.svg){width="550"}

| 範囲 | 説明 |
|--- |--- |
| [!UICONTROL Global] | インストール全体で利用できるシステム全体の設定とリソース。 |
| [!UICONTROL Website] | 現在の web サイトに限定された設定とリソース。 各 web サイトにはデフォルトのストアがあります。 |
| [!UICONTROL Store] | 現在のストアに限定された設定とリソース。 各ストアには、デフォルトのルートカテゴリ（メインメニュー）とデフォルトのストア表示があります。 |
| [!UICONTROL Store View] | 現在のストア表示に制限されている設定とリソース。 |

{style="table-layout:auto"}

## シングルストアモード

Commerceのインストールにストアとストアの表示が 1 つしかない場合は、すべてのストア表示オプションとスコープインジケーターをオフにすることで、表示を簡単にすることができます。 後で [ さらにストア表示を追加 ](../stores-purchase/store-views.md) すると、シングルストアモードが上書きされます。

![ 範囲 – シングルビュー ](./assets/scope-single-view.svg){width="550"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. **[!UICONTROL General]** の下で、ページの下部までスクロール ダウンし、[**[!UICONTROL Single-Store Mode]**] セクションを展開します。

1. **[!UICONTROL Enable Single-Store Mode]** を `Yes` に設定します。

   ![ 一般設定 – シングルストアモードの有効化 ](./assets/general-single-store-mode.png){width="400"}

1. 「**[!UICONTROL Save Config]**」をクリックします。

1. キャッシュを更新するように求められたら、次の操作を行います。

   - ページ上部にあるシステムメッセージの「**[!UICONTROL Cache Management]**」リンクをクリックします。

     ![ システムメッセージ – キャッシュ管理 ](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - 「**[!UICONTROL Page Cache]**」チェックボックスをオンにします。

   - **[!UICONTROL Actions]** を `Refresh` に設定し、「**[!UICONTROL Submit]**」をクリックします
