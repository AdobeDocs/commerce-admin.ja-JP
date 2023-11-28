---
title: ブラウザー機能の検出
description: ブラウザー機能の検出を設定し、顧客のブラウザー設定を変更する必要がある場合に通知を表示する方法を説明します。
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# ブラウザー機能の検出

インターネット上のほとんどの Web サイトやアプリケーションと同様に、Adobe CommerceやMagento Open Sourceでは、訪問者のブラウザーで cookie と JavaScript の両方を使用して完全な操作を許可する必要があります。 ただし、ユーザーのブラウザーが、cookie と JavaScript の両方を禁止する最も高いプライバシー設定に設定されている場合があります。 ストアは、各訪問者のブラウザーの機能をテストし、設定を変更する必要がある場合に通知を表示するように設定できます。

- ブラウザーのプライバシー設定で cookie が許可されていない場合、自動的に [Cookie の有効化](../content-design/pages.md#enable-cookies) ページを参照してください。このページでは、ほとんどのブラウザーで推奨設定をおこなう方法について説明しています。
- ブラウザーのプライバシー設定で JavaScript が許可されていない場合は、各ページのヘッダーの上に次のメッセージが表示されるようにシステムを設定できます。

技術情報については、 [サポートされているブラウザー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) （内） _インストールガイド_.

## ブラウザー機能の検出を設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルの下に _[!UICONTROL General]_を選択します。**[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Browser Capabilities Detection]** 」セクションで次の操作を実行します。

   - Cookie を許可するようにブラウザーを設定する方法を説明する手順を表示するには、 **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** から `Yes`.

   - ユーザーのブラウザーで JavaScript が無効になっている場合に、ヘッダーの上にバナーを表示するには、 **[!UICONTROL Show Notice if JavaScript is Disabled]** から `Yes`.

   - ユーザーのブラウザーでローカルストレージが無効になっている場合に、ヘッダーの上にバナーを表示するには、 **[!UICONTROL Show Notice if Local Storage is Disabled]** から `Yes`.

   ![一般的な設定 — Web ブラウザー機能の検出](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.
