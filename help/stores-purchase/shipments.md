---
title: 発送数
description: 請求書の出荷レコードを作成し、出荷をキャンセルする方法について説明します。
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 0%

---

# 発送数

_[!UICONTROL Shipments]_グリッドには、出荷用に準備されたすべての請求書の出荷記録が一覧表示されます。 注文が[請求済み](invoices.md)以降の場合、出荷レコードを生成できます。

Adobe CommerceとMagento Open Sourceは、部分的な注文と完全な注文の配送をサポートしており、その他のオプションは[Inventory management](../inventory-management/introduction.md)およびサードパーティの拡張機能から利用できます。

![送料グリッド ](./assets/shipments.png){width="600" zoomable="yes"}

## 列の説明

| 列またはコントロール | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となる各引用符のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション：`Select All` / `Deselect All` |
| [!UICONTROL Shipment] | 新しい出荷が初めて保存されたときに割り当てられる一意の連続番号 |
| [!UICONTROL Ship Date] | 発送日 |
| [!UICONTROL Order] | 注文の一意の番号 |
| [!UICONTROL Order Date] | 注文が行われた日時 |
| [!UICONTROL Ship-to Name] | 注文の配送先の名前 |
| [!UICONTROL Total Quantity] | 発送する品目の合計数量 |
| [!UICONTROL Action] | ビューでは、編集モードで出荷が開きます |

{style="table-layout:auto"}

追加の列：

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Order Status] | 注文ステータスを示します |
| [!UICONTROL Purchased From] | 注文が配置されたweb サイト、ストア、ストアビューを示します |
| [!UICONTROL Customer Name] | 注文した顧客または購入者の名前 |
| [!UICONTROL Email] | 登録済みのお客様のメールアドレス |
| [!UICONTROL Customer Group] | 顧客が割り当てられている顧客グループまたは共有カタログの名前 |
| [!UICONTROL Billing Address] | 注文した顧客または購入者の名前 |
| [!UICONTROL Shipping Address] | 注文の配送先の名前 |
| [!UICONTROL Payment Method] | 注文に使用する支払い方法 |
| [!UICONTROL Shipping Information] | 注文の出荷に使用する方法 |

{style="table-layout:auto"}

## 配送の作成

次の手順では、Adobe CommerceまたはMagento Open Sourceで荷物を作成するプロセスについて説明します。 Inventory managementを有効にしている場合は、[複数Sourceの配送を作成](../inventory-management/shipments-create.md)を確認し、行項目ごとに送信するソース（または場所）と数量を選択することができます。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Orders]**&#x200B;に移動します。

1. グリッド内の順序を見つけて開きます。

1. 注文が支払われ、請求され、発送準備ができている場合は、**[!UICONTROL Ship]**&#x200B;をクリックします。

   出荷の上部のセクションには、販売注文の名前、住所、支払い情報が含まれています。

1. 次のセクションの手順に従って、出荷フォームの各セクションに記入してください。

### [!UICONTROL Items to Ship]

順序の各行項目について、必要に応じて&#x200B;**[!UICONTROL Qty to Ship]**&#x200B;を変更します。

### [!UICONTROL Shipping Information]

**方法1:**&#x200B;注文ページの使用

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Orders]**&#x200B;に移動します。

1. 選択した注文の&#x200B;**[!UICONTROL Action]**&#x200B;列で、**[!UICONTROL View]**&#x200B;をクリックします。

1. **[!UICONTROL Ship]**&#x200B;をクリックします。

1. _[!UICONTROL Payment & Shipping Method]_ブロックまで下にスクロールし、**[!UICONTROL Add Tracking Number]**をクリックします。

1. **[!UICONTROL Carrier]**&#x200B;を設定：

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. 配送を追跡するには、**[!UICONTROL Title]**&#x200B;と&#x200B;**[!UICONTROL Number]**&#x200B;を入力します。

**方法2:**&#x200B;出荷ページの使用

この方法は、注文出荷が既に注文ページから作成されている場合にのみ使用できます。
直接出荷ページを使用して、必要に応じて出荷および追跡情報を変更できます。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Shipments]**&#x200B;に移動します。

1. 配送を検索して編集モードで開きます。

1. _[!UICONTROL Payment & Shipping Method]_ブロックまでスクロールします。

1. **[!UICONTROL Carrier]**&#x200B;を選択します。

1. パッケージの&#x200B;**[!UICONTROL Title]**&#x200B;を入力します。

1. トラッキング **[!UICONTROL Number]**&#x200B;を入力します。

1. **[!UICONTROL Add]**&#x200B;をクリックします。

1. 追跡情報を含む電子メールをお客様に送信するには、**[!UICONTROL Send Tracking Information]**&#x200B;をクリックして、アクションを確認します。

   任意の出荷の場所を追跡するには、必要な出荷を編集モードで開き、**[!UICONTROL Track this shipment]**&#x200B;をクリックします。

   ![配送情報と追跡情報](./assets/tracking-information.png){width="600" zoomable="yes"}

### ボタン

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 新規出荷フォームを閉じて、注文に戻ります |
| **[!UICONTROL Submit Shipment]** | 注文の出荷を追加します。 |
| **[!UICONTROL Reset]** | すべてのフィールドを元の値に戻します。 |

{style="table-layout:auto"}

### 配送コメント

1. 必要に応じて、出荷用に「**コメント**」と入力します。

1. 出荷の準備ができたら、**出荷を送信**&#x200B;をクリックします。

## 出荷用のコメントの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL Sales]_で、**[!UICONTROL Sales Email]**を選択します。

1. 「**出荷コメント**」セクションを展開し、必要に応じて設定を変更します。

   ![送信コメント設定](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enabled]** オプションはデフォルトで`Yes`に設定されています。これは、配送コメントが入力されたときに電子メールが顧客に送信されることを意味します。

   - **[!UICONTROL Shipment Comment Email Sender]**&#x200B;で、出荷コメントの電子メールの送信元となる人物を選択します。 デフォルトでは、5つのメールアドレスが用意されています。

   - **[!UICONTROL Shipment Comment Email Template]**&#x200B;の場合、要件に基づいてテンプレートを選択するか、デフォルトのオプションを選択します。

   - **[!UICONTROL Shipment Comment Email Template for Guests]**&#x200B;の場合、ストアにアカウントを持たない顧客に使用するテンプレートを選択します。

   - **[!UICONTROL Shipment Comment Email Copy To]**&#x200B;の場合、電子メールアドレスを入力して、出荷コメントの電子メールコピーを送信します。 複数のメールアドレスをコンマで区切ります。

   - **[!UICONTROL Shipment Comment Email Copy Method]**&#x200B;の場合、環境設定に基づいて`bcc` （ブラインドカーボンコピー）または`separate email copy`方法を選択します。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

## 配送をキャンセル

配送が配送業者にディスパッチされる前に、配送業者がキャンセルをサポートしている場合、注文を開いて配送に移動することでキャンセルできます。 一部の航空会社では、予約後のキャンセルを制限または制限しています。 例えば、UPSはキャンセルを許可していますが、発送後24時間待つ必要があります。 配送がキャンセルされた場合、キャンセルを元に戻すことはできません。 唯一の方法は、注文を再作成することです。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Orders]**&#x200B;に移動します。

1. グリッド内の順序を検索します。

1. _アクション_&#x200B;列で、**[!UICONTROL View]**&#x200B;を選択します。

1. 左側のパネルで、**[!UICONTROL Shipments]**&#x200B;を選択します。

   配送をキャンセルできる場合は、_[!UICONTROL Cancel Shipment]_が上部のボタンバーにオプションとして表示されます。

1. **[!UICONTROL Cancel Shipment]**&#x200B;をクリックします。

1. 確認を求められたら、**[!UICONTROL OK]**&#x200B;をクリックします。

出荷の状態が`Canceled`に変更されます。 配送業者がキャンセルをサポートしていない場合は、エラーメッセージが表示され、配送をキャンセルできなかった理由が説明されます。

## 配送フィールドの説明

### [!UICONTROL Shipping Information]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Carrier] | 選択した通信事業者の名前 |
| [!UICONTROL Title] | キャリアによってパッケージに割り当てられたわかりやすい名前。 |
| [!UICONTROL Number] | パッケージに割り当てられているリンクされたトラッキング番号。 |
| [!UICONTROL Action] | ![ごみ箱アイコン ](../assets/icon-delete-trashcan-solid.png) – 出荷レコードからパッケージ情報を削除します。 |
| [!UICONTROL Add] | 荷物に別の荷物を追加します。 |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Origin Location] | 使用可能な場所のリストを表示します。 |
| [!UICONTROL International] | オンにした場合、国際配送として出荷を識別します。 |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Description] | 項目の説明。 |
| [!UICONTROL SKU] | 品目の在庫保管単位。 |
| [!UICONTROL Weight] | 項目の重み。 |
| [!UICONTROL Qty Ordered] | 注文された品目の数量。 |
| [!UICONTROL Qty Shipped] | 発送された品目の数量。 |
| [!UICONTROL Qty Packed] | このパッケージに含まれるアイテムの数。 |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Comments] | 配送に関するコメントは社内用です。 |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** – 出荷パッケージラベルをダウンロードします。 サイズ：A6 （105 x 148mm、4.1 x 5.6 インチ） |

{style="table-layout:auto"}
