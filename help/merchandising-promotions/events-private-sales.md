---
title: プライベートセールとイベント
description: プライベートセールスやその他のカタログイベントを使用して、既存顧客へのセールスを拡大し、話題と新しいリードを生み出す方法について説明します。
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/8MvnlOp5muOQbx3b7dSKguc4wf-k47v9AtaHXu7b9pU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: bd0aa680-a881-4f35-9dcf-843b0574bc5f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# プライベートセールとイベント

{{ee-feature}}

プライベートセールスやその他のカタログイベントは、既存顧客を活用して話題や新しいリードを生み出したり、余剰在庫をオフロードしたりするための優れた方法です。 期間限定セールの作成、特定のメンバーへのセール制限、スタンドアロンのプライベートセールページの作成を行うことができます。 また、招待とイベントの詳細を定義することもできます。 VIPで提供する優れた顧客体験を通じて、ブランドロイヤルティを高め、注目を集めましょう。 会員限定セールスやプライベートセールスへの限定アクセスを提供して、ブランドロイヤルティを高めます。 また、これらの売上を利用して、過剰な商品を清算することもできます。 お客様グループは、これらの種類のメンバーのみを設定したり、VIPのセールスを設定したりする際に便利です。

![&#x200B; ストアフロントの例 – ホームページ上のイベント &#x200B;](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## イベント管理コンポーネント

- **カテゴリ** – 各イベントは、カタログの[&#x200B; カテゴリ &#x200B;](../catalog/category-create.md)に関連付けられます。

- **イベント** - イベントの販売は、開始日と終了日に基づいています。 [&#x200B; カウントダウンティッカー](#event-ticker)を使用して、残り時間を表示できます。

- **カタログイベントカルーセル** - [&#x200B; カタログイベントウィジェット &#x200B;](../content-design/widget-event-carousel.md)が設定で有効になっている場合、ストアページに開封イベントと今後のイベントのリストとして、終了日で並べ替えて配置できます。 2つ以上のイベントの終了日が同じ場合、設定で指定された順序に基づいてイベントが並べ替えられます。

- **[!UICONTROL Websites]** - カテゴリの権限は、主に[顧客グループ &#x200B;](../customers/customer-groups.md)に基づいています。

- **カテゴリ権限** - [&#x200B; カテゴリ権限](../catalog/category-permissions.md)を使用すると、特定のカテゴリで実行できる特定のアクティビティを完全に制御できます。

- **アクセス制限** - ランディングページ、ログインページ、または登録ページにリダイレクトして、サイトへのパブリック [&#x200B; アクセス &#x200B;](event-configure.md#restrict-access)を禁止します。

- **招待状** - メール メッセージは、ストアでアカウントを作成するためのリンクとともに送信されます。 アカウントの作成機能は、[招待状](invitations.md)を受け取ったユーザーのみに制限できます。

- **個人向けセールスレポート** - [個人向けセールスレポート &#x200B;](../getting-started/private-sales-reports.md)では、招待の送信先、招待された顧客、コンバージョンに関する情報が提供されます。

## イベントティッカー

ティッカーブロックには、開いているイベントのカウントダウンティッカーが表示され、今後のイベントの開始日と終了日が表示されます。 イベントが終了した場合、ティッカーには開始日と終了日が表示されます。

![&#x200B; ストアフロントの例 – イベントカルーセル &#x200B;](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

イベントに対してカテゴリーページティッカーが有効になっている場合は、カテゴリーリストの上部にティッカーブロックが表示されます。 製品ページティッカーが有効になっている場合は、カテゴリに関連付けられている製品の製品ページの上部にもティッカーブロックが表示されます。

イベントティッカーは、[&#x200B; イベントの作成時](event-create.md)に有効にできます。

![&#x200B; ストアフロントの例 – イベントサイドバー](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
