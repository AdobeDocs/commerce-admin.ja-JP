---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: Commerce管理者の[!UICONTROL Sales] > [!UICONTROL Quotes] ページで設定を確認します。
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Adobe Commerce B2Bのインストールと有効化により、企業固有の機能を使用して購買体験をパーソナライズできます。 Adobe Commerce B2Bは、B2BとB2Cの両方のモデルをサポートする統合ソリューションです。 B2B機能について詳しくは、[Adobe Commerce B2B ユーザーガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=ja)を参照してください。

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/ja/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![一般](./assets/quotes-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | web サイト | お客様が見積もり依頼を送信する前に必要な、割引の後のショッピングカートの小計の最小金額。 デフォルト値：`0` |
| [!UICONTROL Minimum Amount Message] | ストアビュー | 顧客が見積もり依頼を送信しようとしたが、必要な最小金額が満たされていない場合に、ショッピングカートに表示されるメッセージ。 |
| [!UICONTROL Default Expiration Period] | web サイト | 見積の要求が送信された日からの期間として、[見積](../../b2b/quote-price-negotiation.md)の既定の有効期間を指定します。 オプション：`Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![添付ファイル &#x200B;](./assets/quotes-attached-files.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | グローバル | 見積書に添付できるファイル形式を指定します。 サポートされているデフォルト値：`doc`、`docx`、`xls`、`xlsx`、`pdf`、`txt`、`jpg`、`png`、および`jpeg` |
| [!UICONTROL Maximum file size] | グローバル | 見積書に添付されているファイルの最大サイズを指定します。 この設定は、サーバー設定で上書きできます。 |

{style="table-layout:auto"}
