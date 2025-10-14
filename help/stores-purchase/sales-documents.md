---
title: 販売ドキュメント
description: Commerce ストアに関するお客様の注文と受け渡しをサポートするための営業文書の設定方法を説明します。
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# 販売ドキュメント

注文ワークフローをサポートし、顧客が送信する注文に関するドキュメントを顧客に提供するには、関連する販売ドキュメントを設定して店舗ブランドを反映し、参照情報を含めます。

## 請求書と梱包明細の構成

店頭ページで使用されるロゴ画像とは異なり、PDF請求書やその他の営業資料のロゴは、高解像度の 300 dpi 画像にすることができます。 ロゴのサイズを変更する際は、縦横比を維持するように注意します。 ロゴのサイズを高さに合わせて変更し、右側の未使用のスペースを気にしないようにします。

![&#x200B; サンプルロゴ &#x200B;](./assets/logo-pdf.png){width="200"}

必要なサイズに合わせてロゴのサイズを変更する 1 つの方法は、正しいサイズで新しい空白の画像を作成することです。 次に、ロゴ画像を貼り付け、高さに合わせてサイズを変更します。 ほとんどの画像編集プログラムでは、縦横比を維持するために倍率をパーセント単位で変更するか、Shift キーを押しながら手動で画像のサイズを変更できます。

**_ロゴを更新するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、その下の「**[!UICONTROL Sales]**」を選択します。

1. **[!UICONTROL Invoice and Packing Slip Design]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; 販売構成 – 販売請求書および梱包明細設計 &#x200B;](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - **[!UICONTROL Logo for PDF Print-outs]** をアップロードするには、「**[!UICONTROL Choose File]**」をクリックし、用意したロゴを見つけて「**[!UICONTROL Open]**」をクリックします。

   - **[!UICONTROL Logo for HTML Print View]** をアップロードするには、「**[!UICONTROL Choose File]**」をクリックし、用意したロゴを見つけて「**[!UICONTROL Open]**」をクリックします。

   - 請求書と梱包明細に表示する住所を入力します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

   参照用に、アップロードした画像のサムネールが各フィールドの前に表示されます。 サムネールがゆがんで表示されても心配ありません。 ロゴの比率は請求書に記載されています。

### 画像を置換

1. 「**[!UICONTROL Choose File]**」をクリックし、別のロゴファイルを選択します。

1. 置き換える画像の「**[!UICONTROL Delete Image]**」チェックボックスをオンにします。

1. 「**[!UICONTROL Save Config]**」をクリックします。

### 画像形式

| 形式 | 要件 |
|--- |------------------------------------------|
| **_PDF_** |  |
| ファイル形式 | JPG（JPEG）、PNG、TIF （TIFF） |
| 画像サイズ | 幅 1,080 ピクセル、高 270 ピクセルまで |
| 解決策 | 300 DPI 推奨 |
| **_HTML_** |  |
| ファイル形式 | JPG （JPEG）, PNG, GIF |
| 画像サイズ | テーマによって決定されます。 |
| 解決策 | 72 または 96 DPI |

{style="table-layout:auto"}

## 参照 ID を追加

注文 ID と顧客 IP アドレスは、注文に伴う販売文書のヘッダーに含めることができます。 デフォルトでは、請求書、出荷梱包明細およびクレジット・メモのヘッダーに受注 ID と顧客 IP アドレスの両方が表示されます。

![&#x200B; セールス構成：PDFの印刷出力 &#x200B;](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_注文 ID の設定を変更するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL PDF Print-outs]**」を選択します。

1. ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) 「**請求書**」セクションを展開します。

1. 必要に応じて **[!UICONTROL Display Order ID in Header]** を設定します。

1. **[!UICONTROL Shipment]** セクションと **[!UICONTROL Credit Memo]** セクションで繰り返します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

**_顧客の IP アドレス設定を変更するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、その下の「**[!UICONTROL Sales]**」を選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL General]**」セクションを展開します。

   ![&#x200B; 販売設定 – 一般的な販売設定 &#x200B;](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. **[!UICONTROL Hide Customer IP]** を好みに合わせて設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
