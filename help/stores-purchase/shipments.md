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

_[!UICONTROL Shipments]_&#x200B;グリッドには、出荷用に準備されたすべての請求書の出荷記録が表示されます。 出荷レコードは、注文が [ 請求 ](invoices.md) 以降の場合に生成できます。

Adobe CommerceとMagento Open Sourceでは、[Inventory management](../inventory-management/introduction.md) およびサードパーティの拡張機能から利用できるその他のオプションを使用して、部分的な注文と完全な注文の出荷をサポートしています。

![ 出荷グリッド ](./assets/shipments.png){width="600" zoomable="yes"}

## 列の説明

| 列またはコントロール | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となる各見積もりのチェックボックスを選択するか、列見出しの選択コントロールを使用します。 オプション：`Select All` / `Deselect All` |
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

以下の手順に従って、Adobe CommerceまたはMagento Open Sourceで商品を作成します。 Inventory managementを使用可能にしている場合は、[ 複数Source納入の作成 ](../inventory-management/shipments-create.md) を検討し、明細品目ごとに送付するソース（または事業所）と数量を選択できます。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Orders]** に移動します。

1. グリッド内の順序を見つけて開きます。

1. 注文が支払われ、請求され、出荷準備が整ったら、「**[!UICONTROL Ship]**」をクリックします。

   出荷の上部のセクションには、販売注文の名前、住所、支払い情報が含まれています。

1. 次の節の手順を使用して、出荷フォームの各セクションに入力します。

### [!UICONTROL Items to Ship]

注文の各品目に対して、必要に応じて **[!UICONTROL Qty to Ship]** を変更します。

### [!UICONTROL Shipping Information]

**方法 1:** 注文ページの使用

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Orders]** に移動します。

1. 選択した注文の [**[!UICONTROL Action]**] 列で、[**[!UICONTROL View]**] をクリックします。

1. 「**[!UICONTROL Ship]**」をクリックします。

1. _[!UICONTROL Payment & Shipping Method]_&#x200B;ブロックまで下にスクロールし、「**[!UICONTROL Add Tracking Number]**」をクリックします。

1. Set **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. 出荷を追跡するには、**[!UICONTROL Title]** と **[!UICONTROL Number]** を入力します。

**方法 2:** 出荷ページの使用

この方法は、注文ページから既に注文出荷が作成されている場合にのみ使用できます。
必要に応じて、「直接出荷」ページを使用して、出荷情報および追跡情報を変更できます。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Shipments]** に移動します。

1. 出荷を検索し、編集モードで開きます。

1. _[!UICONTROL Payment & Shipping Method]_&#x200B;ブロックまで下にスクロールします。

1. **[!UICONTROL Carrier]** を選択します。

1. パッケージ **[!UICONTROL Title]** を入力します。

1. 追跡 **[!UICONTROL Number]** を入力します。

1. 「**[!UICONTROL Add]**」をクリックします。

1. トラッキング情報を含むメールを顧客に送信するには、「**[!UICONTROL Send Tracking Information]**」をクリックし、アクションを確認します。

   出荷の場所を追跡するには、必要な出荷を編集モードで開き、「**[!UICONTROL Track this shipment]**」をクリックします。

   ![ 配送情報および追跡情報 ](./assets/tracking-information.png){width="600" zoomable="yes"}

### ボタン

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 新規出荷フォームをクローズし、受注に戻ります |
| **[!UICONTROL Submit Shipment]** | 注文の出荷を追加します。 |
| **[!UICONTROL Reset]** | すべてのフィールドを元の値に戻します。 |

{style="table-layout:auto"}

### 発送用コメント

1. 必要に応じて、出荷の **コメント** を入力します。

1. 出荷の準備が整ったら、「**出荷の発行**」をクリックします。

## 出荷のコメントを設定します

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 「_[!UICONTROL Sales]_」で、「**[!UICONTROL Sales Email]**」を選択します。

1. 「**出荷コメント**」セクションを展開し、必要に応じて設定を変更します。

   ![ 出荷コメントの構成 ](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enabled]** オプションはデフォルトで `Yes` に設定されています。つまり、出荷コメントが入力されると、メールが顧客に送信されます。

   - **[!UICONTROL Shipment Comment Email Sender]**：出荷コメントの電子メールの送信元の人物を選択します。 デフォルトでは、5 つのメールアドレスが提供されます。

   - **[!UICONTROL Shipment Comment Email Template]**：要件に基づいてテンプレートを選択するか、デフォルトオプションを選択します。

   - **[!UICONTROL Shipment Comment Email Template for Guests]** しくは、ストアにアカウントを持たない顧客に使用するテンプレートを選択します。

   - **[!UICONTROL Shipment Comment Email Copy To]**：出荷コメントの電子メール・コピーを送信する電子メール・アドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - **[!UICONTROL Shipment Comment Email Copy Method]** の場合は、「`bcc` （ブラインドカーボンコピー）」または「`separate email copy` 法」を選択します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 出荷の取消

出荷が運送業者に発送される前に、運送業者が取消をサポートしている場合は、受注をオープンして出荷にナビゲートすることで取消を実行できます。 一部の通信事業者は、予約後のキャンセルを制限または制限しています。 たとえば、UPS はキャンセルを許可しますが、出荷が予約されてから 24 時間待つ必要があります。 出荷が取り消された場合は、取消を取り消すことはできません。 唯一の方法は、注文を再作成することです。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Orders]** に移動します。

1. グリッド内の順序を検索します。

1. 「_アクション_」列で「**[!UICONTROL View]**」を選択します。

1. 左側のパネルで「**[!UICONTROL Shipments]**」を選択します。

   出荷をキャンセルできる場合は、上部のボタンバーにオプションとして _[!UICONTROL Cancel Shipment]_&#x200B;が表示されます。

1. 「**[!UICONTROL Cancel Shipment]**」をクリックします。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL OK]**」をクリックします。

出荷のステータスが「`Canceled`」に変わります。 配送業者がキャンセルをサポートしていない場合は、エラーメッセージが表示され、出荷をキャンセルできなかった理由が説明されます。

## 出荷フィールドの説明

### [!UICONTROL Shipping Information]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Carrier] | 選択した通信事業者の名前 |
| [!UICONTROL Title] | 配送業者によってパッケージに割り当てられた説明的な名前。 |
| [!UICONTROL Number] | パッケージに割り当てられるリンクされたトラッキング番号。 |
| [!UICONTROL Action] | ![ ごみ箱アイコン ](../assets/icon-delete-trashcan-solid.png) – 出荷レコードからパッケージ情報を削除します。 |
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
| [!UICONTROL Package Label] | **PNG** – 出荷パッケージラベルをダウンロードします。 サイズ：A6 （105 x 148 mm、4.1 x 5.6 インチ） |

{style="table-layout:auto"}
