---
title: ストアの URL
description: ストア URL の概要と、ベース URL およびストアコードの設定方法について説明します。
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
source-git-commit: 555c54e9a980aa181e0b4380412ad027d80ee10f
workflow-type: tm+mt
source-wordcount: '1512'
ht-degree: 0%

---

# ストアの URL

Adobe CommerceまたはMagento Open Sourceインストール内の各 Web サイトには、ストアフロントに割り当てられるベース URL と、管理者に割り当てられる別の URL があります。 Adobeでは変数を使用して、ベース URL に関連する内部リンクを定義します。これにより、リンクを更新せずに、ストア全体を別の場所に移動できます。 標準ベース URL はで始まります。 `http`、セキュアベース URL はで始まります。 `https`.

- **ベース URL** — `http://www.yourdomain.com/magento/`
- **セキュアベース URL** — `https://www.yourdomain.com/magento/`
- **IP アドレスを含む URL** — `http://###.###.###.###/magento/` または `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>デフォルトのベース URL 設定から管理 URL を変更しないでください。 管理 URL またはパスを変更するには、 [カスタム管理 URL を使用](#use-a-custom-admin-url).

## セキュアプロトコルを使用

ストアのベース URL は、Adobe Commerceのインストール時に最初に設定されました。 その時点でセキュリティ証明書が使用可能な場合は、次のように指定します。 `HTTPS` ストア、管理者、またはその両方に使用する URL。 Adobe Commerceのインストールに複数のストアが含まれている場合や、後でストアを追加する予定の場合は、URL にストアコードを含めることができます。 すべてのAdobe・リソースと操作は、セキュアなプロトコルで使用できます。

インストール時にドメインのセキュリティ証明書が使用できなかった場合は、ストアを起動する前に設定を更新してください。 ドメインのセキュリティ証明書が確立されたら、暗号化された Secure Sockets Layer(SSL) と [トランスポート層のセキュリティ][1] (TLS) プロトコル。

>[!IMPORTANT]
>
>Adobeでは、安全なプロトコルを使用して、コンテンツページや製品ページを含む、実稼動サイトのすべてのページを送信することを強くお勧めします。

Adobe CommerceとMagento Open Sourceは、すべてのページを `HTTPS` デフォルトでは。 ストアが標準のプロトコルで実行されている場合は、 [HTTP Strict Transport Security][2] (HSTS) を使用し、セキュリティで保護されていないページリクエストをアップグレードする必要があります。 HSTS は、ブラウザーが標準のレンダリングを妨げるオプトインプロトコルです。 `HTTP` 指定したドメイン用の安全でないプロトコルで送信されるページ。 検索エンジンでは、ストアの各ページに標準のインデックスを既に作成している可能性があるので、 `HTTP` URL を使用すると、セキュリティで保護されていないページリクエストをにアップグレードするように Commerce を設定できます。 `HTTPS` 自動的に削除されるので、トラフィックは失われません。 Commerce がストアフロントと管理の両方にセキュア URL を使用するように設定されている場合は、次の 2 つの追加フィールドが表示され、これらを有効にできます `HSTS`.

## ベース URL の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下 _一般_ 左のパネルで、を選択します。 **[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Base URL]** 」セクションに入力します。

   - **[!UICONTROL Base URL]**  — ストアの完全修飾ベース URL を入力します。 URL の末尾は必ずスラッシュで終わり、ストアの追加の URL キーで拡張できます。 例： `http://yourdomain.com/`

     >[!NOTE]
     >
     >内のプレースホルダーを変更しないでください _[!UICONTROL Base Link URL]_フィールドに入力します。 ベース URL への相対リンクを作成するために使用されるプレースホルダーです。

   - **[!UICONTROL Base URL for Static View Files]** — （オプション）次のプレースホルダーで始まるパスを入力して、静的ビューファイルのベース URL の代替の場所を指定します。

     \{\{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]** — （オプション）次のプレースホルダーで始まるパスを入力して、ユーザーメディアファイルのベース URL の代替の場所を指定します。

     \{\{unsecure_base_url}}

     通常のインストールでは、静的ビューファイルまたはメディアファイルのパスを更新する必要はありません。静的ビューファイルはベース URL に対する相対パスなのでです。

   ![一般設定 — Web ベース URL](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >二重中括弧で囲まれたプレースホルダーは、変数のマークアップタグです。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## セキュアベース URL の設定

ドメインに有効なセキュリティ証明書がある場合、ストアフロントと管理者の両方の URL を設定して、セキュリティで保護された (https) チャネルを介してデータを送信できます。 有効なセキュリティ証明書がないと、ストアはセキュア (SSL/TLS) プロトコルで動作しません。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Base URLs (Secure])_ 」セクションで次の操作を実行します。

   ![一般的な設定 — セキュアベース URL](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]**  — 完全なセキュアベース URL を入力し、その後にスラッシュを付けます。 例： `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]**  — セキュアベースリンク URL フィールド内のプレースホルダーを変更しないでください。 セキュアベース URL への相対リンクを作成するために使用されます。

   - **[!UICONTROL Secure Base URL for Static View Files]** — （オプション）次のプレースホルダーで始まるパスを入力して、静的ビューファイルのセキュアベース URL の代替の場所を指定します。

     \{\{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]** — （オプション）次のプレースホルダーで始まるパスを入力して、ユーザーメディアファイルのセキュアベース URL の代替の場所を指定します。

     \{\{secure_base_url}}

1. セキュリティを強化するには、次の両方のオプションをに設定します。 `Yes`.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. の場合 _[!UICONTROL Enhanced Security Settings]_、次の操作を実行します。

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]**  — ストアでセキュリティで保護された HTTPS ページリクエストのみを表示する場合は、をに設定します。 `Yes`.

   - **[!UICONTROL Upgrade Insecure Requests]**  — 標準のセキュリティで保護されていない HTTP ページのリクエストをセキュリティで保護された HTTPS にアップグレードするには、をに設定します。 `Yes`.

1. を設定します。 **[!UICONTROL Offloader Header]** を設定します。

   ほとんどのコマースインストールでは、デフォルトが使用されます `X-Forward-Proto` プロトコルを次のどちらかとして識別するには： `HTTP` または `HTTPS`. サーバー設定で別の offloader_header を使用している場合は、ここに入力します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## ストアコードを URL に含める

>[!NOTE]
>
>次の場合に _ストアコードを URL に追加_ オプションが `Yes`の場合は、ブラウザーの URL にストアコードを含める必要があります。 この設定では、URL の書き換えが正しくマッピングされ、すべてのページが正常に開かれます。 _&quot;404 Page Not Found&quot;_ エラー。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下 _[!UICONTROL General]_左のパネルで、を選択します。**[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL URL Options]** 」セクションに入力します。

1. 設定 **[!UICONTROL Add Store Code]** を選択します。

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![一般設定 — Web URL オプション](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. 次をクリック： **[!UICONTROL Cache Management]** リンクを使用して、メッセージの上部に表示されます。 次に、指示に従ってキャッシュを更新します。

   ![キャッシュ管理メッセージ](./assets/msg-cache-management.png)

## URL のトラブルシューティング

設定手順に従った後も、一部のページは、セキュリティで保護されていない URL(`http://`)、次の操作を実行します。

- （セキュアでない）ベース URL をセキュアな HTTPS URL に変更します。
- サーバー上で、 `.htaccess` ファイル（またはロードバランサー）を使用して、セキュアでない URL がセキュア URL にリダイレクトされるようにします。

## カスタム管理 URL を使用

As a [セキュリティのベストプラクティス](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)の場合、Adobeでは、デフォルトの _admin_ または一般的な用語 _backend_. サイトを特定の悪役から直接保護するわけではありませんが、不正なアクセスを得ようとするスクリプトに対する露出を減らすことができます。

>[!NOTE]
>
>カスタム管理 URL を実装する前に、ホスティングプロバイダーに問い合わせてください。 一部のホスティングプロバイダーでは、ファイアウォール保護ルールを満たすために標準の URL が必要です。

通常のインストールでは、管理 URL とパスは、ベース URL の直後に表示されます。 管理パスは、ルートの下の 1 つのディレクトリです。

- **デフォルトのベース URL**: `http://yourdomain.com/magento/`
- **デフォルトの管理パス**: `admin`
- **デフォルトの管理 URL とパス**: `http://yourdomain.com/magento/admin`

管理者 URL とパスを別の場所に変更することは可能ですが、誤って管理者へのアクセス権が削除されるので、サーバーから修正する必要があります。

>[!NOTE]
>
>予防措置として、サーバー上の設定ファイルの編集方法がわからない限り、自分で Admin URL を変更しないようにしてください。 クラウドインフラストラクチャにデプロイされたAdobe Commerceプロジェクトの場合は、次の手順に従って Admin URL を変更します。 [instructions](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=en#admin-url) （内） *Adobe Commerce on Cloud Infrastructure ガイド*.

### 方法 1：管理者からの変更

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Admin]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Admin Base URL]** 」セクションに入力します。

1. カスタム URL の設定オプションを設定します。

   ![詳細設定 — 管理ベース URL](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   必要に応じて、 **[!UICONTROL Use system value]** チェックボックスを使用して設定を変更します。

   - 設定 **[!UICONTROL Use Custom Admin URL]** から `Yes`.

   - 次を入力します。 **[!UICONTROL Custom Admin URL]**: `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >管理 URL は、同じ Commerce インストールに存在し、ストアフロントと同じドキュメントルートを持つ必要があります。

   - 設定 **[!UICONTROL Custom Admin Path]** から `Yes`.

   - の場合 **[!UICONTROL Custom Admin Path]**&#x200B;に設定し、カスタムの管理フォルダー名として使用するパスを入力します。

     例： `sample_custom_admin`

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. 変更が保存されたら、管理者からログアウトし、新しい管理 URL とパスを使用して再度ログインします。

### 方法 2：サーバーのコマンドラインから管理パスを変更する

1. を開きます。 `app/etc/env.php` ファイルを編集し、 `frontName` のパラメーター `backend` 」セクションに入力します。 次に、ファイルを保存します。

   必ず小文字のみを使用してください。

   >[!NOTE]
   >
   >   このメソッドを使用すると、管理者 URL ではなく管理者パスを変更できます。

   >[!TIP]
   >
   >クラウドインフラストラクチャ上のAdobe Commerceの場合、 `ADMIN_URL` 変数を使用して、Cloud UI にアクセスできます。 詳しくは、 [「管理変数」トピック](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html) （内） _Commerce on Cloud Infrastructure ガイド_.

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

   - 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. 次に、「**[!UICONTROL Flush Magento Cache]**.
   - サーバー上で、以下を実行します。

     ```terminal
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >方法 1 を使用して行った変更は、 `app/etc/env.php` ファイル。

### 方法 3:Commerce CLI を使用して管理パスを変更する

CLI を使用できます。 `setup:config:set` 」コマンドを使用して、管理パスを変更します。 次の例では、 `--backend-frontname` コマースルートから新しい管理パスにパスを変更するオプション：

```terminal
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

このコマンドは、 `backend` > `frontName` 設定オプション ( `app/etc/env.php` ファイル。

## デフォルトの管理 URL と管理パスを復元

無効な管理 URL または管理パスを設定し、バックエンドへのアクセスを失った場合は、コマンドラインから修正する方法があります。

1. デフォルトの管理 URL に戻すには、次のコマンドを実行します。

   ```terminal
   php bin/magento config:set admin/url/use_custom 0
   ```

1. デフォルトの管理パス ( `app/etc/env.php` メソッド 2 の説明に従って )、次のコマンドを実行します。

   ```terminal
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. キャッシュをクリアするには、次のいずれかの方法を使用します。

   - 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. 次に、「**[!UICONTROL Flush Magento Cache]**.
   - サーバー上で、以下を実行します。

     ```terminal
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
