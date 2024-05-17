---
title: ギフトカード製品
description: チェックアウト時に受信者の顧客が利用できる一意のコードを生成するギフトカード製品を作成する方法を説明します。
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: e72977596c4479d2e94b1e066ee166d22cb12405
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# ギフトカード製品

{{ee-feature}}

各ギフトカードには一意のコードがあり、チェックアウト時に 1 人のお客様のみが利用できます。 A [コードプール](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool) ギフトカードを販売する前に確立する必要があります。 参照： [ギフト カード ワークフロー](../stores-purchase/product-gift-card-workflow.md) 買い物かごでのギフト カードの引き換え方法に関する情報を表示します。

![ギフトカード製品ページ](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

ギフトカード製品には次の 3 種類があります。

- **仮想**  – 仮想ギフトカードが受信者のメールアドレスに送信されます。このアドレスは、ギフトカードの購入時に必要になります。 配送先住所は必須ではありません。

- **物理**  – 物理的なギフトカードは受取人の住所に送られます。この住所はギフトカードの購入時に必要になります。

- **組み合わせ**  – 組み合わせたギフトカードが出荷され、受信者にメールで送信されます。 ギフトカードの購入時には、受取人のメールアドレスと配送先住所が必要です。

## ギフトカード製品の作成

次の手順は、を使用してギフトカードを作成するプロセスを示しています。 [製品テンプレート](attribute-sets.md)、必須フィールド、基本設定です。 各必須フィールドには、赤いアスタリスク（`*`）に設定します。 基本を完了したら、必要に応じて他の製品設定を完了できます。

### 手順 1：製品タイプの選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. の右上隅にある _[!UICONTROL Add Product]_（ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"}  ） メニュー、を選択&#x200B;**[!UICONTROL Gift Card]**.

   ![ギフト カードの追加](./assets/product-add-gift-card.png){width="700" zoomable="yes"}

### 手順 2：属性セットの選択

デフォルトのを使用できます `Gift Card` 属性セットまたは別のものを選択します。 製品のテンプレートとして使用する属性セットを選択するには、次のいずれかの操作を行います。

- 内をクリック **[!UICONTROL Attribute Set]** フィールドに、属性セットの名前のすべてまたは一部を入力します。

- 表示されたリストで、使用する属性セットを選択します。

![属性セットを選択](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### 手順 3：必要な設定を完了する

1. を入力 **[!UICONTROL Product Name]** ギフトカード用。

   また、名前にギフトカードのタイプを指定することもできます。 例： _Luma 仮想ギフトカード_.

1. を入力 **[!UICONTROL SKU]** 商品の場合。

   デフォルトでは、製品名がデフォルトの SKU として使用されます。

1. を設定 **[!UICONTROL Card Type]** を次のいずれかに変更します。

   - `Virtual`  – 仮想ギフトカードは、メールで受信者に配信されます。
   - `Physical`  – 物理的なギフトカードは事前に大量生産され、一意のコードでエンボス加工することができます。
   - `Combined`  – 組み合わせギフトカードは、仮想と物理の両方のギフトカードの特性を持っています。

   ![ギフト カード タイプ](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. 固定金額を選択して顧客に提示するには、 **[!UICONTROL Add Amount]** カードの最初の固定値を小数で入力します。

   固定金額の選択を入力するには、それぞれについて、この手順を繰り返します。

1. お客様がギフトカードの値を設定できるようにするには、次の手順を実行します。

   - を設定 **[!UICONTROL Open Amount]** 対象： `Yes`.

   - 許容される最小値と最大値の範囲を定義するには、 **[!UICONTROL Open Amount From]** および **[!UICONTROL To]** 値。

   固定価格、オープン金額価格、またはその両方でギフト カードを作成できます。

   >[!NOTE]
   >
   >ギフトカード製品は、カタログに独自の価格がありません。 ギフトカード価格は、購入中に選択されたギフトカード金額から導出される。

   ![ギフト カードの金額](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### 手順 4：基本設定を完了する

1. 物理的なギフト カードまたは組み合わせギフト カードには、 **[!UICONTROL Quantity]** 在庫あり。

1. 出荷するギフト カードの場合は、 **[!UICONTROL Weight]** パッケージの。

1. が含まれる **[!UICONTROL Categories]** フィールド、を選択 `Gift Card`.

製品を説明する追加の個人属性が存在する場合があります。 選択によってアトリビュート セットが異なり、後で完成させることができます。

### 手順 5: ギフト カード情報を入力する

この _[!UICONTROL Gift Card Information]_製品設定のセクションは、を上書きするために使用できます [ギフトカードの設定](../configuration-reference/sales/gift-cards.md) カードの管理方法を決定する設定。

1. にスクロール ダウンします。 _[!UICONTROL Gift Card Information]_セクション。

   このセクションのデフォルト設定は、システム設定によって決まります。

   ![ギフト カード情報](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. ギフトカードの機能に応じて、追加のフィールドを変更します。

   - **[!UICONTROL Treat Balance as Store Credit]**  – 残高を店舗クレジットとしてギフト カード所有者が引き換えることができるかどうかを決定します。

   - **[!UICONTROL Lifetime (days)]**  – 購入後、ギフトカードの有効期限が切れるまでの日数を指定します。 カードの有効期限を設定しない場合は、このフィールドを空白のままにします。

   - **[!UICONTROL Allow Message]** - ギフトカードの購入者が受信者へのメッセージを入力できるかどうかを決定します。 ギフトメッセージは、仮想（電子メール）と物理（出荷済み）の両方のギフトカードに含めることができます。

   - **[!UICONTROL Email Template]** - ギフトカードの受信者に送信される通知に使用するメールテンプレートを決定します。

### 手順 6：製品情報の入力

必要に応じて、以下の節の情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイトの製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

### 手順 7：製品を公開する

1. カタログに製品を公開する準備が整ったら、 **製品を有効にする** 切り替え先 `Yes`.

1. 次のいずれかの操作を行います。

   **メソッド 1:** 保存とプレビュー

   - 右上隅のをクリックします。 **[!UICONTROL Save]**.

   - ストアで商品を表示するには、次を選択します **[!UICONTROL Customer View]** 日 _Admin_ （ ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ） メニュー、

   ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **メソッド 2:** 保存して閉じる

   日 _[!UICONTROL Save]_（ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ） メニュー、を選択&#x200B;**[!UICONTROL Save & Close]**.

## 注意事項

- A _コードプール_ ギフトカードを販売するには、一意の番号を生成する必要があります。

- ギフト カードは次のように設定できます `Redeemable` または `Non-Redeemable`.

- 税金は **_適用なし_** ギフトカード購入時にギフトカードを購入する。 税金は、購入したギフトカードが製品の購入に使用された場合にのみ適用されます。

- ギフト カードの有効期間は、無制限にすることも、指定した日数に設定することもできます。

- ギフトカードの値は、固定金額に設定することも、最小値と最大値を持つオープン金額に設定することもできます。

- ギフトカード製品は、カタログに独自の価格がありません。 ギフトカード価格は、購入中に選択されたギフトカード金額から導出される。

- 顧客のギフト カード アカウントは、注文時または請求書の時点で作成できます。
