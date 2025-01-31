---
title: アセット同期の有効化
description: Adobe Commerce プロジェクトとExperience Manager Assets プロジェクトを接続して、これら 2 つのシステム間のアセット同期を有効にする方法を説明します。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e9b3ede8945de0a6ed0cdb02e5675d736764d3e4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# アセット同期の有効化

イネーブルメントプロセスでは、AEM オーサリング環境のプログラム ID と環境 ID を使用して、プロジェクトのテナント ID を登録します。 これらの ID は、接続先のAEM Assets プロジェクトを特定し、Commerce環境とAEM Assets環境間の通信を有効にするための資格情報を提供します。

AEM Assets プロジェクトを識別したら、Adobe CommerceとAEM Assetsの間でアセットを同期するための一致ルールを選択します。

- **[!UICONTROL Match by product SKU]** - アセットが正しい商品に関連付けられるようにするために、アセットメタデータの SKU を ](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku)1}Commerce商品 SKU} と一致させるデフォルトのルール。[

- **[!UICONTROL Custom match]** - カスタム・マッチング・ロジックを必要とするより複雑なシナリオや特定のビジネス要件の照合ルール。 カスタムマッチングを実装するには、アセットと商品のマッチング方法を定義するカスタムコードをAdobe Developer App Builderで開発する必要があります。 詳細は近日公開予定です…

最初のオンボーディングでは、デフォルトの *製品 SKU で一致* ルールを使用します。

## 前提条件

- [Commerce アセットを管理するためのAEM Experience Manager Assetsの設定](#aem-assets-configure-aem)

- [CommerceのAEM Assets統合をインストールおよび設定 ](#aem-assets-configure-commerce.md) して、拡張機能を追加し、拡張機能を使用するために必要な資格情報と接続を生成します。

- AEM Assets統合の有効化をリクエストするサポートチケットを作成します。 **[!UICONTROL Program ID]**、**[!UICONTROL Environment ID]**、**[!UICONTROL IMS Org ID]** を指定する必要があります。

  >[!TIP]
  >
  > （オプション） **[!UICONTROL Asset Selector IMS Client ID]** を指定します（使用可能な場合）。

## 接続の設定

1. [AEM Assets オーサリング環境 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) プロジェクトおよび環境 ID を取得します。

   1. AEM Sites コンソールを開き、「**[!UICONTROL Assets]**」を選択します。

   1. 次の URL からプロジェクト ID と環境 ID をコピーして保存します。<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Commerce Admin から、AEM Assets Integration configuration を開きます。

   1. **[!UICONTROL Store]**/設定/**[!UICONTROL ADOBE SERVICES]**/**[!UICONTROL AEM Assets Integration]** に移動します。

      ![AEM Assets統合：統合の有効化 ](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. AEM Assets環境 **[!UICONTROL Program ID]** と **[!UICONTROL Environment ID]** を入力します。

1. 使用可能な場合は、**[!UICONTROL Asset Selector IMS Client ID]** を入力します。

   [[!UICONTROL Assets Selector]](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/overview-asset-selector) では、[IMS ID](../getting-started/adobe-ims-config.md) が必要です。これにより、カテゴリや [!DNL Page Builder] の画像が選択されます。

1. Commerceとアセット照合サービスの間でリクエストを認証する [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) を選択します。

1. **[!UICONTROL Integration enabled]** を `Yes` に設定して、CommerceがAEM Assetsから受信する更新を受け入れるようにします。

   統合を有効にした後、アセットの一致ルールを設定します。

   ![AEM Assets統合でアセットの一致ルールを選択 ](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. アセット同期の一致ルールを定義します。

   1. 「**[!UICONTROL Match by product SKU]**」を選択します。

   1. Commerce製品 SKU に対して定義された ](aem-assets-configure-aem.md#configure-metadata)0}AEM Assets メタデータフィールド名を **[!UICONTROL Match by product SKU attribute name]** フィールドに追加します（例：`commerce:skus`）。[

   ![AEM Assets統合でアセットの一致ルールを選択 ](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]** を選択して更新を適用し、アセットの同期を開始します
