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

[USPS Web ツール ][1] アカウントを開きます。 登録プロセスが完了すると、ユーザー ID と USPS テスト・サーバへの URL が表示されます。

[USPS Web Tools][1] アカウントを開くこともできます。 登録プロセスが完了すると、ユーザー ID と USPS テスト・サーバへの URL が表示されます。 USPS Web Tools の詳細については、それぞれの [ 技術ドキュメント ][2] を参照してください。

## 手順 2：ストアの USP を有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Delivery Methods]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL USPS]**」セクションを展開します。

   >[!NOTE]
   >
   >必要に応じて、まず「**[!UICONTROL Use system value]**」チェックボックスの選択を解除し、説明に従って次の設定を変更します。

1. **[!UICONTROL Enabled for Checkout]** を `Yes` に設定します。

1. 必要に応じて、USPS の配送料にアクセスするための **[!UICONTROL Gateway URL]** を入力します。

   >[!IMPORTANT]
   >
   >2021 年 6 月 24 日（PT）より、USPS Web Tools は、保護されていないすべての HTTP エンドポイントのサポートを削除します。 この変更後、保護されていない HTTP エンドポイントに対するすべての Web ツール API リクエストが失敗します。 **[!UICONTROL Gateway URL]** でセキュアな HTTPS エンドポイントを使用していることを確認します。

   このフィールドはデフォルトでプリセットされており、通常は変更する必要はありません。

1. チェックアウト時に表示されるこの配送方法の **[!UICONTROL Title]** を入力します。

1. USPS アカウントの **[!UICONTROL User ID]** と **[!UICONTROL Password]** を入力します。

1. **[!UICONTROL Mode]** を次のいずれかに設定します。

   - `Development` - テスト環境で USPS を実行します。 開発環境で USPS を実行した後、必ず後で戻ってモードを `Live` に設定してください。
   - `Live`：本番 USPS 環境で USPS を実行します。

## 手順 3：パッケージの説明の入力

1. 複数のパッケージとして送信された場合の注文の管理方法を決定するには、**[!UICONTROL Packages Request Type]** を次のいずれかに設定します。

   - `Divide to Equal Weight` - （1 件のリクエスト）同じ重さでパッケージが分割されている場合、複数のパッケージの出荷を 1 件のリクエストとして送信できます。
   - `Use Origin Weight` - （複数のリクエスト）配送元重量を配送料の計算の基礎として使用する場合は、複数のパッケージを別々のリクエストとして送信する必要があります。

1. 通常、店舗で注文した製品を出荷するために使用されるパッケージのタイプに **[!UICONTROL Container]** を設定します。

1. ストアから出荷された一般的なパッケージの **[!UICONTROL Size]** を設定します。

1. **[!UICONTROL Machinable]** を次のいずれかに設定します。

   - `Yes` – 典型的なパッケージを機械で処理できる場合。
   - `No` – 一般的なパッケージを手動で処理する必要がある場合。

1. 通信事業者の要件に従って **[!UICONTROL Maximum Package Weight]** を入力します。

   ![USPS パッケージ設定 ](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 手順 4：手数料の設定

手数料は任意で、DHL の送料に加算される追加料金として表示されます。 手数料を含める場合は、次の操作を行います。

1. **[!UICONTROL Calculate Handling Fee]** を次のいずれかのメソッドに設定します。

   - `Fixed`
   - `Percent`

1. 手数料の適用方法を決定するには、**[!UICONTROL Handling Applied]** を次のいずれかに設定します。

   - `Per Order`
   - `Per Package`

1. 請求する **[!UICONTROL Handling Fee]** の金額を入力します。

   パーセンテージを入力するには、小数点形式を使用します。 例えば、25% の場合は `0.25` と入力します。

   ![USPS 手数料 ](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 手順 5：許可される方法と適用可能な国を指定

1. **[!UICONTROL Allowed Methods]** しくは、顧客が使用できる各 USPS 配送方法を選択します。

   メソッドは、チェックアウト時に USPS の下に表示されます。 複数の方法を選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

1. USPS 経由で [ 送料無料 ](shipping-free.md) オプションを提供する場合は、送料無料オプションを設定します。

   - 送料無料に使用する方法に **[!UICONTROL Free Method]** を設定します。 USPS 経由で送料無料を提供したくない場合は、`None` を選択します。

   - USPS を使用した送料無料の注文に該当する最小注文額を要求するには、**[!UICONTROL Enable Free Shipping Threshold]** を `Enable` に設定します。 次に、**[!UICONTROL Free Shipping Amount Threshold]** に最小値を入力します。

1. 必要に応じて、**[!UICONTROL Displayed Error Message]** を変更します。

   このテキスト ボックスには既定のメッセージがあらかじめ設定されていますが、USPS が使用できなくなったときに表示する別のメッセージを入力できます。

   ![USPS 許可メソッド ](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. **[!UICONTROL Ship to Applicable Countries]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての [ 国 ](../getting-started/store-details.md#country-options) の顧客がこの配信方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、「_特定の国に発送_ リストが表示されます。 リストで、この配信方法を使用できる国を選択します。

   ![USPS 対象国 ](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. **[!UICONTROL Show Method if Not Applicable]** を次のいずれかに設定します。

   - `Yes` - チェックアウト時に利用可能なすべての USPS 配送方法を一覧表示します（配送に適用されない方法を含む）。
   - `No` – 出荷に適用可能な USPS 出荷方法のみをリストします。

1. ストアから作成された USPS 出荷の詳細を記録したログ ファイルを作成するには、**[!UICONTROL Debug]** を `Yes` に設定します。

1. **[!UICONTROL Sort Order]**：番号を入力して、チェックアウト時に他の配信方法と一緒に表示される USPS の表示順序を決定します。

   `0` = 1 番目、`1` = 2 番目、`2` = 3 番目など。

1. 「**[!UICONTROL Save Config]**」をクリックします。


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
