---
title: 属性入力タイプ
description: 製品属性で使用できる入力タイプについて説明します。入力できるデータのタイプと、フィールドまたは入力コントロールの形式を決定します。
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/8WwqU3ZSqmORqSD2061Pa5MTRqYbH71dOxouz-nLwbo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 780
ht-degree: 0%

---

# 属性入力タイプ

管理者から表示される属性は、製品の作成時に入力するフィールドです。 属性に割り当てられる入力タイプによって、入力できるデータのタイプと、フィールドまたは入力コントロールの形式が決まります。 顧客の観点からは、属性は製品に関する情報を提供し、製品を購入するために必要なオプションとデータ入力フィールドです。

## 入力タイプ

| プロパティ | 説明 |
|--- |--- |
| [!UICONTROL Text Field] | テキストの1行入力フィールド。 |
| [!UICONTROL Text Area] | 製品説明などのテキストの段落を入力するための複数行入力フィールド。 WYSIWYG エディターを使用して、HTML タグを使用してテキストを書式設定したり、タグをテキストに直接入力したりできます。 |
| [!UICONTROL Text Editor] | 属性の場所に完全に機能するテキストエディター。 |
| [!UICONTROL Date] | [優先形式](#date-and-time-options)および[ タイムゾーン ](../getting-started/store-details.md#locale-options)に日付値を表示します。 日付値は、リストまたはカレンダー（![ カレンダーアイコン ](../assets/icon-calendar.png)）から選択できます。 <br/><br/>**_Note:_**システム構成に応じて、_&#x200B;管理者_ ユーザーは日付をフィールドに直接入力するか、カレンダーまたはリストから日付を選択できます。 日付と時刻の値の指定について詳しくは、[日付と時刻のオプション ](#date-and-time-options)を参照してください。 |
| [!UICONTROL Date and Time] | [優先形式](#date-and-time-options)および[ タイムゾーン ](../getting-started/store-details.md#locale-options)の日時の値を表示します。 日付と時刻は手動で入力することも、カレンダーから選択することもできます。 形式の例：MM/DD/YYYYY HH:MM |
| [!UICONTROL Yes/No] | `Yes`と`No`の事前定義済みオプションを含むドロップダウンリストを表示します。 |
| ドロップダウン | 1つの選択のみを受け入れる値のドロップダウンリストを表示します。 ドロップダウン入力タイプは、[設定可能な製品](../catalog/product-create-configurable.md)の主要コンポーネントです。 |
| [!UICONTROL Multiple Select] | 複数の選択を受け入れる値のドロップダウンリストを表示します。 |
| [!UICONTROL Number] [!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクト（Adobeが管理するSaaS インフラストラクチャ）にのみ適用されます。"} | 10進数値を格納する数値入力フィールド。 **Price**&#x200B;入力タイプとは異なり、通貨の書式設定は適用されず、負の値を受け入れます。 この入力タイプは、測定、寸法、または温度範囲などの技術仕様に使用します。 |
| [!UICONTROL Price] | この入力タイプは、定義済みの属性`Price`、`Special Price`、`Tier Price`、`Cost`に加えて、価格フィールドを作成するために使用されます。 使用される通貨は、システム設定によって決まります。 |
| [!UICONTROL Media Image] | 商品ロゴ、ケア手順、食品ラベルの材料など、商品に追加の画像を関連付けます。 製品の属性セットにメディア画像属性を追加すると、追加の画像タイプとなり、ベース、スモール、サムネールが追加されます。 メディア画像の属性は、[ ストアフロントメディアブラウザー](catalog-images-video.md#storefront-media-browser)から除外できます。 |
| [!UICONTROL File] [!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクト（Adobeが管理するSaaS インフラストラクチャ）にのみ適用されます。"} | ファイルをアップロードし、製品属性に関連付けることができます。 サポートされているファイルの種類と最大ファイルサイズは、[製品ファイル属性](../configuration-reference/catalog/product-file-attributes.md)で設定されています。 この入力タイプは、製品マニュアル、仕様書、証明書などの文書に使用します。 |
| [!UICONTROL Fixed Product Tax] | ロケールの要件に基づいて[FPT レート ](../stores-purchase/fixed-product-tax.md)を定義できます。 |
| [!UICONTROL Visual Swatch] | 設定可能な製品のカラー、テクスチャ、パターンを示すスウォッチを表示します。 [ ビジュアルスウォッチ ](swatches.md)には、16進数のカラー値を入力するか、オプションのカラー、マテリアル、テクスチャ、パターンを表すアップロードされた画像を表示できます。 |
| [!UICONTROL Text Swatch] | サイズに頻繁に使用される、設定可能な製品オプションのテキストベースの表現。 [ テキストスウォッチ ](swatches.md)には、16進数のカラー値も含めることができます。 |
| [!UICONTROL Page Builder] | 属性の場所に[[!DNL Page Builder]](../page-builder/workspace.md) ワークスペースがあり、魅力的なコンテンツを製品ページに簡単に追加できます。 |

{style="table-layout:auto"}

## 日付と時刻のオプション

日時フィールドの形式をカスタマイズし、データ入力に使用する入力コントロールを選択できます。 日付の値は、ドロップダウンリストまたはポップアップカレンダーから選択できます。

![例 – ストアフロントポップアップカレンダー](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_日付/時刻フィールドを書式設定する:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Catalog]**&#x200B;を展開し、**[!UICONTROL Catalog]** サブアイテムをクリックします。

1. **[!UICONTROL Date & Time Custom Options]** セクションを展開します。

   ![ カタログ設定 – 日時オプション ](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、_設定リファレンス_&#x200B;の&#x200B;[_日時カスタムオプション_](../configuration-reference/catalog/catalog.md)&#x200B;を参照してください。

1. ポップアップカレンダーを日付フィールドの入力コントロールとして使用するには、**[!UICONTROL Use JavaScript Calendar]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Date Fields Order]**&#x200B;を確立するには、必要に応じて日付フィールドの各部分の順序を設定します。

   - 月
   - 日
   - 年

1. 好みの時間形式を設定するには、**時間形式**&#x200B;を次のいずれかに設定します。

   - `12h AM/PM`
   - `24h`

1. ドロップダウン値の&#x200B;**[!UICONTROL Year Range]**&#x200B;を設定するには、年（YYYY）を入力して&#x200B;**[!UICONTROL from]**&#x200B;と&#x200B;**[!UICONTROL to]**&#x200B;の日付を設定します。

   空白の場合、フィールドのデフォルトは現在の年になります。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

