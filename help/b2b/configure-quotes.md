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

一般的な [B2B 機能 &#x200B;](enable-basic-features.md) で引用符が有効になっている場合は、管理者で引用符のサポートを設定できます。 見積もり設定では、見積もりリクエストに必要な最小注文額、見積もりの有効期間、添付ファイルでサポートされるファイル形式を決定します。

>[!NOTE]
>
>見積の構成オプションおよび見積ネゴシエーション機能の使用機能は、[&#x200B; ロール・リソース &#x200B;](../systems/permissions-user-roles.md#role-resources) を使用して制御されます。 これらのロール リソースは、管理者ユーザーアカウントに割り当てられている管理者ユーザーロールに対して選択する必要があります。 管理者で引用機能へのアクセス権を付与するには、**[!UICONTROL System]**/_[!UICONTROL Permissions]_/**[!UICONTROL User Roles]**&#x200B;に移動し、役割を選択して、_ 役割リソース _ツリーの [!UICONTROL Sales]/[!UICONTROL Operations]/[!UICONTROL Quotes] に移動します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Quotes]**」を選択します。

1. **[!UICONTROL General]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; 販売見積の構成 – 一般 &#x200B;](./assets/quotes-general.png){width="700" zoomable="yes"}

   [&#x200B; 設定リファレンス &#x200B;](../configuration-reference/sales/quotes.md) の _Quotes_ を参照して、Quotes 機能のオプションとその機能の完全なリストを確認してください。

   - 見積依頼を送信する前に満たす必要がある **[!UICONTROL Minimum Amount]** を買い物かごに入力します。

   - **[!UICONTROL Minimum Amount Message]**：買い物かごの合計が最低必要金額を満たさない場合に表示するメッセージを入力します。

   - **[!UICONTROL Default Expiration Period]** の場合は、引用符を有効にしておく必要がある **[!UICONTROL days]**、**[!UICONTROL weeks]**、**[!UICONTROL months]** の数を入力します。

1. **[!UICONTROL Attached files]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - **[!UICONTROL File formats for upload]**：引用符に添付するファイルのサポート対象となる各ファイル タイプのサフィックスを入力します。

     各ファイルのサフィックスを小文字で入力し、コンマで区切ります。

     デフォルトでは、`doc`、`docx`、`xls`、`xlsx`、`pdf`、`txt`、`jpg`、`png` および `jpeg` の形式がサポートされています

   - **[!UICONTROL Maximum file size]**：添付ファイルの最大サイズをメガバイト単位で入力します。

     入力した値は、サーバー設定によって上書きされる場合があります。

     ![&#x200B; 販売見積の構成 – 添付ファイル &#x200B;](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
