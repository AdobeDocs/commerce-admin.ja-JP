---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: の設定を確認します。 [!UICONTROL General] &gt; [!UICONTROL Content Management] コマース管理者のページ。
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5eef49c10680a47574afe3d3ecfa430dca7ad9ff
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
| [!UICONTROL Enable WYSIWYG Editor] | ストア表示 | ストアに対してエディターが有効かどうかを判断します。 オプション：デフォルトで有効/デフォルトで無効/完全に無効 |
| [!UICONTROL WYSIWYG Editor] | Web サイト | WYSIWYG エディターで使用される TinyMCE エディターのバージョンを指定します。 オプション： <br/>**`TinyMCE 5`**– （デフォルト） TinyMCE バージョン 5 をデフォルトの WYSIWYG エディターとして使用します。<br><br>_**&#x200B;注意：**_Adobe CommerceおよびMagento Open Source 2.4.5 の TinyMCE 5.10 ライブラリを更新すると、一部の種類の URL を使用して画像やリンクを更新する際に、任意の JavaScript 実行が許可される脆弱性が解決されます。 TinyMCE 3 は 2.4.0 リリースで非推奨（廃止予定）となり、2.4.3 リリースで削除されました。 TinyMCE 4 は 2.4.4 リリースで削除されました。 |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | グローバル | 次のかどうかを判断します [静的 URL](../../content-design/catalog-urls-dynamic-media.md) は、WYSIWYG エディターから参照されるメディアコンテンツに使用されます。 この設定は、製品、カテゴリ、ページ、ブロックなど、WYSIWYG エディターが使用可能なすべての場所に適用されます。 オプション： <br/>**`Yes`**- WYSIWYG エディターで挿入されるメディアコンテンツに静的 URL を使用します。 静的 URL は絶対 URL で、 [ベース URL](../../stores-purchase/store-urls.md) ストアの変更。<br/>**`No`** （デフォルト） – WYSIWYG エディターによって挿入されるメディアコンテンツに対して、に基づいて動的 URL を使用します。  `{{media url="..."}}` ディレクティブ。 動的 URL は相対 URL で、ストアのベース URL が変更された場合でも破損しません。 |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS ページ階層](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | グローバル | コンテンツページに対してページ階層の使用をアクティベートします。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | グローバル | メタデータを階層内のページに関連付けることができます。 オプション： `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | グローバル | 既定のメニュースタイルを決定します。 オプション： `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![高度なコンテンツツール](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | グローバル | 次のかどうかを判断します [!DNL Page Builder] 高度なコンテンツツールを使用できます。 オプション： <br/>**`Yes`**– が [!DNL Page Builder] ワークスペースは、ページ、ブロック、製品、カテゴリの「コンテンツ」セクションに表示されます。<br/>**`No`**  – 標準の CMS 編集ツールはに表示されます。 _[!UICONTROL Content]_ページ、ブロック、製品、カテゴリのセクション。 |
| [!UICONTROL Enable Page Builder Content Preview] | グローバル | 次のかどうかを判断します [!DNL Page Builder] 製品およびカテゴリに対して、コンテンツプレビューが有効になります。 オプション： `Yes` / `No` <br/>**_注意：_**これをに設定しました `Yes` デフォルトでは、プレビューをオフにすると、製品またはカテゴリフォーム内でプレビューを読み込むことによるパフォーマンスの問題を防ぐことができます。 |
| [!UICONTROL Google Maps API Key] | グローバル | この [!DNL Google Maps] Google アカウントからの API キー。 |
| [!UICONTROL Test Key] |  | を検証します。 [!DNL Google Maps] API キー。 |
| [!UICONTROL Google Maps Style] | グローバル | を貼り付けます [!DNL Google Maps] ここで JSON コードのスタイルを設定して、マップコンテンツタイプのルックアンドフィールを変更します。 |
| [!UICONTROL Default Column Grid Size] | グローバル | 内のデフォルトの列数を決定します [!DNL Page Builder] グリッド。 |
| [!UICONTROL Maximum Column Grid Size] | グローバル | 内の列の最大数を決定 [!DNL Page Builder] グリッド。 |

{style="table-layout:auto"}

>[!TIP]
>
>ページビルダーを使用すると、視覚的なストーリーテリングを強化し、顧客エンゲージメントとロイヤルティを高めるカスタムレイアウトを使用して、コンテンツに富んだページを簡単に作成できます。 これらの機能は、品質を向上し、カスタムページの作成に要する時間とコストを削減するように設計されています。 これらの機能の詳細と、それらを使用してAdobe CommerceやMagento Open Sourceストア向けの魅力的なコンテンツを作成する方法については、を参照してください。 [_ページビルダーユーザーガイド_](../../page-builder/guide-overview.md).
