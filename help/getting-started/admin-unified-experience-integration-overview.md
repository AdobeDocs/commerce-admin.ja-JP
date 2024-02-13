---
title: Adobe Experience Cloud Commerce Admin との統合
description: ユーザーがExperience Cloudのホームページからコマースプロジェクトにアクセスできるように、コマースとExperience Cloudを統合する Admin Unified Experience 拡張機能について説明します。
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: a07c91bc2f01cd110f3e0ccd6d27fe5d37eb2fc9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Adobe Experience Cloud Commerce 統合

{{ee-feature}}

管理 Unified Experience 拡張機能を有効にして、Adobe CommerceプロジェクトをExperience Cloudと統合します。 統合がアクティブな場合、管理者はAdobe Experience Cloudから Commerce プロジェクトにアクセスできます。

![コマースホームページからExperience Cloudにアクセス](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## 使用可能な Commerce プロジェクトを表示

管理者は、アクセス権を持つコマースプロジェクトを表示するには、次を選択します： **[!UICONTROL Commerce]** をExperience Cloudホームページから

![Commerce Projects ワークスペース (Experience Cloud)](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

管理者は、各プロジェクトの管理者とストアフロントを [!DNL Commerce Projects] ワークスペースを開き、追加情報を表示します。

- **Commerce ストアフロントホームページのスナップショット** — ストアフロントホームページのスナップショット。 プロジェクトに複数の Web サイトがある場合、スナップショットには、デフォルトサイトのホームページが表示されます。

- **[プロジェクト名](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** — インスタンスのクラウドプロジェクト環境を識別します。 プロジェクト名のデフォルト値はです。 [Git ブランチ名](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) クラウドプロジェクト内で使用されます。 内のプロジェクト名を変更または更新する [統合エクスペリエンスストアの構成設定](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[ストアフロント URL](../stores-purchase/store-urls.md)** — デフォルトの Web サイトのベース URL を表示します。

- **[環境タイプ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** — 開発環境またはステージング環境にデプロイされたコマースインスタンスは、 [!UICONTROL Development] または [!UICONTROL Staging] ラベル。 ラベルのないインスタンスは、実稼動環境にデプロイされます。

- **コマース管理者アクセス** — クリックして管理者を開きます。 **[!UICONTROL Open]**.

- **ストアフロントアクセス** — 「 」を選択してストアフロントを開きます。 **[!UICONTROL Open storefront]** を選択します。

- **選択したプロジェクトにすばやくアクセス** — 選択 **[!UICONTROL Add to Favorites]** オプションメニューから、 [!UICONTROL Favorites] タブをクリックします。

## 認証フロー

Experience Cloudの統合が有効な場合、管理者は次のワークフローを使用して、コマースプロジェクトを認証し、アクセスします。

1. 「ログイン」ページでExperience Cloudにログインします。

   ![Experience Cloudログインページ](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   管理者は、コマースインスタンスに関連付けられている組織のAdobeビジネスプロファイルを使用してExperience Cloudにサインインする必要があります。 詳しくは、 [Adobeプロファイルの管理](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Experience Cloudのホームページで、 [!UICONTROL Commerce Projects workspace] 選択する **[!UICONTROL Open]**.

1. 「 」を選択して、プロジェクトの管理者にアクセスします。 **[!UICONTROL Open]**.

1. Adobe Commerceログインページで、「 」を選択します。 **[!UICONTROL Sign in with Adobe ID]** 認証を完了し、管理者を開きます。

   ![Adobe Commerceログインページ](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>詳しくは、 [Experience Cloud統合の管理](admin-unified-experience-integration-manage.md) 認証統合が有効または無効の場合の認証Experience Cloudの影響の詳細。

## 要件

- Adobe Commerce 2.4.5 以降
- Adobe Commerce an cloud infrastructure
- Adobe Commerce拡張機能

   - コマース管理 Unified Experience 拡張機能 (`magento/module-unified-experience`)

     このモジュールがコマースインスタンスで使用できない場合、Composer を使用してインストールできます。

   - [Adobe I/Oイベントサービス](https://developer.adobe.com/commerce/extensibility/events/)- Commerce プロジェクトへの管理者アクセスを管理するために、イベントデータをExperience Cloudから送信するために必要です。

     コマースとのAdobe I/Oイベントの統合は、コマースイベント拡張 (`magento/commerce-eventing`) で利用できます ( Adobe Commerce 2.4.4 以降のバージョンで利用できます )。

## 統合の有効化

次の手順に従って、統合を有効にします。 [コマース管理とのExperience Cloud統合の設定](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>コマースインスタンスでExperience Cloudの統合が既に有効になっている場合は、 [Experience Cloud統合の管理](admin-unified-experience-integration-manage.md) 設定の変更または更新、管理者アクセスの管理、トラブルシューティングの詳細。
