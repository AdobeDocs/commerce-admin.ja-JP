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

商品ワークスペースは、基本的にすべての商品タイプで同じですが、フィールドの選択は、使用する属性セットに応じて変わります。 製品属性はフォームの上部に表示され、その後に製品情報の展開可能なセクションが表示されます。 新しい製品を初めて保存すると、 _[!UICONTROL Store View]_chooser は、フォームの左上に表示されます。

![製品ワークスペース](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product] 設定

製品のオンラインステータスは、フォーム上部のスイッチで示されます。 オンラインステータスを変更するには、 **[!UICONTROL Enable Product]** に切り替える `Yes` または `No`.

| 制御 | 説明 |
|-------- | ----------- |
| ![はいを切り替え](../assets/toggle-yes.png) | 製品がオンラインであることを示します。 |
| ![切り替えなし](../assets/toggle-no.png) | 製品がオフラインであることを示します。 |

{style="table-layout:auto"}

## 属性セット

の名前 [属性セット](attribute-sets.md) は左上隅に表示され、製品レコードに表示するフィールドを決定します。 別の属性セットを選択するには、デフォルトの属性セット名の横にある下向き矢印をクリックします。

![属性セット](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## 展開/折りたたむ

セクションを展開または折りたたむには、展開 ![拡張セレクター](../assets/icon-display-expand.png) または折りたたむ ![折りたたみセレクター](../assets/icon-display-collapse.png) アイコン。

## [!UICONTROL Save] メニュー

The _[!UICONTROL Save]_メニューには、保存と続行、製品の保存と作成、製品の保存と複製、または保存と閉じることができるオプションがいくつか含まれています。

![保存メニュー](./assets/product-save-menu.png){width="600" zoomable="yes"}

| コマンド | 説明 |
|--- |--- |
| [!UICONTROL Save] | 現在の製品を保存し、作業を続行します。 |
| [!UICONTROL Save & New] | 現在の製品を保存して閉じ、同じ製品タイプとテンプレートに基づいて新しい製品を開始します。 |
| [!UICONTROL Save & Duplicate] | 現在の製品を保存して閉じ、新しい複製コピーを開きます。 |
| [!UICONTROL Save & Close] | 現在の製品を保存し、に戻ります。 _[!UICONTROL Products]_ワークスペース。 |

{style="table-layout:auto"}

## デフォルトのフィールド値

製品を作成する際に時間を節約するために、複数の製品フィールドのデフォルト値が別のフィールドの値を参照します。 デフォルト値を受け入れるか、別の値を入力することができます。 次のフィールドでは、デフォルト値が自動的に生成されます。

| フィールド | デフォルト |
|----- |------- |
| [!UICONTROL SKU] | 製品名に基づきます。 |
| [!UICONTROL Meta Title] | 製品名に基づきます。 |
| [!UICONTROL Meta Keywords] | 製品名に基づきます。 |
| [!UICONTROL Meta Description] | 製品名と説明に基づきます。 |

{style="table-layout:auto"}

別のフィールドの値を表すプレースホルダーは二重中括弧で囲みます。 製品に含まれる任意の属性コード [属性セット](attribute-sets.md) はプレースホルダーとして使用できます。

![製品フィールドの自動生成](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

これらの設定の詳細なリストについては、 [製品フィールドの自動生成](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) （内） _設定リファレンス_.

### プレースホルダー値を編集

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Product Fields Auto-Generation]** 」セクションに移動し、必要に応じてプレースホルダーの値を変更します。

   例えば、すべての製品に対して特定のキーワードを含めたい場合や、すべてのメタ説明に含めるフレーズがある場合は、該当するフィールドに値を直接入力します。

   >[!NOTE]
   >
   >既存のプレースホルダ値を保持する場合は、各マークアップタグを囲む二重中括弧を保持します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

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
