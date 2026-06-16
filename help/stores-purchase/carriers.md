---
title: 配送業者の設定
description: ストアで利用可能な商用送料アカウントのサポートについて説明します。
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/zKN3BQWHywAOLJ-zaJX1-8b7aAYxtzl8v9J7uJG1rFg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 496
ht-degree: 0%

---

# 配送業者の設定

サポート対象の通信事業者の法人顧客アカウントをお持ちの場合は、チェックアウト時に通信事業者を選択できる利便性をお客様に提供できます。 料金は自動的にダウンロードされるので、情報を調べる必要はありません。

>[!NOTE]
>
>Commerceのインストールに関するその他の配送サービスについては、[Commerce Marketplace](../getting-started/commerce-marketplace.md)を参照してください。

顧客に選択した配送業者を提供する前に、次の手順を完了する必要があります。

- [配送設定](shipping-settings.md)を設定して、ストアの原点を確立します。

- 提供する各キャリアサービスの設定を行います。

   - [**UPS**](ups.md) - United Parcel Service （UPS）は、220以上の国に対して、陸路と空路による国内および国際配送サービスを提供しています。
   - [**USPS**](usps.md) - United States Postal Service （USPS）は、米国政府の独立系郵便局です。 USPSは、陸路と空路による国内外配送サービスを提供しています。
   - [**FedEx**](fedex.md) - FedExは、220以上の国に対して、陸路および空路による国内および国際配送サービスを提供しています。
   - [**DHL**](dhl.md) - DHLは、統合された国際サービスと、レター、商品、情報を管理および輸送するためのカスタマイズされた顧客中心のソリューションを提供しています。

## ディメンションの重み付け

寸法重量は、体積の重量と呼ばれることもあり、重量とパッケージ量の組み合わせに輸送価格を基にした一般的な業界慣行です。 簡単に言えば、寸法の重量は、荷物が運送エリアで占めるスペースの量に基づいて配送料を決定します。 寸法の重さは、通常、パッケージがボリュームに比べて比較的軽い場合に使用されます。

すべての主要な運送業者は、一部の出荷に寸法重量を適用します。 ただし、ディメンションの重み付けの適用方法は、キャリアごとに異なります。 出荷量が多い場合、わずかな配送価格の違いでも、1年間で数千ドルに達する可能性があります。

## 設定

設定オプションはキャリアごとに異なります。 ただし、次の手順を実行する必要があります。

1. 配送業者で送料アカウントを開きます。

1. アカウント番号またはユーザーIDを入力し、システムへのゲートウェイ URLをストアの設定に入力します。

### USPS Web Tools APIの非推奨化

Adobe Commerce バージョン 2.4.6、2.4.7、および2.4.8では、従来のWeb ツール APIを使用して、USPSとの出荷時の統合が可能です。 USPSは、従来のWeb ツール APIに代わるREST ベースのプラットフォームであるUSPS APIを導入しました。

2026年1月25日をもって、USPSは従来のWeb ツール APIを廃止しました。 この日付以降、Web ツール APIへのすべてのリクエストは失敗します。

USPSの配送サービスの中断を避けるには、最新バージョンのAdobe Commerceにアップグレードするか、次の操作を行います。

- [USPS REST API移行品質パッチ &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210)を適用して、USPS REST APIとの統合のサポートを追加します。

- REST APIを使用するようにCommerce USPS設定を更新します。

   - [USPS配送業者の設定](usps.md)

   - [配送ラベルの設定](shipping-label-create.md)

