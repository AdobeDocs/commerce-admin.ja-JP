---
title: ギフトカード商品
description: 受信者の顧客がチェックアウト時に交換する一意のコードを生成するギフトカード製品を作成する方法を説明します。
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# ギフトカード商品

{{ee-feature}}

各ギフトカードには固有のコードがあり、チェックアウト時に 1 人の顧客のみが引き換えることができます。 A [コードプール](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool) ギフトカードを販売する前に、を設定する必要があります。 詳しくは、 [ギフトカードのワークフロー](../stores-purchase/product-gift-card-workflow.md) 買い物かごでのギフトカードの引き換え方法に関する情報を参照してください。

![ギフトカード商品ページ](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

ギフトカード製品には次の 3 種類があります。

- **仮想**  — 仮想ギフトカードが受信者の E メールアドレスに送信されます。これは、ギフトカードの購入時に必要です。 配送先住所は不要です。

- **物理**  — 物理的なギフトカードは、ギフトカードの購入時に必要な受信者の住所に発送されます。

- **組み合わせ**  — 組み合わせギフトカードが発送され、受信者に電子メールで送信されます。 ギフトカードを購入する際には、受信者の E メールおよび配送先住所が必要です。

## ギフトカード商品の作成

以下の手順は、 [製品テンプレート](attribute-sets.md)、必須フィールドおよび基本設定。 各必須フィールドには赤いアスタリスク (`*`) をクリックします。 基本事項を完了したら、必要に応じて、他の製品設定を完了できます。

### 手順 1：製品タイプの選択

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 右上の _[!UICONTROL Add Product]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"}  ) メニューで、「 」を選択します。**[!UICONTROL Gift Card]**.

   ![ギフトカードを追加](./assets/product-add-gift-card.png){width="700" zoomable="yes"}

### 手順 2：属性セットの選択

デフォルトの `Gift Card` 属性セットを選択するか、別の属性を選択します。 製品のテンプレートとして使用する属性セットを選択するには、次のいずれかの操作を行います。

- をクリックします。 **[!UICONTROL Attribute Set]** フィールドに値を入力し、属性セットの名前のすべてまたは一部を入力します。

- 表示されたリストで、使用する属性セットを選択します。

![属性セットを選択](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### 手順 3：必要な設定を完了する

1. を入力します。 **[!UICONTROL Product Name]** ギフトカードに。

   また、名前にギフトカードのタイプを指定することもできます。 例： _Luma 仮想ギフトカード_.

1. を入力します。 **[!UICONTROL SKU]** 製品の。

   デフォルトでは、製品名がデフォルトの SKU として使用されています。

1. 設定 **[!UICONTROL Card Type]** を次のいずれかに変更します。

   - `Virtual`  — 仮想ギフトカードは E メールで受信者に配信されます。
   - `Physical` ・物理ギフトカードは事前に量産でき、ユニークなコードでエンボス加工が可能。
   - `Combined`  — 組み合わせギフトカードは、仮想ギフトカードと物理ギフトカードの両方の特性を持ちます。

   ![ギフトカードのタイプ](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. 顧客に固定金額の選択肢を提供するには、 **[!UICONTROL Add Amount]** カードの最初の固定値を小数で入力します。

   固定金額の選択を入力するには、それぞれに対してこの手順を繰り返します。

1. お客様にギフトカードの価値を設定できるようにするには、次の手順を実行します。

   - 設定 **[!UICONTROL Open Amount]** から `Yes`.

   - 許容可能な最小値と最大値の範囲を定義するには、 **[!UICONTROL Open Amount From]** および **[!UICONTROL To]** 値。

   固定価格、開封額価格、またはその両方を使用してギフトカードを作成できます。

   ![ギフトカードの金額](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### 手順 4：基本設定の完了

1. 現物または組み合わせのギフトカードの場合は、 **[!UICONTROL Quantity]** 在庫数。

1. 発送するギフトカードの場合は、 **[!UICONTROL Weight]** を含める必要があります。

1. Adobe Analytics の **[!UICONTROL Categories]** 「 」フィールドで「 」を選択します。 `Gift Card`.

製品を説明する個々の属性が追加される場合があります。 選択は属性セットを変え、後で完了できます。

### 手順 5：ギフトカード情報の入力

The _[!UICONTROL Gift Card Information]_製品設定のセクションを使用して、 [ギフトカードの設定](../configuration-reference/sales/gift-cards.md) カードの管理方法を決定する設定です。

1. 下にスクロールして、 _[!UICONTROL Gift Card Information]_」セクションに入力します。

   このセクションのデフォルト設定は、システム構成によって決まります。

   ![ギフトカード情報](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. ギフトカードの機能に応じて、追加のフィールドを変更します。

   - **[!UICONTROL Treat Balance as Store Credit]**  — ギフトカードの所有者が残高を店舗クレジットとして引き換えることができるかどうかを決定します。

   - **[!UICONTROL Lifetime (days)]**  — 購入後、ギフトカードの有効期限が切れるまでの日数を決定します。 カードの有効期間の制限を設定しない場合は、このフィールドを空白のままにします。

   - **[!UICONTROL Allow Message]**  — ギフトカードの購入者が受信者へのメッセージを入力できるかどうかを指定します。 仮想（電子メール）ギフトカードと、物理的（発送済み）ギフトカードの両方にギフトメッセージを含めることができます。

   - **[!UICONTROL Email Template]**  — ギフトカードの受信者に送信される通知に使用する電子メールテンプレートを決定します。

### 手順 6：製品情報の入力

必要に応じて、次のセクションの情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイト内の製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

### 手順 7：製品の公開

1. カタログに商品を公開する準備が整ったら、 **製品を有効にする** に切り替える `Yes`.

1. 次のいずれかの操作を行います。

   **メソッド 1:** 保存してプレビュー

   - 右上隅で、 **[!UICONTROL Save]**.

   - ストアで製品を表示するには、 **[!UICONTROL Customer View]** の _管理者_ ( ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ) メニュー

   ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **方法 2:** 保存して閉じる

   次の日： _[!UICONTROL Save]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューで、「 」を選択します。**[!UICONTROL Save & Close]**.

## 覚えておくべきこと

- A _コードプール_ の一意の数を生成してから、ギフトカードを販売用に提供する必要があります。

- ギフトカードは `Redeemable` または `Non-Redeemable`.

- 税金は **_適用されていません_** ギフトカードの購入中にギフトカードを購入する。 税金は、購入したギフトカードを製品の購入に使用した場合にのみ、製品に適用されます。

- ギフトカードの有効期間は、無制限にすることも、指定した日数に設定することもできます。

- ギフトカードの価値は、一定額に設定することも、最小額と最大額の開封額に設定することもできる。

- 顧客のギフトカードのアカウントは、注文が行われたとき、または請求書の時点で作成できます。
