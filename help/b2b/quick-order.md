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

_クイックオーダー_ 機能を使用すると、注文する製品の製品名または SKU がわかっているお客様は、注文プロセスを数回クリックするだけで済みます。 複数の SKU を持つ注文は、手動で入力することも、クイックオーダーフォームにインポートすることもできます。 クイックオーダーは、アカウントにログインしている顧客と、ゲストが使用できます。 有効化すると、ページ上部の顧客名の横に「_クイックオーダー_」リンクが表示されます。

![ クイック注文リンク ](./assets/quick-order-link.png){width="700" zoomable="yes"}

## ストアのクイックオーダーを有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左パネルの「_[!UICONTROL General]_」セクションで、「**[!UICONTROL B2B Features]**」を選択します。

1. **[!UICONTROL Enable Quick Order]** を `Yes` に設定します。

   ![ クイック注文を有効にする ](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save Config]**」をクリックします。

1. プロンプトが表示されたら、「[ キャッシュ管理 ](../systems/cache-management.md)」をクリックし、無効なキャッシュを更新します。

## クイックオーダーのワークフロー

顧客は、次のいずれかの方法を使用して、クイックオーダー用の製品を指定できます。

### 方法 1：個々の製品を入力する

1. 顧客が **[!UICONTROL Quick Order]** リンクをクリックします。

1. SKU または製品名で製品を選択します。

   **SKU でクイック注文** を行うには、お客様が次の手順を実行します。

   - **[!UICONTROL SKU]** を入力します。

   - **[!UICONTROL Add to List]** をクリックします。

     SKU が入力ラインに表示され、製品の詳細が下に表示されます。

     ![ クイックオーダー詳細 ](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   **製品名でクイックオーダー** を行うには、顧客は次の操作を実行します。

   - **[!UICONTROL Product Name]** の最初の数文字を入力します。

     >[!NOTE]
     >
     >_Enter_ キーを使用して製品名を選択しないでください。

   - 一致する可能性のある製品のリストが表示されたら、顧客は注文する製品をクリックします。

     ![ クリックして製品名を選択 ](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. **[!UICONTROL Qty]** を入力します。

1. 次の入力行を使用して、このプロセスを必要な回数だけ繰り返します。

1. **[!UICONTROL Add to Cart]** をクリックします。

### 方法 2：複数の製品を入力する

1. **[!UICONTROL Enter Multiple SKUs]** のボックスで、お客様は次のいずれかの操作を行います。

   - 1 行に 1 つの SKU を入力

   - 同じ行にあるすべての SKU をコンマで区切り、スペースは入れずに入力します。

     ![ 複数の SKU を入力 ](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. 製品をリストに追加するには、「**[!UICONTROL Add to List]**」をクリックします。

1. リスト内の各品目の注文 **[!UICONTROL Qty]** を入力します。

   ![ クイック注文リスト ](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >製品に必要なオプションがある場合は、オプションを選択するように求められます。 買い物かごに到着して製品オプションを追加するまで待つことができます。

   ![ オプションの選択 ](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### 方法 3：製品のリストをアップロードする

1. 「_[!UICONTROL Add from File]_」セクションで、「**[!UICONTROL Download Sample]**」をクリックして注文テンプレートをダウンロードします。

   ![ ファイルから追加 ](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. ダウンロードしたファイルを開きます。

1. テンプレートを使用して、クイックオーダーリストにアップロードする製品 SKU を追加します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   ![ アップロードする SKU](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. ファイルをアップロードするには、**[!UICONTROL Choose]** をクリックし、システムからファイルを選択します。

   項目が「クイックオーダー」リストに追加されます。

1. 準備ができたら、「**[!UICONTROL Add to Cart]**」をクリックします。

お客様は、クイック注文を作成した後、通常どおりチェックアウトを進めることができます。

![ クイックオーダー ](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
