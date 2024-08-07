---
title: 製品タイプ
description: すべてのAdobe Commerce [!DNL Inventory Management] Magento Open Source商品タイプで在庫管理と注文管理をサポートする方法について説明します。
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 製品タイプ

[!DNL Inventory Management] は、Adobe CommerceおよびMagento Open Sourceのすべての商品タイプ（シンプル、設定可能、バーチャル、ダウンロード可能、バンドルおよびグループ化）の在庫管理および注文管理をサポートしています。 オプションと要件は、ソース、在庫、配送の製品タイプによって異なる場合があります。

- [ 単一ソースのマーチャント ](merchant-sourcing.md#single-source-merchants) は、追加の更新を必要とせずに、製品の設定と数量を作成および更新します。 作成および新しく読み込まれたすべての商品は、デフォルトのSourceとデフォルトの在庫に自動的に割り当てられ、有効になっている場合は直ちに顧客が使用できます。

- [ マルチソースマーチャント ](merchant-sourcing.md#multi-source-merchants) 製品の作成中または作成後に、ソース、ソースごとの数量および設定を割り当てます。 [!DNL Commerce] は、新しく読み込まれたすべての商品をデフォルトのSourceに割り当てるため、ソースと数量を割り当てる際に追加の編集が必要になります。

| 製品タイプ | 出荷およびSource選択アルゴリズム |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | 配送時の SSA の推奨事項と上書きをサポートします。 |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | 配送時の SSA の推奨事項と上書きをサポートします。 |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | 常に SSA 推奨を使用します。 システムは、請求書を作成する際にアルゴリズムを暗黙的に実行し、提案された結果を常に使用します。<br/> これらの結果は調整できません。 |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | 常に SSA 推奨を使用します。 システムは、請求書を作成する際にアルゴリズムを暗黙的に実行し、提案された結果を常に使用します。 <br/> これらの結果は調整できません。 |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | 配送時の SSA の推奨事項と上書きをサポートします。 |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | 配送時の SSA の推奨事項と上書きをサポートします。 |
