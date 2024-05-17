---
title: メディアデータベースの使用
description: メディアデータベースを使用してを保存する方法を説明します [!DNL Commerce] メディア ファイル。
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# メディアデータベースの使用

>[!IMPORTANT]
>
>Adobe CommerceおよびMagento Open Source 2.4.3 以降、データベースメディアのストレージ方式は非推奨（廃止予定）になりました。

デフォルトでは、のすべての画像、コンパイル済みの CSS ファイル、コンパイル済みの JavaScript ファイル（ [!DNL Commerce] インスタンスは、web サーバー上のファイルシステムに保存されます。 データベース・サーバ上のデータベースに、これらのファイルを格納するように選択できます。 このアプローチの利点の 1 つは、Web サーバーファイルシステムとデータベースの間の自動同期と逆同期のオプションです。 デフォルトのデータベースを使用して、メディアを保存したり作成したりできます。 新しく作成したデータベースをメディアストレージとして使用できるようにするには、データベースに関する情報とアクセス資格情報をに追加する必要があります `env.php` ファイル。

## データベースワークフロー

1. **ブラウザーはメディアをリクエストします** - ストアのページが顧客のブラウザーで開かれ、ブラウザーはHTMLで指定されたメディアをリクエストします。

1. **ファイルシステム内のメディアが検索されます** - ファイルシステム内のメディアが検索され、見つかった場合は、ブラウザーに渡されます。

1. **システムがデータベース内のメディアを検索** - メディアがファイル・システム内に見つからない場合、メディアの要求が構成で指定されたデータベースに送信されます。

1. **システムがデータベース内のメディアを検索** - PHP スクリプトは、データベースからファイルシステムにファイルを転送し、顧客のブラウザーに送信します。 メディアトリガーに対するブラウザーリクエストは、次のようにスクリプトを実行します。

   - Web サーバーの場合 [書き換え](../merchandising-promotions/url-rewrite.md) は次に対して有効になっています： [!DNL Commerce] サーバでサポートされ、要求されたメディアがファイルシステム内に見つからない場合にのみ PHP スクリプトが実行されます。
   - Web サーバーの書き換えが無効になっている場合 [!DNL Commerce]サーバーでサポートされていない場合でも、必要なメディアがファイルシステム内で使用可能であっても、PHP スクリプトは実行されます。

## メディアストレージにデータベースを使用

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. 左上隅にを設定します **[!UICONTROL Store View]** 対象： `Default Config` をクリックして、グローバルレベルで設定を適用します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Storage Configuration for Media]** を選択し、次の操作を実行します。

   ![詳細設定 – メディアのストレージ設定](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Media Storage]** 対象： `Database`.

   - を設定 **[!UICONTROL Select Media Database]** を使用するデータベースに追加します。

   - 既存のメディアを新しく選択したデータベースに転送するには、 **[!UICONTROL Synchronize]**.

   - を入力 **[!UICONTROL Environment Update Time]** （秒）。

1. 完了したら、 **[!UICONTROL Save Config]**.
