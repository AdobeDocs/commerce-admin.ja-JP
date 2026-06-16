---
title: 顧客グループ
description: 顧客グループを使用して、グループに割り当てられている顧客に対して使用できる割引と、そのグループに関連付けられている税区分を決定します。
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/jbqn6jRo2Pg2fARqEyHGLLzVVG0CyuudtGXklpUCaOw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 445
ht-degree: 0%

---

# 顧客グループ

顧客グループは、使用可能な割引と、そのグループに関連付けられている税区分を決定します。 既定の顧客グループは`General`、`Not Logged In`、`Wholesale`です。

![顧客グループ &#x200B;](assets/customer-groups.png){width="700" zoomable="yes"}

## [!UICONTROL Customer Groups] リストをフィルター

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**&#x200B;に移動します。

1. **[!UICONTROL Filters]**&#x200B;をクリックします。

1. ID、グループ、税区分などの範囲を含む、グループを検索するための条件を入力します。

   ![&#x200B; フィルターオプション &#x200B;](assets/groups-filters.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Apply Filters]**&#x200B;をクリックします。

## 顧客グループの作成

>[!NOTE]
>
>すべてのWeb サイトにアクセスできない管理者ユーザー（「カスタム」 [!UICONTROL Role Scope]を持つ役割を割り当てられている）は、顧客グループを作成、変更、または削除できません。

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**&#x200B;に移動します。

1. **[!UICONTROL Add New Customer Group]**&#x200B;をクリックします。

1. [!DNL **Group Name]**&#x200B;の場合、グループを識別するには、32文字未満の一意の名前を入力してください。

1. グループに適用される&#x200B;**[!UICONTROL Tax Class]**&#x200B;を選択します。

   ![&#x200B; グループ情報](assets/group-information.png){width="600" zoomable="yes"}

1. グループから除外する&#x200B;**[!UICONTROL Excluded Website(s)]**&#x200B;を選択します。

   >[!IMPORTANT]
   >
   >除外されたweb サイトにはインデックスが作成されないため、web サイトを除外すると、製品価格とカタログルールのインデックス作成時間が短縮される可能性があります。 追加されたweb サイト除外を使用して顧客グループを保存すると、製品価格、カタログルール、カタログ検索インデックスが無効になります。 製品、web サイト、および顧客グループが多数ある場合は、顧客グループからweb サイトを除外するまで、インデックス再作成プロセスを一時停止することをお勧めします。

   デフォルトでは、Web サイトは除外されません。 複数の値を選択するには、_Ctrl_ キー（PC）または&#x200B;_Command_ キー（Mac）を押しながら、各オプションをクリックします。

1. 完了したら、**[!UICONTROL Save Customer Group]**&#x200B;をクリックします。

## 顧客グループの編集

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**&#x200B;に移動します。

1. レコードを編集モードで開きます。

1. 必要な変更を加えます。

1. 完了したら、**[!UICONTROL Save Customer Group]**&#x200B;をクリックします。

## 顧客を別のグループに割り当てる

>[!NOTE]
>
>会社グループを変更した後、会社ユーザーはログアウトしてストアフロントにログインし、カタログに新しい価格を表示する必要があります。
>お客様が会社に割り当てられた後、お客様グループは読み取り専用になり、管理者ユーザーは更新できません。

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**&#x200B;に移動します。

1. リストで顧客を見つけ、最初の列のチェックボックスを選択します。

1. **アクション** コントロールを`Assign a Customer Group`に設定し、メニューからグループを選択します。

   ![顧客グループの割り当て](assets/group-assign.png){width="600" zoomable="yes"}

1. 確認を求められたら、**OK**&#x200B;をクリックします。

## 顧客グループを特定の割引に関連付ける

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _プロモーション_ > **[!UICONTROL Cart Price Rules]**&#x200B;に移動します。

1. 適用された割引にグループを関連付けるカート価格ルールを選択するか、[価格ルールを作成](../merchandising-promotions/price-rules-catalog.md)します。

1. ルールが適用される顧客グループを選択します。

   ![お客様グループから特定の割引](assets/group-discount.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save]**&#x200B;をクリックします。

>[!NOTE]
>
> また、事前価格を利用して、顧客グループに商品割引を適用することもできます。 [詳細価格](../catalog/product-price-group.md)を参照してください。

## 顧客グループの削除

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**&#x200B;に移動します。

1. レコードを編集モードで開きます。

1. ボタンバーで、**[!UICONTROL Delete Customer Group]**&#x200B;をクリックします。

1. 確認を求められたら、**OK**&#x200B;をクリックします。

## 顧客グループのデモ

デモを見て顧客グループを作成する方法を学びましょう。

>[!VIDEO](https://video.tv.adobe.com/v/3410171/?captions=jpn&quality=12&learn=on)
