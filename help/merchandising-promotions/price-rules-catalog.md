---
title: カタログ価格ルール
description: 定義済みの条件に基づいて、割引価格で購入者に製品をオファーするために使用できるカタログ価格ルールについて説明します。
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# カタログ価格ルール

カタログ価格ルールを使用して、定義された条件に基づいて、割引価格で製品を購入者にオファーできます。 カタログ価格ルールでは、 [クーポンコード](price-rules-cart-coupon.md)（製品が買い物かごに入れられる前にトリガーされるため）。

例えば、満たされた場合に特別な価格またはプロモーション価格の製品を自動的に表示する価格ルールの条件を定義および設定できます。 定義済みのルールプロパティには、顧客グループ、製品カテゴリ、割引額や割引率、製品の色、製品のサイズ、またはストアで設定されている製品属性のみが含まれる場合があります。 プロモーションを自動的に開始および停止する価格ルールの開始日と終了日を、ルールで定義した日付に設定できます。 保存されたルールのプロパティは、必要に応じて更新または変更できます。

- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 定義したルールを [動的ブロック](../content-design/dynamic-blocks.md) ストアでのイベントや製品のプロモーションに役立ちます。

- ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) 繰り返しプロモーションの場合、保存済みルールを手動でに設定できます。 _アクティブ_ または _非アクティブ_ ステータスを設定します。

## カタログ価格ルールへのアクセス

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![カタログ価格ルール](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. ルールのプロパティを更新します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) クリック **[!UICONTROL Edit]** 表示する _ルール情報_ ページに貼り付けます。

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) リストでルールをクリックして、ルール情報ページを表示します。

   ルールの設定は、 [ルールの作成](price-rules-catalog-create.md)) をクリックします。

## フィルターオプション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | 特定のルール ID 番号のリストをフィルターするテキストを入力します。 |
| [!UICONTROL Rule] | テキストを入力し、ルールが作成された際に定義されたルール名に基づいてリストをフィルタリングします。 |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) ルールに定義された優先度に基づいてリストをフィルターするには、このフィールドにテキストを入力します。 |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) ルールに定義された Web サイトに基づいてリストをフィルタリングするには、このオプションを使用します。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) クリック **[!UICONTROL Edit]** をクリックして、「ルール情報」を表示し、ルール設定を更新します（ルールの作成と同様）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) 動的カレンダーフィールド（宛先：および差出人：）を使用して、ルールの作成時に定義されたルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) 動的カレンダーフィールド（宛先：および差出人：）を使用して、ルールの作成時に定義されたルールの終了日に基づいてリストをフィルタリングします。 |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) ルールのステータス (`Active` または `Inactive`) をクリックします。 |

{style="table-layout:auto"}

## リソースのトラブルシューティング

カタログ価格ルールの問題のトラブルシューティングについては、次の Commerce Support Knowledge Base 記事を参照してください。

- [404 カタログ価格ルールスケジュールの更新が実行されると、ストアフロントでエラーが発生します](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [関連製品とターゲットルールを含む製品ページのパフォーマンスが向上しました。](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [カタログ価格ルールが機能しません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [GraphQLの価格計算](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)
