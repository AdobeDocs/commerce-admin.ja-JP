---
title: コンテンツブロックの配置
description: コードを記述することなく、ページ上の特定の場所、および特定の製品やカテゴリーに対してもブロックを配置します
exl-id: cfc9eb2c-19c8-43f1-937d-4162b5011b8a
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/BgZJJ9DGr8KD2-6XNf3yPTjo3ulGVdp0yyrJMXHWX-4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# コンテンツブロックの配置

ブロックのページレイアウトと配置を制御するコードは、XML [ ウィジェット ](widgets.md)で記述されます。 ページ上の特定の場所にブロックを配置したり、特定の製品やカテゴリーのブロックをコードを記述することなく容易に配置できます。 すべての可能な組み合わせを覚えようとするのではなく、リストから各オプションを選択できます。

次のリストは、通常ブロックが配置されるページタイプ別の場所を示しています。 ページ上の領域の定義方法について詳しくは、[標準ページレイアウト ](page-layout.md#standard-page-layouts)を参照してください。

## カテゴリーページとCMS ページ

| ブロック参照 | 位置 |
|----------|-------- |
| [!UICONTROL Breadcrumbs] | リンクとして現在の場所を表示する多くのページの上部にあるナビゲーション補助。 パンくず参照に追加されたコンテンツは、表示されている場合、パンくずリストの右側に表示されます。 |
| [!UICONTROL Left Column] | コンテンツが左側の列に追加されます。 |
| [!UICONTROL Main Content Area] | コンテンツがメインコンテンツ領域に追加されます。 |
| [!UICONTROL My Cart Extra Actions] | 顧客がページの上部にあるカートアイコンをクリックすると、コンテンツが&#x200B;_カート小計_&#x200B;の下に表示されます。 |
| [!UICONTROL Navigation Bar] | コンテンツは、メインナビゲーションバーの下に表示されます。 |
| [!UICONTROL Page Bottom] | コンテンツは、ページの下部に表示されます。 |
| [!UICONTROL Page Footer] | コンテンツは、ページのフッターの上に表示されます。 |
| [!UICONTROL Page Header] | コンテンツは、ページのヘッダーの下に表示されます。 |
| [!UICONTROL Page Top] | コンテンツがページの上部に表示されます。 |
| [!UICONTROL Right Column] | コンテンツは右側の列に表示されます。 |
| [!UICONTROL Store Language] | コンテンツは、ヘッダーの左上隅に表示されます。 |

{style="table-layout:auto"}

## 製品ページ

| ブロック参照 | 位置 |
|----------|-------- |
| [!UICONTROL Alert URLs] | コンテンツは、商品詳細ページの商品タイトルの下に表示されます。 |
| [!UICONTROL Bottom Block Options Wrapper] | カスタムオプションを追加すると、「_カートに追加_」ボタンの下にコンテンツが表示されます。 |
| [!UICONTROL Breadcrumbs] | コンテンツはパンくずリストの右側に表示されます。ナビゲーションバーの下に表示されるパスとしてリンクを提供するナビゲーション補助です。 |
| [!UICONTROL Info Column Options Wrapper] | カスタムオプションを追加すると、コンテンツが右側に表示されます。 設定可能なオプションにも同じ場所が適用されます。 |
| [!UICONTROL Left Column] | コンテンツは左列ブロックの下に表示されます。 |
| [!UICONTROL Main Content Area] | コンテンツは、メインコンテンツ領域の下に表示されます。 |
| [!UICONTROL My Cart Extra Actions] | 顧客がページの上部にあるカートアイコンをクリックすると、コンテンツが&#x200B;_カート小計_&#x200B;の下に表示されます。 |
| [!UICONTROL Navigation Bar] | コンテンツは、メインナビゲーションバーの下に表示されます。 |
| [!UICONTROL Page Bottom] | コンテンツは、ページの下部に表示されます。 |
| [!UICONTROL Page Footer] | コンテンツは、ページのフッターの上に表示されます。 |
| [!UICONTROL Page Header] | コンテンツは、ページのヘッダーの下に表示されます。 |
| [!UICONTROL Page Top] | コンテンツがページの上部に表示されます。 |
| [!UICONTROL PayPal Express Checkout (Payflow Edition) Shortcut Wrapper] | PayPal支払い方法が有効になっている場合、コンテンツは「_PayPal購入_」ボタンの下に表示されます。 |
| [!UICONTROL PayPal Express Checkout Shortcut Wrapper] | PayPal支払い方法が有効になっている場合、コンテンツは「_PayPal購入_」ボタンの下に表示されます。 |
| [!UICONTROL Product Tags List] | コンテンツが商品タグバーの下に表示されます。 |
| [!UICONTROL Product View Extra Hint] | コンテンツは、製品の主な最高価格の下に表示されます。 |
| [!UICONTROL Right Column] | コンテンツは、右側の列ブロックの下に表示されます。 |
| [!UICONTROL Store Language] | コンテンツは、言語選択の右側に表示されます。 |
| [!UICONTROL Tags List Before] | コンテンツが&#x200B;_[!UICONTROL Add Your Tags]_フィールドの上に表示されます。 |

{style="table-layout:auto"}
