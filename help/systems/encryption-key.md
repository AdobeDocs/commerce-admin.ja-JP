---
title: 暗号化キー
description: セキュリティを向上させるために定期的に変更する必要がある、独自の暗号化キーを自動生成または追加する方法を説明します。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 暗号化キー

Adobe CommerceとMagento Open Sourceは、パスワードやその他の機密データを保護するために暗号化キーを使用します。 業界標準の [!DNL ChaCha20-Poly1305] アルゴリズムは、暗号化が必要なすべてのデータを暗号化するために 256 ビットキーと共に使用されます。 これには、クレジットカードのデータや統合（支払いおよび配送モジュール）のパスワードが含まれます。 さらに、強力なセキュアハッシュアルゴリズム（SHA-256）を使用して、復号化を必要としないすべてのデータをハッシュ化します。

最初のインストールでは、Commerceに暗号化キーを生成させるか、独自の暗号化キーを入力するかを尋ねるプロンプトが表示されます。 暗号化キーツールを使用すると、必要に応じてキーを変更できます。 セキュリティを向上させるには、暗号化キーを定期的に変更する必要があります。また、元のキーが侵害される可能性はいつでも生じます。 キーが変更されるたびに、すべてのレガシーデータが新しいキーを使用して再エンコードされます。

技術情報については、[ インストール ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) の _オンプレミスの高度なインストール_ を参照してください。

## 手順 1：ファイルを書き込み可能にする

暗号化キーを変更するには、次のファイルが書き込み可能であることを確認してください：`[your store]/app/etc/env.php`

## 手順 2：暗号化キーの変更

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Other Settings]_/**[!UICONTROL Manage Encryption Key]**に移動します。

   ![ システム暗号化キー ](./assets/encryption-key.png){width="700" zoomable="yes"}

1. 次のいずれかの操作を行います。

   - 新しいキーを生成するには、**[!UICONTROL Auto-generate Key]** を `Yes` に設定します。
   - 別のキーを使用するには、**[!UICONTROL Auto-generate Key]** を `No` に設定します。 次に、「**[!UICONTROL New Key]**」フィールドに、使用するキーを入力または貼り付けます。

1. 「**[!UICONTROL Change Encryption Key]**」をクリックします。

1. 新しいキーを安全な場所に記録します。

   ファイルに問題が発生した場合は、データを復号化する必要があります。
