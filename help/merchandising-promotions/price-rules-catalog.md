---
title: カタログ価格ルール
description: 定義された条件に基づいて、製品を購入者に割引価格で提供するために使用できるカタログ価格ルールについて説明します。
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/JZE2DF0tp-XOsKjxo-WaQiwA3Y-FrM4TI5qq-Nze-qo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 468
ht-degree: 0%

---

# カタログ価格ルール

カタログの価格設定ルールを使用して、定義された条件に基づいて、購入者に商品を割引価格で提供できます。 カタログ価格ルールでは、[ クーポンコード ](price-rules-cart-coupon.md)は使用されません。これは、商品をショッピングカートに入れる前にトリガーされるためです。

例えば、価格ルールの条件を定義して設定し、条件が満たされると、特別な価格やプロモーション価格の商品が自動的に表示されます。 定義されたルールプロパティには、顧客グループ、製品カテゴリ、割引額または割合、製品の色、製品サイズ、またはストアで設定されたほぼすべての製品属性が含まれます。 ルールで定義した日付に自動的にプロモーションを開始および停止する価格ルールの開始日と終了日を設定できます。 保存されたルールのプロパティは、必要に応じて更新または変更できます。

- ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）定義済みのルールを[動的ブロック ](../content-design/dynamic-blocks.md)にリンクして、ストアでイベントや商品を宣伝することもできます。

- ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）定期的なプロモーションの場合、プロモーションを実行するたびに、保存されたルールを手動で&#x200B;_アクティブ_&#x200B;または&#x200B;_非アクティブ_ ステータスに設定できます。

## カタログ価格ルールへのアクセス

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**に移動します。

   ![ カタログ価格ルール ](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. ルールのプロパティを更新：

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）「**[!UICONTROL Edit]**」をクリックして、_ルール情報_ ページを表示します。

   - ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）リスト内のルールをクリックすると、ルール情報ページが表示されます。

   ここで、ルールの設定を変更できます（[ ルールの作成](price-rules-catalog-create.md)と同様）。

## フィルターオプション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | テキストを入力して、特定のルール ID番号のリストをフィルタリングします。 |
| [!UICONTROL Rule] | ルールの作成時に定義したルール名に基づいてリストをフィルタリングするテキストを入力します。 |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）このフィールドにテキストを入力して、ルールに定義された優先度に基づいてリストをフィルタリングします。 |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）このオプションを使用すると、ルールに対して定義されたweb サイトに基づいてリストをフィルタリングできます。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）「**[!UICONTROL Edit]**」をクリックしてルール情報を表示し、ルール設定を更新します（ルールの作成と同様）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）動的カレンダーフィールド（宛先：および送信元：）を使用して、ルールの作成時に定義されたルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）動的カレンダーフィールド（宛先：および送信元：）を使用して、ルールの作成時に定義されたルールの終了日に基づいてリストをフィルタリングします。 |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）このオプションを使用すると、ルールのステータス （`Active`または`Inactive`）に基づいてリストをフィルタリングできます。 |

{style="table-layout:auto"}
