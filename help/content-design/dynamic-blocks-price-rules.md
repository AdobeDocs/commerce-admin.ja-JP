---
title: 価格ルールのダイナミックブロック
description: ダイナミックブロックをプロモーション価格ルールに関連付けます。
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/Fzw3GXEp2PNXIuvOpN62tBiLhTeMJGsDMfQpRwV1dSg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
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
source-wordcount: 317
ht-degree: 0%

---

# 価格ルールのダイナミックブロック

{{ee-feature}}

作成した[動的ブロック &#x200B;](dynamic-blocks.md)は、プロモーションに関連付けることができます。 関連付けを行うには、まず動的ブロックと[&#x200B; カタログ価格ルール &#x200B;](../merchandising-promotions/price-rules-catalog.md)または[&#x200B; カート価格ルール &#x200B;](../merchandising-promotions/price-rules-cart.md)の両方を作成する必要があります。 関連付けは、価格ルールの作業中や動的ブロックの作業中に行うことができます。

>[!IMPORTANT]
>
>この関連付けを作成すると、ルールが実行されたときに動的ブロックが&#x200B;**のみ**&#x200B;表示されます。 プロモーションがセグメント Aをターゲットにしている場合、ブロックはセグメント Aに表示されます。プロモーションがアクティブでない場合、ブロックは表示されません。

## ダイナミックブロックと価格ルールの関連付け

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_&#x200B;に移動し、次のいずれかを選択します。

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. グリッドで、ダイナミックブロックに関連付けるルールを見つけて、編集モードで開きます。

1. 下にスクロールして、![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**&#x200B;を展開します。

1. 最初の列で、フィルターを`Any`に設定し、**[!UICONTROL Reset Filter]**&#x200B;をクリックします。

   グリッドに、使用可能なすべての動的ブロックが一覧表示されるようになりました。

1. ルールに関連付ける各ダイナミックブロックのチェックボックスを選択します。

   ![選択した動的ブロックの追加](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## 価格ルールの動的ブロックへの関連付け

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**&#x200B;に移動します。

1. グリッドでダイナミックブロックを見つけ、編集モードで開きます。

1. 下にスクロールして、**[!UICONTROL Related Promotions]**&#x200B;を展開します。

   現在関連付けられている価格ルールはすべてグリッドに表示されます。

1. 新しい関連付けられたルールを追加するか、現在の関連付けを削除します。

   - 買い物かごプロモーションを関連付けるには、**[!UICONTROL Add Cart Price Rules]**&#x200B;をクリックします。

   - 製品関連のプロモーションを関連付けるには、**[!UICONTROL Add Catalog Price Rules]**&#x200B;をクリックします。

1. グリッドで、ダイナミックブロックに関連付ける各ルールのチェックボックスを選択します。

1. **[!UICONTROL Add Selected]**&#x200B;をクリックします。

   ![選択した価格ルールを動的ブロックに追加](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。
