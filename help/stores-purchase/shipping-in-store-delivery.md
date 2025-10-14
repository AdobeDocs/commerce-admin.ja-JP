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

![&#x200B; チェックアウト時の店舗内配送方法 &#x200B;](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

ストアフロントのチェックアウト中：

1. 顧客が **[!UICONTROL Pick In Store]** をクリックするか、_[!UICONTROL In-Store Pickup Delivery]_&#x200B;の配送方法を選択します。
1. _[!UICONTROL Pick In Store]_&#x200B;チェックアウトタブが開きます。

顧客が住所を持っている場合、または _[!UICONTROL Pick In Store]_&#x200B;のタブに切り替える前に出荷先住所フォームに以前に入力した場合：

- 設定された RADIUS 内の顧客アドレスに最も近いソースは、ピックアップストアとして自動的に事前に選択されます。
- 顧客が「**[!UICONTROL Select Other]**」をクリックすると、_[!UICONTROL Select Store]_&#x200B;検索フォームが開きます。 事前に選択されたストアまでの設定済みの距離（半径）内のストアのみがリストに表示されます。 リスト内のすべてのストアは、事前に選択されたストアまでの距離で並べ替えられます。
- 顧客が検索フィールドに郵便番号または都市名を入力すると、設定された距離（半径）内の店舗のみが検索された場所に表示されます。 リスト内のすべてのストアは、検索した場所までの距離で並べ替えられます。
- 顧客が検索フィールドから郵便番号または市区町村名をクリアすると、買い物かごの商品に割り当てられているすべての集荷店舗が顧客に表示されます。 リスト内のすべてのストアは、距離（半径）の制限なしで、ソースコードの昇順で並べ替えられます。

お客様が住所を持っていない場合、または _[!UICONTROL Pick In Store]_&#x200B;のタブに切り替える前に出荷先住所フォームに記入していなかった場合：

- ページには、「_利用可能な情報に基づいてピックアップの場所を事前に選択できませんでした_ というメッセージが表示されます。
- 顧客が「**[!UICONTROL Select Store]**」をクリックすると、_[!UICONTROL Select Store]_&#x200B;検索フォームが開きます。
- 買い物かごの商品に割り当てられたすべての集荷店舗は、距離（半径）の制限なしに、ソースコードの昇順で表示されます。
- 顧客が検索フィールドに郵便番号または都市名を入力すると、設定された距離（半径）内の店舗のみが検索された場所に表示されます。 リスト内のすべてのストアは、検索した場所までの距離で並べ替えられます。

## セットアップの前に

- デフォルト以外の在庫とソースがあることを確認します。 ソースをピックアップ場所として構成する方法の詳細については、「[&#x200B; ソースを追加 &#x200B;](../inventory-management/sources-add.md)」を参照してください。
- Distance Priority Algorithm が設定されていることを確認します。 詳細については、「[&#x200B; 距離優先アルゴリズムの設定 &#x200B;](../inventory-management/distance-priority-algorithm.md)」を参照してください。
- オフライン計算に必要なすべてのジオコードが [&#x200B; ダウンロードおよび読み込み &#x200B;](../inventory-management/cli.md#import-geocodes) されていることを確認します。
- [&#x200B; デフォルトの税金宛先計算 &#x200B;](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 設定が完了していることを確認します。

>[!IMPORTANT]
>
>**ストアフロントでは、検索結果が距離（半径）でフィルタリングされ、関連する結果が表示されます。**<br><br>
>顧客が配送先住所を持っている場合、距離（半径）を計算するベースとなる場所は配送先住所から取得されます。<br><br>
>顧客に配送先住所がない場合、距離を計算するためのベース位置は、「[&#x200B; デフォルトの納税先の計算 &#x200B;](../configuration-reference/sales/tax.md#default-tax-destination-calculation)」設定から取得されます。 これらの設定はストア表示ごとに設定されます。受け取りストア検索が正しく機能するように、デフォルトの税宛先計算設定を設定する必要があります。

## 店舗での配信を設定

まず、店舗での配信が有効になっていることを確認します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Delivery Methods]**」を選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL In-Store Delivery]**」セクションを展開します。

   ![&#x200B; 店舗での配信 &#x200B;](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enabled]** を `Yes` に設定します。

   >[!NOTE]
   >
   >必要に応じて、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、任意のフィールドのデフォルトを変更します。

1. 出荷見積の生成に使用する計算方法を説明する **[!UICONTROL Method Name]** を入力します。

   メソッド名は、計算された推定レートの横に買い物かごに表示されます。

1. チェックアウト時に _店舗での配信_ セクションに表示する **[!UICONTROL Title]** を入力します。

   デフォルトのタイトルは `In-Store Pickup Delivery` です。

1. 店舗での集荷サービスの料金を請求するには、**[!UICONTROL Price]** のフィールドに料金を入力します。

1. 店舗前のチェックアウト時に、店舗集荷場所の検索 **[!UICONTROL Search Radius]** をキロメートル単位で入力します。

1. **[!UICONTROL Displayed Error Message]**：店舗での配信が利用できなくなった場合に表示されるメッセージを入力します。

   デフォルトのメッセージは `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. 「**[!UICONTROL Save Config]**」をクリックします。
