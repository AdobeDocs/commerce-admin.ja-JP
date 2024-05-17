---
title: 出荷
description: 請求書の出荷レコードを作成し、出荷をキャンセルする方法を説明します。
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# 出荷

この _[!UICONTROL Shipments]_グリッド出荷用に準備されたすべての請求書の出荷記録を表示します。 注文が次の場合に出荷レコードを生成できます [請求済](invoices.md) またはそれ以降。

Adobe CommerceとMagento Open Sourceは、部分的および完全な注文発送をサポートしており、次の場所から追加のオプションを利用できます [Inventory management](../inventory-management/introduction.md) とサードパーティの拡張機能をサポートしています。

![出荷グリッド](./assets/shipments.png){width="600" zoomable="yes"}

## 列の説明

| 列またはコントロール | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となる各見積もりのチェックボックスを選択するか、列見出しの選択コントロールを使用します。 オプション： `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | 新しい出荷が初めて保存されるときに割り当てられる一意の連続番号 |
| [!UICONTROL Ship Date] | 発送日 |
| [!UICONTROL Order] | 注文の一意の番号 |
| [!UICONTROL Order Date] | 注文された日時 |
| [!UICONTROL Ship-to Name] | 注文の出荷先の名前 |
| [!UICONTROL Total Quantity] | 出荷する品目の合計数 |
| [!UICONTROL Action] | 「表示」を選択すると、出荷が編集モードで開きます |

{style="table-layout:auto"}

追加の列：

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Order Status] | 注文ステータスを示します |
| [!UICONTROL Purchased From] | 注文が行われた web サイト、ストア、ストア表示を示します |
| [!UICONTROL Customer Name] | 注文した顧客または購入者の名前 |
| [!UICONTROL Email] | 登録された顧客の E メール アドレス |
| [!UICONTROL Customer Group] | 顧客が割り当てられている顧客グループまたは共有カタログの名前 |
| [!UICONTROL Billing Address] | 注文した顧客または購入者の名前 |
| [!UICONTROL Shipping Address] | 注文の出荷先の名前 |
| [!UICONTROL Payment Method] | 注文に使用される支払い方法 |
| [!UICONTROL Shipping Information] | 注文を出荷するために使用される方法 |

{style="table-layout:auto"}

## 出荷の作成

以下の手順に従って、Adobe CommerceまたはMagento Open Sourceで商品を作成します。 Inventory managementを有効にしている場合は、次の点を確認してください [マルチソース出荷の作成](../inventory-management/shipments-create.md) ライン品目ごとに送信するソース（または場所）と数量を選択します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッド内の順序を見つけて開きます。

1. 注文が支払われ、請求が行われ、出荷準備が整ったら、 **[!UICONTROL Ship]**.

   出荷の上部のセクションには、販売注文の名前、住所、支払い情報が含まれています。

1. 次の節の手順を使用して、出荷フォームの各セクションに入力します。

### [!UICONTROL Items to Ship]

注文の各行項目に対して、 **[!UICONTROL Qty to Ship]** 必要に応じて。

### [!UICONTROL Shipping Information]

**メソッド 1:** 注文ページの使用

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. が含まれる **[!UICONTROL Action]** 選択したオーダーの列で、 **[!UICONTROL View]**.

1. クリック **[!UICONTROL Ship]**.

1. にスクロール ダウンします。 _[!UICONTROL Payment & Shipping Method]_ブロックしてクリック&#x200B;**[!UICONTROL Add Tracking Number]**.

1. を設定 **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. 出荷を追跡するには、 **[!UICONTROL Title]** および **[!UICONTROL Number]** .

**メソッド 2:** 出荷ページの使用

この方法は、注文ページから既に注文出荷が作成されている場合にのみ使用できます。
必要に応じて、「直接出荷」ページを使用して、出荷情報および追跡情報を変更できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 出荷を検索し、編集モードで開きます。

1. にスクロール ダウンします。 _[!UICONTROL Payment & Shipping Method]_ブロック。

1. 「」を選択します **[!UICONTROL Carrier]**.

1. を入力 **[!UICONTROL Title]** パッケージ用。

1. トラッキングを入力 **[!UICONTROL Number]**.

1. クリック **[!UICONTROL Add]**.

1. トラッキング情報を記載した E メールを顧客に送信するには、 **[!UICONTROL Send Tracking Information]**&#x200B;をクリックし、アクションを確認します。

   出荷の場所を追跡するには、必要な出荷を編集モードで開き、 **[!UICONTROL Track this shipment]**.

   ![配送情報および追跡情報](./assets/tracking-information.png){width="600" zoomable="yes"}

### ボタン

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 新規出荷フォームをクローズし、受注に戻ります |
| **[!UICONTROL Submit Shipment]** | 注文の出荷を追加します。 |
| **[!UICONTROL Reset]** | すべてのフィールドを元の値に戻します。 |

{style="table-layout:auto"}

### 発送用コメント

1. Enter **コメント** 必要に応じて、出荷に対して。

1. 出荷の準備ができたら、 **出荷の発行**.

## 出荷のコメントを設定します

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 次の下 _[!UICONTROL Sales]_を選択&#x200B;**[!UICONTROL Sales Email]**.

1. を展開します。 **出荷コメント** を切り替え、必要に応じて設定を変更します。

   ![出荷コメントの構成](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - この **[!UICONTROL Enabled]** オプションの設定 `Yes` デフォルトでは、出荷コメントが入力されると、メールが顧客に送信されます。

   - の場合 **[!UICONTROL Shipment Comment Email Sender]**&#x200B;出荷注釈メールの送信元を選択します。 デフォルトでは、5 つのメールアドレスが提供されます。

   - の場合 **[!UICONTROL Shipment Comment Email Template]**&#x200B;必要に応じてテンプレートを選択するか、デフォルトオプションを選択します。

   - の場合 **[!UICONTROL Shipment Comment Email Template for Guests]**&#x200B;で、ストアにアカウントを持っていないお客様に使用するテンプレートを選択します。

   - の場合 **[!UICONTROL Shipment Comment Email Copy To]**&#x200B;を入力し、出荷コメントのメールコピーを送信するメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - の場合 **[!UICONTROL Shipment Comment Email Copy Method]**&#x200B;を選択 `bcc` （ブラインドカーボンコピー）または `separate email copy` 使用する環境に応じて選択します。

1. クリック **[!UICONTROL Save Config]**.

## 出荷の取消

出荷が運送業者に発送される前に、運送業者が取消をサポートしている場合は、受注をオープンして出荷にナビゲートすることで取消を実行できます。 一部の通信事業者は、予約後のキャンセルを制限または制限しています。 たとえば、UPS はキャンセルを許可しますが、出荷が予約されてから 24 時間待つ必要があります。 出荷が取り消された場合は、取消を取り消すことはできません。 唯一の方法は、注文を再作成することです。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッド内の順序を検索します。

1. が含まれる _アクション_ 列、を選択 **[!UICONTROL View]**.

1. 左パネルで、を選択します。 **[!UICONTROL Shipments]**.

   出荷を取り消すことができる場合は、 _[!UICONTROL Cancel Shipment]_は、上部のボタンバーにオプションとして表示されます。

1. クリック **[!UICONTROL Cancel Shipment]**.

1. 確認を求められたら、 **[!UICONTROL OK]**.

出荷のステータスが「」に変わります `Canceled`. 配送業者がキャンセルをサポートしていない場合は、エラーメッセージが表示され、出荷をキャンセルできなかった理由が説明されます。

## 出荷フィールドの説明

### [!UICONTROL Shipping Information]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Carrier] | 選択した通信事業者の名前 |
| [!UICONTROL Title] | 配送業者によってパッケージに割り当てられた説明的な名前。 |
| [!UICONTROL Number] | パッケージに割り当てられるリンクされたトラッキング番号。 |
| [!UICONTROL Action] | ![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png)  – 出荷レコードからパッケージ情報を削除します。 |
| [!UICONTROL Add] | 別のパッケージを出荷に追加します。 |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Origin Location] | 使用可能なロケーションのリストが表示されます。 |
| [!UICONTROL International] | オンにすると、国際出荷として出荷が識別されます。 |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Description] | 項目の説明。 |
| [!UICONTROL SKU] | 品目の在庫管理単位。 |
| [!UICONTROL Weight] | アイテムの重み。 |
| [!UICONTROL Qty Ordered] | 注文された品目の数量。 |
| [!UICONTROL Qty Shipped] | 出荷された品目の数量。 |
| [!UICONTROL Qty Packed] | このパッケージに含まれる項目の数。 |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Comments] | 出荷に関するコメントは社内用です。 |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG**  – 出荷パッケージラベルをダウンロードします。 サイズ：A6 （105 x 148 mm、4.1 x 5.6 インチ） |

{style="table-layout:auto"}
