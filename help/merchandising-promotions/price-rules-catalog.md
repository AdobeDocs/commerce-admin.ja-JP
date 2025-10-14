---
title: カタログ価格ルール
description: 定義された一連の条件に基づいて割引価格で購入者に製品を提供するために使用できるカタログ価格ルールについて説明します。
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# カタログ価格ルール

カタログ価格ルールを使用すると、定義された一連の条件に基づいて、割引価格で購入者に製品を提供できます。 カタログ価格ルールは、商品が買い物かごに入れられる前にトリガーされるので、[&#x200B; クーポンコード &#x200B;](price-rules-cart-coupon.md) を使用しません。

例えば、満たされた場合に特別価格またはプロモーション価格で製品を自動的に表示する価格ルールの条件を定義して設定できます。 定義済みのルールプロパティには、顧客グループ、製品カテゴリ、割引額やパーセンテージ、製品カラー、製品サイズ、ストアで設定されたほぼすべての製品属性が含まれます。 ルールで定義した日付に販促を自動的に開始および停止する価格ルールの開始日と終了日を設定できます。 保存済みルールのプロパティは、必要に応じて更新または変更できます。

- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）定義済みのルールを [&#x200B; 動的ブロック &#x200B;](../content-design/dynamic-blocks.md) にリンクして、ストア内のイベントや商品を宣伝することもできます。

- ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）繰り返し行われる昇格の場合、昇格を実行するたびに、保存済みのルールを手動で _アクティブ_ または _非アクティブ_ ステータスにすることができます。

## カタログ価格ルールへのアクセス

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Promotions]_/**[!UICONTROL Catalog Price Rules]**&#x200B;に移動します。

   ![&#x200B; カタログ価格ルール &#x200B;](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. ルールのプロパティを更新します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）「**[!UICONTROL Edit]**」をクリックすると _ルール情報_ ページが表示されます。

   - ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）一覧内のルールをクリックして、[ ルール情報 ] ページを表示します。

   ここで、（ルールの作成 [&#x200B; と同様に）ルールの設定を変更でき &#x200B;](price-rules-catalog-create.md) す。

## フィルターオプション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | 特定のルール ID 番号のリストをフィルタリングするためのテキストを入力します。 |
| [!UICONTROL Rule] | ルールの作成時に定義したルール名に基づいてリストをフィルタリングするためのテキストを入力します。 |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）ルールに定義されている優先度に基づいてリストをフィルタリングするには、このフィールドにテキストを入力します。 |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）ルールに定義されている web サイトに基づいてリストをフィルタリングします。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）「**[!UICONTROL Edit]**」をクリックすると、ルール情報が表示され、ルール設定が更新されます（ルールの作成と同様です）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）動的カレンダーフィールド （宛先：および送信者：）を使用して、ルールの作成時に定義されたルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）動的カレンダーフィールド （宛先：および送信者：）を使用して、ルールの作成時に定義されたルールの終了日に基づいてリストをフィルタリングします。 |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）ルールのステータス （`Active` または `Inactive`）に基づいてリストをフィルターするには、このオプションを使用します。 |

{style="table-layout:auto"}
