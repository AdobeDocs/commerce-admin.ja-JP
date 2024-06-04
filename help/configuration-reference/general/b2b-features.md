---
title: '[!UICONTROL General] &gt; [!UICONTROL B2B Features]'
description: の設定を確認します。 [!UICONTROL General] &gt; [!UICONTROL B2B Features] コマース管理者のページ。
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Adobe Commerce B2B をインストールして有効化すると、会社固有の機能を使用して購入体験をパーソナライズできます。 Adobe Commerce B2B は、B2B モデルと B2C モデルの両方をサポートする統合ソリューションです。 B2B 機能について詳しくは、 [_Adobe Commerce B2B ユーザーガイド_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## [!UICONTROL B2B Features]

![B2B の機能](./assets/b2b-features.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | Web サイト | 有効にすると、顧客はアカウントダッシュボードから会社の割り当てを管理でき、デフォルトでカタログ共有機能と B2B 見積機能も有効になります。 オプション： `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | Web サイト | 有効にすると、顧客およびゲストは SKU または製品名に基づいてすばやく注文できるようになります。 オプション： `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | Web サイト | 有効化すると、顧客は自分のアカウントダッシュボードから購買依頼リストを作成および管理できます。 |

{style="table-layout:auto"}

![会社と共有カタログを有効にした B2B 機能](./assets/b2b-features-company-enabled.png)<!-- zoom -->

会社機能が有効になっている場合、追加のフィールドを共有カタログと B2B 見積もりに使用できます。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | Web サイト | 有効にすると、グローバルに利用できる、または特定の会社に限定して利用できるカスタム価格のキュレートされたカタログを作成できます。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | Web サイト | いつ _[!UICONTROL Enable Shared Catalog]_フィールドの設定： `Yes`、このオプションは使用できます。 有効にすると、共有カタログに割り当てられた製品のみが価格インデックスに保存されます。 共有カタログに割り当てられていない製品は、ストアフロントに表示されません。 オプション： `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | Web サイト | これを有効にすると、会社の購入者は、買い物かごから見積依頼を送信できるようになります。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![B2B 設定 – デフォルトの支払方法設定](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | グローバル | B2B 購入者が使用できる支払い方法の選択を決定します。 オプション： `All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | グローバル | B2B 購入者が使用できる各支払方法を指定します。 |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![B2B 設定 – デフォルトの発送方法](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | グローバル | B2B 購入者がデフォルトで使用できる発送方法の選択を決定します。 オプション： `All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | グローバル | B2B 購入者がデフォルトで使用できる各発送方法を指定します。 <br/>**_注意：_**また、特定のの発送方法を制限することもできます [会社アカウント](../../b2b/account-companies.md). |

{style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

![B2B の機能 – 注文の承認設定](./assets/b2b-features-order-approval.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | Web サイト | 有効化すると、企業は発注書を作成できるようになります。 オプション： `Yes` / `No` |

{style="table-layout:auto"}


