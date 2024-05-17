---
title: カタログ価格ルールの作成
description: 一連の条件が満たされた場合に特定の製品に割引を適用するカタログ価格ルールを作成する方法を説明します。
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 0%

---

# カタログ価格ルールの作成

一連の条件が満たされた場合に特定の製品に割引を適用するには、次の手順に従います。 カタログ価格ルール割引は、商品が買い物かごに入れられる前に有効になります。

## 手順 1：ルールを追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Rule]**.

   この _[!UICONTROL Rule Information]_セクションは、以下のための拡張可能セクションを含む&#x200B;**[!UICONTROL Conditions]**および&#x200B;**[!UICONTROL Actions]**.

   ![カタログ価格ルール – 情報](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. を完了する **[!UICONTROL Rule Name]** および **[!UICONTROL Description]** フィールド。

   これらのフィールドは内部参照用です。

1. を **[!UICONTROL Status]** 必要に応じて価格ルールの。

   デフォルトでは、ステータスはです。 `Inactive`.

   >[!NOTE]
   >
   >ルールを作成したら、ステータスをに変更することで、そのステータスを更新できます。 `Active` または `Inactive` 必要に応じて。

1. 「」を選択します **[!UICONTROL Websites]** ルールを使用できる場所。

1. 「」を選択します **[!UICONTROL Customer Groups]** このルールが適用される。

   複数のグループを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   >[!NOTE]
   >
   >このリストのオプションは、で作成および管理する顧客グループによって異なります _顧客_ > _顧客グループ_.

1. ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ） **[!UICONTROL From]** および **[!UICONTROL To]** 価格ルールが有効になる日付を指定します。

   日付を入力するか、 **[!UICONTROL Calendar]** （![カレンダーアイコン](../assets/icon-calendar.png)）を選択して、日付を選択します。 日付を空白のままにすると、価格ルールが保存されたときにルールが有効になります。

1. 数値を入力して、 **[!UICONTROL Priority]** 他のルールとの関連で、このルールの。

   >[!NOTE]
   >
   >この _[!UICONTROL Priority]_設定は、同じカタログ製品が複数の価格ルールに設定された条件を満たす場合に重要です。 優先度の設定が最も高い（1 が最も高い）ルールが、商品に対してアクティブになります。

## 手順 2：条件の定義

使用できる条件のほとんどは、既存の属性値に基づいています。 すべての製品にルールを適用する場合は、条件を空白のままにします。

>[!NOTE]
>
>少なくとも 1 つの条件付き製品属性の値が空の場合、カタログ価格ルールは製品に適用されません。

>[!NOTE]
>
>を適用するには `Category` 製品属性の条件を any に [束](../catalog/product-create-bundle.md) または [グループ化](../catalog/product-create-grouped.md) 製品、ルールを正しく適用するには、すべての子製品が同じカテゴリに割り当てられている必要があります。 そうでない場合は、 [買い物かご価格ルール](price-rules-cart-create.md) 代わりにプロモーション。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Conditions]** セクション。

   デフォルトでは、最初の条件が表示され、次の状態になります。

   `If **ALL** of these conditions are **TRUE**:`

   ![カタログ価格ルール – 条件ライン 1](./assets/catalog-condition1.png){width="400"}

   ステートメントには 2 つの太字のリンクがあり、クリックすると、ステートメントのその部分のオプションの選択が表示されます。 これらの値の組み合わせを変更することで、様々な条件を作成できます。

1. 次のいずれかの方法で、ステートメントを変更します。

   - クリック **[!UICONTROL ALL]** を選択して、 `ALL` または `ANY`.
   - クリック **[!UICONTROL TRUE]** を選択して、 `TRUE` または `FALSE`.
   - すべての製品にルールを適用する場合は、条件を変更しません。

   これらの値の組み合わせを変更することで、様々な条件を作成できます。 この例では、デフォルトの条件が使用されます。

1. 「」をクリックします _追加_ （![アイコンを追加](../assets/icon-add-green-circle.png)）アイコンをクリックし、製品属性や組み合わせなど、条件のオプションを選択します。

1. の下のリスト **[!UICONTROL Product Attribute]**&#x200B;で、条件の基礎として使用する属性を選択します。

   この例では、条件はです `Attribute Set`.

   ![カタログ価格ルール – 条件ライン 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >属性をリストに表示するには、プロモーションルールの条件で使用するように設定する必要があります。 詳しくは、 [製品属性](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >使用する場合 `is not one of` を含む条件 _SKU_ 製品属性と設定可能な製品については、親と子の両方の製品 SKU を選択する必要があります。 ルール内のすべての子 SKU がリストされないようにするには、 `does not contain` 設定可能な製品とその子製品の共通 SKU 部分を持つ条件。

   選択した条件がステートメントに表示され、その後にさらに 2 つの太字リンクが表示されます。 オプションは、選択する条件属性によって異なります。 ステートメントには次の内容が含まれています。

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. クリック **[!UICONTROL is]** そして、満たす条件を記述した比較演算子を選択します。

   これらのオプションには、異なる比較のオプションが含まれる場合があります。 この例では、次のオプションがあります `is` および `is not`.

1. 条件の値を選択または入力します。

   条件に応じて、グリッドまたはリストから製品を選択したり、数値を入力したりできます。

   ![カタログ価格ルール – 条件ライン 2](./assets/catalog-condition3.png){width="400"}

   条件を完了するためのステートメントに、選択した項目が表示されます。

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. ステートメントに別の条件行を追加するには、 _追加_ （![アイコンを追加](../assets/icon-add-green-circle.png)）アイコンをクリックし、次のいずれかを選択します。

   - `Conditions Combination`
   - `Product Attribute`

   必要な条件がすべて完了するまで手順を繰り返します。

   条件ステートメントの一部を削除する場合は、をクリックします **[!UICONTROL Delete]** （![アイコンを削除](../assets/icon-delete-red-circle.png) 行の最後にあるアイコン。

## 手順 3：アクションの定義

1. を展開 ![展開セレクター](../assets/icon-display-expand.png)この **[!UICONTROL Actions]** を選択し、次の操作を実行します。

   ![カタログ価格ルール – アクション](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. 次の下 **[!UICONTROL Pricing Structure Rules]**、設定 **[!UICONTROL Apply]** を次のいずれかに変更します。

   - `Apply as percentage of original`  – 通常価格のパーセンテージを差し引いて品目を値引きします。 たとえば、通常価格から 10% 引き下げられた最終価格の「値引額」に 10 を入力します。
   - `Apply as fixed amount`  – 通常価格から固定金額を引いて品目を値引きします。 たとえば、最終価格が通常の価格より$10 少ない場合は、「割引額」に 10 と入力します。
   - `Adjust final price to this percentage`  – 最終価格を通常価格に対するパーセンテージで調整します。 たとえば、最終価格が通常価格から 75% 引かれた場合は、「割引額」に 25 と入力します。
   - `Adjust final price to discount value`  – 最終価格を固定の割引額に設定します。 たとえば、最終価格が$20.00 の場合は、「割引額」に 20 と入力します。

   >[!NOTE]
   >
   >_通常価格_ 高度な価格（特別/階層/グループ）やプロモーションの割引がない基本製品価格を指します。 _最終価格_ 買い物かごに表示される割引価格を指します。 <br/>この **_final_** 製品価格は次のように計算されます **_minimum_** 次の算式を使用した関連価格 <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_固定価格_** 製品のカスタマイズ可能なオプション _ではない_ グループ価格、階層価格、特別価格、カタログ価格ルールの影響を受けます。

1. を入力 **[!UICONTROL Discount Amount]**.

1. このルールを適用した後に他のルールの処理を停止するには、次のように設定します： **[!UICONTROL Discard Subsequent Rules]** 対象： `Yes`.

   >[!NOTE]
   >
   >この項目をに設定 `Yes` は、システムが同じ製品に複数の割引（ルール）を適用するのを防ぐためのセーフガードです。

## 手順 4：関連するダイナミック ブロックを追加する

{{ee-feature}}

[ダイナミック ブロック](../content-design/dynamic-blocks.md) カタログ価格ルールに関連付けられている指標は、条件が満たされると常にストアフロントに表示されます。 これはオプションの手順です。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png)この **[!UICONTROL Related Dynamic Blocks]** セクション。

1. の使用 [フィルターを検索](../getting-started/admin-workspace.md) 規則に関連付けるダイナミック ブロックを検索するには

1. 最初の列のチェックボックスをオンにして、ダイナミックブロックをルールに関連付けます。

   ![カタログ価格ルール – 関連するダイナミック ブロック](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save and Continue Edit]**.

## 手順 5：ルールのスケジュール

{{ee-feature}}

>[!NOTE]
>
>ルールをアクティブに設定するには、スケジュールされた更新として追加する必要があります。 詳しくは、 [スケジュールされた変更](price-rule-catalog-scheduled-changes.md).

1. が含まれる _スケジュールされた変更_ ボックス、クリック **[!UICONTROL Schedule New Update]** ボックスの上部）。

   ルールに既存のスケジュールされた更新がある場合は、 **[!UICONTROL View/Edit]** リストされた変更の右側。

   既存の更新を編集するか、カタログ価格ルールを別のキャンペーンに割り当てることができます。 この **既存の更新を編集** オプションはデフォルトで選択されています。

1. ルールをスケジュールするには、 **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** 価格ルールがアクティブであること。

   日付を入力するか、から日付を選択できます。 _カレンダー_ （![カレンダーアイコン](../assets/icon-calendar.png)）に設定します。

   ![カタログ価格ルール – スケジュールの更新](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.

1. が含まれる _ルール情報_ セクションで、 **[!UICONTROL Status]** 対象： `active`.

## 手順 6：ルールを保存してテストする

1. 完了したら、ルールを保存します。

   - ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）クリック **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）クリック **[!UICONTROL Save]**.

     ルール情報ページのスケジュールされた変更には、更新されたタイムラインが表示されます。

     ![カタログ価格ルール – 予定された変更](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. ルールのプロパティを更新します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）クリック **[!UICONTROL Edit]** を表示するには _[!UICONTROL Rule Information]_ページ。

   - ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）リスト内のルールをクリックすると、 _[!UICONTROL Rule Information]_ページ。

1. ルールをテストして、正しく動作することを確認します。

   価格ルールは他のシステムルールと共に毎晩自動的に処理されます。 価格ルールを作成する場合は、ルールをテストする前に、ルールがシステムに入り、正しく機能することを確認するのに十分な時間を確保します。 新しいルールが追加されると、Commerceは価格と優先度をそれに応じて再計算します。

## カタログ価格ルールのデモ

カタログ価格ルールの作成については、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12)

## フィールドの説明

### [!UICONTROL Rule Information]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Rule name] | （必須） ルールの名前は内部参照用です。 |
| [!UICONTROL Description] | ルールの説明には、ルールの目的と使用方法を含める必要があります。 |
| [!UICONTROL Websites] | （必須） ルールを使用できる web サイトを識別します。 |
| [!UICONTROL Customer Groups] | （必須）ルールが適用される顧客グループを識別します。 |
| [!UICONTROL Priority] | このルールの優先度を他のルールと比較して示す数値。 優先順位が最も高いのは数値 1 です。 |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）ルールがストア内でアクティブかどうかを判断します。 オプション： `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）価格ルールが有効になる最初の日を指定します。 空白のままにすると、価格ルールは保存時に有効になります。 |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）価格ルールが有効になる最終日を指定します。 空白のままにすると、価格ルールは無期限に継続されます。 |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

カタログ価格ルールが実行される前に満たす必要がある条件を指定します。 空白の場合、ルールはすべての製品に適用されます。

### [!UICONTROL Actions]

| フィールド | 説明 |
|-----|-----------|
| [!UICONTROL Apply] | 購入に適用される計算のタイプを決定します。 オプション： <br/>**[!UICONTROL Apply as percentage of original]**– 通常価格のパーセンテージを差し引いて品目を値引きします。<br/>**[!UICONTROL Apply as fixed amount]**  – 通常価格から固定金額を引いて品目を値引きします。 <br/>**[!UICONTROL Adjust final price to this percentage]**– 最終価格を通常価格に対するパーセンテージで調整します。<br/>**[!UICONTROL Adjust final price to discount value]**  – 最終価格を固定の割引額に設定します。 <br/><br/>**_注意：_**通常価格は、高度な価格（特別/階層/グループ）やプロモーションの割引がない基本製品価格を指します。 最終価格とは、買い物かごに表示される割引価格を指します。 <br/>この**_final _**製品価格は次のように計算されます**_minimum _**次の算式を使用した関連価格 <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | （必須）提供される割引の金額。 |
| [!UICONTROL Discard Subsequent Rules] | この購入に追加ルールを適用できるかどうかを決定します。 同じ購入に複数の割引が適用されないようにするには、次を選択します `Yes`. オプション： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

いずれかを識別 [ダイナミック ブロック](../content-design/dynamic-blocks.md) ルールに関連付けられている。
