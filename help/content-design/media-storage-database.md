---
title: メディアデータベースの使用
description: メディアデータベースを使用してメディアファイルを保存する方法  [!DNL Commerce]  説明します。
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# メディアデータベースの使用

>[!IMPORTANT]
>
>データベースメディアのストレージ方式は、Adobe CommerceおよびMagento Open Source 2.4.3 で非推奨（廃止予定）となりました。

デフォルトでは、[!DNL Commerce] インスタンスのすべての画像、コンパイル済み CSS ファイル、コンパイル済みJavaScript ファイルが、web サーバー上のファイルシステムに格納されます。 データベース・サーバ上のデータベースに、これらのファイルを格納するように選択できます。 このアプローチの利点の 1 つは、Web サーバーファイルシステムとデータベースの間の自動同期と逆同期のオプションです。 デフォルトのデータベースを使用して、メディアを保存したり作成したりできます。 新しく作成したデータベースをメディアストレージとして使用できるようにするには、データベースに関する情報とアクセス資格情報を `env.php` ファイルに追加する必要があります。

## データベースワークフロー

1. **ブラウザーがメディアをリクエスト** - ストアのページが顧客のブラウザーで開き、ブラウザーが、HTMLで指定されたメディアをリクエストします。

1. **ファイルシステム内のメディアが検索されます** - システムはファイルシステム内のメディアを検索し、見つかった場合はブラウザーに渡します。

1. **システムがデータベース内のメディアを検索** - メディアがファイルシステム内で見つからない場合、メディアのリクエストは、設定で指定されたデータベースに送信されます。

1. **システムがデータベース内のメディアを検索** - PHP スクリプトがデータベースからファイルシステムにファイルを転送し、顧客のブラウザーに送信します。 メディアトリガーに対するブラウザーリクエストは、次のようにスクリプトを実行します。

   - Web サーバー [rewrites](../merchandising-promotions/url-rewrite.md) が [!DNL Commerce] で有効になっており、サーバーでサポートされている場合、PHP スクリプトは、要求されたメディアがファイルシステムに見つからない場合にのみ実行されます。
   - Web サーバーの書き換えが [!DNL Commerce] で無効になっている場合、またはサーバーでサポートされていない場合は、必要なメディアがファイルシステム内にある場合でも、PHP スクリプトが実行されます。

## メディアストレージにデータベースを使用

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. 左上隅の **[!UICONTROL Store View]** を `Default Config` に設定して、グローバルレベルで設定を適用します。

1. **[!UICONTROL Storage Configuration for Media]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![ 詳細設定 – メディアのストレージ設定 ](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - **[!UICONTROL Media Storage]** を `Database` に設定します。

   - 使用するデータベースに **[!UICONTROL Select Media Database]** を設定します。

   - 既存のメディアを新しく選択したデータベースに転送するには、[**[!UICONTROL Synchronize]**] をクリックします。

   - **[!UICONTROL Environment Update Time]** を秒単位で入力します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
