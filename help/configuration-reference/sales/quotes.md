---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: 次のページで設定を確認します： [!UICONTROL Sales] &gt; [!UICONTROL Quotes] コマース管理のページ。
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Adobe Commerce向け B2B のインストールと有効化により、企業固有の機能で購入エクスペリエンスをパーソナライズできます。 Adobe Commerce用 B2B は、B2B モデルと B2C モデルの両方をサポートする統合ソリューションです。 B2B 機能の詳細については、 [B2B for Adobe Commerceユーザーガイド](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![一般](./assets/quotes-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Web サイト | 顧客が見積もりのリクエストを送信する前に必要な、割引後の買い物かごの小計の最小金額。 デフォルト値： `0` |
| [!UICONTROL Minimum Amount Message] | ストア表示 | 顧客が見積もりの要求を送信しようとしたが、必要な最小金額を満たしていない場合に買い物かごに表示されるメッセージ。 |
| [!UICONTROL Default Expiration Period] | Web サイト | のデフォルトの存続期間を決定します [引用](../../b2b/quote-price-negotiation.md) 見積依頼が送信された日からの期間。 オプション： `Days` / `Weeks` / `Months` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Attached Files]

![添付ファイル](./assets/quotes-attached-files.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | グローバル | 引用符に添付できるファイル形式を決定します。 サポートされるデフォルト値： `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`、および `jpeg` |
| [!UICONTROL Maximum file size] | グローバル | 見積書に添付されるファイルの最大サイズを決定します。 この設定は、サーバーの構成で上書きできます。 |

{:style=&quot;table-layout:auto&quot;}
