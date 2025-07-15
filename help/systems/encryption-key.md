---
title: 暗号化キー
description: セキュリティを向上させるために定期的に行う必要がある、独自の暗号化キーの変更方法を説明します。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 4968c40cd6f8a47ea595db20ed5d77c11e134db6
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# 暗号化キー

>[!NOTE]
>
>これらの手順を実行しようとして問題が発生した場合は、ナレッジベースの記事 [ 暗号化キーのローテーションのトラブルシューティング：CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102)」を参照してください。

Adobe CommerceとMagento Open Sourceでは、パスワードやその他の機密データを保護するために暗号化キーを使用します。 業界標準の [!DNL ChaCha20-Poly1305] アルゴリズムは、暗号化が必要なすべてのデータを暗号化するために 256 ビットキーと共に使用されます。 これには、クレジットカードのデータや統合（支払いおよび配送モジュール）のパスワードが含まれます。 さらに、強力なセキュアハッシュアルゴリズム（SHA-256）を使用して、復号化を必要としないすべてのデータをハッシュ化します。

最初のインストールでは、Commerceに暗号化キーを生成させるか、独自の暗号化キーを入力するかを尋ねるプロンプトが表示されます。 暗号化キーツールを使用すると、必要に応じてキーを変更できます。 セキュリティを向上させるには、暗号化キーを定期的に変更する必要があります。また、元のキーが侵害される可能性はいつでも生じます。

技術情報については、[ インストール ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) の _高度なオンプレミスのインストール_ および [PHP 開発者ガイド ](https://developer.adobe.com/commerce/php/development/security/data-encryption/) の _データの再暗号化_ を参照してください。

>[!IMPORTANT]
>
>- これらの手順に従って暗号化キーを変更する前に、次のファイルが書き込み可能であることを確認してください：`[your store]/app/etc/env.php`
>- 管理設定の暗号化キーの変更機能は非推奨（廃止予定）で、2.4.8 で削除されました。2.4.8 にアップグレードした後に暗号化キーを変更するには、このページで説明されている CLI コマンドを使用する必要があります。
>- 暗号化キーを回転すると、すべての顧客セッションと管理者セッション（統合ユーザーを除く）が直ちに無効になり、再度ログインする必要があります。

**暗号化キーを変更するには：**

次の手順では、ターミナルにアクセスする必要があります。

1. [ メンテナンスモード ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode) を有効にします。

   ```bash
   bin/magento maintenance:enable
   ```

1. cron ジョブを無効にします。

   _クラウドインフラストラクチャプロジェクト：_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _オンプレミス プロジェクト_

   ```bash
   crontab -e
   ```

1. 次のいずれかの方法を使用して、暗号化キーを変更します。

   +++CLI コマンド

   新しいコマンドが存在することを確認します。

   ```bash
   bin/magento list | grep encryption:key:change
   ```

   次の出力が表示されます。

   ```bash
   encryption:key:change Change the encryption key inside the env.php file.
   ```

   この出力が表示された場合は、次の CLI コマンドを実行し、エラーなしで完了することを確認します。 特定のシステム設定値または支払いフィールドを再暗号化する必要がある場合は、[PHP 開発ガイド ](https://developer.adobe.com/commerce/php/development/security/data-encryption/) の詳細な _再暗号化に関するガイド_ を参照してください。

   ```bash
   bin/magento encryption:key:change
   ```

+++

   +++管理設定

   >[!IMPORTANT]
   >
   >この機能は廃止され、2.4.8 で削除されました。Adobeでは、CLI を使用して暗号化キーを変更することをお勧めします。

   1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Other Settings]_/**[!UICONTROL Manage Encryption Key]**に移動します。

      ![ システム暗号化キー ](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. 次のいずれかの操作を行います。

      - 新しいキーを生成するには、**[!UICONTROL Auto-generate Key]** を `Yes` に設定します。
      - 別のキーを使用するには、**[!UICONTROL Auto-generate Key]** を `No` に設定します。 次に、「**[!UICONTROL New Key]**」フィールドに、使用するキーを入力または貼り付けます。

   1. 「**[!UICONTROL Change Encryption Key]**」をクリックします。

      >[!NOTE]
      >
      >新しいキーを安全な場所に記録します。 ファイルに問題が発生した場合は、データを復号化する必要があります。

+++

1. キャッシュをフラッシュします。

   _クラウドインフラストラクチャプロジェクト：_

   ```bash
   magento-cloud cc
   ```

   _オンプレミス プロジェクト：_

   ```bash
   bin/magento cache:flush
   ```

1. cron ジョブを有効にします。

   _クラウドインフラストラクチャプロジェクト：_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _オンプレミス プロジェクト：_

   ```bash
   crontab -e
   ```

1. メンテナンスモードを無効にします。

   ```bash
   bin/magento maintenance:disable
   ```
