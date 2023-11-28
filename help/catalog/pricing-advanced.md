---
title: 高度な価格
description: Adobe Commerceで使用できる高度な価格コントロールについて説明します。
exl-id: 0f353341-1b6b-4093-bba9-4a1b88323f8a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# 高度な価格

Adobe CommerceとMagento Open Sourceは、プロモーションや製造元が提供する最小広告価格要件を満たすために使用できる様々な価格オプションをサポートしています。 製品価格の変更は、スケジュールに従って、または製品レベルまたは買い物かごに適用される価格ルールに従っておこなうことができます。

高度な価格で製品の価格を管理し、顧客がより多くの消費を促し、サイトへのトラフィックを促進し、古い在庫を消去するより高い料金を提供します。

The _[!UICONTROL Advanced Pricing]_設定は、特定の顧客グループまたは共有カタログで使用できる特別な価格設定に必要な条件を定義します。 高度な価格設定は、シンプル、仮想、ダウンロード可能、バンドル製品に適用できます。 他の製品タイプに割引価格を適用するには、 [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md). 詳しくは、 [価格範囲](catalog-price-scope.md).

高度な価格データは製品ページと同期されます。 例えば、階層価格数量を更新すると、製品ページの値が更新されます。

![Adobe Commerce用 B2B](../assets/b2b.svg) （で使用可能） [Adobe Commerce用 B2B](./b2b/../introduction.md) のみ ) 共有カタログを使用している場合、高度な価格データは、製品ページと共有カタログの両方と同期されます。 例えば、階層価格数量を更新すると、共有カタログと製品ページの値が更新されます。 共有カタログに表示されるカスタム価格は、顧客グループの価格よりも優先されます。 また、 [共有カタログの価格と構造を設定](https://experienceleague.adobe.com/docs/commerce-admin/b2b/shared-catalogs/define/catalog-shared-pricing-structure.html) （内） _B2B for Adobe Commerceガイド_.

![高度な価格](./assets/product-pricing-advanced-link.png){width="600" zoomable="yes"}

## 高度な価格オプションへのアクセス

1. 製品を編集モードで開きます。

1. の下 **[!UICONTROL Price]**&#x200B;をクリックし、 **[!UICONTROL Advanced Pricing]**.

1. 必要なアドバンスド価格のタイプに関する手順に従います。

   - [グループ価格](product-price-group.md)

   - [特別価格](product-price-special.md)

   - [価格帯](product-price-tier.md)

   - [最小広告価格](product-price-minimum-advertised.md)

## ページ参照

### [!UICONTROL Special Price]

指定した期間または予定キャンペーン中に割引価格を提供するには、特別価格を入力します。 特別価格が利用可能な場合、小売価格が消去され、特別価格は大きな太字のテキストで下に表示されます。

#### [!UICONTROL Special Price From] 日付

{{ce-feature}}

| フィールド | 説明 |
| ---- | ----------- |
| [!UICONTROL From] | 特別価格が利用可能な最初の日付を設定します。 日付を入力するか、カレンダーから選択できます。 |
| [!UICONTROL To] | 特別価格が利用可能な最終日を設定します。 日付を入力するか、カレンダーから選択できます。 |

{style="table-layout:auto"}

### [!UICONTROL Cost]

品目の実際の原価を入力します。

### [!UICONTROL Customer Group Price]

![高度な価格](./assets/product-pricing-advanced-group-price.png){width="600" zoomable="yes"}

特定の顧客グループに対して、プロモーションと階層別の価格を設定します。

| 項目 | 説明 |
| ---- | ----------- |
| [!UICONTROL Website] | グループ価格ルールが適用される Web サイトを識別します。 このオプションは、インストールに複数の Web サイトがある場合にのみ表示されます。 |
| [!UICONTROL Customer Group] | （必須）割引価格の受け取りに適合する顧客グループを識別します。 グループまたはカタログフィールドの値が変更されると、前の設定と一致した対応するカスタム価格行が共有カタログから削除されます。 <br/>**[!UICONTROL ALL GROUPS]**— すべての顧客グループにルールを適用します。<br/>**[!UICONTROL NOT LOGGED IN]**  — 自分のアカウントにログインしていないゲストおよび顧客にルールを適用します。 |
| [!UICONTROL Quantity] | 階層価格を受け取るために必要な数量を指定します。 |
| [!UICONTROL Price] | （必須）特定の Web サイト内で、顧客グループのメンバーに対して固定または割引の製品価格を指定します。 オプション： <br/>**[!UICONTROL Fixed]**- （デフォルト）割引価格は固定小数値で入力されます。 例えば、 `9.99` 割引価格として。<br/>**[!UICONTROL Discount]**  — 割引価格は、基本製品価格のパーセンテージ (%) として入力されます。 例えば、 `10` 10%の割引を受ける場合。 |
| ![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png) | 現在のルールを削除します。 |
| **[!UICONTROL Add]** | 新しいルール用に別の行を挿入します。 |

{style="table-layout:auto"}

### [!UICONTROL Catalog and Tier Price]

特定の共有カタログおよび顧客グループのプロモーションおよび階層別の価格を設定します。

{{b2b-feature}}

![共有カタログを使用する B2B ストアの高度な価格設定](./assets/product-pricing-advanced.png){width="600" zoomable="yes"}

| 項目 | 説明 |
|----|-----------|
| [!UICONTROL Website] | グループ価格ルールが適用される Web サイトを識別します。 このオプションは、インストールに複数の Web サイトがある場合にのみ表示されます。 <br>**_重要：_**A-So 選択_Web サイト&#x200B;_（内） [カタログ価格範囲](catalog-price-scope.md) 設定を使用しない場合は、設定された高度な価格が**すべて&#x200B;**web サイト。 |
| [!UICONTROL Group or Catalog] | （必須）割引価格の受け取りに適合する顧客グループまたは共有カタログを識別します。 グループまたはカタログフィールドの値が変更されると、前の設定と一致した対応するカスタム価格行が共有カタログから削除されます。 <br/>**[!UICONTROL ALL GROUPS]**— すべての顧客グループにルールを適用します。 この値は共有カタログに適用されず、高度な価格データの変更は共有カタログには同期されません。<br/>**[!UICONTROL NOT LOGGED IN]**  — 自分のアカウントにログインしていないゲストおよび顧客にルールを適用します。<br/>**[!UICONTROL Shared Catalogs]**— 特定の共有カタログにルールを適用します。 |
| 数量 | 階層価格を受け取るために必要な数量を指定します。 |
| [!UICONTROL Price] | （必須）特定の Web サイト内で、顧客グループのメンバーに対して固定または割引の製品価格を指定します。 オプション： <br/>**[!UICONTROL Fixed]**- （デフォルト）割引価格は固定小数値で入力されます。 例えば、 `9.99` 割引価格として。<br/>**[!UICONTROL Discount]**  — 割引価格は、基本製品価格のパーセンテージ (%) として入力されます。 例えば、 `10` 10%の割引を受ける場合。 |
| ![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png) | 現在のルールを削除します。 |
| **[!UICONTROL Add]** | 新しいルール用に別の行を挿入します。 |

{style="table-layout:auto"}

### [!UICONTROL Minimum Advertised Price]

製品の最小アドバタイズ価格 (MAP) です。

### [!UICONTROL Display Actual Price]

実際の製品価格を顧客に表示する場所を決定します。

| 項目 | 説明 |
|----|-----------|
| [!UICONTROL Use Config] | 価格表示の現在の構成設定を使用します。 |
| [!UICONTROL On Gesture] | ポップアップに実際の製品価格を表示します ( _クリックして価格_ または _これは何だ？_ リンク。 |
| [!UICONTROL In Cart] | 買い物かごの実際の製品価格を表示します。 |
| [!UICONTROL Before Order Confirmation] | 注文が送信される直前の、チェックアウトプロセスの最後の実際の製品価格を表示します。 |

{style="table-layout:auto"}
