---
title: 税務処理基準
description: 製品区分、顧客区分および税率を使用して税務処理基準を定義する方法を説明します。
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# 税務処理基準

税務処理基準には、製品区分、顧客区分および税率の組合せが組み込まれます。 各顧客は顧客クラスに割り当てられ、各製品は製品クラスに割り当てられます。 Commerceは、各顧客の買い物かごを分析し、顧客クラス、商品クラスおよびリージョンに従って適切な税金を計算します。 この地域は、顧客の発送先住所、請求先住所、または発送元に基づいています。

>[!NOTE]
>
>多数の税率を定義する必要がある場合は、税率をインポートしてプロセスを簡略化できます。

![&#x200B; 税務ルール &#x200B;](./assets/tax-rules.png){width="600" zoomable="yes"}

## 手順 1：税務処理基準情報の完了

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Rules]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add New Tax Rule]**」をクリックします。

1. 「_税務処理基準情報_」に、新規処理基準の **[!UICONTROL Name]** を入力します。

   ![&#x200B; 税制上の措置情報 &#x200B;](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. ルールに適用する **[!UICONTROL Tax Rate]** を選択します。

   既存の税率を編集するには、次の手順を実行します。

   - 税率の上にマウスポインターを置き、_編集_![&#x200B; 鉛筆アイコン &#x200B;](../assets/icon-edit-pencil.png) アイコンをクリックします。

   - 必要に応じてフォームを更新し、「**[!UICONTROL Save]**」をクリックします。

1. 税率を入力するには、次のいずれかの方法を使用します。

### 方法 1：税率の手動入力

1. 「**[!UICONTROL Add New Tax Rate]**」をクリックします。

1. 必要に応じてフォームに入力します（[&#x200B; 税ゾーンと税率 &#x200B;](tax-zones-rates.md) を参照）。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   ![&#x200B; 新税率 &#x200B;](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### 方法 2：税率のインポート

1. ページの下部のセクションまで下にスクロールします。

1. 税率をインポートするには、次の手順を実行します。

   - 「**[!UICONTROL Choose File]**」をクリックして、インポートする税率を含む CSV ファイルに移動します。

   - 「**[!UICONTROL Import Tax Rates]**」をクリックします。

1. 税率をエクスポートするには、「**[!UICONTROL Export Tax Rates]**」をクリックします（[&#x200B; 税率のインポート/エクスポート &#x200B;](../systems/data-transfer-tax-rates.md) を参照）。

![&#x200B; 輸出入税率 &#x200B;](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## 手順 2：追加設定を完了する

1. セクションを開くには、「**[!UICONTROL Additional Settings]**」をクリックします。

   ![&#x200B; 税務処理基準の追加設定 &#x200B;](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. ルールを適用する **[!UICONTROL Customer Tax Class]** を選択します。

   - 顧客税区分を編集するには、「_編集_![&#x200B; 鉛筆アイコン &#x200B;](../assets/icon-edit-pencil.png) アイコンをクリックし、必要に応じてフォームを更新して「**[!UICONTROL Save]**」をクリックします。

   - 税金区分を作成するには、「**[!UICONTROL Add New Tax Class]**」をクリックし、必要に応じてフォームに入力して「**[!UICONTROL Save]**」をクリックします。

1. ルールを適用する **[!UICONTROL Product Tax Class]** を選択します。

   - 製品税クラスを編集するには、_編集_![&#x200B; 鉛筆アイコン &#x200B;](../assets/icon-edit-pencil.png) アイコンをクリックし、必要に応じてフォームを更新して、「**[!UICONTROL Save]**」をクリックします。

   - 税金区分を作成するには、「**[!UICONTROL Add New Tax Class]**」をクリックし、必要に応じてフォームに入力して「**[!UICONTROL Save]**」をクリックします。

1. 複数の税金が適用される場合は、**[!UICONTROL Priority]** の税金の優先度を示す数値を入力します。

   同じ優先度の 2 つの税務処理基準が適用される場合、税金が追加されます。 優先度の異なる 2 つの税金が適用される場合、税金は合計されます。

1. 注文の小計に基づいて税金を計算する場合は、「**[!UICONTROL Calculate off Subtotal Only]**」チェックボックスを選択します。

1. **[!UICONTROL Sort Order]**：この税務処理基準の順序を示す番号を入力します。他の税務処理基準と一緒にリストされます。

1. 完了したら、「**[!UICONTROL Save Rule]**」をクリックします。

## 通貨および税ルールのデモ

次のビデオを視聴して、通貨と税金ルールの管理について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/3410213/?quality=12&learn=on&captions=jpn)
