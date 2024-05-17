---
title: ブラウザー機能の検出
description: ブラウザー機能の検出を設定し、顧客のブラウザー設定を変更する必要がある場合に通知を表示する方法を説明します。
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# ブラウザー機能の検出

インターネット上のほとんどの web サイトやアプリケーションと同様に、Adobe CommerceおよびMagento Open Sourceーでは、訪問者のブラウザーが Cookie と JavaScript の両方を許可している必要があります。 ただし、ユーザーのブラウザーが、Cookie と JavaScript の両方を防ぐ最も高いプライバシー設定に設定されている場合があります。 ストアを設定して、各訪問者のブラウザーの機能をテストし、設定の変更が必要な場合は通知を表示することができます。

- ブラウザーのプライバシー設定で Cookie が許可されていない場合は、システムが自動的に Cookie をにリダイレクトするように設定できます [Cookie を有効にする](../content-design/pages.md#enable-cookies) ページでは、ほとんどのブラウザーで推奨設定を行う方法を説明しています。
- ブラウザーのプライバシー設定で JavaScript が許可されていない場合は、各ページのヘッダーの上に次のメッセージが表示されるようにシステムを設定できます。

技術情報については、を参照してください。 [サポートされているブラウザー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) が含まれる _インストールガイド_.

## ブラウザー機能の検出の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下にある左側のパネル _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Web]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Browser Capabilities Detection]** を選択し、次の操作を実行します。

   - Cookie を許可するようにブラウザーを設定する方法を説明する手順を表示するには、次のように設定します： **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** 対象： `Yes`.

   - ユーザーのブラウザーで JavaScript が無効になっているときにヘッダーの上にバナーを表示するには、次のように設定します **[!UICONTROL Show Notice if JavaScript is Disabled]** 対象： `Yes`.

   - ユーザーのブラウザーでローカルストレージが無効になっているときにヘッダーの上にバナーを表示するには、次のように設定します **[!UICONTROL Show Notice if Local Storage is Disabled]** 対象： `Yes`.

   ![一般設定 – web ブラウザー機能の検出](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.
