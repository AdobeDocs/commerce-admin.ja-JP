---
title: 米国郵政公社 (USPS)
description: USPS を店舗の配送業者として設定する方法を説明します。
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 米国郵政公社 (USPS)

米国郵政公社は、米国政府の独立した郵便局で、陸上及び航空機による国内及び国際海運サービスを提供しています。

## 手順 1: USPS の配送先アカウントを開く

を開きます。 [USPS Web ツール][1] アカウント。 登録プロセスが完了したら、ユーザー ID と USPS テストサーバーへの URL を受け取ります。

また、 [USPS Web ツール][1] アカウント。 登録プロセスが完了したら、ユーザー ID と USPS テストサーバーへの URL を受け取ります。 USPS Web ツールの詳細については、 [技術ドキュメント][2].

## 手順 2：ストアの USPS を有効にする

{{beta2-updates}}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Delivery Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL USPS]** 」セクションに入力します。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、次の設定を変更します。

1. 設定 **[!UICONTROL Enabled for Checkout]** から `Yes`.

1. 必要に応じて、 **[!UICONTROL Gateway URL]** USPS の送料にアクセスする。

   >[!IMPORTANT]
   >
   >2021 年 6 月 24 日から、USPS Web Tools は、セキュリティで保護されていないすべての HTTP エンドポイントのサポートを削除します。 この変更後、セキュリティで保護されていない HTTP エンドポイントに対するすべての Web ツール API リクエストが失敗します。 次の項目を確認します。 **[!UICONTROL Gateway URL]** は、セキュリティで保護された HTTPS エンドポイントを使用します。

   このフィールドはデフォルトで事前設定されており、通常は変更する必要はありません。

1. を入力します。 **[!UICONTROL Title]** チェックアウト時に表示されるこの発送方法。

1. 次を入力します。 **[!UICONTROL User ID]** および **[!UICONTROL Password]** USPS アカウントの

1. 設定 **[!UICONTROL Mode]** を次のいずれかに変更します。

   - `Development`  — テスト環境で USPS を実行します。 開発環境で USPS を実行した後、必ず後で戻り、モードをに設定します。 `Live`.
   - `Live`  — 実稼動環境で USPS を実行します。

## 手順 3：パッケージの説明を入力します。

1. 複数のパッケージとして送信された場合の順序の管理方法を決定するには、 **[!UICONTROL Packages Request Type]** を次のいずれかに変更します。

   - `Divide to Equal Weight` - （1 つの要求）複数のパッケージの出荷は、同じ重みで分けた場合、1 つの要求として提出できます。
   - `Use Origin Weight` - （複数のリクエスト）送料の計算の基礎として接触チャネルの重み付けを使用する場合は、複数のパッケージを個別のリクエストとして送信する必要があります。

1. 設定 **[!UICONTROL Container]** 商品を出荷する際に通常使用される包装の種類に対して。

1. を設定します。 **[!UICONTROL Size]** お客様の店から出荷される標準的なパッケージの

1. 設定 **[!UICONTROL Machinable]** を次のいずれかに変更します。

   - `Yes`  — 通常のパッケージを 1 台のマシンで処理できる場合。
   - `No`  — 通常のパッケージを手動で処理する必要がある場合。

1. 次を入力します。 **[!UICONTROL Maximum Package Weight]** 運送業者の要件に従って。

   ![USPS パッケージ設定](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 手順 4：処理料金の設定

手数料はオプションで、DHL の送料に追加される追加料金として表示されます。 手数料を含める場合は、次の手順を実行します。

1. 設定 **[!UICONTROL Calculate Handling Fee]** を次のいずれかのメソッドに追加します。

   - `Fixed`
   - `Percent`

1. 処理費の適用方法を決定するには、 **[!UICONTROL Handling Applied]** を次のいずれかに変更します。

   - `Per Order`
   - `Per Package`

1. 金額を入力 **[!UICONTROL Handling Fee]** 請求される。

   パーセンテージを入力するには、10 進形式を使用します。 例えば、 `0.25` 25%です。

   ![USPS 取扱手数料](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 手順 5：許可された方法と適用可能な国を指定する

1. の場合 **[!UICONTROL Allowed Methods]**、顧客が利用できる各 USPS 発送方法を選択します。

   このメソッドは、チェックアウト時に USPS の下に表示されます。 複数の方法を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. 次を指定する場合、 [送料無料](shipping-free.md) オプションを USPS 経由で、無料配送オプションを設定します。

   - 設定 **[!UICONTROL Free Method]** 無料配送に使用する方法に。 USPS を通じて送料無料を提供したくない場合は、 `None`.

   - USPS での無料配送に適合する最小注文額を要求するには、 **[!UICONTROL Enable Free Shipping Threshold]** から `Enable`. 次に、最小値を **[!UICONTROL Free Shipping Amount Threshold]**.

1. 必要に応じて、 **[!UICONTROL Displayed Error Message]**.

   このテキストボックスにはデフォルトのメッセージがあらかじめ設定されていますが、USPS が利用できなくなった場合に表示する別のメッセージを入力できます。

   ![USPS で許可されるメソッド](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Ship to Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この配信方法を使用できます。
   - `Specific Countries`  — このオプションを選択すると、 _特定の国に出荷_ リストが表示されます。 この配信方法を使用できる国をリストから選択します。

   ![USPS 適用国](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Show Method if Not Applicable]** を次のいずれかに変更します。

   - `Yes`  — チェックアウト時に使用可能なすべての USPS 発送方法をリストします。これには、出荷に適用されない方法も含まれます。
   - `No`  — 出荷に適用できる USPS 出荷方法のみをリストします。

1. ストアで行われた USPS 出荷の詳細を含むログファイルを作成するには、 **[!UICONTROL Debug]** から `Yes`.

1. の場合 **[!UICONTROL Sort Order]**&#x200B;に値を入力して、チェックアウト時に USPS が他の配信方法と共に表示される際の順序を指定します。

   `0` =最初 `1` =秒 `2` = 3 番目、など。

1. クリック **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
