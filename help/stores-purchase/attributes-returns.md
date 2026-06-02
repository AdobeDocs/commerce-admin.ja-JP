---
title: 属性を返します
description: 返品属性と、ストアで返品を処理するために必要な属性の作成方法について説明します。
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# 属性を返します

{{ee-feature}}

返品属性は、製品返品プロセス中に必要な情報を保存するために使用されます。 デフォルトの属性には、返された製品の条件、返された理由、および返された結果の解決方法を示すフィールドが含まれます。 返品属性を作成するプロセスは、[顧客属性](../customers/attribute-properties.md)の作成に似ています。

![管理者 – 属性](./assets/attribute-returns.png){width="700" zoomable="yes"}を返します

## returns属性の作成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add New Attribute]**」をクリックします。

   ![新しい戻り値 – 属性プロパティ &#x200B;](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### プロパティの定義

1. データ入力中に属性を識別するには、**[!UICONTROL Default Label]**&#x200B;を設定します。

1. **[!UICONTROL Attribute Code]**&#x200B;に、システム内の属性を識別するコードを入力します。

1. データ入力に使用する入力制御の種類を判断するには、**[!UICONTROL Input Type]**&#x200B;を次のいずれかに設定します。

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. フィールドを必須アイテムにするには、**[!UICONTROL Values Required]**&#x200B;を`Yes`に設定します。

1. フィールドに初期値を割り当てるには、**[!UICONTROL Default Value]**&#x200B;を入力します。

1. レコードを保存する前に、フィールドに入力されたデータの正確性を検証するには、**[!UICONTROL Input Validation]**&#x200B;を次のいずれかに設定します。

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. `Text Field`と`Text Area`の入力タイプの場合は、**[!UICONTROL Minimum Text Length]**&#x200B;と&#x200B;**[!UICONTROL Maximum Text Length]**&#x200B;を入力します。

1. 前処理フィルターを適用するには、**[!UICONTROL Input/Output Filter]**&#x200B;を次のいずれかに設定します。

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. 属性を顧客に表示するには、_[!UICONTROL Storefront Properties]_&#x200B;セクションで&#x200B;**[!UICONTROL Show on Storefront]**&#x200B;を`Yes`に設定します。

1. （オプション） **[!UICONTROL Sort Order]**&#x200B;に対して、この属性がページの同じ部分の他の属性と相対的に表示される場所を決定する数値を入力します。 （`0` = first, `1` = second, `2` = thirdなど）

### ラベル/オプションの管理

1. 左側のパネルで、**[!UICONTROL Manage Labels/Options]**&#x200B;を選択します。

1. 「**[!UICONTROL Manage Titles (Size, Color, etc.)]**」セクションで、各ストアビューのラベルを入力します。

   ![&#x200B; ラベルの管理](./assets/return-attributes.png){width="600" zoomable="yes"}

1. 属性の&#x200B;**[!UICONTROL Input Type]**&#x200B;が`Dropdown`の場合、**[!UICONTROL Manage Options (Values of Your Attribute)]** セクションのオプションを管理します。

   - オプションを追加するには、**[!UICONTROL Add Option]**&#x200B;をクリックし、管理者と各ストアビューのラベルを入力します。
   - オプションを選択した既定値にするには、**[!UICONTROL Is Default]**&#x200B;を選択します。
   - オプションを削除するには、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 変更を保存するには、**[!UICONTROL Save Attribute]**&#x200B;をクリックします。
