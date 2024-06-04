---
title: チェックアウト時のアドレス検索
description: ストアのチェックアウト時に住所の検索を含める方法を説明します。
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# チェックアウト時のアドレス検索

{{ee-feature}}

顧客のアドレス帳には、保存されたアドレスや情報が多数含まれている場合があります。特に、通常の再訪問者や、複数の注文や発送場所を入力する企業の場合に顕著です。 多数のアドレスを表示すると、チェックアウトの読み込みと処理が大幅に遅くなり、買い物に否定的なエクスペリエンスになる可能性があります。 チェックアウトの応答性を高めるには、サイトのアドレス検索をアクティブにして設定することをお勧めします。

>[!NOTE]
>
>アドレス検索は、デフォルトでは有効になっていません。 この機能を設定して、サイトに機能を組み込むことができます。

この機能が有効になっていて、顧客の保存アドレス数が設定されている制限を満たしているか超えている場合、 _送料_ および _レビューと支払い_ ステップには 1 つのアドレスのみ表示されます（デフォルト）。 顧客は、次のボタンをクリックして、選択したアドレスを変更できます。 **住所の変更** 次に、市区町村、都道府県、番地または郵便番号で正しい住所を検索します。 この機能は、ギフトレジストリチェックアウトのアドレス選択もサポートします。

![保存された配送先住所が表示されたチェックアウト](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

顧客にデフォルトの配送先住所がない場合、 _送料_ ページ表示 _アドレスが選択されていません_. この場合、顧客は次の操作を行う必要があります。 **住所の変更** 保存したアドレスを選択するか、 **新しいアドレス** チェックアウトを進める前に住所を追加して選択します。 顧客にデフォルトの請求先住所がない場合、 _レビューと支払い_ ページには、配送用に選択した住所が _住所の変更_ オプション。

![アドレスが選択されていないメッセージのチェックアウト](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## 引用符で囲まれたアドレス検索

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B でのみ使用可能）

また、住所検索を有効にすると、顧客の保存済み住所の数が設定された制限を満たしているか、超えている見積もりから作成された注文のチェックアウトにも影響します。 見積もりが完了し、顧客がチェックアウトに進むと、選択した配送先住所のみが表示されます。 ページには、配送先住所がロックされていて、見積書でのみ変更できるというメッセージも表示されます。

![見積書に対してロックされた配送先住所](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## アドレス検索を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Checkout]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Checkout Options]** セクション。

   ![設定 – チェックアウトオプション](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   これらの各設定について詳しくは、を参照してください。 [チェックアウトオプション](../configuration-reference/sales/checkout.md#checkout-options) が含まれる _設定リファレンスガイド_.

1. を設定 **[!UICONTROL Enable Address Search]** 対象： `Yes`.

1. アドレス検索機能を含めるしきい値を指定するには、 **[!UICONTROL Number of Customer Addresses Limit]** オプション。

   必要に応じて、 **[!UICONTROL Use system value]** この変更を行うチェックボックス。

   顧客の保存済みアドレスの数がこの制限を満たしているか、超えている場合、ページにはデフォルトのアドレス（顧客にアドレスがある場合）または _アドレスが選択されていません_ （を使用） _住所の変更_ オプション。 デフォルトの制限はです。 `10`.

1. クリック **[!UICONTROL Save Config]**.
