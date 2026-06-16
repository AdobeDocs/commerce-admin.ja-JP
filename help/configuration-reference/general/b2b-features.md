---
title: '[!UICONTROL General] > [!UICONTROL B2B Features]'
description: Commerce管理者の[!UICONTROL General] > [!UICONTROL B2B Features] ページで設定を確認します。
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
TQID: https://experienceleague.adobe.com/s9-xEtVsEhdegXaObYrfbu-tSvvcqlXVagEw4QJejlk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 347
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Adobe Commerce B2Bのインストールと有効化により、企業固有の機能を使用して購買体験をパーソナライズできます。 Adobe Commerce B2Bは、B2BとB2Cの両方のモデルをサポートする統合ソリューションです。 B2B機能について詳しくは、[_Adobe Commerce B2B ユーザーガイド_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html)を参照してください。

## [!UICONTROL B2B Features]

![B2B機能](./assets/b2b-features.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | web サイト | 有効にすると、顧客はアカウントダッシュボードから会社の割り当てを管理でき、デフォルトでは共有カタログとB2B見積もり機能も有効になります。 オプション：`Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | web サイト | 有効にすると、顧客とゲストはSKUまたは製品名に基づいて注文をすばやく行うことができます。 オプション：`Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | web サイト | 有効にすると、顧客はアカウントダッシュボードから購買グループを作成および管理できます。 |

{style="table-layout:auto"}

企業および共有カタログを有効にした![B2B機能](./assets/b2b-features-company-enabled.png)<!-- zoom -->

会社の機能が有効になっている場合、共有カタログとB2B見積に追加のフィールドを使用できます。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | web サイト | 有効にすると、グローバルまたは特定の企業に限定されたカスタム価格設定で厳選されたカタログを作成できるようになります。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | web サイト | _[!UICONTROL Enable Shared Catalog]_&#x200B;フィールドが`Yes`に設定されている場合、このオプションを使用できます。 有効にすると、共有カタログに割り当てられている製品のみが価格インデックスに保存されます。 共有カタログに割り当てられていない製品は、ストアフロントに表示されません。 オプション：`Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | web サイト | 有効にすると、会社のバイヤーがショッピングカートから見積もり依頼を送信できるようになります。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![B2B設定 – デフォルトの支払い方法の設定](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | グローバル | B2B バイヤーが利用できる支払い方法の選択を決定します。 オプション：`All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | グローバル | B2B バイヤーが利用できる各支払い方法を指定します。 |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![B2B設定 – デフォルトの配送方法](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | グローバル | デフォルトでB2B バイヤーが利用できる配送方法の選択を決定します。 オプション：`All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | グローバル | デフォルトでB2B バイヤーが利用できる各配送方法を指定します。 <br/>**_Note:_**&#x200B;特定の[会社アカウント &#x200B;](../../b2b/account-companies.md)の配送方法を制限することもできます。 |

{style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

![B2B機能 – 注文承認設定](./assets/b2b-features-order-approval.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | web サイト | 有効にすると、会社は発注を作成できます。 オプション：`Yes` / `No` |

{style="table-layout:auto"}


