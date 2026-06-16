---
title: '[!UICONTROL Sales] > [!UICONTROL Shipping Settings]'
description: Commerce管理者の[!UICONTROL Sales] > [!UICONTROL Shipping Settings] ページで設定を確認します。
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
TQID: https://experienceleague.adobe.com/4-Kmcd3F8pQyMgxp-NmkBFVNuEXWuYn-BOzpvxuFMhU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 204
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
