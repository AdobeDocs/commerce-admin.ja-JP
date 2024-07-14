---
title: 税ゾーンと税率
description: 税金を収集および送金する各地域の税率を定義する方法を説明します。
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# 税ゾーンと税率

税率は、通常、特定の地理的領域内で行われる取引に適用されます。 _税金ゾーンおよび税率_ ツールを使用して、税金を収集および送金する各地理的領域の税率を指定します。 各税金ゾーンと税率には一意の識別子があるので、特定の地域に対して複数の税率を設定できます（食品や医薬品には課税しないが、その他の品目には課税する場所など）。

店舗税は、店舗の住所に基づいて計算されます。 注文の実際の顧客税は、顧客が注文情報を完了した後に計算されます。 次に、Commerceは店舗の税金構成に従って税金を計算します。

![ 税区及び税率 ](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## 新しい税率を定義

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Zones and Rates]**に移動します。

1. 右上隅の「**[!UICONTROL Add New Tax Rate]**」をクリックします。

   ![ 新税率 ](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. **[!UICONTROL Tax Identifier]** を入力します。

1. 税率を 1 つの郵便番号に適用するには、**[!UICONTROL Zip/Post Code]** のコードを入力します。

   アスタリスクワイルドカード（`*`）は、コード内の最大 10 文字に一致させるために使用できます。 例えば、`90*` は 90000 ～ 90999 のすべての郵便番号を表します。

1. 郵便番号の範囲に税率を適用するには、次の手順を実行します。

   - 「**[!UICONTROL Zip/Post is Range]**」チェックボックスをオンにし、**[!UICONTROL Range From]** と **[!UICONTROL Range To]** の最初と最後の郵便番号を入力して範囲を定義します。

     ![ZIP/Postは範囲 ](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - 税率を適用する **[!UICONTROL State]** を選択します。

   - 税率を適用する **[!UICONTROL Country]** を選択します。

   - 税率計算に使用する **[!UICONTROL Rate Percent]** を入力します。

1. 複数のストアがある場合は、ストア表示ごとに **[!UICONTROL Tax Titles]** を設定できます。

   >[!NOTE]
   >
   >税金識別子を使用する場合は、このフィールドを空のままにします。

1. 完了したら、「**[!UICONTROL Save Rate]**」をクリックします。

## 既存の税率を編集

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Zones and Rates]**に移動します。

1. _[!UICONTROL Tax Zones and Rates]_グリッドで税率を検索し、編集モードでレコードを開きます。

   リストに多くの料率がある場合は、[ フィルターコントロール ](../getting-started/admin-grid-controls.md) を使用して、必要な料率を見つけます。

1. **[!UICONTROL Tax Rate Information]** に対して必要な変更を加えます。

1. 必要に応じて **[!UICONTROL Tax Titles]** を更新します。

1. 完了したら、「**[!UICONTROL Save Rate]**」をクリックします。

## 税率を削除

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Zones and Rates]**に移動します。

1. 削除する税率を検索し、編集モードで開きます。

1. メニューバーで、「**[!UICONTROL Delete Rate]**」をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。
