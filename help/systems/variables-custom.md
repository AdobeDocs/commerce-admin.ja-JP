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

ビジネスの特定のニーズを満たすために、カスタム変数を作成して、[ ページ ](../content-design/pages.md)、[ ブロック ](../content-design/blocks.md) および [ メールテンプレート ](email-templates.md) に挿入できます。 「_変数を挿入_」ボタンをクリックすると表示される、許可された変数のリストには、[ 事前定義済み ](variables-predefined.md) 変数とカスタム変数の両方が含まれています。 特定のメールテンプレートで使用できる変数のリストは、テンプレートに関連付けられているデータによって決まります。 よく使用されるメールテンプレートとそれに関連する変数のリストについては、[ 変数リファレンス ](variables-reference.md) を参照してください。

![ カスタム変数 ](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>メールおよびニュースレターのテンプレートでは、許可されている事前定義済み変数またはカスタム変数のみを使用できます。

## 手順 1：カスタム変数の作成

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Other Settings]_/**[!UICONTROL Custom Variables]**&#x200B;に移動します。

1. 「**[!UICONTROL Add New Variable]**」をクリックします。

1. **[!UICONTROL Variable Code]** の識別子を入力します。スペースを含めず、すべて小文字を使用します。

   必要に応じて、アンダースコア文字またはハイフンを使用してスペースを表すことができます。 例：`my_custom_variable`

1. 内部参照に使用する **[!UICONTROL Variable Name]** を入力します。 例：`My Custom Variable`

1. 変数に関連付けられている値を入力するには、次のいずれかの操作を行います。

   - **[!UICONTROL Variable HTML Value]** しくは、単純なHTMLタグで書式設定された変数値を入力します。 例：

     `<b>This formatted content appears in place of the variable.</b>`

   - **[!UICONTROL Variable Plain Value]**：変数値を書式設定のないプレーンテキストとして入力します。 例：

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >スペースを広げる必要がある場合は、テキストボックスの右下隅をドラッグします。

   ![ 新しいカスタム変数 ](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 手順 2：コンテンツへのカスタム変数の挿入

[!DNL Page Builder] を使用してカスタム変数を挿入します。

1. 変数をコンテンツに追加するページ、ブロック、カテゴリまたは製品を開きます。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Content]**」セクションを展開します。

1. 「**[!UICONTROL Edit with Page Builder]**」をクリックします。

1. 左側のパネルで「**[!UICONTROL Elements]**」をクリックし、次のいずれかの操作を行います。

   - 変数を挿入する既存のテキスト領域内をクリックします。

   - 新しい **[!UICONTROL Text]** オブジェクトをステージにドラッグします。

1. エディターツールバーの右端にある（![ 変数を挿入 ](./assets/editor-btn-insert-variable.png)）をクリックして、変数を挿入します。

   ステ ![[!DNL Page Builder] ジとパネル ](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. リストで、挿入するカスタム変数を選択し、「**[!UICONTROL Insert Variable]**」をクリックします。

   ![ 新しいカスタム変数 ](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   変数識別子は、エディターでプレースホルダーとして表示されます。

   ![[!DNL Page Builder] ステージ – 変数プレースホルダー ](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。
