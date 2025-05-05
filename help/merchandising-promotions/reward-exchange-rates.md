---
title: 報酬為替レート
description: 獲得した報酬ポイントの数を決定する報酬為替レートを設定する方法を説明します。
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# 報酬為替レート

{{ee-feature}}

報酬の為替レートは、注文金額と獲得したポイントの価値に基づいて獲得したポイント数を決定します。 異なる為替レートは、異なる web サイトや異なる顧客グループに適用できます。 異なる Web サイトや顧客グループの複数の為替レートが同じ顧客に適用される場合、次の優先ルールが適用されます。

## 為替レートの優先度

**1**：特定の web サイトおよび特定の顧客グループに適用されます。

**2**：すべての web サイトと特定の顧客グループに適用されます。

**3**：特定の web サイトとすべての顧客グループに適用されます。

**4**：すべての web サイトとすべての顧客グループに適用されます。

通貨をポイントに変換する場合、ポイント数を分割することはできません。 残りの通貨は切り捨てられます。 例えば、$2.00 が 10 ポイントに換算された場合、ポイントは$2.00 のグループで獲得されます。したがって、$7.00 の注文は 30 ポイントを獲得し、残りの$1.00 は切り捨てられます。 注文の金額は、マーチャントが受け取る金額、または総計から送料、税金、割引、店舗クレジット、ギフトカードを差し引いた金額として定義されます。 ポイントは、注文に非請求項目がない時点で獲得されます（すべての項目は有料またはキャンセルされています）。 管理者ユーザーが、キャンセルされた注文に対する報酬ポイントの獲得を顧客に許可しない場合は、それらのポイントを顧客の管理ページから手動で差し引くことができます。

## 為替レートの設定

![ 報酬為替レート ](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Other Settings]_/**[!UICONTROL Reward Exchange Rates]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add New Rate]**」をクリックします。

1. **[!UICONTROL Reward Exchange Rate Information]** セクションで、次の操作を行います。

   ![ 報酬為替レート – 情報 ](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - 報酬為替レートが適用されるサイトに **[!UICONTROL Website]** を設定します。

   - 報酬の為替レートが適用されるグループに **[!UICONTROL Customer Group]** を設定します。

   - **[!UICONTROL Direction]** を次のいずれかに設定します。

      - `Points to Currency`
      - `Currency to Points`

   どちらの方向設定でも、金額は Web サイトの基本通貨で表されます。

1. _[!UICONTROL Direction]_&#x200B;の設定に従って&#x200B;**[!UICONTROL Rate]**&#x200B;の値を入力します。

   | 方向 | レート設定 |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | 最初の「_[!UICONTROL Rate]_」フィールドに、ポイントの数を入力します。 2 番目の&#x200B;_[!UICONTROL Rate]_ フィールドに、ポイントの金額を入力します。 |
   | [!UICONTROL Currency to Points] | 「最初の _[!UICONTROL Rate]_」フィールドに金額を入力します。 2 番目の&#x200B;_[!UICONTROL Rate]_ フィールドに、金額で表されるポイントの数を入力します。 |

   ポイントを通貨に変換する場合、ポイント数を分割することはできません。 例えば、10 ポイントが 2.00 ドルに換算される場合、ポイントは 10 のグループで交換する必要があります。 したがって、25 ポイントは 4.00 ドルで引き換えられ、5 ポイントが顧客の残高に残ります。

   `Points to Currency` と `Currency to Points` の両方に対してコンバージョンを設定することをお勧めします。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 報酬為替レートの削除

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Other Settings]_/**[!UICONTROL Reward Exchange Rates]**&#x200B;に移動します。

1. 削除する報酬為替レートを見つけて、編集モードで開きます。

1. メニューバーで、「**[!UICONTROL Delete]**」をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Website] | 報酬率が適用される Web サイト。 |
| [!UICONTROL Customer Group] | 報酬レートが適用される顧客グループ。 |
| [!UICONTROL Direction] | 為替レートで定義するトランザクションのタイプを決定します。 オプション：<br/>**[!UICONTROL Points to Currency]**– 注文額に対するクレジットとして適用できるポイントの数を定義します。 最初の「_[!UICONTROL Rate]_」フィールドに、ポイントの数を入力します。 2 番目の&#x200B;_[!UICONTROL Rate]_ フィールドに、ポイントの金額を入力します。<br/>**[!UICONTROL Currency to Points]** – 顧客ポイントを獲得できる注文の量を定義します。 「最初の _[!UICONTROL Rate]_」フィールドに金額を入力します。 2 番目の&#x200B;_[!UICONTROL Rate]_ フィールドに、金額で表されるポイントの数を入力します。 |
