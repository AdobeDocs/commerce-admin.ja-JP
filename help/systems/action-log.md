---
title: アクションログ
description: アクションログと、ストアに加えられたすべての変更を追跡するためにログに記録されたアクションを設定する方法について説明します。
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/UtJhP452hJXDyEyjxrknuF4WPoLza-UcnuWxP6ILtq8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# アクションログ

{{ee-feature}}

アクションログ機能は、ストアで作業する管理者ユーザーが行ったすべての変更を記録（ログ）します。 これにより、ストアに加えられたすべての変更を追跡できます。 これらの変更を追跡すると、ユーザーに対する[管理者権限](permissions.md)の設定と共に、不要な変更からストアを保護するのに役立ちます。

ほとんどの管理者アクションでは、ログ情報には、アクション、ユーザーの名前、アクションの成功または失敗、アクションの影響を受けるオブジェクトのIDが含まれます。 IP アドレスと日付も記録されます。

デフォルトでは、すべての管理者アクションが有効になり、ログに記録されます。 管理者アクションのログを設定するには、オプションを確認し、各アクションタイプのチェックボックスを選択またはオフにします。 Adobe Commerceは、チェックされたタイプのみをログに記録します。

ログに記録された管理者のアクションと詳細を確認するには、[ アクションログレポート ](action-log-report.md)を表示します。

![詳細設定 – 管理者アクションのログ記録](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

構成設定の詳細なリストについては、_構成リファレンス_&#x200B;の[管理者アクション ログ アーカイブ ](../configuration-reference/advanced/system.md)を参照してください。

## ログ記録のための管理者アクションの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL Admin]**&#x200B;を選択します。

1. **[!UICONTROL Admin Actions Logging]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、アクションごとに次の操作を行います。

   - アクションの管理者ログ記録を有効にするには、チェックボックスをオンにします。
   - アクションの管理者ログ記録を無効にするには、チェックボックスをオフにします。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## 管理者のアクションログをアーカイブ

管理者のアクションログは、任意の日数アーカイブできます。 アーカイブは、指定した期間が経過した後に削除することもできます。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL System]**&#x200B;を選択します。

1. **[!UICONTROL Admin Action Log Archiving]**&#x200B;を展開し、オプションを設定します。

   - **[!UICONTROL Logs Entry Lifetime, Days]** - アーカイブされたログを保持する日数を設定します。
   - **[!UICONTROL Log Archiving Frequency]** - アーカイブを作成する頻度を設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
