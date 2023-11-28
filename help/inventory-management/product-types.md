---
title: 製品タイプ
description: 方法を学ぶ [!DNL Inventory Management] は、すべてのAdobe CommerceおよびMagento Open Source製品タイプの在庫と注文の管理をサポートしています。
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 製品タイプ

[!DNL Inventory Management] は、Adobe CommerceおよびMagento Open Sourceのすべての製品タイプ（シンプル、設定可能、仮想、ダウンロード可能、バンドル、グループ化）の在庫と注文の管理をサポートします。 オプションと要件は、ソース、在庫、送料の製品タイプごとに異なる場合があります。

- [単一ソースのマーチャント](merchant-sourcing.md#single-source-merchants) 追加の更新を必要とせずに、製品設定と数量を作成および更新できます。 作成および新規に読み込まれたすべての製品は、デフォルトのソースとデフォルトの在庫に自動的に割り当てられ、有効化されていて在庫がある場合は、すぐに利用できます。

- [マルチソースマーチャント](merchant-sourcing.md#multi-source-merchants) 製品作成中または後に、ソース、ソースごとの数量、および設定を割り当てます。 [!DNL Commerce] は、新しく読み込まれたすべての製品を「デフォルトソース」に割り当て、ソースと数量の割り当てに追加の編集を必要とします。

| 製品タイプ | 発送およびソース選択アルゴリズム |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | 出荷時に SSA の推奨と上書きをサポートします。 |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | 出荷時に SSA の推奨と上書きをサポートします。 |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | 常に SSA レコメンデーションを使用します。 請求書の作成時にアルゴリズムが暗黙的に実行され、常に推奨結果が使用されます。<br/>これらの結果は調整できません。 |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | 常に SSA レコメンデーションを使用します。 請求書の作成時にアルゴリズムが暗黙的に実行され、常に推奨結果が使用されます。 <br/>これらの結果は調整できません。 |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | 出荷時に SSA の推奨と上書きをサポートします。 |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | 出荷時に SSA の推奨と上書きをサポートします。 |
