---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: の設定を確認します。 [!UICONTROL Security] &gt; [!UICONTROL Security.txt] コマース管理者のページ。
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

これらの構成設定の変更の詳細は、次を参照してください [セキュリティ問題のレポート](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![一般](./assets/txt-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | Web サイト | 有効になっている場合、 `security.txt` セキュリティ研究者が潜在的な脆弱性を報告するために必要な情報を含むファイルが保存されます。 オプション：<br />**`Yes`**– を作成します `security.txt` に入力された情報に基づくファイル _連絡先情報_ および _その他の情報_ セクション。<br />**`No`** - （デフォルト）を作成しない `security.txt` ファイル。 |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![連絡先情報](./assets/txt-contact-info.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email] | Web サイト | セキュリティレポートを送信できるメールアドレス。 |
| [!UICONTROL Phone] | Web サイト | セキュリティ上の問題を報告するために使用できる電話番号。 |
| [!UICONTROL Contact Page] | Web サイト | セキュリティ上の連絡先をリストするサイトのページの URL、または _お問い合わせ_ ページ。 例： <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![その他の情報](./assets/txt-other-info.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Encryption] | Web サイト | セキュリティの研究者が暗号化された通信の送信に使用できる暗号化キーの場所を指す URL。 _**このフィールドには暗号化キーを入力しないでください。**_ <br/><br/>鍵が信頼できる情報源からのものであることを確認するのは、研究者の責任です。 研究者は、キーがデジタル署名の生成に使用されたものと同じであると想定してはなりません。 例：<br />Web サーバーから PGP キーを開く –  `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Web サイト | セキュリティ調査が承認されているストア内のページを指す URL。例えば、次のようなものがあります`https://mystore.com/hall-of-fame.html`. 今後の攻撃を防ぐには、脆弱性の問題に関する具体的な情報を明らかにせずに、一般的な説明のみを含めます。 例：<br />下記の研究者の皆様に御礼申し上げます。<br />（yyyy/mm/dd）ジャスティンタイム - SQL 挿入 |
| [!UICONTROL Preferred Languages] | Web サイト | セキュリティ レポートの優先言語を少なくとも 1 つ指定します。 複数の 2 文字を区切る [言語コード](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) コンマで区切ります。 指定した言語の優先度はすべて同じです。 例えば、英語、スペイン語、フランス語を指定するには、 `en, es, fr`. |
| [!UICONTROL Hiring] | Web サイト | セキュリティ関連のジョブ ポジションを一覧表示するサイト上のページの URL。 例： `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Web サイト | セキュリティポリシーと脆弱性レポート手法を説明するページの URL。 例： `https://mystore.com/security-reporting.html` デフォルト： `https://mystore.com/security` |
| [!UICONTROL Signature] | Web サイト | デジタル署名ファイルへのリンク。 デジタル署名はコマンドラインから生成する必要があり、に保存されます。 `.well-known` サーバー上のフォルダー。 詳しくは、を参照してください [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) GitHub で。 例： `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
