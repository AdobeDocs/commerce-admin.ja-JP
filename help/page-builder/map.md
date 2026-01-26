---
title: メディア – マップ
description: ' [!DNL Google Maps] Platform からステージにマップを追加するために使用される、マップコンテンツタイプについて説明  [!DNL Page Builder]  ます。'
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1572'
ht-degree: 0%

---

# メディア – マップ

_Map_ コンテンツタイプを使用して、[[!DNL Google Maps] Platform](https://cloud.google.com/maps-platform/) から [[!DNL Page Builder] stage](workspace.md#stage) にマップを追加します。 例えば、あるブロックにマップを追加し、そのブロックを [ 会社情報 ](../content-design/pages.md#about-us) ページと [ お問い合わせ ](../getting-started/store-details.md#contact-us-form) ページに追加できます。

[!DNL Google Maps] Platform を最大限に活用するには、マップをカスタマイズし、店舗の場所を強調表示し、Google[Places](https://cloud.google.com/maps-platform/places/) を使用して、店舗に関する豊富な情報をすべての [!DNL Google Maps] ーザーに追加します。

## Google マップを埋め込むメリット

1. サイト上で、ビジネスに関する情報（電話番号、web サイト、レビュー、星評価など）の完全な範囲を購入者に提供します。

1. Googleの地図は通常、近くの観光スポット、公園、レストランなどを強調します。 この情報は、顧客が物理的な場所を特定し、旅行を計画するのに役立ちます。

1. 新しいブラウザーウィンドウを開いてサイトを離れることなく、顧客が物理的な店舗の住所を簡単に見つけられるようにします。

1. 実店舗のチェーンがある場合は、サイトにGoogleマップを追加すると、ハイライトされた商品の形でブランドの認知度と信頼性を高めるのに役立ちます。

![ ストアフロントの例 – 場所を使用したマッピング ](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## マップツールボックス

マップコンテナにポインタを合わせると、マップツールボックスが表示されます。

| ツール | アイコン | 説明 |
|--- |--- |--- |
| 移動 | ![ 移動アイコン ](./assets/pb-icon-move.png){width="25"} | マップをステージ上の別の位置に移動します。 |
| （ラベル） | [!UICONTROL Map] | 現在のコンテンツコンテナをマップとして識別します。 マップコンテナの上にマウスポインターを置くと、ツールボックスが表示されます。 |
| 設定 | ![ 設定アイコン ](./assets/pb-icon-settings.png){width="25"} | マップの編集ページが開き、マップとコンテナのプロパティを変更できます。 |
| Hide | ![ アイコンを非表示 ](./assets/pb-icon-hide.png){width="25"} | 現在のマップを非表示にします。 |
| 表示 | ![ アイコンを表示 ](./assets/pb-icon-show.png){width="25"} | 非表示のマップを表示します。 |
| 複製 | ![ 複製アイコン ](./assets/pb-icon-duplicate.png){width="25"} | マップをコピーします。 |
| 削除 | ![ 削除アイコン ](./assets/pb-icon-remove.png){width="25"} | ステージからマップを削除します。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 管理者の [!DNL Google Maps] の設定

マップを追加する前に、まず [ Platform の無料体験版 ](https://cloud.google.com/maps-platform/user-guide/) アカウント [!DNL Google Maps] を開く必要があります。 無料トライアルは 12 ヶ月間続き、300 ドルのクレジットが含まれています。 クレジットを使い果たした場合、Googleはユーザーの許可なくアカウントに請求することはありません。

### 手順 1:[!DNL Google Maps] API キーの取得

[!DNL Google Maps] キーが既にあるかどうかに応じて、次のいずれかの手順を使用して、設定に必要な API キーを取得します。 [!DNL Google Maps] キーを設定するには、アカウントの請求を有効にする権限を持つサイト管理者である必要があります。 [!DNL Google Maps] Platform アカウントを設定する準備が整っていない場合は、この手順をスキップして、今のところプレースホルダーマップを使用できます。

1. [Google Cloud Platform コンソール ](https://cloud.google.com/console/google/maps-apis/overview) に移動します。

1. 「プロジェクト」ドロップダウンをクリックし、API キーを追加するプロジェクトを選択または作成します。

1. API 資格情報を設定するには、[ のドキュメントの ](https://developers.google.com/maps/documentation/javascript/get-api-key) 手順 [!DNL Google Maps] に従ってください。

1. API キーをクリップボードにコピーします。

### 手順 2:[!DNL Google Maps] で [!DNL Commerce] を設定する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![ 展開セレクター ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** を展開します。

   ![ 高度なコンテンツツール ](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   コンテンツ管理の詳細ツールの設定オプションについて詳しくは、[ 設定リファレンスガイド ](../configuration-reference/general/content-management.md) を参照してください。

1. **[!UICONTROL Google Maps API Key]**：手順 1 でコピーしたキーを貼り付けます。

1. 「**[!UICONTROL Test Key]**」をクリックします。

   キーに問題がある場合は、[!DNL Google Maps] Platform サイトに戻って問題を解決してください。 その後、もう一度試してください。

1. キーが確認されたら、「**[!UICONTROL Save Config]**」をクリックします。

## ステージへのマップの追加

1. [!DNL Page Builder] ワークスペースに対してページ、ブロック、またはダイナミック ブロックを開きます。

1. [!DNL Page Builder] パネルで **[!UICONTROL Media]** を展開し、**[!UICONTROL Map]** プレースホルダーをステージにドラッグします。

   ![ マップをステージにドラッグ ](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   [!DNL Google Maps] Platform がストア用に設定されている場合は、ストアの場所のマップが表示されます。

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   [!DNL Google Maps] Platform がまだストアに設定されていない場合は、代わりにプレースホルダーマップが表示されます。

   ![[!DNL Google Maps] プレースホルダー ](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## カスタムマップの場所の追加

1. マップコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

1. _[!UICONTROL Edit Map]_ページの右上隅にある「**[!UICONTROL Add Location]**」をクリックします。

1. マップ上のピンに関連付ける **[!UICONTROL Location Name]** を入力します。

1. カスタム位置に使用する位置座標を収集します。

   または、**[!UICONTROL Position]** のボックスで、表示されたマップ内のピンをドラッグすることもできます。

   必要に応じて、新しいブラウザーウィンドウで [[!DNL Google Maps]](https://www.google.com/maps) に移動し、次のいずれかの方法を使用して座標を取得します。

   ![ マップ座標 ](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **メソッド 1:** URL からコピー

   - 左上隅の **[!UICONTROL Search]** ボックスにアドレスを入力し、「_検索_」（![ 検索アイコン ](../assets/icon-magnify-search.png){width="20"}）アイコンをクリックします。

   - URL の座標をコピーしてメモ帳に貼り付けます。

   **方法 2:** 「What&#39;s here?」からコピーする。

   - マップ上の位置を示す赤いピンを右クリックし、メニューから [**[!UICONTROL What's here?]**] を選択します。

   - 表示されたラベルで、座標を含むテキストをコピーし、メモ帳に貼り付けます。

1. **[!UICONTROL Coordinates]** の各ボックスに、番号をコンマなしで入力します。

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

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   新しい位置がマップおよび _[!UICONTROL Edit Map]_ページのマップ位置グリッドに表示されます。

   ![[!DNL Page Builder] - マップ位置グリッド ](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## マップのスタイル設定 {#styling}

[!DNL Google Maps] Platform スタイルウィザードを使用すると、6 つの定義済みテーマのいずれかを適用したり、カスタムテーマを作成したりできます。 マップスタイルプロパティまたはスタイル設定されたマップへのリンクを含む JSON ファイルを生成できます。

### マップ スタイルを変更する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![ 展開セレクター ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** を展開します。

1. [**[!UICONTROL Google Maps Style]**] テキスト ボックスで、[ マップ スタイルを作成 ](https://mapstyle.withgoogle.com/) をクリックします。

   このアクションにより、別のタブで [[!DNL Google Maps] Platform スタイル設定ウィザード ](https://mapstyle.withgoogle.com/) が開き、[!DNL Google Maps] Platform プロジェクトのスタイルを定義できます。

1. **[!UICONTROL Create a Style]** をクリックし、表示される指示に従います。

   完了したら、「**[!UICONTROL Finish]**」をクリックします。

1. 完成したスタイルを JSON コードまたは URL として書き出すと、[!DNL Commerce] 設定に追加できます。

   - **JSON**：生成された JSON コードが表示されたボックスの下で、「**[!UICONTROL Copy JSON]**」をクリックします。

   - **[!UICONTROL URL]**：生成された URL を含むボックスの下で、「**[!UICONTROL Copy URL]**」をクリックします。

1. 管理者のブラウザータブに戻り、生成したコードまたは URL を **Google マップのスタイル** ボックスに貼り付けます。

   URL を使用している場合は、`YOUR_API_KEY` プレースホルダーを [!DNL Google Maps] API キーに置き換えます。 この URL は、スタイル設定されたGoogle マップにリンクしています。

1. 右上隅の「**[!UICONTROL Save Config]**」をクリックします。

### マップ設定の変更

1. マップコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![ 設定アイコン ](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

1. 必要に応じて基本設定を変更します。

   | オプション | 説明 |
   | ------ | ----------- |
   | [!UICONTROL Height] | 表示されるマップの高さをピクセル単位で指定します。 |
   | [!UICONTROL Show Controls] | 標準のGoogleマップコントロールを表示するかどうかを指定します。 |

   {style="table-layout:auto"}

1. 必要に応じて、_[!UICONTROL Advanced]_の設定を変更します。

   - コンテナに追加されるマップコンテンツの水平方向の位置を制御するには、**[!UICONTROL Alignment]** のいずれかを選択します。

     | オプション | 説明 |
     | ------ | ----------- |
     | `Default` | 現在のテーマのスタイル シートで指定されている線形の既定の設定を適用します。 |
     | `Left` | 指定したパディングの許容値を使用して、マップコンテナの左境界線に沿ってコンテンツを配置します。 |
     | `Center` | 指定したパディングに対する許容値を使用して、コンテンツをマップ コンテナの中央に位置合わせします。 |
     | `Right` | 指定したパディングの許容値を使用して、マップコンテナの右端に沿ってコンテンツを配置します。 |

     {style="table-layout:auto"}

   - マップ コンテナの 4 つの側面すべてに適用される **[!UICONTROL Border]** スタイルを設定します。

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

   - `None` 以外の境界線のスタイルを設定する場合は、境界線の表示オプションを完了します。

     ![ 境界線のカラー ](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | オプション | 説明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 見本を選択するか、カラーピッカーをクリックするか、有効なカラー名または同等の 16 進数値を入力して、カラーを指定します。 |
     | [!UICONTROL Border Width] | 境界線の幅のピクセル数を入力します。 |
     | [!UICONTROL Border Radius] | ピクセル数を入力して、境界線の各コーナーを丸めるために使用する半径のサイズを定義します。 |

     {style="table-layout:auto"}

   - （オプション）マップコンテナに適用する現在のスタイルシートの **[!UICONTROL CSS classes]** の名前を指定します。

     複数のクラス名はスペースで区切ります。

   - マップ コンテナの外側の余白と内側のパディングを指定する **[!UICONTROL Margins and Padding]** の値をピクセル単位で入力します。

     対応する各値をマップのコンテナ図に入力します。

     | コンテナ領域 | 説明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | コンテナのすべての側面の外側の端に適用される空白スペースの量。 |
     | [!UICONTROL Padding] | コンテナのすべての側面の内側の端に適用される空白のスペースの量です。 |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >マップコンテンツタイプには、パディングを使用できません。

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を適用し、[!DNL Page Builder] ワークスペースに戻ります。

### グリッドのサイズの変更

グリッドサイズは、[ のステージの ](column.md) 列 [!DNL Page Builder] に関連するマップのサイズを決定します。 デフォルトでは、マップの幅は 12 列、最大 16 列です。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![ 展開セレクター ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** を展開します。

1. 必要に応じて、グリッドオプションを更新します。

   >[!NOTE]
   >
   >必要に応じて、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、これらの設定を変更します。

   - **[!UICONTROL Default Column Grid Size]** の場合、グリッドの既定のサイズとして新しい値を入力します。

   - **[!UICONTROL Maximum Column Grid Size]** の場合は、デフォルトの最大グリッドサイズに新しい値を入力します。

   ![ 柱通芯のサイズ設定 ](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
