---
title: テーマ
description: レイアウトファイル  [!DNL Commerce]  テンプレートファイル、翻訳ファイル、ストアのルックアンドフィールを定義するスキンなど、テーマについて説明します。
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# テーマ

テーマは、ストアの視覚的表示を決定するファイルのコレクションです。 [!DNL Commerce] を初めてインストールするとき、ストアのデザイン要素は _デフォルト_ テーマに基づいています。 [!DNL Commerce] のインストールに付属する初期のデフォルトテーマに加えて、様々なテーマが利用可能で、それらを _そのまま_ 使用したり、必要に応じて変更したりできます。

レスポンシブテーマは、デバイスのビューポートに合わせてページレイアウトを調整します。 サンプルの _Luma_ テーマには、デスクトップ、タブレットまたはモバイルデバイスから表示できる柔軟なレスポンシブレイアウトが含まれています。

[!DNL Commerce] のテーマには、レイアウトファイル、テンプレートファイル、翻訳ファイル、スキンなどがあります。 スキンは、サポートされる CSS、画像、JavaScript ファイルの集まりです。これらのファイルを組み合わせることで、店舗を訪れた顧客が体験する視覚的なプレゼンテーションとインタラクションを実現します。 テーマとスキンの変更やカスタマイズを行うことができるのは、Commerceのテーマデザインを理解し、サーバーにアクセスできる開発者やデザイン担当者です。 詳しくは、[_フロントエンド開発者ガイド_](https://developer.adobe.com/commerce/frontend-core/guide/themes/) を参照してください。

![Luma テーマ ](./assets/design-responsive.png){width="600" zoomable="yes"}

## デフォルトのテーマ

`Magento Blank` レスポンシブテーマは、様々なデバイスでストアフロントの表示をレンダリングし、デスクトップ、テーブル、モバイルデバイス向けのベストプラクティスを組み込みます。 一部のテーマは、特定のデバイスでのみ使用できるように設計されています。 特定のブラウザー ID[!DNL Commerce] たはユーザーエージェントを検出すると、その特定のブラウザー用に設定されているテーマが使用されます。 検索文字列には、Perl 互換の正規表現（PCRE）を含めることもできます。

![ テーマ ](./assets/themes.png){width="700" zoomable="yes"}

### テーマグリッドのフィルタリング

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Themes]**に移動します。

1. 「**[!UICONTROL Filters]**」をクリックします。

1. ID の範囲、テーマ名（タイトル）、フォルダーパス、親テーマを入力します。

1. 「**[!UICONTROL Apply Filters]**」をクリックすると、テーマのリストが更新されます。

## 現在のテーマの設定を表示する

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Themes]**に移動します。

1. インストールされたテーマの一覧で、調査するテーマを見つけ、その行をクリックして設定を表示します。

1. サンプルページを表示するには、**[!UICONTROL Theme Preview Image]** をクリックします。

![ テーマをプレビュー ](./assets/theme-settings.png){width="600" zoomable="yes"}

## デフォルトのテーマの適用

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**に移動します。

1. 設定するストア表示を見つけ、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Edit]**をクリックします。

1. _[!UICONTROL Default Theme]_の下で、現在のビューに使用するビューに&#x200B;**[!UICONTROL Applied Theme]**を設定します。

   ![ 適用されたテーマ ](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Configuration]**」をクリックします。

## ユーザーエージェントルールの追加

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**に移動します。

1. [_[!UICONTROL Design Rule]_] で、[**[!UICONTROL Add New User Agent Rule]**] をクリックします。

   ![ 設計規程 ](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. **[!UICONTROL Search String]**：特定のデバイスのブラウザー ID を入力します。

   検索文字列は、入力された順序で照合されます。 例えば、Firefox の場合は、次のように入力します。

   `/^mozilla/i`

1. 追加のデバイスを入力するには、この手順を繰り返します。

1. 完了したら、「**[!UICONTROL Save Configuration]**」をクリックします。
