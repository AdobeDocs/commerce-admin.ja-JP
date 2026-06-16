---
title: '[!DNL Page Builder] チュートリアル パート 1: シンプルなページ'
description: サンプルファイルを使用し、手順に従って [!DNL Page Builder]  インターフェイスでシンプルなページを作成します。
exl-id: 2c146241-675f-4d23-9513-1722d5dd3357
feature: Page Builder, Page Content
TQID: https://experienceleague.adobe.com/i6y4j2MrN59vbxZXYOqTmUyjMURsaK-WOYChOFVW2Bc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 3341
ht-degree: 0%

---

# [!DNL Page Builder] チュートリアル パート 1: シンプルなページ

この3つの部分で構成される演習に従って、独自のデザインのコンテンツ豊富なページを簡単に作成できるシンプルなページを作成して、[!DNL Page Builder] ワークスペースに慣れましょう。

![単純なページの例](./assets/pb-tutorial1-simple-layout.png){width="700" zoomable="yes"}

>[!NOTE]
>
>これらのチュートリアル演習は、2.4.1 リリースの[!DNL Page Builder] ワークスペースに対する最近の変更を反映するように更新されます。

## 始める前に

この演習を開始する前に、作業中にセッションがタイムアウトしないように、[管理者セッション有効期間](../systems/security-admin.md)を増やすことをお勧めします。

必要なコンテンツ管理設定を確認します。

- WYSIWYG エディターは、[WYSIWYG オプション &#x200B;](../content-design/editor.md#configure-the-editor)設定で有効になっています。

- [!DNL Page Builder]は、[詳細コンテンツツール &#x200B;](setup.md)設定で有効になっています。

### チュートリアル画像アセットのダウンロード

1. [`simple-page-assets`](./assets/simple-page-assets.zip) ファイルをダウンロードし、ローカルシステムにファイルを保存します。

1. ダウンロードしたファイルに移動し、圧縮されたファイルを抽出します。

   Windows システムで右クリックし、**[!UICONTROL Extract All]** ファイルを選択します。 次に、宛先フォルダーを選択し、**[!UICONTROL Extract]**&#x200B;をクリックします。

   Macでは、zip ファイルをダブルクリックして、抽出したファイルを保存先のフォルダーに移動することができます。

   フォルダーには、次の画像ファイルが含まれています。

   ![[!DNL Page Builder] ウォークスルーのファイル – シンプルなページアセット &#x200B;](./assets/pb-tutorial-simple-page-assets.png){width="500"}

このチュートリアルの3つの部分を順番に進めます。

## パート 1：バナー付きのフルブリード行

シンプルなページの演習のこの部分では、フルブリードの行とバナーを持つページを作成します。 行には、デスクトップとモバイルデバイスの異なる背景画像があります。

バナー![&#128279;](./assets/pb-tutorial1-full-bleed-with-banner.png){width="700" zoomable="yes"}付きの[!DNL Page Builder]件のフルブリード行

### 手順1：ページの作成

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add New Page]**」をクリックし、次の操作を行います。

   - このページがストアで公開されないようにするには、**[!UICONTROL Enable Page]**&#x200B;を`No`に設定します。

   - **[!UICONTROL Page Title]**&#x200B;に対して、`Simple Page`と入力します。

   ![基本ページ設定](./assets/pb-tutorial1-currently-active.png){width="600" zoomable="yes"}

1. **[!UICONTROL Design]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   **[!UICONTROL Layout]**&#x200B;がデフォルトで`Page -- Full Width`に設定されていることに注意してください。 5つの標準[&#x200B; レイアウト &#x200B;](../content-design/page-layout.md) オプションに加えて、[!DNL Page Builder]では、ページ、カテゴリ、製品の全幅レイアウトが追加されます。

1. サンプルデータが使用可能な場合は、**[!UICONTROL New Theme]**&#x200B;を`Magento Luma`に設定します。 そうでない場合は、別の利用可能なテーマを選択するか、空白のままにしてデフォルトのテーマを使用できます。

   _[!UICONTROL New Theme]_&#x200B;設定を使用すると、デフォルトのテーマを上書きしたり、別のテーマをページに適用したりできます。

   >[!NOTE]
   >
   >全幅レイアウトは、互換性のある[&#x200B; テーマ &#x200B;](../content-design/themes.md)でのみ使用できます。

   ![&#x200B; ページデザイン設定](./assets/pb-tutorial1-design-section.png){width="600" zoomable="yes"}

1. 右上隅の「**[!UICONTROL Save]**」をクリックします。

   ページを保存すると、ページの左上隅に「_シンプルなページ_」という名前が表示されます。

### 手順2：行の書式設定

1. **[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   このアクションは、空の行を含む[!DNL Page Builder] プレビューを表示します。

   >[!NOTE]
   >
   >[&#x200B; コンテンツ見出し](workspace.md) フィールドはオプションです。 デフォルトでは、テーマに従って見出しレベル 1 （H1）として書式設定されます。 この演習では、_コンテンツ見出し_&#x200B;は空白のままです。

   ![空の行を含むページコンテンツのプレビュー](./assets/pb-content-preview-empty.png){width="600" zoomable="yes"}

1. コンテンツのプレビュー領域の内側にある&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;をクリックします。

   拡張された[!DNL Page Builder] [&#x200B; ワークスペース &#x200B;](workspace.md)では、左側のパネルに、ステージでコンテンツを構築するために使用できるコンテンツツールが表示されます。

1. 空の行にマウスポインターを置くと、ツールボックスが表示されます。

   各コンテンツコンテナには、類似したオプションのセットを持つツールボックスがあります。

   ![[!DNL Page Builder]行のツールボックス &#x200B;](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

1. 行ツールボックスで、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"} アイコンを選択します。

1. _[!UICONTROL Appearance]_&#x200B;で、**全裁ち落とし**&#x200B;を選択します。

   「全裁ち落とし」設定は、行と背景のコンテンツ領域の左右の境界線を、ページの全幅に拡張します。

   ![行の設定 – フルブリード &#x200B;](./assets/pb-tutorial1-row-settings-appearance-full-bleed.png){width="600" zoomable="yes"}

1. _[!UICONTROL Advanced]_&#x200B;セクションまでスクロールして、すべての&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;設定を`0`に設定します。

   この設定により、バナーが行の全幅を拡張します。

   ![行設定 – マージンとパディング &#x200B;](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. 設定を保存して[!DNL Page Builder] ワークスペースに戻るには、ページの上部までスクロールし、右上隅の「**[!UICONTROL Save]**」をクリックします。

### ステップ 3：バナーを追加する

>[!NOTE]
>
>[!DNL Page Builder]には、_Banner_&#x200B;という新しいコンテンツタイプがあります。このステップで紹介します。 以前はコンテンツメニューの&#x200B;_バナー_ オプションでしたが、現在は&#x200B;_動的ブロック_&#x200B;になっています。

1. [!DNL Page Builder] パネルで、**[!UICONTROL Media]**&#x200B;を展開し、**バナー**&#x200B;のプレースホルダーをステージにドラッグします。

   ![&#x200B; バナーコンテンツタイプをステージにドラッグする](./assets/pb-tutorial1-banner-drag-to-stage.png){width="600" zoomable="yes"}
1. バナーコンテナにカーソルを合わせると、ツールボックスが表示されます。

   >[!NOTE]
   >
   >ステージには2つのコンテンツコンテナがあり、それぞれに個別のツールボックスがあります。 バナーは行の内側にネストされているため、正しいツールボックスで作業していることを確認してください。

   ツールボックスに加えて、_画像をアップロード_&#x200B;および&#x200B;_ギャラリーから選択_ ボタンが含まれているため、ステージから直接バナーを素早く変更できます。

   ![&#x200B; バナーツールボックス &#x200B;](./assets/pb-tutorial1-banner-toolbox.png){width="600" zoomable="yes"}

1. バナーツールボックスで、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

1. _[!UICONTROL Appearance]_&#x200B;で、**[!UICONTROL Collage Right]**&#x200B;を選択します。

   コラージュの右設定では、バナーの右側にコンテンツが配置されます。

   ![&#x200B; バナーの外観 – コラージュ右](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

1. _[!UICONTROL Background]_&#x200B;セクションまでスクロールして、バナーの背景画像を設定します。

   - **[!UICONTROL Background Image]**&#x200B;の場合、「**アップロード**」をクリックします。

     ![&#x200B; バナーの背景 – 画像をアップロード &#x200B;](./assets/pb-tutorial1-row-background-image-upload.png){width="600" zoomable="yes"}

     抽出した単純なページアセットを保存したディレクトリに移動し、`wide-banner-background.jpg` ファイルを選択します。

     画像がアップロードされ、アップロードされた画像のサムネールが表示されます。 ファイル名、画像サイズおよびファイルサイズは以下のとおりです。

     ![&#x200B; メディアギャラリーに背景画像をアップロード &#x200B;](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

   - **[!UICONTROL Background Mobile Image]**&#x200B;の場合、「**アップロード**」をクリックします。

     同じファイルディレクトリで、`wide-banner-background-mobile.jpg` ファイルを選択します。

     モバイル背景画像は、モバイルデバイスに使用され、デスクトップブラウザーウィンドウがモバイルデバイスの幅にリサイズされるたびに使用されます。

     ![&#x200B; モバイル用のサンプル バナー画像ファイルの選択](./assets/pb-tutorial1-row-settings-background-mobile-image-selected.png){width="600" zoomable="yes"}

   - ページの先頭までスクロールして&#x200B;**[!UICONTROL Save]**&#x200B;をクリックし、設定を保存して[!DNL Page Builder] ワークスペースに戻ります。

     背景がステージに表示され、行の全幅が拡張されます。

     ![背景画像を含むバナー](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

   行の右側に表示されるプレースホルダーテキストに注目してください。 このテキストの位置は、_Collage Right_&#x200B;のアピアランス設定を反映しています。

1. プレースホルダーテキストをクリックし、次のメッセージを2行として入力します。

   `Get fit and look fab in new seasonal styles.`

   `New LUMA yoga collection`

   エディターツールバーがテキストボックスの上に表示されます。 テキストは、ステージから直接入力するか、バナーツールボックスで&#x200B;_設定_&#x200B;を選択して入力および書式設定できます。

   ![&#x200B; ステージからバナーコンテンツを編集しています](./assets/pb-tutorial1-banner-stage-text.png){width="600" zoomable="yes"}

1. テキストに書式を適用する：

   - テキストの最初の行を選択します。 次に、**形式**&#x200B;の下のエディターツールバーで、`Heading 2`を選択します。

     ![見出し2形式の適用](./assets/pb-tutorial1-banner-stage-text-format-line1.png){width="600" zoomable="yes"}

   - 2行目のテキストを選択します。 次に、**形式**&#x200B;の下のエディターツールバーで、`Paragraph`を選択します。

   書式設定では、現在のテーマに関連付けられているスタイルシートのスタイルが適用されます。

   書式設定されたテキストを含むコンテンツステージの![&#x200B; バナー](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="600" zoomable="yes"}
__

1. バナーツールボックスを表示するには、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンをもう一度選択してから、_[!UICONTROL Content]_&#x200B;セクションまでスクロールします。

   テキストが「_メッセージテキスト_」ボックスに表示されます。 テキストは、ステージまたはバナー設定の&#x200B;_[!UICONTROL Content]_&#x200B;セクションから入力および編集できます。

   ![&#x200B; バナー設定 – メッセージテキスト &#x200B;](./assets/pb-tutorial1-banner-settings-content-message-text.png){width="600" zoomable="yes"}

1. _[!UICONTROL Content]_&#x200B;セクションを続けて、バナーリンクとボタンを設定します。

   - **リンク**&#x200B;を`Category`に設定し、**[!UICONTROL Select]**&#x200B;をクリックしてカテゴリーツリーを表示します。

   - リンクされたカテゴリとして`What's New`を選択します。

     ![&#x200B; バナーコンテンツ – カテゴリへのリンク &#x200B;](./assets/pb-tutorial1-banner-settings-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Show Button]**&#x200B;を`Always`に設定します。

   - **[!UICONTROL Button Text]**&#x200B;に対して、`Shop Now`をボタンに表示されるテキストとして入力します。

   - **[!UICONTROL Button Type]**&#x200B;の場合、`Primary`の既定値を受け入れます。

     現在のテーマのボタンスタイルによって、ボタンの形式が決まります。

1. バナーオーバーレイを設定します。

   オーバーレイを使用して、「アピアランス」設定で定義されているアクティブコンテンツ領域に背景色を適用できます。 バナーの背景画像は、バナーの全幅にわたって表示されたままになります。

   - **[!UICONTROL Show Overlay]**&#x200B;を`Always`に設定します。

   - **[!UICONTROL Overlay Color]**&#x200B;に対して、次のいずれかの操作を行います。

      - カラーの正方形をクリックし、白いスウォッチを選択します。
      - 「_色なし_」テキストボックスをクリックし、`White`または16進数値`#ffffff`を入力します。

     次に、**[!UICONTROL Apply]**&#x200B;をクリックします。

     ![&#x200B; バナー設定 – ボタンオーバーレイの色](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}

   - ページの先頭までスクロールして&#x200B;**[!UICONTROL Save]**&#x200B;をクリックし、設定を保存して[!DNL Page Builder] ワークスペースに戻ります。

     ボタンは、ステージのバナーメッセージの下に表示されます。

     テキストメッセージとボタンを含むコンテンツステージの![&#x200B; バナー](./assets/pb-tutorial1-banner-stage-background-color.png){width="600" zoomable="yes"}

1. ステージの右上隅で、_フルスクリーンを閉じる_ （![&#x200B; フルスクリーンアイコンを閉じる](./assets/pb-icon-reduce.png)）アイコンをクリックします。

   このアイコンをクリックすると、プレビューが表示されたページの&#x200B;_[!UICONTROL Content]_&#x200B;セクションに戻ります。

   2つのワークスペースモードは、いつでも切り替えることができます。

1. 右上隅の&#x200B;**[!UICONTROL Save]**&#x200B;矢印をクリックし、**[!UICONTROL Save & Close]**&#x200B;を選択します。

1. プロンプトが表示されたら、ページ上部のメッセージの[Cache Management](../systems/cache-management.md) リンクをクリックし、無効なキャッシュを更新します。

## パート 2:2つの同じ列を持つ行が含まれる

この部分では、ページに行を追加し、その行を2つの等しい列に分割します。 次に、リンクされた画像を各列に追加します。 手順では、最初の行の前に新しい各行が追加され、[!DNL Page Builder] パネルがステージに合わせて並べられます。 演習の最後に、行を単純ページの例に一致するように並べ替えます。

![同じ列が2つ含まれる行を使用するページの例](./assets/pb-tutorial1-contained-row-with-two-equal-columns.png){width="600" zoomable="yes"}

### 手順1：行を追加する

1. ページグリッドで、この演習の最初の部分で作成した&#x200B;_シンプルなページ_&#x200B;を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;を選択します。

1. **[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. コンテンツのプレビュー領域の内側にある&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;をクリックします。

1. _[!UICONTROL Layout]_&#x200B;の下の[!DNL Page Builder] パネルで、**[!UICONTROL Row]**&#x200B;プレースホルダーをステージにドラッグし、バナーの上に配置します。

   赤いガイドラインは、2つの行の境界を示します。

   ![&#x200B; バナーの上に新しい行を追加する](./assets/pb-tutorial1-row-drag-to-stage.png){width="600" zoomable="yes"}

1. 新しい行にカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![行のツールボックス &#x200B;](./assets/pb-tutorial1-row-settings.png){width="600" zoomable="yes"}

1. _[!UICONTROL Appearance]_&#x200B;で、**Contained**&#x200B;のデフォルト設定を受け入れます。

   この設定は、行のコンテンツ領域を、テーマで定義されたページの幅に制限します。

   ![&#x200B; デフォルトの「含まれるアピアランス」設定を維持](./assets/pb-tutorial1-row-settings-appearance.png){width="600" zoomable="yes"}

1. 右上隅の「**[!UICONTROL Save]**」をクリックして設定を保存し、[!DNL Page Builder] ワークスペースに戻ります。

### 手順2：列の追加

1. _[!UICONTROL Layout]_&#x200B;の下の[!DNL Page Builder] パネルで、**[!UICONTROL Column]**&#x200B;プレースホルダーを新しい行にドラッグします。

   ![列コンテンツタイプをステージにドラッグする](./assets/pb-tutorial1-column-drag-to-stage.png){width="600" zoomable="yes"}

   行は同じ幅の2つの列に分けられます。 各列は、コンテンツ用の個別のコンテナであり、専用のツールボックスがオプションで用意されています。

   ![2列の幅が同じ行](./assets/pb-tutorial1-columns-equal-width.png){width="600" zoomable="yes"}

1. 最初の列の左上隅にある円形の&#x200B;_グリッド_ コントロール（![&#x200B; グリッドコントロール &#x200B;](./assets/pb-icon-grid-control.png)）をクリックして、グリッドガイドラインを表示します。

   グリッドは、コンテンツが一貫して調整され、デスクトップとモバイルデバイスの両方で正しくレンダリングされることを保証します。 グリッドサイズの設定について詳しくは、[!DNL Page Builder]設定トピックの「[設定 [!DNL Page Builder]](setup.md#configure-page-builder)」セクションを参照してください。

   各列コンテナの上部境界にある括弧（6/12）の数値は、各列のグリッド分割数と行の分割数の合計数を示します。

   ![列のグリッドサイズの詳細を表示](./assets/pb-tutorial1-columns-grid-size.png){width="600" zoomable="yes"}

### 手順3：リンクを含む画像の追加

このステップでは、画像をバナーにアップロードする方法を説明します。

1. [!DNL Page Builder] パネルで、**[!UICONTROL Media]** セクションを展開し、**[!UICONTROL Image]** プレースホルダーを最初の列にドラッグします。

   ![画像コンテンツタイプを最初の列にドラッグする](./assets/pb-tutorial1-column1-media-image-drag.png){width="600" zoomable="yes"}

1. サンプルイメージをプレースホルダーに挿入します。

   ![画像プレースホルダー](./assets/pb-tutorial1-column-image-upload.png){width="600" zoomable="yes"}

   システム上にある画像の場合は、次のいずれかの方法を選択できます。

   - **画像ファイルをアップロード**：最初の列で、**[!UICONTROL Upload Image]**&#x200B;をクリックします。 次に、抽出した単純なページアセットを保存したディレクトリに移動し、`small-banner-1.jpg` ファイルを選択します。

     ![最初の列に画像をアップロードしました](./assets/pb-tutorial1-column1-image.png){width="600" zoomable="yes"}

     この操作を繰り返して、`small-banner-2.jpg` ファイルを2番目の列に追加します。

   - **画像ファイルをドラッグします**: デスクトップで、シンプルなページアセットフォルダーを開き、[!DNL Page Builder] ステージで作業している管理ブラウザーウィンドウと並べて配置します。 次に、シンプルなページアセットフォルダーからファイル `small-banner-1.jpg`をドラッグし、最初の列にドロップします。

     ![画像を2番目の列にドラッグします](./assets/pb-tutorial1-column-image-drag.png){width="600" zoomable="yes"}

     この操作を繰り返して、`small-banner-2.jpg` ファイルを2番目の列に追加します。

1. 各画像にリンクするカタログのページを決定します。

1. 最初の列の画像にカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![画像ツールボックス &#x200B;](./assets/pb-tutorial1-column1-image-settings.png){width="600" zoomable="yes"}

1. 画像をカテゴリにリンクします。

   - 下にスクロールして、**Link**&#x200B;を`Category`に設定します。

   - カテゴリーツリーで、ドリルダウンして`Men's Hoodies & Sweatshirt` カテゴリを選択します。

   - 右上隅の設定を&#x200B;**[!UICONTROL Save]**&#x200B;し、[!DNL Page Builder] ワークスペースに戻ります。

1. 前の手順を繰り返して、2列目の画像を&#x200B;_歯車_ カテゴリにリンクします。

1. ステージの右上隅で、_フルスクリーンを閉じる_ （![&#x200B; フルスクリーンアイコンを閉じる](./assets/pb-icon-reduce.png)）アイコンをクリックします。

   このアイコンをクリックすると、プレビューが表示されたページの&#x200B;_[!UICONTROL Content]_&#x200B;セクションに戻ります。

1. 右上隅の&#x200B;**[!UICONTROL Save]**&#x200B;矢印をクリックし、**[!UICONTROL Save & Close]**&#x200B;を選択します。

1. プロンプトが表示されたら、ページ上部のメッセージの[Cache Management](../systems/cache-management.md) リンクをクリックし、無効なキャッシュを更新します。

## パート 3：不均等な列を持つ全角行

このページの最後の行には、製品レビューのコンテンツが表示されています。 全幅の行を追加し、幅の異なる2つの列に分割します。 最初の列に背景画像が追加され、一致する背景色が行に適用されて統一された効果が得られます。

![異なる幅の列を含む全幅行の例](./assets/pb-tutorial1-full-width-row-two-unequal-columns.png){width="500"}

### 手順1：行を追加する

1. ページグリッドで、この演習の最初の部分で作成した&#x200B;_シンプルなページ_&#x200B;を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;を選択します。

1. **[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. コンテンツのプレビュー領域の内側にある&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;をクリックします。

1. _[!UICONTROL Layout]_&#x200B;の下の[!DNL Page Builder] パネルで、**[!UICONTROL Row]**&#x200B;プレースホルダーをステージにドラッグし、この演習の2番目の部分で作成した行の上に配置します。

   赤いガイドラインは、2つの行の境界を示します。

   ![新しい行を追加する](./assets/pb-tutorial1-add-new-row.png){width="600" zoomable="yes"}

1. 新しい行にカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![行のツールボックス &#x200B;](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. _[!UICONTROL Appearance]_&#x200B;の下の行を編集ページで、**[!UICONTROL Full Width]**&#x200B;を選択します。

   この設定は、コンテンツ領域をテーマで定義される最大ページ幅に制限します。 背景色や画像は制限されず、行の幅が広くなります。

   ![全幅のアピアランスの選択](./assets/pb-tutorial1-row-settings-appearance-full-width.png){width="600" zoomable="yes"}

1. _[!UICONTROL Background]_&#x200B;セクションに、`#f1f1f1`を&#x200B;**[!UICONTROL Background Color]**&#x200B;として入力します。

   ![背景色の設定](./assets/pb-tutorial1-row-settings-background-color.png){width="600" zoomable="yes"}

1. _[!UICONTROL Advanced]_&#x200B;セクションまでスクロールし、すべての&#x200B;**マージンとパディング**&#x200B;の値を`0`に設定します。

   ![余白とパディングの設定](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. ページの先頭までスクロールして&#x200B;**[!UICONTROL Save]**&#x200B;をクリックし、設定を保存して[!DNL Page Builder] ワークスペースに戻ります。

   行の背景色は淡いベージュになっています。

   ![&#x200B; ステージの背景色の行](./assets/pb-tutorial1-row-background-beige.png){width="600" zoomable="yes"}

### 手順2：幅の異なる列を追加する

1. _[!UICONTROL Layout]_&#x200B;の下の[!DNL Page Builder] パネルで、**[!UICONTROL Column]**&#x200B;プレースホルダーをステージの一番上の行にドラッグします。

   ![&#x200B; ステージへの列のドラッグ &#x200B;](./assets/pb-tutorial1-column-drag.png){width="600" zoomable="yes"}

1. 最初の列の右端を、グリッド上の12の4つの位置（`4/12`）にドラッグします。

   2番目の列のサイズは、12 （`8/12`）のうち8つに調整されます。

   ![最初の列のサイズ変更](./assets/pb-tutorial1-column-first-4.png){width="600" zoomable="yes"}

1. 最初の列コンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

1. _[!UICONTROL Advanced]_&#x200B;セクションまでスクロールし、すべての&#x200B;**マージンとパディング**&#x200B;の値を`0`に設定します。

   ![余白とパディングの設定](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. ページの先頭までスクロールして&#x200B;**[!UICONTROL Save]**&#x200B;をクリックし、設定を保存して[!DNL Page Builder] ワークスペースに戻ります。

### 手順3：最初の列に画像を追加する

1. [!DNL Page Builder] パネルで、**[!UICONTROL Media]**&#x200B;を展開し、**[!UICONTROL Image]** コンテンツタイプを最初の列にドラッグします。

   ![画像コンテンツタイプを最初の列にドラッグする](./assets/pb-tutorial1-column1-image-drag.png){width="600" zoomable="yes"}

1. 画像プレースホルダーで、**[!UICONTROL Upload Image]**&#x200B;をクリックします。

   ![画像をアップロード &#x200B;](./assets/pb-tutorial1-column1-image-upload.png){width="600" zoomable="yes"}

1. 抽出した単純なページアセットを保存したディレクトリに移動し、`review-image.jpg` ファイルを選択します。

   アップロードされた画像は最初の列に表示され、行の背景色とシームレスにブレンドされます。

   ![画像を列に追加しました](./assets/pb-tutorial1-column1-image-uploaded.png){width="600" zoomable="yes"}

### 手順4：レビューコンテンツを2列目に追加する

行の2番目の列には、5つ星の評価画像や書式設定されたテキストメッセージなど、顧客レビューのコンテンツを含める必要があります。

1. [!DNL Page Builder] パネルで、**[!UICONTROL Elements]** セクションを展開し、**[!UICONTROL Text]** コンテンツタイプを2番目の列にドラッグします。

   ![&#x200B; テキストコンテンツタイプをステージにドラッグする](./assets/pb-tutorial1-column2-text-drag.png){width="600" zoomable="yes"}

1. テキスト要素をクリックして、エディターツールバーを表示します。

1. ツールバーで、_画像を挿入_ （![画像を挿入アイコン &#x200B;](./assets/editor-btn-insert-edit-image.png)）アイコンをクリックし、次の操作を行います。

   ![&#x200B; テキストに画像を挿入](./assets/pb-tutorial1-column2-editor-toolbar-insert-image.png){width="600" zoomable="yes"}

   - _[!UICONTROL Insert/edit image]_&#x200B;ダイアログで、_[!UICONTROL Source]_ フィールドの横にある&#x200B;_検索_ （![検索アイコン &#x200B;](./assets/editor-btn-find-source.png)）アイコンをクリックします。

     ![画像を挿入/編集ダイアログ &#x200B;](./assets/pb-tutorial1-column2-text-insert-edit-image.png){width="600" zoomable="yes"}

   - _[!UICONTROL Select Images]_&#x200B;ページで、**[!UICONTROL Choose Files]**&#x200B;をクリックします。

   - 単純なページアセットを保存したフォルダーで、`rating.png`を選択します。

   - ページに戻り、画像タイルをダブルクリックして選択し、そのURLをSource フィールドに挿入します。

     ![&#x200B; ページ上の画像を選択しています](./assets/pb-tutorial1-column2-editor-gallery-select-image.png){width="600" zoomable="yes"}

   - **[!UICONTROL Image Description]**&#x200B;の場合、`5-Star Rating`と入力し、**[!UICONTROL OK]**&#x200B;をクリックして画像を列に挿入します。

   - エディターツールバーで、**中央揃え** （![中央揃えボタン &#x200B;](./assets/editor-btn-align-center.png)）をクリックして、列の中央に画像を配置します。

     ![中央の評価画像](./assets/pb-tutorial1-column2-5stars-centered.png){width="600" zoomable="yes"}

1. 5つ星の画像のすぐ後に挿入ポイントを置き、Enter/Return キーを押して新しい行を開始し、次のテキストを入力します。

   `Awesome Tank!`

   `I'm a long distance runner and it keeps me pretty comfortable, although these companies always act like their shirts are magical and really it's just pretty basic stuff. Still it's a great shirt, and I would recommend it.`

   `Antonia Racer Tank – Reviewed by Allyson`

   テキストは入力中に中央に配置されます。

   ![列の中央にあるテキストを確認](./assets/pb-tutorial1-column2-text-unformatted.png){width="600" zoomable="yes"}

1. テキストの書式設定：

   - テキストの最初の行の任意の場所をクリックし、**形式**&#x200B;の下のエディターツールバーで、`Heading 2`を選択します。

   - 残りのテキストを選択し、**形式**&#x200B;の下のエディターツールバーで、`Paragraph`を選択します。

   テキストは、テーマに関連付けられているスタイルシートに従って書式設定されます。

1. 画像のサイズを取得して、コンテンツを列の垂直方向に中央に配置できるようにします。

   - 最初の列の画像にカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   - 画像のサムネールの下に、画像の寸法をメモします。

     ![&#x200B; サムネールの下に表示される画像ディメンション &#x200B;](./assets/pb-tutorial1-column1-image-dimensions.png){width="600" zoomable="yes"}

   - 右上隅で、**閉じる**&#x200B;をクリックします。

1. コンテンツを2列目で垂直方向に中央に配置します。

   - 2番目の列にカーソルを合わせてツールボックスを表示し、_設定_ （![設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   >[!NOTE]
   >
   >正しいツールボックスを表示するには、テキストコンテナではなく列コンテナを選択してください。

   - **[!UICONTROL Minimum Height]**&#x200B;に対して、最初の列の画像の高さをピクセル単位で`450`と入力します。

   - **[!UICONTROL Vertical Alignment]**&#x200B;を`Center`に設定します。

   ![最小の高さと垂直方向の整列の設定](./assets/pb-tutorial1-column2-layout-vertical-alignment.png){width="600" zoomable="yes"}

1. _[!UICONTROL Advanced]_&#x200B;セクションまでスクロールして、すべての&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;値を0に設定します（`0`）。

   ![余白とパディングの設定](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. ページの上部までスクロールし、右上隅の&#x200B;**[!UICONTROL Save]**&#x200B;をクリックして設定を保存し、[!DNL Page Builder] ワークスペースに戻ります。

   ![&#x200B; レビューコンテンツをステージに配置した行](./assets/pb-tutorial1-row-reviw-content.png){width="600" zoomable="yes"}

### 手順5：カタログ製品リンクの挿入

1. `Antonia Racer Tank` テキストを選択し、エディターツールバーの&#x200B;_リンクを挿入_ （![&#x200B; リンクを挿入アイコン &#x200B;](./assets/editor-btn-insert-edit-link.png)）アイコンをクリックします。

1. _リンクを挿入_ ダイアログで、カタログ製品へのリンクを指定します。

   - 製品&#x200B;**[!UICONTROL URL]**&#x200B;を入力します。

     相対URLまたは完全修飾URLを入力できます。 この例では、次の相対リンクが入力されます。

     `../antonia-racer-tank.html`

   - （オプション）「**タイトル**」に、製品名を入力します。

     タイトルリンク属性は、一部のブラウザーでツールチップとして使用されます。

     ![&#x200B; テキストにリンクを挿入](./assets/pb-tutorial1-text-link-insert.png){width="600" zoomable="yes"}

   - 完了したら、**[!UICONTROL OK]**&#x200B;をクリックしてリンクを保存します。

     リンクされたテキストがバナーでハイライト表示されるようになりました。

     ![&#x200B; リンクされたテキストを含むバナー](./assets/pb-tutorial1-text-link-highlight.png){width="600" zoomable="yes"}

1. ステージの右上隅で、_フルスクリーンを閉じる_ （![&#x200B; フルスクリーンアイコンを閉じる](./assets/pb-icon-reduce.png)）アイコンをクリックします。

   このアイコンをクリックすると、プレビューが表示されたページの&#x200B;_[!UICONTROL Content]_&#x200B;セクションに戻ります。

1. 右上隅の「**[!UICONTROL Save]**」をクリックします。

### 手順6：行の並べ替え

3つの行がすべて完了したら、最後の手順は、元の&#x200B;_単純ページ_&#x200B;の例に一致するように行を並べ替えることです。 元の例と一致させるには、最初の行を下に移動し、最後の行を上に移動する必要があります。

1. 必要に応じて、**[!UICONTROL Content]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. コンテンツのプレビュー領域の内側にある&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;をクリックします。

1. ステージの最初の行にカーソルを合わせてツールボックスを表示し、_移動_ （![移動アイコン &#x200B;](./assets/pb-icon-move.png)）アイコンを選択します。

   ![移動](./assets/pb-tutorial1-row-toolbox-move.png){width="600" zoomable="yes"}

1. 行のすべてのコンテンツが選択されていることを確認するには、マウスボタンを押しながら、ページの下部にある赤いガイドラインの下の位置に行をドラッグします。

   >[!NOTE]
   >
   >画像などのコンテンツの一部だけを誤って移動した場合は、コンテンツを属する場所に戻して、もう一度試します。

   ![&#x200B; ステージ上の行を移動する](./assets/pb-tutorial1-row-toolbox-move-to-position.png){width="600" zoomable="yes"}

1. このプロセスを繰り返して、最初の行を2番目の位置に移動します。

   ページ上の行の順序が、シンプルなページの例と一致するようになりました。

1. ステージの右上隅で、_フルスクリーンを閉じる_ （![&#x200B; フルスクリーンアイコンを閉じる](./assets/pb-icon-reduce.png)）アイコンをクリックします。

   このアイコンをクリックすると、プレビューが表示されたページの&#x200B;_[!UICONTROL Content]_&#x200B;セクションに戻ります。

1. 右上隅の&#x200B;**[!UICONTROL Save]**&#x200B;矢印をクリックし、**[!UICONTROL Save & Close]**&#x200B;を選択します。

1. プロンプトが表示されたら、ページ上部のメッセージの[Cache Management](../systems/cache-management.md) リンクをクリックし、無効なキャッシュを更新します。

簡易ページの演習が完了しました。 後で参照できるように、作成した作業を保存します。

準備ができたら、[&#x200B; パート 2: ブロック &#x200B;](2-blocks.md)に進みます。
