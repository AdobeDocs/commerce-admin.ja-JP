---
title: '''[!DNL Page Builder] ウォークスルーパート 2：ブロック`'
description: を使用する際の、単純なブロックと動的ブロックの違いについて説明します。 [!DNL Page Builder].
exl-id: 864a3078-8cb3-4add-bdb7-14189aba535e
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '2053'
ht-degree: 0%

---

# [!DNL Page Builder] ウォークスルーパート 2：ブロック

次の演習では、 [単純ブロック](../content-design/blocks.md) および [動的ブロック](dynamic-block.md)、およびの使用方法 [!DNL Page Builder] をクリックして、各タイプのブロックを作成します。

>[!NOTE]
>
>[!DNL Page Builder] には、という名前の新しいコンテンツタイプがあります。 _バナー_（最初のチュートリアルの演習で紹介される機能で、以前のバナー機能とは無関係です）。 以前は、「バナー」オプションは [コンテンツメニュー](../content-design/content-menu.md)、現在は _ダイナミックブロック_.

![ストアフロントの動的ブロック](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

この演習は、が完了していることを前提としています。 [第 1 部：シンプルなページ](1-simple-page.md)( 前提条件や [ダウンロードしたサンプルファイル](./assets/simple-page-assets.zip). このチュートリアルの演習の各部に従って順番に進みます。

>[!NOTE]
>
>これらのチュートリアルの演習は、 [!DNL Page Builder] workspace（2.4.1 リリース） 以前のAdobe Commerceリリースを使用している場合は、 [!DNL Page Builder] ～に含まれる演習 [[!DNL Commerce] 2.3 ユーザーガイド](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html).

## パート 1：単純なブロックを作成する

このチュートリアルの演習では、コンテンツを含む単純なブロックを次の場所から作成します。 [!DNL Google Maps]. 単純なブロックは、 _CMS ブロック_ または _静的ブロック_&#x200B;を設定する必要があります。 単純なブロックは、再利用するコンテンツに最適です。

### 手順 1：ブロックを作成する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 右上隅で、 **[!UICONTROL Add New Block]**.

1. の場合 **[!UICONTROL Block Title]**，と入力します。 `Google Map`.

1. の場合 **[!UICONTROL Identifier]**，と入力します。 `google-map`.

1. を選択します。 **[!UICONTROL Store View]** ブロックを使用できる場所。

   ![ブロック情報](./assets/pb-tutorial2-block-new-google-map.png){width="600" zoomable="yes"}

1. 右上隅で、 **[!UICONTROL Save]**.

### 手順 2: [!DNL Google Map]

1. 下にスクロールして、 [!DNL Page Builder] コンテンツのプレビュー（現在は空）を表示し、「 **[!UICONTROL Edit with Page Builder]**.

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Media]** をクリックし、 **[!UICONTROL Map]** プレースホルダーをステージに追加します。

   ![マップをステージにドラッグする](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   次の場合、ストアの場所へのマップが表示されます。 [!DNL Google Maps] がお客様のストアに対して設定されている。

   ![ストア用に設定されたGoogle Map](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   次の場合にプレースホルダーマップが表示されます。 [!DNL Google Maps] お客様のストア用にまだ設定されていません。

   ![[!DNL Google Maps] プレースホルダー](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

1. ステージの右上隅で、 _全画面表示を閉じる_ (![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png)) アイコンをクリックします。

   このアイコンをクリックすると、 _[!UICONTROL Content]_プレビューが表示されたブロックのセクション。

1. 右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

### 手順 3：設定 [!DNL Google Maps]

次の場合 [!DNL Google Maps] は既にストア用に設定されています。この手順をスキップして、次の手順に進むことができます。

1. 次に移動： [Google Cloud Platform コンソール](https://console.cloud.google.com/google/maps-apis/overview).

1. 「プロジェクト」ドロップダウンをクリックし、API キーを追加するプロジェクトを選択または作成します。

1. API 資格情報を設定するには、 [instructions][1] （内） [!DNL Google Maps] ドキュメント。

1. API キーをクリップボードにコピーします。

1. に戻ります。 [!DNL Commerce] 管理者に問い合わせて、に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Content Management]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![高度なコンテンツツール](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   詳しくは、 [!UICONTROL Content Management Advanced Tools] 設定オプション ( [_設定リファレンスガイド_](../configuration-reference/general/content-management.md).

1. の場合 **[!UICONTROL Google Maps API Key]**、コピーしたキーを貼り付けます。

1. クリック **[!UICONTROL Test Key]**.

   キーに問題がある場合は、に戻ります。 [!DNL Google Maps] 問題を解決する Platform サイト。 その後、再度お試しください。

1. 鍵が確認されたら、 **[!UICONTROL Save Config]**.

### 手順 4：ページにブロックを追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. グリッドで、 _[!UICONTROL Simple Page]_最初のチュートリアルで作成し、「 」を選択します。**[!UICONTROL Edit]**（内）_[!UICONTROL Action]_ 列。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 「 」セクションで、「 」をクリックします。 **[!UICONTROL Edit with Page Builder]** または、コンテンツプレビュー領域内に配置します。

1. Adobe Analytics の [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、**[!UICONTROL Row]**プレースホルダーをステージの上部に配置します。

   ![ステージの先頭への行の追加](./assets/pb-tutorial2-elements-row-drag-top.png){width="600" zoomable="yes"}

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Add Content]** をクリックし、 **[!UICONTROL Block]** プレースホルダーを新しい行に追加します。

1. 空のブロックコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ (![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![ブロックツールボックス](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. [ ブロックを編集 ] ページで、 **[!UICONTROL Select Block]**.

   ![ブロックを選択](./assets/pb-add-content-block-settings-block-select.png){width="600" zoomable="yes"}

1. 検索ボックスに、 `map` をクリックし、Enter/Return キーを押して、作成したブロックを探します。

   ![リスト内のブロックを検索](./assets/pb-add-content-block-settings-block-find.png){width="600" zoomable="yes"}

1. グリッドで、 **[!UICONTROL Select]** 選ぶ [!DNL Google Maps] ブロック。

1. 右上隅で、 **[!UICONTROL Save]** 設定を保存し、に戻るには、以下の手順に従います。 [!DNL Page Builder] ワークスペース。

1. ステージの右上隅で、 _全画面表示を閉じる_ (![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png)) アイコンをクリックします。

   このアイコンをクリックすると、 _[!UICONTROL Content]_」セクションにプレビューが表示されます。

1. 右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

**おめでとうございます。** これで、ブロックの演習の最初の部分が完了しました。 作業内容は必ず参照用に保持してください。

## パート 2：ダイナミックブロックを作成する

ダイナミックブロックには、場所、タイミング、および表示先を決定するロジックが含まれます。 このチュートリアルの演習では、価格ルールの条件が満たされたときにトリガーされ、特定の顧客セグメントにのみ表示されるプロモーション用の動的ブロックを作成します。 この例の結果は、最初の演習で作成したバナーに似ていますが、ストアフロントにいつ表示されるかを制御するロジックを使用します。

![Luma Tee プロモーションの例](./assets/pb-tutorial2-dynamic-block-row-page.png){width="600" zoomable="yes"}

### 手順 1：新しいダイナミックブロックを作成する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![ダイナミックブロックリスト](./assets/pb-tutorial2-block-dynamic-add.png){width="700" zoomable="yes"}

1. 右上隅で、 **[!UICONTROL Add Dynamic Block]**.

   ![新しいダイナミックブロックページ](./assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 新しいダイナミックブロックの基本設定を入力します。

   - 設定 **[!UICONTROL Enable Dynamic Block]** から `Yes`.

   - の場合 **[!UICONTROL Dynamic Block Name]**，と入力します。 `Tee Shirt Promo`.

   - 設定 **[!UICONTROL Dynamic Block Type]** から `Content Area` をクリックします。 **[!UICONTROL Done]**.

     ダイナミックブロックタイプは、 [ページレイアウト](../content-design/page-layout.md) ブロックを配置する ストアに動的ブロックを設定する場合は、ページレイアウトと [テーマ](../content-design/themes.md)を使用する場合は、空き領域を適切に使用できます。 アクティブなコンテンツ領域が固定幅に制限されているストアと、画面の全幅を拡張しているストアがあります。

     ![ダイナミックブロックタイプの設定](./assets/pb-dynamic-block-type.png){width="600" zoomable="yes"}

   - の場合 **[!UICONTROL Customer Segment]**、動的ブロックに適用する各セグメントのチェックボックスをオンにし、 **完了** をクリックして、セグメントのリストを保存します。

     次の例では、2 つの [顧客セグメント](../customers/customer-segments.md) 「 」は、性別で登録済みの顧客を識別する情報です。 この動的ブロックは、ストアで買い物をしている間にアカウントにログインした、登録済みの女性の顧客にのみ表示されます。

     ![顧客セグメントの選択](./assets/pb-dynamic-block-customer-segment.png){width="600" zoomable="yes"}

### 手順 2：設定の完了

下にスクロールして、 _[!UICONTROL Content]_セクション ( 空の [!DNL Page Builder] コンテンツのプレビューを表示し、**[!UICONTROL Edit with Page Builder]**. 次のタスクを実行します。

**タスク 1:** 背景画像を追加する

1. 行コンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ (![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

1. の下 _[!UICONTROL Appearance]_を選択します。**[!UICONTROL Full Bleed]**.

1. の場合 **[!UICONTROL Minimum Height]**，と入力します。 `400px`.

1. をスクロールします。 _[!UICONTROL Background]_「 」セクションに移動して、**[!UICONTROL Background Image]**クリックして&#x200B;**[!UICONTROL Select from Gallery]**そして、 `wide-banner-background.png` 画像は最初のチュートリアルでアップロードされました。

1. 右上隅で、 **[!UICONTROL Save]** 設定を適用し、に戻るには、次の手順に従います。 [!DNL Page Builder] ワークスペース。

   ![画像を含む行](./assets/pb-tutorial2-row-image.png){width="600" zoomable="yes"}

**タスク 2:** 列を追加

Adobe Analytics の [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、**[!UICONTROL Column]**プレースホルダーを行に配置します。

![列タイプを行にドラッグ](./assets/pb-tutorial2-column-drag.png){width="600" zoomable="yes"}

これで、行が同じ幅の 2 つの列に分割されます。

**タスク 3:** テキストを追加

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をクリックし、 **テキスト** 2 番目の列のプレースホルダー。

   ![テキストボックスを 2 列目にドラッグする](./assets/pb-tutorial2-column-text-drag.png){width="600" zoomable="yes"}

1. エディターに次の 3 行のテキストを入力します。

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![列のテキストの入力](./assets/pb-tutorial2-column-text-editor.png){width="600" zoomable="yes"}

1. 3 行のテキストをすべて選択し、ツールバーを使用して **行の高さ** から `40px`.

   ![行の高さの設定](./assets/pb-tutorial2-column-text-editor-line-height.png){width="600" zoomable="yes"}

1. を設定します。 **[!UICONTROL Font Size]** 各行に対して、次のように指定します。

   | 線 | フォントサイズ |
   |-----| ---------- |
   | 行 1: | `28px` |
   | 行 2: | `24px` |
   | 行 3: | `18px` |

   このブロックはページ上の任意の場所に配置できるので、見出しレベルではなく、デフォルトの段落スタイルを使用します。 また、列でテキストがまだ正しく折り返されていないことを確認する必要はありません。  

   ![書式設定されたテキスト](./assets/pb-tutorial2-column-text-editor-text-formatted.png){width="600" zoomable="yes"}

**タスク 4:** リンクを追加

最初の練習では、 [ボタン](buttons.md) リンクを作成するコンテンツタイプ。 この例では、エディターのツールバーからリンクを挿入する方法を示します。

1. 別のブラウザータブでストアフロントを開き、リンクのターゲットとなるページに移動します。

   完全修飾 URL またはストアドメインへの参照を省略した相対 URL を使用できます。

   完全な URL : `https://mystore.com/women/tops-women/tees-women.html`

   相対 URL : `../women/tops-women/tees-women.html`

1. に戻ります。 [!DNL Page Builder] 「ワークスペース」タブと「テキストエディター」で、 `Shop Tees >` 3 行目にテキストを入力し、「 」を選択します。 **太字** (![太字ボタン](./assets/editor-btn-bold.png)) を編集します。

1. を使用 `Shop Tees >` 3 行目のテキストが選択された状態で、「 」を選択します。 **リンクを挿入/編集** (![リンクの挿入/編集ボタン](./assets/pb-icon-add-link.png)) を編集します。

   ![リンクの挿入](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL URL]**」と入力し、準備した相対リンクを入力します。

1. 設定 **[!UICONTROL Target]** から `None`.

   この設定により、新しいタブを開くのではなく、同じブラウザーウィンドウでページが開きます。

1. の場合 **[!UICONTROL Title]**，と入力します。 `Shop Tees`.

   タイトルリンク属性は、一部のブラウザーではツールチップとして使用されます。

1. リンクを保存してに戻るには、以下を実行します。 [!DNL Page Builder] ワークスペース、クリック **[!UICONTROL OK]**.

   ![リンクの詳細](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="600" zoomable="yes"}

1. ステージの右上隅で、 _全画面表示を閉じる_ (![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png)) アイコンをクリックします。

   このアイコンをクリックすると、 _[!UICONTROL Content]_プレビューが表示されたダイナミックブロックのセクション。

1. 右上隅で、 **[!UICONTROL Save]**.

### 手順 3：価格ルールの追加

1. を開きます。 _Tey Shirt Promo_ 編集モードのダイナミックブロックが再び有効になりました。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Related Promotions]** 「 」セクションで、「 」をクリックします。 **[!UICONTROL Add Cart Price Rules]**.

   ![関連するプロモーション](./assets/pb-dynamic-blocks-related-promotions.png){width="600" zoomable="yes"}

1. 次の日： _関連する買い物かごの価格ルールの追加_ ページで、 _T シャツ 3 枚を購入し、4 枚目の無料を手に入れる_ 価格ルールとクリック **[!UICONTROL Add Selected]**.

   ![関連する買い物かごの価格ルールの追加](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

   価格ルールが _関連するプロモーション_ セクション、の下 _関連する買い物かごの価格ルール_. 複数の価格ルールを動的ブロックに関連付けることができます。 ただし、この簡単な例ではを 1 つだけ使用します。

   ![選択した買い物かごの価格ルール](./assets/pb-dynamic-block-related-cart-price-rule-list.png){width="600" zoomable="yes"}

1. 右上隅で、 **[!UICONTROL Save]**.

### 手順 4：ページにダイナミックブロックを追加する

1. Adobe Analytics の _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**

1. 次を検索： _単純なページ_ 作成した [最初のチュートリアル演習](1-simple-page.md) を開き、編集モードで開きます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 「 」セクションで、「 」をクリックします。 **[!UICONTROL Edit with Page Builder]**.

1. ダイナミックブロックと同じ画像で上の行の上にマウスポインターを置くと、ツールボックスと _削除_ ( ![削除アイコン](./assets/pb-icon-remove.png){width="20"} ) アイコンをクリックします。

   ページからの行の削除を確認するには、  **[!UICONTROL OK]** .

1. Adobe Analytics の [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、新しい&#x200B;**[!UICONTROL Row]**プレースホルダーをステージの上部に配置します。

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Add Content]** をクリックし、 **[!UICONTROL Dynamic Block]** プレースホルダーを新しい行に追加します。

   ![ダイナミックブロックを行にドラッグする](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. ダイナミックブロックコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![ダイナミックブロックツールボックス](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. 次の日： _[!UICONTROL Edit Dynamic Block]_ページ、クリック&#x200B;**[!UICONTROL Select Dynamic Block]**.

   ![ダイナミックブロックを選択](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

1. 次を検索： _[!DNL Tee Shirt Promo]_作成してクリックしたダイナミックブロック&#x200B;**[!UICONTROL Select]**.

   ダイナミックブロック情報の概要は、次のとおりです。

   ![動的ブロック情報](./assets/pb-tutorial2-dynamic-block-edit.png){width="600" zoomable="yes"}

1. デフォルトを受け入れる **[!UICONTROL Template]**, `Dynamic Block Block Template`.

1. 完了したら、「 **[!UICONTROL Save]** 設定を保存し、に戻るには、以下の手順に従います。 [!DNL Page Builder] ワークスペース。

   ![ページプレビューのダイナミックブロック](./assets/pb-tutorial2-dynamic-block-on-page.png){width="600" zoomable="yes"}

1. ステージの右上隅で、 _全画面表示を閉じる_ (![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png)) アイコンをクリックします。

   このアイコンをクリックすると、 _[!UICONTROL Content]_」セクションにプレビューが表示されます。

1. 右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

これで、ブロックの演習の 2 番目の部分が完了しました。 作業内容は必ず参照用に保持してください。

## パート 3：ダイナミックブロックを更新する

この練習の最後の部分では、ページがストア内にある間、ダイナミックブロックを編集します。 次に、顧客セグメントのメンバーとしてストアにログインし、ブロックを表示します。

![ストアフロントのダイナミックブロックのサンプル](./assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

### 手順 1：ダイナミックブロックを編集する

1. Adobe Analytics の _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. 次を検索： _[!DNL Tee Shirt Promo]_グリッドのダイナミックブロックを編集モードで開きます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 「 」セクションで、「 」をクリックします。 **[!UICONTROL Edit with Page Builder]**.

1. 列の幅を変更します。

   - 2 つの列の境界線の上にマウスポインターを置きます。

   - マウスボタンを押しながら、境界線を左に 2 つドラッグします。

     ![グリッド分割](./assets/pb-tutorial2-dynamic-block-edit-column-width.png){width="600" zoomable="yes"}

     1 列目は 12 のグリッド分割のうち 4(4/12)、2 列目は 12 のグリッド分割のうち 8(8/12)です。

     ![2 つの不等列](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png){width="600" zoomable="yes"}

1. テキストの色を変更します。

   - 最初の 2 行のテキストを選択します。

   - エディターツールバーで、「 」を選択します。 **[!UICONTROL Text Color]** をクリックし、 **[!UICONTROL White]** スウォッチ

   ![テキストカラー](./assets/pb-tutorial2-dynamic-block-edit-text-color.png){width="600" zoomable="yes"}

1. ステージの右上隅で、 _全画面表示を閉じる_ (![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png)) アイコンをクリックします。

   このアイコンをクリックすると、 _[!UICONTROL Content]_プレビューが表示されたダイナミックブロックのセクション。

1. 右上隅で、 **[!UICONTROL Save]**.

### 手順 2：ダイナミックブロックを表示する

この動的ブロックは特定の顧客セグメントのメンバーにのみ表示されるので、プロモーションを表示するには、顧客セグメントのメンバーである顧客としてログインする必要があります。 この例では、「 」ブロックは女性のお客様にのみ表示されます。

1. ストアフロントのブラウザーウィンドウを開きます。

1. サンプルページを表示するには、次のようにアドレスバーの URL を変更します。

   mystore.com/sample-page

   ストアが html サフィックスを含むように設定されている場合は、次のようにサフィックスを含めます。

   mystore.com/sample-page.html

1. 女性の顧客としてサインイン：

   - ホームページの右上隅にある、 **[!UICONTROL Sign In]**.

   - サンプルの Luma データがシステムにインストールされている場合は、次の資格情報を使用します。

     **[!UICONTROL Email]** - `roni_cost@example.com`

     **[!UICONTROL Password]** -  `roni_cost3@example.com`

   - クリック **[!UICONTROL Sign In]**.

   - サンプルページに戻り、Tee Shirt プロモーションで作成したダイナミックブロックを確認します。

   ![顧客セグメント用に表示される動的ブロック](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

これで、ブロックの演習が完了しました。 作業内容は必ず参照用に保持してください。

準備が整ったら、次に進みます。 [第 3 部：カタログコンテンツ](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
