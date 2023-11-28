---
title: チェックアウト合計の並べ替え順
description: 表示されるチェックアウト合計と、注文概要でのチェックアウト合計の並べ替え順を設定する方法について説明します。
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# チェックアウト合計の並べ替え順

注文のレビュー中に、合計が注文の下部に表示され、割引、送料、店舗クレジット、税の調整が行われます。 各項目の順序によって計算の順序が決まり、各項目に割り当てられた数値で設定されます。 たとえば、[ 小計 ] はセクションの最初の項目で、10 の値が割り当てられます。 「総計」が最後に表示され、値 100 が割り当てられます。 「合計」セクションのその他すべての項目には、これらの値の間に値が割り当てられます。

![注文の概要には、チェックアウトの合計が表示されます](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_チェックアウト合計の並べ替え順を設定するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** 「 」セクションで「 」を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Checkout Totals Sort Order]** 」セクションに入力します。

   ![並べ替え順を決定するためのチェックアウト合計オプション番号が付けられました](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、 [チェックアウト合計の並べ替え順](../configuration-reference/sales/sales.md#checkout-totals-sort-order) （内） _設定リファレンスガイド_.

1. 設定が特定のストア表示の場合、 [ストア表示を選択](../configuration-reference/scope-change.md#set-the-scope) 設定が適用される場所

   プロンプトが表示されたら、「 **[!UICONTROL OK]** をクリックして続行します。

1. 並べ替え順を _合計_ 「 」セクションで、各項目に割り当てる番号を変更します。

   値が低いほど、リスト内での配置が早くなります。 デフォルト設定では、小計 (`10`) は最初の総計 (`100`) は最後のです。

   必要に応じて、 **[!UICONTROL Use system value]** チェックボックスをオンにして、これらの変更を完了します。

1. クリック **[!UICONTROL Save Config]**.
