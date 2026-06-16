---
title: カートの価格ルール
description: 一連の条件に基づいて、ショッピングカート内の商品に割引を適用するカート価格ルールについて説明します。
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/i3G3iGuomU0cjy3aX9eynyzAtpCgQxeEFAyRUdUUu44
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 451
ht-degree: 0%

---

# カートの価格ルール

カートの価格規則ショッピングカート内の商品に、一連の条件に基づく割引を適用します。 割引は、条件が満たされた場合、または顧客が有効なクーポンコードを入力した場合に、自動的に適用できます。 適用すると、小計の下のカートに割引が表示されます。 カートの価格ルールは、状況と日付範囲を変更することで、シーズンやプロモーションの必要に応じて使用できます。

>[!NOTE]
>
>クーポンカートのルールに、特定の配送方法や支払い方法など、チェックアウトオプションを指定する条件が設定されている場合、その条件は、特定の配送/支払い方法を選択した後にのみチェックアウトで満たされます。 この場合、最後のステップでチェックアウト時にクーポンを適用できます。

![ ストアフロントの例 – カート適用クーポン ](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## カート価格ルールへのアクセス

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**に移動します。

   ![買い物かごの価格ルール ](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. ルールが多い場合は、各列の上部にあるフィルターオプションを使用してリストを合理化し、**[!UICONTROL Search]**&#x200B;をクリックしてフィルターを適用します。

1. すべてのフィルターオプションをクリアして完全なリストを表示するには、**[!UICONTROL Reset Filter]**&#x200B;をクリックします。

1. ルールのプロパティを更新：

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）「**[!UICONTROL Edit]**」をクリックして、ルール情報ページを表示します。

   - ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）リスト内のルールをクリックすると、ルール情報ページが表示されます。

   そこで、ルールの設定を変更できます（ルールの作成と同様）。

## 列によるオプションのフィルタリング

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | テキストを入力して、特定のルール ID番号のリストをフィルタリングします。 |
| [!UICONTROL Rule] | ルールの作成時に定義したルール名に基づいてリストをフィルタリングするテキストを入力します。 |
| [!UICONTROL Coupon Code] | ルールの作成時に定義されたコード名に基づいてリストをフィルタリングするテキストを入力します。 |
| [!UICONTROL Priority] | ルールに対して定義された優先度に基づいてリストをフィルタリングするフリーテキストフィールド。 |
| [!UICONTROL Status] | このオプションを使用して、ルールの状態（`Active`または`Inactive`）に基づいてリストをフィルタリングします。 |
| [!UICONTROL Web Site] | このオプションを使用すると、ルールに対して定義されたweb サイトに基づいてリストをフィルタリングできます。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）「**[!UICONTROL Edit]**」をクリックして&#x200B;_[!UICONTROL Rule Information]_ページを表示し、ルール設定を更新します（ルールの作成と同様）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）動的カレンダーフィールド（_[!UICONTROL To:]_および_[!UICONTROL From:]_）を使用して、ルールの作成時に定義されたとおりに、ルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）動的カレンダーフィールド（_[!UICONTROL To:]_および_[!UICONTROL From:]_）を使用して、ルールの作成時に定義されたとおりに、ルールの終了日に基づいてリストをフィルタリングします。 |

{style="table-layout:auto"}

## Real-Time CDPのオーディエンスを利用して、カートの価格ルールを設定し

Real-Time CDP オーディエンスを[ アクティブ化](../customers/audience-activation.md)してAdobe Commerce インスタンスに登録し、カートの価格ルールを設定する方法について説明します。
