---
title: '[!UICONTROL My Requisition Lists]'
description: アカウントダッシュボードで利用できる購買依頼リストのカスタマーエクスペリエンスについて説明します。
exl-id: ed1b41aa-9c36-49f8-80f2-ad0eb151b7a5
feature: B2B, Companies
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!UICONTROL My Requisition Lists]

購買依頼リストを維持する主な理由は、製品の再発注を容易にすることです。 認証済みの顧客は、品目を買い物かごに追加することで購買依頼リストから品目を簡単に並べ替え、リスト間で品目を移動またはコピーできます。

![&#x200B; 自分の購買依頼リスト &#x200B;](./assets/account-dashboard-my-requisition-lists.png){width="700" zoomable="yes"}

## 購買依頼リストをオープンします。

1. 顧客は、アカウントダッシュボードから **[!UICONTROL My Requisition Lists]** を選択します。

1. 開く購買依頼リストを検索し、**[!UICONTROL View]** をクリックして次のいずれかを実行します。

### 商品を買い物かごに追加

1. お客様は次のいずれかの操作を行って、追加する製品を選択します。

   - 各項目のチェックボックスを選択します。
   - **[!UICONTROL Select All]** をクリックします。

1. カートに追加する **[!UICONTROL Qty]** を入力します。

1. 製品オプションを変更するには、次の操作を行います。

   - 行項目で、_編集_ （![&#x200B; 鉛筆アイコン &#x200B;](../assets/icon-edit-pencil.png)） アイコンをクリックします。
   - 必要なオプションを変更します。
   - **[!UICONTROL Update Requisition List]** をクリックします。

1. **[!UICONTROL Add to Cart]** をクリックします。

   ![&#x200B; 購買依頼リスト詳細 &#x200B;](./assets/requisition-list-view.png){width="700" zoomable="yes"}

### 別のリストに項目をコピー

1. 顧客は、移動する各項目のチェックボックスを選択します。

1. **[!UICONTROL Copy Selected]** をクリックして、次のいずれかの操作を行います。

   - 既存の購買依頼リストを選択します。
   - **[!UICONTROL Create New Requisition List]** をクリックします。

### リストのエクスポート

1. 顧客が、エクスポートする購買依頼リストをオープンします。

1. **[!UICONTROL Export]** リンクをクリックします。

Adobe Commerceは、`sku` 値と `qty` 値を含む CSV リストを生成してダウンロードします。

### 項目を別のリストに移動

1. 顧客は、移動する各項目のチェックボックスを選択します。

1. **[!UICONTROL Move Selected]** をクリックし、次のいずれかの操作を行います。

   - 既存の購買依頼リストを選択します。
   - **[!UICONTROL Create New Requisition List]** をクリックします。

### リストの印刷

1. リストの右上隅にある「**[!UICONTROL Print]**」をクリックします。

1. 出力デバイスを検証し、**[!UICONTROL Print]** をクリックします。

   ![&#x200B; 購買依頼表の印刷 &#x200B;](./assets/requisition-list-print.png){width="500" zoomable="yes"}

### 製品オプションを編集

リストの製品オプションを編集するには、顧客が次の操作を行います。

1. _鉛筆_ （![&#x200B; 鉛筆アイコン &#x200B;](../assets/icon-edit-pencil.png)）アイコンをクリックして、製品ページを開きます。

1. 必要なオプションを変更します。

1. **[!UICONTROL Update Requisition List]** をクリックします。

   ![&#x200B; 購買依頼一覧の更新 &#x200B;](./assets/requisition-list-update.png){width="700" zoomable="yes"}

購買依頼リスト内の製品は、次の場合に編集できます。

- 商品に **[!UICONTROL all options set]** が設定されている（購入リストの [&#x200B; 設定済み商品 &#x200B;](../catalog/product-create-configurable.md) の場合）。

  製品は **[!UICONTROL added to this Requisition List]** です。

- 製品は [&#x200B; オプション付きのシンプルな製品 &#x200B;](../catalog/settings-advanced-custom-options.md) です

- 商品タイプは編集が許可されています。

### 項目を削除

1. 顧客は、削除する各項目のチェックボックスを選択します。

1. **[!UICONTROL Remove Selected]** をクリックします。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL Delete]**」をクリックします。

### リストの名前の変更

1. リストのタイトルの後、顧客は「**[!UICONTROL Rename]**」をクリックします。

1. 別の **[!UICONTROL Requisition List Name]** を入力します。

1. **[!UICONTROL Save]** をクリックします。

   ![&#x200B; 購買依頼リストの名前変更 &#x200B;](./assets/requisition-list-rename.png){width="300"}


### 購買依頼リストの削除

1. 顧客が、削除する購買依頼リストをオープンします。

1. **[!UICONTROL Delete Requisition List]** をクリックします。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL Delete]**」をクリックします。

>[!NOTE]
>
>このアクションは取り消しできません。

## アクション

| アクション | 説明 |
|--- |--- |
| [!UICONTROL Rename] | 購買依頼リストの名前を変更し、摘要を更新できます。 |
| [!UICONTROL Export] | 要求リストを CSV ファイルにエクスポートします。 |
| [!UICONTROL Print] | 現在の購買依頼リストを印刷します。 |
| [!UICONTROL Select] | アクションの対象となる項目の選択を管理します。 <br/>**[!UICONTROL Select All]**– 購買依頼リスト内のすべての品目を選択します。<br/>**[!UICONTROL Remove Selected]** – 選択したすべての品目を購買依頼リストから削除します。 <br/>**[!UICONTROL Copy Selected]**– 選択したすべての品目を別の購買依頼リストにコピーします。 |
| [!UICONTROL Add to Cart] | 選択したアイテムを買い物かごに追加します。 |
| [!UICONTROL Update List] | 小計を再計算して数量の変更を反映します。 |
| [!UICONTROL Delete Requisition List] | 会社ユーザーのアカウントから要求リストを削除します。 |

{style="table-layout:auto"}
