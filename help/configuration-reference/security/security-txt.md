---
title: '[!UICONTROL Security] > [!UICONTROL Security.txt]'
description: Commerce管理者の[!UICONTROL Security] > [!UICONTROL Security.txt] ページで設定を確認します。
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
TQID: https://experienceleague.adobe.com/fXStEab1k6GKC5Tj7CStSGou3uNB-wJk5rZ-7EiFkcg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

これらの設定設定の変更について詳しくは、[&#x200B; セキュリティ問題レポート &#x200B;](../../systems/security-issue-reporting.md)を参照してください。

{{config}}

## [!UICONTROL General]

![一般](./assets/txt-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | web サイト | 有効にすると、セキュリティ研究者が潜在的な脆弱性を報告するために必要な情報を含む`security.txt` ファイルが保存されます。 オプション：<br />**`Yes`**- _連絡先情報_および&#x200B;_その他の情報_ セクションで入力された情報に基づいて`security.txt` ファイルを作成します。<br />**`No`** - （デフォルト） `security.txt` ファイルを作成しません。 |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![連絡先情報](./assets/txt-contact-info.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email] | web サイト | セキュリティレポートを送信できるメールアドレス。 |
| [!UICONTROL Phone] | web サイト | セキュリティ上の懸念を報告するために使用できる電話番号。 |
| [!UICONTROL Contact Page] | web サイト | セキュリティ担当者をリストするサイト上のページ、または&#x200B;_お問い合わせ_ ページのURL。 例：<br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![その他の情報](./assets/txt-other-info.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Encryption] | web サイト | セキュリティ研究者が暗号化通信の送信に使用できる暗号化鍵の場所を示すURL。 _&#x200B;**このフィールドに暗号化キーを入力しないでください。**&#x200B;_ <br/><br/>そのキーが信頼できる情報源から取得されたものであることを確認するのは、研究者の責任です。 研究者は、鍵がデジタル署名を生成するために使用されるものと同じであると仮定してはなりません。 例：<br />Web サーバーからのOpenPGP キー – `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | web サイト | セキュリティ研究者が確認されるストア内のページ（`https://mystore.com/hall-of-fame.html`など）を指すURL。 今後の攻撃を防ぐために、脆弱性の問題に関する具体的な情報を明らかにせずに、一般的な説明のみを含めてください。 例：<br />以下の研究者に感謝します：<br /> （yyyy/mm/dd） Justin Thyme - SQL インジェクション |
| [!UICONTROL Preferred Languages] | web サイト | 1つ以上の優先セキュリティレポート言語を指定します。 複数の2文字[言語コード &#x200B;](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)をコンマで区切ります。 指定した言語はすべて同じ優先度です。 例えば、英語、スペイン語、フランス語を指定するには、`en, es, fr`と入力します。 |
| [!UICONTROL Hiring] | web サイト | セキュリティ関連の職位を一覧表示するサイト上のページのURL。 例：`https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | web サイト | セキュリティポリシーと脆弱性レポートの慣行を説明するページのURL。 例：`https://mystore.com/security-reporting.html` デフォルト：`https://mystore.com/security` |
| [!UICONTROL Signature] | web サイト | デジタル署名ファイルへのリンク。 デジタル署名はコマンドラインから生成する必要があり、サーバーの`.well-known` フォルダーに保存されます。 詳しくは、GitHubの[Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md)を参照してください。 例：`https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
