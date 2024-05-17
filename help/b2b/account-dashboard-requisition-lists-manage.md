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

![マイ購買依頼リスト](./assets/account-dashboard-my-requisition-lists.png){width="700" zoomable="yes"}

## 購買依頼リストをオープンします。

1. アカウントダッシュボードから、顧客は次のいずれかを選択します **[!UICONTROL My Requisition Lists]**.

1. 開く購買依頼リストを検索し、クリックします。 **[!UICONTROL View]** また、次のいずれかの操作をおこないます。

### 商品を買い物かごに追加

1. お客様は次のいずれかの操作を行って、追加する製品を選択します。

   - 各項目のチェックボックスを選択します。
   - クリック数 **[!UICONTROL Select All]**.

1. エントリ数： **[!UICONTROL Qty]** を買い物かごに追加しました。

1. 製品オプションを変更するには、次の操作を行います。

   - 行項目で、 _編集_ （![鉛筆アイコン](../assets/icon-edit-pencil.png)） アイコンをクリックします。
   - 必要なオプションを変更します。
   - クリック数 **[!UICONTROL Update Requisition List]**.

1. クリック数 **[!UICONTROL Add to Cart]**.

   ![購買依頼リスト詳細](./assets/requisition-list-view.png){width="700" zoomable="yes"}

### 別のリストに項目をコピー

1. 顧客は、移動する各項目のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Copy Selected]** 次のいずれかの操作を実行します。

   - 既存の購買依頼リストを選択します。
   - クリック数 **[!UICONTROL Create New Requisition List]**.

### リストのエクスポート

1. 顧客が、エクスポートする購買依頼リストをオープンします。

1. 「」をクリックします **[!UICONTROL Export]** リンク。

Adobe Commerceは、を含む CSV リストを生成してダウンロードします。 `sku` および `qty` 値。

### 項目を別のリストに移動

1. 顧客は、移動する各項目のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Move Selected]** 次のいずれかの操作を行います。

   - 既存の購買依頼リストを選択します。
   - クリック数 **[!UICONTROL Create New Requisition List]**.

### リストの印刷

1. リストの右上隅にある「」をクリックします **[!UICONTROL Print]**.

1. 出力デバイスを検証し、クリックします **[!UICONTROL Print]**.

   ![要求リストの印刷](./assets/requisition-list-print.png){width="500" zoomable="yes"}

### 製品オプションを編集

リストの製品オプションを編集するには、顧客が次の操作を行います。

1. 「」をクリックします _鉛筆_ （![鉛筆アイコン](../assets/icon-edit-pencil.png)）アイコンをクリックして製品ページを開きます。

1. 必要なオプションを変更します。

1. クリック数 **[!UICONTROL Update Requisition List]**.

   ![購買依頼リストの更新](./assets/requisition-list-update.png){width="700" zoomable="yes"}

購買依頼リスト内の製品は、次の場合に編集できます。

- 製品に含まれる **[!UICONTROL all options set]** （次の場合： [設定済みの製品](../catalog/product-create-configurable.md) 購買依頼リスト）。

  製品はです **[!UICONTROL added to this Requisition List]**.

- 製品はです [オプション付きシンプルな製品](../catalog/settings-advanced-custom-options.md)

- 商品タイプは編集が許可されています。

### 項目を削除

1. 顧客は、削除する各項目のチェックボックスを選択します。

1. クリック数 **[!UICONTROL Remove Selected]**.

1. 確認を求められたら、をクリックします **[!UICONTROL Delete]**.

### リストの名前の変更

1. リストタイトルの後、顧客は、 **[!UICONTROL Rename]**.

1. 別のユーザーを入力 **[!UICONTROL Requisition List Name]**.

1. クリック数 **[!UICONTROL Save]**.

   ![購買依頼リスト名の変更](./assets/requisition-list-rename.png){width="300"}


### 購買依頼リストの削除

1. 顧客が、削除する購買依頼リストをオープンします。

1. クリック数 **[!UICONTROL Delete Requisition List]**.

1. 確認を求められたら、をクリックします **[!UICONTROL Delete]**.

>[!NOTE]
>
>このアクションは取り消しできません。

## アクション

| アクション | 説明 |
|--- |--- |
| [!UICONTROL Rename] | 購買依頼リストの名前を変更し、摘要を更新できます。 |
| [!UICONTROL Export] | 要求リストを CSV ファイルにエクスポートします。 |
| [!UICONTROL Print] | 現在の購買依頼リストを印刷します。 |
| [!UICONTROL Select] | アクションの対象となる項目の選択を管理します。 <br/>**[!UICONTROL Select All]**– 購買依頼リストのすべての品目を選択します。<br/>**[!UICONTROL Remove Selected]**  – 選択したすべての品目を購買依頼リストから削除します。 <br/>**[!UICONTROL Copy Selected]**– 選択したすべての品目を別の購買依頼リストにコピーします。 |
| [!UICONTROL Add to Cart] | 選択したアイテムを買い物かごに追加します。 |
| [!UICONTROL Update List] | 小計を再計算して数量の変更を反映します。 |
| [!UICONTROL Delete Requisition List] | 会社ユーザーのアカウントから要求リストを削除します。 |

{style="table-layout:auto"}
