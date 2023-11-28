---
title: メディアデータベースを使用
description: メディアデータベースを使用して [!DNL Commerce] メディアファイル。
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# メディアデータベースを使用

>[!IMPORTANT]
>
>データベースメディアのストレージ方法は、Adobe CommerceおよびMagento Open Source2.4.3 で廃止されました。

デフォルトでは、 [!DNL Commerce] インスタンスは、web サーバー上のファイルシステムに保存されます。 これらのファイルをデータベースサーバー上のデータベースに格納するよう選択できます。 このアプローチの利点の 1 つは、Web サーバーのファイルシステムとデータベース間の自動同期と逆同期のオプションです。 デフォルトのデータベースを使用してメディアを保存するか、作成することができます。 新しく作成したデータベースをメディアストレージとして使用するには、新しく作成したデータベースに関する情報とそのアクセス資格情報を `env.php` ファイル。

## データベースワークフロー

1. **ブラウザーがメディアをリクエストします**  — お客様のブラウザーでストアのページが開き、HTMLーがそのストアで指定されたメディアをリクエストします。

1. **システムがファイルシステム内のメディアを探します**  — システムはファイルシステム内のメディアを検索し、見つかった場合はブラウザに渡します。

1. **システムがデータベース内のメディアを検出**  — メディアがファイルシステムに見つからない場合は、構成で指定されたデータベースにメディアのリクエストが送信されます。

1. **システムがデータベース内のメディアを検出** - PHP スクリプトは、データベースからファイルシステムにファイルを転送し、お客様のブラウザに送信します。 ブラウザーは、スクリプトを実行するメディアトリガーを次のように要求します。

   - Web サーバーの場合 [書き換える](../merchandising-promotions/url-rewrite.md) は有効になっています [!DNL Commerce] サーバがサポートしている場合、PHP スクリプトは、要求されたメディアがファイルシステムに見つからない場合にのみ実行されます。
   - Web サーバーの書き換えが無効な場合 [!DNL Commerce]またはサーバでサポートされていない場合は、必要なメディアがファイルシステム内にあっても、PHP スクリプトは実行されます。

## メディアストレージ用のデータベースの使用

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 左上隅で、 **[!UICONTROL Store View]** から `Default Config` をクリックして、グローバルレベルで設定を適用します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Storage Configuration for Media]** 」セクションで次の操作を実行します。

   ![高度な構成 — メディアのストレージ構成](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Media Storage]** から `Database`.

   - 設定 **[!UICONTROL Select Media Database]** を使用するデータベースに追加します。

   - 既存のメディアを新しく選択したデータベースに転送するには、 **[!UICONTROL Synchronize]**.

   - 次を入力します。 **[!UICONTROL Environment Update Time]** 秒単位で指定します。

1. 完了したら、「 **[!UICONTROL Save Config]**.
