---
title: '[!DNL Page Builder] 設定'
description: について [!DNL Page Builder] Adobe CommerceとMagento Open Sourceの管理での機能設定。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# [!DNL Page Builder] 設定

設定で有効になっている場合、 [!DNL Page Builder] は、CMS ページ、ブロック、およびダイナミック ブロック用の既定のコンテンツ作成ツールです。 さらに、 _[!UICONTROL Enable Advanced CMS]_ボタンオファー [!DNL Page Builder] カテゴリおよび製品のオプションとして使用します。 また、デフォルトの [ページレイアウト](../content-design/page-layout.md) 製品、カテゴリ、CMS の各ページで使用する。 [!DNL Page Builder] は、WYSIWYG を使用するニュースレターコンテンツでは使用できません [エディター](../content-design/editor.md).

>[!NOTE]
>
>インストール時、 [!DNL Page Builder] のデフォルト設定を上書きします。 [!UICONTROL Mask for Meta Description] 設定フィールド。 値の変更元： `{{name}} {{description}}` 対象： `{{name}}`.
><br>
>この設定は、に移動すると利用できます。 [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration]、を展開 [!UICONTROL Catalog]を選択し、 [!UICONTROL Catalog] その下に。 この [!UICONTROL Mask for Meta Description] フィールドの検索条件 [!UICONTROL Product Fields Auto-generation] セクション。

>[!NOTE]
>
>管理者ユーザーには次が必要です [!UICONTROL Content] ユーザーの権限 [役割スコープ](../systems/permissions-user-roles.md) 見る [!UICONTROL Edit with Page Builder] をクリックし、ページビルダーを使用できます。

コンテンツ管理の詳細ツールの設定オプションについて詳しくは、 [_設定リファレンスガイド_](../configuration-reference/general/content-management.md).

## 設定 [!DNL Page Builder]

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Content Management]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** そして、次のことを検証します **[!UICONTROL Enable Page Builder]** はに設定されています。 `Yes`.

   ![高度なコンテンツツール](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. を設定する準備が整っている場合は、 [!DNL Google Maps]、次の手順を実行します。

   - 必要に応じて、に従います [API キーを取得][1] 説明の後、 **[!UICONTROL Google Maps API Key]**.

   - を変更するには **[!UICONTROL Google Maps Style]**、によって生成された JSON コードを貼り付けます。 [[!DNL Google Maps] API スタイル設定ウィザード][2].

   >[!NOTE]
   >
   >参照： [メディア – マップ](map.md) の使用の詳細情報 [!DNL Google Maps] が含まれる [!DNL Page Builder] コンテンツ。

1. でガイドラインの数を設定するには [!DNL Page Builder] 柱通芯、次の操作を行います。

   - の場合 **[!UICONTROL Default Column Grid Size]**&#x200B;で、グリッドに表示するデフォルトの列数を入力します。

   - の場合 **[!UICONTROL Maximum Column Grid Size]**&#x200B;で、グリッドで使用可能にする列の最大数を入力します。

   >[!NOTE]
   >
   >参照： [レイアウト – 列](column.md) を使用する場合の柱通芯の使用方法の詳細 [!DNL Page Builder] コンテンツ。

1. 完了したら、 **[!UICONTROL Save Config]**.

## デフォルトのレイアウトを設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Web]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** 次の手順を実行します。

   ![デフォルトのレイアウト](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Web 構成オプションの詳細については、 [_設定リファレンスガイド_](../configuration-reference/general/web.md#default-layouts).

   - を選択します。 **[!UICONTROL Default Product Layout]** 製品ページに使用する。

   - を選択します。 **[!UICONTROL Default Category Layout]** カテゴリページに使用する。

   - を選択します。 **[!UICONTROL Default Page Layout]** CMS ページに使用する。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 無効 [!DNL Page Builder]

>[!NOTE]
>
>無効化 [!DNL Page Builder] 高度なコンテンツツールを WYSIWYG に置き換えます。 [エディター](../content-design/editor.md)、およびが原因で、ストアフロントに表示エラーが発生する可能性があります。 以前に作成したコンテンツ [!DNL Page Builder] 管理者からは編集できない可能性があります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Content Management]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** およびを設定 **[!UICONTROL Enable Page Builder]** 対象： `No`.

1. 確認を求められたら、 **[!UICONTROL Turn Off]**.

1. 完了したら、 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、 [更新](../systems/cache-management.md) 無効なキャッシュ。

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
