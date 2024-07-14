---
title: 関連する製品ルール
description: 関連する製品ルールと、関連製品、アップセルおよびクロスセルを顧客に動的に提示する際の使用方法について説明します。
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# 関連する製品ルール（ターゲットルール）

{{ee-feature}}

関連製品ルールを使用すると、関連製品、アップセルおよびクロスセルとして顧客に表示される製品の選択をターゲットにすることができます。 各製品ルールを [ 顧客セグメント ](../customers/customer-segments.md) に関連付けて、ターゲットマーチャンダイジングの動的表示を作成できます。

同時に複数のアクティブなルールをトリガーできるので、ルールごとに優先度を設定できます。 ルールが適用される順序と、ページ上での製品の表示順序を定義します。

関連する製品ルールにアクセスするには、**[!UICONTROL Marketing]**/_[!UICONTROL Promotions]_/**[!UICONTROL Related Product Rules]**に移動します。

![ 関連製品ルールリスト ](./assets/related-products-rules.png){width="700" zoomable="yes"}

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 関連する各製品ルールに割り当てられる一意の数値識別子 |
| [!UICONTROL Rule] | 関連商品ルールの名前 |
| [!UICONTROL Start] | 動的カレンダーフィールド（_[!UICONTROL To:]_および_[!UICONTROL From:]_）を使用して、ルールの作成時に定義されたルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | 動的カレンダーフィールド（_[!UICONTROL To:]_および_[!UICONTROL From:]_）を使用して、ルールの作成時に定義されたルールの終了日に基づいてリストをフィルタリングします。 |
| [!UICONTROL Priority] | ルールに定義されている優先度に基づいてリストをフィルタリングするには、このフィールドにテキストを入力します。 |
| [!UICONTROL Applies To] | このオプションは、`Related Products`、`Up-sells` および `Cross-sells` に適用されるルールのリストをフィルタリングします。 |
| [!UICONTROL Status] | このオプションを使用して、ルールのステータス（`Active` または `Inactive`）に基づいてリストをフィルタリングします。 |

{style="table-layout:auto"}

## ルールの優先度

トリガーして、関連製品、アップセルおよびクロスセルを表示できるアクティブなルールが、いつでも複数ある場合があります。 各ルールの優先度によって、ページ上での商品の表示順序が決まります。 この値は任意の整数に設定でき、`1` の優先度は最も高くなります。

プロダクトリレーションルールに含めることができるプロダクト ID の数は、`Result Limit` 値（最大 20）によって決まります。 `Result Limit` 値は、特定のルールベースの製品プロモーションの `Configurable Maximum` と組み合わせて `Real Limit` になり、リストに表示できる一致する製品の実際の数を決定します。

[ 結果の制限 ] + [ 設定可能な最大 ] = [ 実際の制限 ]

例えば、優先度が `1`、`2`、`3` の 3 つのルールがあるとします。

- _ルール 1_ には 2 つの一致する製品が返され、_ルール 2_ には 6 つの一致する製品が返され、_ルール 3_ には 20 の一致する製品が返されます。
- 設定では、_[!UICONTROL Maximum Number of Products for Related Products List]_は `6` に設定されます。

  | ルール | 優先度 | 一致する製品 |
  |---|---|-----|
  | ルール 1 | `1` | `2` |
  | ルール 2 | `2` | `6` |
  | ルール 3 | `3` | `20` |

最初のルールが _設定可能な最大限度_ で許可された数より多く、_実際の限度_ 未満の一致する製品を返した場合、_実際の限度_ に達するまで、他のルールの一致する製品が（優先順位の高い順に）使用されます。

優先度別に、_ルール 1_ から返された一致する製品を最初に使用して、使用可能な 26 のすべてのスロットを埋めることができます。 ルール 1 では一致する製品が 2 つしか返されなかったので、まだ 24 個分の余裕があります。 _ルール 2_ の優先度が次に高く、一致する製品がさらに 6 つ返されます。 現在、18 個のスロットが利用可能です。 _ルール 3_ の優先度は次のレベルで、残りの 18 個のスロットを埋めるのに十分な数の一致する製品があります。 使用可能なすべてのスロットが一杯になると、設定されている回転モードに応じて、各優先度内の ID によって製品がシャッフルまたは並べ替えられ、設定可能な最大限度に減らされる場合があります。 この場合、残りの 6 つの製品がストアに表示されます。

>[!NOTE]
>
>選択した製品は、回転モードに関係なく、常にルールベースの製品の前に表示されます。

## ルールベースの製品関係の設定

製品関係ルールの動作や一致した製品の表示は、設定によって決定されます。 これらの設定は、ルールに一致する製品の表示可能数と表示順序を決定します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下にある「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Rules-Based Product Relations]** のセクションの ![ 展開 ](../assets/icon-display-expand.png) を展開します。

   ![ カタログの設定 – ルールベースの製品関係 ](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. **[!UICONTROL Maximum Number of Products in the Related Products List]** を入力します。

1. **[!UICONTROL Show Related Products]** を次のいずれかに設定します。

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. **[!UICONTROL Rotation Mode for Products in Related Product List]** を次のいずれかに設定します。

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. クロスセル製品の設定を完了するには、次の手順を実行します。

   - **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]** を入力します。

   - **[!UICONTROL Show Cross-Sell Products]** を次のいずれかに設定します。

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** を次のいずれかに設定します。

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. アップセル製品の設定を完了するには、次の手順を実行します。

   - **[!UICONTROL Maximum Number of Products in the Upsell Product List]** を入力します。

   - **[!UICONTROL Show Upsell Products]** を次のいずれかに設定します。

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - **[!UICONTROL Rotation Mode for Products in Upsell Product List]** を次のいずれかに設定します。

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### 回転モード

| モード | 説明 |
|---|---|
| [!UICONTROL By Priority, Then by ID] | 製品は優先度別に並べ替えられ、各優先度内の ID で並べ替えられます。 優先度の低いルールの商品は、使用可能なスロットを埋めるために優先度の高いルールの商品が残っていない場合にのみ表示されます。 |
| [!UICONTROL By Priority, Then Random] | 製品は優先度別に並べ替えられ、各優先度内でランダム化されます。 優先度の低いルールの商品は、使用可能なスロットを埋めるために優先度の高いルールの商品が残っていない場合にのみ表示されます。 |
| [!UICONTROL Weighted Random] | 製品は、優先度が高いルールに属する製品が、優先度が低いルールに属する製品よりも出現する可能性が高くなるようにランダム化されます。 その後、製品は設定可能な最大限度まで削減され、優先度別に再グループ化されます。 このモードを使用すると、優先度の低いルールに属する製品が残りのスロットにいっぱいになる場合でも、優先度の低い製品が表示されることがあります |

{style="table-layout:auto"}

## Real-Time CDP オーディエンスを使用して、関連する製品ルールを通知します

>[!NOTE]
>
>この機能はベータ版です。 ベータ版プログラムへの参加を希望される場合は、[dataconnection@adobe.com](mailto:dataconnection@adobe.com) にリクエストを送信してください。


Real-Time CDP オーディエンスをAdobe Commerce インスタンスに [ アクティブ化 ](../customers/audience-activation.md) して、関連する商品ルールを通知する方法を説明します。
