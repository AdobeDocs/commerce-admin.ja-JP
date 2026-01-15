---
title: 発送設定
description: ストアの発送元と配送ポリシーを定義する配送設定の設定方法を説明します。
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# 発送設定

出荷構成では、すべての出荷の原産地点、出荷方針、および複数の所在地への出荷処理が設定されます。

## 原点

出荷元は、店舗または倉庫から行われた出荷の請求を計算するために使用され、また販売された製品の税率を決定します。 [EU 税 &#x200B;](international-tax-guidelines.md#eu-tax-configuration) を計算する場合は、各ストア表示の [&#x200B; デフォルトの税宛先計算 &#x200B;](../configuration-reference/sales/tax.md) が出荷設定の起源に対応していることを確認してください。

![&#x200B; 接触チャネル &#x200B;](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Shipping Settings]**」を選択します。

1. ![&#x200B; のセクションの &#x200B;](../assets/icon-display-expand.png) 展開セレクター **[!UICONTROL Origin]** を展開し、以下を完了します。

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] （必要に応じて 2 行目）

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 配送ポリシー

配送ポリシーでは、会社の配送に関するビジネスルールとガイドラインを説明する必要があります。 例えば、送料無料をトリガーとする価格ルールがある場合、送料ポリシーの条件を説明できます。

![&#x200B; チェックアウト時の送料 &#x200B;](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

チェックアウト時に配送ポリシーを表示するには、設定の配送ポリシーパラメーターを入力します。 このテキストは、お客様がチェックアウト時に _配送ポリシーを参照_ をクリックすると表示されます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Shipping Settings]**」を選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Shipping Policy Parameters]**」セクションを展開します。

1. **[!UICONTROL Apply Custom Shipping Policy]** を `Yes` に設定します。

1. テキストボックスに **[!UICONTROL Shipping Policy]** を貼り付けるか入力します。

   >[!NOTE]
   >
   >ワードプロセッサーを使用してテキストを作成する場合は、ドキュメントを.txt ファイルとして保存して、テキストから制御文字を削除してください。 次に、テキストをコピーして「出荷ポリシー」テキストボックスに貼り付けます。

   ![&#x200B; 配送ポリシーのパラメーター &#x200B;](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 複数のアドレス

複数の住所配送オプションを使用すると、お客様はチェックアウト時に注文を複数の住所に発送し、注文を発送できる最大住所数を決定できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Multishipping Settings]**」を選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Options]**」セクションを展開します。

   ![&#x200B; 複数の住所を使用する配送オプション &#x200B;](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Allow Shipping to Multiple Addresses]** を `Yes` に設定します。

1. **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]** を入力します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B）配送先住所が複数ある注文の場合、[&#x200B; 対顧客払い &#x200B;](../b2b/enable-basic-features.md#configure-payment-on-account) の支払い方法は、有効になっている場合でも、チェックアウト時には使用できません。

## E メール出荷トラッキング URL

[!BADGE SaaS のみ &#x200B;]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクトにのみ適用されます（Adobeで管理される SaaS インフラストラクチャ）。"}

[!BADGE &#x200B; サンドボックス &#x200B;]{type=Caution tooltip="リストされた項目は、現在、サンドボックス環境でのみ使用できます。 Adobeでは、最初にサンドボックス環境で新しいリリースを使用できるようにして、リリースが実稼動環境で使用できるようになる前に、今後の変更をテストするための時間を提供します。"}

デフォルトでは、買い物客のメールで送信される出荷トラッキング番号はプレーンテキストです。 カスタムトラッキング URL 機能を有効にすると、これらのトラッキング番号をクリック可能なリンクに変換できます。 この機能を使用すると、様々な配送業者の URL をトラッキングするためのテンプレートを定義できます。 各テンプレートには、トラッキング web サイトの完全な URL と、トラッキング番号のプレースホルダーが含まれます。 Commerceは、メールの実際のトラッキング番号でプレースホルダーを置き換えます。

次の配送業者がサポートされています。

- 米国郵政公社（USPS）
- UPS （統一宅配便）
- フェデラル エクスプレス （FedEx）
- DHL Express （DHL）

カスタムトラッキング URL を有効にする、または編集するには：

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Shipping Settings]**」を選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Shipment Tracking URLs]**」セクションを展開します。

1. **[!UICONTROL Enable Custom Tracking URLs]** を `Yes` に設定します。

1. サポートされる各通信事業者に対して、デフォルトの URL テンプレートが提供されます。 これらの値を変更する必要がある場合は、対応するフィールドに新しい URL テンプレートを入力します。 実際のトラッキング番号のプレースホルダーとして `{{tracking_number}}` を使用します。 例えば、UPS が URL を `https://www.ups.com/newtracker?tracknumber` に変更した場合、新しいトラッキング URL テンプレートは次のようになります。

   ```text
   https://www.ups.com/newtracker?tracknumber={{tracking_number}}
   ```

1. 「**[!UICONTROL Save Config]**」をクリックします。
