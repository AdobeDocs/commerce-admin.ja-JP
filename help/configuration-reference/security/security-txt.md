---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: 次のページで設定を確認します： [!UICONTROL Security] &gt; [!UICONTROL Security.txt] コマース管理のページ。
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

これらの設定の変更について詳しくは、 [セキュリティ上の問題のレポート](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![一般](./assets/txt-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | Web サイト | 有効にすると、 `security.txt` ファイルを保存します。このファイルには、セキュリティ研究者が潜在的な脆弱性を報告するために必要な情報が含まれています。 オプション：<br />**`Yes`**- `security.txt` ファイルを _連絡先情報_ および _その他の情報_ セクション。<br />**`No`** - （デフォルト） `security.txt` ファイル。 |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![連絡先情報](./assets/txt-contact-info.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email] | Web サイト | セキュリティレポートを送信できる電子メールアドレス。 |
| [!UICONTROL Phone] | Web サイト | セキュリティ上の問題の報告に使用できる電話番号。 |
| [!UICONTROL Contact Page] | Web サイト | セキュリティの連絡先が一覧表示されるサイト上のページの URL、または _お問い合わせ_ ページに貼り付けます。 例: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![その他の情報](./assets/txt-other-info.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Encryption] | Web サイト | セキュリティ研究者が暗号化された通信を送信する際に使用できる暗号化キーの場所を指す URL です。 _**このフィールドに暗号化キーを入力しないでください。**_ <br/><br/>鍵が信頼できる情報源から来たものであることを確かめるのは研究者の責任です。 研究者は、デジタル署名の生成に使用された鍵と同じ鍵を持つとは考えてはなりません。 例：<br />Web サーバーからの OpenPGP キー — `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Web サイト | セキュリティ研究者が確認されるストア内のページを指す URL。例：`https://mystore.com/hall-of-fame.html`. 将来の攻撃を防ぐには、脆弱性の問題に関する具体的な情報を明らかにすることなく、一般的な説明のみを含めます。 例：<br />以下の研究者に感謝を申し上げます。<br />(yyyy/mm/dd) Justin Thyme - SQL インジェクション |
| [!UICONTROL Preferred Languages] | Web サイト | 1 つ以上の優先セキュリティレポート言語を指定します。 複数の 2 文字で区切る [言語コード](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) をコンマで指定します。 指定されたすべての言語は同じ優先順位を持ちます。 例えば、英語、スペイン語、フランス語を指定するには、次のように入力します。 `en, es, fr`. |
| [!UICONTROL Hiring] | Web サイト | セキュリティ関連のジョブ位置をリストするサイト上のページの URL。 例： `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Web サイト | セキュリティポリシーおよび脆弱性レポートのプラクティスについて説明するページの URL。 例： `https://mystore.com/security-reporting.html` デフォルト： `https://mystore.com/security` |
| [!UICONTROL Signature] | Web サイト | 電子署名ファイルへのリンク。 電子署名は、コマンドラインから生成され、 `.well-known` フォルダーをサーバー上に置きます。 詳しくは、 [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) GitHub で 例： `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
