---
title: セールスドキュメント
description: コマースストアの顧客の注文と達成をサポートするようにセールスドキュメントを設定する方法を説明します。
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# セールスドキュメント

注文ワークフローをサポートし、顧客が送信した注文に関するドキュメントを提供するには、ストアのブランドを反映するように関連する販売ドキュメントを設定し、参照情報を含めます。

## 請求書および梱包明細の構成

ストアフロントページで使用されるロゴ画像とは異なり、PDF請求書や他の販売ドキュメントのロゴは、高解像度の 300 dpi の画像にすることができます。 ロゴのサイズを変更する際は、縦横比を保持するように注意してください。 ロゴを高さに合うようにサイズ変更し、右側の未使用のスペースを気にしないようにします。

![サンプルロゴ](./assets/logo-pdf.png){width="200"}

必要なサイズに合わせてロゴのサイズを変更する方法の 1 つは、正しいサイズの新しい空白の画像を作成する方法です。 次に、ロゴイメージを貼り付け、高さに合わせてサイズを変更します。 ほとんどの画像編集プログラムでは、縦横比を維持するためにパーセンテージで拡大・縮小するか、Shift キーを押しながら手動で画像のサイズを変更することができます。

**_ロゴを更新するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Invoice and Packing Slip Design]** 」セクションで次の操作を実行します。

   ![販売構成 — 販売請求書および梱包明細の設計](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - 次の手順で **[!UICONTROL Logo for PDF Print-outs]**&#x200B;をクリックし、 **[!UICONTROL Choose File]**&#x200B;をクリックし、作成したロゴを探して、 **[!UICONTROL Open]**.

   - 次の手順で **[!UICONTROL Logo for HTML Print View]**&#x200B;をクリックし、 **[!UICONTROL Choose File]**&#x200B;をクリックし、作成したロゴを探して、 **[!UICONTROL Open]**.

   - 請求書および梱包明細に表示する住所を入力します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

   参照用に、アップロードされた画像のサムネールが各フィールドの前に表示されます。 サムネールがゆがんで表示されても、心配する必要はありません。 ロゴの比率は請求書に正しい。

### 画像の置換

1. クリック **[!UICONTROL Choose File]** 別のロゴファイルを選択します。

1. を選択します。 **[!UICONTROL Delete Image]** チェックボックスをオンにします。

1. クリック **[!UICONTROL Save Config]**.

### 画像形式

| 形式 | 要件 |
|--- |------------------------------------------|
| **_PDF_** |  |
| ファイル形式 | JPG(JPEG)、PNG、TIF(TIFF) |
| 画像サイズ | 幅 1,080 ピクセル、高さ 270 ピクセルまで |
| 解決策 | 300 DPI を推奨 |
| **_HTML_** |  |
| ファイル形式 | JPG(JPEG)、PNG、GIF |
| 画像サイズ | テーマ別に決定されます。 |
| 解決策 | 72 または 96 DPI |

{style="table-layout:auto"}

## 参照 ID を追加

注文 ID と顧客 IP アドレスは、注文に付随する販売ドキュメントのヘッダーに含めることができます。 デフォルトでは、注文 ID と顧客 IP アドレスの両方が請求書のヘッダー、出荷梱包明細およびクレジットメモに表示されます。

![セールス構成 —PDFの印刷アウト](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_注文 ID の設定を変更するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL PDF Print-outs]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **請求書** 」セクションに入力します。

1. 設定 **[!UICONTROL Display Order ID in Header]** 好みに応じて

1. 次に対して繰り返します。 **[!UICONTROL Shipment]** および **[!UICONTROL Credit Memo]** セクション。

1. 完了したら、「 **[!UICONTROL Save Config]**.

**_顧客の IP アドレス設定を変更するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL General]** 」セクションに入力します。

   ![セールス構成 — 一般的なセールス設定](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Hide Customer IP]** を選択します。

1. 完了したら、「 **[!UICONTROL Save Config]**.
