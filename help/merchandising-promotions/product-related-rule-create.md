---
title: 関連製品ルールの作成
description: 関連製品、アップセル、およびクロスセルを表示するためにトリガーできる関連製品ルールを作成する方法について説明します。
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
TQID: https://experienceleague.adobe.com/jfs0iFZxLKfvJpRGLA6Hi1dADcGEvm4PJIolOf2nfI4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 648
ht-degree: 0%

---

# 関連製品ルールの作成

{{ee-feature}}

関連製品ルールを作成するプロセスは、価格ルールの設定に似ています。 まず、一致する条件を定義し、次に表示する製品を選択します。 どの時点でも、関連商品、アップセル、クロスセルを表示するためにトリガーできるいくつかのアクティブなルールが存在する場合があります。 各ルールの優先順位によって、製品ブロックがページに表示される順序が決まります。

>[!NOTE]
>
>ターゲット ルールで属性を使用するには、[_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md) プロパティを`Yes`に設定する必要があります。

>[!NOTE]
>
>`All Store Views` スコープ値は、すべての製品属性の[!UICONTROL Products to Match]条件と[!UICONTROL Products to Display]条件の両方に常に使用されます。 これは、ストアビューやweb サイトごとに異なる製品属性の値が異なる場合にも適用されます。

## 関連製品ルールの作成

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add Rule]**」をクリックします。

   ![関連製品ルール – 情報](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. 次のように&#x200B;**[!UICONTROL Rule Information]**&#x200B;を入力します。

   - 管理者で作業する際にルールを識別するには、**[!UICONTROL Rule Name]**&#x200B;を入力します。

   - **[!UICONTROL Priority]**&#x200B;に、他のルールの結果が同じ場所をターゲットとする場合に、ページ上に結果が表示される順序を決定する数値を入力します。 番号`1`は最優先事項です。

   - ルールを有効にするには、**[!UICONTROL Status]**&#x200B;を`Active`に設定します。

   - **[!UICONTROL Apply To]**&#x200B;を次のいずれかに設定します：

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - ルールを特定の期間アクティブにする場合は、**[!UICONTROL From]**&#x200B;日と&#x200B;**[!UICONTROL To]**&#x200B;日を入力します。

   - **[!UICONTROL Result Limit]**&#x200B;に、結果リストに表示するレコードの数を入力します。 最大数は20です。

   - ルールが特定の[顧客セグメント &#x200B;](../customers/customer-segments.md)に適用される場合、**[!UICONTROL Customer Segments]**&#x200B;を`Specified`に設定し、リストから顧客セグメントを選択します。

   - ルールが特定の[Real-Time CDP オーディエンス &#x200B;](../customers/audience-activation.md)に適用される場合、**[!UICONTROL Real-Time CDP Audience]**&#x200B;を`Specified`に設定し、リストからReal-Time CDP オーディエンスを選択します。

     ![関連製品ルール - Real-Time CDP オーディエンス &#x200B;](./assets/rtcdp-related-products.png){width="500"}

1. 左側のパネルで、**[!UICONTROL Products to Match]**&#x200B;を選択し、[&#x200B; カタログ価格ルール &#x200B;](price-rules-catalog.md)の場合と同じように条件を作成します。

   ![関連製品ルール – 一致する製品](./assets/catalog-related-products-match.png){width="500"}

1. 左側のパネルで、**[!UICONTROL Products to Display]**&#x200B;を選択し、[&#x200B; カタログ価格ルール &#x200B;](price-rules-catalog.md)の場合と同じように結果条件を作成します。

   ![関連製品ルール – 表示する製品](./assets/catalog-related-products-to-display.png){width="500"}

   表示された結果に含める製品を記述する条件を完了します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## 関連製品ルールの削除

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**&#x200B;に移動します。

1. 削除する関連製品ルールを見つけます。

1. ルールをクリックして詳細ページを開きます。

1. 右上隅の「**[!UICONTROL Delete]**」をクリックします。

1. アクションを確認するには、**[!UICONTROL OK]**&#x200B;をクリックします。

## 関連製品ルールのデモ

関連製品のルール設定について詳しくは、次の動画をご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Rule Name] | 内部使用のルールを識別する名前。 |
| [!UICONTROL Priority] | ページ上の同じ場所をターゲットとする他の結果セットと共に表示されるときに、ルールの結果が表示される順序を指定します。 値は、優先度が1の整数に設定できます。 例えば、適用されるアップセルルールが複数ある場合、最も優先度の高いルールが他のルールよりも先に表示されます。 結果の各セット内の製品の並べ替え順序はランダムです。 手動で設定されたアップセル、クロスセル、関連製品は、常にルールベースの製品プロモーションの前にページに表示されます。 |
| [!UICONTROL Status] | ルールのアクティブなステータスを制御します。 オプション：`Active` / `Inactive` |
| [!UICONTROL Apply To] | ルールに関連付けられている製品関係のタイプを識別します。 オプション：`Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | 一定期間ルールがアクティブな場合、この設定によってルールがアクティブな最初の日付が決まります。 |
| [!UICONTROL To Date] | ルールが一定期間アクティブである場合、この設定により、ルールがアクティブである最後の日付が決まります。 |
| [!UICONTROL Result Limit] | 一度に結果に表示される製品数を指定します。 最大数は20です。 一致する結果がより多く見つかった場合、ページが更新されるたびに製品がブロック内を回転します。 |
| [!UICONTROL Customer Segments] | ルールが適用される顧客セグメントを識別します。 オプション：`All` / `Specified` |

{style="table-layout:auto"}
