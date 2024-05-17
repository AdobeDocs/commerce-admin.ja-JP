---
title: 属性セット
description: 製品レコード内の属性の表示場所を決定するグループに属性を整理する方法を説明します。
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 属性セット

製品を作成する最初の手順の 1 つは、製品レコードのテンプレートとして使用する属性セットを選択することです。 属性セットは、データ入力時に使用できるフィールドと、顧客に表示される値を決定します。

属性は、製品レコード内の表示場所を決定するグループに整理されます。 ストアには、最初の属性セット（と呼ばれます）が付属しています _default_）を選択できます。このプロパティには、一般的に使用される属性のセットが含まれます。 少数の属性のみを追加する場合は、それらの属性をこのデフォルトの属性セットに追加します。 特定の種類の情報が必要な製品を販売する場合は、製品に必要な特定の属性を含む専用の属性セットを作成する方が良い場合があります。

![属性セット](./assets/attribute-sets.png){width="700" zoomable="yes"}

## 属性セットの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. クリック **[!UICONTROL Add New Set]**.

   ![属性セット – 名前を編集](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. を入力 **[!UICONTROL Name]** を属性セットに使用します。

1. を設定 **[!UICONTROL Based On]** を、テンプレートとして使用する既存の属性セットに追加します。

1. click **[!UICONTROL Save]**.

   次のページには、次の情報が表示されます。

   - 左側の列には、属性セットの名前が表示されます。 この名前は内部参照用であり、必要に応じて変更できます。
   - ページの中央には、属性グループの現在選択されている項目が一覧表示されます。
   - 右側の列には、属性セットに現在割り当てられていない属性の選択が一覧表示されます。

1. セットにアトリビュートを追加するには、 **[!UICONTROL Unassigned Attributes]** で適切なフォルダーにリストします **[!UICONTROL Groups]** 列。

   >[!NOTE]
   >
   >システム属性にはドットが付いており、から削除できません _[!UICONTROL Groups]_リスト。 ただし、属性セットの別のグループにドラッグすることはできます。

1. 完了したら、 **[!UICONTROL Save]**.

![属性セット – 編集](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## 属性グループの作成

1. が含まれる _[!UICONTROL Groups]_列に属性セットを設定し、クリックします&#x200B;**[!UICONTROL Add New]**.

1. を入力 **[!UICONTROL Name]** 新しいグループとして、をクリックします。 **[!UICONTROL OK]**.

1. 次のいずれかの操作をおこないます。

   - ドラッグ **[!UICONTROL Unassigned Attributes]** を新規グループに追加します。
   - 他のグループから新しいグループにアトリビュートをドラッグします。

   新しいグループは、属性セットに基づくすべての製品の属性のセクションになります。

## 属性セットの削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. リストで属性セットを選択し、編集モードで開きます。

1. クリック **[!UICONTROL Delete]**.

1. 確認を求められたら、 **[!UICONTROL OK]**.
