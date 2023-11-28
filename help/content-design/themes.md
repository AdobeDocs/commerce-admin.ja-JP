---
title: テーマ
description: 詳細 [!DNL Commerce] テーマ（ストアの外観と操作性を定義するレイアウトファイル、テンプレートファイル、翻訳ファイル、スキンなど）。
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# テーマ

テーマとは、ストアの視覚的表示を決定するファイルの集まりです。 を初めてインストールしたとき [!DNL Commerce]を使用する場合、ストアのデザイン要素は _デフォルト_ テーマ。 最初のデフォルトテーマに加えて、 [!DNL Commerce] インストール、使用可能なテーマの多様な種類が使用できます _現状_ 必要に応じて、またはを変更します。

レスポンシブテーマでは、デバイスの表示ポートに合わせてページのレイアウトが調整されます。 サンプル _Luma_ テーマには、デスクトップ、タブレット、モバイルデバイスから表示できる、柔軟でレスポンシブレイアウトがあります。

[!DNL Commerce] テーマには、レイアウトファイル、テンプレートファイル、翻訳ファイル、スキンが含まれます。 スキンは、サポートする CSS、画像および JavaScript ファイルのコレクションです。これらを組み合わせて、顧客がストアを訪問したときに体験する視覚的なプレゼンテーションやインタラクションを作成します。 テーマとスキンは、コマースのテーマのデザインを理解し、サーバーにアクセスできる開発者またはデザイン担当者が変更およびカスタマイズできます。 詳しくは、 [_フロントエンド開発者ガイド_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Luma のテーマ](./assets/design-responsive.png){width="600" zoomable="yes"}

## デフォルトのテーマ

The `Magento Blank` レスポンシブテーマは、ストアフロントの表示を様々なデバイス向けにレンダリングし、デスクトップ、テーブルおよびモバイルデバイス向けのベストプラクティスを組み込みます。 一部のテーマは、特定のデバイスでのみ使用するように設計されています。 条件 [!DNL Commerce] は、特定のブラウザー ID またはユーザーエージェントを検出し、特定のブラウザー用に設定されたテーマを使用します。 検索文字列には、Perl 互換正規表現 (PCRE) も含めることができます。

![テーマ](./assets/themes.png){width="700" zoomable="yes"}

### テーマグリッドのフィルタリング

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. クリック **[!UICONTROL Filters]**.

1. ID 範囲、テーマ名（またはタイトル）、フォルダーパス、または親テーマを入力します。

1. クリック **[!UICONTROL Apply Filters]** をクリックして、テーマのリストを更新します。

## 現在のテーマ設定を表示する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. インストールされたテーマの一覧で、確認するテーマを探し、行をクリックして設定を表示します。

1. サンプルページを表示するには、 **[!UICONTROL Theme Preview Image]**.

![テーマをプレビュー](./assets/theme-settings.png){width="600" zoomable="yes"}

## デフォルトのテーマの適用

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 設定するストア表示を見つけ、 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. の下 _[!UICONTROL Default Theme]_，設定&#x200B;**[!UICONTROL Applied Theme]**を現在のビューに使用するビューに追加します。

   ![適用されたテーマ](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Configuration]**.

## ユーザーエージェントルールを追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. の下 _[!UICONTROL Design Rule]_をクリックし、**[!UICONTROL Add New User Agent Rule]**.

   ![デザインルール](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Search String]**」に、特定のデバイスのブラウザー ID を入力します。

   検索文字列は、入力された順序で一致します。 例えば、Firefox の場合は、次のように入力します。

   `/^mozilla/i`

1. 追加のデバイスを入力するには、この手順を繰り返します。

1. 完了したら、「 **[!UICONTROL Save Configuration]**.
