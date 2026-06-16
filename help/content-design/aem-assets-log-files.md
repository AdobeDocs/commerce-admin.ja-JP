---
title: ログのローテーションの設定
description: Commerce用AEM Assets統合のログローテーションを設定します。
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/I6iWurcyEbPi3fJmBZAnvbPlZfOJiSS4yGR6j5xFsp4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 0%

---

# Experience Manager Assetsの設定

Commerce用AEM Assets統合では、Commerce インスタンスに次のログファイルが提供されます。

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

システム管理者に、これらのログのログファイルのローテーションスケジュールを確認して、サイズが大きすぎないようにしてください。 一部の環境では、ログファイルは自動的にローテーションされますが、他の環境では手動でログローテーションを設定する必要があります。 詳しくは、次のトピックを参照してください。

- Adobe Commerce オンプレミスのインストールの場合は、システム管理者に[ ログローテーション ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings)の設定を依頼します。
- クラウドインフラストラクチャプロジェクト上のAdobe Commerceについては、[ ログの表示と管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html)を参照してください。
