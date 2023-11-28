---
title: 出荷
description: 請求書の出荷レコードを作成し、出荷をキャンセルする方法を説明します。
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 1%

---

# 出荷

The _[!UICONTROL Shipments]_グリッドは、出荷用に準備されたすべての請求書の出荷レコードをリストします。 注文が発生すると、出荷レコードを生成できます [請求済み](invoices.md) または後で。

Adobe CommerceとMagento Open Sourceは、一部および完全な注文出荷をサポートし、追加のオプションを次から利用できます。 [Inventory management](../inventory-management/introduction.md) およびサードパーティの拡張機能。

![出荷グリッド](./assets/shipments.png){width="600" zoomable="yes"}

## 列の説明

| 列またはコントロール | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となる各引用符のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション： `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | 新しい出荷が初めて保存される際に割り当てられる一意の順次番号 |
| [!UICONTROL Ship Date] | 発送日 |
| [!UICONTROL Order] | 注文の一意の番号 |
| [!UICONTROL Order Date] | 注文が行われた日時 |
| [!UICONTROL Ship-to Name] | 注文の発送先の人物の名前 |
| [!UICONTROL Total Quantity] | 出荷する品目の合計数量 |
| [!UICONTROL Action] | 出荷を編集モードで表示します |

{style="table-layout:auto"}

追加の列：

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Order Status] | 注文ステータスを示します |
| [!UICONTROL Purchased From] | 注文がおこなわれた Web サイト、ストア、およびストアの表示を示します |
| [!UICONTROL Customer Name] | 注文を行った顧客または購入者の名前 |
| [!UICONTROL Email] | 登録顧客の電子メールアドレス |
| [!UICONTROL Customer Group] | 顧客が割り当てられている顧客グループまたは共有カタログの名前 |
| [!UICONTROL Billing Address] | 注文を行った顧客または購入者の名前 |
| [!UICONTROL Shipping Address] | 注文の発送先の人物の名前 |
| [!UICONTROL Payment Method] | 注文に使用する支払い方法 |
| [!UICONTROL Shipping Information] | 注文の出荷に使用するメソッド |

{style="table-layout:auto"}

## 出荷の作成

次の手順では、Adobe CommerceまたはMagento Open Sourceで出荷を作成するプロセスについて説明します。 Inventory managementを有効にしている場合は、 [複数ソース出荷の作成](../inventory-management/shipments-create.md) をクリックし、行項目ごとに送信するソース（または場所）と数量を選択します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッド内の順序を探し、開きます。

1. 注文が支払済み、請求済みで、出荷準備が整っている場合は、「 **[!UICONTROL Ship]**.

   出荷の上部のセクションには、受注からの名前、住所、支払い情報が含まれます。

1. 出荷フォームの各セクションに、次のセクションの手順に従って入力します。

### [!UICONTROL Items to Ship]

順序内の各行項目に対して、 **[!UICONTROL Qty to Ship]** 必要に応じて。

### [!UICONTROL Shipping Information]

**メソッド 1:** 注文ページの使用

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Adobe Analytics の **[!UICONTROL Action]** 列をクリックし、 **[!UICONTROL View]**.

1. クリック **[!UICONTROL Ship]**.

1. 下にスクロールして、 _[!UICONTROL Payment & Shipping Method]_ブロックしてクリックします。**[!UICONTROL Add Tracking Number]**.

1. 設定 **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. 出荷を追跡するには、 **[!UICONTROL Title]** および **[!UICONTROL Number]** .

**方法 2:** 出荷ページの使用

この方法は、注文の出荷が注文ページから既に作成されている場合にのみ使用できます。
必要に応じて、直送ページを使用して出荷および追跡情報を変更できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 出荷を検索し、編集モードで開きます。

1. 下にスクロールして、 _[!UICONTROL Payment & Shipping Method]_ブロック。

1. を選択します。 **[!UICONTROL Carrier]**.

1. を入力します。 **[!UICONTROL Title]** パッケージの

1. トラッキングを入力 **[!UICONTROL Number]**.

1. クリック **[!UICONTROL Add]**.

1. 追跡情報を含む E メールを顧客に送信するには、 **[!UICONTROL Send Tracking Information]**&#x200B;をクリックし、アクションを確定します。

   出荷の場所を追跡するには、必要な出荷を編集モードで開き、 **[!UICONTROL Track this shipment]**.

   ![発送および追跡情報](./assets/tracking-information.png){width="600" zoomable="yes"}

### ボタン

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | [ 新しい出荷 ] フォームをクローズし、注文に戻ります |
| **[!UICONTROL Submit Shipment]** | 注文の出荷を追加します。 |
| **[!UICONTROL Reset]** | すべてのフィールドを元の値に戻します。 |

{style="table-layout:auto"}

### 発送コメント

1. 入力 **コメント** 必要に応じて、出荷用に。

1. 出荷の準備が整ったら、「 **出荷を送信**.

## 出荷に対するコメントを設定します

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下 _[!UICONTROL Sales]_を選択します。**[!UICONTROL Sales Email]**.

1. を展開します。 **出荷コメント** セクションで設定を変更し、必要に応じて変更します。

   ![出荷コメントの設定](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - The **[!UICONTROL Enabled]** オプションが `Yes` デフォルトでは、送料のコメントが入力されると、E メールが顧客に送信されます。

   - の場合 **[!UICONTROL Shipment Comment Email Sender]**「 」で、出荷コメントの電子メールの送信元の人物を選択します。 デフォルトでは、5 つの電子メールアドレスが提供されます。

   - の場合 **[!UICONTROL Shipment Comment Email Template]**」で、必要に応じてテンプレートを選択するか、デフォルトのオプションを選択します。

   - の場合 **[!UICONTROL Shipment Comment Email Template for Guests]**「 」で、ストアにアカウントを持たないお客様に使用するテンプレートを選択します。

   - の場合 **[!UICONTROL Shipment Comment Email Copy To]**「 」で、E メールアドレスを入力して、出荷コメントの E メールコピーを送信します。 複数の電子メールアドレスはコンマで区切ります。

   - の場合 **[!UICONTROL Shipment Comment Email Copy Method]**&#x200B;を選択します。 `bcc` （ブラインドカーボンコピー）または `separate email copy` メソッドを選択します。

1. クリック **[!UICONTROL Save Config]**.

## 出荷のキャンセル

配送業者がキャリアに出荷する前に、注文を開き、配送先に移動することで、キャリアがキャンセルをサポートする場合にキャンセルできます。 一部の通信事業者は、予約後のキャンセルを制限または制限します。 たとえば、UPS はキャンセルを許可しますが、出荷が予約されてから 24 時間待つ必要があります。 出荷が取り消された場合、取り消しを取り消すことはできません。 唯一のリソースは、順序を再作成することです。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッド内の順序を検索します。

1. Adobe Analytics の _アクション_ 列、選択 **[!UICONTROL View]**.

1. 左側のパネルで、を選択します。 **[!UICONTROL Shipments]**.

   出荷が取り消される場合は、 _[!UICONTROL Cancel Shipment]_は上部のボタンバーにオプションとして表示されます。

1. クリック **[!UICONTROL Cancel Shipment]**.

1. 確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.

出荷のステータスが次の値に変わります： `Canceled`. 運送業者がキャンセルをサポートしていない場合は、エラーメッセージが表示され、出荷をキャンセルできなかった理由が示されます。

## 出荷フィールドの説明

### [!UICONTROL Shipping Information]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Carrier] | 選択した通信事業者の名前 |
| [!UICONTROL Title] | 通信事業者がパッケージに割り当てたわかりやすい名前。 |
| [!UICONTROL Number] | パッケージに割り当てられている、リンクされたトラッキング番号。 |
| [!UICONTROL Action] | ![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png)  — 出荷レコードからパッケージ情報を削除します。 |
| [!UICONTROL Add] | 別のパッケージを出荷に追加します。 |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Origin Location] | 使用可能な場所のリストを表示します。 |
| [!UICONTROL International] | オンにすると、出荷が国際出荷として識別されます。 |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Description] | 項目の説明。 |
| [!UICONTROL SKU] | 品目の在庫管理単位。 |
| [!UICONTROL Weight] | 項目の重み。 |
| [!UICONTROL Qty Ordered] | 注文された品目の数量。 |
| [!UICONTROL Qty Shipped] | 出荷された品目の数量。 |
| [!UICONTROL Qty Packed] | このパッケージに含まれる項目の数。 |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Comments] | 出荷に関するコメントは、内部で使用されます。 |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG**  — 出荷パッケージのラベルをダウンロードします。 サイズ： A6 （105 x 148 mm、4.1 x 5.6 インチ） |

{style="table-layout:auto"}
