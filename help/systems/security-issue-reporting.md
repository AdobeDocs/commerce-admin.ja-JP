---
title: セキュリティ上の問題のレポート
description: セキュリティ研究者がサイトに関するセキュリティ上の問題を報告する際に使用できる、連絡先情報およびセキュリティ関連のリンクの設定方法を説明します。
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# セキュリティ上の問題のレポート

The `security.txt` ファイルには、連絡先情報とセキュリティ関連のリンクが含まれており、セキュリティ研究者がサイトに関するセキュリティ上の問題を報告する際に使用できます。 セキュリティ情報が時間の経過と共に変化する場合は、 `security.txt` ファイルは最新です。

**_security.txt を構成するには、次の手順に従います。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL Security]_をクリックし、**[!UICONTROL Security.txt]**.

1. Adobe Analytics の _[!UICONTROL General]_セクション、設定&#x200B;**[!UICONTROL Enable]**から `Yes`.

   ![一般的なセキュリティ設定](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. の下 _[!UICONTROL Contact Information]_、次の情報を入力します。

   - ストアのセキュリティ問題を管理する人の電子メールアドレスと電話番号。

   - ストアの URL **[!UICONTROL Contact Page]**. このページは、ストアのセキュリティ連絡先のリストか、 _お問い合わせ_ ページに貼り付けます。

   ![連絡先情報の設定](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. の下 _[!UICONTROL Other Information]_、次の情報を入力します。

   - パブリックの URL **[!UICONTROL Encryption]** キー。 例： `https://example.com/pgp-key.txt`

   - の URL **[!UICONTROL Acknowledgments]** セキュリティ研究者がお客様の店舗の代わりに取り組んでいることが認識されるページ。

   - お使いの **[!UICONTROL Preferred Languages]** セキュリティ関連の通信用。 標準の 2 文字を入力 [言語コード](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) サポートされる言語ごとに、コンマで区切って入力します。 例えば、英語、スペイン語、フランス語を指定するには、次のように入力します。 `en, es, fr`. 指定した言語は、表示順序に関係なく、すべて同じ優先順位を持ちます。

   - の URL **[!UICONTROL Hiring]** お客様の店舗でのセキュリティ関連の雇用機会をリストするページ。

   - セキュリティの URL **[!UICONTROL Policy]** ページに貼り付けます。

   - デジタルの URL **[!UICONTROL Signature]** サーバーに保存されたファイル。 例： `https://mystore.com/.well-known/security.txt.sig`

   デジタル署名は、サーバーの CLI（コマンドラインインターフェイス）から設定する必要があります。 詳しくは、 [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) GitHub で

   ![その他の情報](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.
