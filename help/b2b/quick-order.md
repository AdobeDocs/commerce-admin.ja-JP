---
title: クイックオーダー
description: クイック注文機能について学び、顧客のために有効にします。
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
TQID: https://experienceleague.adobe.com/iwH1JStasz7KM-ECeWAvP-x4niVm-QFg4-GMw8r3SoI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 438
ht-degree: 0%

---

# クイックオーダー

_クイックオーダー_&#x200B;機能を使用すると、注文する商品の商品名またはSKUを知っている顧客の場合、注文プロセスが数回クリックに短縮されます。 複数のSKUを持つ注文は、手動で入力するか、クイック注文フォームに読み込むことができます。 クイックオーダーは、アカウントにログインしているお客様やゲストが利用できます。 有効にすると、_クイックオーダー_ リンクがページの上部、顧客名の横に表示されます。

![&#x200B; クイック注文リンク &#x200B;](./assets/quick-order-link.png){width="700" zoomable="yes"}

## ストアのクイックオーダーを有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルの「_[!UICONTROL General]_」セクションで、「**[!UICONTROL B2B Features]**」を選択します。

1. **[!UICONTROL Enable Quick Order]**&#x200B;を`Yes`に設定します。

   ![&#x200B; クイックオーダーを有効にする](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

1. プロンプトが表示されたら、[Cache Management](../systems/cache-management.md)をクリックし、無効なキャッシュを更新します。

## クイック注文ワークフロー

顧客は、次のいずれかの方法を使用して、クイックオーダー用に商品を指定できます。

### 方法1：個々の製品を入力する

1. お客様は&#x200B;**[!UICONTROL Quick Order]** リンクをクリックします。

1. SKUまたは製品名で製品を選択します。

   SKU **による** クイック注文を行うには、お客様は次の操作を行います。

   - **[!UICONTROL SKU]**&#x200B;を入力します。

   - **[!UICONTROL Add to List]**&#x200B;をクリックします。

     SKUが入力ラインに表示され、下に商品の詳細が表示されます。

     ![&#x200B; クイック注文の詳細](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   製品名&#x200B;**で** クイック注文を行うには、お客様は次の操作を行います。

   - **[!UICONTROL Product Name]**&#x200B;の最初の数文字を入力します。

     >[!NOTE]
     >
     >_Enter_ キーを使用して製品の名前を選択しないでください。

   - 一致する可能性のある商品のリストが表示されたら、顧客は注文する商品をクリックします。

     ![&#x200B; クリックして製品名を選択](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. **[!UICONTROL Qty]**&#x200B;を入力します。

1. 次の入力ラインを使用して、このプロセスを必要な回数だけ繰り返します。

1. **[!UICONTROL Add to Cart]**&#x200B;をクリックします。

### 方法2：複数の製品を入力する

1. **[!UICONTROL Enter Multiple SKUs]** ボックスでは、お客様は次のいずれかの操作を行います。

   - 1行につき1つのSKUを入力

   - 同じ行のすべてのSKUをコンマで区切り、スペースなしで入力します。

     ![複数のSKUを入力](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. 商品をリストに追加するには、**[!UICONTROL Add to List]**&#x200B;をクリックします。

1. リスト内の各項目に対して注文する&#x200B;**[!UICONTROL Qty]**&#x200B;を入力します。

   ![&#x200B; クイック注文リスト &#x200B;](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >製品に必要なオプションがある場合、顧客はオプションを選択するように求められます。 顧客がショッピングカートに入るまで、商品オプションを追加するのを待つこともできます。

   ![&#x200B; オプションの選択](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### 方法3：製品のリストをアップロードする

1. _[!UICONTROL Add from File]_&#x200B;セクションで、**[!UICONTROL Download Sample]**&#x200B;をクリックして注文テンプレートをダウンロードします。

   ![&#x200B; ファイルから追加](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. ダウンロードしたファイルを開きます。

1. テンプレートを使用して、クイック注文リスト用にアップロードする製品SKUを追加します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   アップロードする![SKU](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. ファイルをアップロードするには、**[!UICONTROL Choose]**&#x200B;をクリックし、システムからファイルを選択します。

   項目がクイック注文リストに追加されます。

1. 準備ができたら、**[!UICONTROL Add to Cart]**&#x200B;をクリックします。

顧客がクイック注文を作成した後、通常どおりチェックアウトを進めることができます。

![&#x200B; クイックオーダー](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
