---
title: 属性を返します
description: 返品属性と、ストアで返品を処理するために必要な属性の作成方法について説明します。
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 属性を返します

{{ee-feature}}

returns 属性は、製品の返品プロセス中に必要な情報を保存するために使用されます。 デフォルトの属性には、返される製品の条件、返される理由、返される結果の解決方法を示すフィールドが含まれます。 戻り値属性の作成プロセスは、の作成プロセスと似ています。 [顧客属性](../customers/attribute-properties.md).

![管理者 – 属性を返します](./assets/attribute-returns.png){width="700" zoomable="yes"}

## 戻り値の属性の作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Attribute]**.

   ![新しい戻り値 – 属性プロパティ](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### プロパティの定義

1. データ入力時に属性を識別するには、 **[!UICONTROL Default Label]**.

1. の場合 **[!UICONTROL Attribute Code]**&#x200B;を入力し、システム内の属性を識別するコードを入力します。

1. データ入力に使用される入力コントロールの種類を決定するには、次のように設定します **[!UICONTROL Input Type]** を次のいずれかに変更します。

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. フィールドを必須項目にするには、次のように設定します **[!UICONTROL Values Required]** 対象： `Yes`.

1. フィールドに初期値を割り当てるには、 **[!UICONTROL Default Value]**.

1. レコードを保存する前に、フィールドに入力されたデータの正確性を検証するには、次のように設定します **[!UICONTROL Input Validation]** を次のいずれかに変更します。

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. の場合 `Text Field` および `Text Area` 入力タイプ、を入力 **[!UICONTROL Minimum Text Length]** および **[!UICONTROL Maximum Text Length]**.

1. 前処理フィルターを適用するには、を設定します **[!UICONTROL Input/Output Filter]** を次のいずれかに変更します。

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. 顧客に属性を表示するには、次のように設定します **[!UICONTROL Show on Storefront]** 対象： `Yes` が含まれる _[!UICONTROL Storefront Properties]_セクション。

1. （オプション） **[!UICONTROL Sort Order]**&#x200B;を入力します。この属性がページの同じ部分にある他の属性との相対的な位置を決定するための数値を入力します。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

### ラベル/オプションの管理

1. 左パネルで、を選択します。 **[!UICONTROL Manage Labels/Options]**.

1. が含まれる **[!UICONTROL Manage Titles (Size, Color, etc.)]** セクションで、各ストア表示のラベルを入力します。

   ![ラベルの管理](./assets/return-attributes.png){width="600" zoomable="yes"}

1. 次の場合 **[!UICONTROL Input Type]** 属性がの場合 `Dropdown`でオプションを管理します **[!UICONTROL Manage Options (Values of Your Attribute)]** セクション。

   - オプションを追加するには、 **[!UICONTROL Add Option]** そして、管理者のラベルと各ストア表示を入力します。
   - オプションを選択したデフォルトにするには、 **[!UICONTROL Is Default]**.
   - オプションを削除するには、 **[!UICONTROL Delete]**.

1. 変更を保存するには、をクリックします **[!UICONTROL Save Attribute]**.
