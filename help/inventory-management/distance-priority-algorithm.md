---
title: 距離優先アルゴリズムの設定
description: 出荷先所在地の事業所をソース事業所と比較して、出荷を履行する最も近いソースを決定するための構成を設定します。
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---

# 距離優先アルゴリズムの設定

距離優先アルゴリズムでは、出荷先所在地の事業所がソース事業所と比較され、出荷を履行する最も近いソースが決定されます。 距離は、データベースデータを用いてある場所から別の場所へ移動したり、車を運転したり、歩いたり、自転車で移動したりするのに費やした物理的な距離または時間によって決定される。 これを使用 [ソース選択アルゴリズム](selection-reservations.md) 出荷先アドレスに最も近いソースをレコメンデーションする。

>[!NOTE]
>
>[ 距離優先アルゴリズム ] を使用している場合は、住所と GPS 座標を入力します [ソース](sources-add.md) 推奨されます。

出荷履行の最も近いソースを検索するための距離と時間を計算するには、次の 2 つの方法があります。

- **Googleの地図**  – 使用 [Google マッププラットフォーム][1] 配送先住所と配送元場所の間の距離と時間を計算するサービス。 このオプションは、ソースの緯度と経度（GPS 座標）を使用し、計算モードに応じて住所を使用する場合があります。 にGoogle API キーが必要です [Geocoding API][2] および [Distance Matrix API][3] を有効にすると、Google経由で料金が発生する場合があります。

- **オフライン計算**  – 郵便番号および GPS 座標を使用してダウンロードおよび読み込んだジオコードデータを使用して距離を計算し、出荷先住所に最も近いソースを決定します。 このオプションを設定するには、開発者の支援が必要な場合があり、コマンドラインの手順を使用して最初にジオコードをダウンロードして読み込みます。

>[!NOTE]
>
>複数の国を含むマルチストア web サイトの場合は、 [既定の税宛先](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} （国ごとに）。

## Google マップの使用

開始するためにGoogle アカウントは必要ありません。 このプロセスには、Google アカウントと、必要に応じたプロジェクトの作成が含まれます。 このオプションでは、設定を行ってアルゴリズムを使用するために、Google アカウントに追加された請求アカウントおよびお支払い方法が必要です。
ただし、オフライン計算よりも高度で正確なGoogleの MAP 距離ベースのアルゴリズムをお勧めします。

### 手順 1:Google API キーの作成

キーはです [Google マッププラットフォーム][1] および次を持つ必要があります [Geocoding API][2] および [Distance Matrix API][3] 有効。 詳しくは、を参照してください [距離優先アルゴリズムの設定](distance-priority-algorithm.md).

1. 訪問 [Google マッププラットフォーム][1] をクリックして、 **[!UICONTROL Get Started]**.

1. プラットフォームを有効にするには、次を選択します **[!UICONTROL Maps, Routes, and Places]** をクリックして、 **[!UICONTROL Continue]**.

   ![Googleがキーに対して Platform をマッピングします](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Google アカウントを使用してログインするか、アカウントを作成します。

1. プロジェクトを設定します。

   - プロジェクトを選択するか、新しいプロジェクト名を入力します。

   - 条件に同意するには、を選択します `Yes`.

   - クリック **[!UICONTROL Next]**.

1. 請求アカウントを入力するか、作成します。 請求アカウントは後でスキップして追加できます。

   このサービスを利用するには、課金アカウントが必要です。

1. Google Cloud Platform オプションを開いて設定するには、以下をクリックします。 **[!UICONTROL Console]**.

   - プロジェクトを開きます。

   - メニューを展開し、 **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**.

     ![Google API サービス](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - を検索 [Geocoding API][2] および [Distance Matrix API][3]. 各サービスを選択して有効にします。

1. メニューを展開し、 **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]**&#x200B;を作成し、Google API キーをコピーします。

   ![Google API キーのコピー](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### 手順 2:Google MAP プロバイダーの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Inventory]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Distance Provider for Distance Based SSA]_セクションとセット&#x200B;**[!UICONTROL Provider]**対象： `Google MAP`.

   ![距離ベースの SSA のプロバイダ](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Google Distance Provider]_をクリックして、設定を指定します。

   - の場合 **[!UICONTROL Google API Key]**&#x200B;に、Google アカウントからコピーしたキーを入力します。

   - の場合 **[!UICONTROL Computation mode]**、設定を選択します。

     >[!NOTE]
     >
     >出荷にこのアルゴリズムを使用する際に、出荷に対して選択された計算モード（運転、自転車、または歩行）でルートとデータが返されない場合、SSA はデフォルトでソース プライオリティを使用します。 の設定 [在庫あたりのソースの優先度](stocks-prioritize-sources.md) 推奨されます。

     | オプション | 説明 |
     | ----- | ----- |
     | `Driving` | （既定）道路ネットワークを使用して標準運転方向を要求します。 |
     | `Walking` | 歩行者用道路および歩道（利用可能な場合）を使用して歩行方向を要求します。 |
     | `Bicycling` | 自転車道および優先する道路（利用可能な場合）を使用して自転車道をリクエストします。 この [距離マトリックス サービス][4] は、米国および一部のカナダの都市でのみ利用できます。 |

   - の場合 **[!UICONTROL Value]**&#x200B;値のタイプを選択します。

     | オプション | 説明 |
     | ----- | ----- |
     | `Distance` | （既定値）ポイント間の距離をメトリック（キロメートルとメートル）またはインペリアル（マイルとフィート）で返します。 |
     | `Time to Destination` | 発送元の場所から配送先住所への移動に必要な時間を時間と分単位で返します。 |

   ![Google距離プロバイダー](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

## オフライン計算を使用

オフライン計算では、国コードを使用して、発送先と発送元アドレスの間の距離を決定します。 このオプションを設定するには、開発者の支援が必要になる場合があります。 を使用 [!DNL Inventory Management] データをダウンロードしてインポートする CLI コマンド [geonames.org][5].

>[!NOTE]
>
>からジオコードをインポートしました [geonames.org][5] カナダやアイルランドなど、一部の国には制限があります。 こちらを参照してください [GeoNames 郵便番号ファイル][6] を参照してください。

### 手順 1：ジオコードのダウンロードと読み込み

完全なコマンドライン設定を使用して、出荷先のジオコード国をダウンロードおよび読み込み、ソース場所を含めることができます。 この手順では、コマンドラインタスクに関する開発者向け支援が必要になる場合があります。 こちらを参照してください [ジオコードの読み込み](cli.md#import-geocodes).

さらにジオコードを追加する場合は、常にこれらのコマンドを実行します。

### 手順 2：計算を設定する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Inventory]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Distance Provider for Distance Based SSA]_セクション。

1. の選択を解除 **[!UICONTROL Use system value]** チェックボックスとセット **[!UICONTROL Provider]** 対象： `Offline Calculation`.

   ![距離ベースの SSA の距離プロバイダ](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
[4]: https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes
[5]: https://www.geonames.org/
[6]: https://download.geonames.org/export/zip/readme.txt
