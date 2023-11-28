---
title: 発送ラベルを設定
description: 配送ラベルを生成するためのストアの設定方法を説明します。
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# 発送ラベルを設定

次の設定は、製品レベルで、ラベルの印刷に使用される各キャリアの設定で行う必要があります。 ラベルを印刷するには、すべての通信事業者がアカウントを開く必要があります。 次に、使用する予定の各通信事業者に対して、ストアの設定を完了します。

## 通信事業者の要件

| [!UICONTROL Carrier] | 要件 |
|-------|--------|
| [USPS](usps.md) | USPS アカウントが必要です。 2018 年 2 月 23 日現在、USPS は送料を含むすべての送料ラベルを要求しています。 |
| [UPS](ups.md) | UPS アカウントが必要です。 送料ラベルは、米国以外の店舗に対して米国固有の資格情報が必要な出荷に対してのみ使用できます。 |
| [FedEx](fedex.md) | FedEx アカウントが必要です。 米国以外の店舗では、海外発送の場合のみ、発送ラベルがサポートされます。 FedEx は、米国以外からの国内出荷を許可していません |
| [DHL](dhl.md) | DHL アカウントが必要です。 発送ラベルは、米国からの出荷に対してのみサポートされます。 |

{style="table-layout:auto"}

## 手順 1：製造国を確認する

製造国は、USPS と FedEx が国際的に出荷するすべての製品に必要です。 更新が必要な製品が多数ある場合は、次のいずれかを実行できます。 [インポート](../systems/data-import.md) 複数のレコードを更新する場合は、在庫グリッドを使用します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 次のいずれかの方法を使用して、発送ラベルレコードを更新します。

### 方法 1：単一レコードを更新する

1. グリッドで、更新する製品を探し、編集モードで開きます。

1. を更新します。 **製造国** 必要に応じて。

   ![製造国](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.

### 方法 2：複数のレコードを更新する

1. グリッドで、更新する各製品のチェックボックスを選択します。

   例えば、中国で製造されたすべての製品。

1. を設定します。 **[!UICONTROL Actions]** ～を制御する `Update Attributes` をクリックします。 **[!UICONTROL Submit]**.

1. Adobe Analytics の _属性を更新_ フォーム、 **製造国** フィールドに値を入力し、 **変更** チェックボックス。

1. 国を選択します。

1. クリック **[!UICONTROL Save]**.

## 手順 2 ストア情報の確認

{{beta2-updates}}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Shipping Settings]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Origin]** セクションで、以下のフィールドが完了していることを確認します。

   - **[!UICONTROL Street Address]**  — 出荷元の住所。 例えば、会社やウェアハウスの場所です。 このフィールドは、発送用ラベルに必須です。
   - **[!UICONTROL Street Address Line 2]**  — 追加の住所情報（フロアや玄関など）。 このフィールドの使用をお勧めします。

   ![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Adobe Analytics の _セールス_ セクションの左側のパネルで、「 」を選択します。 **[!UICONTROL Delivery Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL USPS]** セクションで、以下のフィールドが完了していることを確認します。

   - **[!UICONTROL Secure Gateway URL]**  — ゲートウェイ URL が自動的に入力されます。
   - **[!UICONTROL Password]**  — パスワードは USPS から提供され、Web サービスを通じてシステムにアクセスできます。
   - **長さ、幅、高さ、周囲**  — パッケージのデフォルトのサイズ。 これらのフィールドを表示するには、 **[!UICONTROL Size]** から `Large`.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **FedEx** セクションで、次のフィールドが完了していることを確認します。

   - メートル番号
   - キー
   - パスワード

   この情報は通信事業者が提供し、Web サービスを通じてシステムにアクセスするために必要です。

1. 左側のパネルで、を展開します。 **[!UICONTROL General]** を選択します。 **[!UICONTROL General]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Store Information]** セクションで、次のフィールドが完了していることを確認します。

   - **[!UICONTROL Store Name]**  — ストアまたはストア表示の名前。
   - **[!UICONTROL Store Contact Telephone]**  — 店舗または店舗表示の主要連絡先の電話番号。
   - **[!UICONTROL Country]**  — ストアの基準となる国。
   - **[!UICONTROL VAT Number]**  — 該当する場合は、店舗の付加価値税番号。 （米国に拠点を置く店舗では不要）
   - **[!UICONTROL Store Contact Address]**  — 店舗または店舗表示の主要連絡先の住所。

1. 複数の店舗があり、連絡先情報がデフォルトと異なる場合は、 **[!UICONTROL Store View]** を設定し、情報が完了していることを確認します。

   情報が見つからない場合は、ラベルを印刷しようとするとエラーが表示されます。

   ![ストア情報](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.
