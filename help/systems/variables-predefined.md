---
title: 定義済み変数の使用
description: 定義済みの変数と、それをメールテンプレートに追加する方法について説明します。
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: https://experienceleague.adobe.com/TKhaNVRFLc3VK0iDkCpqoWSnvFRJmDWAIw1uBPzlh00
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 387
ht-degree: 0%

---

# 定義済み変数の使用

[定義済みの](variables-predefined.md)変数を使用すると、[電子メール &#x200B;](email-templates.md)および[&#x200B; ニュースレター](../merchandising-promotions/newsletters.md) テンプレートやその他の種類のコンテンツを簡単にパーソナライズできます。 許可されている[定義済み](variables-predefined.md)変数のリストは、「変数を挿入」ボタンをクリックすると表示されます。 次の画像に示すように、特定のメールテンプレートで使用可能な変数のリストは、テンプレートに関連付けられているデータによって決まります。 頻繁に使用されるメールテンプレートと関連する変数の一覧については、[変数リファレンス &#x200B;](variables-reference.md)を参照してください。

![電子メールテンプレートの定義済み変数](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## メールテンプレートへの変数の追加

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**&#x200B;に移動します。

1. 次のいずれかの操作を行います。

   - 既存のテンプレートに変数を追加するには、リスト内のテンプレートをクリックして、編集モードで開きます。

   - 新しいテンプレートで変数を使用するには、**[!UICONTROL Add New Template]**&#x200B;をクリックし、デフォルトのテンプレートコードをカスタマイズします。 [&#x200B; メッセージテンプレート &#x200B;](email-template-custom.md#message-templates)を参照してください。

1. _[!UICONTROL Load default template]_&#x200B;で、カスタマイズする&#x200B;**[!UICONTROL Template]**&#x200B;を選択します。

1. テンプレートを適用するには、**[!UICONTROL Load Template]**&#x200B;をクリックします。

   _[!UICONTROL Currently used for]_&#x200B;フィールドには、テンプレートの設定パスが表示されます。_[!UICONTROL Template Subject]_&#x200B;と&#x200B;_[!UICONTROL Template Content]_&#x200B;は、選択したテンプレートに対して自動的に生成されます。

   - **[!UICONTROL Template Subject]** – このテキストは、電子メールの件名に表示されます。

   - **[!UICONTROL Template Content]** – このテキストは、送信された電子メールの完全な内容で表示されます。

   ![&#x200B; メールテンプレートコンテンツ &#x200B;](./assets/email-template-content.png){width="600" zoomable="yes"}

1. **[!UICONTROL Template Name]**&#x200B;を入力します。

1. この電子メールテンプレートで使用できる[定義済み](variables-predefined.md)変数のリストについては、**[!UICONTROL Insert Variable]**&#x200B;をクリックしてください。

   テンプレートに挿入する変数を決定します。 次に、右上隅の&#x200B;_閉じる_ （X）をクリックします。 （後で元に戻ります）

1. テンプレートのモックアップを表示するには、ボタンバーの「**[!UICONTROL Preview Template]**」をクリックします。

   新しいタブでプレビューが開いたら、他のコンテンツに関連して変数を配置する場所を決定します。 次に、元のタブに戻って続行します。

   ![&#x200B; テンプレートのプレビュー](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. **[!UICONTROL Template Content]** ボックスで、変数を表示する位置に挿入ポイントを置き、**[!UICONTROL Insert Variable...]**&#x200B;をクリックします。

1. 使用可能な変数のリストで、テンプレートに挿入する変数をクリックします。

1. 完了したら、**[!UICONTROL Save Template]**&#x200B;をクリックします。

## テンプレートをプレーンテキストに変換

1. テンプレートを編集モードで開きます。

1. ページの上部で、**[!UICONTROL Convert to Plain Text]**&#x200B;をクリックします。

1. タグの削除を求めるメッセージが表示されたら、**[!UICONTROL OK]**&#x200B;をクリックします。

1. プレーンテキストのバージョンを保存するには、**[!UICONTROL Save Template]**&#x200B;をクリックします。

## HTMLのバージョンを復元

1. ページの上部で、**[!UICONTROL Return HTML Version]**&#x200B;をクリックします。

1. HTML バージョンのテンプレートを保存するには、**[!UICONTROL Save Template]**&#x200B;をクリックします。
