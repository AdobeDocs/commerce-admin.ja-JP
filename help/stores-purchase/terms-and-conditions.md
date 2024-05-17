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

手動の場合 _利用条件_ 機能が有効になっている場合は、購入が確定する前に、お客様は販売条件に同意する必要があります。 販売条件には、通常、B2C または B2B サイトに関して法律で要求される可能性のある開示情報が含まれており、購入者および販売者の権利の概要が説明されています。 利用条件メッセージは、支払い情報の後、支払い情報の直前に表示されます _注文する_ ボタン。

![チェックアウト時の利用条件](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## 手順 1：チェックアウトに関する利用条件を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Checkout]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Checkout Options]** セクション。

   ![チェックアウトオプション](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. を確認します。 **[!UICONTROL Enable Onepage Checkout]** はに設定されています。 `Yes`.

1. を設定 **[!UICONTROL Enable Terms and Conditions]** 対象： `Yes`.

1. クリック **[!UICONTROL Save Config]**.

## 手順 2：独自の利用条件情報を追加する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![利用条件グリッド](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. 右上隅のをクリックします。 **[!UICONTROL Add New Condition]**.

1. を入力 **[!UICONTROL Condition Name]** 内部参照用。

   ![新規条件](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Status]** 対象： `Enabled`.

1. を設定 **[!UICONTROL Applied]** を次のいずれかに変更します。

   - `Automatically`  – 条件はチェックアウト時に自動的に承認されます。
   - `Manually`  – お客様は、注文を行う際に、手動で条件を受け入れる必要があります。

1. を設定 **[!UICONTROL Show Content as]** を次のいずれかに変更します。

   - `Text`  – 利用条件コンテンツを書式なしのテキストとして表示します。
   - `HTML` - フォーマット可能なHTMLとしてコンテンツを表示します。

1. 各を選択 **[!UICONTROL Store View]** これらの利用条件を使用する場所。

1. 下にスクロールして、表示する情報を入力します。

   - を入力 **[!UICONTROL Checkbox Text]** 利用規約リンクのテキストとして使用されます。 例： `I understand and accept the terms and conditions of the sale`.

   - が含まれる **[!UICONTROL Content]** ボックスに、販売条件の全文を入力します。

1. （任意） **[!UICONTROL Content Height (css)]** チェックアウト時に利用条件ステートメントが表示されるテキストボックスの高さをピクセル単位で指定します。

   たとえば、96 dpi のディスプレイでテキスト ボックスの高さを 1 インチにするには、次のように入力します `96`. コンテンツがボックスの高さを超えると、スクロールバーが表示されます。

1. クリック **[!UICONTROL Save Condition]**.
