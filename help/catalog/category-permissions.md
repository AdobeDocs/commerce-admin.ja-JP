---
title: カテゴリ権限
description: カテゴリを使用して製品価格の表示を制御する方法、および買い物かごに製品を追加できる顧客グループを決定する方法、およびランディングページを指定する方法について説明します。
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# カテゴリ権限

{{ee-feature}}

カテゴリへのアクセスは、特定の顧客グループに限定することも、完全に制限することもできます。 製品価格の表示を制御し、買い物かごに製品を追加できる顧客グループを決定し、ランディングページを指定できます。

>[!NOTE]
>
>カテゴリ権限はグローバルな範囲を持ち、有効にすると、個々の権限に応じて各カテゴリへのアクセスを制限します。 デフォルトでは、カテゴリ権限は有効になっていません。

例えば、卸売の顧客にのみ販売する場合、誰でもカタログを閲覧できますが、価格は表示され、 _卸売_ 顧客グループとして割り当てられます。 次の例では、ログインしたユーザーのみが「コレクション」カテゴリにアクセスできます。 ゲストの場合、「コレクション」オプションはメインメニューに表示されません。

![ログインしたユーザーが「コレクション」カテゴリを表示する](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

有効にすると、新しい _[!UICONTROL Category Permissions]_セクションが [ カテゴリ ] ページに表示され、各カテゴリに必要なアクセス権を適用できます。 異なる Web サイトや顧客グループの各カテゴリに複数の権限ルールを追加できます。

## 手順 1：カテゴリ権限の設定

>[!IMPORTANT]
>
>すべての既存 [グループ権限設定](../configuration-reference/catalog/catalog.md#category-permissions) は次の項目で無視されます： **_すべて_** カタログのカテゴリ ( **_[!UICONTROL Shared Catalog]_** 機能が有効になっている。 [!UICONTROL Shared Catalog] は、カタログが有効な場合に、カタログ内のすべてのカテゴリ権限を完全に制御します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Category Permissions]** 」セクションに入力します。

   ![カテゴリ権限](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、 [カテゴリ権限](../configuration-reference/catalog/catalog.md#category-permissions) （内） _設定リファレンス_.

1. 設定 **[!UICONTROL Enable]** から `Yes`.

1. ストアで許可または制限する内容に応じて、その他のオプションを設定します（以下の節を参照）。

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** リンクを使用してキャッシュを更新し、指示に従ってキャッシュを更新します。

### [!UICONTROL Allow Browsing Category]

このオプションは、 [web サイト](../getting-started/websites-stores-views.md).

次の項目のメンバーを許可するには： **_特定の顧客グループ_** カテゴリ製品を参照するには、次の手順を実行します。

1. 設定 **[!UICONTROL Allow Browsing Category]** から `Specified Customer Groups`.

1. Adobe Analytics の **[!UICONTROL Customer Groups]** 」ボックスで、カテゴリ内の製品を閲覧できる各グループを選択します。

   複数のグループを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各グループをクリックします。

   ![卸売顧客グループによる閲覧を許可](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

宛先 **_アクセスとリダイレクトをランディングページに制限_**、次の操作を実行します。

1. 設定 **[!UICONTROL Allow Browsing Category]** から `No, Redirect to Landing Page`.

1. を選択します。 **[!UICONTROL Landing Page]** 訪問者がリダイレクトされる場所。

   ![ホームページにリダイレクト](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >ただし、 _[!UICONTROL Allow Browsing Category]_設定は web サイトのすべてのカテゴリに適用され、ストア表示ごとに異なるランディングページを設定できます。

### [!UICONTROL Display Product Prices]

このオプションは、 [web サイト](../getting-started/websites-stores-views.md).

次のメンバーのみを許可するには： **_特定の顧客グループ_** カテゴリ内の製品の価格を確認するには、次の手順を実行します。

1. 設定 **[!UICONTROL Display Product Prices]** から `Yes, for Specified Customer Groups`.

1. Adobe Analytics の **[!UICONTROL Customer Groups]** ボックスで、カテゴリ内の製品の価格を表示できる各グループを選択します。

   複数のグループを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各グループをクリックします。

   ![卸売顧客グループのみが価格を表示できます](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

このオプションは、 [web サイト](../getting-started/websites-stores-views.md).

次のメンバーのみを許可するには： **_特定の顧客グループ_** カテゴリ製品を買い物かごに入れるには、次の手順を実行します。

1. 設定 **[!UICONTROL Allow Adding to Cart]** から `Yes, for Specified Customer Groups`.

1. Adobe Analytics の **[!UICONTROL Customer Groups]** 」ボックスで、カテゴリから買い物かごに製品を追加できる各グループを選択します。

   複数のグループを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各グループをクリックします。

   ![卸売顧客グループのみが製品を買い物かごに入れることができます](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

このオプションを設定すると、特定の顧客グループのメンバーがカタログ検索を使用できなくなります。 これは、 [web サイト](../getting-started/websites-stores-views.md).

- 許可する手順は次のとおりです。 **_ログインした顧客のみ_** カタログ検索を使用するには、「 `NOT LOGGED IN`.

- 許可する手順は次のとおりです。 **_特定の顧客グループのみ_** 「カタログ検索」を使用するには、カテゴリ検索の使用から除外する各グループを選択します。

  複数のグループを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各グループをクリックします。

  ![一般顧客グループではカタログ検索は許可されていません](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## 手順 2：カテゴリ権限の適用

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーで、ターゲットカテゴリを選択します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** をクリックし、次の操作を実行します。

   - 権限ルールを作成するには、 **[!UICONTROL New Permission]**.

     ![カテゴリ権限セクション](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - 該当する項目を選択 **[!UICONTROL Website]** および **[!UICONTROL Customer Group]**.

   - 必要に応じて、個々の権限を設定します。

   >[!NOTE]
   >
   >条件 `Browsing Category` = `Deny` 権限は親カテゴリに対して設定されているので、この権限は [パンくずリスト](navigation-breadcrumb-trail.md) （子カテゴリページ上）

1. 完了したら、「 **[!UICONTROL Save]**.

>[!NOTE]
>
>存在する場合 **_許可_** 権限が `Root Category`に設定されている場合、これらの権限は自動的にすべてのサブカテゴリと、 `Catalog`. 製品が複数のカテゴリに割り当てられ、 **_許可_** 少なくとも 1 つのカテゴリの権限。自動的に同じ権限が割り当てられます **_許可_** 割り当てられたすべてのカテゴリの権限。
