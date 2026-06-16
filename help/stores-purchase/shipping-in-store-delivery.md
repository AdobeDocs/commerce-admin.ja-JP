---
title: 実店舗での配送
description: ストアに店舗内配送オプションを設定する方法を説明します。
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/9pETzHXJvXmnJKhRbS7maASWBuMtbTbhJtCRKHekGTo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 570
ht-degree: 0%

---

# 実店舗での配送

また、実店舗での受け取り方法では、決済時に受け取り場所として使用するソースを選択することができます。

![ チェックアウト時の店舗内配達方法](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

ストアフロントのチェックアウト時に、次の操作を行います。

1. お客様は&#x200B;**[!UICONTROL Pick In Store]**&#x200B;をクリックするか、_[!UICONTROL In-Store Pickup Delivery]_の配送方法を選択します。
1. 「_[!UICONTROL Pick In Store]_チェックアウト」タブが開きます。

お客様が住所を持っている場合、または&#x200B;_[!UICONTROL Pick In Store]_タブに切り替える前に以前に配送先住所フォームに入力した場合：

- 設定された半径内の顧客アドレスに最も近いソースが、ピックアップストアとして自動的に事前選択されます。
- お客様が&#x200B;**[!UICONTROL Select Other]**&#x200B;をクリックすると、_[!UICONTROL Select Store]_検索フォームが開きます。 選択したストアまでの設定済みの距離（半径）内のストアのみがリストに表示されます。 リスト内のすべてのストアは、選択したストアまでの距離で並べ替えられます。
- お客様が検索フィールドに郵便番号または市区町村名を入力すると、検索場所までの設定距離（半径）内の店舗のみがリストに表示されます。 リスト内のすべてのストアは、検索した場所までの距離で並べ替えられます。
- 顧客が検索フィールドから郵便番号または市区町村名をクリアすると、ショッピングカート内の商品に割り当てられているすべてのピックアップストアが顧客に表示されます。 リスト内のすべてのストアは、距離（半径）の制限なしに、ソースコードの昇順で並べ替えられます。

お客様が住所を持っていない場合、または&#x200B;_[!UICONTROL Pick In Store]_タブに切り替える前に以前に配送先住所フォームに入力していない場合：

- ページに「_利用可能な情報に基づいて受け取り場所を事前選択できませんでした_」というメッセージが表示されます。
- お客様が&#x200B;**[!UICONTROL Select Store]**&#x200B;をクリックすると、_[!UICONTROL Select Store]_検索フォームが開きます。
- ショッピングカート内の商品に割り当てられたすべてのピックアップストアは、距離（半径）の制限なしに、ソースコードの昇順で表示されます。
- お客様が検索フィールドに郵便番号または市区町村名を入力すると、検索場所までの設定距離（半径）内の店舗のみがリストに表示されます。 リスト内のすべてのストアは、検索した場所までの距離で並べ替えられます。

## 設定の前

- デフォルト以外の在庫とソースがあることを確認します。 受け取り場所としてソースを設定する方法について詳しくは、[ ソースを追加](../inventory-management/sources-add.md)を参照してください。
- 距離優先アルゴリズムが設定されていることを確認します。 詳しくは、[距離優先アルゴリズムの設定](../inventory-management/distance-priority-algorithm.md)を参照してください。
- オフライン計算に必要なすべてのジオコードが[ ダウンロードおよびインポート ](../inventory-management/cli.md#import-geocodes)されていることを確認してください。
- [既定の税宛先計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation)設定が構成されていることを確認してください。

>[!IMPORTANT]
>
>**ストアフロントでは、検索結果が距離（半径）でフィルタリングされ、関連する結果が表示されます：**<br><br>
>お客様が配送先住所を持っている場合、距離（半径）を計算するベースの場所は、配送先住所から取得されます。<br><br>
>お客様が配送先住所を持っていない場合、距離を計算するベースの場所は、[既定の税宛先計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation)設定から取得されます。これらの設定はストアビューごとに設定され、ピックアップストア検索が正しく機能するように、デフォルトの税宛先計算の設定を行う必要があります。

## 実店舗配送の設定

まず、実店舗配信が有効になっていることを確認します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Delivery Methods]**&#x200B;を選択します。

1. **[!UICONTROL In-Store Delivery]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![実店舗配信](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

   >[!NOTE]
   >
   >必要に応じて、**[!UICONTROL Use system value]** チェックボックスをオフにして、任意のフィールドのデフォルトを変更します。

1. 出荷見積の作成に使用する計算方法を説明する&#x200B;**[!UICONTROL Method Name]**&#x200B;を入力します。

   メソッド名は、ショッピングカート内の計算された見積もり率の横に表示されます。

1. チェックアウト時に&#x200B;_店舗内配信_ セクションに表示する&#x200B;**[!UICONTROL Title]**&#x200B;を入力します。

   既定のタイトルは`In-Store Pickup Delivery`です。

1. 実店舗での受け取りサービスに対して顧客に請求するには、**[!UICONTROL Price]** フィールドに手数料を入力します。

1. ストアフロントのチェックアウトで店舗の受け取り場所を検索する場合は、**[!UICONTROL Search Radius]**&#x200B;をキロメートル単位で入力します。

1. **[!UICONTROL Displayed Error Message]**&#x200B;について、実店舗配信が利用できなくなった場合に表示されるメッセージを入力します。

   既定のメッセージは`In-Store Delivery is not available. To use this delivery method, please contact us.`です

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。
