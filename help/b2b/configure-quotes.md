---
title: 引用符の設定
description: 見積もり依頼に必要な最低注文金額、見積もり有効期間、添付ファイルを制御する見積もり設定について説明します。
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
TQID: https://experienceleague.adobe.com/RenH7-cnfF8qVEqFQc7IPMVsIp0alug5OgvYlr5piTM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# 引用符の設定

一般的な[B2B機能](enable-basic-features.md)で引用符が有効になっている場合は、管理者で引用符のサポートを設定できます。 見積もり設定では、見積もり要求に必要な最低注文金額、見積もりの有効期間、添付ファイルでサポートされるファイル形式を決定します。

>[!NOTE]
>
>見積もり設定オプションと見積もり交渉関数を使用する機能は、[役割リソース ](../systems/permissions-user-roles.md#role-resources)を使用して制御されます。 これらのロールリソースは、管理者ユーザーアカウントに割り当てられた管理者ユーザーロールに対して選択する必要があります。 管理者の見積もり関数へのアクセス権を付与するには、**[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**に移動し、役割を選択して、_&#x200B;役割リソース _ツリーの[!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes]に移動します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Quotes]**&#x200B;を選択します。

1. **[!UICONTROL General]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![販売見積もり設定 – 一般](./assets/quotes-general.png){width="700" zoomable="yes"}

   見積もり機能オプションとその機能の完全なリストについては、_設定リファレンス_&#x200B;の[見積](../configuration-reference/sales/quotes.md)を参照してください。

   - 見積の要求を送信する前に満たす必要がある&#x200B;**[!UICONTROL Minimum Amount]**&#x200B;をショッピング カートに入力します。

   - **[!UICONTROL Minimum Amount Message]**&#x200B;の場合、ショッピングカートの合計が必要な最小金額を満たさない場合に表示するメッセージを入力します。

   - **[!UICONTROL Default Expiration Period]**&#x200B;に、引用符が有効な状態を維持する&#x200B;**[!UICONTROL days]**、**[!UICONTROL weeks]**&#x200B;または&#x200B;**[!UICONTROL months]**&#x200B;の数値を入力します。

1. **[!UICONTROL Attached files]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - **[!UICONTROL File formats for upload]**&#x200B;に対して、引用符に添付されているファイルでサポートされている各ファイル タイプのサフィックスを入力します。

     各ファイルのサフィックスを小文字で入力し、コンマで区切ります。

     デフォルトでは、次の形式がサポートされています：`doc`、`docx`、`xls`、`xlsx`、`pdf`、`txt`、`jpg`、`png`、および`jpeg`

   - **[!UICONTROL Maximum file size]**&#x200B;の場合、添付ファイルの最大サイズをメガバイト単位で入力します。

     入力した値は、サーバー設定によって上書きされる可能性があります。

     ![販売見積もり設定 – 添付ファイル ](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
