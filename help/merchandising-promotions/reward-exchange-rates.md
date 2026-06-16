---
title: ポイント換算レート
description: 獲得したポイント数を決定するポイント換算レートを設定する方法を説明します。
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
TQID: https://experienceleague.adobe.com/Iwr92ju0R1z6DFP-5n4O4bqIBYnYWtdn18ImbHJhoHU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 571
ht-degree: 0%

---

# ポイント換算レート

{{ee-feature}}

ポイント換算レートは、注文金額と獲得したポイントの値に基づいて、獲得したポイント数を決定します。 異なる為替レートは、異なるweb サイトや異なる顧客グループに適用できます。 異なるweb サイトや顧客グループからの複数の為替レートが同じ顧客に適用される場合は、次の優先度のルールが適用されます。

## 為替レートの優先度

**1**：特定のWeb サイトおよび特定の顧客グループに適用されます。

**2**：すべてのWeb サイトと特定の顧客グループに適用されます。

**3**：特定のWeb サイトとすべての顧客グループに適用されます。

**4**：すべてのWeb サイトとすべての顧客グループに適用されます。

通貨をポイントに変換する場合、ポイント数は分割できません。 残りの通貨は切り捨てられます。 例えば、2.00 ドルが10 ポイントにコンバージョンした場合、2.00 ドルのグループでポイントが加算されます。 したがって、7.00 ドルの注文は30 ポイントを獲得し、残りの1.00 ドルは切り捨てられます。 注文の金額は、加盟店が受け取る金額、または総送料、税金、割引、店舗のクレジット、ギフトカードを差し引いた金額として定義されます。 ポイントは、注文に未請求のアイテムがない時点で獲得されます（すべてのアイテムが支払われるかキャンセルされます）。 管理者ユーザーがキャンセルされた注文に対する報酬ポイントの獲得を顧客に許可しない場合は、それらのポイントを顧客の管理ページから手動で差し引くことができます。

## 為替レートの設定

![&#x200B; ポイント換算レート &#x200B;](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add New Rate]**」をクリックします。

1. **[!UICONTROL Reward Exchange Rate Information]** セクションで、次の操作を行います。

   ![&#x200B; ポイント換算レート – 情報](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - ポイント換算レートが適用されるサイトに&#x200B;**[!UICONTROL Website]**&#x200B;を設定します。

   - ポイント換算レートが適用されるグループに&#x200B;**[!UICONTROL Customer Group]**&#x200B;を設定します。

   - **[!UICONTROL Direction]**&#x200B;を次のいずれかに設定します：

      - `Points to Currency`
      - `Currency to Points`

   どちらの方向設定でも、金額はweb サイトの基本通貨で表されます。

1. _[!UICONTROL Direction]_&#x200B;設定に従って&#x200B;**[!UICONTROL Rate]**&#x200B;値を入力します。

   | 方向 | レート設定 |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | 最初の&#x200B;_[!UICONTROL Rate]_&#x200B;フィールドに、ポイント数を入力します。 2番目の&#x200B;_[!UICONTROL Rate]_ フィールドに、ポイントの金銭的価値を入力します。 |
   | [!UICONTROL Currency to Points] | 最初の&#x200B;_[!UICONTROL Rate]_&#x200B;フィールドに金銭的価値を入力します。 2番目の&#x200B;_[!UICONTROL Rate]_ フィールドに、金銭的価値で表されるポイント数を入力します。 |

   ポイントを通貨に変換する場合、ポイント数を分割することはできません。 例えば、10 ポイントが2.00 ドルにコンバージョンした場合、10 ポイントをグループで交換する必要があります。 したがって、25 ポイントは4.00 ドルに引き換えられ、顧客の残高には5 ポイントが残ります。

   `Points to Currency`と`Currency to Points`の両方にコンバージョンを設定することをお勧めします。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## ポイント換算レートの削除

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**&#x200B;に移動します。

1. 削除するポイント換算レートを検索し、編集モードで開きます。

1. メニューバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. アクションを確認するには、**[!UICONTROL OK]**&#x200B;をクリックします。

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Website] | 報酬レートが適用されるweb サイト。 |
| [!UICONTROL Customer Group] | 報酬レートが適用される顧客グループ。 |
| [!UICONTROL Direction] | 為替レートで定義されるトランザクションのタイプを指定します。 オプション：<br/>**[!UICONTROL Points to Currency]**– 注文金額に対してクレジットとして適用できるポイント数を定義します。 最初の&#x200B;_[!UICONTROL Rate]_&#x200B;フィールドに、ポイント数を入力します。 2番目の&#x200B;_[!UICONTROL Rate]_ フィールドに、ポイントの金銭的価値を入力します。<br/>**[!UICONTROL Currency to Points]** – 顧客ポイントを獲得できる注文金額を定義します。 最初の&#x200B;_[!UICONTROL Rate]_&#x200B;フィールドに金銭的価値を入力します。 2番目の&#x200B;_[!UICONTROL Rate]_ フィールドに、金銭的価値で表されるポイント数を入力します。 |
