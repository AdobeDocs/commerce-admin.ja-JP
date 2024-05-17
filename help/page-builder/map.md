---
title: メディア – マップ
description: からマップを追加するために使用される、マップ コンテンツタイプについて説明します [!DNL Google Maps] プラットフォームからへ [!DNL Page Builder] ステージ。
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# メディア – マップ

の使用 _マップ_ マップを追加するコンテンツタイプ [[!DNL Google Maps] Platform][1] に [[!DNL Page Builder] ステージ](workspace.md#stage). たとえば、マップをブロックに追加してから、そのブロックをブロックに追加できます [会社情報](../content-design/pages.md#about-us) および [お問い合わせ](../getting-started/store-details.md#contact-us-form) ページ。

を最大限に活用するには [!DNL Google Maps] Platform を使用すると、マップをカスタマイズしたり、店舗の場所を強調表示したり、Googleを使用したりできます [場所][2] ストアに関する豊富な情報をすべてのに追加するには [!DNL Google Maps].

## Google マップを埋め込むメリット

1. サイト上で、ビジネスに関する情報（電話番号、web サイト、レビュー、星評価など）の完全な範囲を購入者に提供します。

1. Googleの地図は通常、近くの観光スポット、公園、レストランなどを強調します。 この情報は、顧客が物理的な場所を特定し、旅行を計画するのに役立ちます。

1. 新しいブラウザーウィンドウを開いてサイトを離れることなく、顧客が物理的な店舗の住所を簡単に見つけられるようにします。

1. 実店舗のチェーンがある場合は、サイトにGoogleマップを追加すると、ハイライトされた商品の形でブランドの認知度と信頼性を高めるのに役立ちます。

![ストアフロントの例 – 場所を使用したマッピング](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## マップツールボックス

マップコンテナにポインタを合わせると、マップツールボックスが表示されます。

| ツール | アイコン | 説明 |
|--- |--- |--- |
| 移動 | ![移動アイコン](./assets/pb-icon-move.png){width="25"} | マップをステージ上の別の位置に移動します。 |
| （ラベル） | [!UICONTROL Map] | 現在のコンテンツコンテナをマップとして識別します。 マップコンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![設定アイコン](./assets/pb-icon-settings.png){width="25"} | マップの編集ページが開き、マップとコンテナのプロパティを変更できます。 |
| Hide | ![アイコンを非表示](./assets/pb-icon-hide.png){width="25"} | 現在のマップを非表示にします。 |
| 表示 | ![アイコンを表示](./assets/pb-icon-show.png){width="25"} | 非表示のマップを表示します。 |
| 複製 | ![アイコンを複製](./assets/pb-icon-duplicate.png){width="25"} | マップをコピーします。 |
| 削除 | ![アイコンを削除](./assets/pb-icon-remove.png){width="25"} | ステージからマップを削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 設定 [!DNL Google Maps] 管理者に問い合わせる

マップを追加する前に、まず [アカウント][3] 無料トライアルのために [!DNL Google Maps] プラットフォーム。 無料トライアルは 12 ヶ月間続き、300 ドルのクレジットが含まれています。 クレジットを使い果たした場合、Googleはユーザーの許可なくアカウントに請求することはありません。

### 手順 1：を入手する [!DNL Google Maps] API キー

既にがあるかどうかに応じて [!DNL Google Maps] キーを入力し、次のいずれかの手順で、設定に必要な API キーを取得します。 を設定するには [!DNL Google Maps] キー、アカウントの請求を有効にする権限を持つサイト管理者である必要があります。 を設定する準備が整っていない場合 [!DNL Google Maps] Platform アカウントの場合は、この手順をスキップして、当面はプレースホルダーマップを使用します。

1. に移動します [Google Cloud Platform コンソール](https://cloud.google.com/console/google/maps-apis/overview).

1. 「プロジェクト」ドロップダウンをクリックし、API キーを追加するプロジェクトを選択または作成します。

1. API 資格情報を設定するには、次に従います。 [指示][4] が含まれる [!DNL Google Maps] ドキュメント。

1. API キーをクリップボードにコピーします。

### 手順 2：設定 [!DNL Google Maps] 。対象： [!DNL Commerce]

1. が含まれる _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Content Management]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![高度なコンテンツツール](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   コンテンツ管理の詳細ツールの設定オプションについて詳しくは、 [設定リファレンスガイド](../configuration-reference/general/content-management.md).

1. の場合 **[!UICONTROL Google Maps API Key]**&#x200B;手順 1 でコピーしたキーをペーストします。

1. クリック **[!UICONTROL Test Key]**.

   キーに問題がある場合は、に戻ります [!DNL Google Maps] 問題を解決する Platform サイト。 その後、もう一度試してください。

1. キーが確認されたら、 **[!UICONTROL Save Config]**.

## ステージへのマップの追加

1. ページ、ブロック、またはダイナミックブロックを開いて、 [!DNL Page Builder] ワークスペース。

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Media]** をドラッグします。 **[!UICONTROL Map]** ステージへのプレースホルダー。

   ![マップをステージにドラッグします](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   次の場合 [!DNL Google Maps] Platform がストア用に設定され、ストアの場所を示すマップが表示されます。

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   次の場合 [!DNL Google Maps] お使いのストアに Platform がまだ設定されていない場合は、代わりにプレースホルダーマップが表示されます。

   ![[!DNL Google Maps] プレースホルダー](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## カスタムマップの場所の追加

1. マップコンテナにポインタを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

1. の右上隅にある _[!UICONTROL Edit Map]_ページ、クリック&#x200B;**[!UICONTROL Add Location]**.

1. を入力 **[!UICONTROL Location Name]** マップ上のピンに関連付けるピン。

1. カスタム位置に使用する位置座標を収集します。

   または、で **[!UICONTROL Position]** ボックスを選択すると、表示されたマップ内のピンをドラッグできます。

   必要に応じて、に移動します [[!DNL Google Maps]][5] 新しいブラウザーウィンドウで、次のいずれかの方法を使用して座標を取得します。

   ![マップ座標](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **メソッド 1:** URL からコピー

   - 左上隅にアドレスを **[!UICONTROL Search]** ボックスをクリックし、 _検索_ （ ![検索アイコン](../assets/icon-magnify-search.png){width="20"} ） アイコンをクリックします。

   - URL の座標をコピーしてメモ帳に貼り付けます。

   **メソッド 2:** 「What&#39;s here?」からコピーします。

   - マップ上の位置を示す赤いピンを右クリックし、 **[!UICONTROL What's here?]** メニューで変更できます。

   - 表示されたラベルで、座標を含むテキストをコピーし、メモ帳に貼り付けます。

1. 各フィールドに数字をコンマなしで入力します **[!UICONTROL Coordinates]** ボックス。

   また、マップ上で使用可能にする残りの情報を入力することもできます。

1. マップの場所に関連付ける他の情報を入力します。

   | オプション | 説明 |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | 所在地の電話番号。 |
   | [!UICONTROL Street Address] | 場所の住所。 |
   | [!UICONTROL City] | 場所の市区町村。 |
   | [!UICONTROL Region/State] | 場所の地域または州。 |
   | [!UICONTROL Zip/Postal Code] | その場所の郵便番号。 |
   | [!UICONTROL Country] | 場所の国。 |
   | [!UICONTROL Comment] | 含めるコメント。 |

   {style="table-layout:auto"}

1. 完了したら、 **[!UICONTROL Save]**.

   新しい位置がマップおよび上のマップ位置グリッドに表示されます _[!UICONTROL Edit Map]_ページ。

   ![[!DNL Page Builder] - マップ位置グリッド](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## マップのスタイル設定 {#styling}

の使用 [!DNL Google Maps] 6 つの定義済みテーマのいずれかを適用したり、カスタムテーマを作成したりするための Platform スタイルウィザード。 マップスタイルプロパティまたはスタイル設定されたマップへのリンクを含む JSON ファイルを生成できます。

### マップ スタイルを変更する

1. が含まれる _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Content Management]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. の下 **[!UICONTROL Google Maps Style]** テキストボックスで、 [マップ スタイルを作成][6].

   このアクションにより、が開きます [[!DNL Google Maps] Platform スタイル設定ウィザード][6] 別のタブで、のスタイルを定義できます [!DNL Google Maps] Platform プロジェクト。

1. クリック **[!UICONTROL Create a Style]** 表示される指示に従います。

   完了したら、 **[!UICONTROL Finish]**.

1. 完成したスタイルを JSON コードまたは URL として書き出すと、に追加できます。 [!DNL Commerce] 設定。

   - **JSON**：生成された JSON コードを含んだボックスの下で、をクリックします **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**：生成された URL を含むボックスの下で、をクリックします **[!UICONTROL Copy URL]**.

1. 管理ブラウザータブに戻り、生成したコードまたは URL をに貼り付けます。 **Google マップ スタイル** ボックス。

   URL を使用している場合は、 `YOUR_API_KEY` プレースホルダー [!DNL Google Maps] API キー。 この URL は、スタイル設定されたGoogle マップにリンクしています。

1. 右上隅のをクリックします。 **[!UICONTROL Save Config]**.

### マップ設定の変更

1. マップコンテナにカーソルを合わせると、ツールボックスが表示されるので、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

1. 必要に応じて基本設定を変更します。

   | オプション | 説明 |
   | ------ | ----------- |
   | [!UICONTROL Height] | 表示されるマップの高さをピクセル単位で指定します。 |
   | [!UICONTROL Show Controls] | 標準のGoogleマップコントロールを表示するかどうかを指定します。 |

   {style="table-layout:auto"}

1. を変更する _[!UICONTROL Advanced]_必要に応じて設定します。

   - コンテナに追加されるマップコンテンツの水平方向の位置を制御するには、 **[!UICONTROL Alignment]**:

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | 指定したパディングの許容値を使用して、マップコンテナの左境界線に沿ってコンテンツを配置します。 |
     | `Center` | 指定したパディングに対する許容値を使用して、コンテンツをマップ コンテナの中央に位置合わせします。 |
     | `Right` | 指定したパディングの許容値を使用して、マップコンテナの右端に沿ってコンテンツを配置します。 |

     {style="table-layout:auto"}

   - を **[!UICONTROL Border]** マップ コンテナの 4 つの側面すべてに適用されるスタイル：

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 関連付けられたスタイル シートで指定されている既定の罫線スタイルを適用します。 |
     | `None` | コンテナの境界線の表示はしません。 |
     | `Dotted` | コンテナの境界線は点線で表示されます。 |
     | `Dashed` | コンテナの境界線は破線で表示されます。 |
     | `Solid` | コンテナの境界線は実線で表示されます。 |
     | `Double` | コンテナの境界線は二重線で表示されます。 |
     | `Groove` | コンテナの境界線は溝付き線で表示されます。 |
     | `Ridge` | コンテナの境界線は、境界線として表示されます。 |
     | `Inset` | コンテナの境界線は、インセットされた線として表示されます。 |
     | `Outset` | コンテナの境界線は、先頭行として表示されます。 |

     {style="table-layout:auto"}

   - 境界線のスタイルを `None`の場合は、次のボーダー表示オプションを入力します。

     ![境界線のカラー](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション）の名前を指定します **[!UICONTROL CSS classes]** を現在のスタイルシートからマップ コンテナに適用します。

     複数のクラス名はスペースで区切ります。

   - 次の値をピクセル単位で入力 **[!UICONTROL Margins and Padding]** マップ コンテナの外側の余白と内側のパディングを指定します。

     対応する各値をマップのコンテナ図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >マップコンテンツタイプには、パディングを使用できません。

1. 完了したら、 **[!UICONTROL Save]** 設定を適用し、 [!DNL Page Builder] ワークスペース。

### グリッドのサイズの変更

グリッド サイズによって、に関連するマップのサイズが決まります。 [列](column.md) 日 [!DNL Page Builder] ステージ。 デフォルトでは、マップの幅は 12 列、最大 16 列です。

1. が含まれる _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Content Management]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. 必要に応じて、グリッドオプションを更新します。

   >[!NOTE]
   >
   >必要に応じて、 **[!UICONTROL Use system value]** チェックボックスをオンにして、これらの設定を変更します。

   - の場合 **[!UICONTROL Default Column Grid Size]**：グリッドのデフォルトサイズの新しい値を入力します。

   - の場合 **[!UICONTROL Maximum Column Grid Size]**：デフォルトの最大グリッドサイズの新しい値を入力します。

   ![列グリッドのサイズ設定](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
