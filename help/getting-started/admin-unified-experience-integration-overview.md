---
title: Commerce Admin のAdobe Experience Cloud統合
description: CommerceをExperience Cloudと統合して、ユーザーが拡張機能のホームページからCommerce プロジェクトにアクセスできるようにする管理Experience Cloud拡張機能について説明します。
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# CommerceのAdobe Experience Cloud統合

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce機能" src="../assets/adobe-logo.svg" width="20" height="20" /> Adobe Commerceのみの専用機能（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">詳細情報</a>）</td></tr>
</table>

管理者の統合エクスペリエンス拡張機能を有効にして、Adobe Commerce プロジェクトをExperience Cloudと統合します。 統合がアクティブになると、管理者はAdobe Experience CloudからCommerce プロジェクトにアクセスできます。

![Experience CloudのホームページからCommerceへのアクセス](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## 使用可能なCommerce プロジェクトの表示

管理者は、次を選択して、アクセス権限のあるCommerce プロジェクトを表示できます。 **[!UICONTROL Commerce]** Experience Cloudのホームページから。

![Experience CloudのCommerce プロジェクトワークスペース](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

管理者は、各プロジェクトの管理者およびストアフロントをから開くことができます [!DNL Commerce Projects] ワークスペースを開いて、追加情報を表示します。

- **Commerce ストアフロントのホームページのスナップショット**- ストアフロントのホームページのスナップショット。 プロジェクトに複数の web サイトがある場合、スナップショットには、デフォルトサイトのホームページが表示されます。

- **[プロジェクト名](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**- インスタンスのクラウドプロジェクト環境を識別します。 プロジェクト名のデフォルトはです。 [Git ブランチ名](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) クラウドプロジェクト内。 でプロジェクト名を変更または更新する [統合 Experience ストアの設定](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[ストアフロント URL](../stores-purchase/store-urls.md)**— デフォルトの Web サイトのベース URL を表示します。

- **[環境タイプ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** – 開発環境またはステージング環境にデプロイされたCommerce インスタンスは、 [!UICONTROL Development] または [!UICONTROL Staging] ラベル。 ラベルのないインスタンスは、実稼動環境にデプロイされます。

- **Commerce管理者アクセス** – をクリックして管理者を開きます。 **[!UICONTROL Open]**.

- **ストアフロントへのアクセス** – 選択してストアフロントを開きます。 **[!UICONTROL Open storefront]** 「オプション」メニューから選択します。

- **プロジェクトを選択するためのクイックアクセス** – 選択 **[!UICONTROL Add to Favorites]** オプションメニューからにプロジェクトを追加する [!UICONTROL Favorites] タブ。

## 認証フロー

Experience Cloudの統合が有効な場合、管理者は次のワークフローを使用してCommerce プロジェクトの認証を行い、プロジェクトにアクセスします。

1. Experience Cloudのログインページからログインします。

   ![Experience Cloudのログインページ](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   管理者は、Commerce インスタンスに関連付けられている組織のAdobeビジネスプロファイルを使用して、Experience Cloudにログインする必要があります。 参照： [Adobeプロファイルの管理](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Experience Cloudのホームページで、 [!UICONTROL Commerce Projects workspace] 選択による **[!UICONTROL Open]**.

1. を選択して、プロジェクトの管理者にアクセスします。 **[!UICONTROL Open]**.

1. Adobe Commerceのログインページで、 **[!UICONTROL Sign in with Adobe ID]** をクリックして認証を完了し、管理者を開きます。

   ![Adobe Commerceのログインページ](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>参照： [Experience Cloud統合の管理](admin-unified-experience-integration-manage.md) Experience Cloud統合が有効または無効な場合に認証ワークフローが影響を受ける方法の詳細を説明します。

## 要件

- Adobe Commerce 2.4.5 以降
- クラウドインフラストラクチャー上のAdobe Commerce
- Adobe Commerce拡張機能

   - Commerce Admin Unified Experience 拡張機能（`magento/module-unified-experience`）

     モジュールがCommerce インスタンスで使用できない場合は、Composer を使用してインストールできます。

   - [Adobe I/Oイベントサービス](https://developer.adobe.com/commerce/extensibility/events/)- Experience CloudからCommerce プロジェクトへの管理者アクセスを管理するために、イベントデータを送信する必要があります。

     CommerceとのAdobe I/Oイベント統合は、Commerce イベント拡張機能（`magento/commerce-eventing`）に含まれています。Adobe Commerce 2.4.4 以降のバージョンで使用できます。

## 統合の有効化

次の手順に従って、統合を有効にします。 [Commerce Admin とのExperience Cloud統合の設定](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Commerce インスタンスでExperience Cloud統合が既に有効になっている場合は、以下を参照してください。 [Experience Cloud統合の管理](admin-unified-experience-integration-manage.md) 設定の変更または更新、管理者アクセスの管理、トラブルシューティングについて詳しくは、
