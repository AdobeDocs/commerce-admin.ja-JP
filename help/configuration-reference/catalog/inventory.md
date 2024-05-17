---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: の設定を確認します。 [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] コマース管理者のページ。
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 768c9fdc37127b408230983e39e98b11149713a7
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] Adobe CommerceおよびMagento Open Sourceの場合、商品インベントリを管理するツールを提供します。 複数の倉庫、店舗、集荷場所、直荷主などに 1 つの店舗を持つマーチャントは、これらの機能を使用して販売の数量を管理し、注文を完了するための出荷を処理できます。 これらの機能の詳細と、それらを使用して複数の場所で在庫を管理する方法については、を参照してください [_[!DNL Inventory Management] ユーザーガイド&#x200B;_](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![在庫オプション](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | グローバル | に設定されている場合 `Yes`注文する際に、在庫数を減らします。 （を使用） _在庫の管理_ 有効にすると、注文された製品と数量に対して予約が入力されます。 オプション： `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | ストア表示 | に設定されている場合 `Yes`注文がキャンセルされると、品目を在庫に戻します。 （を使用） _在庫の管理_ 有効にすると、キャンセルされた製品および数量の予約がクリアされます。 オプション： `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | グローバル | に設定されている場合 `Yes`、在庫切れの製品を表示します。 製品アラートも有効になっている場合は、ユーザーは登録して、製品が利用可能になった際に通知を受け取ることができます。 オプション： `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Web サイト | しきい値を設定します。 `Only x left` メッセージ。 例えば、3 に設定した場合、在庫の品目が 3 個以下になるとメッセージが表示されます。 値がに設定されている場合、メッセージは表示されません `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | ストア表示 | に設定されている場合 `Yes`。が表示されます `In Stock` または `Out of Stock` 製品ページのメッセージ。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | グローバル | 買い物かごに商品を読み込む際に在庫チェックを実行するかどうかを決定します。 このインベントリチェックを無効にすると、特に、買い物かごに多くの商品がある場合に、チェックアウト手順のパフォーマンスが向上します。 ただし、事前検証をスキップした場合は、次が表示される可能性があります _在庫切れ_ チェックアウトプロセスの後半でエラーが発生します。 オプション： `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | グローバル | に設定されている場合 `Yes`は、カタログの変更（製品の削除、製品 SKU の変更、製品タイプの変更など）に従って在庫データが調整され、在庫とカタログの一貫性が維持されます。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![製品ストックオプション](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | グローバル | 完全な在庫管理を使用してカタログ内の品目を管理するかどうかを決定します。 オプション： <br/>**はい**  – 現在在庫にある項目数を追跡するために、完全な在庫管理を有効化します。 <br/>**不可**  – 現在在庫のある項目数は追跡されません。 |
| [!UICONTROL Backorders] | グローバル | 店舗でのバックオーダーの管理方法を決定します。 バックオーダーによってオーダーの処理ステータスが変更されることはありません。 ファンドは、商品が在庫しているかどうかに関係なく、注文が行われるとすぐに承認または取得されます。 製品が利用可能になると、出荷されます。 オプション： <br/>**バックオーダーなし**  – 商品の在庫切れ時にバックオーダーを受け付けません。 <br/>**0 未満の数量を許可**  – 数量がゼロを下回った場合にバックオーダーを受け入れます。 <br/>**0 未満の数量を許可し、お客様に通知**  – 数量がゼロを下回った場合はバックオーダーを受け入れますが、オーダーは引き続き発注可能であることを顧客に通知します。 |
| [!UICONTROL Use deferred Stock update] | グローバル | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）バックオーダーが許可されている場合に、在庫更新を延期するかどうかを指定します（ _バックオーダー_ オプションがに設定されています。 `No backorders` デフォルト値）。 単一の製品または web サイト全体で機能し、 _ジョブキュー_ 注文が行われた後に在庫数量インジケーターを非同期で更新できるようにするメカニズム。 このオプションはでも機能します [非同期注文の配置](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) ～と組み合わせて [Inventory management](../../inventory-management/introduction.md). |
| 買い物かごで許可される最大数量 | グローバル | 1 回の注文で購入できる商品の最大数を決定します。 デフォルトでは、最大数量は 10,000 に設定されています。 |
| [!UICONTROL Out-of-Stock Threshold] | グローバル | 商品が在庫切れとみなされる在庫レベルを決定します。 オプション： <br/>**正の金額**  – を使用 _バックオーダー_ 無効にする場合は、正の値を入力します。 「バックオーダー」が有効化されている場合、この金額は無視されます。 <br/>**ゼロ**  – を使用 _バックオーダー_ 有効、入力する `0` 無制限のバックオーダーが可能になります。 <br/>**マイナスの金額**  – を使用 _バックオーダー_ 有効にする場合は、マイナスの金額を入力することをお勧めします。 金額は販売可能数量に追加されます。 例えば、-50 と入力すると、この金額までの注文が許可されます。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | グローバル | 顧客グループに応じて、購入できる商品の最小金額を決定します。 デフォルトでは、最小数量は 1 に設定されています。 クリック **[!UICONTROL Add Minimum Qty]** 特定の顧客グループに対して別の値を入力します。 |
| [!UICONTROL Notify for Quantity Below] | グローバル | 在庫がしきい値を下回ったという通知が送信される在庫レベルを決定します。 |
| [!UICONTROL Enable Qty Increments] | グローバル | 品目を数量単位で販売できるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Qty Increments] | グローバル | 増分量を構成する製品の数を設定します。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | グローバル | クレジット メモに含まれる品目を自動的に在庫に返すかどうかを決定します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![管理の一括操作](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

>[!NOTE]
>
>とサポートを設定するには **非同期キューマネージャー**&#x200B;の場合は、コマンドラインを使用する必要があります。 これには、開発者の支援が必要になる場合があります。 参照： [メッセージキューコンシューマーの開始](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) が含まれる _設定ガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | グローバル | 次のような一括製品アクションに対して一括操作を非同期で実行するかどうかを指定します [一括](../../inventory-management/bulk-assignment.md) ソースの割り当て、ソースの割り当て解除、 [在庫をソースに転送](../../inventory-management/inventory-transfer.md). 最大で一括アクションを収集します _[!UICONTROL Asynchronous batch size]_その後、これらのアクションを実行します。 この機能は、デフォルトでは無効になっています。 有効にする前に、一括アクションでパフォーマンスを確認することをお勧めします。 オプション：<br/>**`Yes`**– のすべての一括操作を実行します [!DNL Inventory Management] 非同期。 有効にするには、非同期キューマネージャーを設定する必要があります。<br/>**`No`**- デフォルト。 一括操作を非同期で実行しません。 |
| [!UICONTROL Asynchronous batch size] | グローバル | を設定 **[!UICONTROL Run asynchronously]** 対象： `Yes` に値を入力するには _[!UICONTROL Asynchronous batch size]_フィールド。 <br/>デフォルトバッチサイズは 100 です。 バルクプロセスがこの量に達すると、実行されます。 |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | グローバル | ストック/ソースのインデックス再作成に使用する方法を決定します。 オプション： `Synchronous` / `Asynchronous` （非同期キューマネージャーは非同期モードに設定する必要があります） |

{style="table-layout:auto"}

>[!NOTE]
>
> 注文関連アクティビティの在庫更新の依存関係により、次の条件にかかわらず、製品の保存時にも在庫インデクサーがトリガーされます `Synchronous` または `Asynchronous` の設定値。


## [!UICONTROL Distance Provider for Distance Based SSA]

![距離ベースの SSA の距離プロバイダ](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Provider] | グローバル | 距離優先ソース選択アルゴリズムに使用するプロバイダを決定します。 この機能はデフォルトで有効になっています。 オプション： <br/>**`Google MAP`**-Google サービスを使用して、発送先住所と発送元場所（住所および GPS 座標）の間の距離と時間を計算します。 このオプションにはGoogle API キーが必要で、Google経由で料金が発生する場合があります。<br/>**`Offline Calculation`**  – 埋め込みデータベースを使用して距離を計算し、配送先住所に最も近いソースを特定します。 このオプションを使用するには、コマンドラインを使用して出荷するすべての国のデータベースの場所のコンテンツを最初にダウンロードするために、開発者の支援が必要になる場合があります。 |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google距離プロバイダー](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Google API key] | グローバル | Google MAP プロバイダーのGoogle API キーを入力します。 キーはです [!DNL Google Maps Platform] および次を持つ必要があります [!DNL Geocoding API] および [!DNL Distance Matrix API] 有効。 詳しくは、を参照してください [距離優先アルゴリズムの設定](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) が含まれる _Inventory management ガイド_. |
| [!UICONTROL Computation mode] | グローバル | 配送先住所と在庫に割り当てられたすべてのソースからの距離を計算する方向とパスを決定します。 既定では、計算は運転モードを使用します。 オプション： <br/>**`Driving`**- デフォルト設定。道路ネットワークを使用して標準走行方向を要求します。<br/>**`Walking`**  – 歩行者用道路および歩道（利用可能な場合）を使用して歩行方向をリクエストします。 <br/>**`Bicycling`**・自転車道および優先ストリートを利用した自転車道案内のリクエスト（現在、米国および一部のカナダ都市のみ利用可能） |
| [!UICONTROL Value] | グローバル | 出荷先所在地への出荷元事業所の距離と時間の計算対象と返品対象を示します。 距離優先アルゴリズムでは、出荷先住所までの距離または時間が最も短いソースをお勧めします。これにより、出荷を満たすためにより速く、より安価になります。 オプション： <br/>**`Distance`**- ポイント間の距離を、メートル（キロメートルとメートル）またはフィート（インチ/フィート）単位で返します。<br/>**`Time to Destination`**  – 発送元の場所から配送先住所への移動に必要な時間を時間と分単位で返します。 |

{style="table-layout:auto"}
