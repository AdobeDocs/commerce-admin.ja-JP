---
title: アセット同期の有効化
description: Adobe Commerce プロジェクトとExperience Manager Assets プロジェクトを接続して、これら 2 つのシステム間のアセット同期を有効にする方法を説明します。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: d8e255259e4a8b87c63a4d1c013b4c1feb2b29cb
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# アセット同期の有効化

CommerceをAEM Assets インスタンスに接続するようにCommerce環境設定を更新して、アセットの同期を有効にします。 統合により、CommerceとAEM Assetsの間でアセットを同期できるので、商品イメージやその他のアセットを常に最新の状態に保つことができます。

AEM Assets プロジェクトを特定した後、Adobe CommerceとAEM Assetsの間でアセットを同期するための一致ルールを選択します。

- **[!UICONTROL Match by product SKU]** - アセットが正しい商品に関連付けられるようにするために、アセットメタデータの SKU を ](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/glossary#sku)1}Commerce商品 SKU} と一致させるデフォルトのルール。[

- **[!UICONTROL Custom match]** - カスタム・マッチング・ロジックを必要とするより複雑なシナリオや特定のビジネス要件の照合ルール。 カスタムマッチングを実装するには、アセットと商品のマッチング方法を定義するカスタムコードをAdobe Developer App Builderで開発する必要があります。 詳細は近日公開予定です…

最初のオンボーディングでは、デフォルトの *製品 SKU で一致* ルールを使用します。

## 前提条件

- [Commerce アセットを管理するためのAEM Assetsの設定](aem-assets-configure-aem.md)

- [CommerceのAEM Assets統合をインストールおよび設定 ](aem-assets-configure-commerce.md) して、拡張機能を追加し、拡張機能を使用するために必要な資格情報と接続を生成します。

- AEM Assets統合の有効化をリクエストするサポートチケットを作成します。 Commerceに接続するAEM Assets オーサリング環境用の **[!UICONTROL Program ID]**、**[!UICONTROL Environment ID]** および **[!UICONTROL IMS Org ID]** を指定する必要があります。

  >[!TIP]
  >
  > （オプション） **[!UICONTROL Asset Selector IMS Client ID]** を指定します（使用可能な場合）。 [2}AEM Assets Selector](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app) ドキュメントの {ImsAuthProps *を参照してください。*

## 接続の設定

1. [AEM Assets オーサリング環境 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) プロジェクトおよび環境 ID を取得します。

   1. AEM Sites コンソールを開き、「**[!UICONTROL Assets]**」を選択します。

   1. 次の URL からプロジェクト ID と環境 ID をコピーして保存します。<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. Commerce Admin から、AEM Assets Integration configuration を開きます。

   1. **[!UICONTROL Store]**/設定/**[!UICONTROL ADOBE SERVICES]**/**[!UICONTROL AEM Assets Integration]** に移動します。

      ![AEM Assets統合：統合の有効化 ](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. AEM Assets環境 **[!UICONTROL Program ID]** と **[!UICONTROL Environment ID]** を入力します。

   *[!UICONTROL Use system value]* から選択内容を削除して、設定値を編集します。

1. 使用可能な場合は、**[!UICONTROL Asset Selector IMS Client ID]** を入力します。

   [ アセットセレクター IMS クライアント ID](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props) は、[!UICONTROL Assets Selector] に必要です。これは、ユーザーがCommerce製品ページに直接ビジュアルアセットを埋め込むことができるAEM Assets機能です。

1. Commerceとアセット照合サービスの間でリクエストを認証する [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) を選択します。

1. **[!UICONTROL Integration enabled]** を `Yes` に設定して、CommerceがAEM Assetsからの受信アップデートを受け入れるようにします。

   統合を有効にすると、アセットの一致条件を指定するために、追加の設定オプションを使用できます。

1. アセット同期の一致ルールを定義します。

   1. **[!UICONTROL Match by product SKU]** または **[!UICONTROL Custom match (Requires App Builder)]** を選択します。

   1. Commerce製品 SKU に対して定義された ](aem-assets-configure-aem.md#configure-metadata)0}AEM Assets メタデータフィールド名を **[!UICONTROL Match by product SKU attribute name]** フィールドに追加します（例：`commerce:skus`）。[

1. 「**[!UICONTROL Save Config]**」を選択すると、更新を適用し、アセットの同期を開始します。

   設定のアップデートは、初期同期プロセスをトリガーし、CommerceがAEM Assetsから受信するアップデートを受け入れるようにします。同期に要する時間は、アセットのボリュームと具体的な設定によって異なります。 この統合では、自動化されたプロセスを活用して、同期に要する時間を最小限に抑えます。

## 次の手順

[CommerceでのAEM Assetsの使用](aem-assets-manage.md)
