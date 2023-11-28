---
title: コンテンツ配信ネットワークを使用する
description: コンテンツ配信ネットワーク (CDN) を使用してメディアファイルを保存する方法について説明します。
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# コンテンツ配信ネットワークを使用する

コンテンツ配信ネットワーク (CDN) を使用して、メディアファイルを保存できます。 Adobe Commerce on cloud infrastructure には Fastly CDN が含まれます ( [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) （内） _Commerce on Cloud Infrastructure ガイド_) をクリックします。 インストールされているコマースインスタンス _オンプレミス_ には、特定の CDN との統合は含まれていないので、任意の CDN を使用できます。

CDN を設定した後、管理者から設定を完了する必要があります。 変更は、グローバルレベルまたは Web サイトレベルでおこなうことができます。 CDN をメディアストレージに使用すると、コマースストアページ上のメディアへのすべてのパスが、設定で指定された CDN パスに変更されます。

## CDN ワークフロー

1. **ブラウザーがメディアをリクエストします**  — お客様のブラウザーでストアのページが開き、HTMLーがそのストアで指定されたメディアをリクエストします。
1. **CDN に送信されたリクエスト。見つかった画像と提供された画像**  — リクエストが最初に CDN に送信されます。 CDN のストレージに画像が含まれている場合、メディアファイルは顧客のブラウザーに提供されます。
1. **メディアが見つかりません。リクエストの送信先： [!DNL Commerce] web サーバー** - CDN にメディアファイルがない場合、リクエストは [!DNL Commerce] Web サーバー。 メディアファイルがファイルシステムに存在する場合、Web サーバはそれらをお客様のブラウザに送信します。

>[!IMPORTANT]
>
>セキュリティ上の理由から、CDN をメディアストレージとして使用する場合、CDN がサブドメインの外部にあると JavaScript が正しく機能しないことがあります。

## コンテンツ配信ネットワークの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Web]**.

1. 左上隅で、 **[!UICONTROL Store View]** 必要に応じて。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Base URLs]** 」セクションで次の操作を実行します。

   ![一般設定 — Web ベース URL](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - を更新します。 **[!UICONTROL Base URL for Static View Files]** と、静的ビューファイルが格納される CDN 上の場所の URL。

   - を更新します。 **[!UICONTROL Base URL for User Media Files]** を、CDN 上の JavaScript ファイルの URL に置き換えます。

     これらのフィールドは、空白のままにすることも、プレースホルダーで始めることもできます。 `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Base URLs (Secure)]** 」セクションで次の操作を実行します。

   ![一般設定 — Web ベース URL （セキュア）](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - を更新します。 **[!UICONTROL Secure Base URL for Static View Files]** と、静的ビューファイルが格納される CDN 上の場所の URL。

   - を更新します。 **[!UICONTROL Secure Base URL for User Media Files]** を、CDN 上の JavaScript ファイルの URL に置き換えます。

     これらのフィールドは、空白のままにすることも、プレースホルダーで始めることもできます。 `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. 完了したら、「 **[!UICONTROL Save Config]**.
