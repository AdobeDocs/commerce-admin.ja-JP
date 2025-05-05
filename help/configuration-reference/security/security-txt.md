---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Commerce Admin の [!UICONTROL Security] &gt; [!UICONTROL Security.txt] ページで設定を確認します。
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

これらの設定の変更について詳しくは、[ セキュリティ上の問題のレポート ](../../systems/security-issue-reporting.md) を参照してください。

{{config}}

## [!UICONTROL General]

![ 一般 ](./assets/txt-general.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | Web サイト | 有効にすると、セキュリティ研究者が潜在的な脆弱性を報告するために必要な情報を含む `security.txt` ファイルが保存されます。 オプション：<br />**`Yes`**- _連絡先情報_ および _その他の情報_ セクションに入力された情報に基づいて `security.txt` ファイルを作成します。<br />**`No`** - （デフォルト） `security.txt` ファイルを作成しません。 |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![ お問い合わせ先 ](./assets/txt-contact-info.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email] | Web サイト | セキュリティレポートを送信できるメールアドレス。 |
| [!UICONTROL Phone] | Web サイト | セキュリティ上の問題を報告するために使用できる電話番号。 |
| [!UICONTROL Contact Page] | Web サイト | セキュリティ上の連絡先をリストするサイトのページ、または _お問い合わせ_ ページの URL。 例：<br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![ その他の情報 ](./assets/txt-other-info.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Encryption] | Web サイト | セキュリティの研究者が暗号化された通信の送信に使用できる暗号化キーの場所を指す URL。 _&#x200B;**このフィールドには暗号化キーを入力しないでください。**&#x200B;_ <br/><br/> 鍵が信頼できる情報源からのものであることを確認するのは、研究者の責任です。 研究者は、キーがデジタル署名の生成に使用されたものと同じであると想定してはなりません。 例：<br />OpenPGP キー（web サーバーから） - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Web サイト | セキュリティ調査者が確認されているストア内のページを指す URL。`https://mystore.com/hall-of-fame.html` など。 今後の攻撃を防ぐには、脆弱性の問題に関する具体的な情報を明らかにせずに、一般的な説明のみを含めます。 例：<br /> 次の研究者の皆様に感謝します。<br /> （yyyy/mm/dd） Justin Thyme - SQL injection |
| [!UICONTROL Preferred Languages] | Web サイト | セキュリティ レポートの優先言語を少なくとも 1 つ指定します。 複数の 2 文字 [ 言語コード ](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) をコンマで区切ります。 指定した言語の優先度はすべて同じです。 例えば、英語、スペイン語、フランス語を指定するには、「`en, es, fr`」と入力します。 |
| [!UICONTROL Hiring] | Web サイト | セキュリティ関連のジョブ ポジションを一覧表示するサイト上のページの URL。 例：`https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Web サイト | セキュリティポリシーと脆弱性レポート手法を説明するページの URL。 例：`https://mystore.com/security-reporting.html` デフォルト：`https://mystore.com/security` |
| [!UICONTROL Signature] | Web サイト | デジタル署名ファイルへのリンク。 デジタル署名はコマンドラインから生成する必要があり、サーバー上の `.well-known` フォルダーに保存されます。 詳しくは、GitHub の [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) を参照してください。 例：`https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
