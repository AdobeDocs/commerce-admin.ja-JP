---
title: '[!DNL Page Builder] 設定'
description: Adobe Commerce [!DNL Page Builder]  よびMagento Open Sourceの管理での機能設定について説明します。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# [!DNL Page Builder] 設定

設定で有効にした場合、[!DNL Page Builder] れはCMSページ、ブロック、動的ブロック用のデフォルトのコンテンツ作成ツールになります。 さらに、「_[!UICONTROL Enable Advanced CMS]_」ボタンを使用すると、カテゴリと製品のオプションとして [!DNL Page Builder] を使用できます。 また、商品、カテゴリ、CMSの各ページで使用するデフォルトの [ ページレイアウト ](../content-design/page-layout.md) を選択することもできます。 WYSIWYG [!DNL Page Builder]editor[ を使用するニュースレターコンテンツには、](../content-design/editor.md) れは使用できません。

>[!NOTE]
>
>インストール時に、[!DNL Page Builder] は [!UICONTROL Mask for Meta Description] 設定フィールドのデフォルト設定を上書きします。 値が `{{name}} {{description}}` から `{{name}}` に変更されます。
><br>
>この設定にアクセスするには、[!UICONTROL Stores] / _[!UICONTROL Settings]_/ [!UICONTROL Configuration] に移動し、[!UICONTROL Catalog] を展開して、その下にある [!UICONTROL Catalog] を選択します。 [!UICONTROL Mask for Meta Description] フィールドは [!UICONTROL Product Fields Auto-generation] セクションにあります。

>[!NOTE]
>
>管理者ユーザーが [!UICONTROL Content] のボタンを表示し、ページビルダーを使用するには、[ 役割の範囲 ](../systems/permissions-user-roles.md) に対する [!UICONTROL Edit with Page Builder] 権限が必要です。

コンテンツ管理の詳細ツールの設定オプションについて詳しくは、[_設定リファレンスガイド_](../configuration-reference/general/content-management.md) を参照してください。

## [!DNL Page Builder] の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![ 拡張セレクター ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** を展開し、**[!UICONTROL Enable Page Builder]** が `Yes` に設定されていることを確認します。

   ![ 高度なコンテンツツール ](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. [!DNL Google Maps] をセットアップする準備ができている場合は、次の操作を行います。

   - 必要に応じて、[API キーの取得 ](https://developers.google.com/maps/documentation/javascript/get-api-key) の手順に従い、**[!UICONTROL Google Maps API Key]** をコピー&amp;ペーストします。

   - **[!UICONTROL Google Maps Style]** を変更するには、[[!DNL Google Maps] API スタイル設定ウィザード ](https://mapstyle.withgoogle.com/) で生成された JSON コードを貼り付けます。

   >[!NOTE]
   >
   >[ コンテンツでの ](map.md) の使用について詳しくは、[!DNL Google Maps] メディア – マップ [!DNL Page Builder] を参照してください。

1. [!DNL Page Builder] 列グリッドのガイドラインの数を設定するには、次の手順を実行します。

   - **[!UICONTROL Default Column Grid Size]**：グリッドに表示するデフォルトの列数を入力します。

   - **[!UICONTROL Maximum Column Grid Size]**：グリッドで使用可能にする列の最大数を入力します。

   >[!NOTE]
   >
   >[ コンテンツを操作する際に列グリッドを使用する方法について詳しくは、](column.md) レイアウト – 列 [!DNL Page Builder] を参照してください。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## デフォルトのレイアウトを設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Web]**」を選択します。

1. ![ 拡張セレクター ](../assets/icon-display-expand.png) を展開し **[!UICONTROL Default Layouts]** 以下を実行します。

   ![ デフォルトのレイアウト ](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Web 設定オプションについて詳しくは、[_設定リファレンスガイド_](../configuration-reference/general/web.md#default-layouts) を参照してください。

   - 製品ページに使用する **[!UICONTROL Default Product Layout]** を選択します。

   - カテゴリページに使用する **[!UICONTROL Default Category Layout]** を選択します。

   - CMS ページに使用する **[!UICONTROL Default Page Layout]** を選択します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## Disable [!DNL Page Builder]

>[!NOTE]
>
>[!DNL Page Builder] を無効にすると、「詳細コンテンツツール」がWYSIWYG [editor](../content-design/editor.md) に置き換わり、ストアフロントに表示エラーが発生する可能性があります。 以前に [!DNL Page Builder] で作成したコンテンツは、管理者からは編集できない場合があります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![ 展開セレクター ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** を展開し、「**[!UICONTROL Enable Page Builder]**」を `No` に設定します。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL Turn Off]**」をクリックします。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. プロンプトが表示されたら、無効なキャッシュを [ 更新 ](../systems/cache-management.md) します。
