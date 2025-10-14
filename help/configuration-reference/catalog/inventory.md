---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Commerce Admin の [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] ページで設定を確認します。
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>Adobe CommerceおよびMagento Open Source用の [!DNL Inventory Management] は、商品インベントリを管理するツールを提供します。 複数の倉庫、店舗、集荷場所、直荷主などに 1 つの店舗を持つマーチャントは、これらの機能を使用して販売の数量を管理し、注文を完了するための出荷を処理できます。 これらの機能の詳細と、それらの機能を使用して複数の場所で在庫を管理する方法については、『 [_[!DNL Inventory Management] ユーザーガイド _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=ja) 』を参照してください。

## [!UICONTROL Stock Options]

![&#x200B; ストック・オプション &#x200B;](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://experienceleague.adobe.com/ja/docs/commerce-admin/inventory/configuration/global-options) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | グローバル | `Yes` に設定すると、注文が行われるときに在庫数が減ります。 _在庫を管理_ が有効になっている場合、注文された製品と数量に対して予約が入力されます。 オプション：`Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | ストア表示 | `Yes` に設定すると、注文がキャンセルされたときに品目を在庫に戻します。 _在庫を管理_ が有効になっている場合、キャンセルされた製品と数量の予約はクリアされます。 オプション：`Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | グローバル | `Yes` に設定すると、在庫切れの製品が表示されます。 製品アラートも有効になっている場合は、ユーザーは登録して、製品が利用可能になった際に通知を受け取ることができます。 オプション：`Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Web サイト | `Only x left` メッセージのしきい値を設定します。 例えば、3 に設定した場合、在庫の品目が 3 個以下になるとメッセージが表示されます。 値が `0` に設定されている場合、メッセージは表示されません。 |
| [!UICONTROL Display products availability in Stock on Storefront] | ストア表示 | `Yes` に設定すると、は製品ページに `In Stock` または `Out of Stock` メッセージを表示します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | グローバル | 買い物かごに商品を読み込む際に在庫チェックを実行するかどうかを決定します。 このインベントリチェックを無効にすると、特に、買い物かごに多くの商品がある場合に、チェックアウト手順のパフォーマンスが向上します。 ただし、事前検証をスキップすると、チェックアウトプロセスの後半で _在庫切れ_ エラーが表示される場合があります。 オプション：`Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | グローバル | 「`Yes`」に設定すると、在庫データはカタログの変更（製品の削除、製品 SKU の変更、製品タイプの変更など）に従って調整され、在庫とカタログの一貫性が維持されます。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![&#x200B; 商品ストックオプション &#x200B;](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://experienceleague.adobe.com/ja/docs/commerce-admin/inventory/configuration/global-options) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | グローバル | 完全な在庫管理を使用してカタログ内の品目を管理するかどうかを決定します。 オプション：<br/>**はい** – 完全な在庫管理をアクティブ化して、現在在庫にある項目数を追跡します。 <br/>**いいえ** – 現在在庫のある項目数は追跡しません。 |
| [!UICONTROL Backorders] | グローバル | 店舗でのバックオーダーの管理方法を決定します。 バックオーダーによってオーダーの処理ステータスが変更されることはありません。 ファンドは、商品が在庫しているかどうかに関係なく、注文が行われるとすぐに承認または取得されます。 製品が利用可能になると、出荷されます。 オプション：<br/>**バックオーダーなし** – 商品が在庫切れの場合にバックオーダーを受け付けません。 <br/>**0 未満の数量を許可** – 数量が 0 を下回った場合にバックオーダーを受け入れます。 <br/>**0 未満の数量を許可し、顧客に通知**：数量がゼロを下回った場合はバックオーダーを受け入れますが、発注が可能であることを顧客に通知します。 |
| [!UICONTROL Use deferred Stock update] | グローバル | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）バックオーダーが許可されている場合に、在庫更新を延期するかどうかを指定します（「_バックオーダー_」オプションが `No backorders` のデフォルト値以外に設定されている場合）。 単一の製品または web サイト全体で機能し、_ジョブキュー_ メカニズムを使用して、注文が行われた後に在庫数量インジケーターを非同期で更新できます。 このオプションは、[&#128279;](../../inventory-management/introduction.md)Inventory management[&#x200B; と組み合わせて &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html?lang=ja#asynchronous-order-placement) 非同期注文プレースメント  でも機能します。 |
| 買い物かごで許可される最大数量 | グローバル | 1 回の注文で購入できる商品の最大数を決定します。 デフォルトでは、最大数量は 10,000 に設定されています。 |
| [!UICONTROL Out-of-Stock Threshold] | グローバル | 商品が在庫切れとみなされる在庫レベルを決定します。 オプション：<br/>**プラス金額** - _バックオーダー_ が無効の場合は、プラス金額を入力します。 「バックオーダー」が有効化されている場合、この金額は無視されます。 <br/>**ゼロ** - _バックオーダー_ が使用可能な場合、`0` を入力すると無制限のバックオーダーが可能になります。 <br/>**マイナス金額** - _バックオーダー_ が有効な場合は、マイナス金額の入力をお勧めします。 金額は販売可能数量に追加されます。 例えば、-50 と入力すると、この金額までの注文が許可されます。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | グローバル | 顧客グループに応じて、購入できる商品の最小金額を決定します。 デフォルトでは、最小数量は 1 に設定されています。 「**[!UICONTROL Add Minimum Qty]**」をクリックして、特定の顧客グループに別の値を入力します。 |
| [!UICONTROL Notify for Quantity Below] | グローバル | 在庫がしきい値を下回ったという通知が送信される在庫レベルを決定します。 |
| [!UICONTROL Enable Qty Increments] | グローバル | 品目を数量単位で販売できるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Qty Increments] | グローバル | 増分量を構成する製品の数を設定します。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | グローバル | クレジット メモに含まれる品目を自動的に在庫に返すかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![&#x200B; 管理の一括操作 &#x200B;](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://experienceleague.adobe.com/ja/docs/commerce-admin/inventory/configuration/global-options) -->

>[!NOTE]
>
>**非同期キューマネージャー** を設定およびサポートするには、コマンドラインを使用する必要があります。 これには、開発者の支援が必要になる場合があります。 _設定ガイド_ の [&#x200B; メッセージキューコンシューマーの開始 &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html?lang=ja) を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | グローバル | 一括製品アクション （[&#x200B; 一括 &#x200B;](../../inventory-management/bulk-assignment.md) ソースの割り当て、ソースの割り当て解除、[&#x200B; ソースへの在庫の転送 &#x200B;](../../inventory-management/inventory-transfer.md) など）に対して一括操作を非同期で実行するかどうかを指定します。 _[!UICONTROL Asynchronous batch size]_&#x200B;までの一括アクションを収集し、それらのアクションを実行します。 この機能は、デフォルトでは無効になっています。 有効にする前に、一括アクションでパフォーマンスを確認することをお勧めします。 オプション：<br/>**`Yes`**- [!DNL Inventory Management] のすべての一括操作を非同期で実行します。 有効にするには、非同期キューマネージャーを設定する必要があります。<br/>**`No`**- デフォルト。 一括操作を非同期で実行しません。 |
| [!UICONTROL Asynchronous batch size] | グローバル | フィールドの値を入力するには、**[!UICONTROL Run asynchronously]** を `Yes` に設定 _[!UICONTROL Asynchronous batch size]_&#x200B;ます。 <br/> デフォルトバッチサイズは 100 です。 バルクプロセスがこの量に達すると、実行されます。 |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | グローバル | ストック/ソースのインデックス再作成に使用する方法を決定します。 オプション：`Synchronous`/`Asynchronous` （非同期キューマネージャーは非同期モードに設定する必要があります） |

{style="table-layout:auto"}

>[!NOTE]
>
> 注文関連アクティビティの在庫更新の依存関係により、`Synchronous` または `Asynchronous` の設定に関係なく、製品の保存時にも在庫インデクサーがトリガーされます。


## [!UICONTROL Distance Provider for Distance Based SSA]

![&#x200B; 距離ベース SSA の距離プロバイダ &#x200B;](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://experienceleague.adobe.com/ja/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Provider] | グローバル | Distance Priority Source Selection Algorithm に使用するプロバイダを指定します。 この機能はデフォルトで有効になっています。 オプション：<br/>**`Google MAP`**- Google サービスを使用して、発送先住所と発送元場所（住所および GPS 座標）の間の距離と時間を計算します。 このオプションにはGoogle API キーが必要で、Google経由で料金が発生する場合があります。<br/>**`Offline Calculation`** – 埋め込みデータベースを使用して距離を計算し、発送先住所に最も近いソースを特定します。 このオプションを使用するには、コマンドラインを使用して出荷するすべての国のデータベースの場所のコンテンツを最初にダウンロードするために、開発者の支援が必要になる場合があります。 |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google ディスタンス プロバイダー &#x200B;](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://experienceleague.adobe.com/ja/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Google API key] | グローバル | Google MAP プロバイダーのGoogle API キーを入力します。 キーは [!DNL Google Maps Platform] からで、[!DNL Geocoding API] と [!DNL Distance Matrix API] を有効にする必要があります。 詳しくは、_Inventory managementガイドの [Configure the Distance Priority Algorithm](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) を参照してください_ |
| [!UICONTROL Computation mode] | グローバル | 配送先住所と在庫に割り当てられたすべてのソースからの距離を計算する方向とパスを決定します。 既定では、計算は運転モードを使用します。 オプション：<br/>**`Driving`**- デフォルト設定では、道路ネットワークを使用して標準的な運転方向を要求します。<br/>**`Walking`** – 歩行者パスおよび歩道（利用可能な場合）を使用して歩行方向をリクエストします。 <br/>**`Bicycling`**– 自転車道および優先ストリートを使用した自転車道案内をリクエストします（現在、米国および一部のカナダの都市でのみ利用可能）。 |
| [!UICONTROL Value] | グローバル | 出荷先所在地への出荷元事業所の距離と時間の計算対象と返品対象を示します。 距離優先アルゴリズムでは、出荷先住所までの距離または時間が最も短いソースをお勧めします。これにより、出荷を満たすためにより速く、より安価になります。 オプション：<br/>**`Distance`**- ポイント間の距離をメトリック（キロメートルとメートル）またはインペリアル（マイルとフィート）で返します。<br/>**`Time to Destination`** - ソースの場所から配送先住所への移動に必要な時間を時間と分単位で返します。 |

{style="table-layout:auto"}
