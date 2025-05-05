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

設定全体で参照されるので、事前にストアカタログ階層を計画しておいてください。 各ストアには個別の [ ルートカテゴリ ](../catalog/category-root.md) を設定できます。これにより、ストアごとに完全に異なるメインメニューオプションのセットを設定できます。

![ スコープ図 ](./assets/scope-multisite.svg){width="550"}

## ストアを追加

Adobe CommerceまたはMagento Open Sourceの 1 つのインストールに、1 つの管理者を共有する複数のストアを含めることができます。 同じ web サイトの配下にあるストアは、同じ IP アドレスとドメインを持ち、同じセキュリティ証明書を使用し、単一のチェックアウトプロセスを共有します。

理解しておくべき重要なことは、ストアでは同じコードを使用し、管理者を共有することです。 各ストアは個別のカタログを持つことができますが、ストアはカタログを共有できます。 各ストアには個別の [ ルートカテゴリ ](../catalog/category-root.md) を設定できるので、ストアごとに異なるメインメニューを使用できます。 ストアには、様々なブランディング、プレゼンテーション、コンテンツを含めることもできます。 ストア階層は設定全体で使用されるので、開始する前に、将来の成長を考慮してストア階層を計画する必要があります。

![ 範囲 – 複数のストア ](./assets/scope-multistore.svg){width="550"}

次に、複数のストアに対して URL を設定する方法の例を示します。

| URL | 説明 |
| --- | ----------- |
| `yourdomain.com/store1`<br>`yourdomain.com/store2` | 各ストアには異なるパスがありますが、1 つのドメインを共有します。 |
| `store1.yourdomain.com`<br>`store2.yourdomain.com` | 各ストアには、プライマリドメインの異なるサブドメインがあります。 |

Adobe Commerceのマルチストアインストールは、管理者だけでなく、サーバーのコマンドラインからも設定する必要があります。 サーバー環境の設定手順について詳しくは、Adobe Commerce[ 設定ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=ja) を参照してください。

### 手順 1：ストアドメインの選択

最初のステップは、ストアの配置方法を選択することです。 ストアはドメインを共有する必要がありますか。それぞれのストアにサブドメインを含めるか、明確に異なるドメインを持たせますか。 ストアごとに、次のいずれかの操作を行います。

- ストアをプライマリドメインの 1 レベル下に配置する場合は、何もする必要はありません。
- プライマリドメインのサブドメインを設定します。
- 別のプライマリドメインを設定します。

### 手順 2：ストアの作成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL All Stores]**&#x200B;に移動します。

1. 「**[!UICONTROL Create Store]**」をクリックして、新しいストアのオプションを設定します。

   - **[!UICONTROL Web Site]** – 新しいストアの親となる web サイトを選択します。 インストールに web サイトが 1 つしかない場合は、デフォルト（`Main Website`）を使用します。

   - 「**[!UICONTROL Name]**」 – 新しいストアの名前を入力します。 この名前は内部参照用です。

   - 「**[!UICONTROL Code]**」 – ストアを識別するコードを小文字で入力します。 例：`mainstore`。

   - **[!UICONTROL Root Category]** – 新しいストアのメインメニューのカテゴリ構造を定義する [ ルートカテゴリ ](../catalog/category-root.md) に設定します。 ストアの特定のルートカテゴリを既に作成している場合は、そのカテゴリを選択します。 それ以外の場合は、「`Default Category`」を選択します。 後で戻って設定を更新することもできます。

   ![ ストアを作成 – ストアオプション ](./assets/stores-all-store-information.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save Store]**」をクリックします。

### 手順 3：デフォルトのストア表示の作成

1. 「**[!UICONTROL Create Store View]**」をクリックして、ストア表示オプションを設定します。

   - **[!UICONTROL Store]** – 作成した新しいストアに設定します。

   - 「**[!UICONTROL Name]**」 – ビューの名前を入力します。 例：`English`。

   - 「**[!UICONTROL Code]**」 – ビューのコードを小文字で入力します。

   - **[!UICONTROL Status]** — `Enabled` に設定します。

   - **[!UICONTROL Sort Order]**：他のストアと一緒にリストされたときのストアの位置を決定する番号を入力します。

1. 「**[!UICONTROL Save Store View]**」をクリックします。

   ストアを編集モードで開くと、デフォルトのビューが表示されていることがわかります。

   ![ デフォルト表示を使用した新しいストア ](./assets/new-store-default-view.png){width="600" zoomable="yes"}

### 手順 4：ストア URL の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;をクリックします。

1. 左側の左パネルの「_[!UICONTROL General]_」で、「**[!UICONTROL Web]**」を選択します。

1. 左上隅で、新しいストア用に作成したビューに **[!UICONTROL Store View]** を設定します。

1. [ 範囲 ](../getting-started/websites-stores-views.md#scope-settings) 切り替えを確認するプロンプトが表示されたら、「**[!UICONTROL OK]**」をクリックします。

   ![ ストア表示の選択 ](./assets/create-store-config-view.png){width="600" zoomable="yes"}

1. 「![ 展開セレクター ](../assets/icon-display-expand.png) 「**[!UICONTROL Base URLs]**」セクションを展開し、ストアのベース URL を入力します。

   必要に応じて、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、設定を変更します。

   ![ 一般設定 – web ベース URL](./assets/config-general-web-base-urls-clear-checkbox.png){width="600" zoomable="yes"}

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」 **[!UICONTROL Secure Base URLs]** クションを展開し、ストア [ セキュア URL](store-urls.md) を設定する場合は前の手順を繰り返します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

### 手順 5：サーバーの設定

複数の Web サイトをサポートするようにサーバーを構成するには、『 [ 構成ガイド _の ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=ja) 複数の Web サイトまたはストア_ を参照してください。

Web サーバーの設定のヘルプについては、次のリソースを参照してください。

- [NGNX で複数の Web サイトを設定する ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html?lang=ja)
- [Apache で複数の web サイトを設定する ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html?lang=ja)

クラウドインフラストラクチャー上のAdobe Commerceについては、[ 複数の web サイトまたはストアの設定 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html?lang=ja) を参照してください。

## Web サイトの追加

複数の web サイトを、1 つのAdobe Commerceまたは同じドメインまたは異なるドメインを持つMagento Open Sourceのインストールからセットアップできます。 デフォルトでは、同じ web サイトの配下にあるストアは同じ IP アドレスとドメインを持ち、同じセキュリティ証明書を使用し、単一のチェックアウトプロセスを共有します。 各ストアに専用のチェックアウトプロセスを独自のドメインで実行する場合は、各ストアに個別の IP アドレスと個別のセキュリティ証明書が必要です。

Adobe CommerceまたはMagento Open Sourceのマルチサイトインストールは、管理者だけでなく、サーバーのコマンドラインからも設定する必要があります。 サーバー環境の設定手順について詳しくは、Commerce[ 設定ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=ja) を参照してください。

![ 範囲 – web サイト ](./assets/scope-multisite.svg){width="550"}

### 手順 1:web サイトの作成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL All Stores]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Create Website]**」をクリックします。

1. **[!UICONTROL Web Site Information]** のオプションを設定します。

   ![Web サイトの作成 – オプション ](./assets/create-website-info.png){width="600" zoomable="yes"}

   - 「**[!UICONTROL Name]**」 – 新しい Web サイトのドメインを入力します。 例：`domain.com`。

   - 「**[!UICONTROL Code]**」 – ドメインを指すためにサーバーで使用されるコードを入力します。

     コードは、小文字（a ～ z）で始まる必要があり、文字（a ～ z）、数字（0 ～ 9）、アンダースコア（_）記号を任意に組み合わせることができます。

   - **[!UICONTROL Sort Order]** — _（オプション）_ このサイトが他のサイトと一緒にリストされる順序を決定する番号を入力します。 このサイトをリストの先頭に表示するには、ゼロ （`0`）を入力します。

1. 「**[!UICONTROL Save Web Site]**」をクリックします。

1. 新しい web サイトに必要な各 [ ストア ](#add-stores) および [ ストア表示 ](store-views.md) を設定します。

   その後、web サイトを編集モードで開いて、デフォルトストアを設定できます。

### 手順 2：ストア URL の設定

[ ストア URL](store-urls.md) を設定するには、手順に従います。

### 手順 3：サーバーの設定

複数の Web サイトをサポートするようにサーバーを構成するには、『 [ 構成ガイド _の ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=ja) 複数の Web サイトまたはストア_ を参照してください。

Web サーバーの設定のヘルプについては、次のチュートリアルを参照してください。

- [NGNX で複数の Web サイトを設定する ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html?lang=ja)
- [Apache で複数の web サイトを設定する ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html?lang=ja)

クラウドインフラストラクチャー上のAdobe Commerceについては、[ 複数の web サイトまたはストアの設定 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html?lang=ja) を参照してください。
