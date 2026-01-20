---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings] ページで設定を確認します。
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

これらの設定の変更について詳しくは、[&#x200B; ストアと購入エクスペリエンスガイド &#x200B;](../../stores-purchase/shipping-settings.md) の _発送設定_ を参照してください。

## [!UICONTROL Origin]

![&#x200B; 接触チャネル &#x200B;](./assets/shipping-settings-origin.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Country] | Web サイト | 元の国。 |
| [!UICONTROL Region/State] | Web サイト | 原点の領域または状態。 |
| [!UICONTROL ZIP/Postal Code] | Web サイト | 元の郵便番号。 |
| [!UICONTROL City] | Web サイト | 原点都市。 |
| [!UICONTROL Street Address] | Web サイト | POI の住所。 |
| [!UICONTROL Street Address Line 2] | Web サイト | 必要に応じて、元の住所（番地）の追加行。 |

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![&#x200B; 配送ポリシーのパラメーター &#x200B;](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Apply Custom Shipping Policy] | Web サイト | チェックアウト時に配送ポリシーが表示されるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Shipping Policy] | ストア表示 | 配送ポリシーをテキストとして含みます。 |

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE SaaS のみ &#x200B;]{type=Positive url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクトにのみ適用されます（Adobeで管理される SaaS インフラストラクチャ）。"}

![&#x200B; 配送ポリシーのパラメーター &#x200B;](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Custom Tracking URLs] | ストア表示 | 買い物客の電子メールで送信された出荷トラッキング番号がリンクかプレーンテキストかを決定します。 デフォルト値 `No` は、数値がプレーンテキストであることを示します。 オプション：`Yes` / `No` |
| [!UICONTROL USPS Tracking URL] | ストア表示 | 米国郵便サービスの出荷用の URL テンプレート。 |
| [!UICONTROL UPS Tracking URL] | ストア表示 | United Parcel Service 出荷用の URL テンプレート。 |
| [!UICONTROL FedEx Tracking URL] | ストア表示 | Federal Express 出荷用の URL テンプレート。 |
| [!UICONTROL DHL Tracking URL] | ストア表示 | DHL Express 出荷用の URL テンプレート。 |

{style="table-layout:auto"}
