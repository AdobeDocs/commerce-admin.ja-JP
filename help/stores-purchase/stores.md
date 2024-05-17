---
title: ストアとサイトの構造
description: Web サイト、ストア、ストア表示階層について説明します。
exl-id: d745cbd0-151b-4f82-bb6c-fb6b9565a014
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# ストアとサイトの構造

Adobe CommerceまたはMagento Open Sourceがインストールされると、メインの web サイト、ストアおよびストアビューを含む階層が作成されます。 必要に応じて、追加の web サイト、ストア、ストア表示を作成できます。 例えば、メインの web サイトに加えて、別のドメインを持つ追加の web サイトがある場合などです。 各 web サイト内に複数のストアを配置でき、各ストア内でストアを個別に表示できます。 多くのインストールでは、1 つの web サイトと 1 つのストアがありますが、異なる言語をサポートするために複数のストア表示があります。

設定全体で参照されるので、事前にストアカタログ階層を計画しておいてください。 各店舗は、個別のを持つことができます [ルートカテゴリ](../catalog/category-root.md)を使用すると、ストアごとに完全に異なるメインメニューオプションのセットを使用できます。

![スコープ図](./assets/scope-multisite.svg){width="550"}

## ストアを追加

Adobe CommerceまたはMagento Open Sourceの 1 つのインストールに、1 つの管理者を共有する複数のストアを含めることができます。 同じ web サイトの配下にあるストアは、同じ IP アドレスとドメインを持ち、同じセキュリティ証明書を使用し、単一のチェックアウトプロセスを共有します。

理解しておくべき重要なことは、ストアでは同じコードを使用し、管理者を共有することです。 各ストアは個別のカタログを持つことができますが、ストアはカタログを共有できます。 各店舗は、個別のを持つことができます [ルートカテゴリ](../catalog/category-root.md)これにより、店舗ごとに異なるメインメニューを持つことができます。 ストアには、様々なブランディング、プレゼンテーション、コンテンツを含めることもできます。 ストア階層は設定全体で使用されるので、開始する前に、将来の成長を考慮してストア階層を計画する必要があります。

![範囲 – 複数のストア](./assets/scope-multistore.svg){width="550"}

次に、複数のストアに対して URL を設定する方法の例を示します。

| URL | 説明 |
| --- | ----------- |
| `yourdomain.com/store1`<br>`yourdomain.com/store2` | 各ストアには異なるパスがありますが、1 つのドメインを共有します。 |
| `store1.yourdomain.com`<br>`store2.yourdomain.com` | 各ストアには、プライマリドメインの異なるサブドメインがあります。 |

Adobe Commerceのマルチストアインストールは、管理者だけでなく、サーバーのコマンドラインからも設定する必要があります。 Adobe Commerce [設定ガイド](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) サーバー環境の設定手順を詳しく説明します。

### 手順 1：ストアドメインの選択

最初のステップは、ストアの配置方法を選択することです。 ストアはドメインを共有する必要がありますか。それぞれのストアにサブドメインを含めるか、明確に異なるドメインを持たせますか。 ストアごとに、次のいずれかの操作を行います。

- ストアをプライマリドメインの 1 レベル下に配置する場合は、何もする必要はありません。
- プライマリドメインのサブドメインを設定します。
- 別のプライマリドメインを設定します。

### 手順 2：ストアの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. クリック **[!UICONTROL Create Store]** そして、新しいストアのオプションを設定します。

   - **[!UICONTROL Web Site]**  – 新しいストアの親となる Web サイトを選択します。 インストールに web サイトが 1 つしかない場合は、デフォルトのを使用します（`Main Website`）に設定します。

   - **[!UICONTROL Name]**  – 新しいストアの名前を入力します。 この名前は内部参照用です。

   - **[!UICONTROL Code]** — ストアを識別するコードを小文字で入力します。 例： `mainstore`.

   - **[!UICONTROL Root Category]**  – に設定 [ルートカテゴリ](../catalog/category-root.md) 新しいストアのメインメニューのカテゴリ構造を定義します。 ストアの特定のルートカテゴリを既に作成している場合は、そのカテゴリを選択します。 それ以外の場合は、 `Default Category`. 後で戻って設定を更新することもできます。

   ![ストアを作成 – ストアオプション](./assets/stores-all-store-information.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Store]**.

### 手順 3：デフォルトのストア表示の作成

1. クリック **[!UICONTROL Create Store View]** ストア表示オプションを設定します。

   - **[!UICONTROL Store]**  – 作成した新しいストアに設定します。

   - **[!UICONTROL Name]** — ビューの名前を入力します。 例： `English`.

   - **[!UICONTROL Code]** — ビューのコードを小文字で入力します。

   - **[!UICONTROL Status]**  – に設定 `Enabled`.

   - **[!UICONTROL Sort Order]**  – 他のストアと一緒にリストされた場合のストアの位置を決定する番号を入力します。

1. クリック **[!UICONTROL Save Store View]**.

   ストアを編集モードで開くと、デフォルトのビューが表示されていることがわかります。

   ![デフォルトの表示を使用した新しいストア](./assets/new-store-default-view.png){width="600" zoomable="yes"}

### 手順 4：ストア URL の設定

1. 日 _Admin_ サイドバー、クリック **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 次の下 _[!UICONTROL General]_左側の左側のパネルで、を選択します。**[!UICONTROL Web]**.

1. 左上隅にを設定します **[!UICONTROL Store View]** 新しいストア用に作成したビューに移動します。

1. 確認を求められたら [範囲](../getting-started/websites-stores-views.md#scope-settings) 切り替え，クリック **[!UICONTROL OK]**.

   ![ストア表示の選択](./assets/create-store-config-view.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Base URLs]** 「」セクションに、ストアのベース URL を入力します。

   必要に応じて、 **[!UICONTROL Use system value]** チェックボックスをオンにして、設定を変更します。

   ![一般設定 – web ベース URL](./assets/config-general-web-base-urls-clear-checkbox.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Secure Base URLs]** をセクションし、ストアを設定する場合は前の手順を繰り返します [セキュア URL](store-urls.md).

1. クリック **[!UICONTROL Save Config]**.

### 手順 5：サーバーの設定

複数の Web サイトをサポートするようにサーバーを設定するには、を参照してください。 [複数の web サイトまたはストア](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) が含まれる _設定ガイド_.

Web サーバーの設定のヘルプについては、次のリソースを参照してください。

- [NGNX で複数の Web サイトを設定する](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Apache での複数の web サイトの設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

クラウドインフラストラクチャー上のAdobe Commerceについては、以下を参照してください。 [複数の web サイトまたはストアを設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).

## Web サイトの追加

複数の web サイトを、1 つのAdobe Commerceまたは同じドメインまたは異なるドメインを持つMagento Open Sourceのインストールからセットアップできます。 デフォルトでは、同じ web サイトの配下にあるストアは同じ IP アドレスとドメインを持ち、同じセキュリティ証明書を使用し、単一のチェックアウトプロセスを共有します。 各ストアに専用のチェックアウトプロセスを独自のドメインで実行する場合は、各ストアに個別の IP アドレスと個別のセキュリティ証明書が必要です。

Adobe CommerceまたはMagento Open Sourceのマルチサイトインストールは、管理者だけでなく、サーバーのコマンドラインからも設定する必要があります。 Commerce [設定ガイド](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) サーバー環境の設定手順を詳しく説明します。

![範囲 – Web サイト](./assets/scope-multisite.svg){width="550"}

### 手順 1:web サイトの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. 右上隅のをクリックします。 **[!UICONTROL Create Website]**.

1. を **[!UICONTROL Web Site Information]** オプション：

   ![Web サイトの作成 – オプション](./assets/create-website-info.png){width="600" zoomable="yes"}

   - **[!UICONTROL Name]**  – 新しい Web サイトのドメインを入力します。 例： `domain.com`.

   - **[!UICONTROL Code]** — ドメインを指すためにサーバーで使用されるコードを入力します。

     コードは、小文字（a ～ z）で始まる必要があり、文字（a ～ z）、数字（0 ～ 9）、アンダースコア（_）記号を任意に組み合わせることができます。

   - **[!UICONTROL Sort Order]** — _（オプション）_ このサイトが他のサイトと一緒に表示される順序を決定する番号を入力します。 このサイトをリストの上部に表示するには、ゼロ （`0`）に設定します。

1. クリック **[!UICONTROL Save Web Site]**.

1. 各 [store](#add-stores) および [ストア表示](store-views.md) これは、新しい web サイトに必要です。

   その後、web サイトを編集モードで開いて、デフォルトストアを設定できます。

### 手順 2：ストア URL の設定

を設定するには [url を格納](store-urls.md)、手順に従います。

### 手順 3：サーバーの設定

複数の Web サイトをサポートするようにサーバーを設定するには、を参照してください。 [複数の web サイトまたはストア](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) が含まれる _設定ガイド_.

Web サーバーの設定のヘルプについては、次のチュートリアルを参照してください。

- [NGNX で複数の Web サイトを設定する](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Apache での複数の web サイトの設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

クラウドインフラストラクチャー上のAdobe Commerceについては、以下を参照してください。 [複数の web サイトまたはストアを設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).
