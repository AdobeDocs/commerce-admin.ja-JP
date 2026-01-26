---
title: 距離優先アルゴリズムの設定
description: 出荷先所在地の事業所をソース事業所と比較して、出荷を履行する最も近いソースを決定するための構成を設定します。
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# 距離優先アルゴリズムの設定

距離優先アルゴリズムでは、出荷先所在地の事業所がソース事業所と比較され、出荷を履行する最も近いソースが決定されます。 距離は、データベースデータを用いてある場所から別の場所へ移動したり、車を運転したり、歩いたり、自転車で移動したりするのに費やした物理的な距離または時間によって決定される。 この [Source選択アルゴリズムを使用すると ](selection-reservations.md) 出荷先アドレスに最も近い出荷元をお勧めします。

>[!NOTE]
>
>[ 距離優先アルゴリズム ] を使用している場合は、[ ソース ](sources-add.md) の完全な住所と GPS 座標を入力することをお勧めします。

出荷履行の最も近いソースを検索するための距離と時間を計算するには、次の 2 つの方法があります。

- **Googleの地図** - [Googleの地図 Platform](https://cloud.google.com/maps-platform/) サービスを使用して、発送先住所と発送元住所の間の距離と時間を計算します。 このオプションは、ソースの緯度と経度（GPS 座標）を使用し、計算モードに応じて住所を使用する場合があります。 [Geocoding API](https://developers.google.com/maps/documentation/geocoding/start) および [Distance Matrix API](https://developers.google.com/maps/documentation/distance-matrix/start) を有効にしている場合、Google API キーが必要であり、Googleを通じて料金が発生する場合があります。

- **オフライン計算** - ダウンロードおよび読み込んだジオコードデータ（郵便番号および GPS 座標を使用）を使用して距離を計算し、発送先住所に最も近いソースを決定します。 このオプションを設定するには、開発者の支援が必要な場合があり、コマンドラインの手順を使用して最初にジオコードをダウンロードして読み込みます。

>[!NOTE]
>
>複数の国を含むマルチストア web サイトの場合は、国ごとに [ デフォルトの納税先 ](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} を設定します。

## Google マップの使用

開始するためにGoogle アカウントは必要ありません。 このプロセスには、Google アカウントと、必要に応じたプロジェクトの作成が含まれます。 このオプションでは、設定を行ってアルゴリズムを使用するために、Google アカウントに追加された請求アカウントおよびお支払い方法が必要です。
ただし、オフライン計算よりも高度で正確なGoogleの MAP 距離ベースのアルゴリズムをお勧めします。

### 手順 1:Google API キーの作成

キーは [Google地図プラットフォームからのもので ](https://cloud.google.com/maps-platform/)[Geocoding API](https://developers.google.com/maps/documentation/geocoding/start) および [Distance Matrix API](https://developers.google.com/maps/documentation/distance-matrix/start) が有効になっている必要があります。 詳しくは、「距離優先アルゴリズムの設定 [ を参照してください ](distance-priority-algorithm.md)。

1. [Google Maps Platform にアクセスし ](https://cloud.google.com/maps-platform/) 「**[!UICONTROL Get Started]**」をクリックします。

1. プラットフォームを有効にするには、「**[!UICONTROL Maps, Routes, and Places]**」を選択し、「**[!UICONTROL Continue]**」をクリックします。

   ![Googleがキーの Platform をマップする ](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Google アカウントを使用してログインするか、アカウントを作成します。

1. プロジェクトを設定します。

   - プロジェクトを選択するか、新しいプロジェクト名を入力します。

   - 条件に同意するには、「`Yes`」を選択します。

   - 「**[!UICONTROL Next]**」をクリックします。

1. 請求アカウントを入力するか、作成します。 請求アカウントは後でスキップして追加できます。

   このサービスを利用するには、課金アカウントが必要です。

1. Google Cloud Platform オプションを開いて設定するには、「**[!UICONTROL Console]**」をクリックします。

   - プロジェクトを開きます。

   - メニューを展開し、**[!UICONTROL APIs & Services]**/**[!UICONTROL Library]** をクリックします。

     ![Google API サービス ](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - [Geocoding API](https://developers.google.com/maps/documentation/geocoding/start) と [Distance Matrix API](https://developers.google.com/maps/documentation/distance-matrix/start) を検索します。 各サービスを選択して有効にします。

1. メニューを展開し、**[!UICONTROL APIs & Services]**/**[!UICONTROL Credentials]** をクリックして、Google API キーをコピーします。

   ![Google API キーのコピー ](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### 手順 2:Google MAP プロバイダーの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、「**[!UICONTROL Inventory]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png) 「_[!UICONTROL Distance Provider for Distance Based SSA]_」セクションを展開し、「**[!UICONTROL Provider]**」を「`Google MAP`」に設定します。

   ![ 距離ベース SSA のプロバイダ ](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. ![ のセクションの ](../assets/icon-display-expand.png) 展開セレクター _[!UICONTROL Google Distance Provider]_を展開し、設定を指定します。

   - **[!UICONTROL Google API Key]**: Google アカウントからコピーしたキーを入力します。

   - **[!UICONTROL Computation mode]**：設定を選択します。

     >[!NOTE]
     >
     >配送にこのアルゴリズムを使用する際に、配送に対して選択された計算モード（運転、自転車、または歩行）でルートとデータが返されない場合、SSA はデフォルトでSource プライオリティを使用します。 [ 在庫あたりのソースの優先度 ](stocks-prioritize-sources.md) を設定することをお勧めします。

     | オプション | 説明 |
     | ----- | ----- |
     | `Driving` | （既定）道路ネットワークを使用して標準運転方向を要求します。 |
     | `Walking` | 歩行者用道路および歩道（利用可能な場合）を使用して歩行方向を要求します。 |
     | `Bicycling` | 自転車道および優先する道路（利用可能な場合）を使用して自転車道をリクエストします。 [Distance Matrix Service](https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes) は、米国および一部のカナダの都市でのみ利用できます。 |

   - **[!UICONTROL Value]** の場合、値タイプを選択します。

     | オプション | 説明 |
     | ----- | ----- |
     | `Distance` | （既定値）ポイント間の距離をメトリック（キロメートルとメートル）またはインペリアル（マイルとフィート）で返します。 |
     | `Time to Destination` | 発送元の場所から配送先住所への移動に必要な時間を時間と分単位で返します。 |

   ![Google ディスタンス プロバイダー ](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## オフライン計算を使用

オフライン計算では、国コードを使用して、発送先と発送元アドレスの間の距離を決定します。 このオプションを設定するには、開発者の支援が必要になる場合があります。 [!DNL Inventory Management] CLI コマンドを使用して、[geonames.org](https://www.geonames.org/) からデータをダウンロードして読み込みます。

>[!NOTE]
>
>[geonames.org](https://www.geonames.org/) から読み込まれたジオコードには、カナダやアイルランドなど、一部の国に対する制限があります。 詳しくは、[GeoNames 郵便番号ファイル ](https://download.geonames.org/export/zip/readme.txt) を参照してください。

### 手順 1：ジオコードのダウンロードと読み込み

完全なコマンドライン設定を使用して、出荷先のジオコード国をダウンロードおよび読み込み、ソース場所を含めることができます。 この手順では、コマンドラインタスクに関する開発者向け支援が必要になる場合があります。 [ ジオコードの読み込み ](cli.md#import-geocodes) を参照してください。

さらにジオコードを追加する場合は、常にこれらのコマンドを実行します。

### 手順 2：計算を設定する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、「**[!UICONTROL Inventory]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「_[!UICONTROL Distance Provider for Distance Based SSA]_」セクションを展開します。

1. 「**[!UICONTROL Use system value]**」チェックボックスの選択を解除し、「**[!UICONTROL Provider]**」を「`Offline Calculation`」に設定します。

   ![ 距離ベース SSA の距離プロバイダ ](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
