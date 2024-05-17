---
title: クイックオーダー
description: クイックオーダー機能と、顧客に対して有効にする方法を説明します。
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# クイックオーダー

この _クイック注文_ 注文する製品の製品名または SKU がわかっているお客様は、この機能を使用すると、注文プロセスを数回クリックするだけで済みます。 複数の SKU を持つ注文は、手動で入力することも、クイックオーダーフォームにインポートすることもできます。 クイックオーダーは、アカウントにログインしている顧客と、ゲストが使用できます。 有効にすると、 _クイック注文_ リンクはページ上部の顧客名の横に表示されます。

![クイック注文リンク](./assets/quick-order-link.png){width="700" zoomable="yes"}

## ストアのクイックオーダーを有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. が含まれる _[!UICONTROL General]_左側のパネルの「」セクションで、**[!UICONTROL B2B Features]**.

1. を設定 **[!UICONTROL Enable Quick Order]** 対象： `Yes`.

   ![クイックオーダーを有効にする](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、 [キャッシュ管理](../systems/cache-management.md) 無効なキャッシュを更新します。

## クイックオーダーのワークフロー

顧客は、次のいずれかの方法を使用して、クイックオーダー用の製品を指定できます。

### 方法 1：個々の製品を入力する

1. ユーザーが **[!UICONTROL Quick Order]** リンク。

1. SKU または製品名で製品を選択します。

   を配置するには **sku によるクイックオーダー**&#x200B;を使用する場合、顧客は次のことを行います。

   - エントリ数： **[!UICONTROL SKU]**.

   - クリック数 **[!UICONTROL Add to List]**.

     SKU が入力ラインに表示され、製品の詳細が下に表示されます。

     ![クイックオーダーの詳細](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   を配置するには **商品名で簡単に注文**&#x200B;を使用する場合、顧客は次のことを行います。

   - の最初の数文字を入力します **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >を使用しないでください。 _Enter_ 商品名を選択するためのキー。

   - 一致する可能性のある製品のリストが表示されたら、顧客は注文する製品をクリックします。

     ![クリックして製品名を選択](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. エントリ数： **[!UICONTROL Qty]**.

1. 次の入力行を使用して、このプロセスを必要な回数だけ繰り返します。

1. クリック数 **[!UICONTROL Add to Cart]**.

### 方法 2：複数の製品を入力する

1. が含まれる **[!UICONTROL Enter Multiple SKUs]** お客様は、次のいずれかの操作を行います。

   - 1 行に 1 つの SKU を入力

   - 同じ行にあるすべての SKU をコンマで区切り、スペースは入れずに入力します。

     ![複数の SKU を入力](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. 製品をリストに追加するには、をクリックします **[!UICONTROL Add to List]**.

1. エントリ数： **[!UICONTROL Qty]** リスト内の項目ごとに並べ替えられる。

   ![クイック注文リスト](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >製品に必要なオプションがある場合は、オプションを選択するように求められます。 買い物かごに到着して製品オプションを追加するまで待つことができます。

   ![オプションを選択](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### 方法 3：製品のリストをアップロードする

1. が含まれる _[!UICONTROL Add from File]_セクションで、をクリック&#x200B;**[!UICONTROL Download Sample]**注文テンプレートをダウンロードします。

   ![ファイルから追加](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. ダウンロードしたファイルを開きます。

1. テンプレートを使用して、クイックオーダーリストにアップロードする製品 SKU を追加します。

1. 完了したら、をクリックします **[!UICONTROL Save]**.

   ![アップロードする SKU](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. ファイルをアップロードするには、をクリックします **[!UICONTROL Choose]** システムからファイルを選択します。

   項目が「クイックオーダー」リストに追加されます。

1. 準備ができたら、クリックします **[!UICONTROL Add to Cart]**.

お客様は、クイック注文を作成した後、通常どおりチェックアウトを進めることができます。

![クイック注文](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
