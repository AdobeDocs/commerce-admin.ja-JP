---
title: カタログイベントカルーセルウィジェット
description: カタログイベントカルーセルウィジェットを使用して、今後のイベントのスライダーをページに表示する方法を説明します。
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# カタログイベントカルーセルウィジェット

{{ee-feature}}

カタログイベントカルーセルウィジェットには、今後のイベントのスライダーと、各イベントのカウントダウンティッカーが表示されます。 カルーセルを表示するページレイアウトのページと領域を選択し、一度に表示されるイベントの幅と数を制御できます。 取得される結果は、テーマ、ページ上で表示される位置、選択したオプションによって異なります。

![左側のサイドバーのイベントカルーセル](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## 手順 1：カタログカルーセルウィジェットを有効にする

開始する前に、 [instructions](../merchandising-promotions/event-configure.md) を設定するには、以下を実行します。 _カタログイベント_ ストアフロントで有効にするためのウィジェット。

![カタログイベントの設定](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## 手順 2：ウィジェットを作成する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅で、 **[!UICONTROL Add Widget]**.

1. Adobe Analytics の _[!UICONTROL Settings]_セクションで、以下の操作を実行します。

   - 設定 **[!UICONTROL Type]** から `Catalog Events Carousel`.

   - を選択します。 **[!UICONTROL Design Theme]** それは店で使われている。

1. クリック **[!UICONTROL Continue]**.

   ![イベントカルーセルのウィジェット設定](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. Adobe Analytics の _[!UICONTROL Storefront Properties]_セクションで、以下の操作を実行します。

   - の場合 **[!UICONTROL Widget Title]**」で、ウィジェットの説明的なタイトルを入力します。

     このタイトルは、 _管理者_.

   - の場合 **[!UICONTROL Assign to Store Views]**」で、ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択するか、 `All Store Views`. 複数のビューを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

   - （オプション）の場合 **[!UICONTROL Sort Order]**」、数値を入力して、この項目がページの同じ部分に他の項目と共に表示される順序を決定します。 (`0` =最初 `1` =秒 `3` = 3 番目、など )

     ![Widget ストアフロントプロパティ](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## 手順 3：場所の選択

1. Adobe Analytics の _レイアウトの更新_ セクションで、 **[!UICONTROL Add Layout Update]**.

1. 設定 **[!UICONTROL Display On]** から `Specified Page`.

1. 設定 **[!UICONTROL Page]** から `CMS Home Page`.

1. 設定 **[!UICONTROL Container]** 次のいずれかを選択します。

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >結果は、テーマとページのレイアウトに応じて異なります。 また、 _[!UICONTROL Catalog Events Carousel Default Template]_」と入力します。

1. ストアフロントの別の場所にイベントカルーセルを表示する場合は、 **[!UICONTROL Add Layout Update]** その場所に対して、上記の手順を繰り返します。

   ![レイアウトの更新](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save and Continue Edit]**.

   現時点では、メッセージを無視してキャッシュを更新できます。

## 手順 4：オプションの設定

1. 左側のパネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. の場合 **[!UICONTROL Frame Size]**」で、同時にスライダーに表示するイベントの数を入力します。

   一度に 1 つのイベントのみを表示するには、「 `1`.

1. の場合 **[!UICONTROL Scroll]**&#x200B;をクリックしてスクロールするイベントリストの数を入力します。

   次のイベントにスクロールするには、「 `1`.

1. カスタムの幅の場合は、 **[!UICONTROL Block Custom Width]**.

   次の例では、カスタムの幅を 250 ピクセルに設定しています。

   ![カスタム幅ウィジェットオプション](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save]**.

1. キャッシュを更新するよう求められたら、ページ上部のメッセージに表示されるリンクをクリックし、指示に従います。
