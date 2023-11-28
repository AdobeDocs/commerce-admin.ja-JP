---
title: '[!UICONTROL My Requisition Lists]'
description: 顧客のアカウントダッシュボードで使用できる購買依頼リストの顧客体験について説明します。
exl-id: ed1b41aa-9c36-49f8-80f2-ad0eb151b7a5
feature: B2B, Companies
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!UICONTROL My Requisition Lists]

購買依頼リストを維持する主な理由は、製品の発注を容易にするためです。 承認済み顧客は、買い物かごに品目を追加して、購買依頼リストから品目を簡単に並べ替えたり、品目を別のリストに移動またはコピーしたりできます。

![自分の購買依頼リスト](./assets/account-dashboard-my-requisition-lists.png){width="700" zoomable="yes"}

## 購買依頼リストをオープンします。

1. 顧客がアカウントダッシュボードから選択する **[!UICONTROL My Requisition Lists]**.

1. オープンする購買依頼リストを検索し、クリックします。 **[!UICONTROL View]** 次のいずれかの操作を行います。

### 買い物かごに製品を追加

1. 顧客は、次のいずれかを実行して、追加する製品を選択します。

   - 各項目のチェックボックスを選択します。
   - クリック数 **[!UICONTROL Select All]**.

1. 次に入る **[!UICONTROL Qty]** を買い物かごに追加する必要があります。

1. 製品オプションを変更するには、次の操作を行います。

   - 行項目で、 _編集_ (![鉛筆アイコン](../assets/icon-edit-pencil.png)) アイコンをクリックします。
   - 必要なオプションを変更します。
   - クリック数 **[!UICONTROL Update Requisition List]**.

1. クリック数 **[!UICONTROL Add to Cart]**.

   ![購買依頼リストの詳細](./assets/requisition-list-view.png){width="700" zoomable="yes"}

### 項目を別のリストにコピーする

1. 顧客が移動する各項目のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Copy Selected]** では、次のいずれかの操作を実行します。

   - 既存の購買依頼リストを選択します。
   - クリック数 **[!UICONTROL Create New Requisition List]**.

### リストのエクスポート

1. 顧客が、エクスポートする購買依頼リストを開きます。

1. 次をクリック： **[!UICONTROL Export]** リンク。

Adobe Commerceは、 `sku` および `qty` 値。

### 項目を別のリストに移動

1. 顧客が移動する各項目のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Move Selected]** 次のいずれかの操作を行います。

   - 既存の購買依頼リストを選択します。
   - クリック数 **[!UICONTROL Create New Requisition List]**.

### リストを印刷する

1. リストの右上隅で、顧客がクリックする **[!UICONTROL Print]**.

1. 出力デバイスを検証し、「 」をクリックします。 **[!UICONTROL Print]**.

   ![購買依頼リストの印刷](./assets/requisition-list-print.png){width="500" zoomable="yes"}

### 製品オプションを編集

リスト内の製品オプションを編集するには、顧客は次の操作を行います。

1. 次をクリック： _鉛筆_ (![鉛筆アイコン](../assets/icon-edit-pencil.png)) アイコンをクリックして、製品ページを開きます。

1. 必要なオプションを変更します。

1. クリック数 **[!UICONTROL Update Requisition List]**.

   ![購買依頼リストの更新](./assets/requisition-list-update.png){width="700" zoomable="yes"}

購買依頼リスト内の製品は、次の場合に編集できます。

- 製品には **[!UICONTROL all options set]** ( [構成済み製品](../catalog/product-create-configurable.md) （「購買依頼リスト」内）。

  製品は **[!UICONTROL added to this Requisition List]**.

- 製品は [オプション付きのシンプルな製品](../catalog/settings-advanced-custom-options.md)

- 製品タイプで編集が許可されています。

### 項目を削除

1. 顧客が、削除する各項目のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Remove Selected]**.

1. 確認を求められたら、「 」をクリックします **[!UICONTROL Delete]**.

### リスト名の変更

1. リストのタイトルの後、顧客は **[!UICONTROL Rename]**.

1. 別の **[!UICONTROL Requisition List Name]**.

1. クリック数 **[!UICONTROL Save]**.

   ![購買依頼リストの名前変更](./assets/requisition-list-rename.png){width="300"}


### 購買依頼リストを削除します。

1. 顧客が、削除する購買依頼リストを開きます。

1. クリック数 **[!UICONTROL Delete Requisition List]**.

1. 確認を求められたら、「 」をクリックします **[!UICONTROL Delete]**.

>[!NOTE]
>
>この操作は元に戻せません。

## アクション

| アクション | 説明 |
|--- |--- |
| [!UICONTROL Rename] | 購買依頼リストの名前を変更し、摘要を更新できます。 |
| [!UICONTROL Export] | 購買依頼リストを CSV ファイルにエクスポートします。 |
| [!UICONTROL Print] | 現在の購買依頼リストを印刷します。 |
| [!UICONTROL Select] | アクションの対象となる項目の選択を管理します。 <br/>**[!UICONTROL Select All]**— 購買依頼リスト内のすべての品目を選択します。<br/>**[!UICONTROL Remove Selected]**  — 選択したすべての品目を購買依頼リストから削除します。 <br/>**[!UICONTROL Copy Selected]**— 選択したすべての品目を別の購買依頼リストにコピーします。 |
| [!UICONTROL Add to Cart] | 選択した項目を買い物かごに追加します。 |
| [!UICONTROL Update List] | 数量の変化を反映して小計を再計算します。 |
| [!UICONTROL Delete Requisition List] | 会社ユーザーのアカウントから購買依頼リストを削除します。 |

{style="table-layout:auto"}
