---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: 次のページで設定を確認します： [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] コマース管理のページ。
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 80630957dbe25d21c45f64d8027a39b7b396619d
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] Adobe CommerceとMagento Open Sourceの場合は、製品の在庫を管理するためのツールが提供されます。 複数の倉庫、店舗、受け取り場所、受け取り場所、受け取り船などに 1 つの店舗を持つ商人は、これらの機能を使用して、販売数量を維持し、受注を完了するために出荷を処理できます。 これらの機能と、それらを使用して複数の場所で在庫を管理する方法について詳しくは、 [_[!DNL Inventory Management] ユーザーガイド&#x200B;_](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![在庫オプション](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | グローバル | に設定した場合、 `Yes`を指定すると、注文時に在庫数量が減少します。 を使用 _在庫の管理_ 有効にすると、注文した製品と数量に対して予約が入力されます。 オプション： `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | ストア表示 | に設定した場合、 `Yes`。注文がキャンセルされると、品目が在庫に戻されます。 を使用 _在庫の管理_ 有効にすると、キャンセルされた製品と数量の予約が消去されます。 オプション： `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | グローバル | に設定した場合、 `Yes`「 」は、在庫切れの製品を表示します。 製品アラートも有効になっている場合は、新規登録して、製品が利用可能になった時点で通知を受け取ることができます。 オプション： `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Web サイト | のしきい値を設定します。 `Only x left` メッセージ。 例えば、3 に設定した場合、在庫が 3 つ以下のアイテムがあるときにメッセージが表示されます。 値が `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | ストア表示 | に設定した場合、 `Yes`、には、 `In Stock` または `Out of Stock` メッセージが表示されます。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | グローバル | 買い物かごに製品を読み込む際に在庫チェックを実行するかどうかを指定します。 この在庫チェックを無効にすると、特に買い物かごに多数の品目がある場合に、チェックアウト手順のパフォーマンスを向上させることができます。 ただし、事前検証をスキップすると、 _在庫切れ_ エラーについては、後でチェックアウトプロセスで説明します。 オプション： `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | グローバル | に設定する場合 `Yes`、在庫データは、カタログの変更（製品の削除、製品の SKU の変更、製品の種類の変更など）に従って調整され、在庫とカタログとの一貫性が維持されます。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Product Stock Options]

![製品在庫オプション](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | グローバル | カタログ内の項目を管理するために、完全な在庫管理を使用するかどうかを指定します。 オプション： <br/>**はい**  — 現在在庫中の品目数を追跡するために、完全な在庫管理を有効化します。 <br/>**いいえ**  — 現在在庫されている品目の数を追跡しません。 |
| [!UICONTROL Backorders] | グローバル | 店舗でのバックオーダーの管理方法を決定します。 バックオーダーでは、オーダーの処理ステータスは変更されません。 商品が在庫にあるかどうかに関係なく、注文が行われると、資金は引き続き直ちに承認または取得されます。 製品が入手可能になると、その製品は出荷されます。 オプション： <br/>**バックオーダーがありません**  — 製品が在庫切れの場合は、バックオーダーを受け入れません。 <br/>**0 未満の数量を許可**  — 数量がゼロを下回った場合は、バックオーダーを受け入れます。 <br/>**0 未満の数量を許可し、顧客に通知**  — 数量がゼロを下回った場合はバックオーダーを受け入れますが、注文は依然として発注可能であることを顧客に通知します。 |
| [!UICONTROL Use deferred Stock update] | グローバル | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) バックオーダーが許可される場合に在庫更新を延期するかどうかを決定します ( _バックオーダー_ オプションは、 `No backorders` デフォルト値 )。 単一の製品または Web サイト全体で機能し、 _ジョブキュー_ メカニズムを使用して、注文がおこなわれた後、在庫数量指標を非同期で更新できるようにします。 また、このオプションは [非同期の注文プレースメント](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) ～と組み合わせて [Inventory management](../../inventory-management/introduction.md). |
| 買い物かごで許可される最大数量 | グローバル | 1 回の注文で購入できる製品の最大数を決定します。 デフォルトでは、最大数量は 10,000 に設定されています。 |
| [!UICONTROL Out-of-Stock Threshold] | グローバル | 製品が在庫切れと見なされる在庫レベルを決定します。 オプション： <br/>**正の金額**  — を含む _バックオーダー_ 無効、正の数を入力します。 「バックオーダー」が有効な場合、この金額は無視されます。 <br/>**ゼロ**  — を含む _バックオーダー_ 有効、入力 `0` では、無限の逆オーダーが可能です。 <br/>**負の金額**  — を含む _バックオーダー_ 有効にする場合は、負の値を入力することをお勧めします。 金額が販売可能数量に追加されます。 例えば、-50 と入力すると、この金額までの注文が許可されます。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | グローバル | 顧客グループに応じて、購入可能な品目の最小金額を決定します。 デフォルトでは、最小数量は 1 に設定されています。 クリック **[!UICONTROL Add Minimum Qty]** をクリックして、特定の顧客グループに別の値を入力します。 |
| [!UICONTROL Notify for Quantity Below] | グローバル | 在庫がしきい値を下回ったという通知が送信される在庫レベルを決定します。 |
| [!UICONTROL Enable Qty Increments] | グローバル | 品目を数量単位で販売できるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Qty Increments] | グローバル | 数量の増分を構成する製品の数を指定します。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | グローバル | クレジットメモに含まれる品目を在庫に自動的に返すかどうかを指定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Admin Bulk Operations]

![管理一括操作](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

>[!NOTE]
>
>設定とサポートをおこなうには、以下を実行します。 **非同期キューマネージャー**&#x200B;に値を指定する場合は、コマンドラインを使用する必要があります。 開発者の支援が必要になる場合があります。 詳しくは、 [メッセージキューコンシューマーを開始](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) （内） _設定ガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | グローバル | 一括操作を非同期で実行するかどうかを指定します。 [一括](../../inventory-management/bulk-assignment.md) ソースの割り当て、ソースの割り当て解除、および [在庫をソースに移転](../../inventory-management/inventory-transfer.md). 最大で _[!UICONTROL Asynchronous batch size]_をクリックして、そのアクションを実行します。 この機能は、デフォルトでは無効になっています。 を有効にする前に、バルクアクションを使用したパフォーマンスを確認することをお勧めします。 オプション：<br/>**`Yes`**— のすべての一括操作を実行します [!DNL Inventory Management] 非同期で を有効にするには、非同期キューマネージャーを設定する必要があります。<br/>**`No`**— デフォルト。 一括操作を非同期で実行しません。 |
| [!UICONTROL Asynchronous batch size] | グローバル | 設定 **[!UICONTROL Run asynchronously]** から `Yes` 値を入力する _[!UICONTROL Asynchronous batch size]_フィールドに入力します。 <br/>デフォルトのバッチサイズは 100 です。 一括処理がこの量に達すると、実行されます。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Inventory Indexer Settings]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | グローバル | 在庫/ソースのインデックス再作成に使用する方法を決定します。 オプション： `Synchronous` / `Asynchronous` （非同期モード用に非同期キューマネージャーを設定する必要があります） |

>[!NOTE]
>
> 注文関連のアクティビティの在庫更新の依存関係により、在庫インデクサーは、 `Synchronous` または `Asynchronous` 設定。


{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Distance Provider for Distance Based SSA]

![距離ベースの SSA の距離プロバイダ](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Provider] | グローバル | 距離優先ソース選択アルゴリズムに使用するプロバイダを決定します。 この機能は、デフォルトで有効になっています。 オプション： <br/>**`Google MAP`**- Googleサービスを使用して、配送先住所と発送元の場所（住所と GPS 座標）の間の距離と時間を計算します。 このオプションを使用するにはGoogle API キーが必要で、Googleを通じた料金が発生する場合があります。<br/>**`Offline Calculation`**  — 埋め込みデータベースを使用して距離を計算し、配送先住所に最も近い発送元を決定します。 このオプションを使用するには、コマンドラインを使用して出荷するすべての国のデータベースの場所の内容を最初にダウンロードする開発者支援が必要になる場合があります。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google Distance Provider]

![Google Distance Provider](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Google API key] | グローバル | Google MAP プロバイダーのGoogle API キーを入力します。 キーは [!DNL Google Maps Platform] そして、 [!DNL Geocoding API] および [!DNL Distance Matrix API] 有効。 詳しくは、 [距離優先アルゴリズムを設定する](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) （内） _Inventory managementガイド_. |
| [!UICONTROL Computation mode] | グローバル | 配送先住所と在庫に割り当てられているすべてのソースからの距離を計算する方向とパスを決定します。 デフォルトでは、計算には駆動モードが使用されます。 オプション： <br/>**`Driving`**— 既定の設定では、道路ネットワークを使用して標準の運転指示を要求します。<br/>**`Walking`**  — 歩行者の道と歩道（利用可能な場合）を利用して歩く道をリクエスト。 <br/>**`Bicycling`**— 自転車の道や好みの通りを使用して自転車の道をリクエストします（現在、米国および一部のカナダの都市でのみ利用可能です）。 |
| [!UICONTROL Value] | グローバル | 発送先住所への発送元の場所の距離と時間の計算と返却を示します。 「距離優先度アルゴリズム」では、出荷先住所までの距離または時間が最も短いソースを推奨します。これにより、出荷を達成するのにより迅速で安価な処理が可能になります。 オプション： <br/>**`Distance`**— 指標（キロメートル単位、メートル単位）またはインチ単位（マイル単位、フィート単位）のポイント間の距離を戻します。<br/>**`Time to Destination`**  — ソースの場所から配送先住所への移動に必要な時間を時間と分単位で戻します。 |

{:style=&quot;table-layout:auto&quot;}
