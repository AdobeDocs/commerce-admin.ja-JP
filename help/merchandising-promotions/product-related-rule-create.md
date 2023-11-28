---
title: 関連する製品ルールの作成
description: 関連製品、アップセルおよびクロスセルを表示するためにトリガーできる関連製品ルールを作成する方法を説明します。
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: 8f5a5fb6c277086e5f70221e4a6a5ae1b9e1abfe
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# 関連する製品ルールの作成

{{ee-feature}}

関連する製品ルールの作成プロセスは、価格ルールの設定に似ています。 まず、一致する条件を定義し、次に表示する製品を選択します。 いつでも、関連製品、アップセルおよびクロスセルを表示するためにトリガーできるアクティブなルールが複数存在する場合があります。 各ルールの優先度によって、製品のブロックがページに表示される順序が決まります。

>[!NOTE]
>
>ターゲットルールで使用する属性の場合、 [_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md) プロパティは次のように設定する必要があります： `Yes`.

>[!NOTE]
>
>The `All Store Views` 範囲の値は常に両方に使用されます [!UICONTROL Products to Match] および [!UICONTROL Products to Display] すべての製品属性の条件。 これは、ストアの表示や Web サイトごとに製品属性の値が異なる場合にも当てはまります。

## 関連する製品ルールの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. 右上隅で、 **[!UICONTROL Add Rule]**.

   ![関連製品ルール — 情報](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. 次を完了： **[!UICONTROL Rule Information]** 次のように指定します。

   - を入力します。 **[!UICONTROL Rule Name]** を使用して、管理者で作業する際にルールを識別する。

   - の場合 **[!UICONTROL Priority]**「 」では、他のルールの結果が同じ場所をターゲットとする場合に、結果がページに表示される順序を決定する数値を入力します。 数値 `1` が最も優先度が高い。

   - ルールを有効にするには、 **[!UICONTROL Status]** から `Active`.

   - 設定 **[!UICONTROL Apply To]** を次のいずれかに変更します。

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - ルールを特定の期間アクティブにする場合は、 **[!UICONTROL From]** および **[!UICONTROL To]** 日付。

   - の場合 **[!UICONTROL Result Limit]**「 」で、結果リストに表示するレコード数を入力します。 最大数は 20 です。

   - ルールが特定の [顧客セグメント](../customers/customer-segments.md)，設定 **[!UICONTROL Customer Segments]** から `Specified` 「 」リストから顧客セグメントを選択します。

1. 左側のパネルで、を選択します。 **[!UICONTROL Products to Match]** そして、 [カタログ価格ルール](price-rules-catalog.md).

   ![関連製品ルール — 一致する製品](./assets/catalog-related-products-match.png){width="500"}

1. 左側のパネルで、を選択します。 **[!UICONTROL Products to Display]** 結果の条件を作成します。 [カタログ価格ルール](price-rules-catalog.md).

   ![関連製品ルール — 表示する製品](./assets/catalog-related-products-to-display.png){width="500"}

   条件を満たして、表示される結果に含める製品を記述します。

1. 完了したら、「 **[!UICONTROL Save]**.

## 関連する製品ルールの削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. 削除する関連製品ルールを見つけます。

1. ルールをクリックして、詳細ページを開きます。

1. 右上隅で、 **[!UICONTROL Delete]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## 関連する製品ルールのデモ

関連する製品ルールの作成については、このビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Rule Name] | 内部使用のルールを識別する名前。 |
| [!UICONTROL Priority] | ページ上の同じ場所をターゲットとする他の結果セットと共に表示される場合に、ルールの結果を表示する順序を決定します。 値は任意の整数に設定でき、最も優先度が高い 1 を設定できます。 例えば、適用される複数のアップセルルールがある場合は、優先度が最も高いものが他のものより先に表示されます。 結果の各セット内の商品の並べ替え順はランダムです。 手動で設定したアップセル、クロス販売および関連製品は、常にルールベースの製品プロモーションの前にページに表示されます。 |
| [!UICONTROL Status] | ルールのアクティブなステータスを制御します。 オプション： `Active` / `Inactive` |
| [!UICONTROL Apply To] | ルールに関連付けられている製品関係のタイプを識別します。 オプション： `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | 一定の期間、ルールがアクティブである場合、この設定によってルールがアクティブな最初の日付が決まります。 |
| [!UICONTROL To Date] | 一定の期間、ルールがアクティブである場合、この設定によってルールがアクティブになる最後の日付が決まります。 |
| [!UICONTROL Result Limit] | 結果に一度に表示される製品の数を決定します。 最大数は 20 です。 一致する結果がさらに見つかった場合、ページが更新されるたびに、製品がブロック内を回転します。 |
| [!UICONTROL Customer Segments] | ルールを適用する顧客セグメントを識別します。 オプション： `All` / `Specified` |

{style="table-layout:auto"}
