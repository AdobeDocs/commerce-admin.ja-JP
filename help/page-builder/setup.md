---
title: '[!DNL Page Builder] 設定'
description: Adobe Commerce [!DNL Page Builder] Magento Open Sourceの管理での機能設定について説明します。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# [!DNL Page Builder] 設定

設定で有効にした場合、[!DNL Page Builder] が CMS ページ、ブロック、動的ブロック用のデフォルトのコンテンツ作成ツールになります。 さらに、「_[!UICONTROL Enable Advanced CMS]_」ボタンを使用すると、カテゴリと製品のオプションとして [!DNL Page Builder] を使用できます。 製品、カテゴリおよび CMS ページに使用するデフォルトの [&#x200B; ページレイアウト &#x200B;](../content-design/page-layout.md) を選択することもできます。 [!DNL Page Builder] は、WYSIWYG [&#x200B; エディター &#x200B;](../content-design/editor.md) を使用するニュースレターコンテンツでは使用できません。

>[!NOTE]
>
>インストール時に、[!DNL Page Builder] は [!UICONTROL Mask for Meta Description] 設定フィールドのデフォルト設定を上書きします。 値が `{{name}} {{description}}` から `{{name}}` に変更されます。
><br>
>この設定にアクセスするには、[!UICONTROL Stores] / _[!UICONTROL Settings]_/ [!UICONTROL Configuration] に移動し、[!UICONTROL Catalog] を展開して、その下にある [!UICONTROL Catalog] を選択します。 [!UICONTROL Mask for Meta Description] フィールドは [!UICONTROL Product Fields Auto-generation] セクションにあります。

>[!NOTE]
>
>管理者ユーザーが [!UICONTROL Edit with Page Builder] のボタンを表示し、ページビルダーを使用するには、[&#x200B; 役割の範囲 &#x200B;](../systems/permissions-user-roles.md) に対する [!UICONTROL Content] 権限が必要です。

コンテンツ管理の詳細ツールの設定オプションについて詳しくは、[_設定リファレンスガイド_](../configuration-reference/general/content-management.md) を参照してください。

## [!DNL Page Builder] の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![&#x200B; 拡張セレクター &#x200B;](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** を展開し、**[!UICONTROL Enable Page Builder]** が `Yes` に設定されていることを確認します。

   ![&#x200B; 高度なコンテンツツール &#x200B;](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. [!DNL Google Maps] をセットアップする準備ができている場合は、次の操作を行います。

   - 必要に応じて、[API キーの取得 ][1] の手順に従い、**[!UICONTROL Google Maps API Key]** をコピー&amp;ペーストします。

   - **[!UICONTROL Google Maps Style]** を変更するには、[[!DNL Google Maps] API スタイル設定ウィザード ][2] で生成された JSON コードを貼り付けます。

   >[!NOTE]
   >
   >[!DNL Page Builder] コンテンツでの [!DNL Google Maps] の使用について詳しくは、[&#x200B; メディア – マップ &#x200B;](map.md) を参照してください。

1. [!DNL Page Builder] 列グリッドのガイドラインの数を設定するには、次の手順を実行します。

   - **[!UICONTROL Default Column Grid Size]**：グリッドに表示するデフォルトの列数を入力します。

   - **[!UICONTROL Maximum Column Grid Size]**：グリッドで使用可能にする列の最大数を入力します。

   >[!NOTE]
   >
   >[!DNL Page Builder] コンテンツを操作する際に列グリッドを使用する方法について詳しくは、[&#x200B; レイアウト – 列 &#x200B;](column.md) を参照してください。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## デフォルトのレイアウトを設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左パネルで、「**[!UICONTROL Web]**」を選択します。

1. ![&#x200B; 拡張セレクター &#x200B;](../assets/icon-display-expand.png) を展開し **[!UICONTROL Default Layouts]** 以下を実行します。

   ![&#x200B; デフォルトのレイアウト &#x200B;](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Web 設定オプションについて詳しくは、[_設定リファレンスガイド_](../configuration-reference/general/web.md#default-layouts) を参照してください。

   - 製品ページに使用する **[!UICONTROL Default Product Layout]** を選択します。

   - カテゴリページに使用する **[!UICONTROL Default Category Layout]** を選択します。

   - CMS ページに使用する **[!UICONTROL Default Page Layout]** を選択します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## Disable [!DNL Page Builder]

>[!NOTE]
>
>[!DNL Page Builder] を無効にすると、詳細コンテンツツールが WYSIWYG [editor](../content-design/editor.md) に置き換わり、ストアフロントに表示エラーが発生する場合があります。 以前に [!DNL Page Builder] で作成したコンテンツは、管理者からは編集できない場合があります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** を展開し、「**[!UICONTROL Enable Page Builder]**」を `No` に設定します。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL Turn Off]**」をクリックします。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. プロンプトが表示されたら、無効なキャッシュを [&#x200B; 更新 &#x200B;](../systems/cache-management.md) します。

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
