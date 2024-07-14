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

returns 属性は、製品の返品プロセス中に必要な情報を保存するために使用されます。 デフォルトの属性には、返される製品の条件、返される理由、返される結果の解決方法を示すフィールドが含まれます。 戻り値属性を作成するプロセスは、[ 顧客属性 ](../customers/attribute-properties.md) の作成に似ています。

![Admin – 属性を返します ](./assets/attribute-returns.png){width="700" zoomable="yes"}

## 戻り値の属性の作成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Returns]**に移動します。

1. 右上隅の「**[!UICONTROL Add New Attribute]**」をクリックします。

   ![ 新しい戻り値 – 属性プロパティ ](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### プロパティの定義

1. データ入力時に属性を識別するには、**[!UICONTROL Default Label]** を設定します。

1. **[!UICONTROL Attribute Code]**：システム内の属性を識別するコードを入力します。

1. データ入力に使用される入力コントロールの種類を決定するには、**[!UICONTROL Input Type]** を次のいずれかに設定します。

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. フィールドを必須項目にするには、**[!UICONTROL Values Required]** を `Yes` に設定します。

1. フィールドに初期値を割り当てるには、**[!UICONTROL Default Value]** を入力します。

1. レコードを保存する前に、フィールドに入力されたデータの正確性を検証するには、**[!UICONTROL Input Validation]** を次のいずれかに設定します。

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. `Text Field` と `Text Area` の入力タイプには、**[!UICONTROL Minimum Text Length]** と **[!UICONTROL Maximum Text Length]** を入力します。

1. 前処理フィルターを適用するには、**[!UICONTROL Input/Output Filter]** を次のいずれかに設定します。

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. 顧客に属性を表示するには、_[!UICONTROL Storefront Properties]_の節で&#x200B;**[!UICONTROL Show on Storefront]**を `Yes` に設定します。

1. （オプション） **[!UICONTROL Sort Order]** の場合は、数値を入力して、ページの同じ部分にある他の属性に対するこの属性の相対的な位置を決定します。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

### ラベル/オプションの管理

1. 左側のパネルで「**[!UICONTROL Manage Labels/Options]**」を選択します。

1. 「**[!UICONTROL Manage Titles (Size, Color, etc.)]**」セクションで、各ストアビューのラベルを入力します。

   ![ ラベルの管理 ](./assets/return-attributes.png){width="600" zoomable="yes"}

1. 属性の **[!UICONTROL Input Type]** が `Dropdown` の場合は、「**[!UICONTROL Manage Options (Values of Your Attribute)]**」セクションでオプションを管理します。

   - オプションを追加するには、「**[!UICONTROL Add Option]**」をクリックし、管理者および各ストア表示のラベルを入力します。
   - オプションを選択したデフォルトにするには、「**[!UICONTROL Is Default]**」を選択します。
   - オプションを削除するには、「削 **[!UICONTROL Delete]**」をクリックします。

1. 変更を保存するには、「**[!UICONTROL Save Attribute]**」をクリックします。
