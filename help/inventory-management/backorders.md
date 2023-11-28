---
title: '"設定" [!DNL Inventory Management] バックオーダー数'
description: 在庫切れ製品の販売をサポートするためにバックオーダーを設定する方法を説明します。
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management] バックオーダー

残りの注文は、数量がゼロに達した後、または事実上在庫切れの後も、店舗が製品を販売し続けるのを可能にします。 顧客の注文が逆注文の場合、資金は直ちに承認され、取り込まれ、注文の処理ステータスは変更されず、出荷は在庫が使用可能になるまで保留状態のままになります。

店舗と販売に応じて、次のレベルでバックオーダーを有効または無効にできます。

- **[!UICONTROL Global]**  — サイトレベルのカタログ内のすべての製品

- **[!UICONTROL Product]**  — サイト、ソース、在庫の設定を上書きする特定の製品

## バックオーダーの設定について

バックオーダーを最も効果的にサポートするために、特定のしきい値と設定を設定することを強くお勧めします。

### 在庫切れしきい値

このしきい値に負の値を指定すると、製品が在庫切れと見なされる前にバックオーダーできる製品の最大数量が設定されます。 この金額は販売可能数量に加算されます。 製品レベルで設定された値は、グローバルレベルで設定された値よりも優先されます。

販売可能数量の数式は次のとおりです。 `(Quantity - (Out-of-Stock Threshold))`.

次に例を示します。

- 数量： 25
- 次の数量を通知： 10
- X のみ左しきい値： 5
- 在庫切れしきい値： -50

この製品の販売可能数量は次のとおりです。 `75 (25 - (-50))`.

![バックオーダーが有効になる前の販売可能数量の例](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![バックオーダーが有効になった後の販売可能数量の例](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

顧客が使用可能な 25 個の製品を購入すると、新規受注は「バックオーダー」と入力します。 製品の販売可能数量が 5（70 品目が販売された）に減少すると、 _製品_ ページにメッセージが表示されます `Only 5 left` 店の前で 販売可能数量が `0`に値を指定しない場合、製品は `Out of Stock` 店の前に

>[!NOTE]
>
>顧客が _[!UICONTROL backorder qty]_, [!DNL Inventory Management] は、販売可能数量から数量を自動的に減算します。 注文が出荷されず、取り消された場合、数量は集計された仮想販売可能数量に戻ります。 The **_取り消された注文数量は、どのソースにも割り当てられていません_**が返されるが、販売可能な製品の合計数 (_[!UICONTROL Salable Quantity]_ 」列をクリックします )。

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### 在庫ステータス

製品はに設定する必要があります `In Stock` バックオーダーを有効にする際のステータス。 この値は、 _製品_ ページに貼り付けます。 複数ソースのマーチャントの場合は、少なくとも 1 つのソースが `In Stock`. 次を通じてステータスにアクセスし、設定します。 _製品_ ページと割り当て済み _ソース_ グリッド。

## バックオーダーをグローバルに設定

これらの手順では、サイトレベルですべての製品のバックオーダーを有効にします。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 設定 **[!UICONTROL Store View]** から `Default Config`.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Inventory]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. の場合 **[!UICONTROL Backorders]**、選択を解除 **[!UICONTROL Use system value]** チェックボックスをオンにして、次のオプションを選択します。

   | オプション | 説明 |
   | -- | -- |
   | `No Backorders` | 製品が在庫切れの場合にバックオーダーを受け入れないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れる。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロ未満の場合にバックオーダーを受け入れ、受注が未完了であることを顧客に通知する。 |

1. の場合 **[!UICONTROL Out-of-Stock Threshold]**、選択を解除 **[!UICONTROL Use system value]** 」チェックボックスにチェックを入れ、別の金額を入力します。

   | 値 | 説明 |
   | -- | -- |
   | 正の金額 | 「バックオーダー」を無効にした状態で、正の値を入力します。 |
   | ゼロ | 「バックオーダー」を有効にした場合、入力 `0` では、無限の逆オーダーが可能です。 |
   | 負の金額 | 「バックオーダー」を有効にした場合は、負の値を入力することをお勧めします。 金額が販売可能数量に追加されます。 例えば、 `-50` ：この金額までの注文を許可します。 |

1. クリック **[!UICONTROL Save Config]**.

## 製品のバックオーダーの設定

製品レベルの設定は、グローバル設定を上書きします。 製品レベルでバックオーダーを設定して、グローバルストアまたはソースレベルでの設定を上書きすることができます。 例えば、あなたの店舗が世界中でバックオーダーをサポートしている場合があります。 製品設定を使用すると、他の製品やソースに影響を与えることなく、バックオーダーを無効にしたり、在庫切れのしきい値を変更したりできます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. で製品を開く **[!UICONTROL Edit]** モードに切り替え、ページを下にスクロールして _[!UICONTROL Sources]_領域。

   を使用せずに設定された製品の場合 [!DNL Inventory Management]に値を指定しない場合、「 」タブは表示されません。 The `Advanced Inventory` ボタンが _[!UICONTROL Quantity]_フィールドに入力します。

1. クリック **[!UICONTROL Advanced Inventory]**.

   このアクションは、製品固有の設定のページを表示します。 次のリストにある設定 `global` ストアの現在のグローバル設定を表示します。

1. の場合 **[!UICONTROL Backorders]**、選択を解除 **[!UICONTROL Use Config Setting]** チェックボックスをオンにして、次のオプションを選択します。

   | オプション | 説明 |
   | -- | -- |
   | `No Backorders` | 製品が在庫切れの場合にバックオーダーを受け入れないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れる。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロ未満の場合にバックオーダーを受け入れ、そのオーダーを引き続き発注できることを顧客に通知する。 |

1. の場合 **[!UICONTROL Out-of-Stock Threshold]**、選択を解除 **[!UICONTROL Use Config Setting]** チェックボックスに金額を入力します。

   | 値 | 説明 |
   | -- | -- |
   | 正の金額 | 「バックオーダー」を無効にした状態で、正の値を入力します。 |
   | ゼロ | 「バックオーダー」を有効にした場合、入力 `0` では、無限の逆オーダーが可能です。 |
   | 負の金額 | 「バックオーダー」を有効にした場合は、負の値を入力することをお勧めします。 金額が販売可能数量に追加されます。 例えば、 `-50` を使用して、その金額までの注文を許可します。 |

   ![バックオーダー用に構成された高度な在庫](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Done]**&#x200B;を、 **[!UICONTROL Save]**.
