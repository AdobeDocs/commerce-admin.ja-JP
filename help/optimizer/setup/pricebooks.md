---
title: プライスブック
description: 価格表を[!DNL Adobe Commerce]のカタログと価格データからマッピングする方法を説明します。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaSのみ" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="CCDMのみでプロビジョニングされたAdobe Commerce as a Cloud Service インスタンス（Adobeで管理されるSaaS インフラストラクチャ）に適用されます。"
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 1041abe0e7d7c1212a717d5fd03180ce7fd32958
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%
---
# プライスブック

価格表：顧客層と市場をまたいで、カタログソースの製品価格を定義します。 彼らは親と子の価格表の階層をサポートしています。

![価格表の階層](../assets/price-book-hier.png)

## 主要な概念

| 条件 | 説明 |
| ------ | ------------- |
| **価格表** | カタログソースの価格を定義する論理グループ（特定の地域や顧客層など）。製品価格の管理に使用されます。 |
| **フォールバック価格表** | 階層の最上位の価格表。 親は持たず、*のみ*&#x200B;の価格表で、それ自体とそのすべての子孫の価格表の通貨を定義します。<br/><br/>価格表の作成中に（APIを介して）親が定義されていない場合、新しいフォールバック価格表が作成されます。 |
| **親価格表** | 子で明示的に設定されていない場合に、子の価格表が価格を継承できる、より上位レベルの価格表。 |
| **階層の深さ** | 最大3つのレベル（フォールバック/子/孫） <br/><br/>取り込み時に適用されません。 |
| **通貨** | フォールバック価格表にのみ定義されます。 すべての児童価格本に継承されます。<br/><br/> フォールバック価格表の作成中に（APIを介して）通貨が指定されていない場合、通貨はデフォルトでUSDになります。 |
| **製品価格** | 特定の価格表の中の製品（SKU）に割り当てられた特定の価格。 |
| **割引** | 割引は商品価格で定義されています。 継承しない。 |

## 価格表の導入

コンポーザブルカタログデータモデル（CCDM）でAdobe Commerce as a Cloud Serviceを使用する場合、価格表はカタログと価格データからマッピングされます。 手動で作成されたものではありません。

マッピングの概要は次のとおりです。

- **カタログソース→ストアビュー** – ローカライズされた属性を含むストアビューの製品データは、カタログソースにマッピングされます。
- **Web サイト→価格表または価格表** - Web サイトの価格表は、該当する価格表または価格表にマップされます。
- **顧客グループの価格→価格表エントリ** – 顧客グループの価格は、関連する価格エントリにマップされます。

Adobe Commerce設定でソースカタログ、web サイト、価格設定を管理し、利用可能な価格表を設定して、関連するカタログビューでマップされた価格表を割り当てます。 価格表が割り当てられていない場合、カタログ ビューではデフォルトの価格表が使用されます。

カタログビューでは、利用可能な価格台帳の設定とカタログデータおよびポリシーを使用して、商品の返品価格を含むマーチャンダイジング体験を決定します。

>[!NOTE]
>
>Commerce B2Bでは、共通カタログ設定に基づいて、各カタログビューに1つの価格表が作成され、割り当てられます。 これらのビューに対して価格表の可用性を設定する必要はありません。

## チェックアウトの価格

価格表は、マーチャンダイジングとストアフロントのカタログ体験をサポートします。 Commerce Coreは、引き続きカートとチェックアウトを処理します。 CCDMでのみ利用可能な価格が、自動的にチェックアウトで使用される価格になるわけではありません。

Commerceのコア設定と価格に一貫性を持たせ、実装検証の一環として、表示価格、カートへの追加、プロモーション、チェックアウトをテストします。

## 価格表の表示

カタログデータの同期が完了したら、**[!UICONTROL Catalog views]** ワークスペースで利用可能な価格表とそのIDを表示します。

1. _ストア設定_&#x200B;に移動し、**[!UICONTROL Catalog views]**&#x200B;をクリックします。

1. **[!UICONTROL Create catalog view]**&#x200B;をクリックします。

1. カタログビュー設定の&#x200B;**[!UICONTROL Price Books]** セクションで、利用可能な価格表を確認します。

   ![価格書名とID](../assets/price-book-name-ids.png)

## 価格表の可用性の設定

Commerce管理のカタログビューワークスペースで使用可能な価格表を設定することで、マッピングされた価格表をカタログビューに関連付けることができます。

>[!NOTE]
>
>プライベートカタログビュー（[!UICONTROL Catalog Protection]が有効なビュー）は、1つの価格表のみを参照できます。

1. **[!UICONTROL Catalog views]** ワークスペースから、設定するカタログ ビューを選択します。

1. 「**[!UICONTROL Price Books]**」セクションで、カタログビューで裏付けられたストアで利用可能な価格表を選択します。
