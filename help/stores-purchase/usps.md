---
title: 米国郵政公社（USPS）
description: ストアの配送業者としての USPS の設定方法を説明します。
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 米国郵政公社（USPS）

米国郵便サービスは、陸路および空路による国内外の輸送サービスを提供する、米国政府の独立した郵便サービスです。

## 手順 1:USPS 出荷アカウントを開く

を開く [USPS Web ツール][1] アカウント。 登録プロセスが完了すると、ユーザー ID と USPS テスト・サーバへの URL が表示されます。

を開くこともできます [USPS Web ツール][1] アカウント。 登録プロセスが完了すると、ユーザー ID と USPS テスト・サーバへの URL が表示されます。 USPS Web Tools の詳細については、 [技術ドキュメント][2].

## 手順 2：ストアの USP を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Delivery Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL USPS]** セクション。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、説明に従って次の設定を変更します。

1. を設定 **[!UICONTROL Enabled for Checkout]** 対象： `Yes`.

1. 必要に応じて、を入力します **[!UICONTROL Gateway URL]** usps の配送料にアクセスする方法

   >[!IMPORTANT]
   >
   >2021 年 6 月 24 日（PT）より、USPS Web Tools は、保護されていないすべての HTTP エンドポイントのサポートを削除します。 この変更後、保護されていない HTTP エンドポイントに対するすべての Web ツール API リクエストが失敗します。 次のことを確認します **[!UICONTROL Gateway URL]** は、セキュア HTTPS エンドポイントを使用します。

   このフィールドはデフォルトでプリセットされており、通常は変更する必要はありません。

1. を入力 **[!UICONTROL Title]** （チェックアウト時に表示されるこの配送方法に対して）。

1. を入力 **[!UICONTROL User ID]** および **[!UICONTROL Password]** （USPS アカウント用）

1. を設定 **[!UICONTROL Mode]** を次のいずれかに変更します。

   - `Development` - テスト環境で USPS を実行します。 開発環境で USPS を実行したら、必ず後で戻ってモードをに設定してください。 `Live`.
   - `Live`  – 実稼動環境で USPS を実行します。

## 手順 3：パッケージの説明の入力

1. 複数のパッケージとして送信された場合の注文の管理方法を決定するには、を設定します **[!UICONTROL Packages Request Type]** を次のいずれかに変更します。

   - `Divide to Equal Weight`  – （1 件のリクエスト）複数のパッケージは、同じ重さでパッケージが割られている場合、1 件のリクエストとして送信できます。
   - `Use Origin Weight` - （複数のリクエスト）配送元重量を配送料の計算の基礎として使用する場合、複数のパッケージを別々のリクエストとして送信する必要があります。

1. を設定 **[!UICONTROL Container]** 通常、店舗で注文した製品を出荷するために使用される梱包のタイプ。

1. を **[!UICONTROL Size]** ストアから出荷された一般的なパッケージの。

1. を設定 **[!UICONTROL Machinable]** を次のいずれかに変更します。

   - `Yes`  – 通常のパッケージをマシンで処理できる場合。
   - `No`  – 通常のパッケージを手動で処理する必要がある場合。

1. を入力 **[!UICONTROL Maximum Package Weight]** 通信事業者の要件に応じて調整します。

   ![USPS パッケージ設定](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 手順 4：手数料の設定

手数料は任意で、DHL の送料に加算される追加料金として表示されます。 手数料を含める場合は、次の操作を行います。

1. を設定 **[!UICONTROL Calculate Handling Fee]** 次のいずれかの方法を使用します。

   - `Fixed`
   - `Percent`

1. 手数料の適用方法を決定するには、を設定します **[!UICONTROL Handling Applied]** を次のいずれかに変更します。

   - `Per Order`
   - `Per Package`

1. 金額を入力 **[!UICONTROL Handling Fee]** 請求される。

   パーセンテージを入力するには、小数点形式を使用します。 例えば、 `0.25` 25% の場合。

   ![USPS 手数料](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 手順 5：許可される方法と適用可能な国を指定

1. の場合 **[!UICONTROL Allowed Methods]**&#x200B;を選択します。顧客が使用できる各 USPS 配送方法を選択します。

   メソッドは、チェックアウト時に USPS の下に表示されます。 複数の方法を選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

1. を指定する場合 [送料無料](shipping-free.md) オプションから USPS に移動し、送料無料オプションを設定します。

   - を設定 **[!UICONTROL Free Method]** を送料無料に使用する方法に変更します。 USPS 経由で送料無料を提供しない場合は、次を選択します `None`.

   - USPS で送料無料の注文に該当する最小注文額を要求するには、を設定します **[!UICONTROL Enable Free Shipping Threshold]** 対象： `Enable`. 次に、で最小値を入力します **[!UICONTROL Free Shipping Amount Threshold]**.

1. 必要に応じて、 **[!UICONTROL Displayed Error Message]**.

   このテキスト ボックスには既定のメッセージがあらかじめ設定されていますが、USPS が使用できなくなったときに表示する別のメッセージを入力できます。

   ![USPS で許可されたメソッド](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Ship to Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたこの配信方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _特定の国に出荷_ リストが表示されます。 リストで、この配信方法を使用できる国を選択します。

   ![USPS 対象国](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Show Method if Not Applicable]** を次のいずれかに変更します。

   - `Yes` - チェックアウト時に利用可能なすべての USPS 配送方法を一覧表示します（配送に適用されない方法を含む）。
   - `No`  – 出荷に適用可能な USPS 出荷方法のみをリストします。

1. ストアから作成された USPS 出荷の詳細を記録したログ ファイルを作成するには、次のように設定します **[!UICONTROL Debug]** 対象： `Yes`.

1. の場合 **[!UICONTROL Sort Order]**：数字を入力して、チェックアウト時に他の配信方法と共にリストされたときに USPS が表示されるシーケンスを決定します。

   `0` =最初、 `1` =秒、 `2` = 3 番目、以下同様です。

1. クリック **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
