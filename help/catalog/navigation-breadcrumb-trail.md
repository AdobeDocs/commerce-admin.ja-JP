---
title: パンくずリスト
description: 様々なパンくずリストパターンと、コンテンツページおよびカタログページに表示するように設定する方法について説明します。
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# パンくずリスト

A _パンくずリスト_ は、ストア内の他のページとの関連で顧客がどこにいるかを示す一連のリンクです。 パンくずリストで任意のリンクをクリックすると、前のページに戻ることができます。

パンくずリストは、コンテンツページおよびカタログページに表示されるように設定できます。 パンくずリストの形式と位置は、テーマによって異なりますが、通常はヘッダーのすぐ下にあります。 デフォルトでは、パンくずリストは CMS ページに表示されます。

![ストアフロントに表示されるパンくずリスト](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## パン粉の一般的な種類

パンくずリストは、3 つの主なタイプに分けることができ、目的が異なります。 各種パン粉の実装の本質と主な原則を以下に述べた。

### 階層ベースのパンくずリスト

このタイプのパンくずは、サイトで設定されたカテゴリ階層に基づいています。 表示されたチェーンは、構造内のどこにあるかをユーザーに示します。 この場合、各テキストリンクは、前のページより 1 レベル高いページを対象としています。

例： `Men > Tops > Hoodies & Sweatshirts`

このタイプの利点は、ユーザーが自分が属するカテゴリレベルを簡単に確認でき、カタログページ間のナビゲーションに簡単にアクセスできることです。

### 履歴ベースのパンくずリスト

履歴（またはパス）ベースのナビゲーションは、ブラウザーの戻るボタンに似ています。 このタイプのナビゲーションを使用すると、ユーザーは変更を加えずに、前に訪問したページにすばやく戻ることができます。

このタイプの利点は、カテゴリページで複数のフィルターを選択した後、前のページに戻りたい場合に最も役立つことです。

例： `Home > What's New > Gear > Bags`

### 属性ベースのパンくずリスト

このタイプのパンくずリストには、カテゴリページで選択された属性が表示されます。 他のタイプとの主な違いは、属性ベースのパンくずリストが、特定の製品（価格、品質、色など）のナビゲーションレイヤーで顧客が選択したフィルターとオプションを表している点です。

例： `Home > Suits > All Suits > Refined by > Slim Fit`

## CMS ページからパンくずリストを追加/削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Web]**.

   ![CMS ページのパンくずリストを表示](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. を展開します。 _[!UICONTROL Default Pages]_」セクションに入力します。

1. 選択を解除すると、 **[!UICONTROL Use system value]** チェックボックス。

1. 設定 **[!UICONTROL Show Breadcrumbs for CMS Pages]** から `No` または `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

>[!NOTE]
>
>親カテゴリがある場合、子カテゴリページのパンくずリストに親カテゴリが表示されません `Browsing Category`= `Deny` [カテゴリ権限](category-permissions.md) 設定。
