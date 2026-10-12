---
title: パンくずリスト
description: パンくずリストの様々なパターンと、コンテンツページとカタログページに表示するように設定する方法について説明します。
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
TQID: 'https://experienceleague.adobe.com/v1hA4y0MmxxTtH3WbspqosZM1JMk4PMyhK1xeLxALOE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 48c59cc5-3c2e-5df1-8756-f5c139a28932
    internal-label: Site Navigation
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%
---
# パンくずリスト

_パンくずリスト_&#x200B;は、顧客がストア内の他のページに関連する位置を示す一連のリンクです。 パンくずリスト内の任意のリンクをクリックして、前のページに戻ることができます。

パンくずリストは、コンテンツページとカタログページに表示するように設定できます。 パンくずリストの形式と位置はテーマによって異なりますが、通常はヘッダーのすぐ下にあります。 デフォルトでは、パンくずリストはCMS ページに表示されます。

ストアフロントに表示された![ パンくずリスト ](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## パンくずリストの一般的な種類

パンくずリストは、目的が異なる3つの主な種類に分けることができます。 各タイプのパンくずリストの実装の本質と主な原則は以下のとおりです。

### 階層ベースのパンくずリスト

この種類のパンくずリストは、サイトで設定されたカテゴリ階層に基づいています。 提示されたチェーンは、構造内のどこにあるかをユーザーに伝えます。 この場合、各テキストリンクは、前のページよりも1 レベル高いページを対象としています。

例：`Men > Tops > Hoodies & Sweatshirts`

このタイプの利点は、ユーザーが自分がどのカテゴリーレベルにあるかを簡単に確認でき、カタログページ間のナビゲーションに簡単にアクセスできることです。

### 履歴ベースのパンくずリスト

履歴（またはパス）ベースのナビゲーションは、ブラウザーの「戻る」ボタンに似ています。 このタイプのナビゲーションでは、ユーザーは変更することなく、以前に訪問したページにすばやく戻ることができます。

このタイプの利点は、顧客がカテゴリーページで複数のフィルターを選択した後に前のページに戻りたい場合に最も役立つことです。

例：`Home > What's New > Gear > Bags`

### 属性ベースのパンくずリスト

このタイプのパンくずリストには、カテゴリーページで選択した属性が表示されます。 他のタイプとの主な違いは、属性ベースのパンくずリストは、顧客が特定の製品（価格、品質、色など）のナビゲーションレイヤーで選択したフィルターとオプションを表していることです。

例：`Home > Suits > All Suits > Refined by > Slim Fit`

## CMS ページからパンくずリストを追加または削除する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左側のパネルで、**[!UICONTROL Web]**を選択します。

   ![CMS ページのパンくずリストを表示](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. _[!UICONTROL Default Pages]_セクションを展開します。

1. 「**[!UICONTROL Use system value]**」チェックボックスの選択を解除します。

1. **[!UICONTROL Show Breadcrumbs for CMS Pages]**&#x200B;を`No`または`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

>[!NOTE]
>
>親カテゴリは、`Browsing Category`= `Deny` [ カテゴリ権限](category-permissions.md)の設定がある場合、子カテゴリページのパンくずリストには表示されません。
