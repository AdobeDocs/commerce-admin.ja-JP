---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: 次のページで設定を確認します： [!UICONTROL General] &gt; [!UICONTROL Content Management] コマース管理のページ。
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG オプション](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | ストア表示 | エディターがストアに対して有効になっているかどうかを指定します。 オプション：デフォルトで有効/デフォルトで無効/完全に無効 |
| [!UICONTROL WYSIWYG Editor] | Web サイト | WYSIWYG エディタに使用する TinyMCE エディタのバージョンを決定します。 オプション： <br/>**`TinyMCE 5`**- （デフォルト）デフォルトの WYSIWYG エディタとして TinyMCE バージョン 5 を使用します。<br><br>_**&#x200B;注意：**_Adobe CommerceとMagento Open Source2.4.5 の TinyMCE 5.10 ライブラリが更新され、一部の種類の URL を使用して画像やリンクを更新する際に、任意の JavaScript が実行される脆弱性が解決されました。 TinyMCE 3 は 2.4.0 リリースで廃止され、2.4.3 リリースで削除されました。 TinyMCE 4 は 2.4.4 リリースで削除されました。 |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | グローバル | 次の場合に決定 [静的 URL](../../content-design/catalog-urls-dynamic-media.md) は、WYSIWYG エディターから参照されるメディアコンテンツに対して使用されます。 この設定は、製品、カテゴリ、ページ、ブロックなど、WYSIWYG エディターが使用可能なすべての場所に適用されます。 オプション： <br/>**`Yes`**- WYSIWYG エディターで挿入されるメディアコンテンツに静的 URL を使用します。 静的 URL は絶対 URL で、 [ベース URL](../../stores-purchase/store-urls.md) 」という名前に変更されます。<br/>**`No`** （デフォルト） — WYSIWYG エディターで挿入されるメディアコンテンツの動的 URL を、  `{{media url="..."}}` ディレクティブ。 動的 URL は相対 URL で、ストアのベース URL が変更されても壊れません。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS ページ階層](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | グローバル | コンテンツページでのページ階層の使用をアクティベートします。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | グローバル | 階層内のページにメタデータを関連付けることができます。 オプション： `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | グローバル | 既定のメニュースタイルを決定します。 オプション： `Content` / `Left Column` / `Right Column` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Content Tools]

![高度なコンテンツツール](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | グローバル | を [!DNL Page Builder] 高度なコンテンツツールを使用できます。 オプション： <br/>**`Yes`**- [!DNL Page Builder] ワークスペースが、ページ、ブロック、製品およびカテゴリの「コンテンツ」セクションに表示されます。<br/>**`No`**  — 標準の CMS 編集ツールは、 _[!UICONTROL Content]_ページ、ブロック、製品、カテゴリのセクション。 |
| [!UICONTROL Enable Page Builder Content Preview] | グローバル | を [!DNL Page Builder] コンテンツのプレビューは、製品とカテゴリに対して有効になります。 オプション： `Yes` / `No` <br/>**_注意：_**これは、 `Yes` デフォルトでは、プレビューをオフにすると、製品フォームまたはカテゴリフォーム内でのプレビューの読み込みに伴うパフォーマンスの問題を防ぐことができます。 |
| [!UICONTROL Google Maps API Key] | グローバル | The [!DNL Google Maps] Googleアカウントからの API キー。 |
| [!UICONTROL Test Key] |  | を検証します。 [!DNL Google Maps] API キー。 |
| [!UICONTROL Google Maps Style] | グローバル | を貼り付けます。 [!DNL Google Maps] style JSON コードをここに追加して、Map コンテンツタイプのルックアンドフィールを変更します。 |
| [!UICONTROL Default Column Grid Size] | グローバル | 列の既定の数を指定します。 [!DNL Page Builder] グリッド。 |
| [!UICONTROL Maximum Column Grid Size] | グローバル | 列の最大数を決定します。 [!DNL Page Builder] グリッド。 |

{:style=&quot;table-layout:auto&quot;}

>[!TIP]
>
>Page Builder を使用すると、視覚的なストーリーテリングを強化し、顧客のエンゲージメントと忠誠度を高めるカスタムレイアウトで、コンテンツに富んだページを簡単に作成できます。 これらの機能は、品質を向上し、カスタムページの作成に要する時間とコストを削減するように設計されています。 これらの機能、およびそれらを使用してAdobe CommerceやMagento Open Sourceストアの魅力的なコンテンツを作成する方法について詳しくは、 [_Page Builder ユーザーガイド_](../../page-builder/guide-overview.md).

{:style=&quot;table-layout:auto&quot;}
