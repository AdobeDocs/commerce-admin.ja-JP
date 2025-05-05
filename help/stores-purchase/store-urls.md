---
title: URL を格納
description: ストア URL と、ベース URL およびストアコードの設定方法について説明します。
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# URL を格納

Adobe CommerceまたはMagento Open Source インストール内の各 web サイトには、ストアフロントに割り当てられたベース URL と、管理者に割り当てられた別の URL があります。 Adobeでは、変数を使用してベース URL に対する内部リンクを定義します。これにより、リンクを更新することなく、ストア全体をある場所から別の場所に移動させることができます。 標準のベース URL は `http` で始まり、セキュアなベース URL は `https` で始まります。

- **ベース URL** — `http://www.yourdomain.com/magento/`
- **セキュア ベース URL** — `https://www.yourdomain.com/magento/`
- **IP アドレスを含む URL** — `http://###.###.###.###/magento/` または `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>デフォルトのベース URL 設定から管理者 URL を変更しないでください。 管理 URL またはパスを変更するには、[ カスタム管理 URL の使用 ](#use-a-custom-admin-url) を参照してください。

## セキュアなプロトコルを使用

ストアのベース URL は、最初にAdobe Commerceのインストール時に設定されたものです。 その時点でセキュリティ証明書が使用可能であった場合は、ストア、管理者、またはその両方に使用する `HTTPS` の URL を指定できます。 Adobe Commerceのインストールに複数のストアが含まれている場合、または後でストアを追加する予定の場合は、URL にストアコードを含めることができます。 すべてのAdobeのリソースと操作は、安全なプロトコルで使用できます。

インストール時にドメインのセキュリティ証明書が使用できなかった場合は、ストアを起動する前に必ず設定を更新してください。 ドメインのセキュリティ証明書が確立されたら、暗号化された Secure Sockets Layer （SSL）および [Transport Layer Security][1] （TLS）プロトコルで動作するように、ベース URL の一方または両方を設定できます。

>[!IMPORTANT]
>
>Adobeでは、コンテンツページや製品ページを含む、実稼動サイトのすべてのページを、安全なプロトコルを使用して送信することを強くお勧めします。

Adobe CommerceとMagento Open Sourceは、デフォルトですべてのページを `HTTPS` で配信するように設定できます。 ストアが標準プロトコルで実行されている場合は、[HTTP Strict Transport Security][2] （HSTS）を有効にし、保護されていないページリクエストをアップグレードすることで、セキュリティを向上させることができます。 HSTS は、指定されたドメインの安全でないプロトコルで送信される標準 `HTTP` ページをブラウザーがレンダリングするのを防ぐオプトインプロトコルです。 検索エンジンが標準の `HTTP` URL でストアの各ページに既にインデックスを作成している可能性があるので、保護されていないページリクエストを自動的に `HTTPS` にアップグレードするようにCommerceを設定できます。これにより、トラフィックが失われなくなります。 Commerceがストアフロントと管理者の両方にセキュア URL を使用するように設定されている場合、`HSTS` を有効にできる 2 つのフィールドが追加で表示されます。

## ベース URL の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左パネルの _一般_ の下で、「**[!UICONTROL Web]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Base URL]**」セクションを展開します。

   - 「**[!UICONTROL Base URL]**」 – ストアの完全修飾ベース URL を入力します。 ストアから追加の URL キーで拡張できるように、URL の末尾には必ずスラッシュを付けてください。 例：`http://yourdomain.com/`

     >[!NOTE]
     >
     >「_[!UICONTROL Base Link URL]_」フィールドのプレースホルダーは変更しないでください。 これは、ベース URL への相対リンクの作成に使用されるプレースホルダーです。

   - **[!UICONTROL Base URL for Static View Files]** - （オプション）次のプレースホルダーで始まるパスを入力して、静的ビューファイルのベース URL の別の場所を指定します。

     \{\{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]** - （オプション）次のプレースホルダーで始まるパスを入力して、ユーザーメディアファイルのベース URL の代替の場所を指定します。

     \{\{unsecure_base_url}}

     通常のインストールでは、静的ビューファイルやメディアファイルのパスはベース URL に対する相対パスなので、更新する必要はありません。

   ![ 一般設定 – web ベース URL](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >二重中括弧で囲まれたプレースホルダーは、変数のマークアップタグです。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## セキュアなベース URL の設定

ドメインに有効なセキュリティ証明書がある場合、ストアフロントと管理者の両方の URL を設定して、安全な（https）チャネルでデータを送信できます。 有効なセキュリティ証明書がないと、ストアはセキュアな（SSL/TLS）プロトコルで動作できません。

1. ![ 展開セレクター ](../assets/icon-display-expand.png)_[!UICONTROL Base URLs (Secure]）_ セクションを展開し、次の操作を行います。

   ![ 一般設定 – セキュアなベース URL](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]**：完全なセキュア・ベース URL を入力し、その後にスラッシュを入力します。 例：`https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** - 「セキュアベースリンク URL」フィールドのプレースホルダーを変更しないでください。 安全なベース URL への相対リンクを作成するために使用されます。

   - **[!UICONTROL Secure Base URL for Static View Files]** — （オプション）次のプレースホルダーで始まるパスを入力して、静的ビューファイルのセキュアなベース URL の別の場所を指定します。

     \{\{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]** — （オプション）次のプレースホルダーで始まるパスを入力して、ユーザーメディアファイルのセキュアなベース URL の別の場所を指定します。

     \{\{secure_base_url}}

1. セキュリティを強化するには、次の両方のオプションを `Yes` に設定します。

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. _[!UICONTROL Enhanced Security Settings]_&#x200B;の場合は、次の手順を実行します。

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** - ストアにセキュアな HTTPS ページリクエストのみを表示する場合は、`Yes` に設定します。

   - **[!UICONTROL Upgrade Insecure Requests]** – 標準の保護されていない HTTP ページのリクエストを保護された HTTPS にアップグレードするには、`Yes` に設定します。

1. サーバーの **[!UICONTROL Offloader Header]** を設定します。

   ほとんどのCommerce インストールでは、プロトコルを `HTTP` または `HTTPS` として識別するためにデフォルトの `X-Forward-Proto` が使用されています。 サーバー設定で別の offloader_header を使用している場合は、ここに入力します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## URL にストアコードを含める

>[!NOTE]
>
>「_URL にストアコードを追加_ オプションが `Yes` に設定されている場合、ブラウザーの URL にストアコードを含める必要があります。 この設定により、_「404 Page Not Found」_ エラーを発生させずに、URL の書き換えが正しくマッピングされ、すべてのページが正常に開かれます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左パネルの「_[!UICONTROL General]_」で、「**[!UICONTROL Web]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL URL Options]**」セクションを展開します。

1. **[!UICONTROL Add Store Code]** を環境設定に合わせて設定します。

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![ 一般設定 – web URL オプション ](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. ワークスペースの上部にあるメッセージの「**[!UICONTROL Cache Management]**」リンクをクリックします。 次に、指示に従ってキャッシュを更新します。

   ![ キャッシュ管理メッセージ ](./assets/msg-cache-management.png)

## URL のトラブルシューティング

設定手順に従った後も、一部のページが引き続き保護されていない URL （`http://`）で提供される場合は、次の手順を実行します。

- （セキュアでない）ベース URL をセキュアな HTTPS URL に変更します。
- サーバーで `.htaccess` ファイル（またはロードバランサー）を編集して、保護されていない URL が保護された URL にリダイレクトされるようにします。

## カスタム管理 URL を使用

[ セキュリティのベストプラクティス ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=ja) として、Adobeでは、デフォルトの _管理者_ や一般的な用語（_バックエンド_ ではなく、一意の管理者 URL を使用することをお勧めします。 判定された不正アクターからサイトを直接保護することはありませんが、不正アクセスを試みるスクリプトへの露出を減らすことができます。

>[!NOTE]
>
>カスタムの管理 URL を実装する前に、ホスティングプロバイダーに確認してください。 一部のホスティングプロバイダーは、ファイアウォール保護ルールを満たすために標準 URL を必要とします。

通常のインストールでは、管理者 URL とパスはベース URL の直後に続きます。 管理者パスはルートの 1 つ下のディレクトリです。

- **デフォルトのベース URL**: `http://yourdomain.com/magento/`
- **既定の管理パス**: `admin`
- **デフォルトの管理者 URL とパス**:`http://yourdomain.com/magento/admin`

管理者 URL とパスを別の場所に変更することは可能ですが、誤った場合は管理者へのアクセスができなくなるので、サーバーから修正する必要があります。

>[!NOTE]
>
>予防措置として、サーバー上の設定ファイルの編集方法がわからない場合は、管理者 URL を自分で変更しないでください。 クラウドインフラストラクチャー上にデプロイされたAdobe Commerce プロジェクトの場合は、*クラウドインフラストラクチャー上のAdobe Commerce ガイド [&#128279;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=ja#admin-url) の  手順* に従って、管理者 URL を変更します。

### 方法 1：管理者から変更する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL Admin]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Admin Base URL]**」セクションを展開します。

1. カスタム URL の設定オプションを設定します。

   ![ 詳細設定 – 管理ベース URL](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   必要に応じて、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、設定を変更します。

   - **[!UICONTROL Use Custom Admin URL]** を `Yes` に設定します。

   - **[!UICONTROL Custom Admin URL]** を入力：`http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >管理者 URL は、同じCommerce インストール内にあり、ストアフロントと同じドキュメントルートを持つ必要があります。

   - **[!UICONTROL Custom Admin Path]** を `Yes` に設定します。

   - **[!UICONTROL Custom Admin Path]**：カスタム管理フォルダー名として使用するパスを入力します。

     例：`sample_custom_admin`

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. 変更を保存したら、管理者からログアウトし、新しい管理者 URL とパスを使用してログインし直します。

### 方法 2：サーバーコマンドラインからの管理パスの変更

1. `app/etc/env.php` ファイルをテキストエディターで開き、`backend` セクションの `frontName` パラメーターの値を変更します。 次に、ファイルを保存します。

   必ず小文字のみを使用してください。

   >[!NOTE]
   >
   >   この方法を使用すると、管理パスを変更できますが、管理 URL は変更できません。

   >[!TIP]
   >
   >クラウドインフラストラクチャー上のAdobe Commerceの場合、Cloud UI の `ADMIN_URL` 変数を使用してカスタム管理パスを設定できます。 [2&rbrace;Cloud Infrastructure ガイドのCommerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=ja) 管理者変数に関するトピック _を参照してください。_

   - **デフォルトの管理パス**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **新しい管理パス**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. キャッシュをクリアするには、次のいずれかの方法を使用します。

   - _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Tools]_/**[!UICONTROL Cache Management]**&#x200B;に移動します。 次に、「**[!UICONTROL Flush Magento Cache]**」をクリックします。
   - サーバーで、次の操作を実行します。

     ```bash
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >メソッド 1 を使用して行った変更は、`app/etc/env.php` ファイルで行った変更よりも優先されます。

### 方法 3:Commerce CLI を使用して管理パスを変更する

CLI `setup:config:set` コマンドを使用して、管理パスを変更できます。 次の例では、`--backend-frontname` オプションを使用して、パスをCommerce ルートから新しい管理パスに変更します。

```bash
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

このコマンドは、`app/etc/env.php` ファイルの `backend` > `frontName` 設定オプションを更新します。

## デフォルトの管理者 URL と管理パスを復元

無効な管理者 URL または管理パスを設定していて、バックエンドへのアクセス権を失った場合、コマンドラインから修正する方法があります。

1. デフォルトの管理者 URL に戻すには、次のコマンドを実行します。

   ```bash
   php bin/magento config:set admin/url/use_custom 0
   ```

1. デフォルトの管理者パス（メソッド 2 で説明したように `app/etc/env.php` で設定）に戻すには、次のコマンドを実行します。

   ```bash
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. キャッシュをクリアするには、次のいずれかの方法を使用します。

   - _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Tools]_/**[!UICONTROL Cache Management]**&#x200B;に移動します。 次に、「**[!UICONTROL Flush Magento Cache]**」をクリックします。
   - サーバーで、次の操作を実行します。

     ```bash
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
