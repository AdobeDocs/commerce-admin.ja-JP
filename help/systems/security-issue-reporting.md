---
title: セキュリティ問題のレポート
description: サイトに関するセキュリティ上の問題を報告するためにセキュリティ研究者が使用できる連絡先情報およびセキュリティ関連リンクを設定する方法について説明します。
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# セキュリティ問題のレポート

`security.txt` ファイルには、連絡先情報とセキュリティ関連リンクが含まれており、セキュリティ研究者がサイトのセキュリティ上の問題を報告するために使用できます。 セキュリティ情報が時間の経過と共に変化する場合は、`security.txt` ファイルの情報が最新であることを確認してください。

**_security.txt を構成するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL Security]_の下の左パネルで、「**[!UICONTROL Security.txt]**」をクリックします。

1. _[!UICONTROL General]_セクションで、**[!UICONTROL Enable]**を `Yes` に設定します。

   ![ 一般的なセキュリティ設定 ](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. _[!UICONTROL Contact Information]_の下に、次の情報を入力します。

   - ストアのセキュリティ問題を管理する人物のメールアドレスと電話番号。

   - ストアの **[!UICONTROL Contact Page]** の URL。 このページは、店舗のセキュリティ担当者のリストまたは _お問い合わせ_ ページのいずれかです。

   ![ 連絡先情報の設定 ](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. _[!UICONTROL Other Information]_の下に、次の情報を入力します。

   - 公開 **[!UICONTROL Encryption]** 鍵の URL。 例：`https://example.com/pgp-key.txt`

   - ストアに代わってセキュリティ研究者の活動が認められる **[!UICONTROL Acknowledgments]** ページの URL。

   - セキュリティ関連の通信に対する **[!UICONTROL Preferred Languages]** ール。 サポートされている各言語に対して、標準の 2 文字 [ 言語コード ](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) をコンマで区切って入力します。 例えば、英語、スペイン語、フランス語を指定するには、「`en, es, fr`」と入力します。 指定した言語は、表示順序に関係なく、すべて同じ優先度になります。

   - ストアでのセキュリティ関連の雇用機会を一覧表示する **[!UICONTROL Hiring]** ページの URL。

   - セキュリティ **[!UICONTROL Policy]** ページの URL。

   - サーバーに保存されているデジタル **[!UICONTROL Signature]** ファイルの URL。 例：`https://mystore.com/.well-known/security.txt.sig`

   デジタル署名は、サーバの CLI （コマンドライン インターフェイス）から設定する必要があります。 詳しくは、GitHub の [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) を参照してください。

   ![ その他の情報 ](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
