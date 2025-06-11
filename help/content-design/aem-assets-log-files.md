---
title: ログのローテーションの設定
description: CommerceのAEM Assets統合のログローテーションを設定します。
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Experience Manager Assetsの設定

AEM Assets Integration for Commerceは、Commerce インスタンスに次のログファイルを提供します。

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

これらのログが大きくなりすぎないようにするには、システム管理者にこれらのログのログファイル回転スケジュールを確認するように依頼してください。 環境によっては、ログファイルが自動的にローテーションされますが、それ以外の環境では、ログローテーションを手動で設定する必要があります。 詳しくは、次のトピックを参照してください。

- Adobe Commerceのオンプレミスインストールの場合は、システム管理者に依頼して [ ログローテーション ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=ja#server-settings) を設定します。
- クラウドインフラストラクチャプロジェクトのAdobe Commerceについては、[ ログの表示と管理 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html?lang=ja) を参照してください。
