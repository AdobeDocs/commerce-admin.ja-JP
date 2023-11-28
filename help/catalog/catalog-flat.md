---
title: フラットカタログ
description: 各行に商品やカテゴリに関する必要なデータがすべて含まれるフラットカタログの作成について説明します。
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# フラットカタログ

>[!IMPORTANT]
>
>フラットカタログの使用は、ベストプラクティスとして推奨されなくなりました。 この機能を継続して使用すると、パフォーマンスが低下し、その他のインデックス作成の問題が発生することがわかっています。 詳細な説明と解決策については、 [ヘルプセンター](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>影響を受けるバージョンは次のとおりです。 <br/>- Adobe Commerce on cloud infrastructure 2.3.x 以降<br/>- Adobe Commerce（オンプレミス）、2.3.x 以降<br/>-Magento Open Source、2.3.x 以降 <br/><br/>どのリリースバージョンでも、一部の拡張機能はフラットテーブルでのみ機能するので、フラットテーブルを無効にするとリスクが生じます。 フラットカタログインデクサーを使用する拡張機能があることがわかっている場合は、これらの値をに設定する際に、このリスクに注意する必要があります。 `No`.

Commerce では通常、エンティティ属性値 (EAV) モデルに基づいて、複数のテーブルにカタログデータを格納します。 製品属性は多くのテーブルに格納されるので、SQL クエリは長く複雑な場合があります。

これに対し、フラットカタログではその場でテーブルを作成し、各行には製品またはカテゴリに関する必要なデータがすべて含まれます。 フラットカタログは、毎分、または cron ジョブに従って、自動的に更新されます。 フラットカタログのインデックス作成は、カタログと買い物かごの価格ルールの処理を高速化することもできます。 500,000 個もの SKU を持つカタログは、フラットカタログとしてすばやくインデックスを作成できます。

>[!NOTE]
>
>フラットカタログをライブストアに対して有効にする前に、開発環境で設定をテストしておく必要があります。

## 手順 1：フラットカタログを有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. を展開します。 _ストアフロント_ 」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Use Flat Catalog Category]** から `Yes`. ( 必要に応じて、 **[!UICONTROL Use system value]** チェックボックス )

   - 設定 **[!UICONTROL Use Flat Catalog Product]** から `Yes`.

   ![フラットカタログ構成](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** を選択し、指示に従ってキャッシュを更新します。

## 手順 2：結果の確認

結果の検証に使用できる方法は 2 つあります。

### 方法 1：単一の製品の結果を検証する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を編集モードで開きます。

1. の場合 **[!UICONTROL Name]**、テキストを追加 `_TEST` を製品名の末尾に追加します。

1. クリック **[!UICONTROL Save]**.

1. 新しいブラウザータブで、ストアのホームページに移動し、次の操作を実行します。

   - 編集した製品を検索します。

   - 割り当てられたカテゴリの製品を参照するには、ナビゲーションを使用します。

     必要に応じて、ページを更新して結果を確認します。 変更は 1 分以内に、または [Cron](../systems/cron.md) スケジュール。

   ![フラットカタログ付きストアフロント](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### 方法 2：カテゴリの結果の確認

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左上隅で、 **[!UICONTROL Store View]** が `All Store Views`.

   プロンプトが表示されたら、をクリックします。 **[!UICONTROL OK]** をクリックして確定します。

1. カテゴリツリーで、既存のカテゴリを選択し、 **[!UICONTROL Add Subcategory]**&#x200B;をクリックし、次の操作を実行します。

   - の場合 **[!UICONTROL Category Name]**，と入力します。 `Test Category`.

   - 完了したら、「 **[!UICONTROL Save]**.

     ![サブカテゴリをテスト](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Products in Category]** 「 」セクションで、「 」をクリックします。 **[!UICONTROL Reset Filter]** すべての製品を表示します。

   - 新しいカテゴリに追加する複数の製品のチェックボックスを選択します。

   - click **[!UICONTROL Save]**.

   ![カテゴリ製品をテスト](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. 新しいブラウザータブで、ストアのホームページに移動し、ストアナビゲーションを使用して作成したカテゴリを参照します。

   必要に応じて、ページを更新して結果を確認します。 変更は、1 分以内または Cron スケジュールに従って表示されます。

## 手順 3：テストデータを削除する

次の手順を実行して、テストデータを削除し、元の製品名とカタログ設定を復元します。

### テストカテゴリを削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーで、作成したテストサブカテゴリを選択します。

1. 右上隅で、 **[!UICONTROL Delete]**.

1. 確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.

   このカテゴリの削除では、カテゴリに割り当てられている製品は削除されません。

### 元の製品名を復元

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. テスト製品を編集モードで開きます。

1. を削除します。 `_TEST` 追加したテキスト **[!UICONTROL Product Name]**.

1. 右上隅で、 **[!UICONTROL Save]**.

### 元のカタログ設定を復元

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. を展開します。 _ストアフロント_ 」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Use Flat Catalog Category]** から `No`.

   - 設定 **[!UICONTROL Use Flat Catalog Product]** から `No`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、キャッシュを更新します。
