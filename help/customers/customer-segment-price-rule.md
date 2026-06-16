---
title: 価格ルールの顧客セグメント
description: 顧客セグメントをカート価格ルールに関連付けて、ストアのターゲットを絞ったプロモーションを定義できるようにする方法について説明します。
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
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
source-wordcount: 232
ht-degree: 0%

---

# 価格ルールの顧客セグメント

{{ee-feature}}

顧客セグメントは、[買い物かご価格ルール &#x200B;](../merchandising-promotions/price-rules-cart.md)に関連付けることで、ターゲットを絞ったプロモーションに使用できます。

![買い物かごの価格ルール – ターゲット顧客セグメント &#x200B;](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**セグメントをカート価格ルールに関連付けるには：**&#x200B;_

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _プロモーション_ > **[!UICONTROL Cart Price Rules]**&#x200B;に移動します。

1. 新規または既存のルールを開きます。

   * 新しいルールを使用するには、右上隅の「**[!UICONTROL Add New Rule]**」をクリックします。
   * 既存のルールを使用するには、リスト内のルールをクリックして、編集モードでルールを開きます。

1. 下にスクロールして、**[!UICONTROL Conditions]** セクションを展開します。

1. 条件を追加します。

   * 条件のリストを表示する&#x200B;_追加_ （![&#x200B; リストアイコン &#x200B;](../assets/icon-add-green-circle.png)）アイコンをクリックします。 次に、**[!UICONTROL Customer Segment]**&#x200B;を選択します。

   ![買い物かごの価格ルール – 顧客セグメント条件を追加](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   デフォルトでは、条件は一致する条件を見つけるように設定されています。 必要に応じて、**[!UICONTROL matches]** リンクをクリックし、演算子を次のいずれかに変更します。

   * `does not match`
   * `is one of`
   * `is not one of`

   ![条件演算子](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. 特定のセグメントをターゲットにするには、「その他&#x200B;**...**」リンクをクリックして追加のオプションを表示します。 次に、_Chooser_ （![&#x200B; リストアイコン &#x200B;](../assets/icon-list-chooser.png)）アイコンをクリックして、顧客セグメントのリストを表示します。

1. リストで、条件でターゲットにする各セグメントのチェックボックスを選択します。

   ![買い物かごの価格ルール – 条件選択リスト &#x200B;](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. **[!UICONTROL Select]**&#x200B;をクリックして、選択した顧客セグメントを条件に配置します。

1. 必要に応じて、残りの価格ルールを完了します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。
