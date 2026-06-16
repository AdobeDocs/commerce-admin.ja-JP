---
title: カテゴリ – デザイン設定
description: '[!UICONTROL Design]設定を使用して、カテゴリ、関連するすべての製品ページ、ページレイアウトの外観を定義する方法について説明します。'
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/cRTRPl-UTfAKXY8rmtVKlnAZooVWpTCjSkVSdNHXp28
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 379
ht-degree: 0%

---

# カテゴリ – デザイン設定

_[!UICONTROL Design]_セクションでは、カテゴリの外観、関連するすべての製品ページ、ページレイアウトを制御できます。 カテゴリ ページとその関連製品をプロモーション用にカスタマイズしたり、カテゴリを区別したりできます。 たとえば、ブランドや特別な商品ラインのために独自のデザインを作成したり、特定の期間のためにアップデートを適用したりすることができます。

![ カテゴリの設定をデザイン ](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>同じ製品が各カテゴリの異なるデザイン設定を持つ複数のカテゴリに割り当てられている場合は、[検索エンジン最適化の設定オプション ](../configuration-reference/catalog/catalog.md#search-engine-optimization)で、**製品URLのカテゴリーパスを使用** = `Yes`を設定することをお勧めします。 この設定にアクセスするには、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動し、**[!UICONTROL Catalog]**を展開して、左側のパネルの下にある&#x200B;**カタログ**を選択し、ページの&#x200B;**検索エンジン最適化**セクションを展開します。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | 現在のカテゴリが親カテゴリからデザイン設定を継承できるようにします。 使用すると、「デザイン」セクションの他のすべてのフィールドが使用できなくなります。 オプション：`Yes` / ` No` |
| [!UICONTROL Theme] | カテゴリにカスタムテーマを適用します。 |
| [!UICONTROL Layout] | カテゴリーページに別のレイアウトを適用します。 オプション：<br/>**[!UICONTROL No layout updates]**- デフォルトでは、カテゴリーページのレイアウト更新は使用できません。<br/>**[!UICONTROL Empty]** – 独自のページレイアウトの定義に使用します。 （XMLについて理解する必要があります） <br/>**[!UICONTROL 1 column]**- 1列のレイアウトをカテゴリーページに適用します。<br/>**[!UICONTROL 2 columns with left bar]** – 左側のサイドバーを含む2列レイアウトをカテゴリーページに適用します。<br/>**[!UICONTROL 2 columns with right bar]**– 右側のサイドバーを持つ2列レイアウトをカテゴリーページに適用します。<br/>**[!UICONTROL 3 columns]** - 3列レイアウトをカテゴリ ページに適用します。<br/>**[!UICONTROL Page -- Full Width]**- （[Page Builder](../page-builder/introduction.md)が必要）CMS ページの全幅レイアウトをカテゴリーページに適用します。<br/>**[!UICONTROL Category -- Full Width]** - （ページビルダーが必要）カテゴリーページの全幅レイアウトをカテゴリーページに適用します。<br/>**[!UICONTROL Product -- Full Width]**- （ページビルダーが必要）製品ページの全幅レイアウトをカテゴリーページに適用します。 |
| [!UICONTROL Custom Layout Update] | サーバー上で使用可能なカスタムレイアウト更新ファイルを一覧表示します。 カテゴリに適用するカスタム レイアウト更新を選択します。 |
| [!UICONTROL Apply Design to Products] | 選択すると、カテゴリ内のすべての製品にカスタム設定が適用されます。 |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

_[!UICONTROL Scheduled Design Update]_セクションは、カスタムデザインがカテゴリーページに適用される日付の範囲を決定します。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | カスタムレイアウトがカテゴリに適用される日付の範囲を指定します。 |

![ デザイン更新をスケジュールしました](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
