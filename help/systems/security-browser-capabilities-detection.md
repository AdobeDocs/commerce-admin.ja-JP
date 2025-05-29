---
title: ブラウザー機能の検出
description: ブラウザー機能の検出を設定し、顧客のブラウザー設定を変更する必要がある場合に通知を表示する方法を説明します。
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# ブラウザー機能の検出

インターネット上のほとんどの web サイトやアプリケーションと同様に、Adobe CommerceおよびMagento Open Sourceでは、訪問者のブラウザーが完全な操作のために Cookie とJavaScriptの両方を許可する必要があります。 ただし、ユーザーのブラウザーが、Cookie とJavaScriptの両方を防ぐ最高のプライバシー設定に設定されている場合があります。 ストアを設定して、各訪問者のブラウザーの機能をテストし、設定の変更が必要な場合は通知を表示することができます。

- ブラウザーのプライバシー設定で Cookie が許可されていない場合は、システムが自動的に [Cookie を有効にする ](../content-design/pages.md#enable-cookies) ページにリダイレクトするように設定できます。このページでは、ほとんどのブラウザーで推奨設定を行う方法を説明します。
- ブラウザーのプライバシー設定によってJavaScriptが許可されていない場合は、すべてのページのヘッダーの上に次のメッセージが表示されるようにシステムを設定できます。

技術情報については、_インストールガイド_ の [ サポートされているブラウザー ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=ja#supported-browsers) を参照してください。

## ブラウザー機能の検出の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下にある左側のパネルで、「**[!UICONTROL Web]**」を選択します。

1. **[!UICONTROL Browser Capabilities Detection]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - Cookie を許可するようにブラウザーを設定する方法を説明する手順を表示するには、**[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** を `Yes` に設定します。

   - ユーザーのブラウザーでJavaScriptが無効になっているときにヘッダーの上にバナーを表示するには、**[!UICONTROL Show Notice if JavaScript is Disabled]** を `Yes` に設定します。

   - ユーザーのブラウザーでローカルストレージが無効になっているときにヘッダーの上にバナーを表示するには、**[!UICONTROL Show Notice if Local Storage is Disabled]** を `Yes` に設定します。

   ![ 一般設定 – web ブラウザー機能の検出 ](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
