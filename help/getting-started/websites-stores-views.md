---
title: サイト、ストア、および表示範囲
description: 顧客に対してショッピングエクスペリエンスを提供するために使用できる Web サイト、ストア、ストア表示の階層について説明します。
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# サイト、ストア、および表示範囲

Adobe CommerceとMagento Open Sourceのインストールには、 [階層](../stores-purchase/stores.md) web サイト、ストア、ストアの表示数を格納します。 用語 _範囲_ 階層内で、製品、属性、カテゴリなどのデータベースエンティティがコンテンツ要素または設定を適用する場所を決定します。 Web サイト、ストア、およびストア表示には、1 対多の親と子の関係があります。 1 つのインストールに複数の Web サイトを含め、各 Web サイトに複数のストアやビューを保存できます。

>[!NOTE]
>
>詳しくは、 [複数の Web サイトまたはストア](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) （内） [!DNL Commerce] 開発者向けドキュメント。

## Web サイト

インストールは 1 つから始まります [web サイト](../stores-purchase/stores.md#add-websites)（と呼ばれる） _メイン Web サイト_ デフォルトでは。 また、1 回のインストールに対して複数の Web サイトを設定し、それぞれに独自の IP アドレスとドメインを設定することもできます。

## ストア

1 つの Web サイトに複数の [ストア](../stores-purchase/stores.md#add-stores)には、それぞれ独自のメインメニューがあります。 店舗は商品カタログを共有しますが、異なる商品やデザインを選ぶことができます。 同じ Web サイトにあるすべてのストアは、管理者とチェックアウトを共有します。

## ストア表示

顧客が利用できる各ストアは、 _[表示](../stores-purchase/store-views.md)_. 最初は、ストアのデフォルトビューは 1 つです。 様々な言語をサポートするため、または他の目的でストアビューを追加できます。 ユーザーは、ヘッダーの言語選択を使用して、ストア表示を変更できます。

Web サイト、ストア、ストアの表示を操作する場合は、次の点に注意してください。

- コマースインスタンスにはカスケードモデルがありま→。グローバル Web サイト→ストア→ストア表示です。
- 各 Web サイトには、少なくとも 1 つのデフォルトのストアおよびストア表示があります。
- 各ストアビューには異なるベース URL を設定できます。
- Web サイトの主な機能は、最上位レベルの機能設定です。
- ストアの主な機能は、ルートカテゴリ設定です。
- ストア表示の主な機能は、翻訳情報と通貨記号の設定です。

## 範囲設定

Adobe CommerceまたはMagento Open Sourceのインストールに Web サイト、ストア、表示の階層がある場合は、コンテキスト、または _範囲_ を設定します。 また、多くのデータベースエンティティのコンテキストに、特定のスコープを割り当てて、ストア階層での使用方法を決定することもできます。 詳しくは、 [製品範囲](../catalog/introduction.md#product-scope) および [価格の範囲](../catalog/catalog-price-scope.md).

郵便番号などの一部の設定は、システム全体で同じ値が使用されるので、グローバルスコープを持ちます。 The [web サイト](../stores-purchase/stores.md#add-websites) スコープは、すべてのストアとそのビューを含む、階層のそのレベル以下のすべてのストアに適用されます。 範囲を持つ項目 [ストア表示](../stores-purchase/store-views.md) は、ストアビューごとに異なる方法で設定できます。これは、通常、複数の言語をサポートするために使用されます。 設定のデフォルト値を上書きするには、 [範囲の設定](../configuration-reference/scope-change.md#set-the-scope).

ストアがで動作している場合を除く。 [シングルストアモード](#single-store-mode)の場合、各設定の範囲は、フィールドラベルの下の小さなテキストに表示されます。 インストールに複数の Web サイト、ストア、または表示が含まれる場合は、 [ストア表示](../stores-purchase/store-views.md) ここでは、変更を加える前に設定が適用されます。

![Web サイト、ストア、ストア表示の階層](./assets/scope-multisite.svg){width="550"}

| 範囲 | 説明 |
|--- |--- |
| [!UICONTROL Global] | インストール全体で使用可能なシステム全体の設定とリソース。 |
| [!UICONTROL Website] | 現在の Web サイトに限定される設定およびリソース。 各 Web サイトにはデフォルトのストアがあります。 |
| [!UICONTROL Store] | 現在のストアに限定される設定とリソース。 各ストアには、デフォルトのルートカテゴリ（メインメニュー）とデフォルトのストア表示があります。 |
| [!UICONTROL Store View] | 現在のストア表示に限定される設定とリソース。 |

{style="table-layout:auto"}

## シングルストアモード

コマースインストールに 1 つのストアとストアの表示のみが含まれる場合は、すべてのストア表示オプションとスコープインジケーターをオフにすることで、表示を簡素化できます。 単一ストアモードは、 [ストア表示を増やす](../stores-purchase/store-views.md) 後で。

![範囲 — 単一ビュー](./assets/scope-single-view.svg){width="550"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下 **[!UICONTROL General]**&#x200B;をクリックし、ページの下部まで下にスクロールして、 **[!UICONTROL Single-Store Mode]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enable Single-Store Mode]** から `Yes`.

   ![一般設定 — シングルストアモードを有効にする](./assets/general-single-store-mode.png){width="400"}

1. クリック **[!UICONTROL Save Config]**.

1. キャッシュを更新するように求められたら、次の操作を行います。

   - 次をクリック： **[!UICONTROL Cache Management]** リンクをクリックします。

     ![システムメッセージ — キャッシュ管理](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Page Cache]** チェックボックス。

   - を使用 **[!UICONTROL Actions]** に設定 `Refresh`をクリックし、 **[!UICONTROL Submit]**
