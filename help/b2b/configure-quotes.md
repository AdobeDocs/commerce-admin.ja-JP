---
title: 引用符の設定
description: 見積依頼の最小必要注文額、見積の有効期間、添付ファイルを制御する見積構成について説明します。
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 引用符の設定

一般 [B2B 機能](enable-basic-features.md)を使用する場合は、管理者で引用符のサポートを設定できます。 見積もりの構成によって、見積もり依頼の最小必要注文額、見積もりの有効期間、添付ファイルでサポートされるファイル形式が決まります。

>[!NOTE]
>
>見積もり構成オプションと見積もりネゴシエーション機能を使用する機能は、 [役割リソース](../systems/permissions-user-roles.md#role-resources). これらのロールリソースは、管理者ユーザーアカウントに割り当てられている管理者ユーザーロールに対して選択する必要があります。 管理者で見積もり機能へのアクセス権を付与するには、に移動します。 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**、役割を選択し、に移動します。 [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] （内）_&#x200B;役割のリソース&#x200B;_ツリー。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Quotes]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL General]** 」セクションで次の操作を実行します。

   ![販売見積もり構成 — 一般](./assets/quotes-general.png){width="700" zoomable="yes"}

   詳しくは、 [引用符](../configuration-reference/sales/quotes.md) （内） _設定リファレンス_ を参照してください。

   - 次を入力します。 **[!UICONTROL Minimum Amount]** 見積もりのリクエストを送信する前に満たす必要がある買い物かご。

   - の場合 **[!UICONTROL Minimum Amount Message]**」には、買い物かごの合計が最小必要量を満たさない場合に表示するメッセージを入力します。

   - の場合 **[!UICONTROL Default Expiration Period]**、 **[!UICONTROL days]**, **[!UICONTROL weeks]**&#x200B;または **[!UICONTROL months]** 見積もりは有効なままです。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Attached files]** 」セクションで次の操作を実行します。

   - の場合 **[!UICONTROL File formats for upload]**&#x200B;をクリックし、引用符に添付されたファイルに対してサポートする各ファイルタイプのサフィックスを入力します。

     各ファイルのサフィックスを小文字で入力し、コンマで区切ります。

     デフォルトでは、次の形式がサポートされています。 `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`、および `jpeg`

   - の場合 **[!UICONTROL Maximum file size]**&#x200B;には、添付ファイルの最大サイズをメガバイト単位で入力します。

     入力した値は、サーバー設定によって上書きされる場合があります。

     ![販売見積もり構成 — 添付ファイル](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.
