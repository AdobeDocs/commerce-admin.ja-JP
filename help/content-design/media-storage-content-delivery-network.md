---
title: コンテンツ配信ネットワークの利用
description: コンテンツ配信ネットワーク（CDN）を使用してメディアファイルを保存する方法を説明します。
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/c-Aw3S5unZlMdDG1k080D4CIMcILglNa4ymZxPt6HBk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# コンテンツ配信ネットワークの利用

コンテンツ配信ネットワーク（CDN）を使用して、メディアファイルを保存できます。 Adobe Commerce on Cloud Infrastructureには、Fastly CDNが含まれています（_Commerce on Cloud Infrastructure ガイド_&#x200B;の[Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html)を参照）。 オンプレミス _にインストールされているCommerce インスタンスには、特定のCDNとの統合が含まれていません。任意のCDNを使用できます。_

CDNを設定したら、管理者から設定を完了する必要があります。 変更は、グローバルレベルでもweb サイトレベルでも実行できます。 CDNをメディアストレージに使用すると、Commerce ストアページ上のメディアへのすべてのパスが、設定で指定されたCDN パスに変更されます。

## CDN ワークフロー

1. **Browser requests media** - ストアのページがお客様のブラウザーで開き、ブラウザーがHTMLで指定されたメディアをリクエストします。
1. **リクエストがCDNに送信されました。画像が見つかり、提供されました** – 最初にCDNにリクエストが送信されます。 CDNに画像がストレージ内にある場合は、メディアファイルをお客様のブラウザに配信します。
1. **メディアが見つかりません。リクエストは[!DNL Commerce] web サーバー**&#x200B;に送信されました – CDNにメディアファイルがない場合、リクエストは[!DNL Commerce] web サーバーに送信されます。 メディアファイルがファイルシステム内に見つかった場合、web サーバーはメディアファイルをお客様のブラウザーに送信します。

>[!IMPORTANT]
>
>セキュリティ上、CDNをメディアストレージとして使用する場合、CDNがサブドメインの外部にある場合、JavaScriptが正しく機能しないことがあります。

## コンテンツ配信ネットワークの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左側のパネルで、**[!UICONTROL Web]**&#x200B;を選択します。

1. 左上隅で、必要に応じて&#x200B;**[!UICONTROL Store View]**&#x200B;を設定します。

1. **[!UICONTROL Base URLs]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![一般設定 – web ベース URL](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - 静的ビューファイルが保存されているCDN上の場所のURLを使用して、**[!UICONTROL Base URL for Static View Files]**&#x200B;を更新します。

   - CDNのJavaScript ファイルのURLを使用して、**[!UICONTROL Base URL for User Media Files]**&#x200B;を更新します。

     これらのフィールドは両方とも空白のままにするか、プレースホルダーで始めることができます：`{% raw %}{{unsecure_base_url}}{% endraw %}`

1. **[!UICONTROL Base URLs (Secure)]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![一般設定 – web ベース URL （セキュア） &#x200B;](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - 静的ビューファイルが保存されているCDN上の場所のURLを使用して、**[!UICONTROL Secure Base URL for Static View Files]**&#x200B;を更新します。

   - CDNのJavaScript ファイルのURLを使用して、**[!UICONTROL Secure Base URL for User Media Files]**&#x200B;を更新します。

     これらのフィールドは両方とも空白のままにするか、プレースホルダーで始めることができます：`{% raw %}{{unsecure_base_url}}{% endraw %}`

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
