---
title: 属性の入力タイプ
description: 入力可能なデータの種類と、フィールドまたは入力コントロールの形式を決定する、製品属性で使用可能な入力タイプについて説明します。
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# 属性の入力タイプ

属性は、管理者から表示されると、製品の作成時に入力するフィールドです。 属性に割り当てられる入力タイプによって、入力できるデータのタイプと、フィールドまたは入力コントロールの形式が決まります。 顧客の立場から見ると、属性は製品に関する情報を提供し、製品を購入するために入力する必要のあるオプションとデータ入力フィールドです。

## 入力タイプ

| プロパティ | 説明 |
|--- |--- |
| [!UICONTROL Text Field] | テキストの 1 行の入力フィールドです。 |
| [!UICONTROL Text Area] | 製品の説明など、テキストの段落を入力する複数行の入力フィールド。 WYSIWYG エディターを使用して、テキストをHTMLタグで書式設定したり、テキストに直接タグを入力したりできます。 |
| [!UICONTROL Text Editor] | 属性の場所にある、完全に機能するテキストエディター。 |
| [!UICONTROL Date] | 日付値を [推奨フォーマット](#date-and-time-options) および [タイムゾーン](../getting-started/store-details.md#locale-options). 日付値は、リストまたはカレンダー ( ![カレンダーアイコン](../assets/icon-calendar.png) ) をクリックします。 <br/><br/>**_注意：_**システム構成に応じて、_管理者&#x200B;_ユーザーは、フィールドに日付を直接入力したり、カレンダーやリストから日付を選択したりできます。 日付と時刻の値の指定について詳しくは、 [日付と時間のオプション](#date-and-time-options). |
| [!UICONTROL Date and Time] | 日付と時刻の値を [推奨フォーマット](#date-and-time-options) および [タイムゾーン](../getting-started/store-details.md#locale-options). 日付と時刻は、手動で入力することも、カレンダーから選択することもできます。 形式の例： MM/DD/YYYY HH:MM |
| [!UICONTROL Yes/No] | 次の定義済みオプションを含むドロップダウンリストを表示します。 `Yes` および `No`. |
| ドロップダウン | 1 つの選択のみを受け入れる値のドロップダウンリストを表示します。 ドロップダウン入力タイプは、 [設定可能な製品](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | 複数の選択を受け入れる値のドロップダウンリストを表示します。 |
| [!UICONTROL Price] | この入力タイプは、事前定義された属性に加えて、価格フィールドを作成するために使用されます。 `Price`, `Special Price`, `Tier Price`、および `Cost`. 使用される通貨は、システム設定によって決まります。 |
| [!UICONTROL Media Image] | 特別な画像を製品（製品のロゴ、ケアの指示、食品ラベルの材料など）に関連付けます。 メディアイメージ属性を製品の属性セットに追加すると、追加のイメージタイプになり、ベース、小、サムネールと共に表示されます。 メディア画像属性は、 [storefront メディアブラウザー](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | 以下を定義できます。 [FPT レート](../stores-purchase/fixed-product-tax.md) ロケールの要件に基づきます。 |
| [!UICONTROL Visual Swatch] | 設定可能なプロダクトの色、テクスチャ、またはパターンを示すスウォッチを表示します。 A [ビジュアルスウォッチ](swatches.md) は 16 進数のカラー値で塗りつぶすことも、アップロードした画像を表示してオプションの色、素材、テクスチャまたはパターンを表すこともできます。 |
| [!UICONTROL Text Swatch] | サイズに頻繁に使用される、設定可能な製品オプションのテキストベースの表現です。 [テキストスウォッチ](swatches.md) には、16 進数のカラー値を含めることもできます。 |
| [!UICONTROL Page Builder] | A [[!DNL Page Builder]](../page-builder/workspace.md) ワークスペース（製品ページに魅力的なコンテンツを簡単に追加できる属性の場所） |

{style="table-layout:auto"}

## 日付と時間のオプション

日付および時間フィールドの形式をカスタマイズし、データ入力に使用する入力コントロールを選択できます。 日付値は、ドロップダウンリストまたはポップアップカレンダーから選択できます。

![例 — ストアフロントポップアップカレンダー](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_日付/時間フィールドの形式を設定するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** をクリックし、 **[!UICONTROL Catalog]** サブ項目。

1. を展開します。 **[!UICONTROL Date & Time Custom Options]** 」セクションに入力します。

   ![カタログ設定 — 日付と時間のオプション](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   これらのオプションの詳細な一覧については、 [_日付と時刻のカスタムオプション_](../configuration-reference/catalog/catalog.md) （内） _設定リファレンス_.

1. 日付フィールドの入力コントロールとしてポップアップカレンダーを使用するには、 **[!UICONTROL Use JavaScript Calendar]** から `Yes`.

1. 次の手順で **[!UICONTROL Date Fields Order]**、必要に応じて、日付フィールドの各部分の順序を設定します。

   - 月
   - 日
   - 年

1. 希望の時間形式を設定するには、 **時間形式** を次のいずれかに変更します。

   - `12h AM/PM`
   - `24h`

1. 次の手順で **[!UICONTROL Year Range]** ドロップダウン値に年 (YYYY) を入力して、 **[!UICONTROL from]** および **[!UICONTROL to]** 日付。

   空白の場合、フィールドはデフォルトで現在の年に設定されます。

1. 完了したら、「 **[!UICONTROL Save Config]**.
