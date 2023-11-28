---
title: 定義済み変数の使用
description: 事前定義済みの変数と、電子メールテンプレートに追加する方法について説明します。
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 定義済み変数の使用

[定義済み](variables-predefined.md) 変数を使用すると、パーソナライズが容易になります [電子メール](email-templates.md) および [ニュースレター](../merchandising-promotions/newsletters.md) テンプレートおよびその他のタイプのコンテンツ。 許可される [定義済み](variables-predefined.md) 変数は、「変数を挿入」ボタンをクリックすると表示されます。 次の図に示すように、特定の電子メールテンプレートで使用可能な変数のリストは、テンプレートに関連付けられているデータによって決まります。 詳しくは、 [変数リファレンス](variables-reference.md) を参照してください。

![メールテンプレート用の事前定義済み変数](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## E メールテンプレートへの変数の追加

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 次のいずれかの操作を行います。

   - 変数を既存のテンプレートに追加するには、リスト内のテンプレートをクリックして、編集モードで開きます。

   - 変数を新しいテンプレートで使用するには、 **[!UICONTROL Add New Template]** デフォルトのテンプレートコードをカスタマイズします。 詳しくは、 [メッセージテンプレート](email-template-custom.md#message-templates).

1. の下 _[!UICONTROL Load default template]_、選択&#x200B;**[!UICONTROL Template]**を選択します。

1. テンプレートを適用するには、 **[!UICONTROL Load Template]**.

   The _[!UICONTROL Currently used for]_「 」フィールドには、テンプレートの設定パスが表示されます。 The_[!UICONTROL Template Subject]_ および _[!UICONTROL Template Content]_は、選択したテンプレートを基準に自動的に生成されます。

   - **[!UICONTROL Template Subject]**  — このテキストは、E メールの件名行に表示されます。

   - **[!UICONTROL Template Content]**  — このテキストは、送信された E メールの完全なコンテンツに表示されます。

   ![メールテンプレートコンテンツ](./assets/email-template-content.png){width="600" zoomable="yes"}

1. を入力します。 **[!UICONTROL Template Name]**.

1. リストの [定義済み](variables-predefined.md) この電子メールテンプレートで使用できる変数は、 **[!UICONTROL Insert Variable]**.

   テンプレートに挿入する変数を決定します。 次に、「 _閉じる_ (X) を使用します。 （後で戻ります）。

1. テンプレートのモックアップを表示するには、 **[!UICONTROL Preview Template]** をクリックします。

   プレビューが新しいタブで開いたら、他のコンテンツとの関係で変数を配置する場所を指定します。 続行するには、元のタブに戻ります。

   ![テンプレートをプレビュー](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Template Content]** 」ボックスで、変数を表示する場所に挿入ポイントを置き、 **[!UICONTROL Insert Variable...]**.

1. 使用可能な変数のリストで、テンプレートに挿入する変数をクリックします。

1. 完了したら、「 **[!UICONTROL Save Template]**.

## テンプレートをプレーンテキストに変換します

1. テンプレートを編集モードで開きます。

1. ページ上部で、「 **[!UICONTROL Convert to Plain Text]**.

1. タグを削除するよう求められたら、 **[!UICONTROL OK]**.

1. プレーンテキストバージョンを保存するには、 **[!UICONTROL Save Template]**.

## HTMLバージョンの復元

1. ページ上部で、「 **[!UICONTROL Return HTML Version]**.

1. テンプレートのHTMLバージョンを保存するには、 **[!UICONTROL Save Template]**.
