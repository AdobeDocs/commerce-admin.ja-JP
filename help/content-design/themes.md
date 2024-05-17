---
title: テーマ
description: について [!DNL Commerce] レイアウトファイル、テンプレートファイル、翻訳ファイル、ストアのルックアンドフィールを定義するスキンなどのテーマ。
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# テーマ

テーマは、ストアの視覚的表示を決定するファイルのコレクションです。 を初めてインストールしたとき [!DNL Commerce]ストアのデザイン要素は、に基づいています。 _デフォルト_ テーマ。 に付属する最初のデフォルトテーマに加えて [!DNL Commerce] インストールすると、使用可能なテーマが多種多様になります _現状_ または、必要に応じて変更します。

レスポンシブテーマは、デバイスのビューポートに合わせてページレイアウトを調整します。 サンプル _Luma_ テーマには、デスクトップ、タブレットまたはモバイルデバイスから表示できる柔軟なレスポンシブレイアウトが含まれています。

[!DNL Commerce] テーマには、レイアウトファイル、テンプレートファイル、翻訳ファイル、スキンなどがあります。 スキンは、サポートする CSS ファイル、画像ファイル、JavaScript ファイルのコレクションです。これらのファイルを組み合わせることで、顧客がストアを訪問したときに体験する視覚的なプレゼンテーションとインタラクションを作成できます。 テーマとスキンの変更やカスタマイズを行うことができるのは、Commerceのテーマデザインを理解し、サーバーにアクセスできる開発者やデザイン担当者です。 詳しくは、 [_フロントエンド開発者ガイド_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Luma テーマ](./assets/design-responsive.png){width="600" zoomable="yes"}

## デフォルトのテーマ

この `Magento Blank` レスポンシブテーマは、様々なデバイス向けにストアフロントの表示をレンダリングし、デスクトップ、テーブル、モバイルデバイス向けのベストプラクティスを組み込みます。 一部のテーマは、特定のデバイスでのみ使用できるように設計されています。 条件 [!DNL Commerce] 特定のブラウザー ID またはユーザーエージェントを検出します。このエージェントは、特定のブラウザー用に設定されたテーマを使用します。 検索文字列には、Perl 互換の正規表現（PCRE）を含めることもできます。

![テーマ](./assets/themes.png){width="700" zoomable="yes"}

### テーマグリッドのフィルタリング

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. クリック **[!UICONTROL Filters]**.

1. ID の範囲、テーマ名（タイトル）、フォルダーパス、親テーマを入力します。

1. クリック **[!UICONTROL Apply Filters]** でテーマのリストを更新します。

## 現在のテーマの設定を表示する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. インストールされたテーマの一覧で、調査するテーマを見つけ、その行をクリックして設定を表示します。

1. サンプルページを表示するには、 **[!UICONTROL Theme Preview Image]**.

![テーマをプレビュー](./assets/theme-settings.png){width="600" zoomable="yes"}

## デフォルトのテーマの適用

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 次の下 _[!UICONTROL Default Theme]_、設定&#x200B;**[!UICONTROL Applied Theme]**を、現在のビューに使用するビューに変更します。

   ![適用されたテーマ](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Configuration]**.

## ユーザーエージェントルールの追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 次の下 _[!UICONTROL Design Rule]_を選択し、**[!UICONTROL Add New User Agent Rule]**.

   ![デザイン規則](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Search String]**&#x200B;を入力し、特定のデバイスのブラウザー ID を入力します。

   検索文字列は、入力された順序で照合されます。 例えば、Firefox の場合は、次のように入力します。

   `/^mozilla/i`

1. 追加のデバイスを入力するには、この手順を繰り返します。

1. 完了したら、 **[!UICONTROL Save Configuration]**.
