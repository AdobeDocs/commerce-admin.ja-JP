---
title: セキュリティ問題のレポート
description: サイトに関するセキュリティ上の問題を報告するためにセキュリティ研究者が使用できる連絡先情報およびセキュリティ関連リンクを設定する方法について説明します。
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# セキュリティ問題のレポート

この `security.txt` ファイルには、セキュリティ研究者がサイトのセキュリティ上の問題を報告するために使用できる連絡先情報とセキュリティ関連リンクが含まれています。 セキュリティ情報が時間と共に変化する場合は、 `security.txt` ファイルは最新です。

**_security.txt を構成するには、次の手順に従います。_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL Security]_を選択し、**[!UICONTROL Security.txt]**.

1. が含まれる _[!UICONTROL General]_セクション、設定&#x200B;**[!UICONTROL Enable]**対象： `Yes`.

   ![一般的なセキュリティ設定](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. 次の下 _[!UICONTROL Contact Information]_を入力します。

   - ストアのセキュリティ問題を管理する人物のメールアドレスと電話番号。

   - ストアの URL **[!UICONTROL Contact Page]**. このページは、ストアのセキュリティ連絡先のリストまたは _お問い合わせ_ ページ。

   ![連絡先情報の設定](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. 次の下 _[!UICONTROL Other Information]_を入力します。

   - パブリックの URL **[!UICONTROL Encryption]** キー。 例： `https://example.com/pgp-key.txt`

   - の URL **[!UICONTROL Acknowledgments]** セキュリティの研究者がストアに代わって彼らの取り組みを認められているページ。

   - あなたの **[!UICONTROL Preferred Languages]** セキュリティ関連の通信。 標準の 2 文字を入力してください [言語コード](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) サポートされている言語ごとに、コンマで区切ります。 例えば、英語、スペイン語、フランス語を指定するには、 `en, es, fr`. 指定した言語は、表示順序に関係なく、すべて同じ優先度になります。

   - の URL **[!UICONTROL Hiring]** 店舗でのセキュリティ関連の雇用機会を一覧表示するページです。

   - セキュリティ URL **[!UICONTROL Policy]** ページ。

   - デジタルの URL **[!UICONTROL Signature]** サーバーに保存されているファイル。 例： `https://mystore.com/.well-known/security.txt.sig`

   デジタル署名は、サーバの CLI （コマンドライン インターフェイス）から設定する必要があります。 詳しくは、 [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) GitHub で。

   ![その他の情報](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.
