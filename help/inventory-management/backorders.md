---
title: "Configure [!DNL Inventory Management] backorders"
description: 在庫切れ製品の販売をサポートするためのバックオーダーを設定する方法を説明します。
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# [!DNL Inventory Management] 件のバックオーダーの設定

バックオーダーを使用すると、数量がゼロに達した後や、事実上在庫切れになった後も、店舗で製品を販売し続けることができます。 顧客の注文がバックオーダーの場合、資金は直ちに承認および取得され、注文の処理ステータスは変更されず、在庫が利用可能になるまで出荷は保留中のままになります。

店舗や売上に応じて、次のレベルでバックオーダーを有効または無効にできます。

- **[!UICONTROL Global]** - サイト レベルでのカタログ内のすべての製品

- **[!UICONTROL Product]** - サイト、ソース、在庫の設定を上書きする特定の製品

## バックオーダー設定について

バックオーダーを最適にサポートするために、特定のしきい値と設定を設定することを強くお勧めします。

### 在庫切れのしきい値

このしきい値に負の値を使用して、商品が実際に在庫切れと見なされるまでの間にバックオーダー可能な商品の最大数量を設定します。 この金額は売れる量に加算されます。 製品レベルで設定された値は、グローバルレベルで設定された値を上書きします。

販売可能数量の式は `(Quantity - (Out-of-Stock Threshold))` です。

以下は例です。

- 数量：25
- 以下の数量を通知：10
- X 左スレッショルドのみ：5
- 在庫切れのしきい値：-50

この商品の販売可能数量は `75 (25 - (-50))` です。

![ バックオーダーが有効化される前の販売可能数量の例 ](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![ バックオーダーが有効化された後の販売可能数量の例 ](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

顧客が使用可能な 25 個の製品を購入すると、新規オーダーはバックオーダーとして入力されます。 製品の販売可能数量が 5 に減ると（70 個の品目が販売されました）、「_製品_」ページにストアフロントにメッセージ `Only 5 left` が表示されます。 販売可能数量が `0` に達すると、製品はストアフロントに `Out of Stock` として表示されます。

>[!NOTE]
>
>顧客が _[!UICONTROL backorder qty]_を使用して注文すると、[!DNL Inventory Management] は販売可能な数量から数量を自動的に減算します。 注文が出荷されず、キャンセルされた場合、その数量は集計された仮想販売可能数量に戻されます。**_キャンセル済み注文数量はどのソースにも割り当てられていません_**が、販売できる商品の合計数（商品グリッドの_[!UICONTROL Salable Quantity]_ 列）に返されます。

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### 在庫ステータス

バックオーダーを有効にする場合は、製品を `In Stock` ステータスに設定する必要があります。 この値は、_製品_ ページから設定できます。 マルチソースマーチャントの場合、`In Stock` とマークされたソースが少なくとも 1 つ必要です。 _製品_ ページと割り当てられた _ソース_ グリッドからステータスにアクセスして設定します。

## バックオーダーのグローバルな設定

これらのステップにより、サイト・レベルですべての製品のバックオーダーが可能になります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. **[!UICONTROL Store View]** を `Default Config` に設定します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、「**[!UICONTROL Inventory]**」を選択します。

1. ![ 展開セレクター ](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]** を展開します。

1. **[!UICONTROL Backorders]** の場合は、「**[!UICONTROL Use system value]**」チェックボックスの選択を解除し、オプションを選択します。

   | オプション | 説明 |
   | -- | -- |
   | `No Backorders` | 商品が在庫切れになった場合にバックオーダーを受け付けないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れること。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロを下回った場合にバックオーダーを受け入れ、顧客に対してオーダーがまだ発注可能であることを通知します。 |

1. **[!UICONTROL Out-of-Stock Threshold]** の場合は、「**[!UICONTROL Use system value]**」チェックボックスの選択を解除して、別の金額を入力します。

   | 値 | 説明 |
   | -- | -- |
   | 正の金額 | 「バックオーダー」を使用不可にした状態で、正の値を入力します。 |
   | ゼロ | 「バックオーダー」が使用可能になっている場合は、`0` と入力すると無限バックオーダーが可能になります。 |
   | マイナスの金額 | 「バックオーダー」を使用可能にする場合は、マイナスの値を入力することをお薦めします。 金額は販売可能数量に追加されます。 例えば、この金額までの注文を許可するには、「`-50`」と入力します。 |

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 商品のバックオーダーの設定

製品レベルの設定は、グローバル設定よりも優先されます。 グローバル店舗またはソース レベルの設定を上書きするために、製品レベルでバックオーダーを構成できます。 例えば、店舗はバックオーダーをグローバルにサポートしている場合があります。 製品設定を使用すると、他の製品やソースに影響を与えることなく、バックオーダーを無効にしたり、在庫切れのしきい値を変更したりできます。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 製品を **[!UICONTROL Edit]** モードで開き、ページを下にスクロールして _[!UICONTROL Sources]_領域に移動します。

   [!DNL Inventory Management] を使用せずに設定された製品の場合、タブは表示されません。 「`Advanced Inventory`」ボタンが「_[!UICONTROL Quantity]_」フィールドの下に表示されます。

1. 「**[!UICONTROL Advanced Inventory]**」をクリックします。

   製品固有の設定のページを表示します。 `global` としてリストされた設定は、ストアの現在のグローバル設定を表示します。

1. **[!UICONTROL Backorders]** の場合は、「**[!UICONTROL Use Config Setting]**」チェックボックスの選択を解除し、オプションを選択します。

   | オプション | 説明 |
   | -- | -- |
   | `No Backorders` | 商品が在庫切れになった場合にバックオーダーを受け付けないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れること。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロを下回った場合にバックオーダーを受け入れ、顧客に対してオーダーを引き続き発注できる旨を通知する。 |

1. **[!UICONTROL Out-of-Stock Threshold]** の場合は、「**[!UICONTROL Use Config Setting]**」チェックボックスの選択を解除して金額を入力します。

   | 値 | 説明 |
   | -- | -- |
   | 正の金額 | 「バックオーダー」を使用不可にした状態で、正の値を入力します。 |
   | ゼロ | 「バックオーダー」が使用可能になっている場合は、`0` と入力すると無限バックオーダーが可能になります。 |
   | マイナスの金額 | 「バックオーダー」を使用可能にする場合は、マイナスの値を入力することをお薦めします。 金額は販売可能数量に追加されます。 例えば、`-50` と入力すると、その金額を上限とする注文が許可されます。 |

   ![ バックオーダー用に構成された事前在庫 ](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Done]**」をクリックし、「**[!UICONTROL Save]**」をクリックします。
