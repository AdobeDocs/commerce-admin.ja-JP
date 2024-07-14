---
title: コンテンツ配信ネットワークの使用
description: コンテンツ配信ネットワーク（CDN）を使用してメディアファイルを保存する方法について説明します。
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# コンテンツ配信ネットワークの使用

コンテンツ配信ネットワーク（CDN）は、メディアファイルの保存に使用できます。 クラウドインフラストラクチャー上のAdobe Commerceには、Fastly CDN が含まれます（_クラウドインフラストラクチャー上のCommerce ガイドの [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) を参照_）。 _オンプレミス_ でインストールされたCommerce インスタンスには、特定の CDN との統合が含まれていません。任意の CDN を使用できます。

CDN を設定したら、管理者から設定を完了する必要があります。 変更は、グローバルレベルまたは web サイトレベルで行うことができます。 CDN がメディアストレージに使用される場合、Commerce ストアページ上のメディアへのすべてのパスは、設定で指定された CDN パスに変更されます。

## CDN ワークフロー

1. **ブラウザーがメディアをリクエスト** - ストアのページが顧客のブラウザーで開かれ、ブラウザーは、HTMLで指定されたメディアをリクエストします。
1. **リクエストは CDN に送信されます。画像が見つかり、提供されます** - リクエストは最初に CDN に送信されます。 CDN のストレージに画像が格納されている場合は、顧客のブラウザーにメディアファイルが提供されます。
1. **メディアが見つからない、[!DNL Commerce] web サーバーにリクエストが送信される** - CDN にメディアファイルがない場合、リクエストは [!DNL Commerce] web サーバーに送信されます。 メディア・ファイルがファイル・システム内で見つかった場合、Web サーバはメディア・ファイルをお客様のブラウザに送信します。

>[!IMPORTANT]
>
>セキュリティのため、CDN がメディアストレージとして使用されている場合、CDN がサブドメインの外部にある場合、JavaScriptが正しく機能しない可能性があります。

## コンテンツ配信ネットワークの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Web]**」を選択します。

1. 左上隅で、必要に応じて **[!UICONTROL Store View]** を設定します。

1. **[!UICONTROL Base URLs]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![ 一般設定 – web ベース URL](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - 静的ビューファイルが格納されている CDN 上の場所の URL で **[!UICONTROL Base URL for Static View Files]** を更新します。

   - CDN のJavaScript ファイルの URL で **[!UICONTROL Base URL for User Media Files]** を更新します。

     これらのフィールドは両方とも空白のままでも、プレースホルダーで始めることもできます（例：`{% raw %}{{unsecure_base_url}}{% endraw %}`）。

1. **[!UICONTROL Base URLs (Secure)]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![ 一般設定 – web ベース URL （セキュア） ](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - 静的ビューファイルが格納されている CDN 上の場所の URL で **[!UICONTROL Secure Base URL for Static View Files]** を更新します。

   - CDN のJavaScript ファイルの URL で **[!UICONTROL Secure Base URL for User Media Files]** を更新します。

     これらのフィールドは両方とも空白のままでも、プレースホルダーで始めることもできます（例：`{% raw %}{{unsecure_base_url}}{% endraw %}`）。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
