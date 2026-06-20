---
title: 商品レビューを管理
description: 投稿されたレビューがストアの一般公開に適していることを確認するために、商品レビューを管理する方法について説明します。
exl-id: 90c3e918-f435-4468-b41b-e8044ad14fb0
feature: Merchandising, Products
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/DGRJr-P9TUQ1TFh4Da1Z4VwrKfWe2rw5wmbwq9IlAFg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 419
ht-degree: 0%

---

# 商品レビューを管理

Commerce製品レビューの場合、提出された製品レビューは、表示される前に承認されている必要があります。 これにより、レビューがストアの一般公開に適していることを確認できます。 送信されたレビューは、承認または却下されるまで`Pending`状態です。

## 管理画面での製品レビューの表示

管理画面で特定の製品に関するすべてのレビューを表示するには、次の操作を行います。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

1. 表示する製品を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

1. 製品ページで、下にスクロールして![拡張セレクター](../assets/icon-display-expand.png)、**[!UICONTROL Product Reviews]** セクションを展開します。

   このグリッドでは、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;リンクをクリックして、特定のレビューを変更することもできます。

## レビューのステータスを更新

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL Pending Reviews]**&#x200B;または&#x200B;**[!UICONTROL All Reviews]**&#x200B;に移動します。

1. リストで、保留中のレビューをクリックして詳細を表示し、必要に応じて編集します。

1. 評価に応じて&#x200B;**[!UICONTROL Status]**&#x200B;を変更します。

   - 保留中のレビューを承認するには、`Approved`を選択します。

   - レビューを却下するには、`Not Approved`を選択します。 未承認のレビューは&#x200B;_[!UICONTROL Pending Reviews]_&#x200B;ページのリストから消えます。

   >[!NOTE]
   >
   >`Pending`と`Not Approved`のステータスを持つレビューは、ストアフロントに表示されません。

1. 該当する場合は、商品レビューの&#x200B;**[!UICONTROL Visibility]**&#x200B;を異なるストアビューで表示するように設定します。

1. 必要に応じて、**[!UICONTROL Detailed Rating]**、**[!UICONTROL Nickname]**、**[!UICONTROL Summary of Review]**&#x200B;の値を変更します。

   レビューが利用可能なストアビューを変更するには、_[!UICONTROL Visibility]_&#x200B;列で必要なストアビューを選択します。

   ![&#x200B; レビューページを編集](./assets/edit-review-page.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Review]**&#x200B;をクリックします。

## 一括更新

複数のレビューを同時に更新または削除できます。

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**&#x200B;に移動します。

1. 更新するレビューを選択します。

1. アクションを適用するには、左上隅の&#x200B;_[!UICONTROL Action]_&#x200B;セレクターを使用します。

1. **[!UICONTROL Submit]**&#x200B;をクリック

## 製品レビューの削除

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**&#x200B;に移動します。

1. 削除する製品レビューを見つけて、編集モードで開きます。

1. メニューバーで、**[!UICONTROL Delete Review]** ボタンをクリックします。

1. アクションを確認するには、**[!UICONTROL OK]**&#x200B;をクリックします。

## ボタンバー

| ボタン | 説明 |
|----------|--------------|
| **[!UICONTROL Back]** | 変更を保存せずにレビューページに戻ります |
| **[!UICONTROL Delete Review]** | レビューを削除します |
| **[!UICONTROL Reset]** | レビューフォームに保存されていない変更を以前の値にリセットします |
| **[!UICONTROL Previous]** | 前のレビューを開きます |
| **[!UICONTROL Next]** | 次のレビューを開きます |
| **[!UICONTROL Save and Previous]** | 現在の変更を保存し、以前のレビューを開きます。 このボタンは、他のレビューがある場合に表示されます。 |
| **[!UICONTROL Save and Next]** | 現在の変更を保存し、次のビューを開きます。 このボタンは、他のレビューがある場合に表示されます。 |
| **[!UICONTROL Save Review]** | 変更内容を保存してレビュー編集ページを閉じます |
