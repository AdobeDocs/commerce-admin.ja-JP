---
title: 属性セット
description: 製品レコード内の属性の表示場所を決定するグループに属性を整理する方法を説明します。
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 43550b9370f4ed4b631ae7773324ed0913718a79
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 属性セット

製品を作成する最初の手順の 1 つは、製品レコードのテンプレートとして使用する属性セットを選択することです。 属性セットは、データ入力時に使用できるフィールドと、顧客に表示される値を決定します。

属性は、製品レコード内の表示場所を決定するグループに整理されます。 ストアには、一般的に使用される一連の属性を含む初期属性セット（_デフォルト_）が用意されています。 少数の属性のみを追加する場合は、それらの属性をこのデフォルトの属性セットに追加します。 特定の種類の情報が必要な製品を販売する場合は、製品に必要な特定の属性を含む専用の属性セットを作成する方が良い場合があります。

![ 属性セット ](./assets/attribute-sets.png){width="700" zoomable="yes"}

## 属性セットの作成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Attribute Set]**&#x200B;に移動します。

1. 「**[!UICONTROL Add New Set]**」をクリックします。

   ![ 属性セット – 名前を編集 ](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. 属性セットの **[!UICONTROL Name]** を入力します。

1. テンプレートとして使用する既存の属性セットに **[!UICONTROL Based On]** を設定します。

1. 「**[!UICONTROL Save]**」をクリックします。

   次のページには、次の情報が表示されます。

   - 左側の列には、属性セットの名前が表示されます。 この名前は内部参照用であり、必要に応じて変更できます。
   - ページの中央には、属性グループの現在選択されている項目が一覧表示されます。
   - 右側の列には、属性セットに現在割り当てられていない属性の選択が一覧表示されます。

1. セットに属性を追加するには、属性リストから **[!UICONTROL Groups]** 列の適切なフォルダーに **[!UICONTROL Unassigned Attributes]** 属性をドラッグします。 セットから属性を削除するには、属性を **[!UICONTROL Unassigned Attributes]** のリストにドラッグします。

   >[!NOTE]
   >
   >システム属性はドットでマークされ、_[!UICONTROL Groups]_&#x200B;ータリストから削除できません。 ただし、属性セットの別のグループにドラッグすることはできます。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

![ 属性セット – 編集 ](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## 属性グループの作成

1. 属性セットの「_[!UICONTROL Groups]_」列で、「**[!UICONTROL Add New]**」をクリックします。

1. 新しいグループの **[!UICONTROL Name]** を入力し、[**[!UICONTROL OK]**] をクリックします。

1. 次のいずれかの操作をおこないます。

   - **[!UICONTROL Unassigned Attributes]** を新しいグループにドラッグします。
   - 他のグループから新しいグループにアトリビュートをドラッグします。
   - 不要な属性を **[!UICONTROL Unassigned Attributes]** にドラッグします。

   新しいグループは、属性セットに基づくすべての製品の属性のセクションになります。

## 属性セットの削除

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Attribute Set]**&#x200B;に移動します。

1. リストで属性セットを選択し、編集モードで開きます。

1. 「**[!UICONTROL Delete]**」をクリックします。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL OK]**」をクリックします。
