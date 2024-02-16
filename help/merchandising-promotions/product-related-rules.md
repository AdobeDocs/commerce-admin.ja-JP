---
title: 関連する製品ルール
description: 関連する製品ルールと、それらを使用して、関連する製品、アップセルおよびクロスセルを顧客に動的に表示する方法について説明します。
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# 関連する製品ルール（ターゲットルール）

{{ee-feature}}

関連する製品ルールを使用すると、顧客に提示される製品の選択を関連製品、アップセルおよびクロスセルとしてターゲット設定できます。 各製品ルールは、 [顧客セグメント](../customers/customer-segments.md) ターゲットのマーチャンダイジングの動的な表示を生成する。

複数のアクティブなルールを同時にトリガーできるので、各ルールに優先度を設定できます。 ルールが適用され、製品がページに表示される順序を定義します。

関連する製品ルールにアクセスするには、に移動します。 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

![関連する製品ルールリスト](./assets/related-products-rules.png){width="700" zoomable="yes"}

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 関連する各製品ルールに割り当てられる一意の数値識別子 |
| [!UICONTROL Rule] | 関連する製品ルールの名前 |
| [!UICONTROL Start] | 動的カレンダーフィールド (_[!UICONTROL To:]_および_[!UICONTROL From:]_) をクリックして、ルールが作成された際に定義されたルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | 動的カレンダーフィールド (_[!UICONTROL To:]_および_[!UICONTROL From:]_) をクリックして、ルールの作成日時に定義されたルールの終了日に基づいてリストをフィルタリングします。 |
| [!UICONTROL Priority] | このフィールドにテキストを入力し、ルールに定義された優先度に基づいてリストをフィルタリングします。 |
| [!UICONTROL Applies To] | このオプションは、適用するルールのリストをフィルターします。 `Related Products`, `Up-sells`、および `Cross-sells`. |
| [!UICONTROL Status] | このオプションを使用して、ルールのステータス (`Active` または `Inactive`) をクリックします。 |

{style="table-layout:auto"}

## ルールの優先度

いつでも、関連製品、アップセルおよびクロスセルを表示するためにトリガーできるアクティブなルールが複数存在する場合があります。 各ルールの優先度によって、ページ上での商品の表示順序が決まります。 値は任意の整数に設定でき、 `1` 最も優先度が高い

製品の関係ルールに含めることができる製品 ID の数は、 `Result Limit` 値（最大 20）。 The `Result Limit` 値、との組み合わせ `Configurable Maximum` 特定のルールベースの製品プロモーションの場合、 `Real Limit`、およびは、リストに表示できる、一致する製品の実際の数を決定します。

[結果の制限] + [設定可能な最大値] = [実際の制限]

例えば、優先度がの 3 つのルールがあるとします。 `1`, `2`、および `3`.

- に対して、一致する製品が 2 つ返されます。 _ルール 1_, 6 つの一致する製品 _ルール 2_、および一致する製品 20 個： _ルール 3_.
- この設定では、 _[!UICONTROL Maximum Number of Products for Related Products List]_が `6`.

  | ルール | 優先度 | 一致する製品 |
  |---|---|-----|
  | ルール 1 | `1` | `2` |
  | ルール 2 | `2` | `6` |
  | ルール 3 | `3` | `20` |

最初のルールが、 _設定可能な最大限界値_（ただし、より小さい） _実際の限界_&#x200B;の場合、他のルールと一致する製品が（優先順に） _実際の限界_ に到達しました。

優先度別に、一致する製品がから返されます。 _ルール 1_ は、最初に使用可能な 26 個のスロットをすべて埋めるために使用できます。 ルール 1 は一致する製品を 2 つだけ返したので、さらに 24 個の余地が残っています。 _ルール 2_ は次に高い優先度を持ち、さらに 6 つの一致する製品を返します。 現在、18 個のスロットが空き容量で満たされます。 _ルール 3_ は次の優先度を持ち、残りの 18 個のスロットを満たすのに十分な一致製品を持ちます。 使用可能なすべてのスロットが満たされ、設定されている回転モードに応じて、製品は各優先度内の ID でシャッフルまたは並べ替えられ、設定可能な最大値に減らされます。 この場合、残り 6 つの製品が店舗に表示されます。

>[!NOTE]
>
>選択した製品は、回転モードに関係なく、ルールベースの製品の前に常に表示されます。

## ルールベースの製品関係を設定する

製品関係ルールの動作と一致する製品の表示は、設定によって決まります。 これらの設定は、ルールに一致する製品の表示数と表示順を決定します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張](../assets/icon-display-expand.png) の **[!UICONTROL Rules-Based Product Relations]** 」セクションに入力します。

   ![カタログ設定 — ルールベースの製品関係](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. 次を入力します。 **[!UICONTROL Maximum Number of Products in the Related Products List]**.

1. 設定 **[!UICONTROL Show Related Products]** を次のいずれかに変更します。

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. 設定 **[!UICONTROL Rotation Mode for Products in Related Product List]** を次のいずれかに変更します。

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. クロス販売製品の設定を完了するには、次の手順を実行します。

   - 次を入力します。 **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]**.

   - 設定 **[!UICONTROL Show Cross-Sell Products]** を次のいずれかに変更します。

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - 設定 **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** を次のいずれかに変更します。

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. アップセル製品の設定を完了するには、次の手順を実行します。

   - 次を入力します。 **[!UICONTROL Maximum Number of Products in the Upsell Product List]**.

   - 設定 **[!UICONTROL Show Upsell Products]** を次のいずれかに変更します。

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - 設定 **[!UICONTROL Rotation Mode for Products in Upsell Product List]** を次のいずれかに変更します。

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 完了したら、「 **[!UICONTROL Save Config]**.

### 回転モード

| モード | 説明 |
|---|---|
| [!UICONTROL By Priority, Then by ID] | 製品は優先順位で並べ替えられ、優先順位ごとに ID で並べ替えられます。 優先度が低いルールの製品は、使用可能なスロットを埋める優先度が高いルールの製品が残っていない場合にのみ表示されます。 |
| [!UICONTROL By Priority, Then Random] | 製品は優先順位で並べ替えられ、次に各優先度内でランダム化されます。 優先度が低いルールの製品は、使用可能なスロットを埋める優先度が高いルールの製品が残っていない場合にのみ表示されます。 |
| [!UICONTROL Weighted Random] | 優先度の高いルールに属する製品が、優先度の低いルールに属する製品よりも出現する確率が高くなるように、製品がランダム化されます。 その後、製品は設定可能な最大数に減らされ、優先度ごとに再グループ化されます。 このモードでは、優先度の低い製品が、他のスロットに優先度の高いルールの製品がいっぱいになる場合でも、表示される可能性があります |

{style="table-layout:auto"}

## Real-Time CDPオーディエンスを使用して、関連する製品ルールに通知を送信する

>[!NOTE]
>
>この機能はベータ版です。 ベータ版プログラムに参加したい場合は、にリクエストを送信してください。 [dataconnection@adobe.com](mailto:dataconnection@adobe.com).


方法を学ぶ [アクティブ化](../customers/audience-activation.md) Real-Time CDPオーディエンスをAdobe Commerceインスタンスに取り込み、関連する製品ルールに通知します。
