---
title: 製品タイプ
description: ' [!DNL Inventory Management] が、すべてのAdobe CommerceおよびMagento Open Source製品タイプの在庫管理と注文管理をどのようにサポートしているかをご覧ください。'
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 213
ht-degree: 0%

---

# 製品タイプ

[!DNL Inventory Management]は、シンプル、設定可能、バーチャル、ダウンロード可能、バンドル、グループ化など、Adobe CommerceとMagento Open Sourceのすべての商品タイプの在庫管理と注文管理をサポートしています。 オプションと要件は、ソース、在庫、配送の製品タイプによって異なる場合があります。

- [&#x200B; シングルソースマーチャント &#x200B;](merchant-sourcing.md#single-source-merchants)は、追加の更新を必要とせずに、製品設定と数量を作成および更新します。 作成および新規に読み込まれたすべての商品は、デフォルトのSourceおよびデフォルトのStockに自動的に割り当てられます。有効になっている場合や在庫がある場合は、すぐに利用できます。

- [&#x200B; マルチソースマーチャント &#x200B;](merchant-sourcing.md#multi-source-merchants)は、製品作成中または作成後に、ソース、ソースごとの数量、設定を割り当てます。 [!DNL Commerce]では、新しくインポートされたすべての商品がデフォルトのSourceに割り当てられるため、ソースと数量を割り当てるために追加の編集が必要です。

| 製品タイプ | 配送とSourceの選択アルゴリズム |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | 出荷時のSSAの推奨事項とオーバーライドをサポートします。 |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | 出荷時のSSAの推奨事項とオーバーライドをサポートします。 |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | 常にSSA レコメンデーションを使用します。 請求書の作成時にアルゴリズムが暗黙的に実行され、常に提案された結果が使用されます。<br/>これらの結果は調整できません。 |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | 常にSSA レコメンデーションを使用します。 請求書の作成時にアルゴリズムが暗黙的に実行され、常に提案された結果が使用されます。 <br/>これらの結果は調整できません。 |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | 出荷時のSSAの推奨事項とオーバーライドをサポートします。 |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | 出荷時のSSAの推奨事項とオーバーライドをサポートします。 |
