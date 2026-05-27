---
title: '[!UICONTROL Sales] > [!UICONTROL Shipping Settings]'
description: Commerce管理者の[!UICONTROL Sales] > [!UICONTROL Shipping Settings] ページで設定を確認します。
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

これらの設定の変更について詳しくは、_ストアおよび購入エクスペリエンスガイド_&#x200B;の[出荷設定](../../stores-purchase/shipping-settings.md)を参照してください。

## [!UICONTROL Origin]

![Origin](./assets/shipping-settings-origin.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Country] | web サイト | 原産地国。 |
| [!UICONTROL Region/State] | web サイト | 原産地地域または州。 |
| [!UICONTROL ZIP/Postal Code] | web サイト | 原産地住所の郵便番号 |
| [!UICONTROL City] | web サイト | 原産地都市。 |
| [!UICONTROL Street Address] | web サイト | 原産地住所。 |
| [!UICONTROL Street Address Line 2] | web サイト | 必要に応じて、原点の住所の余分な行を追加します。 |

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![配送ポリシーパラメーター](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Apply Custom Shipping Policy] | web サイト | チェックアウト時に配送ポリシーが表示されるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Shipping Policy] | ストアビュー | 配送ポリシーをテキストとして含みます。 |

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクト（Adobeで管理されるSaaS インフラストラクチャ）にのみ適用されます。"}

![配送ポリシーパラメーター](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Custom Tracking URLs] | ストアビュー | 買い物客の電子メールで送信される出荷追跡番号がリンクかプレーンテキストかを指定します。 デフォルト値の`No`は、数値がプレーンテキストであることを示します。 オプション：`Yes` / `No` |
| [!UICONTROL USPS Tracking URL] | ストアビュー | 米国郵便サービスの出荷用URL テンプレート。 |
| [!UICONTROL UPS Tracking URL] | ストアビュー | United Parcel Serviceの出荷用URL テンプレート。 |
| [!UICONTROL FedEx Tracking URL] | ストアビュー | Federal Expressの出荷用URL テンプレート。 |
| [!UICONTROL DHL Tracking URL] | ストアビュー | DHL Expressの発送用のURL テンプレート。 |

{style="table-layout:auto"}
