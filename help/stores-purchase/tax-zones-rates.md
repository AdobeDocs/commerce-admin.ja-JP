---
title: 税ゾーンと税率
description: 税金を収集して送金する各地域に対して税率を定義する方法を説明します。
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# 税ゾーンと税率

税率は、通常、特定の地理的地域内で発生するトランザクションに適用されます。 以下を使用します。 _税ゾーンと税率_ ツールを使用して、税金を収集および送金する各地理的地域の税率を指定します。 各税ゾーンと税率には一意の識別子が割り当てられているので、特定の地域（食糧や医療に税を課さないが他の品目に税を課す場所など）に対して、複数の税率を割り当てることができます。

店舗税は、店舗の住所に基づいて計算されます。 注文の実際の顧客税は、顧客が注文情報を完了した後に計算されます。 次に、コマースは、ストアの税金設定に基づいて税金を計算します。

![税ゾーンと税率](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## 新しい税率を定義

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 右上隅で、 **[!UICONTROL Add New Tax Rate]**.

   ![新しい税率](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. を入力します。 **[!UICONTROL Tax Identifier]**.

1. 郵便番号に税率を適用するには、 **[!UICONTROL Zip/Post Code]**.

   アスタリスクワイルドカード (`*`) は、コード内の 10 文字まで一致させるために使用できます。 例： `90*` は、90000 ～ 90999のすべての郵便番号を表します。

1. 郵便番号の範囲に税率を適用するには、次の手順を実行します。

   - を選択します。 **[!UICONTROL Zip/Post is Range]** 」チェックボックスに移動し、次の期間の最初と最後の郵便番号を入力して、範囲を定義します。 **[!UICONTROL Range From]** および **[!UICONTROL Range To]**.

     ![ZIP/POST が範囲](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL State]** 税率が適用される場合。

   - を選択します。 **[!UICONTROL Country]** 税率が適用される場合。

   - 次を入力します。 **[!UICONTROL Rate Percent]** 税率の計算に使用される値です。

1. 複数のストアがある場合、 **[!UICONTROL Tax Titles]** 各ストア表示に対して

   >[!NOTE]
   >
   >税金識別子を使用する場合は、このフィールドを空のままにします。

1. 完了したら、「 **[!UICONTROL Save Rate]**.

## 既存の税率の編集

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 税率を _[!UICONTROL Tax Zones and Rates]_グリッドを開き、編集モードでレコードを開きます。

   リストに多くの料金がある場合は、 [フィルターコントロール](../getting-started/admin-grid-controls.md) 必要な料金を見つけるために。

1. 必要な変更を **[!UICONTROL Tax Rate Information]**.

1. を更新します。 **[!UICONTROL Tax Titles]** 必要に応じて。

1. 完了したら、「 **[!UICONTROL Save Rate]**.

## 税率の削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 削除する税率を見つけ、編集モードで開きます。

1. メニューバーで、 **[!UICONTROL Delete Rate]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.
