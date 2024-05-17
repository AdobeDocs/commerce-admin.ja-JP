---
title: 見積の設定
description: 見積もり要求に必要な最小注文額、見積もりの有効期間、添付ファイルを制御する見積もり設定について説明します。
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 見積の設定

一般規則で引用符が有効になっている場合 [B2B の機能](enable-basic-features.md)を参照し、管理者で引用符のサポートを設定できます。 見積もり設定では、見積もりリクエストに必要な最小注文額、見積もりの有効期間、添付ファイルでサポートされるファイル形式を決定します。

>[!NOTE]
>
>見積の構成オプションおよび見積ネゴシエーション機能の使用機能は、 [役割リソース](../systems/permissions-user-roles.md#role-resources). これらのロール リソースは、管理者ユーザーアカウントに割り当てられている管理者ユーザーロールに対して選択する必要があります。 管理者で引用機能へのアクセス権を付与するには、次の場所に移動します。 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**を選択し、役割を選択して、に移動します。 [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] が含まれる_&#x200B;役割リソース&#x200B;_ツリー。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Quotes]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL General]** を選択し、次の操作を実行します。

   ![販売見積の構成 – 一般](./assets/quotes-general.png){width="700" zoomable="yes"}

   参照： [見積もり](../configuration-reference/sales/quotes.md) が含まれる _設定リファレンス_ 引用符の機能オプションとその機能の完全なリストについて説明します。

   - を入力 **[!UICONTROL Minimum Amount]** 買い物かご内で、見積もり依頼を送信する前に満たす必要がある場合。

   - の場合 **[!UICONTROL Minimum Amount Message]**、買い物かごの合計が最低必要量を満たさない場合に表示するメッセージを入力します。

   - の場合 **[!UICONTROL Default Expiration Period]**、次の数を入力 **[!UICONTROL days]**, **[!UICONTROL weeks]**、または **[!UICONTROL months]** 見積もりは有効なままです。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Attached files]** を選択し、次の操作を実行します。

   - の場合 **[!UICONTROL File formats for upload]**：引用符に添付するファイルでサポートする各ファイルタイプのサフィックスを入力します。

     各ファイルのサフィックスを小文字で入力し、コンマで区切ります。

     デフォルトでは、次の形式がサポートされています。 `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`、および `jpeg`

   - の場合 **[!UICONTROL Maximum file size]**：添付ファイルの最大サイズ（メガバイト単位）を入力します。

     入力した値は、サーバー設定によって上書きされる場合があります。

     ![販売見積の構成 – 添付ファイル](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.
