---
title: '[!DNL Commerce] アップグレード'
description: Adobe CommerceとMagento Open Sourceのアップグレードがカタログと設定に与える影響  [!DNL Inventory Management]  ついて説明します。
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce] アップグレード

以前のリリースで単一ソースのインベントリを使用した場合、この情報には、新機能の詳細と既存のカタログおよびインベントリ設定の変更点が含まれます。

Adobe CommerceおよびMagento Open Sourceの [!DNL Inventory Management] には、すべての product stock management を強化および更新し、新機能を追加する機能、機能強化およびデベロッパーサポートが含まれています。 Sourceの選択アルゴリズムと同時チェックアウトを含むすべての機能が標準で利用でき、注文数量をソースと注文フルフィルメントに照合できます。 Web サイト、店舗、マーチャントタイプに応じて、追加の在庫およびソースを作成したり、在庫金額を割り当てたりできます。 詳しくは、[Inventory management](introduction.md) を参照してください。

Magento Open Source 2.4.x またはAdobe Commerce 2.4.x をインストールすると、次の最初の変更が行われます。

- [Inventory management](enable.md) は、グローバル ストアまたは商品レベルで有効になります。 「在庫の管理」オプションを使用すると、在庫数量の追跡、集計した販売可能数量の計算、および請求書と出荷への購買を追跡するための予約管理を有効または無効にできます。 このオプションを無効にすると、在庫、受注および出荷の管理に ERP およびその他のサード・パーティ・サービスを使用できます。 詳しくは、以下の [!DNL Inventory Management] モジュールを参照してください。

- [&#x200B; デフォルトのSource](sources-manage.md) と [&#x200B; デフォルトの在庫 &#x200B;](stocks-manage.md) がシステムに追加されます。 これらのデフォルトを無効にしたり削除したりしないでください。 [!DNL Commerce] では、既存の製品と新しく読み込んだ製品をこれらのデフォルトに割り当てます。

  >[!IMPORTANT]
  >
  >デフォルトの在庫およびデフォルトのSourceは、現在非推奨となっている `CatalogInventory` モジュールの一部なので、使用することは強くお勧めしません。 カスタムの在庫とソースを作成して使用することをお勧めします。

   - 在庫は、買い物かごと注文を追跡するための予約を含む、集計された仮想販売可能数量を提供し、同時チェックアウトを保証します。

   - カタログ内の既存の商品はすべて、デフォルトのSourceに割り当てられます。 新しいソースを追加するまで、製品インターフェイスは変更されません。 1 つの場所からのみ製品を出荷する場合、ソースに関するその他の違いはありません。 出荷事業所ごとにカスタム [&#x200B; ソース &#x200B;](sources-add.md) および [&#x200B; 数量の割当 &#x200B;](quantities-manage.md) を作成できます。

   - ソースを集荷場所として設定し、そのソースに対して [&#x200B; 数量を割り当て &#x200B;](quantities-manage.md) ことができます。

   - Web サイトがデフォルトの在庫に割り当てられます。 カスタム [&#x200B; 在庫 &#x200B;](stocks-add.md) を作成して、販売チャネル（web サイト）とソース（場所）を接続できます。

- 追加の [&#x200B; 設定オプション &#x200B;](configuration.md) を製品およびグローバルストアに追加します。 一部の既存の設定オプションには、更新されたオプションと動作が含まれています。

   - 数量の通知下記では、通知を送信し、販売可能数量から控除します。

   - 在庫切れのしきい値は、正の金額、ゼロおよび負の金額をサポートします。 「バックオーダー」を使用可能にすると、プラスの金額は無視され、ゼロ（または無限）とみなされます。

   - バックオーダーでは、ゼロ（無限）およびマイナスの金額がサポートされます。 有効になっている場合、下記の数量の通知は販売可能数量から差し引かれません。

- 新規予約では、受注が出荷されたときに数量控除に変換され、潜在的な売上が追跡されます。 予約に直接アクセスしたり、予約を作成したりすることはできません。 [!DNL Commerce] は、注文、出荷、クレジット・メモを通じて予約を作成し、バックグラウンドで管理します。

- [&#x200B; 注文と出荷 &#x200B;](shipments.md) には、Source選択アルゴリズムを使用して出荷を推奨する新機能が含まれており、複数のソースからの一部の出荷をサポートして注文を履行します。

- 新しい [&#x200B; 読み込み/書き出し機能 &#x200B;](inventory-import-export.md) を使用すると、カタログ内のすべての SKU について、ソースの一括追加、在庫数量の更新、在庫ステータスの設定（在庫の有無）を行うことができます。 これらの機能を使用すると、1 つのソース、選択したソース、またはすべてのソースを変更できます。

- 製品グリッドページを通じた新しい一括オプションは、一括 [&#x200B; ソースの割り当てと割り当て解除 &#x200B;](bulk-assignment.md) および [&#x200B; ソースへの在庫の転送 &#x200B;](inventory-transfer.md) をサポートしています。

- [!DNL Inventory Management] は B2B カタログをサポートします。 現在、すべての B2B 製品をデフォルトのSourceとデフォルトの在庫に割り当てる必要があります。

## [!DNL Commerce Order Management] と [!DNL Inventory Management]

[Commerce Order Management （MCOM） &#x200B;](https://commerce-docs.github.io/oms-documentation-archive/) は [!DNL Inventory Management] と互換性がありません。 MCOM モジュールをインストールすると、シングルソースおよびマルチソースの管理、在庫、予約など、すべての在庫管理機能が [!DNL Commerce] に提供されます。 [!DNL Inventory Management] のモジュールは、デフォルトで無効になっています。

MCOM は、高度なオムニチャネル注文管理、グローバルな在庫およびマルチソーシング、倉庫への保管フルフィルメント、一元化されたカスタマーサービスのための豊富な機能とサービスを提供します。 機能の完全な一覧については、[MCOM 機能の一覧 &#x200B;](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/) を参照してください。

[!DNL Inventory Management] は、既存の [!DNL Commerce] 機能を拡張し、追加のオプションを使用して処理中の注文、手持在庫、在庫用の利用可能な在庫、拡張機能の開発のための API を追跡します。

## [!DNL Inventory Management] モジュール

[!DNL Inventory Management] のモジュールを無効にすると、次の操作を実行できます。

- 現在、Adobe CommerceまたはMagento Open Source 2.0/2.1/2.2/2.3 にあり、2.4.x に移行しているマーチャントのアップグレードを迅速化します。

- カスタムまたはサードパーティの在庫および注文管理モジュールを使用します。

- 在庫管理に [!DNL Order Management System] を使用します。 現在のコネクタは、[!DNL Inventory Management] インターフェイスをサポートしていません。 Adobe Commerce 2.4.0 にアップグレードする OMS マーチャントの場合、これらのモジュールを無効にする必要があります。

詳しくは、[&#x200B; インストールとアップデート &#x200B;](install-update.md) を参照してください。
