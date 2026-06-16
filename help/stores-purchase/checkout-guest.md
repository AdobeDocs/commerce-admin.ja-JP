---
title: ゲストチェックアウト
description: ストアでゲストチェックアウト機能を有効にする方法について説明します。
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
TQID: https://experienceleague.adobe.com/jxrHQ1knuqHBmM1DsVa9NqdV-XNFdQDWjvwW4kHEyYM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# ゲストチェックアウト

ストアは、買い物客が購入する前にアカウントを開くように設定できます。 デフォルト設定では、チェックアウトプロセスを完了した後にアカウントに登録するオプションを使用して、ゲストが購入できます。

![Luma ストアに「ゲストとしてチェックアウト」と表示される](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_ゲストチェックアウトを無効にするには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Checkout]**&#x200B;を選択します。

1. **[!UICONTROL Checkout Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![設定ページでチェックアウトオプションが拡張されました](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

これらの各構成設定の詳細については、_構成リファレンスガイド_&#x200B;の[&#x200B; チェックアウトオプション &#x200B;](../configuration-reference/sales/checkout.md#checkout-options)を参照してください。

1. 設定が特定のストアビューの場合、[設定が適用されるストアビュー](../configuration-reference/scope-change.md#set-the-scope)を選択します。

   プロンプトが表示されたら、**[!UICONTROL OK]**&#x200B;をクリックして続行します。

1. **[!UICONTROL Allow Guest Checkout]**&#x200B;を`No`に設定します。

   必要に応じて、**[!UICONTROL Use system value]** チェックボックスをオフにして、この設定の変更を有効にします。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

## 登録済み電子メールに対するゲスト注文のアクセスを許可

[!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクト（Adobeで管理されるSaaS インフラストラクチャ）にのみ適用されます。"}

オプションのストアレベル設定は、デフォルトで無効になっていますが、ゲストの買い物客は、登録済みの顧客アカウントに一致するメールアドレスを使用して、注文した注文を追跡できます。

有効にすると、登録済みの電子メールで行われたゲストチェックアウトの注文にアクセスできるようになりますが、顧客の注文履歴にも表示されます。

この機能を有効にするには、**Stores** / 設定/**Configuration** / 営業/**Sales** / **ゲストチェックアウト**&#x200B;に移動し、**登録済み電子メールのゲストオーダーアクセスを許可**&#x200B;設定を`Yes`に設定します。
