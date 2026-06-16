---
title: '[!DNL Commerce]件のアップグレード'
description: Adobe CommerceとMagento Open Sourceのアップグレードがカタログと [!DNL Inventory Management] 設定にどのような影響を与えるかを説明します。
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
TQID: https://experienceleague.adobe.com/rAnH5pJjtg4ujbQdHow-B6urN090iTTt19mv4sadVnc
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
source-wordcount: 749
ht-degree: 0%

---

# [!DNL Commerce]件のアップグレード

以前のリリースでシングルソースインベントリを使用した場合、この情報では、既存のカタログとインベントリ設定の新機能と変更の詳細が提供されます。

Adobe CommerceおよびMagento Open Sourceの[!DNL Inventory Management]には、すべての製品在庫管理を強化および更新し、新機能を追加する機能、機能強化、および開発者サポートが含まれています。 Source Selection AlgorithmやConcurrent Checkoutを含むあらゆる機能を、注文数をソースや注文フルフィルメントに一致させ、すぐに利用できます。 web サイト、実店舗、マーチャントのタイプに応じて、在庫とソースの追加、在庫量の割り当てなどを行うことができます。 詳細については、[Inventory management](introduction.md)を参照してください。

Magento Open Source 2.4.xまたはAdobe Commerce 2.4.xをインストールすると、次の最初の変更が発生します。

- [Inventory management](enable.md)は、グローバルストアまたは商品レベルで有効になります。 「在庫の管理」オプションを使用すると、在庫数量の追跡、集計販売可能数量の計算、および購入の追跡から請求書および出荷に至るまでの予約管理を有効または無効にできます。 ERPやその他のサードパーティサービスを使用して、在庫、注文、配送を管理する場合は、このオプションを無効にすることができます。 詳細については、以下の「[!DNL Inventory Management] モジュール」を参照してください。

- [既定のSource](sources-manage.md)と[既定のStock](stocks-manage.md)がシステムに追加されます。 これらのデフォルトを無効にしたり削除したりしないでください。 [!DNL Commerce]は、既存の製品と新しくインポートした製品をこれらのデフォルトに割り当てます。

  >[!IMPORTANT]
  >
  >既定のStockと既定のSourceの使用は、現在は非推奨となっている`CatalogInventory` モジュールの一部であるため、強くお勧めしません。 代わりに、カスタム在庫とソースを作成して使用することをお勧めします。

   - 在庫では、ショッピングカートや注文を追跡し、同時チェックアウトを保証するための予約とともに、集計されたバーチャル販売可能数量を提供します。

   - カタログ内のすべての既存商品は、デフォルトのSourceに割り当てられます。 新しいソースを追加するまで、製品インターフェイスは変更されません。 1つの場所からのみ製品を出荷する場合、ソースに他の違いはありません。 出荷場所ごとにカスタム [&#x200B; ソース &#x200B;](sources-add.md)と[数量](quantities-manage.md)を割り当てることができます。

   - ソースをピックアップ場所として設定し、そのソースに[数量](quantities-manage.md)を割り当てることができます。

   - Web サイトでは、デフォルトのストックに割り当てられます。 カスタム [在庫](stocks-add.md)を作成して、販売チャネル（web サイト）とソース（場所）を接続できます。

- 追加の[設定オプション &#x200B;](configuration.md)が製品とグローバルストアに追加されます。 既存の設定オプションの中には、更新されたオプションや動作を受け取るものもあります。

   - 「数量の通知」の下では、販売可能数量から通知と控除額が送信されます。

   - 在庫切れしきい値は、正の量、ゼロ、負の量をサポートします。 Backordersを有効にすると、正の量は無視され、ゼロ（または無限）と見なされます。

   - Backordersはゼロ（無限）とマイナスの量をサポートしています。 有効になっている場合、「次の数量に対する通知」は販売可能数量から差し引かれません。

- 新しい予約注文が出荷されたときに数量の差し引きに変換し、潜在的な売上を追跡します。 予約に直接アクセスしたり、作成したりすることはありません。 [!DNL Commerce]は、注文、発送、クレジットメモを通じて、予約をバックグラウンドで作成および管理します。

- [注文と配送](shipments.md)には、Source選択アルゴリズムを使用して配送を推奨し、複数のソースからの部分的な配送をサポートして注文を処理するための新機能が含まれています。

- 新しい[読み込み/書き出し機能](inventory-import-export.md)を使用すると、カタログ内のすべてのSKUのソースの一括追加、在庫量の更新、在庫ステータス（在庫切れ）の設定を行うことができます。 これらの機能を使用すると、1つ、選択した、またはすべてのソースを変更できます。

- 製品グリッドページを介した新しいバルクオプションでは、一括[&#x200B; ソースの割り当てと割り当て解除](bulk-assignment.md)および[&#x200B; ソースへの在庫の転送](inventory-transfer.md)がサポートされます。

- [!DNL Inventory Management]はB2B カタログをサポートしています。 現在のところ、すべてのB2B商品をDefault SourceとDefault Stockに割り当てる必要があります。

## [!DNL Commerce Order Management]と[!DNL Inventory Management]

[Commerce Order Management （MCOM） &#x200B;](https://commerce-docs.github.io/oms-documentation-archive/)は[!DNL Inventory Management]と互換性がありません。 MCOM モジュールをインストールすると、単一およびマルチソース管理、在庫、予約など、[!DNL Commerce]にすべての在庫管理機能が提供されます。 [!DNL Inventory Management] モジュールは既定では無効になっています。

MCOMは、高度なオムニチャネルの注文管理、グローバルな在庫とマルチソーシング、実店舗から倉庫へのフルフィルメント、一元化された顧客サービスなど、幅広い機能とサービスを提供しています。 機能の完全なリストについては、[MCOM機能リスト &#x200B;](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/)を参照してください。

[!DNL Inventory Management]は、処理中の注文、手元の在庫、在庫の利用可能な在庫、拡張機能の開発のためのAPIを追跡するための追加オプションを含む、既存の[!DNL Commerce]機能を拡張します。

## [!DNL Inventory Management]個のモジュール

[!DNL Inventory Management] モジュールを無効にして、次の操作を行うことができます。

- 現在Adobe CommerceまたはMagento Open Source 2.0/2.1/2.2/2.3にあるマーチャントのアップグレードを高速化し、2.4.xに移行します。

- カスタムまたはサードパーティの在庫管理および注文管理モジュールを使用します。

- 在庫管理に[!DNL Order Management System]を使用します。 現在のコネクタは[!DNL Inventory Management] インターフェイスをサポートしていません。 OMS マーチャントがAdobe Commerce 2.4.0にアップグレードする場合、これらのモジュールを無効にする必要があります。

詳細については、[&#x200B; インストールと更新](install-update.md)を参照してください。
