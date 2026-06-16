---
title: ブラウザー機能の検出
description: お客様のブラウザー設定を変更する必要がある場合に、ブラウザー機能の検出を設定し、通知を表示する方法について説明します。
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/zPxdplYIYblw6-tsDvxEmvKfAx-2M6opb6qjX7YL1I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 0%

---

# ブラウザー機能の検出

インターネット上のほとんどのweb サイトやアプリケーションと同様に、Adobe CommerceとMagento Open Sourceでは、訪問者のブラウザーでCookieとJavaScriptの両方が完全に動作することを許可する必要があります。 ただし、ユーザーのブラウザーがCookieとJavaScriptの両方を防ぐ最高のプライバシー設定に設定されることがあります。 ストアは、各訪問者のブラウザーの機能をテストするように設定でき、設定を変更する必要がある場合に通知を表示します。

- ブラウザーのプライバシー設定でCookieを許可しない場合は、ほとんどのブラウザーで推奨される設定を行う方法を説明する「[Cookieを有効にする](../content-design/pages.md#enable-cookies)」ページに自動的にリダイレクトするようにシステムを設定できます。
- ブラウザーのプライバシー設定でJavaScriptが許可されていない場合は、すべてのページのヘッダーの上に次のメッセージを表示するように設定できます。

技術情報については、_インストールガイド_&#x200B;の[&#x200B; サポートされているブラウザー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=ja#supported-browsers)を参照してください。

## ブラウザー機能の検出の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左側のパネルで、**[!UICONTROL Web]**&#x200B;を選択します。

1. **[!UICONTROL Browser Capabilities Detection]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - Cookieを許可するようにブラウザーを設定する方法を説明する手順を表示するには、**[!UICONTROL Redirect to CMS-page if Cookies are Disabled]**&#x200B;を`Yes`に設定します。

   - ユーザーのブラウザーでJavaScriptが無効になっている場合に、ヘッダーの上にバナーを表示するには、**[!UICONTROL Show Notice if JavaScript is Disabled]**&#x200B;を`Yes`に設定します。

   - ユーザーのブラウザーでローカルストレージが無効になっている場合に、ヘッダーの上にバナーを表示するには、**[!UICONTROL Show Notice if Local Storage is Disabled]**&#x200B;を`Yes`に設定します。

   ![一般設定 – web ブラウザー機能の検出](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
