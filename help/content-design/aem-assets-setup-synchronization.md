---
title: アセット同期の有効化
description: Adobe Commerce プロジェクトとExperience Manager Assets プロジェクトを接続して、これら 2 つのシステム間のアセット同期を有効にする方法を説明します。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# アセット同期の有効化

>[!BEGINSHADEBOX]

**前提条件**

- [Commerce アセットを管理するためのAEM Experience Manager Assetsの設定](#aem-assets-configure-aem)
- [CommerceのAEM Assets統合をインストールおよび設定 ](#aem-assets-configure-commerce.md) して、拡張機能を追加し、拡張機能を使用するために必要な資格情報と接続を生成します。

>[!ENDSHADEBOX]

このイネーブルメントプロセスでは、AEM オーサリング環境用のプログラム ID と環境 ID を指定して、テナント ID を登録します。 これらの ID は、接続先のAEM Assets プロジェクトを特定し、CommerceとAEM Assetsの間の通信とワークフローを有効にするための資格情報を提供します。

AEM Assets プロジェクトを特定したら、Adobe CommerceとAEM Assets間のアセットの同期に使用する一致ルールを選択します。

Adobe CommerceのAEM Assets統合では、CommerceとAEM Assetsの間でアセットを同期するための 2 つの一致するルールをサポートしています。

- **製品 SKU による一致** – これは、製品の最小在庫管理単位（SKU）に基づいてアセットに一致するデフォルトの一致ルールです。 SKU は、各製品の一意の ID です。 このルールは、アセットメタデータの SKU をCommerce製品 SKU と照合し、アセットが正しい製品に関連付けられていることを確認します。

- **カスタム一致** – この一致ルールは、カスタム一致ロジックが必要なより複雑なシナリオや特定のビジネス要件に使用します。 このルールを使用するには、アセットと商品のマッチング方法を定義するカスタムコードをAdobe Developer App Builderに実装する必要があります。 詳細は近日公開予定です…

最初のオンボーディングでは、デフォルトの `Match by product sku` ルールを使用します。 必要に応じて、後で一致ルールを変更できます。

## 統合の有効化

1. [AEM Assets オーサリング環境 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) のプロジェクトと環境 ID を取得します。

   1. AEM Sites コンソールを開き、「**[!UICONTROL Assets]**」を選択します。

   1. 次の URL からプロジェクト ID と環境 ID をコピーして保存します。<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Commerce Admin から、AEM Assets Integration configuration を開きます。

   1. **[!UICONTROL Store]**/設定/**[!UICONTROL CATALOG]**/**[!UICONTROL Catalog]** を選択します。

   1. **[!UICONTROL Experience Manager Assets integration]** を展開します。

      ![AEM Assets統合：統合の有効化 ](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. **[!UICONTROL Program ID]** と **[!UICONTROL Environment ID]** を入力して、接続先のExperience Manager Assets プロジェクトを特定します。

1. **[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)** を選択して（例：`Assets integration`）、Adobe Commerceと ARES サービスの間で API リクエストを認証するための OAUTH 資格情報を追加します。

1. **[!UICONTROL Enable integration]** を `Yes` に設定して、CommerceがAEM Assetsから受信する更新を受け入れるようにします。

   統合を有効にした後、アセットの一致ルールを設定できます。

   ![AEM Assets統合でアセットの一致ルールを選択 ](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. アセット同期の一致ルールを定義します。

   1. 「**[!UICONTROL Match by product SKU]**」を選択します。

   1. Commerce製品 SKU に対して定義された ](aem-assets-configure-aem.md#configure-metadata)0}AEM Assets メタデータフィールド名を **[!UICONTROL Match by product SKU attribute name]** フィールドに追加します（例：`commerce:skus`）。[

1. 設定を適用し、**[!UICONTROL Save Config]** を選択して同期プロセスを開始します。
