---
title: 暗号化キー
description: 独自の暗号化キーを自動生成または追加する方法を説明します。このキーは定期的に変更して、セキュリティを強化する必要があります。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# 暗号化キー

Adobe CommerceとMagento Open Sourceは、パスワードやその他の機密データを保護するために暗号化キーを使用します。 業界標準 [!DNL ChaCha20-Poly1305] アルゴリズムは、256 ビットキーと共に使用し、暗号化が必要なすべてのデータを暗号化します。 これには、クレジットカードデータと統合（支払いおよび配送モジュール）パスワードが含まれます。 さらに、強力な Secure Hash Algorithm(SHA-256) が、復号化を必要としないすべてのデータをハッシュ化するために使用されます。

初期インストール時に、Commerce で暗号化キーを生成するか、独自のキーを入力するかのどちらかを求めるプロンプトが表示されます。 暗号化キーツールを使用すると、必要に応じてキーを変更できます。 セキュリティを強化するために、暗号化キーを定期的に変更する必要があります。元のキーはいつでも不正になる可能性があります。 キーが変更されるたびに、すべての従来のデータが新しいキーを使用して再エンコードされます。

技術情報については、 [高度なオンプレミスインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) （内） _インストールガイド_.

## 手順 1：ファイルを書き込み可能にする

暗号化キーを変更するには、次のファイルが書き込み可能であることを確認してください。 `[your store]/app/etc/env.php`

## 手順 2：暗号化キーの変更

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![システム暗号化キー](./assets/encryption-key.png){width="700" zoomable="yes"}

1. 次のいずれかの操作を行います。

   - 新しいキーを生成するには、 **[!UICONTROL Auto-generate Key]** から `Yes`.
   - 別のキーを使用するには、 **[!UICONTROL Auto-generate Key]** から `No`. 次に、 **[!UICONTROL New Key]** 「 」フィールドに、使用するキーを入力または貼り付けます。

1. クリック **[!UICONTROL Change Encryption Key]**.

1. 新しいキーの記録を安全な場所に保存します。

   ファイルに問題が発生した場合は、データを復号化する必要があります。
