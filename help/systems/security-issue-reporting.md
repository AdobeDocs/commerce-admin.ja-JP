---
title: セキュリティ問題の報告
description: セキュリティ研究者がサイトに関するセキュリティ上の懸念を報告するために使用できる連絡先情報とセキュリティ関連リンクを設定する方法について説明します。
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# セキュリティ問題の報告

`security.txt` ファイルには、セキュリティ研究者がサイトに関するセキュリティ上の懸念を報告するために使用できる連絡先情報とセキュリティ関連のリンクが含まれています。 セキュリティ情報が時間の経過とともに変更される場合は、`security.txt` ファイルの情報が最新であることを確認してください。

**_security.txt:_**&#x200B;を設定するには

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL Security]_&#x200B;の下の左側のパネルで、**[!UICONTROL Security.txt]**&#x200B;をクリックします。

1. _[!UICONTROL General]_&#x200B;セクションで、**[!UICONTROL Enable]**&#x200B;を`Yes`に設定します。

   ![一般的なセキュリティ設定](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. _[!UICONTROL Contact Information]_&#x200B;で、次のように入力します。

   - ストアのセキュリティ問題を管理するユーザーのメールアドレスと電話番号。

   - ストアの&#x200B;**[!UICONTROL Contact Page]**&#x200B;のURL。 このページは、ストアのセキュリティ担当者のリストか、_お問い合わせ_ ページのいずれかです。

   ![連絡先情報の設定](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. _[!UICONTROL Other Information]_&#x200B;で、次のように入力します。

   - パブリック **[!UICONTROL Encryption]** キーのURL。 例：`https://example.com/pgp-key.txt`

   - セキュリティ研究者がストアの代理として取り組みを評価される&#x200B;**[!UICONTROL Acknowledgments]** ページのURL。

   - セキュリティ関連の通信に使用する&#x200B;**[!UICONTROL Preferred Languages]**。 サポートされている各言語の標準の2文字[言語コード &#x200B;](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)をコンマで区切って入力します。 例えば、英語、スペイン語、フランス語を指定するには、`en, es, fr`と入力します。 指定した言語はすべて、外観の順序に関係なく同じ優先順位を持ちます。

   - ストアのセキュリティ関連の雇用機会を一覧表示する&#x200B;**[!UICONTROL Hiring]** ページのURL。

   - セキュリティ **[!UICONTROL Policy]** ページのURL。

   - サーバーに保存されているデジタル **[!UICONTROL Signature]** ファイルのURL。 例：`https://mystore.com/.well-known/security.txt.sig`

   デジタル署名は、サーバーのCLI （コマンドラインインターフェイス）から設定する必要があります。 詳しくは、GitHubの[Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md)を参照してください。

   ![その他の情報](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
