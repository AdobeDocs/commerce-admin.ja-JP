---
title: 暗号化キー
description: セキュリティを向上させるために定期的に変更する必要がある、独自の暗号化キーを自動生成または追加する方法を説明します。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 65c15bb84b28088a6e8f06f3592600779ba033f5
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# 暗号化キー

>[!NOTE]
>
>これらの手順を実行しようとして問題が発生した場合は、ナレッジベースの記事 [ 暗号化キーのローテーションのトラブルシューティング：CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102)」を参照してください。

Adobe CommerceとMagento Open Sourceは、パスワードやその他の機密データを保護するために暗号化キーを使用します。 業界標準の [!DNL ChaCha20-Poly1305] アルゴリズムは、暗号化が必要なすべてのデータを暗号化するために 256 ビットキーと共に使用されます。 これには、クレジットカードのデータや統合（支払いおよび配送モジュール）のパスワードが含まれます。 さらに、強力なセキュアハッシュアルゴリズム（SHA-256）を使用して、復号化を必要としないすべてのデータをハッシュ化します。

最初のインストールでは、Commerceに暗号化キーを生成させるか、独自の暗号化キーを入力するかを尋ねるプロンプトが表示されます。 暗号化キーツールを使用すると、必要に応じてキーを変更できます。 セキュリティを向上させるには、暗号化キーを定期的に変更する必要があります。また、元のキーが侵害される可能性はいつでも生じます。

技術情報については、[ インストール ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) の _オンプレミスの高度なインストール_ を参照してください。

>[!IMPORTANT]
>
>これらの手順に従って暗号化キーを変更する前に、次のファイルが書き込み可能であることを確認してください：`[your store]/app/etc/env.php`

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

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Other Settings]_/**[!UICONTROL Manage Encryption Key]**に移動します。

   ![ システム暗号化キー ](./assets/encryption-key.png){width="700" zoomable="yes"}

1. 次のいずれかの操作を行います。

   - 新しいキーを生成するには、**[!UICONTROL Auto-generate Key]** を `Yes` に設定します。
   - 別のキーを使用するには、**[!UICONTROL Auto-generate Key]** を `No` に設定します。 次に、「**[!UICONTROL New Key]**」フィールドに、使用するキーを入力または貼り付けます。

1. 「**[!UICONTROL Change Encryption Key]**」をクリックします。

   >[!NOTE]
   >
   >新しいキーを安全な場所に記録します。 ファイルに問題が発生した場合は、データを復号化する必要があります。

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
