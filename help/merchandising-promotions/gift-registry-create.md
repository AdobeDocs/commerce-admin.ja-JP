---
title: ギフトレジストリの設定
description: 店舗の顧客に対してギフトレジストリの種類を設定する方法を説明します。
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---

# ギフトレジストリの設定

{{ee-feature}}

結婚式、誕生日、記念日、新しい赤ちゃん、その他の特別な日など、あらゆる種類のイベントに対してギフトレジストリを作成できます。 デフォルトで、Adobe Commerceには次の特別なイベントが含まれています。

- 赤ちゃん
- 誕生日
- 結婚式

レジストリを作成すると、顧客のアカウントのギフトレジストリの種類のリストのオプションになります。

3 つの用意されたギフトレジストリのいずれかを使用するか、独自のカスタムレジストリを作成できます。 各ギフトレジストリタイプには、複数の属性が含まれます。これは、顧客がギフトレジストリを作成するために完了するデータ入力フィールドです。 属性は、イベント、時間、場所、または必要なその他の情報に関する追加情報を提供します。 入力タイプに応じて、一部の属性には複数のオプションがあります。 例えば、 `Wedding` ギフトレジストリの種類に属性があります `Role`、 `Bride`, `Groom`、および `Partner` オプション。 属性と入力タイプについて詳しくは、 [属性](../customers/attribute-properties.md).

![ギフトレジストリの種類](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## 準備済みのギフトレジストリを使用

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

   誕生日、結婚式、ベビーレジストリーは、顧客が自分のアカウントで使用する準備が整っています。

1. 必ず [電子メールテンプレート設定](../systems/email-templates.md#configure-email-templates)ブランドを反映させるために使用します。

## カスタムギフトレジストリの作成

1. 管理者のサイドバーで、 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

1. 右上隅で、 **[!UICONTROL Add Gift Registry Type]**.

1. の下 **[!UICONTROL General Information]**、次の手順を実行します。

   - 一意の **[!UICONTROL Code]** 内部でギフトレジストリを識別します。

     コードの先頭には小文字を使用する必要があります。 残りのコードは、小文字 (a ～ z)、数字 (0 ～ 9)、アンダースコア (`_`) をクリックします。

   - の場合 **[!UICONTROL Label]**&#x200B;ストアに表示するギフトレジストリの名前を入力します。

     このラベルは、顧客が使用できるギフトレジストリの種類のリストのオプションです。

   - の場合 **[!UICONTROL Sort Order]**」に数値を入力して、このギフトレジストリが他のタイプと共に表示される際の順序を決定します。

   - ギフトレジストリを有効にするには、 **[!UICONTROL Is Listed]** から `Yes`.

     ![ギフトレジストリ — 一般情報](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. ギフトレジストリの各セクションを調べて、含める情報の種類を判断します。

1. 左側のパネルで、を選択します。 **[!UICONTROL Attributes]** をクリックします。 **[!UICONTROL Add Attribute]**.

   ![ギフトレジストリ — 新しい属性](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. 各属性に対して、次の操作を実行します。

   - ユニークを割り当て **[!UICONTROL Code]** 内部的に属性を識別する。 コードの長さは最大 15 文字で、先頭には小文字を使用する必要があります。 残りのコードでは、小文字の文字 (`a`-`z`)，数値 (`0`-`9`) とアンダースコア (`_`) 文字を使用して単語を区切ります。

   - を選択します。 **[!UICONTROL Input Type]** データ入力に使用します。 カスタム型または静的型のいずれかを使用できます。

   - 入力タイプに複数のオプションがある場合は、 **[!UICONTROL Add New Option]** 各オプションの情報を入力します。

     一部の入力タイプには、追加のプロパティがあります。 例えば、イベントの場所には、イベントを検索可能にする追加のプロパティがあり、お客様のストアのギフトレジストリの公開リストに含まれています。

      - 設定 **[!UICONTROL Attribute Group]** をギフトレジストリのセクションのどこに属性を表示するかを指定します。

      - の場合 **[!UICONTROL Label]**」で、レジストリ内のデータ入力フィールドを識別する名前を入力します。

      - 顧客が選択を行うか、フィールドに値を入力する必要がある場合は、 **[!UICONTROL Is Required]** から `Yes`.

      - の場合 **[!UICONTROL Sort Order]**「 」に数値を入力して、ストア内で使用可能な他のギフトレジストリと共にこのギフトレジストリが表示される順序を決定します。

1. 別のオプションを追加するには、 **新しいオプションを追加**.

   追加された各新しいオプションは、上部の新しいセクションに表示されます。 新しい属性に対して、この手順を繰り返します。

1. 完了したら、「 **[!UICONTROL Save]**.

## フィールドの説明

### [!UICONTROL General Information]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Code] | 内部的にギフトレジストリタイプを識別する一意の名前です。 コードの最初の文字は小文字にする必要があります。 残りのコードは、小文字 (a ～ z)、数字 (0 ～ 9)、アンダースコア文字 (`_`) をクリックします。 |
| [!UICONTROL Label] | ストアに表示されるギフトレジストリタイプの名前です。 |
| [!UICONTROL Sort Order] | このギフトレジストリの種類が他の種類と共に表示される場合の順序を決定します。 |
| [!UICONTROL Is Listed] | 店舗の顧客がギフトレジストリの種類を使用できるかどうかを指定します。 オプション： `Yes` / `No`. |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Code] | 内部的に属性を識別する一意の名前。 このコードには、小文字 (a ～ z)、数字 (0 ～ 9)、アンダースコア文字 (`_`) をクリックします。 |
| [!UICONTROL Input Type] | 属性に関連付けられるデータのタイプと入力コントロールを、タイプに従って決定します。 |
| [!UICONTROL Attribute Group] | ギフトレジストリに属性が一覧表示されているグループを選択します。 |
| [!UICONTROL Label] | 顧客のアカウントダッシュボードで属性を識別する名前。 |
| [!UICONTROL Is Required] | 属性が必須のエントリであるかどうかを示します。 ギフトレジストリは、必要な属性がすべて完了するまで保存できません。 オプション： `Yes` / `No`. |
| [!UICONTROL Sort Order] | 属性が他の属性と共に表示される場合に、その属性が表示される順序を決定します。 |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

属性に関連付けられているデータのタイプと入力コントロールを選択します。

**_[!UICONTROL Custom Types]_**

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Text] | 属性をテキストフィールドとして表示します。 |
| [!UICONTROL Select] | 属性をドロップダウンリストとして表示します。 クリック **[!UICONTROL Add New Option]** ドロップダウンリストに条件を追加するには：<br/>**[!UICONTROL Code]**— 内部的に属性を識別する一意の名前。<br/>**[!UICONTROL Label]**  — 顧客のアカウントダッシュボードで属性を識別する名前。<br/>**[!UICONTROL Is Default]**— このスイッチを設定して、デフォルトの条件を選択します。<br/>**[!UICONTROL Delete Option]**  — クリックしてオプションを削除します。 |
| [!UICONTROL Date] | 属性を日付フィールドとして表示します。 オプション： `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | 属性を国のドロップダウンリストとして表示します。 設定 **[!UICONTROL Show Region]** 移動先： `Yes` / `No`. |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Event Date] | ストアでの date 属性の使用方法を決定します。 オプション： <br/>**[!UICONTROL Searchable]**— 属性が詳細検索で使用可能かどうかを指定します。 オプション： `Yes` / `No`.<br/>**[!UICONTROL Is Listed]**  — ストアで使用可能なイベントのリストにイベントが含まれるかどうかを決定します。 オプション： `Yes` / `No`. <br/>**[!UICONTROL Date Format]**— イベント日の形式を決定します。 オプション： `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | 属性を国のリストとして表示します。 オプション： <br/>**[!UICONTROL Searchable]**— 属性が詳細検索で使用可能かどうかを指定します。 オプション： `Yes` / `No`.<br/>**[!UICONTROL Is Listed]**  — ストアで使用可能なイベントのリストにイベントが含まれるかどうかを決定します。 オプション： `Yes` / `No`. <br/>**[!UICONTROL Show Region]**— イベントの地域を決定します。 |
| [!UICONTROL Event Location] | ギフトレジストリに関連するイベントの場所。 <br/>設定 **[!UICONTROL Is Searcheable]** 移動先： `Yes` / `No` <br/>設定 **[!UICONTROL Is Listed]** 移動先： `Yes` / `No` |
| [!UICONTROL Role] | ギフト受信者を識別する役割。 例： `Bride`, `Groom`または `Partner`.<br/>**[!UICONTROL Is Searcheable]**— に設定 `Yes`/ `No`<br/>**&#x200B;リスト済み&#x200B;**— に設定 `Yes` / `No`<br/>**[!UICONTROL Add New Option]**  — クリックして、ドロップダウンメニューにさらに条件を追加します。<br/>**コード**  — 内部的に属性を識別する一意の名前。<br/>**[!UICONTROL Label]**— 顧客のアカウントダッシュボードで属性を識別する名前。<br/>**[!UICONTROL Is Default]**  — このスイッチを設定して、デフォルトの条件を選択します。<br/>**[!UICONTROL Delete Option]**— クリックしてオプションを削除します。 |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

ギフトレジストリに属性が一覧表示されているグループを選択します。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Event Information] | ギフトレジストリイベント、その時刻、場所などに関する情報を追加するすべてのギフトレジストリ属性をグループ化します。 |
| [!UICONTROL Gift Registry Properties] | ギフトレジストリに関する情報を直接追加するすべての属性を組み合わせます。 |
| [!UICONTROL Privacy Settings] | ギフトレジストリイベントのプライバシーに関する情報を追加する属性をリストします。 |
| [!UICONTROL Recipients Information] | ギフトレジストリを作成した人に関する情報を提供する属性をグループ化します。 |
| [!UICONTROL Shipping Address] | ギフトレジストリイベントの配送先住所に関する情報を追加する属性を組み合わせます。 |

{style="table-layout:auto"}
