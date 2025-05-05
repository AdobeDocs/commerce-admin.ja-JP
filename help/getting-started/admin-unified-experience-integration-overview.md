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
<tr><td><img alt="Adobe Commerce機能" src="../assets/adobe-logo.svg" width="20" height="20" /> Adobe Commerceのみの専用機能（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=ja#product-editions"> 詳細情報 </a>）</td></tr>
</table>

管理者の統合エクスペリエンス拡張機能を有効にして、Adobe Commerce プロジェクトをExperience Cloudと統合します。 統合がアクティブになると、管理者はAdobe Experience CloudからCommerce プロジェクトにアクセスできます。

![Experience CloudホームページからCommerceへのアクセス ](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## 使用可能なCommerce プロジェクトの表示

管理者は、Experience Cloudのホームページから「プロジェクト」を選択して、アクセス権 **[!UICONTROL Commerce]** 持つCommerce プロジェクトを表示できます。

![Experience CloudのCommerce プロジェクトワークスペース ](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

管理者は、各プロジェクトの管理者とストアフロントを [!DNL Commerce Projects] Workspace から開いて、追加情報を表示できます。

- **Commerce ストアフロントのホームページのスナップショット** - ストアフロントのホームページのスナップショット。 プロジェクトに複数の web サイトがある場合、スナップショットには、デフォルトサイトのホームページが表示されます。

- **[プロジェクト名 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=ja)** - インスタンスのクラウドプロジェクト環境を識別します。 プロジェクト名のデフォルトは、クラウドプロジェクトの [Git ブランチ名 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html?lang=ja) です。 [ 統合エクスペリエンスストアの設定 ](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin) でプロジェクト名を変更または更新します。

- **[ストアフロント URL](../stores-purchase/store-urls.md)** - デフォルトの web サイトのベース URL を表示します。

- **[環境タイプ ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=ja)** – 開発環境またはステージング環境にデプロイされたCommerce インスタンスは、[!UICONTROL Development] ラベルまたは [!UICONTROL Staging] ラベルで識別されます。 ラベルのないインスタンスは、実稼動環境にデプロイされます。

- **Commerce管理者アクセス** - 「**[!UICONTROL Open]**」をクリックして管理者を開きます。

- **ストアフロントへのアクセス** - オプションメニューから「**[!UICONTROL Open storefront]**」を選択してストアフロントを開きます。

- **プロジェクトを選択するためのクイックアクセス** - オプションメニューから「**[!UICONTROL Add to Favorites]**」を選択して、「[!UICONTROL Favorites]」タブにプロジェクトを追加します。

## 認証フロー

Experience Cloudの統合が有効な場合、管理者は次のワークフローを使用してCommerce プロジェクトの認証を行い、プロジェクトにアクセスします。

1. Experience Cloudのログインページからログインします。

   ![Experience Cloudサインイン ページ ](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   管理者は、Commerce インスタンスに関連付けられている組織のAdobeビジネスプロファイルを使用して、Experience Cloudにログインする必要があります。 [Adobeプロファイルの管理 ](https://helpx.adobe.com/jp/enterprise/using/manage-adobe-profiles.html) を参照してください。

1. Experience Cloudのホームページで、「**[!UICONTROL Open]**」を選択して [!UICONTROL Commerce Projects workspace] を開きます。

1. **[!UICONTROL Open]** を選択して、プロジェクトの管理者にアクセスします。

1. Adobe Commerceのログインページで、「**[!UICONTROL Sign in with Adobe ID]**」を選択して認証を完了し、管理者を開きます。

   ![Adobe Commerceのサインイン ページ ](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Experience Cloud統合を有効または無効にすると認証ワークフローに与える影響について詳しくは、[Experience Cloud統合の管理 ](admin-unified-experience-integration-manage.md) を参照してください。

## 要件

- Adobe Commerce 2.4.5 以降
- クラウドインフラストラクチャー上のAdobe Commerce
- Adobe Commerce拡張機能

   - Commerce Admin Unified Experience Extension （`magento/module-unified-experience`）

     モジュールがCommerce インスタンスで使用できない場合は、Composer を使用してインストールできます。

   - [Adobe I/Oイベントサービス ](https://developer.adobe.com/commerce/extensibility/events/) - Experience CloudからCommerce プロジェクトへの管理者アクセスを管理するために、イベントデータを送信する必要があります。

     CommerceとのAdobe I/Oイベント統合は、Adobe Commerce 2.4.4 以降のバージョンで使用できるCommerce Event Extension （`magento/commerce-eventing`）によって有効になります。

## 統合の有効化

[Commerce管理者とExperience Cloud統合を設定する ](admin-unified-experience-integration-configure.md) 手順に従って、統合を有効にします。

>[!TIP]
>
>Experience Cloud統合が既にCommerce インスタンスで有効になっている場合は、設定の変更または更新、管理者アクセスの管理、トラブルシューティングについて詳しくは [Experience Cloud統合の管理 ](admin-unified-experience-integration-manage.md) を参照してください。
