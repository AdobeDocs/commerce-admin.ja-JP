---
title: 属性入力タイプ
description: 入力できるデータのタイプとフィールドまたは入力コントロールの形式を決定する、製品属性で使用できる入力タイプについて説明します。
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# 属性入力タイプ

管理者から表示する場合、属性は製品の作成時に入力するフィールドです。 属性に割り当てられる入力タイプによって、入力できるデータのタイプと、フィールドまたは入力コントロールの形式が決まります。 属性は、顧客の観点から見ると、製品に関する情報を提供します。また、製品を購入するために入力する必要があるオプションとデータ入力フィールドです。

## 入力タイプ

| プロパティ | 説明 |
|--- |--- |
| [!UICONTROL Text Field] | テキストの 1 行入力フィールド。 |
| [!UICONTROL Text Area] | 製品の説明など、テキストの段落を入力するための複数行の入力フィールド。 WYSIWYG エディターを使用して、HTMLタグでテキストの書式を設定したり、テキストにタグを直接入力したりできます。 |
| [!UICONTROL Text Editor] | 属性の場所に完全に機能するテキストエディター。 |
| [!UICONTROL Date] | 日付値を [ 優先形式 ](#date-and-time-options) および [ タイムゾーン ](../getting-started/store-details.md#locale-options) で表示します。 日付値は、リストまたはカレンダー（![ カレンダーアイコン ](../assets/icon-calendar.png)）から選択できます。 <br/><br/>**_メモ：_**&#x200B;システムの設定に応じて、_ 管理者 _ユーザーはフィールドに日付を直接入力したり、カレンダーやリストから日付を選択したりできます。 日付と時刻の値を指定する方法については、[ 日付と時刻のオプション ](#date-and-time-options) を参照してください。 |
| [!UICONTROL Date and Time] | 日付と時刻の値を [ 優先形式 ](#date-and-time-options) および [ タイムゾーン ](../getting-started/store-details.md#locale-options) で表示します。 日時は、手動で入力することも、カレンダーから選択することもできます。 形式の例：MM/DD/YYYY HH:MM |
| [!UICONTROL Yes/No] | `Yes` と `No` の定義済みオプションを含むドロップダウン リストを表示します。 |
| ドロップダウン | 1 つの選択のみを受け入れる値のドロップダウン リストを表示します。 ドロップダウン入力タイプは、[ 設定可能な製品 ](../catalog/product-create-configurable.md) の主要コンポーネントです。 |
| [!UICONTROL Multiple Select] | 複数の値を選択できるドロップダウン リストを表示します。 |
| [!UICONTROL Price] | この入力タイプは、事前定義済みの属性（`Price`、`Special Price`、`Tier Price`、`Cost`）に加えて価格フィールドを作成するために使用されます。 使用する通貨は、システム設定によって決まります。 |
| [!UICONTROL Media Image] | 製品ロゴ、ケアの説明、食品ラベルの材料など、製品に追加の画像を関連付けます。 メディア画像属性を製品の属性セットに追加すると、ベース、小、サムネールと共に、追加の画像タイプになります。 メディア画像属性は、[ ストアフロントメディアブラウザー ](catalog-images-video.md#storefront-media-browser) から除外できます。 |
| [!UICONTROL Fixed Product Tax] | ロケールの要件に基づいて [FPT 率 ](../stores-purchase/fixed-product-tax.md) を定義できます。 |
| [!UICONTROL Visual Swatch] | 設定可能な商品のカラー、テクスチャ、パターンを示すスウォッチが表示されます。 [ 視覚的なスウォッチ ](swatches.md) には、16 進数カラー値を入力するか、オプションのカラー、マテリアル、テクスチャまたはパターンを表すアップロード済み画像を表示できます。 |
| [!UICONTROL Text Swatch] | サイズ調整によく使用される、設定可能な商品オプションのテキストベースの表現です。 [ テキストスウォッチ ](swatches.md) には、16 進数のカラー値を含めることもできます。 |
| [!UICONTROL Page Builder] | 魅力的なコンテンツを製品ページに簡単に追加できる、属性の場所にある [[!DNL Page Builder]](../page-builder/workspace.md) ワークスペース。 |

{style="table-layout:auto"}

## 日付と時刻のオプション

日付と時刻のフィールドの形式をカスタマイズし、データ入力に使用する入力コントロールを選択できます。 日付の値は、ドロップダウンリストまたはポップアップカレンダーから選択できます。

![ 例 – ストアフロントのポップアップカレンダー ](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_日付/時間フィールドをフォーマットするには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、「**[!UICONTROL Catalog]**」サブアイテムをクリックします。

1. 「**[!UICONTROL Date & Time Custom Options]**」セクションを展開します。

   ![ カタログの設定 – 日付と時刻のオプション ](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、[_設定リファレンス_](../configuration-reference/catalog/catalog.md) の _日付と時刻のカスタムオプション_ を参照してください。

1. 日付フィールドの入力コントロールとしてポップアップ カレンダーを使用するには、**[!UICONTROL Use JavaScript Calendar]** を `Yes` に設定します。

1. **[!UICONTROL Date Fields Order]** を確立するには、必要に応じて日付フィールドの各部分の順序を設定します。

   - 月
   - 日
   - 年

1. 希望する時間形式を設定するには、**時間形式** を次のいずれかに設定します。

   - `12h AM/PM`
   - `24h`

1. ドロップダウン値の **[!UICONTROL Year Range]** を指定するには、年（YYYY）を入力して **[!UICONTROL from]** 日と **[!UICONTROL to]** 日を設定します。

   空白の場合、フィールドのデフォルト値は現在の年になります。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
