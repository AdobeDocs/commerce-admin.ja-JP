---
title: チェックアウトの利用条件
description: ストアで設定できる利用規約機能について説明します。
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# チェックアウトの利用条件

手動 _利用規約_ 機能が有効になっている場合、お客様は購入が確定する前に販売条件に同意する必要があります。 販売条件には、通常、B2C または B2B サイトに関して法律で要求される可能性のある開示情報が含まれており、購入者および販売者の権利の概要が説明されています。 利用規約メッセージは、支払い情報の後、「注文する _ボタンの直前に表示さ_ ます。

![&#x200B; チェックアウト時の利用条件 &#x200B;](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## 手順 1：チェックアウトに関する利用条件を有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Checkout]**」を選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Checkout Options]**」セクションを展開します。

   ![&#x200B; チェックアウトオプション &#x200B;](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Onepage Checkout]** が `Yes` に設定されていることを確認します。

1. **[!UICONTROL Enable Terms and Conditions]** を `Yes` に設定します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 手順 2：独自の利用条件情報を追加する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Terms and Conditions]**&#x200B;に移動します。

   ![&#x200B; 利用条件グリッド &#x200B;](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. 右上隅の「**[!UICONTROL Add New Condition]**」をクリックします。

1. 内部参照の **[!UICONTROL Condition Name]** を入力します。

   ![&#x200B; 新規条件 &#x200B;](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. **[!UICONTROL Status]** を `Enabled` に設定します。

1. **[!UICONTROL Applied]** を次のいずれかに設定します。

   - `Automatically` – 条件はチェックアウト時に自動的に承認されます。
   - `Manually` – お客様は、注文を行う際に手動で条件を受け入れる必要があります。

1. **[!UICONTROL Show Content as]** を次のいずれかに設定します。

   - `Text` – 利用条件コンテンツを書式なしのテキストとして表示します。
   - `HTML` - フォーマット可能なHTMLとしてコンテンツを表示します。

1. これらの利用条件を使用する各 **[!UICONTROL Store View]** を選択します。

1. 下にスクロールして、表示する情報を入力します。

   - 利用条件リンクのテキストとして使用する **[!UICONTROL Checkbox Text]** を入力します。 例：`I understand and accept the terms and conditions of the sale`。

   - **[!UICONTROL Content]** のボックスに、販売条件の全文を入力します。

1. （オプション） **[!UICONTROL Content Height (css)]** をピクセル単位で入力して、チェックアウト時に利用条件ステートメントが表示されるテキストボックスの高さを指定します。

   たとえば、96 dpi のディスプレイでテキスト ボックスの高さを 1 インチにするには、`96` と入力します。 コンテンツがボックスの高さを超えると、スクロールバーが表示されます。

1. 「**[!UICONTROL Save Condition]**」をクリックします。
