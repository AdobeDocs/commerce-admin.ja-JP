---
title: チェックアウト時のアドレス検索
description: ストアのチェックアウト時にアドレス検索を含める方法を説明します。
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# チェックアウト時のアドレス検索

{{ee-feature}}

顧客のアドレス帳には、多くの保存済みの住所や情報が含まれている場合があります。特に、通常の返品顧客や、複数の注文や出荷場所を入力する会社が含まれています。 多数のアドレスを表示すると、チェックアウトの読み込みと処理が大幅に遅くなり、買い物ができなくなる可能性があります。 チェックアウトの応答性を高めるために、サイトのアドレス検索をアクティブ化し、設定することをお勧めします。

>[!NOTE]
>
>アドレス検索は、デフォルトでは有効になっていません。 この機能を設定して、サイトに機能を組み込むことができます。

この機能を有効にし、顧客の保存済みアドレスの数が設定された制限を超える場合、 _送料_ および _レビューと支払い_ ステップには、1 つのアドレスのみが表示されます（デフォルト）。 顧客は、 **住所の変更** そして、市区町村、都道府県、番地、郵便番号で正しい住所を検索します。 この機能は、ギフトレジストリのチェックアウト用の住所の選択もサポートします。

![保存した配送先住所を含むチェックアウトが表示されます](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

顧客がデフォルトの配送先住所を持っていない場合、 _送料_ ページ表示 _アドレスが選択されていません_. この場合、顧客は **住所の変更** 保存されたアドレスを選択するか、 **新しい住所** をクリックしてアドレスを追加し、選択してから、チェックアウトを続行します。 顧客がデフォルトの請求先住所を持っていない場合、 _レビューと支払い_ ページには、配送先として選択した住所と _住所の変更_ オプション。

![アドレスが選択されていないチェックアウト](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## ロックされたアドレスの検索で引用符が使用されます

![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B では、Adobe Commerceでのみ使用可能 )

また、住所の検索を有効にすると、顧客の保存済み住所の数が設定された制限を満たす、または超える見積もりから作成される注文のチェックアウトにも影響します。 見積もりが完了し、顧客がチェックアウトに進むと、選択した配送先住所のみが表示されます。 また、配送先住所がロックされ、見積もりでのみ変更できるというメッセージもページに表示されます。

![見積もり用にロックされた発送先住所](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## アドレス検索を有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Checkout]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Checkout Options]** 」セクションに入力します。

   ![設定 — チェックアウトオプション](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   これらの各設定について詳しくは、 [チェックアウトオプション](../configuration-reference/sales/checkout.md#checkout-options) （内） _設定リファレンスガイド_.

1. 設定 **[!UICONTROL Enable Address Search]** から `Yes`.

1. アドレス検索機能を含めるしきい値を指定するには、 **[!UICONTROL Number of Customer Addresses Limit]** オプション。

   必要に応じて、 **[!UICONTROL Use system value]** チェックボックスをオンにして、この変更を行います。

   顧客の保存済みアドレスの数がこの制限を超える場合、ページにはデフォルトのアドレス（顧客のアドレスがある場合）または _アドレスが選択されていません_ と _住所の変更_ オプション。 デフォルトの制限は次のとおりです。 `10`.

1. クリック **[!UICONTROL Save Config]**.
