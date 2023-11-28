---
title: チェックアウトに関する利用条件
description: ストアに設定できる利用条件機能について説明します。
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# チェックアウトに関する利用条件

手動の場合 _利用条件_ 機能を有効にすると、購入が確定される前に、お客様は販売の利用条件に同意する必要があります。 販売の利用条件には、通常、B2C または B2B サイトに関して法律で必要となる可能性のある開示情報が含まれ、購入者および販売者の権利の概要が示されます。 利用条件メッセージは、支払い情報の直後、 _発注_ 」ボタンをクリックします。

![チェックアウト時の利用条件](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## 手順 1：チェックアウトの利用条件を有効にします

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Checkout]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Checkout Options]** 」セクションに入力します。

   ![チェックアウトオプション](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. を確認します。 **[!UICONTROL Enable Onepage Checkout]** が `Yes`.

1. 設定 **[!UICONTROL Enable Terms and Conditions]** から `Yes`.

1. クリック **[!UICONTROL Save Config]**.

## 手順 2：独自の利用条件情報を追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![利用条件グリッド](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. 右上隅で、 **[!UICONTROL Add New Condition]**.

1. 次を入力します。 **[!UICONTROL Condition Name]** 内部参照用。

   ![新しい条件](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Status]** から `Enabled`.

1. 設定 **[!UICONTROL Applied]** を次のいずれかに変更します。

   - `Automatically`  — 条件はチェックアウト時に自動的に受け入れられます。
   - `Manually` ：お客様は、注文を行う際に、条件を手動で承認する必要があります。

1. 設定 **[!UICONTROL Show Content as]** を次のいずれかに変更します。

   - `Text`  — 利用条件の内容を書式なしのテキストとして表示します。
   - `HTML`  — コンテンツをHTMLとして表示します（書式設定可能）。

1. それぞれ選択 **[!UICONTROL Store View]** を使用する場合。

1. 下にスクロールして、表示する情報を入力します。

   - 次を入力します。 **[!UICONTROL Checkbox Text]** を利用して、利用条件リンクのテキストとして使用できます。 例： `I understand and accept the terms and conditions of the sale`.

   - Adobe Analytics の **[!UICONTROL Content]** ボックスに、販売条件の全文を入力します。

1. （オプション） **[!UICONTROL Content Height (css)]** チェックアウト時に利用条件文が表示されるテキストボックスの高さをピクセル単位で指定します。

   例えば、テキストボックスの高さを 96 dpi ディスプレイで 1 インチにするには、次のように入力します。 `96`. コンテンツがボックスの高さを超える場合は、スクロールバーが表示されます。

1. クリック **[!UICONTROL Save Condition]**.
