---
title: 店舗での配信
description: ストア用にストア内配信オプションを設定する方法を説明します。
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# 店舗での配信

店舗内配送方式では、お客様はチェックアウト時に集荷場所として使用するソースを選択できます。

![チェックアウト時の店舗内配信方法](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

ストアフロントのチェックアウト中：

1. 顧客のクリック数 **[!UICONTROL Pick In Store]** または、 _[!UICONTROL In-Store Pickup Delivery]_発送方法。
1. この _[!UICONTROL Pick In Store]_「チェックアウト」タブが開きます。

顧客が住所を持っている場合、または切り替える前に出荷先住所フォームに以前に入力した場合 _[!UICONTROL Pick In Store]_タブ：

- 設定された RADIUS 内の顧客アドレスに最も近いソースは、ピックアップストアとして自動的に事前に選択されます。
- 顧客がをクリックした場合 **[!UICONTROL Select Other]**, _[!UICONTROL Select Store]_検索フォームが開きます。 事前に選択されたストアまでの設定済みの距離（半径）内のストアのみがリストに表示されます。 リスト内のすべてのストアは、事前に選択されたストアまでの距離で並べ替えられます。
- 顧客が検索フィールドに郵便番号または都市名を入力すると、設定された距離（半径）内の店舗のみが検索された場所に表示されます。 リスト内のすべてのストアは、検索した場所までの距離で並べ替えられます。
- 顧客が検索フィールドから郵便番号または市区町村名をクリアすると、買い物かごの商品に割り当てられているすべての集荷店舗が顧客に表示されます。 リスト内のすべてのストアは、距離（半径）の制限なしで、ソースコードの昇順で並べ替えられます。

お客様が住所を持っていない、または以前に配送先住所フォームを入力していなかったために、 _[!UICONTROL Pick In Store]_タブ：

- このページには、 _利用可能な情報に基づいて集荷場所を事前に選択できませんでした_ メッセージ。
- 顧客がをクリックした場合 **[!UICONTROL Select Store]**, _[!UICONTROL Select Store]_検索フォームが開きます。
- 買い物かごの商品に割り当てられたすべての集荷店舗は、距離（半径）の制限なしに、ソースコードの昇順で表示されます。
- 顧客が検索フィールドに郵便番号または都市名を入力すると、設定された距離（半径）内の店舗のみが検索された場所に表示されます。 リスト内のすべてのストアは、検索した場所までの距離で並べ替えられます。

## セットアップの前に

- デフォルト以外の在庫とソースがあることを確認します。 ソースをピックアップ場所として設定する方法の詳細については、を参照してください。 [ソースを追加](../inventory-management/sources-add.md).
- Distance Priority Algorithm が設定されていることを確認します。 詳しくは、を参照してください [距離優先アルゴリズムの設定](../inventory-management/distance-priority-algorithm.md).
- 次が揃っていることを確認します [ダウンロードしてインポート済み](../inventory-management/cli.md#import-geocodes) オフライン計算に必要なすべてのジオコード。
- が設定されていることを確認します。 [デフォルト税金宛先計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 設定。

>[!IMPORTANT]
>
>**ストアフロントでは、検索結果が距離（半径）でフィルタリングされ、関連する結果が表示されます。**<br><br>
>顧客が配送先住所を持っている場合、距離（半径）を計算するためのベース位置は配送先住所から取得されます。<br><br>
>顧客が配送先住所を持っていない場合、距離を計算するためのベースとなる場所は [デフォルト税金宛先計算](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 設定。 これらの設定はストア表示ごとに設定されます。受け取りストア検索が正しく機能するように、デフォルトの税宛先計算設定を設定する必要があります。

## 店舗での配信を設定

まず、店舗での配信が有効になっていることを確認します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Delivery Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL In-Store Delivery]** セクション。

   ![店舗での配信](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enabled]** 対象： `Yes`.

   >[!NOTE]
   >
   >必要に応じて、 **[!UICONTROL Use system value]** チェックボックスをオンにして、任意のフィールドのデフォルトを変更します。

1. を入力 **[!UICONTROL Method Name]** 出荷見積の作成に使用する計算方法を示します。

   メソッド名は、計算された推定レートの横に買い物かごに表示されます。

1. を入力 **[!UICONTROL Title]** 自分が出演したい _店舗での配信_ チェックアウト中にセクションに移動します。

   デフォルトのタイトルはです。 `In-Store Pickup Delivery`.

1. 店舗での集荷サービスの料金を顧客に請求するには、手数料を **[!UICONTROL Price]** フィールド。

1. を入力 **[!UICONTROL Search Radius]** 店舗のピックアップ場所のキロメートルでストアフロントチェックアウトで検索します。

1. の場合 **[!UICONTROL Displayed Error Message]**&#x200B;で、ストア内配信が使用できなくなった場合に表示されるメッセージを入力します。

   デフォルトのメッセージはです。 `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. クリック **[!UICONTROL Save Config]**.
