---
title: 製品設定 – [!UICONTROL Gift Options]
description: 商品の場合、[!UICONTROL Gift Options]の設定によって、ギフトメッセージを含めることができるか、チェックアウト時にギフトのラッピングオプションを利用できるかが決まります。
exl-id: 21597e38-60f5-45e5-8d99-955d088c5c48
feature: Catalog Management, Products, Gift
TQID: 'https://experienceleague.adobe.com/MIzb2vY-DiVqODkNFmgX3tFLejQFZMtOETUDPoHrt-Y'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 4fc0a729-4349-5307-bd06-1b4bfbaf5d0c
    internal-label: Gift
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%
---
# 製品設定 – [!UICONTROL Gift Options]

_[!UICONTROL Gift Options]_セクションでは、チェックアウト時に商品レベルでギフトメッセージとギフト包装オプションを設定できます。 既定の構成設定を上書きするには、**[!UICONTROL Use Config Settings]**チェックボックスの選択を解除します。

![ ギフトオプション ](./assets/product-gift-options-ee.png){width="600" zoomable="yes"}

## 1つの商品にギフトオプションを設定する

1. 製品を編集モードで開きます。

1. 下にスクロールして、_[!UICONTROL Gift Options]_セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - 既定の設定を上書きするには、**[!UICONTROL Use Config Settings]** チェックボックスの選択を解除します。

   - 製品に必要に応じて&#x200B;**[!UICONTROL Allow Gift Message]**&#x200B;を設定します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （[Adobe Commerce](../landing/home.md#product-editions)のみ）商品の必要に応じて&#x200B;**[!UICONTROL Allow Gift Wrapping]**&#x200B;を設定します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （[Adobe Commerce](../landing/home.md#product-editions)のみ）該当する場合は、**[!UICONTROL Price for Gift Wrapping]**&#x200B;を入力します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## ストアのギフトメッセージを有効にする

Commerceでは、デフォルトで、チェックアウトプロセス中に、お客様が注文や商品にパーソナライズされたギフトメッセージを追加できるようにしています。

この機能を顧客に提供するには、ストアの&#x200B;_ギフトメッセージ_&#x200B;を有効にします。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、下の「**[!UICONTROL Sales]**」を選択します。

1. ページの![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]**&#x200B;を展開します。

1. **[!UICONTROL Allow Gift Messages on Order Level]**&#x200B;の場合、`Yes`を選択して、注文全体に対して1つのギフトメッセージを有効にします。

1. **[!UICONTROL Allow Gift Messages for Order Items]**&#x200B;の場合、`Yes`を選択して、カスタマーショッピングカート内の個々のアイテムにギフトメッセージを個別に追加できるようにします。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

この設定を使用すると、次の例に示すように、お客様はストアフロントからカートページにギフトメッセージを追加できます。

![ ギフトメッセージ ](./assets/gift-message.png){width="600" zoomable="yes"}
