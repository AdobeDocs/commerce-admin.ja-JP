---
title: 顧客グループ
description: 顧客グループを使用して、グループに割り当てられた顧客と、そのグループに関連付けられている税区分に使用可能な割引を決定します。
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: c2fd228311a4b990be9c1409d2cdd2b5677fe2af
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# 顧客グループ

顧客グループによって、使用可能な割引と、そのグループに関連付けられている税区分が決定されます。 デフォルトの顧客グループは次のとおりです `General`, `Not Logged In`、および `Wholesale`.

![顧客グループ](assets/customer-groups.png){width="700" zoomable="yes"}

## をフィルター [!UICONTROL Customer Groups] list

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. クリック **[!UICONTROL Filters]**.

1. ID、グループ、税区分の範囲など、グループを検索する基準を入力します。

   ![フィルターオプション](assets/groups-filters.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Apply Filters]**.

## 顧客グループの作成

>[!NOTE]
>
>管理者ユーザーは、すべての web サイトにアクセスできない（「カスタム」の役割が割り当てられている） [!UICONTROL Role Scope]）を使用して、顧客グループを作成、変更または削除することはできません。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. クリック **[!UICONTROL Add New Customer Group]**.

1. の場合 [!DNL **Group Name]**に、グループを識別するための一意の名前を 32 文字未満で入力します。

1. 「」を選択します **[!UICONTROL Tax Class]** これはグループに適用されます。

   ![グループ情報](assets/group-information.png){width="600" zoomable="yes"}

1. 「」を選択します **[!UICONTROL Excluded Website(s)]** グループから除外する顧客。

   >[!IMPORTANT]
   >
   >Web サイトを除外すると、除外された web サイトのインデックスが作成されなくなるので、製品価格とカタログルールのインデックス作成時間が短縮される可能性があります。 顧客グループを保存して web サイトの除外を追加すると、製品価格、カタログルールおよびカタログ検索インデックスが無効になります。 製品、web サイトおよび顧客グループが多数ある場合は、顧客グループから web サイトを除外するまで再インデックス処理を一時停止することをお勧めします。

   デフォルトで除外される web サイトはありません。 複数の値を選択するには、を押したままにします _Ctrl_ キー（PC）または _コマンド_ キー（Mac）を押し、各オプションをクリックします。

1. 完了したら、 **[!UICONTROL Save Customer Group]**.

## 顧客グループの編集

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. レコードを編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、 **[!UICONTROL Save Customer Group]**.

## 顧客を別のグループに割り当てる

>[!NOTE]
>
>会社グループを変更した後、会社のユーザーはログアウトしてストアフロントにログインして、カタログに新しい価格を表示する必要があります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. リストで顧客を見つけ、最初の列のチェックボックスを選択します。

1. を **アクション** コントロール先 `Assign a Customer Group` メニューからグループを選択します。

   ![顧客グループの割り当て](assets/group-assign.png){width="600" zoomable="yes"}

1. 確認を求められたら、 **OK**.

## 顧客グループと特定の割引を関連付けます

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _プロモーション_ > **[!UICONTROL Cart Price Rules]**.

1. 適用された割引にグループを関連付ける買い物かご価格ルールを選択します。または、 [価格ルールの作成](../merchandising-promotions/price-rules-catalog.md).

1. ルールを適用する顧客グループを選択します。

   ![顧客グループと特定値引](assets/group-discount.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.

>[!NOTE]
>
> また、Advance pricing を使用して、顧客グループに製品割引を適用することもできます。 参照： [高度な価格設定](../catalog/product-price-group.md).

## 顧客グループの削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. レコードを編集モードで開きます。

1. ボタン バーで、をクリックします **[!UICONTROL Delete Customer Group]**.

1. 確認を求められたら、 **OK**.

## 顧客グループのデモ

このデモを見て、顧客グループを作成する方法を学びます。

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
