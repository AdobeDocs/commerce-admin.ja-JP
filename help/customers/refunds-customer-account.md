---
title: 顧客アカウントダッシュボードでの返金
description: 店舗のお客様は、アカウントダッシュボードで注文に関連付けられた返金情報を表示できます。
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/ggaeec6NA2K12-eHl7ESC10nU2u11ihbaxaPlbNAE9I
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# 顧客アカウントダッシュボードでの返金

{{ee-feature}}

注文に対して払い戻しが発行された場合、顧客はアカウントダッシュボードで注文に関連付けられた払い戻し情報を表示できます。 [ ストアクレジット設定](../customers/credit-configure.md)について「[!UICONTROL _ストアクレジット履歴を顧客に表示_]」オプションを有効にしている場合、顧客は[ ストアクレジット ](../customers/store-credit.md)履歴にもアクセスできます。

## ストアフロントで返金を表示する

1. ストアフロントから、顧客は自分のアカウントにログインします。

1. 次のいずれかの方法を使用して、注文を検索します。

   * **最近の注文**&#x200B;のリストで注文を検索し、**[!UICONTROL View]**&#x200B;をクリックします。
   * 左側のパネルで、**[!UICONTROL My Orders]**&#x200B;を選択します。 次に、リスト内の順序を見つけて、**[!UICONTROL View]**&#x200B;をクリックします。

1. お客様は「**[!UICONTROL Refunds]**」タブをクリックして、払い戻しの詳細を表示します。

   ![ ストアフロントでの詳細の払い戻し](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## ストアフロントでストアクレジット残高と履歴を表示する

方法1: **顧客アカウントダッシュボード**&#x200B;から

1. ストアフロントから、顧客はアカウントにログインします。

1. 返金がストアクレジットに適用された場合、左側のパネルで「**[!UICONTROL Store Credit]**」を選択します。

1. ストアクレジットに返金された金額は、アクションの日時と共にリストに表示されます。

   ![ クレジットの保管に返金された金額](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >Store Credit ページには、お客様が[ ギフトカード ](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card)を引き換えるためのリンクも表示されます。

方法2: **_レビューと支払い_ ページ**&#x200B;から

1. 顧客が商品をカートに追加しました。

2. _チェックアウト_ ページに進みます。

3. **[!UICONTROL Shipping]** ステップを通過します。

4. ストアクレジットが利用可能な場合、顧客は&#x200B;**[!UICONTROL Use Store Credit]**&#x200B;をクリックします。

   ![ レビューと支払いページからクレジットを保管](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. お客様がストアクレジットの使用に関する考えを変更した場合、「_注文概要_」セクションの「**[!UICONTROL Remove]**」をクリックします。

## 管理画面での支払いアクション

特定の[支払い方法](../configuration-reference/sales/payment-methods.md)に対して支払いアクションを設定できます。 各支払い方法には、さまざまな支払いアクションがあります。

| 支払いアクション | 説明 |
|--- |---|
| [!UICONTROL Capture Online] | 請求書が送信されると、システムはサードパーティの支払いゲートウェイから支払いをキャプチャします。 その後、管理者ユーザーはクレジットメモを作成し、請求書を無効にすることができます。 |
| [!UICONTROL Capture Offline] | 請求書が送信された場合、システムは支払いをキャプチャしません。 支払いはゲートウェイを通じて直接取得され、支払いはAdobe Commerceを通じて取得できないことが前提となります。 その後、管理者ユーザーはクレジットメモを作成できますが、請求書を無効にすることはできません。 （注文がオンライン決済を使用していたとしても、請求書は基本的にオフラインの請求書です）。 |
| [!UICONTROL Not Capture] | 請求書が送信された場合、システムは支払いをキャプチャしません。 支払いは、後でAdobe Commerceを通じてキャプチャされると想定されます。 完了した請求書に&#x200B;[!UICONTROL _Capture_] ボタンがあります。 取り込む前に、請求書をキャンセルできます。 キャプチャ後、クレジットメモを作成し、請求書を無効にすることができます。 |

{style="table-layout:auto"}

>[!WARNING]
>
>後でAdobe Commerceを通じて支払いを取り込むことに確信がない限り、[!UICONTROL _取り込みしない_] オプションを選択します。 支払いが&#x200B;[!UICONTROL _キャプチャ_] ボタンを使用してキャプチャされるまで、クレジットメモを作成することはできません。
