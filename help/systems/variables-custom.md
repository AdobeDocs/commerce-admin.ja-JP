---
title: カスタム変数の追加
description: カスタム変数を作成して、ページ、ブロック、製品コンテンツに挿入する方法を説明します。
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 1%

---

# カスタム変数の追加

ビジネスの特定のニーズを満たすには、カスタム変数を作成し、に挿入します [ページ](../content-design/pages.md), [ブロック](../content-design/blocks.md)、および [メールテンプレート](email-templates.md). をクリックすると表示される、許可された変数のリスト _変数を挿入_ ボタンに次の両方が含まれる： [定義済み](variables-predefined.md) およびカスタム変数。 特定のメールテンプレートで使用できる変数のリストは、テンプレートに関連付けられているデータによって決まります。 を参照してください。 [変数リファレンス](variables-reference.md) よく使用されるメールテンプレートとそれに関連する変数のリスト。

![カスタム変数](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>メールおよびニュースレターのテンプレートでは、許可されている事前定義済み変数またはカスタム変数のみを使用できます。

## 手順 1：カスタム変数の作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. クリック **[!UICONTROL Add New Variable]**.

1. 識別子を入力 **[!UICONTROL Variable Code]**（スペースを含めず、すべての小文字を使用）。

   必要に応じて、アンダースコア文字またはハイフンを使用してスペースを表すことができます。 例： `my_custom_variable`

1. を入力 **[!UICONTROL Variable Name]**（内部参照に使用）。 例： `My Custom Variable`

1. 変数に関連付けられている値を入力するには、次のいずれかの操作を行います。

   - の場合 **[!UICONTROL Variable HTML Value]**&#x200B;を入力し、単純なHTMLタグで書式設定された変数値を入力します。 例：

     `<b>This formatted content appears in place of the variable.</b>`

   - の場合 **[!UICONTROL Variable Plain Value]**&#x200B;を選択し、書式設定のないプレーンテキストとして変数値を入力します。 例：

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >スペースを広げる必要がある場合は、テキストボックスの右下隅をドラッグします。

   ![新規カスタム変数](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

## 手順 2：コンテンツへのカスタム変数の挿入

使用方法 [!DNL Page Builder] をクリックして、カスタム変数を挿入します。

1. 変数をコンテンツに追加するページ、ブロック、カテゴリまたは製品を開きます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** セクション。

1. クリック **[!UICONTROL Edit with Page Builder]**.

1. 左側のパネルで、 **[!UICONTROL Elements]** 次のいずれかの操作を行います。

   - 変数を挿入する既存のテキスト領域内をクリックします。

   - 新しいをドラッグ **[!UICONTROL Text]** オブジェクトをステージに追加します。

1. エディターツールバーの右端にある（ ![変数を挿入](./assets/editor-btn-insert-variable.png) ）を選択して、変数を挿入します。

   ![[!DNL Page Builder] ステージとパネル](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. リストで、挿入するカスタム変数を選択し、 **[!UICONTROL Insert Variable]**.

   ![新規カスタム変数](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   変数識別子は、エディターでプレースホルダーとして表示されます。

   ![[!DNL Page Builder] ステージ – 変数のプレースホルダー](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.
