---
title: 戻り値
description: 返品ワークフローと返品承認の発行について説明します。
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# 戻り値

交換または払い戻しのために商品を返品することをリクエストするお客様には、_返品商品承認_ （RMA）を付与できます。 通常、顧客はマーチャントに連絡して払い戻しをリクエストします。 承認されると、返される製品を識別する一意の RMA 番号が割り当てられます。 この設定では、すべての製品に対して RMA を有効にするか、特定の製品にのみ RMA を許可するかを指定できます。 _[!UICONTROL Returns]_&#x200B;グリッドには、現在の返品要求（RMA）がリストされ、新しい返品要求を入力するために使用されます。

![&#x200B; グリッドを返します &#x200B;](./assets/return.png){width="600" zoomable="yes"}

RMA は、シンプル、グループ化、設定可能、バンドル製品タイプに対して発行できます。 ただし、仮想製品、ダウンロード可能な製品、ギフトカードでは RMA を使用できません。

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となる返品のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション：`Select All`/`Deselect All`/`Select Visible`/`Unselect Visible` |
| [!UICONTROL RMA] | 各返品に割り当てられる一意の数値識別子 |
| [!UICONTROL Requested] | 返品された日時 |
| [!UICONTROL Order] | 元の注文の一意の番号 |
| [!UICONTROL Ordered] | 注文された日時 |
| [!UICONTROL Customer] | 注文した顧客または購入者の名前 |
| [!UICONTROL Status] | ステータスを返します。 オプション：`Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** は、リターンを編集モードで開きます。 |

{style="table-layout:auto"}

## RMA と再来訪ワークフロー

1. **リクエストを受信** - ストアフロントに対して [&#x200B; 有効 &#x200B;](rma-configure.md#enable-rmas-for-your-store) になっている場合、登録ユーザーとゲストの両方が RMA をリクエストできます。 また、[&#x200B; 管理者で RMA リクエストを送信する &#x200B;](#create-a-return-request-in-the-admin) こともできます。

2. **RMA 発行済み** - リクエストを検討した後、リクエストを部分的または完全に承認したり、リクエストをキャンセルしたりできます。 返品を承認し、返品出荷の支払いに同意した場合は、サポートされている通信事業者で管理者から出荷注文を作成できます。

3. **受入商品および返品処理済** – 次のフロー・チャートは、返品処理を完了するための作業指示を示しています。

   ![&#x200B; 製品返品ワークフロー &#x200B;](./assets/workflow-customer-returns.png){width="500"}

## RMA ステータス

返品承認（RMA）には、ライフサイクル中に多数のステータス（保留や承認済みなど）が割り当てられている場合があります。 RMA ステータスは、ユーザーまたはマーチャントから発行された RMA リクエストの進行状況を示します。

| ステータス | 説明 |
|--- |--- |
| [!UICONTROL Pending] | ストアフロントのユーザーまたは管理者のマーチャントによって RMA リクエストが発生した場合に、そのリクエストに割り当てられる最初のステータス。 |
| [!UICONTROL Authorized] | このステータスは、リクエストされたすべての項目が返品について管理者のマーチャントによって承認された場合に RMA に割り当てられます。 |
| [!UICONTROL Partially Authorized] | リクエストされた項目のいずれかが拒否され、他の製品が承認された場合、このステータスが RMA に割り当てられます。 |
| [!UICONTROL Denied] | 要求されたすべての品目が返品に対して管理担当者によって拒否された場合、このステータスが RMA に割り当てられます。 |
| [!UICONTROL Return Received] | このステータスは、要求された品目がユーザーから受け取られると、マーチャントによって RMA に割り当てられます。 |
| [!UICONTROL Return Partially Received] | このステータスは、要求された品目が部分的に返品され、一部の品目が処理を拒否されると、マーチャントによって RMA に割り当てられます。 |
| [!UICONTROL Approved] | このステータスは、要求された品目が承認され、さらに処理されると、マーチャントによって RMA に割り当てられます。 |
| [!UICONTROL Rejected] | このステータスは、要求された品目がさらに処理するために拒否されると、マーチャントによって RMA に割り当てられます。 |
| [!UICONTROL Processed and Closed] | このステータスは、要求されたすべての品目が承認され、さらに処理されると、マーチャントによって RMA に割り当てられます。 |
| [!UICONTROL Closed] | このステータスは、要求された品目が返品の処理を拒否されたときに、マーチャントによって RMA に割り当てられます。 |

{style="table-layout:auto"}

## 管理者での再来訪リクエストの作成

マーチャントは、顧客に代わって管理者から返品リクエストを作成できます。 お客様は、Adobe Commerce ストアのストアフロントで [&#x200B; 返品リクエストを作成 &#x200B;](rma-customer-experience.md) できます。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Returns]** に移動します。

1. 「**[!UICONTROL New Return Request]**」をクリックします。

1. 返品要求を作成するには、`Complete` のステータスを持つ受注をクリックします。

1. 「_[!UICONTROL Return Information]_」セクションで、「**[!UICONTROL Return Items]**」タブを選択します。

1. 戻るアイテムを追加するには、[**[!UICONTROL Add Items]**] をクリックします。

1. 必要な製品のチェックボックスをオンにして、「**[!UICONTROL Add Selected Product to returns]**」をクリックします。

1. **[!UICONTROL Requested]**：返される項目の数を入力します。

1. **[!UICONTROL Return Reason]** を次のいずれかに設定します。

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   返品の理由がリストされた選択肢と異なる場合は、「`Other`」オプションを選択すると、独自の理由を入力できます。

1. **[!UICONTROL Item Condition]** を次のいずれかに設定します。

   - `Unopened`
   - `Opened`
   - `Damaged`

1. **[!UICONTROL Resolution]** を次のいずれかに設定します。

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. 返品を作成するには、「**[!UICONTROL Submit Returns]**」をクリックします。

   ![RMA 項目が要求されました &#x200B;](./assets/return-item-request.png){width="600" zoomable="yes"}

   新しく送信された RMA リクエストが、`Pending` ステータスで **[!UICONTROL Returns]** ページに表示されます。
