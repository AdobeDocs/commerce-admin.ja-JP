---
title: フラット カタログ
description: 製品またはカテゴリに関して必要なすべてのデータが各行に含まれるフラットなカタログの作成について説明します。
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# フラット カタログ

>[!IMPORTANT]
>
>フラット カタログを使用することは、現在ではベスト プラクティスとして推奨されていません。 この機能を継続的に使用すると、パフォーマンスの低下やその他のインデックス作成の問題が発生することが知られています。 詳細な説明と解決策については、こちらを参照してください [ヘルプセンター](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>影響を受けるバージョンは次のとおりです。 <br/>- クラウドインフラストラクチャー上のAdobe Commerce、2.3.x 以降<br/>- Adobe Commerce（オンプレミス）、2.3.x 以降<br/>- Magento Open Source, 2.3.x 以上 <br/><br/>どのリリースバージョンでも、一部の拡張機能はフラットテーブルでのみ機能するので、フラットテーブルを無効にした場合にリスクが発生します。 フラットカタログインデクサーを使用する拡張機能があることがわかっている場合は、それらの値をに設定する際に、このリスクに注意する必要があります `No`.

Commerceは通常、Entity-Attribute-Value （EAV）モデルに基づいて、カタログデータを複数のテーブルに格納します。 製品属性は多くのテーブルに格納されるので、SQL クエリは長くて複雑な場合があります。

これに対し、フラットなカタログはその場でテーブルを作成し、各行には、製品またはカテゴリに関する必要なデータがすべて含まれています。 フラットなカタログは、毎分、または cron ジョブに従って自動的に更新されます。 フラットなカタログインデックス作成により、カタログと買い物かごの価格ルールの処理も迅速化できます。 50 万個もの SKU を持つカタログは、フラットカタログとしてすばやくインデックスを作成できます。

>[!NOTE]
>
>ライブストアに対してフラットカタログを有効にする前に、必ず開発環境で設定をテストしてください。

## 手順 1：フラットカタログを有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開します。 _ストアフロント_ を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Use Flat Catalog Category]** 対象： `Yes`. （必要に応じて、 **[!UICONTROL Use system value]** チェックボックスをオンにします）。

   - を設定 **[!UICONTROL Use Flat Catalog Product]** 対象： `Yes`.

   ![フラットなカタログ設定](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

1. キャッシュの更新を求めるメッセージが表示されたら、 **[!UICONTROL Cache Management]** システムメッセージで、手順に従ってキャッシュを更新します。

## 手順 2：結果の確認

結果を検証する方法は 2 つあります。

### 方法 1：単一の製品の結果の確認

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を編集モードで開きます。

1. の場合 **[!UICONTROL Name]**、テキストを追加します `_TEST` 製品名の末尾に追加されます。

1. クリック **[!UICONTROL Save]**.

1. 新しいブラウザータブで、ストアのホームページに移動し、次の操作を行います。

   - 編集した製品を検索します。

   - ナビゲーションを使用して、割り当てられたカテゴリの下の製品を参照します。

     必要に応じて、ページを更新して結果を確認します。 変更は 1 分以内に、または状況に応じて表示されます [Cron](../systems/cron.md) スケジュール。

   ![フラットカタログ付きストアフロント](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### 方法 2：カテゴリの結果の確認

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左上隅で、次のことを確認します **[!UICONTROL Store View]** はに設定されています。 `All Store Views`.

   プロンプトが表示されたら、 **[!UICONTROL OK]** を確認します。

1. カテゴリ ツリーで、既存のカテゴリを選択し、 **[!UICONTROL Add Subcategory]**&#x200B;をクリックし、次の手順を実行します。

   - の場合 **[!UICONTROL Category Name]**、と入力します `Test Category`.

   - 完了したら、 **[!UICONTROL Save]**.

     ![サブカテゴリのテスト](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Products in Category]** セクションでクリック **[!UICONTROL Reset Filter]** すべての商品を表示します。

   - 新しいカテゴリに追加する複数の製品のチェックボックスをオンにします。

   - click **[!UICONTROL Save]**.

   ![テスト カテゴリ製品](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. 新しいブラウザータブでストアのホームページに移動し、ストアナビゲーションを使用して、作成したカテゴリを参照します。

   必要に応じて、ページを更新して結果を確認します。 変更は 1 分以内か、cron スケジュールに従って表示されます。

## 手順 3：テストデータを削除

テストデータを削除して元の製品名とカタログ設定を復元するには、次の手順を実行します。

### テストカテゴリを削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーで、作成したテストサブカテゴリを選択します。

1. 右上隅のをクリックします。 **[!UICONTROL Delete]**.

1. 確認を求められたら、 **[!UICONTROL OK]**.

   このカテゴリ削除によって、カテゴリに割り当てられている製品が削除されるわけではありません。

### 元の製品名を復元

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. テスト製品を編集モードで開きます。

1. を削除 `_TEST` に追加したテキスト **[!UICONTROL Product Name]**.

1. 右上隅のをクリックします。 **[!UICONTROL Save]**.

### 元のカタログ設定を復元

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開します。 _ストアフロント_ を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Use Flat Catalog Category]** 対象： `No`.

   - を設定 **[!UICONTROL Use Flat Catalog Product]** 対象： `No`.

1. 完了したら、 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、キャッシュを更新します。
