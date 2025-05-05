---
title: 「設定  [!DNL Inventory Management]  グローバルオプション」
description: Web サイトの製品と Stock に対するデフォル  [!DNL Inventory Management]  設定オプションを設定する方法について説明します。
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# [!DNL Inventory Management] グローバルオプションの設定

Web サイトの製品と Stock に対するデフォルトの設定オプションを設定します。 これらの設定の一部は、[ 製品オプションの設定 ](product-options.md) で製品ごとに上書きできます。 距離優先アルゴリズムの設定については、[ 距離優先アルゴリズムの設定 ](distance-priority-algorithm.md) を参照してください。

## 製品および在庫オプションのグローバルな設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、「**[!UICONTROL Inventory]**」を選択します。

1. **[!UICONTROL Stock Options]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、オプションを設定します。

   ![ ストック・オプション ](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - 注文時に手持数量を調整するには、**[!UICONTROL Decrease Stock When Order is Placed]** を `Yes` に設定します。

   - 注文がキャンセルされた場合に商品を在庫に戻すには、を **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** リックして `Yes` ださい。

   - 在庫切れの製品をカタログに引き続き表示するには、**[!UICONTROL Display Out of Stock Products]** を `Yes` に設定します。

   - [ 価格アラート ](alert-setup.md) が有効になっている場合、お客様は登録して、製品が再入荷したときに通知を受け取ることができます。

   - 商品ページに最後の在庫残高を表示するための開始を設定するには、**[!UICONTROL Only X left Threshold]** の金額を入力します。

     在庫数がしきい値に達すると、メッセージが表示され始めます。 例えば、`3` に設定した場合、在庫の量が 3 に達するとメッセージ `Only 3 left` が表示されます。 メッセージは、在庫数がゼロに達するまで、在庫数を反映するように調整されます。

   - 製品ページに「在庫切れ」または「在庫切れ」のメッセージを表示するには、**[!UICONTROL Display Products Availability In Stock on Storefront]** を `Yes` に設定します。

   - カートに商品を読み込む際に在庫を確認するには、**[!UICONTROL Enable Inventory Check On Cart Load]** を `Yes` に設定します。 このオプションを無効にすると、在庫確認はスキップされます。 このオプションを無効にすると、特に買い物かごに多くのアイテムがある場合、チェックアウトが高速化されます。 ただし、事前検証をスキップすると、後のチェックアウトプロセスで「在庫切れ」のエラーが表示される場合があります。

   - 在庫とカタログの一貫性を維持するには、**[!UICONTROL Synchronize with Catalog]** を `Yes` に設定します。 このオプションを有効にすると、カタログの変更（製品が削除された、製品 SKU が変更された、製品タイプが変更されたなど）に応じて在庫データが調整されます。

1. **[!UICONTROL Product Stock Options]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、オプションを設定します。

   - カタログの [ 在庫管理 ](enable.md) を有効化するには、「**[!UICONTROL Manage Stock]**」を「`Yes`」に設定します。

     ![ 商品ストックオプション ](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - **[!UICONTROL Backorders]** を次のいずれかに設定します。

     | オプション | 説明 |
     | ----- | ----- |
     | `No Backorders` | 在庫切れの場合は [ 受注残 ](backorders.md) は受け付けておりません。 |
     | `Allow Qty Below 0` | バックオーダーは、数量がゼロを下回った場合に受け入れられます。 |
     | `Allow Qty Below 0 and Notify Customer` | バックオーダーは、数量がゼロを下回ると受け入れられ、オーダーを発注できる旨が顧客に通知されます。 |

   - **[!UICONTROL Maximum Qty Allowed in Shopping Cart]** を入力します。

   - **[!UICONTROL Out-of-Stock Threshold]** の金額を入力してください：

     | 値 | 説明 |
     | ----- |-----|
     | 正の金額 | 「バックオーダー」を無効にした状態で、プラスの金額を入力します。 |
     | ゼロ | 「バックオーダー」が使用可能になっている場合は、`0` と入力すると無限バックオーダーが可能になります。 |
     | マイナスの金額 | 「バックオーダー」が使用可能な場合は、マイナスの金額を入力することをお薦めします。 金額は販売可能数量に追加されます。 例えば、この金額までの注文を許可するには、「`-50`」と入力します。 |

   - 選択したグループと金額の **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** を入力します。

   - **[!UICONTROL Notify for Quantity Below]**：品目が在庫切れであることをトリガーが通知する在庫レベルを入力します。

   - 製品の数量増分を有効化するには、「**[!UICONTROL Enable Qty Increments]**」を「`Yes`」に設定します。 次に、**[!UICONTROL Qty Increments]** の要件を満たすために購入する必要がある品目の数を入力します。

     例えば、6 単位で販売される商品は、`6`、`12`、`18` などの数量で購入できます。

   - [!DNL Inventory Management] の場合、**[!UICONTROL Automatically Return Credit Memo Item to Stock]** は `No` に設定されます。 クレジット・メモを発行する場合は、入力および選択して在庫をソースに戻します。

1. **[!UICONTROL Admin bulk operations]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、オプションを設定します。

   ![ 管理の一括操作 ](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - 一括製品アクションに対して一括操作を非同期で実行するように **[!UICONTROL Run asynchronously]** を設定

     これらの操作には、一括 [ ソースの割り当てと割り当て解除 ](bulk-assignment.md) および [ ソースへの在庫の転送 ](inventory-transfer.md) が含まれます。 非同期バッチサイズまでの一括アクションを収集してから、それらのアクションを実行します。 このオプションは、デフォルトでは無効になっています。 有効にする前に、一括アクションでパフォーマンスを確認することをお勧めします。

     >[!NOTE]
     >
     >_非同期キューマネージャー_ を設定およびサポートするには、コマンドラインを使用してコマンドを発行する必要があります。 この手順には、開発者の支援が必要な場合があります。 _設定ガイド_ の [ メッセージキューコンシューマーの開始 ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html?lang=ja) を参照してください。

   - 有効な場合、**[!UICONTROL Asynchronous batch size]** を設定します。 デフォルトバッチサイズは 100 です。 バルクプロセスがこの量に達すると、システムはトリガーします。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
