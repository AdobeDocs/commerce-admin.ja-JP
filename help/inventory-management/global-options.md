---
title: '"設定" [!DNL Inventory Management] グローバルオプション»'
description: デフォルトの設定方法を説明します [!DNL Inventory Management] web サイトの製品および在庫の設定オプションです。
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management] グローバルオプション

Web サイトの製品と在庫に対するデフォルトの設定オプションを設定します。 これらの設定の一部は、製品ごとに、 [製品オプションの設定](product-options.md). 距離の優先度を設定するには、 [距離優先アルゴリズムの設定](distance-priority-algorithm.md).

## 製品と在庫のオプションをグローバルに設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Inventory]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Stock Options]** 」セクションに移動して、次のオプションを設定します。

   ![在庫オプション](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - 注文時に手持数量を調整するには、 **[!UICONTROL Decrease Stock When Order is Placed]** から `Yes`.

   - オーダーが取り消された場合に品目を在庫に戻すには、次の手順に従います。 **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** から `Yes`.

   - 在庫切れの商品をカタログに表示し続けるには、 **[!UICONTROL Display Out of Stock Products]** から `Yes`.

   - 次の場合 [価格通知](alert-setup.md) を有効にすると、新規登録して、製品の在庫が再び切れたときに通知を受け取ることができます。

   - 製品ページの最後の残り在庫金額の表示の開始を設定するには、次の金額を入力します： **[!UICONTROL Only X left Threshold]**.

     在庫数がしきい値に達すると、メッセージが表示され始めます。 例えば、 `3`、メッセージ `Only 3 left` 在庫数が 3 に達すると表示されます。 数量がゼロに達するまで、在庫数量を反映するようにメッセージが調整されます。

   - 製品ページに「在庫切れ」または「在庫切れ」のメッセージを表示するには、 **[!UICONTROL Display Products Availability In Stock on Storefront]** から `Yes`.

   - 買い物かごに製品を読み込む際に在庫を確認するには、 **[!UICONTROL Enable Inventory Check On Cart Load]** から `Yes`. このオプションを無効にした場合、在庫チェックはスキップされます。 このオプションを無効にすると、特に買い物かごに多数の品目がある場合に、チェックアウトが高速化されます。 ただし、事前検証をスキップした場合、後でチェックアウトプロセスで「在庫切れ」エラーが表示されることがありました。

   - 在庫とカタログの一貫性を保つには、 **[!UICONTROL Synchronize with Catalog]** から `Yes`. このオプションを有効にすると、カタログの変更（製品の削除、製品の SKU の変更、製品のタイプの変更など）に従って在庫データが調整されます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Product Stock Options]** 」セクションに移動して、次のオプションを設定します。

   - 有効化するには [在庫管理](enable.md) カタログに対して、 **[!UICONTROL Manage Stock]** から `Yes`.

     ![製品在庫オプション](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Backorders]** を次のいずれかに変更します。

     | オプション | 説明 |
     | ----- | ----- |
     | `No Backorders` | [バックオーダー](backorders.md) は、製品が在庫切れの場合は受け入れられません。 |
     | `Allow Qty Below 0` | 数量がゼロを下回った場合は、バックオーダーが受け入れられます。 |
     | `Allow Qty Below 0 and Notify Customer` | 数量がゼロを下回った場合は、バックオーダーが受け入れられ、注文が可能であることを顧客に通知します。 |

   - 次を入力します。 **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - 次の金額を入力： **[!UICONTROL Out-of-Stock Threshold]**:

     | 値 | 説明 |
     | ----- |-----|
     | 正の金額 | 「バックオーダー」を無効にした状態で、正の金額を入力します。 |
     | ゼロ | 「バックオーダー」を有効にした場合、入力 `0` では、無限の逆オーダーが可能です。 |
     | 負の金額 | 「バックオーダー」を有効にした場合、負の金額を入力することをお勧めします。 金額が販売可能数量に追加されます。 例えば、 `-50` ：この金額までの注文を許可します。 |

   - 次を入力します。 **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** 選択したグループと金額の

   - の場合 **[!UICONTROL Notify for Quantity Below]**「 」に、品目が在庫切れであることをトリガーが通知する在庫レベルを入力します。

   - 製品の数量増分を有効にするには、 **[!UICONTROL Enable Qty Increments]** から `Yes`. 次に、 **[!UICONTROL Qty Increments]**、必要に応じて購入する必要がある品目の数を入力します。

     例えば、6 個の単位で販売される品目は、 `6`, `12`, `18`など。

   - の場合 [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** が `No`. クレジット・メモを発行する際は、を入力し、在庫をソースに返却することを選択します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Admin bulk operations]** 」セクションに移動して、次のオプションを設定します。

   ![管理一括操作](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Run asynchronously]** 一括操作を非同期で実行する

     これらの操作には一括が含まれます [ソースの割り当てと割り当て解除](bulk-assignment.md)、および [在庫のソースへの移行](inventory-transfer.md). 非同期バッチサイズまでのバルクアクションを収集し、それらのアクションを実行します。 このオプションはデフォルトでは無効になっています。 を有効にする前に、バルクアクションを使用したパフォーマンスを確認することをお勧めします。

     >[!NOTE]
     >
     >設定とサポートをおこなうには、以下を実行します。 _非同期キューマネージャー_&#x200B;に値を指定する場合は、コマンドラインを使用してコマンドを発行する必要があります。 この手順には、開発者の支援が必要になる場合があります。 詳しくは、 [メッセージキューコンシューマーを開始](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) （内） _設定ガイド_.

   - 有効な場合、 **[!UICONTROL Asynchronous batch size]**. デフォルトのバッチサイズは 100 です。 一括処理がこの量に達すると、システムはそれをトリガーします。

1. 完了したら、「 **[!UICONTROL Save Config]**.
