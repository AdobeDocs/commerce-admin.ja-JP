---
title: '[!DNL Page Builder]設定'
description: Adobe CommerceおよびMagento Open Sourceの管理画面で [!DNL Page Builder] 機能の設定について説明します。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
TQID: https://experienceleague.adobe.com/qXSCIQN-Tpo-n2CTrXy2xzDssA6xQfuWGAVxuRgI-5o
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# [!DNL Page Builder]設定

設定で有効になっている場合、[!DNL Page Builder]は、CMS Pages、Blocks、およびDynamic Blocksのデフォルトのコンテンツ作成ツールです。 さらに、_[!UICONTROL Enable Advanced CMS]_&#x200B;ボタンは、カテゴリと製品のオプションとして[!DNL Page Builder]を提供します。 商品、カテゴリ、CMS ページに使用するデフォルトの[&#x200B; ページレイアウト &#x200B;](../content-design/page-layout.md)を選択することもできます。 WYSIWYG [editor](../content-design/editor.md)を使用するニュースレターコンテンツには[!DNL Page Builder]を使用できません。

>[!NOTE]
>
>インストールすると、[!DNL Page Builder]は[!UICONTROL Mask for Meta Description]設定フィールドのデフォルト設定を上書きします。値が`{{name}} {{description}}`から`{{name}}`に変更されました。
><br>>この設定にアクセスするには、[!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration]に移動し、[!UICONTROL Catalog]を展開し、下に[!UICONTROL Catalog]を選択します。[!UICONTROL Mask for Meta Description] フィールドは[!UICONTROL Product Fields Auto-generation] セクションにあります。

>[!NOTE]
>
>[!UICONTROL Edit with Page Builder] ボタンを表示し、ページビルダーを使用するには、管理者ユーザーが[役割スコープ &#x200B;](../systems/permissions-user-roles.md)に対して[!UICONTROL Content]権限を持っている必要があります。

コンテンツ管理の詳細ツール設定オプションについて詳しくは、[_設定リファレンスガイド_](../configuration-reference/general/content-management.md)&#x200B;を参照してください。

## [!DNL Page Builder]の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左側のパネルで、**[!UICONTROL Content Management]**&#x200B;を選択します。

1. ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**&#x200B;を展開し、**[!UICONTROL Enable Page Builder]**&#x200B;が`Yes`に設定されていることを確認します。

   ![高度なコンテンツ ツール &#x200B;](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. [!DNL Google Maps]を設定する準備ができたら、次の操作を行います。

   - 必要に応じて、[API キーを取得](https://developers.google.com/maps/documentation/javascript/get-api-key)の手順に従い、**[!UICONTROL Google Maps API Key]**&#x200B;をコピー&amp;ペーストします。

   - **[!UICONTROL Google Maps Style]**&#x200B;を変更するには、[[!DNL Google Maps] API スタイル ウィザード &#x200B;](https://mapstyle.withgoogle.com/)によって生成されたJSON コードを貼り付けます。

   >[!NOTE]
   >
   >[!DNL Page Builder] コンテンツで[!DNL Google Maps]を使用する方法について詳しくは、[&#x200B; メディア – マップ &#x200B;](map.md)を参照してください。

1. [!DNL Page Builder]列グリッドのガイドラインの数を設定するには、次の操作を行います。

   - **[!UICONTROL Default Column Grid Size]**&#x200B;に、グリッドに表示する列のデフォルト数を入力します。

   - **[!UICONTROL Maximum Column Grid Size]**&#x200B;に、グリッドで使用できる最大列数を入力します。

   >[!NOTE]
   >
   >[!DNL Page Builder] コンテンツを操作する際に列グリッドを使用する方法について詳しくは、[&#x200B; レイアウト – 列](column.md)を参照してください。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## デフォルトレイアウトの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左側のパネルで、**[!UICONTROL Web]**&#x200B;を選択します。

1. ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]**&#x200B;を展開し、次の操作を行います。

   ![&#x200B; デフォルトレイアウト &#x200B;](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Web設定オプションについて詳しくは、[_設定リファレンスガイド_](../configuration-reference/general/web.md#default-layouts)&#x200B;を参照してください。

   - 製品ページに使用する&#x200B;**[!UICONTROL Default Product Layout]**&#x200B;を選択します。

   - カテゴリーページに使用する&#x200B;**[!UICONTROL Default Category Layout]**&#x200B;を選択します。

   - CMS ページに使用する&#x200B;**[!UICONTROL Default Page Layout]**&#x200B;を選択します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## [!DNL Page Builder]を無効にする

>[!NOTE]
>
>[!DNL Page Builder]を無効にすると、高度なコンテンツツールがWYSIWYG [editor](../content-design/editor.md)に置き換わり、ストアフロントで表示エラーが発生する可能性があります。 以前[!DNL Page Builder]で作成したコンテンツは、管理者から編集できない可能性があります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左側のパネルで、**[!UICONTROL Content Management]**&#x200B;を選択します。

1. ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**&#x200B;を展開し、**[!UICONTROL Enable Page Builder]**&#x200B;を`No`に設定します。

1. 確認を求められたら、**[!UICONTROL Turn Off]**&#x200B;をクリックします。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. プロンプトが表示されたら、[更新](../systems/cache-management.md)して無効なキャッシュを削除します。
