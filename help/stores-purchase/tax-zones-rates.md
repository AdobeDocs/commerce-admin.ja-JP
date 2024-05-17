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

税率は、通常、特定の地理的領域内で行われる取引に適用されます。 の使用 _税ゾーンと税率_ 税金を収集および送金する各地域の税率を指定するツール。 各税金ゾーンと税率には一意の識別子があるので、特定の地域に対して複数の税率を設定できます（食品や医薬品には課税しないが、その他の品目には課税する場所など）。

店舗税は、店舗の住所に基づいて計算されます。 注文の実際の顧客税は、顧客が注文情報を完了した後に計算されます。 次に、Commerceは店舗の税金構成に従って税金を計算します。

![税ゾーンと税率](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## 新しい税率を定義

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Tax Rate]**.

   ![新しい税率](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. を入力 **[!UICONTROL Tax Identifier]**.

1. 税率を 1 つの郵便番号に適用するには、次のコードを入力します **[!UICONTROL Zip/Post Code]**.

   アスタリスクワイルドカード（`*`）を使用して、コード内の最大 10 文字と一致させることができます。 例： `90*` 90000 ～ 90999 のすべての郵便番号を表します。

1. 郵便番号の範囲に税率を適用するには、次の手順を実行します。

   - 「」を選択します **[!UICONTROL Zip/Post is Range]** チェックボックスをオンにして、の最初と最後の郵便番号を入力して範囲を定義します **[!UICONTROL Range From]** および **[!UICONTROL Range To]**.

     ![ZIP/Post が範囲](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL State]** 税率が適用されます。

   - を選択します。 **[!UICONTROL Country]** 税率が適用されます。

   - を入力 **[!UICONTROL Rate Percent]** これは税率計算に使用されます。

1. 複数のストアがある場合は、を設定できます **[!UICONTROL Tax Titles]** （ストア表示ごとに表示）。

   >[!NOTE]
   >
   >税金識別子を使用する場合は、このフィールドを空のままにします。

1. 完了したら、 **[!UICONTROL Save Rate]**.

## 既存の税率を編集

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. での税率の検索 _[!UICONTROL Tax Zones and Rates]_グリッドを使用し、編集モードでレコードを開きます。

   リストに多くの料金がある場合は、 [フィルターコントロール](../getting-started/admin-grid-controls.md) 必要なレートを見つけるために。

1. に対して必要な変更を行います。 **[!UICONTROL Tax Rate Information]**.

1. を更新 **[!UICONTROL Tax Titles]** 必要に応じて。

1. 完了したら、 **[!UICONTROL Save Rate]**.

## 税率を削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 削除する税率を検索し、編集モードで開きます。

1. メニューバーで、 **[!UICONTROL Delete Rate]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.
