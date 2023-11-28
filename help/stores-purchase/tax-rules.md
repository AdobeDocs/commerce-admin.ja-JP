---
title: 税ルール
description: 製品区分、顧客区分および税率を使用して税務処理基準を定義する方法を説明します。
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# 税ルール

税ルールには、製品区分、顧客区分および税率の組み合わせが組み込まれます。 各顧客は顧客クラスに割り当てられ、各製品は製品クラスに割り当てられます。 コマースは、各顧客の買い物かごを分析し、顧客と製品の区分、および地域に基づいて適切な税金を計算します。 地域は、顧客の配送先住所、請求先住所または配送元に基づきます。

>[!NOTE]
>
>多数の税率を定義する必要がある場合は、税率をインポートすることでプロセスを簡略化できます。

![税ルール](./assets/tax-rules.png){width="600" zoomable="yes"}

## 手順 1：税務処理基準情報の入力

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. 右上隅で、 **[!UICONTROL Add New Tax Rule]**.

1. の下 _税務処理基準情報_、 **[!UICONTROL Name]** 新しいルール用。

   ![税務処理基準情報](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL Tax Rate]** ルールに適用される

   既存の税率を編集するには、次の手順を実行します。

   - 税率の上にマウスポインターを置いて、 _編集_ ![鉛筆アイコン](../assets/icon-edit-pencil.png) アイコン。

   - 必要に応じてフォームを更新し、「 **[!UICONTROL Save]**.

1. 税率を入力するには、次のいずれかの方法を使用します。

### 方法 1：税率を手動で入力します。

1. クリック **[!UICONTROL Add New Tax Rate]**.

1. 必要に応じてフォームに入力します ( [税ゾーンと税率](tax-zones-rates.md)) をクリックします。

1. 完了したら、「 **[!UICONTROL Save]**.

   ![新しい税率](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### 方法 2：税率のインポート

1. ページ下部のセクションまで下にスクロールします。

1. 税率をインポートするには、次の手順を実行します。

   - クリック **[!UICONTROL Choose File]** をクリックし、インポートする税率を含む CSV ファイルに移動します。

   - クリック **[!UICONTROL Import Tax Rates]**.

1. 税率をエクスポートするには、 **[!UICONTROL Export Tax Rates]** ( [税率のインポート/エクスポート](../systems/data-transfer-tax-rates.md)) をクリックします。

![税率のインポート/エクスポート](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## 手順 2：追加の設定を完了する

1. セクションを開くには、 **[!UICONTROL Additional Settings]**.

   ![税務処理基準の追加設定](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL Customer Tax Class]** ルールを適用する先にドラッグします。

   - 顧客税区分を編集するには、 _編集_ ![鉛筆アイコン](../assets/icon-edit-pencil.png) アイコンをクリックし、必要に応じてフォームを更新して、 **[!UICONTROL Save]**.

   - 税区分を作成するには、 **[!UICONTROL Add New Tax Class]**&#x200B;必要に応じてフォームに入力し、 **[!UICONTROL Save]**.

1. を選択します。 **[!UICONTROL Product Tax Class]** ルールを適用する先にドラッグします。

   - 製品税区分を編集するには、 _編集_ ![鉛筆アイコン](../assets/icon-edit-pencil.png) アイコンをクリックし、必要に応じてフォームを更新して、 **[!UICONTROL Save]**.

   - 税区分を作成するには、 **[!UICONTROL Add New Tax Class]**&#x200B;必要に応じてフォームに入力し、 **[!UICONTROL Save]**.

1. 複数の税金が適用される場合は、この税金の優先度を示す数値を入力します。 **[!UICONTROL Priority]**.

   同じ優先順位を持つ 2 つの税務処理基準が適用される場合、税金が追加されます。 優先順位の設定が異なる 2 つの税金が適用される場合、税金は複合されます。

1. 注文の小計に基づいて税金を設定する場合は、 **[!UICONTROL Calculate off Subtotal Only]** チェックボックス。

1. の場合 **[!UICONTROL Sort Order]**」に値を入力して、他の値と共にこの税務処理基準の順序を示します。

1. 完了したら、「 **[!UICONTROL Save Rule]**.

## 通貨と税ルールのデモ

通貨と税金ルールの管理については、このビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
