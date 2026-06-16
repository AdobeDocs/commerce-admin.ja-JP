---
title: 属性セット
description: 属性をグループに整理して、製品レコードのどこに表示するかを決定する方法を説明します。
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/MXe9ockAmhKgFC-ND2CUxqHRAsShfA5Tf8yJsJWy04o
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# 属性セット

製品を作成する際の最初の手順の1つは、製品レコードのテンプレートとして使用される属性セットを選択することです。 属性セットは、データ入力時に使用できるフィールドと、顧客に表示される値を決定します。

属性は、商品レコードのどこに表示されるかを決定するグループに整理されます。 ストアには、一般的に使用される属性のセットを含む初期属性セット（_default_&#x200B;と呼ばれます）が付属しています。 一部の属性のみを追加する場合は、これらの属性をこのデフォルトの属性セットに追加できます。 特定の種類の情報を必要とする製品を販売する場合は、製品に必要な特定の属性を含む専用の属性セットを作成することをお勧めします。

![属性セット &#x200B;](./assets/attribute-sets.png){width="700" zoomable="yes"}

## 属性セットの作成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**&#x200B;に移動します。

1. **[!UICONTROL Add New Set]**&#x200B;をクリックします。

   ![属性セット – 編集名](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. 属性セットの&#x200B;**[!UICONTROL Name]**&#x200B;を入力します。

1. テンプレートとして使用する既存の属性セットに&#x200B;**[!UICONTROL Based On]**&#x200B;を設定します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

   次のページには、次の情報が表示されます。

   - 左側の列には、属性セットの名前が表示されます。 名前は内部参照用で、必要に応じて変更できます。
   - ページの中央には、現在の属性グループの選択内容が一覧表示されます。
   - 右側の列には、現在属性セットに割り当てられていない属性の選択が一覧表示されます。

1. セットに属性を追加するには、**[!UICONTROL Unassigned Attributes]** リストから&#x200B;**[!UICONTROL Groups]**&#x200B;列の適切なフォルダーに属性をドラッグします。 セットから属性を削除するには、属性を&#x200B;**[!UICONTROL Unassigned Attributes]** リストにドラッグします。

   >[!NOTE]
   >
   >システム属性はドットでマークされ、_[!UICONTROL Groups]_&#x200B;リストから削除できません。 ただし、属性セット内の別のグループにドラッグすることもできます。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

![属性セット – 編集](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## 属性グループの作成

1. 属性セットの&#x200B;_[!UICONTROL Groups]_&#x200B;列で、**[!UICONTROL Add New]**&#x200B;をクリックします。

1. 新しいグループの&#x200B;**[!UICONTROL Name]**&#x200B;を入力し、**[!UICONTROL OK]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   - **[!UICONTROL Unassigned Attributes]**&#x200B;を新しいグループにドラッグします。
   - 他のグループから新しいグループに属性をドラッグします。
   - 不要な属性を&#x200B;**[!UICONTROL Unassigned Attributes]**&#x200B;にドラッグします。

   新しいグループは、属性セットに基づく製品内の属性のセクションになります。

## 属性セットの削除

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**&#x200B;に移動します。

1. リストで属性セットを選択し、編集モードで開きます。

1. **[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認を求められたら、**[!UICONTROL OK]**&#x200B;をクリックします。
