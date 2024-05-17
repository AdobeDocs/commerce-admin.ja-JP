---
title: カタログ価格ルール
description: 定義された一連の条件に基づいて割引価格で購入者に製品を提供するために使用できるカタログ価格ルールについて説明します。
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# カタログ価格ルール

カタログ価格ルールを使用すると、定義された一連の条件に基づいて、割引価格で購入者に製品を提供できます。 カタログ価格ルールは使用しません [クーポンコード](price-rules-cart-coupon.md)これは、商品が買い物かごに入れられる前にトリガーされるためです。

例えば、満たされた場合に特別価格またはプロモーション価格で製品を自動的に表示する価格ルールの条件を定義して設定できます。 定義済みのルールプロパティには、顧客グループ、製品カテゴリ、割引額やパーセンテージ、製品カラー、製品サイズ、ストアで設定されたほぼすべての製品属性が含まれます。 ルールで定義した日付に販促を自動的に開始および停止する価格ルールの開始日と終了日を設定できます。 保存済みルールのプロパティは、必要に応じて更新または変更できます。

- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）定義済みのルールをにリンクすることもできます [動的ブロック](../content-design/dynamic-blocks.md) ストア内のイベントまたは製品のプロモーションに役立ちます。

- ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）定期的なプロモーションの場合、保存済みのルールをに手動で設定できます _アクティブ_ または _Inactive_ プロモーションを実行するたびにステータスを設定します。

## カタログ価格ルールへのアクセス

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![カタログ価格ルール](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. ルールのプロパティを更新します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）クリック **[!UICONTROL Edit]** を表示するには _ルール情報_ ページ。

   - ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）リスト内のルールをクリックして、[Rule Information] ページを表示します。

   ここで、ルールの設定を変更できます（類似： [ルールの作成](price-rules-catalog-create.md)）に設定します。

## フィルターオプション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | 特定のルール ID 番号のリストをフィルタリングするためのテキストを入力します。 |
| [!UICONTROL Rule] | ルールの作成時に定義したルール名に基づいてリストをフィルタリングするためのテキストを入力します。 |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）ルールに定義された優先度に基づいてリストをフィルタリングするには、このフィールドにテキストを入力します。 |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）ルールに定義された web サイトに基づいてリストをフィルタリングします。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）クリック **[!UICONTROL Edit]** ルール情報を表示し、ルール設定を更新します（ルールの作成と同様）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）動的カレンダーフィールド（To：および From:）を使用して、ルールの作成時に定義したルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）動的カレンダーフィールド（宛先：および送信者：）を使用して、ルールの作成時に定義されたルールの終了日に基づいてリストをフィルタリングします。 |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）ルールのステータスに基づいてリストをフィルタリングする場合に使用します（`Active` または `Inactive`）に設定します。 |

{style="table-layout:auto"}

## リソースのトラブルシューティング

カタログ価格ルールに関する問題のトラブルシューティングについて詳しくは、Commerce サポートナレッジベースの次の記事を参照してください。

- [404 カタログ価格ルール スケジュールの更新が実行されると、店舗フロントでエラーが発生します](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [製品ページと関連製品およびターゲットルールのパフォーマンスの向上](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [カタログ価格ルールが機能しない](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [GraphQLの価格計算](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)
