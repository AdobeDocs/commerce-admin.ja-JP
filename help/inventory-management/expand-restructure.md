---
title: 在庫の拡大と再構築
description: マルチソースのマーチャントに拡大する方法や、シングルソースのマーチャントに縮小する方法を説明します。
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 219
ht-degree: 0%

---

# 在庫の拡大と再構築

ビジネスの成長や変化に合わせて、[!DNL Inventory Management]はお客様のニーズをサポートします。 マルチソースのマーチャントに拡張することも、シングルソースのマーチャントに容易に縮小することもできます。

## マルチソースに拡張

シングルソースの加盟店は、新しい店舗、倉庫、ドロップシッパーなどを追加することができます。 拡張するには、マルチソーシングに拡張するためにいくつかの追加と在庫の更新が必要です。

1. 新しい場所ごとに[&#x200B; カスタムソース &#x200B;](sources-add.md)を追加します。

   バンドル商品には、デフォルトのSourceのみを使用します。

1. 新しいソースに対して、必要に応じて[&#x200B; カスタム在庫](stocks-add.md)を追加します。

   例えば、web サイト、国、ロケール、またはその他の方法ごとにストックを作成できます。 カスタム在庫にソースを割り当てることができます。 バンドル製品にはデフォルトのStockのみを使用します。

1. 製品の[&#x200B; ソース割り当てと数量](quantities-manage.md)を更新します。

   また、[一括処理ツール &#x200B;](bulk-assignment.md)および[読み込み/書き出し](inventory-import-export.md)機能を使用して、ソースと製品データをすばやく追加することもできます。

## シングルソースに再構築

オンラインセールスを一箇所に減らして配送したいマルチソースマーチャントの場合、ソース、在庫、数量を変更して更新します。

1. [&#x200B; カスタムソース &#x200B;](sources-disable.md)を無効にします。

1. 商品の在庫をデフォルトのSourceに転送します。

   マスアクションを使用することをお勧めします。 [Sourceへの在庫の転送](inventory-transfer.md)を参照してください。

1. すべてのWeb サイトを[既定のStock](stocks-manage.md)に割り当てます。
