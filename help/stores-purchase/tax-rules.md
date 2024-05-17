---
title: 税務処理基準
description: 製品区分、顧客区分および税率を使用して税務処理基準を定義する方法を説明します。
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# 税務処理基準

税務処理基準には、製品区分、顧客区分および税率の組合せが組み込まれます。 各顧客は顧客クラスに割り当てられ、各製品は製品クラスに割り当てられます。 Commerceは、各顧客の買い物かごを分析し、顧客クラス、商品クラスおよびリージョンに従って適切な税金を計算します。 この地域は、顧客の発送先住所、請求先住所、または発送元に基づいています。

>[!NOTE]
>
>多数の税率を定義する必要がある場合は、税率をインポートしてプロセスを簡略化できます。

![税務処理基準](./assets/tax-rules.png){width="600" zoomable="yes"}

## 手順 1：税務処理基準情報の完了

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Tax Rule]**.

1. 次の下 _税務処理基準情報_、a と入力します **[!UICONTROL Name]** 新しいルール用。

   ![税務処理基準情報](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL Tax Rate]** それは該当する規則だ。

   既存の税率を編集するには、次の手順を実行します。

   - 税率にカーソルを合わせて、 _編集_ ![鉛筆アイコン](../assets/icon-edit-pencil.png) アイコン。

   - 必要に応じてフォームを更新し、 **[!UICONTROL Save]**.

1. 税率を入力するには、次のいずれかの方法を使用します。

### 方法 1：税率の手動入力

1. クリック **[!UICONTROL Add New Tax Rate]**.

1. 必要に応じてフォームに入力します（ [税ゾーンと税率](tax-zones-rates.md)）に設定します。

1. 完了したら、 **[!UICONTROL Save]**.

   ![新しい税率](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### 方法 2：税率のインポート

1. ページの下部のセクションまで下にスクロールします。

1. 税率をインポートするには、次の手順を実行します。

   - クリック **[!UICONTROL Choose File]** 読み込む税率を含む CSV ファイルに移動します。

   - クリック **[!UICONTROL Import Tax Rates]**.

1. 税率をエクスポートするには、 **[!UICONTROL Export Tax Rates]** （を参照） [インポート/エクスポート税率](../systems/data-transfer-tax-rates.md)）に設定します。

![インポート/エクスポート税率](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## 手順 2：追加設定を完了する

1. セクションを開くには、をクリックします **[!UICONTROL Additional Settings]**.

   ![税務処理基準の追加設定](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL Customer Tax Class]** 規則を適用する。

   - 顧客税区分を編集するには、 _編集_ ![鉛筆アイコン](../assets/icon-edit-pencil.png) アイコンをクリックし、必要に応じてフォームを更新して、 **[!UICONTROL Save]**.

   - 税金区分を作成するには、次をクリックします。 **[!UICONTROL Add New Tax Class]**&#x200B;必要に応じてフォームに入力し、 **[!UICONTROL Save]**.

1. を選択します。 **[!UICONTROL Product Tax Class]** 規則を適用する。

   - 製品税区分を編集するには、 _編集_ ![鉛筆アイコン](../assets/icon-edit-pencil.png) アイコンをクリックし、必要に応じてフォームを更新して、 **[!UICONTROL Save]**.

   - 税金区分を作成するには、次をクリックします。 **[!UICONTROL Add New Tax Class]**&#x200B;必要に応じてフォームに入力し、 **[!UICONTROL Save]**.

1. 複数の税金が適用される場合、この税金の優先度を示す数値を入力します **[!UICONTROL Priority]**.

   同じ優先度の 2 つの税務処理基準が適用される場合、税金が追加されます。 優先度の異なる 2 つの税金が適用される場合、税金は合計されます。

1. 注文の小計に基づいて税金を計算する場合は、 **[!UICONTROL Calculate off Subtotal Only]** チェックボックス。

1. の場合 **[!UICONTROL Sort Order]**&#x200B;を入力し、この税務処理基準の順序を示す番号を他のユーザーとともにリスト表示します。

1. 完了したら、 **[!UICONTROL Save Rule]**.

## 通貨および税ルールのデモ

次のビデオを視聴して、通貨と税金ルールの管理について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
