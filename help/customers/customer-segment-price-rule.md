---
title: 価格ルールの顧客セグメント
description: 顧客セグメントと買い物かご価格ルールの関連付けを説明し、ストアをターゲットにしたプロモーションを定義できるようにします。
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# 価格ルールの顧客セグメント

{{ee-feature}}

顧客セグメントは、次の項目に関連付けることで、ターゲットプロモーションに使用できます [買い物かご価格ルール](../merchandising-promotions/price-rules-cart.md).

![買い物かご価格ルール – ターゲット顧客セグメント](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_**セグメントを買い物かご価格ルールに関連付ける手順は、次のとおりです。**_

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _プロモーション_ > **[!UICONTROL Cart Price Rules]**.

1. 新規または既存のルールを開きます。

   * 新しいルールを使用するには、 **[!UICONTROL Add New Rule]** 右上隅
   * 既存のルールを使用するには、リストでルールをクリックして、編集モードで開きます。

1. 下にスクロールして、 **[!UICONTROL Conditions]** セクション。

1. 条件を追加します。

   * 「」をクリックします _追加_ （![リストアイコン](../assets/icon-add-green-circle.png)） アイコンで条件のリストを表示します。 次に、を選択します **[!UICONTROL Customer Segment]**.

   ![買い物かご価格ルール – 顧客セグメント条件の追加](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   デフォルトでは、条件は一致する条件を検索するように設定されています。 必要に応じて、 **[!UICONTROL matches]** リンクして、オペレーターを次のいずれかに変更します。

   * `does not match`
   * `is one of`
   * `is not one of`

   ![条件演算子](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. 特定のセグメントをターゲットにするには、「詳細」をクリックします **...** 追加のオプションを表示するリンク。 次に、 _選択_ （![リストアイコン](../assets/icon-list-chooser.png)）アイコンをクリックして、顧客セグメントのリストを表示します。

1. リストで、条件でターゲットにする各セグメントのチェックボックスを選択します。

   ![買い物かご価格ルール – 条件選択リスト](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Select]** 選択した顧客セグメントを条件に配置します。

1. 必要に応じて、残りの価格ルールを完了します。

1. 完了したら、 **[!UICONTROL Save]**.
