---
title: 統合の設定
description: Adobe Commerce プロジェクトとExperience Manager Assets プロジェクトを連携して、2つのシステム間でアセットを同期する方法について説明します。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
TQID: https://experienceleague.adobe.com/c31KPRTUtXyMBCFiOEMPS7erhR3d-dQoxdB5ScgN1tk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 571
ht-degree: 3%

---

# 統合の設定

CommerceをAEM Assets インスタンスに接続し、アセットの同期に一致する方法を選択して、統合を設定します。

AEM Assets プロジェクトを特定したら、Adobe CommerceとAEM Assets間でアセットを同期するための一致するルールを選択します。

- **[!UICONTROL Match by product SKU]** - アセットが正しい商品に関連付けられていることを確認するために、アセットメタデータのSKUと[Commerce商品SKU](https://experienceleague.adobe.com/ja/docs/commerce-operations/implementation-playbook/glossary#sku)を一致させるデフォルトのルール。

- **[!UICONTROL Custom match]** – より複雑なシナリオまたはカスタム一致ロジックを必要とする特定のビジネス要件の一致ルール。 カスタムマッチングを実装するには、Adobe Developer App Builderでカスタムコードを開発して、アセットと商品のマッチング方法を定義する必要があります。 詳細については、近日公開予定です…

初期設定では、デフォルトの&#x200B;*製品SKU*&#x200B;による一致ルールを使用します。

## 前提条件

- [AEM Assets パッケージのインストール](aem-assets-configure-aem.md)

- [Adobe Commerce パッケージ &#x200B;](aem-assets-configure-commerce.md)をインストールして拡張機能を追加し、拡張機能を使用するために必要な資格情報と接続を生成します。

- Commerce向けAEM Assets統合の有効化をリクエストするためのサポートチケットを作成します。 チケットには、Commerceに接続するAEM Assets オーサリング環境用の&#x200B;**[!UICONTROL Program ID]**、**[!UICONTROL Environment ID]**&#x200B;および&#x200B;**[!UICONTROL IMS Org ID]**&#x200B;が含まれています。

- **[!UICONTROL Asset Selector IMS Client ID]**&#x200B;を指定してください。 *AEM Assets Selector* ドキュメントの[ImsAuthProps](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app)を参照してください。

## 接続の設定

1. [AEM Assets オーサリング環境](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) プロジェクトと環境IDを取得します。

   1. AEM Sites コンソールを開き、**[!UICONTROL Assets]**&#x200B;を選択します。

   1. プロジェクト IDと環境IDをURL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`からコピーして保存します
1. Commerce管理者から、AEM Assets統合設定を開きます。

   1. **[!UICONTROL Store]** / 設定/ **[!UICONTROL ADOBE SERVICES]** / **[!UICONTROL AEM Assets Integration]**&#x200B;に移動します。

      ![AEM Assets統合で統合を有効にする](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. AEM Assets環境&#x200B;**[!UICONTROL Program ID]**&#x200B;および&#x200B;**[!UICONTROL Environment ID]**&#x200B;にアクセスします。

   *[!UICONTROL Use system value]*&#x200B;から選択範囲を削除して、設定値を編集します。

1. **[!UICONTROL Asset Selector IMS Client ID]**&#x200B;を入力します。

   [Asset Selector IMS Client ID](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props)は、Commerce製品ページにビジュアルアセットを直接埋め込むことができるAEM Assets機能である[!UICONTROL Assets Selector]に必要です。

1. Commerceとアセットマッチングサービス間のリクエストを認証する場合は、[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)を選択します。

1. **[!UICONTROL Integration enabled]**&#x200B;を`Yes`に設定して、CommerceがAEM Assetsからの受信アップデートを受け入れるようにします。

   統合を有効にすると、アセットの一致条件を指定するための追加の設定オプションが使用できるようになります。

1. アセット同期の一致ルールを定義します。

   1. **[!UICONTROL Match by product SKU]**&#x200B;または&#x200B;**[!UICONTROL Custom match (Requires App Builder)]**&#x200B;を選択してください。

   1. 例えば、**[!UICONTROL Match by product SKU attribute name]** フィールドの`commerce:skus`に、Commerce製品SKUに定義されている[AEM Assets メタデータフィールド名](aem-assets-configure-aem.md#configure-metadata)を追加します。

1. **[!UICONTROL Save Config]**&#x200B;を選択して更新を適用し、アセットの同期を開始します。

   設定の更新により、最初の同期プロセスがトリガーされ、CommerceはAEM Assetsからの受信アップデートを受け入れることができます。 同期に必要な時間は、アセットの量と特定の設定によって異なります。 統合では、自動化されたプロセスを活用して、同期に必要な時間を最小限に抑えます。

### カスタムドメイン URLの設定

販売者がAEM ダッシュボードで[&#x200B; カスタムドメイン名](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/custom-domain-names/add-custom-domain-name){target=_blank}を設定した場合は、Commerceでこの&#x200B;**カスタムドメイン URL**&#x200B;を追加する必要があります。これにより、AEM Assets統合で使用できます。

1. **[!UICONTROL Store]** / 設定/ **[!UICONTROL ADOBE SERVICES]** / **[!UICONTROL AEM Assets Integration]**&#x200B;に移動します。

   ![AEM Assets統合で統合を有効にする](assets/aem-assets-view.png){width="600" zoomable="yes"}

1. **カスタムドメイン URL**&#x200B;を&#x200B;**[!UICONTROL Asset Custom Domain]** フィールドに追加します。

1. **[!UICONTROL Save Config]**&#x200B;をクリックして更新を適用し、アセットの同期を開始します。

## 次のステップ

[CommerceでのAEM Assetsの使用](aem-assets-manage.md)
