---
title: 製品ワークスペース
description: 製品ワークスペースで使用できる設定とコントロールについて説明します。
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# 製品ワークスペース

製品ワークスペースは、すべての製品タイプで基本的に同じですが、フィールドの選択は、使用する属性セットによって変わります。 製品属性はフォームの上部に表示され、その後に商品情報の展開可能なセクションが続きます。 新しい製品を初めて保存する場合、 _[!UICONTROL Store View]_選択はフォームの左上に表示されます。

![製品ワークスペース](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product] 設定

製品のオンラインステータスは、フォーム上部のスイッチで示されます。 オンラインステータスを変更するには、 **[!UICONTROL Enable Product]** 切り替え先 `Yes` または `No`.

| 制御 | 説明 |
|-------- | ----------- |
| ![「はい」を切り替え](../assets/toggle-yes.png) | 製品がオンラインであることを示します。 |
| ![いいえ切り替え](../assets/toggle-no.png) | 製品がオフラインであることを示します。 |

{style="table-layout:auto"}

## 属性セット

の名前 [属性セット](attribute-sets.md) は左上隅に表示され、製品レコードに表示されるフィールドを決定します。 別の属性セットを選択するには、デフォルトの属性セット名の横にある下向き矢印をクリックします。

![属性セット](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## 展開/折りたたむ

セクションを展開または折りたたむには、展開をクリックします ![展開セレクター](../assets/icon-display-expand.png) または折りたたむ ![セレクターを折りたたむ](../assets/icon-display-collapse.png) アイコン。

## [!UICONTROL Save] メニュー

この _[!UICONTROL Save]_メニューには、保存して続行、製品を保存して作成、製品を保存して複製、保存して閉じるなどの操作を行える複数のオプションが含まれています。

![保存メニュー](./assets/product-save-menu.png){width="600" zoomable="yes"}

| コマンド | 説明 |
|--- |--- |
| [!UICONTROL Save] | 現在の製品を保存して、作業を続行します。 |
| [!UICONTROL Save & New] | 現在の製品を保存して閉じ、同じ製品タイプとテンプレートに基づいて新しい製品を開始します。 |
| [!UICONTROL Save & Duplicate] | 現在の製品を保存して閉じ、新しい複製コピーを開きます。 |
| [!UICONTROL Save & Close] | 現在の製品を保存し、に戻ります _[!UICONTROL Products]_ワークスペース。 |

{style="table-layout:auto"}

## デフォルトのフィールド値

製品の作成時に時間を節約するために、複数の製品フィールドのデフォルト値は別のフィールドの値を参照します。 デフォルト値をそのまま使用するか、別の値を入力します。 次のフィールドには、デフォルト値が自動的に生成されています。

| フィールド | デフォルト |
|----- |------- |
| [!UICONTROL SKU] | 製品名に基づいています。 |
| [!UICONTROL Meta Title] | 製品名に基づいています。 |
| [!UICONTROL Meta Keywords] | 製品名に基づいています。 |
| [!UICONTROL Meta Description] | 製品名と説明に基づいています。 |

{style="table-layout:auto"}

別のフィールドの値を表すプレースホルダーは、二重中括弧で囲まれています。 製品に含まれる属性コード [属性セット](attribute-sets.md) プレースホルダーとして使用できます。

![製品フィールドの自動生成](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

これらの設定の詳細なリストについては、を参照してください [製品フィールドの自動生成](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) が含まれる _設定リファレンス_.

### プレースホルダー値の編集

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Product Fields Auto-Generation]** をセクション化し、必要な変更をプレースホルダー値に加えます。

   例えば、すべてのメタ説明に含めるすべての製品またはフレーズに含める特定のキーワードがある場合は、適切なフィールドに直接値を入力します。

   >[!NOTE]
   >
   >既存のプレースホルダー値を保持する場合は、各マークアップタグを囲む二重中括弧を保持します。

1. 完了したら、 **[!UICONTROL Save Config]**.

### 共通のプレースホルダー

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`
