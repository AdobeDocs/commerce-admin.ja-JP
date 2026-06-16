---
title: ウィジェットの作成と管理
description: ストア全体でコンテンツを自動的に更新するウィジェットを作成および管理する方法について説明します。
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/f5cIxzZeOxfvqJbVLFPfCmB285I0ovGEbNqAWOFCw4s
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 0%

---

# ウィジェットの作成と管理

ウィジェットは再利用可能なコンポーネントです。 ウィジェットを容易に作成したり、既存のウィジェットを変更して、ストア全体のコンテンツを自動的に更新したりできます。 また、使用されなくなったウィジェットを削除することもできます。

![ ウィジェット ](./assets/widgets.png){width="700" zoomable="yes"}

## ウィジェットを作成

ウィジェットを作成するプロセスは、各[ ウィジェットタイプ ](widgets.md#widget-types)でほぼ同じです。 手順の最初の部分に従って、目的の特定の種類のウィジェットの最後の部分を完了できます。

### 手順1：種類の選択

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**に移動します。

1. **[!UICONTROL Add Widget]**&#x200B;をクリックします。

1. _[!UICONTROL Settings]_セクション：

   - 作成するウィジェットタイプに&#x200B;**[!UICONTROL Type]**&#x200B;を設定します。

   - **[!UICONTROL Design Theme]**&#x200B;が現在のテーマに設定されていることを確認します。

     ![ ウィジェット設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

### 手順2：ストアフロントのプロパティとレイアウトの指定

1. _[!UICONTROL Storefront Properties]_セクション：

   - 「**[!UICONTROL Widget Title]**」に、ウィジェットの説明的なタイトルを入力します。

     このタイトルは、管理者からのみ表示されます。

   - **[!UICONTROL Assign to Store Views]**&#x200B;で、ウィジェットを表示するストアビューを選択します。

     特定のストアビュー、または`All Store Views`を選択できます。 複数のビューを選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]**&#x200B;の場合、ページの同じ部分で他のユーザーと一緒にこの項目を表示する順序を決定する番号を入力します。 （`0` = first, `1` = second, `3` = thirdなど）

     ![ ストアフロントのプロパティ ](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. _[!UICONTROL Layout Updates]_セクションで、**[!UICONTROL Add Layout Update]**をクリックします。

1. **[!UICONTROL Display On]**&#x200B;を表示するページの種類に設定します。

1. **[!UICONTROL Container]** リストで、配置するページレイアウトの領域を選択します。

   ![ レイアウトの更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. ウィジェットがリンクの場合は、**[!UICONTROL Template]**&#x200B;を次のいずれかに設定します。

   - `Block Template` - コンテンツを書式設定して、ページ上にスタンドアロン単位として配置できるようにします。
   - `Inline Template` – 他のコンテンツ内に配置できるように、コンテンツをフォーマットします。 例えば、テキストの段落内に配置されたリンクなどです。

### ステップ 3：ウィジェットオプションを完了する

各ウィジェットの種類のオプションは多少異なりますが、プロセスは基本的に同じです。 次の使用例は、特定のカテゴリの製品リストをページネーション コントロールと共に表示します。

1. 左側のパネルで、**[!UICONTROL Widget Options]**&#x200B;を選択します。

1. **[!UICONTROL Select Block]**&#x200B;をクリックします。

1. リストの上に表示する&#x200B;**[!UICONTROL Title]**&#x200B;を入力します（`Featured Products`など）。

1. ページ分割コントロールの場合は、**[!UICONTROL Display Page Control]**&#x200B;を`Yes`に設定し、次の操作を行います。

   - **[!UICONTROL Number of Products per Page]**&#x200B;を入力します。

   - 合計&#x200B;**[!UICONTROL Number of Products to Display]**&#x200B;を入力します。

   - **[!UICONTROL Condition]**&#x200B;を特集する製品のカテゴリに設定します。

     このプロセスは、[価格ルール ](../merchandising-promotions/price-rules-catalog.md)の条件を設定するのと同じです。

### 手順4：結果を保存して確認する

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

1. プロンプトが表示されたら、ワークスペースの上部にある指示に従って、必要に応じてキャッシュを更新します。

1. ストアフロントに戻り、ウィジェットが正しく動作していることを確認します。

   別の場所に移動するには、ウィジェットを再度開いて、別のページまたはブロック参照を試します。

## ウィジェット作成デモ

ウィジェットの作成について詳しくは、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12&learn=on)

## ウィジェットの編集

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**に移動します。

1. グリッドの上にあるフィルターを使用してウィジェットを見つけ、ウィジェット名をクリックします。

1. 必要な変更を加える：

   ウィジェットオプションについて詳しくは、ウィジェットを作成する手順を参照してください。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## ウィジェットの削除

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**に移動します。

1. グリッドの上にあるフィルターを使用してウィジェットを見つけ、削除するウィジェットのチェックボックスを選択します。

1. リストの左上隅で、**[!UICONTROL Actions]**&#x200B;を`Delete`に設定します。

1. 完了したら、**[!UICONTROL Submit]**&#x200B;をクリックします。

1. アクションを確認するには、**[!UICONTROL OK]**&#x200B;をクリックします。
