---
title: カタログイベントカルーセルウィジェット
description: カタログイベントカルーセルウィジェットを使用して、今後のイベントのスライダーをページに表示する方法を説明します。
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# カタログイベントカルーセルウィジェット

{{ee-feature}}

カタログイベントカルーセルウィジェットには、今後のイベントのスライダーと各イベントのカウントダウンティッカーが表示されます。 カルーセルを表示するページとページレイアウトの領域を選択し、一度に表示するイベントの幅と数を制御することができます。 取得する結果は、テーマ、ページ上での表示位置、選択したオプションによって異なります。

![左側のサイドバーのイベントカルーセル](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## 手順 1：カタログカルーセルウィジェットを有効にする

開始する前に、に従ってください [指示](../merchandising-promotions/event-configure.md) を設定します _カタログイベント_ ストアフロントに対して有効になるようにウィジェット。

![カタログイベントの設定](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## 手順 2：ウィジェットの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Widget]**.

1. が含まれる _[!UICONTROL Settings]_セクションで、次の操作を行います。

   - を設定 **[!UICONTROL Type]** 対象： `Catalog Events Carousel`.

   - を選択します。 **[!UICONTROL Design Theme]** それは店で使われます。

1. クリック **[!UICONTROL Continue]**.

   ![イベントカルーセルのウィジェット設定](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. が含まれる _[!UICONTROL Storefront Properties]_セクションで、次の操作を行います。

   - の場合 **[!UICONTROL Widget Title]**、ウィジェットのわかりやすいタイトルを入力します。

     このタイトルは、次の場所からのみ表示されます： _Admin_.

   - の場合 **[!UICONTROL Assign to Store Views]**&#x200B;で、ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択することも、 `All Store Views`. 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]**&#x200B;を入力し、この項目がページの同じ部分に他のユーザーと表示される順序を決定します。 （`0` =最初、 `1` =秒、 `3` = 3 番目、など）。

     ![ウィジェットのストアフロントのプロパティ](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## 手順 3：場所の選択

1. が含まれる _レイアウトの更新_ セクションで、をクリック **[!UICONTROL Add Layout Update]**.

1. を設定 **[!UICONTROL Display On]** 対象： `Specified Page`.

1. を設定 **[!UICONTROL Page]** 対象： `CMS Home Page`.

1. を設定 **[!UICONTROL Container]** 次のいずれか：

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >結果は、テーマやページのレイアウトによって異なります。 また、を指定する必要があります _[!UICONTROL Catalog Events Carousel Default Template]_カテゴリ設定で定義します。

1. イベントカルーセルをストアフロントの別の場所に表示する場合は、をクリックします **[!UICONTROL Add Layout Update]** その場所に対してこれらの手順を繰り返します。

   ![レイアウトの更新](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save and Continue Edit]**.

   現時点では、メッセージを無視してキャッシュを更新できます。

## 手順 4：オプションの設定

1. 左パネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. の場合 **[!UICONTROL Frame Size]**&#x200B;で、スライダーに同時にリストするイベントの数を入力します。

   一度に 1 つのイベントのみを表示するには、次のように入力します `1`.

1. の場合 **[!UICONTROL Scroll]**&#x200B;を選択し、クリックごとにスクロールするイベントの数を入力します。

   次のイベントまでスクロールするには、と入力します。 `1`.

1. カスタム幅の場合は、ピクセル数を入力します **[!UICONTROL Block Custom Width]**.

   次のサンプルページでは、カスタムの幅を 250 ピクセルに設定しています。

   ![カスタム幅ウィジェットオプション](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

1. キャッシュを更新するように求めるプロンプトが表示されたら、ページ上部のメッセージに記載されているリンクをクリックし、指示に従います。
