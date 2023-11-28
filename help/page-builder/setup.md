---
title: '[!DNL Page Builder] 設定'
description: 詳細 [!DNL Page Builder] 機能の設定をAdobe CommerceおよびMagento Open Sourceの管理者に公開しました。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] 設定

設定で有効にした場合、 [!DNL Page Builder] は、CMS ページ、ブロック、動的ブロック用のデフォルトのコンテンツ作成ツールです。 また、 _[!UICONTROL Enable Advanced CMS]_ボタンオファー [!DNL Page Builder] を「カテゴリ」と「製品」のオプションとして使用できます。 デフォルトの [ページレイアウト](../content-design/page-layout.md) 製品、カテゴリ、CMS ページに使用する [!DNL Page Builder] は、WYSIWYG を使用するニュースレターコンテンツには使用できません [編集者](../content-design/editor.md).

>[!NOTE]
>
>インストール時に、 [!DNL Page Builder] は、 [!UICONTROL Mask for Meta Description] 設定フィールド。 値が次の値から変更されます： `{{name}} {{description}}` から `{{name}}`.
><br>
>この設定には、 [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration]、展開 [!UICONTROL Catalog]を選択します。 [!UICONTROL Catalog] の下に The [!UICONTROL Mask for Meta Description] フィールドが [!UICONTROL Product Fields Auto-generation] 」セクションに入力します。

>[!NOTE]
>
>管理者ユーザーは、 [!UICONTROL Content] 権限 [役割の範囲](../systems/permissions-user-roles.md) 見る [!UICONTROL Edit with Page Builder] ボタンを使用してページビルダーを使用できる。

コンテンツ管理の高度なツールの設定オプションについて詳しくは、 [_設定リファレンスガイド_](../configuration-reference/general/content-management.md).

## 設定 [!DNL Page Builder]

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Content Management]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** そして確認してください **[!UICONTROL Enable Page Builder]** が `Yes`.

   ![高度なコンテンツツール](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. を設定する準備が整っている場合は、 [!DNL Google Maps]、次の操作を実行します。

   - 必要に応じて、 [API キーを取得][1] 手順をコピーし、 **[!UICONTROL Google Maps API Key]**.

   - 次の手順で **[!UICONTROL Google Maps Style]**、 [[!DNL Google Maps] API スタイル設定ウィザード][2].

   >[!NOTE]
   >
   >詳しくは、 [メディア — マップ](map.md) を使用する方法の詳細 [!DNL Google Maps] の [!DNL Page Builder] コンテンツ。

1. 内のガイドラインの数を設定するには [!DNL Page Builder] 柱通芯を使用する場合は、次の操作を行います。

   - の場合 **[!UICONTROL Default Column Grid Size]**&#x200B;をクリックし、グリッドに表示するデフォルトの列数を入力します。

   - の場合 **[!UICONTROL Maximum Column Grid Size]**」には、グリッドで使用可能にする列の最大数を入力します。

   >[!NOTE]
   >
   >詳しくは、 [レイアウト — 列](column.md) を参照して、 [!DNL Page Builder] コンテンツ。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## デフォルトレイアウトの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** 次の操作を実行します。

   ![デフォルトのレイアウト](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Web 設定オプションについて詳しくは、 [_設定リファレンスガイド_](../configuration-reference/general/web.md#default-layouts).

   - を選択します。 **[!UICONTROL Default Product Layout]** 製品ページに使用する

   - を選択します。 **[!UICONTROL Default Category Layout]** をカテゴリページに使用します。

   - を選択します。 **[!UICONTROL Default Page Layout]** を CMS ページに使用する

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 無効にする [!DNL Page Builder]

>[!NOTE]
>
>無効化 [!DNL Page Builder] 高度なコンテンツツールを WYSIWYG に置き換える [編集者](../content-design/editor.md)ストアフロントで表示エラーが発生する場合があります。 以前にで作成したコンテンツ [!DNL Page Builder] 管理者が編集できない可能性があります。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Content Management]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** と設定します。 **[!UICONTROL Enable Page Builder]** から `No`.

1. 確認するメッセージが表示されたら、「 **[!UICONTROL Turn Off]**.

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、 [更新](../systems/cache-management.md) 無効なキャッシュがあります。

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
