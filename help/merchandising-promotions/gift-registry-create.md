---
title: ギフト レジストリの設定
description: ストア顧客のギフトレジストリタイプを設定する方法を説明します。
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# ギフト レジストリの設定

{{ee-feature}}

ギフトレジストリは、結婚式、誕生日、記念日、新しい赤ちゃん、またはその他の特別な機会など、あらゆる種類のイベントに対して作成できます。 Adobe Commerceには、デフォルトで次のような特別なイベントが含まれています。

- 赤ちゃん
- 誕生日
- 結婚式

レジストリを作成すると、顧客のアカウントにあるギフト レジストリの種類の一覧のオプションになります。

3 つのギフト レジストリのいずれかを使用するか、独自のカスタム レジストリを作成できます。 各ギフトレジストリタイプには、複数の属性が含まれます。これらは、顧客がギフトレジストリを作成するために入力するデータ入力フィールドです。 属性は、イベント、時間、場所に関する追加情報、または必要なその他の情報を提供します。 入力タイプに応じて、一部の属性には複数のオプションがあります。 例： `Wedding` ギフト レジストリの種類には属性があります `Role`、を含む `Bride`, `Groom`、および `Partner` オプション。 属性と入力タイプについて詳しくは、を参照してください。 [属性](../customers/attribute-properties.md).

![ギフト レジストリの種類](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## 準備済みギフト レジストリの使用

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

   誕生日、結婚式、赤ちゃんのレジストリは、顧客が自分のアカウントから使用する準備ができています。

1. 必ずを完了させてください。 [メールテンプレート設定](../systems/email-templates.md#configure-email-templates)そのため、ブランドが反映されます。

## カスタムギフトレジストリの作成

1. 管理サイドバーで、に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Gift Registry Type]**.

1. 次の下 **[!UICONTROL General Information]**、以下を完了します。

   - 一意のを入力 **[!UICONTROL Code]** ギフトレジストリを内部的に識別します。

     コードは小文字で始める必要があります。 残りのコードは、小文字（a ～ z）、数字（0 ～ 9）、アンダースコア（`_`）に設定します。

   - の場合 **[!UICONTROL Label]**、ストアに表示するギフトレジストリの名前を入力します。

     このラベルは、顧客が利用できるギフト レジストリの種類の一覧のオプションです。

   - の場合 **[!UICONTROL Sort Order]**&#x200B;を入力して、このギフト レジストリが他の種類と共に一覧表示されるときの表示順序を決定します。

   - ギフト レジストリをアクティブにするには、次のように設定します **[!UICONTROL Is Listed]** 対象： `Yes`.

     ![ギフト レジストリ – 一般情報](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. ギフト レジストリの各セクションを調べて、含める情報の種類を決定します。

1. 左パネルで、を選択します。 **[!UICONTROL Attributes]** をクリックして、 **[!UICONTROL Add Attribute]**.

   ![ギフト レジストリ – 新しい属性](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. 各属性に対して、次の操作を行います。

   - 一意のを割り当て **[!UICONTROL Code]** 属性を内部的に識別する場合。 コードは最大 15 文字で、小文字で始める必要があります。 残りのコードには小文字（`a`-`z`）、数値（`0`-`9`）、およびアンダースコア（`_`）文字を使用して単語を区切ります。

   - を選択します。 **[!UICONTROL Input Type]** データ入力に使用されます。 カスタムタイプまたは静的タイプのいずれかを使用できます。

   - 入力タイプに複数のオプションがある場合は、 **[!UICONTROL Add New Option]** 各オプションの情報を入力します。

     一部の入力タイプには、追加のプロパティがあります。 例えば、「イベントの場所」には、イベントを検索可能にする追加のプロパティがあり、ストアの公開ギフトレジストリリストに含まれています。

      - を設定 **[!UICONTROL Attribute Group]** 属性を表示するギフトレジストリ内のセクションに移動します。

      - の場合 **[!UICONTROL Label]**&#x200B;を入力し、レジストリ内のデータ入力フィールドを識別する名前を入力します。

      - 顧客がフィールドで選択や値の入力を行う必要がある場合は、を設定します **[!UICONTROL Is Required]** 対象： `Yes`.

      - の場合 **[!UICONTROL Sort Order]**&#x200B;を入力して、ストアで利用可能な他のギフトレジストリと共に一覧表示されるときにこのギフトレジストリが表示される順序を決定します。

1. 別のオプションを追加するには、をクリックします **新しいオプションを追加**.

   追加された新しいオプションはそれぞれ、上部の新しいセクションに表示されます。 新しい属性に対して、このプロセスを繰り返します。

1. 完了したら、 **[!UICONTROL Save]**.

## フィールドの説明

### [!UICONTROL General Information]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Code] | ギフト レジストリの種類を内部的に識別する一意の名前。 コードの最初の文字は、小文字にする必要があります。 残りのコードは、小文字（a ～ z）、数字（0 ～ 9）、アンダースコア文字（`_`）に設定します。 |
| [!UICONTROL Label] | ストアに表示されるギフト レジストリの種類の名前。 |
| [!UICONTROL Sort Order] | このギフト レジストリの種類が他の種類と共に一覧表示されるときに表示される順序を決定します。 |
| [!UICONTROL Is Listed] | ギフト レジストリの種類がストア内の顧客に対して利用可能かどうかを決定します。 オプション： `Yes` / `No`. |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Code] | 属性を内部的に識別する一意の名前。 コードには、小文字（a ～ z）、数字（0 ～ 9）、アンダースコア文字（`_`）に設定します。 |
| [!UICONTROL Input Type] | タイプに従って、属性に関連付けられたデータのタイプと入力コントロールを決定します。 |
| [!UICONTROL Attribute Group] | ギフトレジストリに属性がリストされているグループを選択します。 |
| [!UICONTROL Label] | 顧客のアカウントダッシュボードで属性を識別する名前。 |
| [!UICONTROL Is Required] | 属性が必須エントリかどうかを示します。 ギフト レジストリは、必要な属性がすべて完了するまで保存できません。 オプション： `Yes` / `No`. |
| [!UICONTROL Sort Order] | 他の属性と一緒にリストされた場合に表示される属性のシーケンスを指定します。 |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

属性に関連付けられているデータの種類と入力コントロールを選択します。

**_[!UICONTROL Custom Types]_**

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Text] | 属性をテキストフィールドとして表示します。 |
| [!UICONTROL Select] | 属性をドロップダウンリストとして表示します。 クリック **[!UICONTROL Add New Option]** ドロップダウンリストに条件を追加するには、以下を実行します。<br/>**[!UICONTROL Code]**– 属性を内部的に識別する一意の名前。<br/>**[!UICONTROL Label]**  – 顧客のアカウントダッシュボードで属性を識別する名前。<br/>**[!UICONTROL Is Default]**– このスイッチを設定して、デフォルトの条件を選択します。<br/>**[!UICONTROL Delete Option]** - 「」をクリックすると、オプションが削除されます。 |
| [!UICONTROL Date] | 属性を日付フィールドとして表示します。 オプション： `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | 属性を国のドロップダウンリストとして表示します。 を設定 **[!UICONTROL Show Region]** コピー先： `Yes` / `No`. |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Event Date] | ストアでの date 属性の使用方法を決定します。 オプション： <br/>**[!UICONTROL Searchable]**– 属性を詳細検索に使用できるかどうかを決定します。 オプション： `Yes` / `No`.<br/>**[!UICONTROL Is Listed]** - イベントを、ストアで使用可能なイベントのリストに含めるかどうかを決定します。 オプション： `Yes` / `No`. <br/>**[!UICONTROL Date Format]**- イベント日付の形式を決定します。 オプション： `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | 属性を国のリストとして表示します。 オプション： <br/>**[!UICONTROL Searchable]**– 属性を詳細検索に使用できるかどうかを決定します。 オプション： `Yes` / `No`.<br/>**[!UICONTROL Is Listed]** - イベントを、ストアで使用可能なイベントのリストに含めるかどうかを決定します。 オプション： `Yes` / `No`. <br/>**[!UICONTROL Show Region]**- イベントの地域を決定します。 |
| [!UICONTROL Event Location] | ギフト レジストリに関連するイベントの場所。 <br/>を設定 **[!UICONTROL Is Searcheable]** コピー先： `Yes` / `No` <br/>を設定 **[!UICONTROL Is Listed]** コピー先： `Yes` / `No` |
| [!UICONTROL Role] | ギフト受取人を識別する役割。 例： `Bride`, `Groom`、または `Partner`.<br/>**[!UICONTROL Is Searcheable]**– に設定 `Yes`/ `No`<br/>**&#x200B;リストされる&#x200B;**– に設定 `Yes` / `No`<br/>**[!UICONTROL Add New Option]** - クリックすると、ドロップダウンメニューに条件がさらに追加されます。<br/>**コード**  – 属性を内部的に識別する一意の名前。<br/>**[!UICONTROL Label]**– 顧客のアカウントダッシュボードで属性を識別する名前。<br/>**[!UICONTROL Is Default]**  – このスイッチを設定して、デフォルトの条件を選択します。<br/>**[!UICONTROL Delete Option]**- 「」をクリックすると、オプションが削除されます。 |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

ギフトレジストリに属性がリストされているグループを選択します。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Event Information] | ギフト レジストリ イベント、その時刻、場所などに関する情報を追加するすべてのギフト レジストリ属性をグループ化します。 |
| [!UICONTROL Gift Registry Properties] | ギフトレジストリに関する情報を直接追加するすべての属性を結合します。 |
| [!UICONTROL Privacy Settings] | ギフト レジストリ イベントのプライバシーに関する情報を追加する属性の一覧が表示されます。 |
| [!UICONTROL Recipients Information] | ギフト レジストリを作成する人に関する情報を提供する属性をグループ化します。 |
| [!UICONTROL Shipping Address] | ギフト レジストリ イベントの配送先住所に関する情報を追加する属性を結合します。 |

{style="table-layout:auto"}
