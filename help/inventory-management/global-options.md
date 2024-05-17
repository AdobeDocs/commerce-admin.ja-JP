---
title: '"設定 [!DNL Inventory Management] グローバルオプション」'
description: デフォルトの [!DNL Inventory Management] web サイトの製品および在庫の設定オプション。
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management] グローバルオプション

Web サイトの製品と Stock に対するデフォルトの設定オプションを設定します。 これらの設定の一部は、次の方法で製品ごとに上書きできます [製品オプションの設定](product-options.md). 距離の優先順位の設定については、を参照してください。 [距離優先アルゴリズムの設定](distance-priority-algorithm.md).

## 製品および在庫オプションのグローバルな設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Inventory]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Stock Options]** 「」セクションを選択して、次のオプションを設定します。

   ![在庫オプション](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - 注文時に手持数量を調整するには、次のように設定します **[!UICONTROL Decrease Stock When Order is Placed]** 対象： `Yes`.

   - 注文がキャンセルされた場合に商品を在庫に戻すには、 **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** 対象： `Yes`.

   - 在庫切れの製品をカタログに引き続き表示するには、次のように設定します **[!UICONTROL Display Out of Stock Products]** 対象： `Yes`.

   - 次の場合 [価格アラート](alert-setup.md) を有効にすると、顧客は新規登録して、製品が再入荷したときに通知を受け取ることができます。

   - 商品ページに最後に残っている在庫金額を表示するための開始を設定するには、金額を入力します **[!UICONTROL Only X left Threshold]**.

     在庫数がしきい値に達すると、メッセージが表示され始めます。 例えば、がに設定されている場合 `3`、メッセージ `Only 3 left` 在庫数が 3 に達すると表示されます。 メッセージは、在庫数がゼロに達するまで、在庫数を反映するように調整されます。

   - 製品ページに「在庫中」または「在庫切れ」のメッセージを表示するには、次のように設定します **[!UICONTROL Display Products Availability In Stock on Storefront]** 対象： `Yes`.

   - カートに商品を読み込む際に在庫を確認するには、次を設定します **[!UICONTROL Enable Inventory Check On Cart Load]** 対象： `Yes`. このオプションを無効にすると、在庫確認はスキップされます。 このオプションを無効にすると、特に買い物かごに多くのアイテムがある場合、チェックアウトが高速化されます。 ただし、事前検証をスキップすると、後のチェックアウトプロセスで「在庫切れ」のエラーが表示される場合があります。

   - 在庫とカタログの一貫性を維持するには、次を設定します **[!UICONTROL Synchronize with Catalog]** 対象： `Yes`. このオプションを有効にすると、カタログの変更（製品が削除された、製品 SKU が変更された、製品タイプが変更されたなど）に応じて在庫データが調整されます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Product Stock Options]** 「」セクションを選択して、次のオプションを設定します。

   - アクティベートするには [在庫管理](enable.md) カタログに対して、を設定します **[!UICONTROL Manage Stock]** 対象： `Yes`.

     ![製品ストックオプション](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Backorders]** を次のいずれかに変更します。

     | オプション | 説明 |
     | ----- | ----- |
     | `No Backorders` | [バックオーダー](backorders.md) 在庫切れの場合は受け付けません。 |
     | `Allow Qty Below 0` | バックオーダーは、数量がゼロを下回った場合に受け入れられます。 |
     | `Allow Qty Below 0 and Notify Customer` | バックオーダーは、数量がゼロを下回ると受け入れられ、オーダーを発注できる旨が顧客に通知されます。 |

   - を入力 **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - の金額を入力 **[!UICONTROL Out-of-Stock Threshold]**:

     | 値 | 説明 |
     | ----- |-----|
     | 正の金額 | 「バックオーダー」を無効にした状態で、プラスの金額を入力します。 |
     | ゼロ | バックオーダーが使用可能な場合、次のように入力します `0` 無制限のバックオーダーが可能になります。 |
     | マイナスの金額 | 「バックオーダー」が使用可能な場合は、マイナスの金額を入力することをお薦めします。 金額は販売可能数量に追加されます。 例えば、 `-50` この金額までの注文を許可します。 |

   - を入力 **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** 選択したグループおよび金額に対して。

   - の場合 **[!UICONTROL Notify for Quantity Below]**&#x200B;を入力し、在庫切れをトリガーが通知する在庫レベルを入力します。

   - 製品の増分量を有効にするには、を設定します **[!UICONTROL Enable Qty Increments]** 対象： `Yes`. 次に、に対して **[!UICONTROL Qty Increments]**、要件を満たすために購入する必要がある品目の数を入力します。

     例えば、6 単位で販売される商品は、次の数で購入できます。 `6`, `12`, `18`など。

   - の場合 [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** はに設定されています。 `No`. クレジット・メモを発行する場合は、入力および選択して在庫をソースに戻します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Admin bulk operations]** 「」セクションを選択して、次のオプションを設定します。

   ![管理の一括操作](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Run asynchronously]** 一括操作を非同期的に実行して一括製品アクションを実行するには

     これらの操作には一括が含まれます [ソースの割り当てと割り当て解除](bulk-assignment.md)、および [ソースへの在庫の移動](inventory-transfer.md). 非同期バッチサイズまでの一括アクションを収集してから、それらのアクションを実行します。 このオプションは、デフォルトでは無効になっています。 有効にする前に、一括アクションでパフォーマンスを確認することをお勧めします。

     >[!NOTE]
     >
     >とサポートを設定するには _非同期キューマネージャー_&#x200B;の場合は、コマンドラインを使用してコマンドを発行する必要があります。 この手順には、開発者の支援が必要な場合があります。 参照： [メッセージキューコンシューマーの開始](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) が含まれる _設定ガイド_.

   - 有効な場合は、 **[!UICONTROL Asynchronous batch size]**. デフォルトバッチサイズは 100 です。 バルクプロセスがこの量に達すると、システムはトリガーします。

1. 完了したら、 **[!UICONTROL Save Config]**.
