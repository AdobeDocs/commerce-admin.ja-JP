---
title: 配送ラベルの設定
description: 配送ラベルを生成するためのストアを設定する方法を説明します。
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# 配送ラベルの設定

ラベルの印刷に使用する各通信事業者の設定で、製品レベルで次の設定をおこなう必要があります。 ラベルを印刷するには、すべての通信事業者がアカウントを開く必要があります。 次に、使用する通信事業者ごとに、ストアで設定を完了します。

## 通信事業者の要件

| [!UICONTROL Carrier] | 要件 |
|-------|--------|
| [USPS](usps.md) | 配送ラベルの郵送用に USPS アカウントが必要です。 |
| [UPS](ups.md) | UPS アカウントが必要です。 配送ラベルは、米国以外の店舗では米国固有の資格情報が必要な配送に対してのみ使用できます。 |
| [FedEx](fedex.md) | FedEx アカウントが必要です。 米国以外の店舗の場合、国際配送に対してのみ配送ラベルがサポートされます。 FedEx は米国外からの国内出荷を許可していません |
| [DHL](dhl.md) | DHL アカウントが必要です。 配送ラベルは、米国発の配送に対してのみサポートされます。 |

{style="table-layout:auto"}

## 手順 1：製造国を確認する

USPS および FedEx により国際出荷されるすべての製品には製造国が必要です。 更新が必要な製品が多数ある場合は、更新を [ インポート ](../systems/data-import.md) するか、在庫グリッドを使用して複数のレコードを更新できます。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 次のいずれかの方法を使用して、出荷ラベル・レコードを更新します。

### 方法 1：単一レコードの更新

1. グリッドで、更新する製品を見つけ、編集モードで開きます。

1. 必要に応じて **製造国** を更新します。

   ![ 製造国 ](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. 「**[!UICONTROL Save]**」をクリックします。

### 方法 2：複数のレコードを更新する

1. グリッドで、更新する各製品のチェックボックスを選択します。

   例えば、中国で製造されているすべての製品です。

1. **[!UICONTROL Actions]** コントロールを `Update Attributes` に設定し、**[!UICONTROL Submit]** をクリックします。

1. 「_属性を更新_」フォームで「**製造国**」フィールドを見つけ、「**変更**」チェックボックスを選択します。

1. 国を選択してください。

1. 「**[!UICONTROL Save]**」をクリックします。

## 手順 2 ストア情報の確認

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Shipping Settings]**」を選択します。

1. ![ のセクションの ](../assets/icon-display-expand.png) 展開セレクター **[!UICONTROL Origin]** を展開し、次のフィールドが入力されていることを確認します。

   - **[!UICONTROL Street Address]** – 出荷元の住所。 例えば、会社や倉庫の場所などです。 このフィールドは出荷ラベルに必須です。
   - **[!UICONTROL Street Address Line 2]** – 床や入り口など、その他の住所情報。 このフィールドの使用をお勧めします。

   ![ 接触チャネル ](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. 左パネルの「_売上_」セクションで、「**[!UICONTROL Delivery Methods]**」を選択します。

1. ![ のセクションの ](../assets/icon-display-expand.png) 展開セレクター **[!UICONTROL USPS]** を展開し、次のフィールドが入力されていることを確認します。

   - **[!UICONTROL Secure Gateway URL]** - システムが自動的にゲートウェイ URL を入力します。
   - **[!UICONTROL Password]** - パスワードは USPS から提供され、Web サービスを通じてユーザーがシステムにアクセスできるようにします。
   - **Length、Width、Height、Girth** - パッケージのデフォルトの寸法。 これらのフィールドを表示するには、**[!UICONTROL Size]** を `Large` に設定します。

1. 「![FedEx](../assets/icon-display-expand.png)」セクションの「**拡張セレクター**」を展開し、次のフィールドに入力されていることを確認します。

   - メートル番号
   - キー
   - パスワード

   この情報は通信事業者から提供され、Web サービスを通じてシステムにアクセスするために必要です。

1. 左側のパネルで「**[!UICONTROL General]**」を展開し、その下の「**[!UICONTROL General]**」を選択します。

1. 「![ 拡張セレクター ](../assets/icon-display-expand.png)」 **[!UICONTROL Store Information]** セクションを展開し、次のフィールドが入力されていることを確認します。

   - **[!UICONTROL Store Name]** - ストアまたはストア表示の名前。
   - **[!UICONTROL Store Contact Telephone]** – 店舗または店舗表示の主要連絡先の電話番号。
   - **[!UICONTROL Country]** - ストアのベースとなる国。
   - **[!UICONTROL VAT Number]** – 店舗の付加価値税番号（該当する場合）。 （米国の店舗は不要）
   - **[!UICONTROL Store Contact Address]** – 店舗または店舗表示の主要連絡先の住所。

1. 複数のストアがあり、連絡先情報がデフォルトと異なる場合は、それぞれに **[!UICONTROL Store View]** を設定し、情報が完全であることを確認します。

   情報がない場合、ラベルを印刷しようとするとエラーが表示されます。

   ![ 店舗情報 ](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save Config]**」をクリックします。
