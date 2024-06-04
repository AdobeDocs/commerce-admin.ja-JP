---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: の設定を確認します。 [!UICONTROL Sales] &gt; [!UICONTROL Quotes] コマース管理者のページ。
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Adobe Commerce B2B をインストールして有効化すると、会社固有の機能を使用して購入体験をパーソナライズできます。 Adobe Commerce B2B は、B2B モデルと B2C モデルの両方をサポートする統合ソリューションです。 B2B 機能について詳しくは、 [Adobe Commerce B2B ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![一般](./assets/quotes-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Web サイト | 顧客が見積依頼を送信する前に必要となる、割引の後の買い物かごの小計の最小金額。 デフォルト値 `0` |
| [!UICONTROL Minimum Amount Message] | ストア表示 | 顧客が見積依頼を送信しようとしたが、最低限必要な金額を満たしていない場合に、買い物かごに表示されるメッセージ。 |
| [!UICONTROL Default Expiration Period] | Web サイト | のデフォルトの存続期間を決定します [見積もり](../../b2b/quote-price-negotiation.md) 見積もり依頼が送信された日からの期間。 オプション： `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![添付ファイル](./assets/quotes-attached-files.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | グローバル | 見積もりに添付できるファイル形式を決定します。 サポートされているデフォルト値： `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`、および `jpeg` |
| [!UICONTROL Maximum file size] | グローバル | 見積もりに添付するファイルの最大サイズを決定します。 この設定は、サーバー設定で上書きできます。 |

{style="table-layout:auto"}
