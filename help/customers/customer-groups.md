---
title: 顧客グループ
description: 顧客グループを使用して、グループに割り当てられた顧客に対して使用可能な割引と、そのグループに関連付けられた税区分を決定します。
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# 顧客グループ

顧客グループは、使用可能な割引と、グループに関連付けられている税区分を決定します。 デフォルトの顧客グループは、 `General`, `Not Logged In`、および `Wholesale`.

![顧客グループ](assets/customer-groups.png){width="700" zoomable="yes"}

## フィルター [!UICONTROL Customer Groups] リスト

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. クリック **[!UICONTROL Filters]**.

1. ID、グループ、税区分の範囲を含む、グループを検索するための条件を入力します。

   ![フィルターオプション](assets/groups-filters.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Apply Filters]**.

## 顧客グループの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. クリック **[!UICONTROL Add New Customer Group]**.

1. の場合 [!DNL **Group Name]**、グループを識別する一意の名前を 32 文字未満で入力します。

1. を選択します。 **[!UICONTROL Tax Class]** これはグループに適用されます。

   ![グループ情報](assets/group-information.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL Excluded Website(s)]** グループから除外する

   >[!IMPORTANT]
   >
   >除外された Web サイトはインデックス付けされないので、Web サイトを除外すると、製品価格やカタログルールのインデックス作成時間が短縮される可能性があります。 顧客グループを追加された Web サイトの除外と共に保存すると、製品価格、カタログルール、カタログ検索のインデックスが無効化されます。 製品、Web サイト、顧客グループが多数ある場合は、顧客グループから Web サイトを除外するまでインデックス再作成プロセスを一時停止することをお勧めします。

   デフォルトでは、Web サイトは除外されません。 複数の値を選択する場合は、 _Ctrl_ キー (PC) または _コマンド_ キー (Mac) を押し、各オプションをクリックします。

1. 完了したら、「 **[!UICONTROL Save Customer Group]**.

## 顧客グループの編集

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. レコードを編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、「 **[!UICONTROL Save Customer Group]**.

## 顧客を別のグループに割り当てる

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. リストで顧客を見つけ、最初の列のチェックボックスを選択します。

1. を設定します。 **アクション** ～を制御する `Assign a Customer Group` をクリックし、メニューからグループを選択します。

   ![顧客グループの割り当て](assets/group-assign.png){width="600" zoomable="yes"}

1. 確認するメッセージが表示されたら、「 **OK**.

## 特定の割引に顧客グループを関連付ける

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _プロモーション_ > **[!UICONTROL Cart Price Rules]**.

1. 適用された割引にグループを関連付ける買い物かごの価格ルールを選択します。または、 [価格ルールを作成する](../merchandising-promotions/price-rules-catalog.md).

1. ルールを適用する顧客グループを選択します。

   ![特定の割引に対する顧客グループ](assets/group-discount.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.

>[!NOTE]
>
> また、「Advance」の価格設定を使用して、製品の割引を顧客グループに適用することもできます。 詳しくは、 [高度な価格](../catalog/product-price-group.md).

## 顧客グループの削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. レコードを編集モードで開きます。

1. ボタンバーで、 **[!UICONTROL Delete Customer Group]**.

1. 確認するメッセージが表示されたら、「 **OK**.

## 顧客グループのデモ

次のデモを見て、顧客グループの作成について学びます。

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
