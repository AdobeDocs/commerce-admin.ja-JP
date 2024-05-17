---
title: 事前定義済みの変数の使用
description: 事前定義済みの変数と、メールテンプレートで追加する方法について説明します。
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 事前定義済みの変数の使用

[定義済み](variables-predefined.md) 変数を使用すると、パーソナライズが容易になります [電子メール](email-templates.md) および [ニュースレター](../merchandising-promotions/newsletters.md) テンプレート、およびその他のタイプのコンテンツ。 許可されたのリスト [定義済み](variables-predefined.md) 変数は、「変数を挿入」ボタンをクリックすると表示されます。 次の画像に示すように、特定のメールテンプレートで使用可能な変数のリストは、テンプレートに関連付けられているデータによって決定されます。 を参照してください。 [変数リファレンス](variables-reference.md) よく使用されるメールテンプレートとそれに関連する変数のリスト。

![メールテンプレートの事前定義済み変数](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## メールテンプレートへの変数の追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 次のいずれかの操作を行います。

   - 既存のテンプレートに変数を追加するには、リストでテンプレートをクリックして、編集モードで開きます。

   - 新しいテンプレートで変数を使用するには、をクリックします。 **[!UICONTROL Add New Template]** デフォルトテンプレートコードをカスタマイズします。 参照： [メッセージテンプレート](email-template-custom.md#message-templates).

1. 次の下 _[!UICONTROL Load default template]_、を選択します&#x200B;**[!UICONTROL Template]**をカスタマイズします。

1. テンプレートを適用するには、 **[!UICONTROL Load Template]**.

   この _[!UICONTROL Currently used for]_フィールドには、テンプレートの設定パスが表示されます。 この_[!UICONTROL Template Subject]_ および _[!UICONTROL Template Content]_選択したテンプレートを基準にして自動的に生成されます。

   - **[!UICONTROL Template Subject]**  – このテキストは、メールの件名に表示されます。

   - **[!UICONTROL Template Content]**  – このテキストは、送信されたメールのコンテンツ全体に表示されます。

   ![メールテンプレートコンテンツ](./assets/email-template-content.png){width="600" zoomable="yes"}

1. を入力 **[!UICONTROL Template Name]**.

1. のリストについては、 [定義済み](variables-predefined.md) このメールテンプレートで使用できる変数をクリックします **[!UICONTROL Insert Variable]**.

   テンプレートに挿入する変数を決定します。 次に、 _閉じる_ （X）右上隅 （後でこれに戻ります）。

1. テンプレートのモックアップを表示するには、をクリックしてください **[!UICONTROL Preview Template]** をクリックします。

   新しいタブでプレビューが開いたら、他のコンテンツを基準として変数を配置する場所を指定します。 その後、元のタブに戻って続行します。

   ![テンプレートのプレビュー](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. が含まれる **[!UICONTROL Template Content]** ボックスで、変数を表示する位置に挿入ポイントを置き、クリックします **[!UICONTROL Insert Variable...]**.

1. 使用可能な変数の一覧で、テンプレートに挿入する変数をクリックします。

1. 完了したら、 **[!UICONTROL Save Template]**.

## テンプレートをプレーンテキストに変換

1. テンプレートを編集モードで開きます。

1. ページの上部で、 **[!UICONTROL Convert to Plain Text]**.

1. タグの削除を求めるプロンプトが表示されたら、 **[!UICONTROL OK]**.

1. プレーンテキストのバージョンを保存するには、をクリックします **[!UICONTROL Save Template]**.

## HTMLのバージョンを復元する

1. ページの上部で、 **[!UICONTROL Return HTML Version]**.

1. テンプレートのHTMLバージョンを保存するには、 **[!UICONTROL Save Template]**.
