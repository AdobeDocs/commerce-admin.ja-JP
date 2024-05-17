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

Adobe CommerceとMagento Open Sourceは、パスワードやその他の機密データを保護するために暗号化キーを使用します。 業界標準 [!DNL ChaCha20-Poly1305] アルゴリズムは、暗号化を必要とするすべてのデータを暗号化するために 256 ビットキーと共に使用されます。 これには、クレジットカードのデータや統合（支払いおよび配送モジュール）のパスワードが含まれます。 さらに、強力なセキュアハッシュアルゴリズム（SHA-256）を使用して、復号化を必要としないすべてのデータをハッシュ化します。

最初のインストールでは、Commerceに暗号化キーを生成させるか、独自の暗号化キーを入力するかを尋ねるプロンプトが表示されます。 暗号化キーツールを使用すると、必要に応じてキーを変更できます。 セキュリティを向上させるには、暗号化キーを定期的に変更する必要があります。また、元のキーが侵害される可能性はいつでも生じます。 キーが変更されるたびに、すべてのレガシーデータが新しいキーを使用して再エンコードされます。

技術情報については、を参照してください [オンプレミスでの高度なインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) が含まれる _インストールガイド_.

## 手順 1：ファイルを書き込み可能にする

暗号化キーを変更するには、次のファイルが書き込み可能であることを確認してください。 `[your store]/app/etc/env.php`

## 手順 2：暗号化キーの変更

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![システム暗号化キー](./assets/encryption-key.png){width="700" zoomable="yes"}

1. 次のいずれかの操作を行います。

   - 新しいキーを生成するには、を設定します **[!UICONTROL Auto-generate Key]** 対象： `Yes`.
   - 別のキーを使用するには、を設定します **[!UICONTROL Auto-generate Key]** 対象： `No`. 次に、 **[!UICONTROL New Key]** フィールドに、使用するキーを入力または貼り付けます。

1. クリック **[!UICONTROL Change Encryption Key]**.

1. 新しいキーを安全な場所に記録します。

   ファイルに問題が発生した場合は、データを復号化する必要があります。
