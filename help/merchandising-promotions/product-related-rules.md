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

関連製品ルールを使用すると、関連製品、アップセルおよびクロスセルとして顧客に表示される製品の選択をターゲットにすることができます。 各製品ルールは、 [顧客セグメント](../customers/customer-segments.md) ターゲットマーチャンダイジングの動的表示を生成する。

同時に複数のアクティブなルールをトリガーできるので、ルールごとに優先度を設定できます。 ルールが適用される順序と、ページ上での製品の表示順序を定義します。

関連する製品ルールにアクセスするには、に移動します。 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

![関連する製品ルールリスト](./assets/related-products-rules.png){width="700" zoomable="yes"}

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 関連する各製品ルールに割り当てられる一意の数値識別子 |
| [!UICONTROL Rule] | 関連商品ルールの名前 |
| [!UICONTROL Start] | 動的カレンダーフィールドを使用する（_[!UICONTROL To:]_および_[!UICONTROL From:]_）を選択し、ルールの作成時に定義したルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | 動的カレンダーフィールドを使用する（_[!UICONTROL To:]_および_[!UICONTROL From:]_）を選択し、ルールの作成時に定義したルールの終了日に基づいてリストをフィルタリングします。 |
| [!UICONTROL Priority] | ルールに定義されている優先度に基づいてリストをフィルタリングするには、このフィールドにテキストを入力します。 |
| [!UICONTROL Applies To] | このオプションは、に適用されるルールのリストをフィルタリングします `Related Products`, `Up-sells`、および `Cross-sells`. |
| [!UICONTROL Status] | このオプションを使用して、ルールのステータス（`Active` または `Inactive`）に設定します。 |

{style="table-layout:auto"}

## ルールの優先度

トリガーして、関連製品、アップセルおよびクロスセルを表示できるアクティブなルールが、いつでも複数ある場合があります。 各ルールの優先度によって、ページ上での商品の表示順序が決まります。 この値は、以下の構文で、任意の整数に設定することができます。 `1` 優先順位が最も高い。

プロダクトリレーションルールに含めることができるプロダクト ID の数は、によって決まります。 `Result Limit` 値（最大 20 個）。 この `Result Limit` 値、と `Configurable Maximum` 特定のルールベースの製品プロモーションの場合、 `Real Limit`、およびリストに表示できる一致する製品の実際の数を決定します。

[結果の制限] + [設定可能な最大値] = [実際の制限]

例えば、優先度がの 3 つのルールがあるとします `1`, `2`、および `3`.

- 一致する商品が 2 つ返される _ルール 1_、6 つの一致する製品： _ルール 2_、および 20 個の一致する製品 _ルール 3_.
- 設定で、 _[!UICONTROL Maximum Number of Products for Related Products List]_はに設定されています。 `6`.

  | ルール | 優先度 | 一致する製品 |
  |---|---|-----|
  | ルール 1 | `1` | `2` |
  | ルール 2 | `2` | `6` |
  | ルール 3 | `3` | `20` |

最初のルールが、許可されているよりも多くの一致する製品を返す場合 _設定可能な最大制限_&#x200B;ただし、より小さい _実際の制限_、まで、他のルールの一致する製品が（優先順に）使用されます _実際の制限_ に達しました。

優先度別に、一致する商品が返されます _ルール 1_ 最初に使用して、使用可能な 26 個のスロットをすべて埋めることができます。 ルール 1 では一致する製品が 2 つしか返されなかったので、まだ 24 個分の余裕があります。 _ルール 2_ は次に優先順位が高く、一致する商品をさらに 6 つ返します。 現在、18 個のスロットが利用可能です。 _ルール 3_ は、残りの 18 個のスロットを埋めるのに十分な一致製品で、次のレベルの優先度を持っています。 使用可能なすべてのスロットが一杯になると、設定されている回転モードに応じて、各優先度内の ID によって製品がシャッフルまたは並べ替えられ、設定可能な最大限度に減らされる場合があります。 この場合、残りの 6 つの製品がストアに表示されます。

>[!NOTE]
>
>選択した製品は、回転モードに関係なく、常にルールベースの製品の前に表示されます。

## ルールベースの製品関係の設定

製品関係ルールの動作や一致した製品の表示は、設定によって決定されます。 これらの設定は、ルールに一致する製品の表示可能数と表示順序を決定します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルでを展開します。 **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開](../assets/icon-display-expand.png) この **[!UICONTROL Rules-Based Product Relations]** セクション。

   ![カタログの設定 – ルールベースの製品関係](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. を入力 **[!UICONTROL Maximum Number of Products in the Related Products List]**.

1. を設定 **[!UICONTROL Show Related Products]** を次のいずれかに変更します。

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. を設定 **[!UICONTROL Rotation Mode for Products in Related Product List]** を次のいずれかに変更します。

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. クロスセル製品の設定を完了するには、次の手順を実行します。

   - を入力 **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]**.

   - を設定 **[!UICONTROL Show Cross-Sell Products]** を次のいずれかに変更します。

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - を設定 **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** を次のいずれかに変更します。

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. アップセル製品の設定を完了するには、次の手順を実行します。

   - を入力 **[!UICONTROL Maximum Number of Products in the Upsell Product List]**.

   - を設定 **[!UICONTROL Show Upsell Products]** を次のいずれかに変更します。

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - を設定 **[!UICONTROL Rotation Mode for Products in Upsell Product List]** を次のいずれかに変更します。

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 完了したら、 **[!UICONTROL Save Config]**.

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
>この機能はベータ版です。 ベータ版プログラムへの参加を希望される場合は、以下にリクエストを送信します。 [dataconnection@adobe.com](mailto:dataconnection@adobe.com).


方法を学ぶ [アクティベート](../customers/audience-activation.md) Adobe Commerce インスタンスにオーディエンスをReal-Time CDPし、関連する製品ルールを通知します。
