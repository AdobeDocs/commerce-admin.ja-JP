---
title: 加盟店のソーシングタイプ
description: シングルソースとマルチソースの加盟店モードを比較して、[!DNL Inventory Management]でソース、在庫、数量を割り当てる方法を選択します。
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/-ABDMLnAibksuQGkdEM683g8JwcUSt2DQERC0WJnQiM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
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
source-wordcount: '487'
ht-degree: 0%
---
# 加盟店のソーシングタイプ

[!DNL Commerce]は、単一のweb サイトを持つ単一のストアから、web サイト、店舗、倉庫、ドロップシッパーの国際的なネットワークに至るまで、あらゆる規模のビジネスに対して[!DNL Inventory Management]をサポートしています。 Adobe CommerceやMagento Open Sourceを利用しているあらゆるマーチャントは、ビジネス内のロケーション数やソース数にもとづいて2種類に分類されます。

- シングルソースマーチャントは、ひとつの地域から商品を出荷します。 インストールにカスタムソースとストックを追加するまで、シングルソースマーチャント/モードとみなされます。

- マルチソースのマーチャントは、実店舗、倉庫、ドロップシッパー、流通センターなど、複数の場所から商品を出荷します。 場所ごとにカスタムソースを追加すると、自動的にマルチソースマーチャントになります。

## シングルソースマーチャント

シングルソースマーチャントは、手元にある在庫を管理し、注文を処理する単一の場所を持っています。 通常、同じカタログ、在庫、場所から商品を販売する複数のweb サイト（または販売チャネル）があります。

たとえば、米国、ドイツ、フランス、ブラジルのサイトを単一のweb サイトまたはマルチサイトで実装しており、そのすべてが1つの大規模な倉庫から製品を取得しています。 この単一の情報源は、注文を受け取る販売チャネルに関係なく、すべての在庫量、出荷、返品を管理します。

最初のステップは以下のとおりです。

- 必要に応じて、ストアのインベントリの[ グローバル設定と商品設定](configuration.md)を構成します。

- 1つの在庫場所に関する情報を含む[ デフォルトのSource](sources-manage.md)を更新します。 追加のソースを作成する必要はありません。

- [ デフォルトのStock](stocks-manage.md)を更新します。 すべてのweb サイトがセールスチャネルとして選択されていることを確認します。 新しいWeb サイトを追加すると、[!DNL Commerce]は自動的に既定のStockに追加します。 追加のストックを作成する必要はありません。

>[!NOTE]
>
>ビジネスの拡大に伴い、ソースと在庫を追加し、[!DNL Inventory Management]設定を更新して、マルチソースマーチャントになります。 すべての詳細については、[ インベントリの展開と再構築](expand-restructure.md)を参照してください。

## マルチソースマーチャント

マルチソースのマーチャントは、ひとつのweb サイトまたは複数のサイトを展開し、複数の場所をまたいで手元の在庫やフルフィルメントを管理しています。

たとえば、米国、ドイツ、フランス、ブラジルのweb サイトを複数サイトに実装している場合などです。 ビジネスでは、これらの国に複数の倉庫や店舗があり、すべての在庫在庫を管理し、注文を処理するドロップシッパーサービスが利用できます。 これらの場所とweb サイトは、[!DNL Commerce]のソースとストックになります。 お客様は、南北アメリカ向けの在庫とヨーロッパ向けの在庫を作成し、ロケールと場所に基づいてweb サイトとソースを割り当てることができます。 各web サイトを購入する顧客は、割り当てられたソースの販売可能な在庫にしかアクセスできません。

最初のステップは以下のとおりです。

- 必要に応じて、ストアのインベントリのグローバル設定を行います。

- 倉庫、店舗、配送センター、ドロップシッパーなど、在庫場所に[ カスタムソース ](sources-add.md)を追加します。

- 複数のソースを使用してweb サイトをマッピングするには、各地域に[ カスタム ストック ](stocks-add.md)を追加します。 注文を処理する際に役立つ、各在庫のソースを場所の優先度で並べ替えます。

- 商品にソースを割り当て、場所ごとに数量を追加します。

- 数量しきい値や取り寄せ注文など、製品ごとに追加の設定を行います。
