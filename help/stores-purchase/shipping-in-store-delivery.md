---
title: 店舗での配信
description: ストアの店舗内配信オプションを設定する方法を説明します。
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# 店舗での配信

店舗での配信方法を使用すると、顧客は、チェックアウト時にピックアップ場所として使用するソースを選択できます。

![チェックアウト時の店舗内配信方法](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

ストアフロントのチェックアウト時：

1. 顧客がクリックする **[!UICONTROL Pick In Store]** またはを選択します。 _[!UICONTROL In-Store Pickup Delivery]_発送方法。
1. The _[!UICONTROL Pick In Store]_「チェックアウト」タブが開きます。

顧客が住所を持っている場合、または以前に配送先住所フォームに入力してから _[!UICONTROL Pick In Store]_タブ：

- 設定された半径内で顧客アドレスに最も近いソースは、自動的に受け取り用ストアとして事前に選択されます。
- 顧客が **[!UICONTROL Select Other]**、 _[!UICONTROL Select Store]_検索フォームが開きます。 事前に選択したストアまでの設定された距離（半径）内のストアのみがリストに表示されます。 リスト内のすべての店舗は、事前に選択された店舗までの距離で並べ替えられます。
- 顧客が検索フィールドに郵便番号や市区町村名を入力すると、検索した場所までの設定された距離（半径）内の店舗のみがリストに表示されます。 リスト内のすべての店舗は、検索された場所までの距離で並べ替えられます。
- 顧客が検索フィールドから郵便番号または市区町村名をクリアすると、買い物かごの商品に割り当てられている受け取り店舗がすべて顧客に表示されます。 リスト内のすべての店舗は、距離（半径）の制限なしで、ソースコードの昇順で並べ替えられます。

顧客が住所を持っていない場合、または以前に配送先住所フォームに入力していない場合は、 _[!UICONTROL Pick In Store]_タブ：

- ページに _入手可能な情報に基づいてピックアップの場所を事前に選択できませんでした_ メッセージ。
- 顧客が **[!UICONTROL Select Store]**、 _[!UICONTROL Select Store]_検索フォームが開きます。
- 買い物かご内の商品に割り当てられた受け取り店舗は、距離（半径）の制限なしに、ソースコードの昇順で表示されます。
- 顧客が検索フィールドに郵便番号や市区町村名を入力すると、検索した場所までの設定された距離（半径）内の店舗のみがリストに表示されます。 リスト内のすべての店舗は、検索された場所までの距離で並べ替えられます。

## 設定前

- デフォルト以外の在庫とソースがあることを確認します。 ソースをピックアップの場所として設定する方法について詳しくは、 [ソースを追加](../inventory-management/sources-add.md).
- 距離優先度アルゴリズムが設定されていることを確認します。 詳しくは、 [距離優先アルゴリズムを設定する](../inventory-management/distance-priority-algorithm.md).
- 次の条件を満たしていることを確認します。 [ダウンロード済みおよびインポート済み](../inventory-management/cli.md#import-geocodes) オフラインでの計算に必要なすべてのジオコード。
- が設定されていることを確認します。 [デフォルトの税金宛先の計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 設定。

>[!IMPORTANT]
>
>**ストアフロントでは、検索結果が距離（半径）でフィルタリングされ、関連する結果が表示されます。**<br><br>
>顧客が配送先住所を持っている場合、距離（半径）を計算する基準位置は配送先住所から取得されます。<br><br>
>顧客が配送先住所を持っていない場合、距離を計算する基準位置は、 [デフォルトの税金宛先の計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 設定。 これらの設定は、店舗表示ごとに設定され、受け取り店舗の検索が正しく機能するように、「デフォルトの税金宛先の計算」設定を構成する必要があります。

## ストア内配信の設定

まず、ストア内配信が有効になっていることを確認します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Delivery Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL In-Store Delivery]** 」セクションに入力します。

   ![店内配信](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled]** から `Yes`.

   >[!NOTE]
   >
   >必要に応じて、 **[!UICONTROL Use system value]** チェックボックスを使用して、任意のフィールドのデフォルトを変更できます。

1. 次を入力します。 **[!UICONTROL Method Name]** これは、出荷見積もりの作成に使用される計算方法を説明します。

   方法名は、買い物かご内の計算済み推定レートの横に表示されます。

1. 次を入力します。 **[!UICONTROL Title]** に対して表示する _ストア内配信_ セクションをチェックアウト中にクリックします。

   デフォルトのタイトルはです。 `In-Store Pickup Delivery`.

1. 店頭受取サービスの顧客に対して料金を請求するには、 **[!UICONTROL Price]** フィールドに入力します。

1. 次を入力します。 **[!UICONTROL Search Radius]** 店舗のチェックアウトでの店舗ピックアップ場所の検索（キロメートル）。

1. の場合 **[!UICONTROL Displayed Error Message]**」に値を入力する場合は、ストア内配信が使用できなくなった場合に表示されるメッセージを入力します。

   デフォルトのメッセージは、 `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. クリック **[!UICONTROL Save Config]**.
