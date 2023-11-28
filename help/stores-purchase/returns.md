---
title: 戻り値
description: 返品ワークフローと返品された商品認証の発行について説明します。
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# 戻り値

A _返品された商品認証_ (RMA) は、交換用または返金用の品目の返品を要求する顧客に付与できます。 通常、顧客はマーチャントに連絡して返金を要求します。 承認済の場合は、返品された製品を識別するために一意の RMA 番号が割り当てられます。 この構成では、すべての製品に対して RMA を有効にするか、特定の製品に対してのみ RMA を許可することができます。 The _[!UICONTROL Returns]_grid は、現在の返品要求 (RMA) をリストし、新しい返品要求の入力に使用します。

![グリッドを返します](./assets/return.png){width="600" zoomable="yes"}

RMA は、シンプル、グループ化、構成、およびバンドルの製品タイプに対して発行できます。 ただし、仮想製品、ダウンロード可能な製品、ギフトカードでは RMA を利用できません。

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となる戻り値のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション： `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL RMA] | 各戻り値に割り当てられる一意の数値識別子 |
| [!UICONTROL Requested] | リターンがおこなわれた日時 |
| [!UICONTROL Order] | 元の注文の一意の番号 |
| [!UICONTROL Ordered] | 注文が行われた日時 |
| [!UICONTROL Customer] | 注文を行った顧客または購入者の名前 |
| [!UICONTROL Status] | ステータスを返します。 オプション： `Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** 編集モードで戻り値を開きます。 |

{style="table-layout:auto"}

## RMA および返品ワークフロー

1. **リクエストを受信** - If [有効](rma-configure.md#enable-rmas-for-your-store) ストアフロントの場合、登録ユーザーとゲストの両方が RMA を要求できます。 また、 [管理者で RMA 要求を発行](#create-a-return-request-in-the-admin).

2. **RMA 発行済**  — リクエストを検討した後、リクエストを部分的に承認する、完全に承認する、またはリクエストをキャンセルすることができます。 返品を承認し、返品出荷の支払いに同意した場合は、管理者から、サポートされている運送業者との出荷注文を作成できます。

3. **受け取った商品と製品の返品処理**  — 次のフロー・チャートは、返品プロセスを完了するためのオペレーショナル・オーダーを示しています。

   ![製品返品ワークフロー](./assets/workflow-customer-returns.png){width="500"}

## RMA ステータス

ライフサイクルの間、返品された商品承認 (RMA) には、多くのステータス（保留中や承認済みなど）が割り当てられる場合があります。 RMA ステータスは、ユーザーまたはマーチャントが発生した RMA 要求の進行状況を示します。

| ステータス | 説明 |
|--- |--- |
| [!UICONTROL Pending] | ストアフロント上のユーザーまたは管理者のマーチャントによって RMA 要求が発行された際に RMA 要求に割り当てられた初期ステータス。 |
| [!UICONTROL Authorized] | このステータスは、要求されたすべての品目が管理者のマーチャントによって返品に対して承認された場合に RMA に割り当てられます。 |
| [!UICONTROL Partially Authorized] | 要求された品目のいずれかが拒否され、他の製品が承認された場合、このステータスが RMA に割り当てられます。 |
| [!UICONTROL Denied] | このステータスは、返品に関して管理者のマーチャントによって要求されたすべての品目が拒否された場合に RMA に割り当てられます。 |
| [!UICONTROL Return Received] | このステータスは、要求された品目がユーザーから受け取られた場合に、RMA に対してマーチャントによって割り当てられます。 |
| [!UICONTROL Return Partially Received] | このステータスは、要求された品目が部分的に返品され、一部の品目が処理を拒否された場合に、RMA に対して商人によって割り当てられます。 |
| [!UICONTROL Approved] | このステータスは、要求品目がさらに処理するために承認された場合に、RMA に対してマーチャントによって割り当てられます。 |
| [!UICONTROL Rejected] | このステータスは、要求品目が後で処理するために拒否された場合に、RMA に対してマーチャントによって割り当てられます。 |
| [!UICONTROL Processed and Closed] | このステータスは、要求されたすべての品目がさらに処理するために承認された場合に、RMA に対してマーチャントによって割り当てられます。 |
| [!UICONTROL Closed] | このステータスは、要求された品目が返品処理を拒否された場合に、RMA に対してマーチャントによって割り当てられます。 |

{style="table-layout:auto"}

## 管理者での返信リクエストの作成

マーチャントは、顧客に代わって管理者から返品依頼を作成できます。 お客様が [return リクエストの作成](rma-customer-experience.md) Adobe Commerce店の店の店頭で

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. クリック **[!UICONTROL New Return Request]**.

1. 返品リクエストを作成するには、 `Complete` ステータス。

1. の下 _[!UICONTROL Return Information]_セクションで、**[!UICONTROL Return Items]**タブをクリックします。

1. 返す項目を追加するには、 **[!UICONTROL Add Items]**.

1. 必要な製品のチェックボックスを選択し、 **[!UICONTROL Add Selected Product to returns]**.

1. の場合 **[!UICONTROL Requested]**&#x200B;に値を入力する場合は、返す項目数を入力します。

1. 設定 **[!UICONTROL Return Reason]** を次のいずれかに変更します。

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   返品の理由がリストに表示された選択肢と異なる場合は、 `Other` オプション。

1. 設定 **[!UICONTROL Item Condition]** を次のいずれかに変更します。

   - `Unopened`
   - `Opened`
   - `Damaged`

1. 設定 **[!UICONTROL Resolution]** を次のいずれかに変更します。

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. リターンを作成するには、 **[!UICONTROL Submit Returns]**.

   ![要求された RMA 品目](./assets/return-item-request.png){width="600" zoomable="yes"}

   新しく送信された RMA 要求は、 **[!UICONTROL Returns]** ページと `Pending` ステータス。
