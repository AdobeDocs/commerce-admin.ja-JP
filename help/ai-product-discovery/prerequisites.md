---
title: AI製品の発見の前提条件
description: カタログのエンリッチメントとPDPのエンリッチメントの要件を確認し、クラウドインフラストラクチャまたはオンプレミスのAdobe Commerceにshared enrichment拡張機能をインストールします。
role: Admin, Developer
source-git-commit: 591fca4f18862d289fb233997e8848cb4692d1e7
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%
---
# 前提条件

カタログのエンリッチメントまたはPDP エンリッチメントを使用する前に、すべてのデプロイメントに適用される要件を確認し、Commerce プラットフォームの設定を完了します。

## すべてのデプロイメントの要件 {#all-deployments}

| 要件 | 適用先 | 詳細 |
| --- | --- | --- |
| Edgeでの最適化 | PDPの強化 | 必須。 Optimize at Edgeは、強化された商品データをAI エージェントに提供します。 Edgeでの最適化に関するガイド [&#128279;](https://experienceleague.adobe.com/ja/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)を参照してください。 |
| ログ転送 | 両方のワークフロー | オプション。 エージェント型トラフィックにもとづいてエンリッチメントのレコメンデーションを可能にします。 この機能がなければ、製品ページや製品ページを手動で選択することもできます。 [&#x200B; ログ転送ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/brand-visibility/using/log-forwarding/log-forwarding-overview)を参照してください。 |
| クローラブルストアフロント | カタログの強化 | クロールベースのレコメンデーションに必要です。 LLM指向およびエージェント型のボットは、商品ページにアクセスできる必要があります。 |
| [!DNL Adobe Admin Console] アクセス | 両方のワークフロー | 必須。 セットアップ中、[!DNL Adobe Commerce]は組織のGenAI ライダーのステータスを確認します。 組織がGenAI ライダーをオプトアウトしない限り、アクセスできます。 |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
-->

## Commerceプラットフォームの設定 {#set-up}

>[!BEGINTABS]

>[!TAB Commerce on Cloud インフラストラクチャまたはオンプレミス ]

クラウド インフラストラクチャまたはオンプレミスの[!DNL Adobe Commerce]の場合、共有エンリッチメント拡張機能をインストールすると、カタログ エンリッチメントとPDP エンリッチメントの両方が有効になります。

**開始する前：**

- [!DNL Adobe Commerce] 2.4.7以降（PHP 8.3以降）。 [&#x200B; リリースノート &#x200B;](release-notes.md)を参照してください。
- [!DNL Adobe IMS]組織。 お客様の組織に統合機能がない場合は、[Adobe IMS統合の概要](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview)を参照してください。 カタログのエンリッチメントでは、サインイン済みの管理者ユーザーのIMS アクセストークンを使用します。 Commerceのユーザー名とパスワードのみでログインすると、このトークンは提供されません。
- Commerce アプリケーションサーバーへのコマンドラインアクセスと、`repo.magento.com`からパッケージをダウンロードする権限。

**インストールして確認：**

1. [!DNL Live Search]も[!DNL Product Recommendations]も有効になっていない場合は、Commerce プロジェクトディレクトリから[!DNL Catalog Service]を追加します。

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service]は[!DNL Live Search]および[!DNL Product Recommendations]と共に自動的にインストールされるので、いずれかのサービスが有効になっている場合は、この手順をスキップしてください。

1. 別のCommerce サービス用にまだ設定されていない場合は、API キーとSaaS データスペースを使用して[Commerce サービスコネクタ &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/user-guides/integration-services/saas)を設定します。

1. 共有エンリッチメント拡張機能を追加します。

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. 変更をデプロイします。

   - **クラウド インフラストラクチャ：**&#x200B;変更をコミットして`composer.json`および`composer.lock`にプッシュします。
   - **オンプレミス：** アプリケーションをアップグレードし、キャッシュをクリアします。

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. 管理画面で、**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**&#x200B;に移動し、Commerceがカタログデータを書き出すことを確認します。

   正常に送信された製品レコードの数は、ソースレコードと一致する必要があり、失敗したり、送信を待ったりすることはありません。 失敗したレコードの場合は、エラーの詳細を確認し、問題を解決して、影響を受けるレコードの再同期をスケジュールします。

1. **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]**&#x200B;に移動し、想定されるカタログデータが[!DNL Catalog Service]で使用可能であることを確認します。

ステータスの詳細とトラブルシューティングについては、[&#x200B; データフィードのステータスの監視](/help/systems/data-feed-sync-status.md#monitor-data-feed-status)を参照してください。

>[!TAB Adobe Commerce as a Cloud Service]

[!DNL Adobe Commerce as a Cloud Service]の場合、[!DNL Catalog Service]のインストール、カタログ エンリッチメント、およびPDP エンリッチメントは、アカウントのプロビジョニング中に処理されます。

使用するワークフローに適用されるすべてのデプロイメント [&#128279;](#all-deployments)の要件を完了します。

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## 次のステップ {#next-step}

[&#x200B; エンリッチメント設定](settings.md)を設定して、Commerce インスタンスをAI Product Discoveryに接続します。
