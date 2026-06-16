---
title: 製品ワークスペース
description: 製品ワークスペースで使用できる設定とコントロールについて説明します。
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
TQID: https://experienceleague.adobe.com/O9e0Z-bHxbokLZd4RbT1puWWAGWnF7SDqvGcc4Bteco
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 467
ht-degree: 0%

---

# 製品ワークスペース

製品ワークスペースは、使用する属性セットによってフィールドの選択が変わりますが、基本的にはすべての製品タイプで同じです。 製品属性がフォームの上部にあり、その後に製品情報の拡張可能なセクションが続きます。 新しい製品を初めて保存すると、フォームの左上に&#x200B;_[!UICONTROL Store View]_&#x200B;の選択画面が表示されます。

![製品ワークスペース &#x200B;](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product]設定

製品のオンラインステータスは、フォームの上部にあるスイッチで示されます。 オンライン状態を変更するには、**[!UICONTROL Enable Product]** スイッチを`Yes`または`No`に設定します。

| 制御 | 説明 |
|-------- | ----------- |
| ![はい](../assets/toggle-yes.png)に切り替え | 製品がオンラインであることを示します。 |
| ![No](../assets/toggle-no.png)を切り替え | 製品がオフラインであることを示します。 |

{style="table-layout:auto"}

## 属性セット

[属性セット &#x200B;](attribute-sets.md)の名前が左上隅に表示され、製品レコードに表示されるフィールドが決定されます。 別の属性セットを選択するには、デフォルトの属性セット名の横にある下向き矢印をクリックします。

![属性セット &#x200B;](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## 展開/折りたたみ

セクションを展開または折りたたむには、「![拡張セレクター](../assets/icon-display-expand.png)」を展開または「![&#x200B; セレクターを折りたたむ](../assets/icon-display-collapse.png)」アイコンをクリックします。

## [!UICONTROL Save] メニュー

_[!UICONTROL Save]_&#x200B;メニューには、製品の保存と続行、製品の保存と作成、製品の保存と複製、または保存と閉じることができるいくつかのオプションが含まれています。

![&#x200B; メニューを保存](./assets/product-save-menu.png){width="600" zoomable="yes"}

| コマンド | 説明 |
|--- |--- |
| [!UICONTROL Save] | 現在の製品を保存して作業を続行します。 |
| [!UICONTROL Save & New] | 現在の製品を保存して閉じ、同じ製品タイプとテンプレートに基づいて新しい製品を開始します。 |
| [!UICONTROL Save & Duplicate] | 現在の製品を保存して閉じ、新しい重複コピーを開きます。 |
| [!UICONTROL Save & Close] | 現在の製品を保存して、_[!UICONTROL Products]_&#x200B;ワークスペースに戻ります。 |

{style="table-layout:auto"}

## デフォルトのフィールド値

製品を作成する際の時間を節約するために、複数の製品フィールドのデフォルト値は、別のフィールドの値を参照します。 デフォルト値を受け入れるか、別の値を入力します。 次のフィールドは自動的にデフォルト値を生成します。

| フィールド | Default |
|----- |------- |
| [!UICONTROL SKU] | 商品名にもとづいて。 |
| [!UICONTROL Meta Title] | 商品名にもとづいて。 |
| [!UICONTROL Meta Keywords] | 商品名にもとづいて。 |
| [!UICONTROL Meta Description] | 商品名と説明にもとづいて傾向スコアを生成できます。 |

{style="table-layout:auto"}

別のフィールドの値を表すプレースホルダーは、二重中括弧で囲まれています。 製品[属性セット &#x200B;](attribute-sets.md)に含まれるすべての属性コードをプレースホルダーとして使用できます。

![製品フィールドの自動生成](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

これらの設定の詳細なリストについては、_設定リファレンス_&#x200B;の[製品フィールド自動生成](../configuration-reference/catalog/catalog.md#product-fields-auto-generation)を参照してください。

### プレースホルダー値の編集

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Product Fields Auto-Generation]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、必要に応じてプレースホルダー値を変更します。

   例えば、製品ごとに含める特定のキーワードや、すべてのメタディスクリプションに含めるフレーズがある場合は、適切なフィールドに値を直接入力します。

   >[!NOTE]
   >
   >既存のプレースホルダー値を保持する場合は、各マークアップタグを囲む二重中括弧を保持します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

### 共通プレースホルダー

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`
