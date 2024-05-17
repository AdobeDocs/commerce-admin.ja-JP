---
title: '"設定 [!DNL Inventory Management] バックオーダー」'
description: 在庫切れ製品の販売をサポートするためのバックオーダーを設定する方法を説明します。
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management] バックオーダー

バックオーダーを使用すると、数量がゼロに達した後や、事実上在庫切れになった後も、店舗で製品を販売し続けることができます。 顧客の注文がバックオーダーの場合、資金は直ちに承認および取得され、注文の処理ステータスは変更されず、在庫が利用可能になるまで出荷は保留中のままになります。

店舗や売上に応じて、次のレベルでバックオーダーを有効または無効にできます。

- **[!UICONTROL Global]** - カタログ内のすべての製品（サイトレベル）

- **[!UICONTROL Product]** - サイト、ソース、在庫の設定を上書きする特定の製品

## バックオーダー設定について

バックオーダーを最適にサポートするために、特定のしきい値と設定を設定することを強くお勧めします。

### 在庫切れのしきい値

このしきい値に負の値を使用して、商品が実際に在庫切れと見なされるまでの間にバックオーダー可能な商品の最大数量を設定します。 この金額は売れる量に加算されます。 製品レベルで設定された値は、グローバルレベルで設定された値を上書きします。

販売可能数量の式は次のとおりです `(Quantity - (Out-of-Stock Threshold))`.

以下は例です。

- 数量：25
- 以下の数量を通知：10
- X 左スレッショルドのみ：5
- 在庫切れのしきい値：-50

この商品の販売可能数量は `75 (25 - (-50))`.

![バックオーダーが有効化される前の販売可能数量の例](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![バックオーダーが有効化された後の販売可能数量の例](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

顧客が使用可能な 25 個の製品を購入すると、新規オーダーはバックオーダーとして入力されます。 商品の販売可能数量が 5 に減少する（70 点販売済み）と、 _製品_ ページにメッセージが表示される `Only 5 left` 店先で。 販売可能数量に達した場合 `0`製品は次のように表示されます `Out of Stock` 店の前で。

>[!NOTE]
>
>顧客がを使用して注文する場合 _[!UICONTROL backorder qty]_, [!DNL Inventory Management] 販売可能数量から数量が自動的に減算されます。 注文が出荷されず、キャンセルされた場合、その数量は集計された仮想販売可能数量に戻されます。 この&#x200B;**_キャンセル済み注文数量がどのソースにも割り当てられていません_**ただし、は販売できる製品の合計数（_[!UICONTROL Salable Quantity]_ 列（製品グリッド上）

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### 在庫ステータス

製品はに設定する必要があります `In Stock` バックオーダーを有効にする際のステータス。 この値は、 _製品_ ページ。 マルチソースマーチャントの場合、としてマークされたソースが少なくとも 1 つ必要です。 `In Stock`. へのアクセスとステータスの設定 _製品_ ページして割り当て済み _ソース_ グリッド。

## バックオーダーのグローバルな設定

これらのステップにより、サイト・レベルですべての製品のバックオーダーが可能になります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. を設定 **[!UICONTROL Store View]** 対象： `Default Config`.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Inventory]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. の場合 **[!UICONTROL Backorders]**、選択を解除 **[!UICONTROL Use system value]** チェックボックスをオンにしてオプションを選択します。

   | オプション | 説明 |
   | -- | -- |
   | `No Backorders` | 商品が在庫切れになった場合にバックオーダーを受け付けないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れること。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロを下回った場合にバックオーダーを受け入れ、顧客に対してオーダーがまだ発注可能であることを通知します。 |

1. の場合 **[!UICONTROL Out-of-Stock Threshold]**、選択を解除 **[!UICONTROL Use system value]** チェックボックスをオンにして、別の量を入力します。

   | 値 | 説明 |
   | -- | -- |
   | 正の金額 | 「バックオーダー」を使用不可にした状態で、正の値を入力します。 |
   | ゼロ | バックオーダーが使用可能な場合、次のように入力します `0` 無制限のバックオーダーが可能になります。 |
   | マイナスの金額 | 「バックオーダー」を使用可能にする場合は、マイナスの値を入力することをお薦めします。 金額は販売可能数量に追加されます。 例えば、 `-50` この金額までの注文を許可します。 |

1. クリック **[!UICONTROL Save Config]**.

## 商品のバックオーダーの設定

製品レベルの設定は、グローバル設定よりも優先されます。 グローバル店舗またはソース レベルの設定を上書きするために、製品レベルでバックオーダーを構成できます。 例えば、店舗はバックオーダーをグローバルにサポートしている場合があります。 製品設定を使用すると、他の製品やソースに影響を与えることなく、バックオーダーを無効にしたり、在庫切れのしきい値を変更したりできます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. で製品を開く **[!UICONTROL Edit]** をモードにし、ページを下にスクロールして「」を表示します。 _[!UICONTROL Sources]_領域。

   を指定せずに設定した製品の場合 [!DNL Inventory Management]この場合、「」タブは表示されません。 この `Advanced Inventory` ボタンは以下に表示されます _[!UICONTROL Quantity]_フィールド。

1. クリック **[!UICONTROL Advanced Inventory]**.

   製品固有の設定のページを表示します。 としてリストされた設定 `global` ストアの現在のグローバル設定を表示します。

1. の場合 **[!UICONTROL Backorders]**、選択を解除 **[!UICONTROL Use Config Setting]** チェックボックスをオンにしてオプションを選択します。

   | オプション | 説明 |
   | -- | -- |
   | `No Backorders` | 商品が在庫切れになった場合にバックオーダーを受け付けないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れること。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロを下回った場合にバックオーダーを受け入れ、顧客に対してオーダーを引き続き発注できる旨を通知する。 |

1. の場合 **[!UICONTROL Out-of-Stock Threshold]**、選択を解除 **[!UICONTROL Use Config Setting]** チェックボックスをオンにして金額を入力します。

   | 値 | 説明 |
   | -- | -- |
   | 正の金額 | 「バックオーダー」を使用不可にした状態で、正の値を入力します。 |
   | ゼロ | バックオーダーが使用可能な場合、次のように入力します `0` 無制限のバックオーダーが可能になります。 |
   | マイナスの金額 | 「バックオーダー」を使用可能にする場合は、マイナスの値を入力することをお薦めします。 金額は販売可能数量に追加されます。 例えば、 `-50` その金額までの注文を許可します。 |

   ![バックオーダー用に設定された事前在庫](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Done]**、次に **[!UICONTROL Save]**.
