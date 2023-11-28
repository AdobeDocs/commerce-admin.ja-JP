---
title: '[!UICONTROL General] &gt; [!UICONTROL B2B Features]'
description: 次のページで設定を確認します： [!UICONTROL General] &gt; [!UICONTROL B2B Features] コマース管理のページ。
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Adobe Commerce向け B2B のインストールと有効化により、企業固有の機能で購入エクスペリエンスをパーソナライズできます。 Adobe Commerce用 B2B は、B2B モデルと B2C モデルの両方をサポートする統合ソリューションです。 B2B 機能の詳細については、 [_B2B for Adobe Commerceユーザーガイド_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## [!UICONTROL B2B Features]

![B2B 機能](./assets/b2b-features.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | Web サイト | 有効にすると、顧客は自分のアカウントダッシュボードから会社の割り当てを管理でき、デフォルトで共有カタログと B2B 見積もり機能も有効になります。 オプション： `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | Web サイト | 有効にすると、顧客とゲストは SKU または製品名に基づいて迅速に注文を行うことができます。 オプション： `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | Web サイト | 有効にすると、顧客は自分のアカウントダッシュボードから購買依頼リストを作成および管理できます。 |

{:style=&quot;table-layout:auto&quot;}

![会社および共有カタログを有効にした B2B 機能](./assets/b2b-features-company-enabled.png)<!-- zoom -->

「会社」機能を有効にすると、共有カタログと B2B 見積もりに追加のフィールドを使用できます。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--------------------------------------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | Web サイト | を有効にすると、カスタム価格で、グローバルに、または特定の会社に限定して使用できる、キュレーションされたカタログを作成できます。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | Web サイト | 次の場合に _[!UICONTROL Enable Shared Catalog]_フィールドが `Yes`の場合、このオプションを使用できます。 有効にすると、共有カタログに割り当てられている製品のみが価格指数に保存されます。 共有カタログに割り当てられていない商品は、ストアフロントには表示されません。 オプション： `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | Web サイト | 有効にすると、会社の購入者は買い物かごから見積もりのリクエストを送信できます。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Default B2B Payment Methods]

![B2B 構成 — デフォルトの支払い方法設定](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

|[!UICONTROL Applicable Payment Methods]|Global|B2B 購入者が利用できる支払い方法の選択を決定します。 オプション： `All Payment Methods` / `Specific Payment Methods`| |[!UICONTROL Payment Methods]|Global|B2B 購入者が利用できる各支払い方法を指定します。|

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Default B2B Shipping Methods]

![B2B 設定 — デフォルトの発送方法](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

|[!UICONTROL Applicable Shipping Methods]|Global|B2B 購入者に対してデフォルトで使用可能な発送方法の選択を決定します。 オプション： `All Shipping Methods` / `Specific Shipping Methods`| |[!UICONTROL Shipping Methods]|Global|B2B 購入者がデフォルトで使用できる各発送方法を指定します。 <br/>**_注意：_**また、特定の [会社アカウント](../../b2b/account-companies.md).|

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Order Approval Configuration]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | Web サイト | 有効にすると、会社は発注書を作成できます。 オプション： `Yes` / `No` |

![B2B 機能 — 注文の承認設定](./assets/b2b-features-order-approval.png)<!-- zoom -->

{:style=&quot;table-layout:auto&quot;}
