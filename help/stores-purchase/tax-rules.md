---
title: 税ルール
description: 製品区分、顧客区分および税率を使用して税ルールを定義する方法を説明します。
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
TQID: https://experienceleague.adobe.com/ik-dbYrFRZQ9EvgjFCx6pv5WBnPtk6AHBe2oB4GPn8I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 439
ht-degree: 0%

---

# 税ルール

税ルールには、商品クラス、顧客クラス、税率の組み合わせが組み込まれています。 各顧客には顧客クラスが、各製品には製品クラスが割り当てられます。 Commerceは、お客様のショッピングカートを分析し、お客様や商品クラス、地域に応じて適切な税金を計算します。 地域は、顧客の配送先住所、請求先住所、配送元に基づいています。

>[!NOTE]
>
>多数の税率を定義する必要がある場合は、それらを読み込むことでプロセスを簡素化できます。

![税ルール &#x200B;](./assets/tax-rules.png){width="600" zoomable="yes"}

## 手順1：税ルール情報の入力

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add New Tax Rule]**」をクリックします。

1. _税ルール情報_&#x200B;で、新しいルールの&#x200B;**[!UICONTROL Name]**&#x200B;を入力します。

   ![税ルール情報](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. ルールに適用される&#x200B;**[!UICONTROL Tax Rate]**&#x200B;を選択します。

   既存の税率を編集するには、次の操作を行います。

   - 税率にカーソルを合わせ、_編集_ ![鉛筆アイコン &#x200B;](../assets/icon-edit-pencil.png) アイコンをクリックします。

   - 必要に応じてフォームを更新し、**[!UICONTROL Save]**&#x200B;をクリックします。

1. 税率を入力するには、次のいずれかの方法を使用します。

### 方法1：税率を手動で入力する

1. **[!UICONTROL Add New Tax Rate]**&#x200B;をクリックします。

1. 必要に応じてフォームに記入してください（[税域と税率](tax-zones-rates.md)を参照）。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   ![新しい税率](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### 方法2：輸入税率

1. ページの下部にあるセクションまでスクロールします。

1. 税率を読み込むには、次の操作を行います。

   - 「**[!UICONTROL Choose File]**」をクリックし、読み込む税率を含むCSV ファイルに移動します。

   - **[!UICONTROL Import Tax Rates]**&#x200B;をクリックします。

1. 税率をエクスポートするには、**[!UICONTROL Export Tax Rates]**&#x200B;をクリックします（[税率のインポートとエクスポート &#x200B;](../systems/data-transfer-tax-rates.md)を参照）。

![税率の読み込み/書き出し](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## 手順2：追加の設定を完了

1. セクションを開くには、**[!UICONTROL Additional Settings]**&#x200B;をクリックします。

   ![税ルールの追加設定](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. ルールが適用される&#x200B;**[!UICONTROL Customer Tax Class]**&#x200B;を選択します。

   - 顧客税区分を編集するには、_編集_ ![鉛筆アイコン &#x200B;](../assets/icon-edit-pencil.png) アイコンをクリックし、必要に応じてフォームを更新して、**[!UICONTROL Save]**&#x200B;をクリックします。

   - 税区分を作成するには、**[!UICONTROL Add New Tax Class]**&#x200B;をクリックし、必要に応じてフォームに記入し、**[!UICONTROL Save]**&#x200B;をクリックします。

1. ルールが適用される&#x200B;**[!UICONTROL Product Tax Class]**&#x200B;を選択します。

   - 製品税区分を編集するには、_編集_ ![鉛筆アイコン &#x200B;](../assets/icon-edit-pencil.png) アイコンをクリックし、必要に応じてフォームを更新して、**[!UICONTROL Save]**&#x200B;をクリックします。

   - 税区分を作成するには、**[!UICONTROL Add New Tax Class]**&#x200B;をクリックし、必要に応じてフォームに記入し、**[!UICONTROL Save]**&#x200B;をクリックします。

1. 複数の税が適用される場合は、この税の優先度を&#x200B;**[!UICONTROL Priority]**&#x200B;に示す数値を入力します。

   同じ優先度を持つ2つの税制が適用される場合、税金が追加されます。 優先度の設定が異なる2つの税金が適用される場合、税金は配合されます。

1. 注文の小計に基づいて税金を計算する場合は、「**[!UICONTROL Calculate off Subtotal Only]**」チェックボックスを選択します。

1. 「**[!UICONTROL Sort Order]**」に、他の人と共に表示されたときに、この税ルールの順序を示す番号を入力します。

1. 完了したら、**[!UICONTROL Save Rule]**&#x200B;をクリックします。

## 通貨と税ルールのデモ

次のビデオを見て、通貨と税ルールの管理について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12&learn=on)
