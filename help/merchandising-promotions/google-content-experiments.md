---
title: '[!DNL Google Content Experiments]'
description: Commerceの製品、カテゴリまたはコンテンツページに対して A/B テストを使用  [!DNL Google Content Experiments]  設定する方法を説明します。
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

次の例は、Google Analyticsコンテンツ実験を使用して、製品、カテゴリまたはコンテンツページの A/B テストを設定する方法を示しています。 手順を進めながら、2 つのブラウザータブを開いたままにすることをお勧めします。Commerce管理者と [!DNL Google Analytics] アカウントの間で何度も往復する必要があるからです。

>[!NOTE]
>
>[!DNL Google Content Experiments] は非推奨（廃止予定）となり、[Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en) による置き換えが予定されています。

## 手順 1. コンテンツ実験を有効にする（Commerce）

1. Commerce インストールの管理者にログインします。

1. 手順に従って、Commerce設定のコンテンツ実験で [&#128279;](google-analytics.md)0&rbrace;Google Analytics&rbrace; を有効にします。

   ![Sales configuration - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## 手順 2. バリエーションの設定（Commerce）

同じ製品、カテゴリまたはページの複数のバリエーションを作成します。

- 各バリエーションには、一意の [URL キー ](../catalog/catalog-urls.md) が必要です。
- 各バリエーションで、同じ [ ストア表示 ](../getting-started/websites-stores-views.md#scope-settings) が選択されている必要があります。

テストする各エンティティのバリエーションを最大 10 個作成できます。 製品の場合は、「保存して複製 [ を使用して時間を節約 ](../catalog/product-workspace.md) ます。

## 手順 3. 実験の設定（Google）

>[!NOTE]
>
>実験を作成するには、Google アカウントに対する適切な権限が必要です。

1. 別のブラウザータブを開き、[Google Analytics][2] アカウントにログインします。

   必要に応じて、**[!UICONTROL Account]** に移動し、**[!UICONTROL Property]** をクリックします。

1. 左側のサイドバーで「**[!UICONTROL Admin]**」を選択し、次のいずれかの方法を使用します。

   **方法 1:** 既存のビューを選択する

   「_[!UICONTROL View]_」列のヘッダーで、下向き矢印をクリックし、実験のデータを提供するビューを選択します。

   **方法 2:** 新しいレポートビューの作成

   - _表示_ 列のヘッダーで、「表示」をクリックし、次の **[!UICONTROL Create View]** 順を実行します。

      - 実験の場所を `Website` または `Mobile app` として識別します。

      - 説明 **[!UICONTROL Reporting View Name]** を入力します。

      - **[!UICONTROL Reporting Time Zone]** を指定してください

   - 完了したら、「**[!UICONTROL Create View]**」をクリックし、戻る矢印をクリックして前のページに戻ります。

1. _[!UICONTROL Reports]_&#x200B;の下の左パネルで、**[!UICONTROL Behavior]**/**[!UICONTROL Experiments]**&#x200B;を選択します。

1. 「**[!UICONTROL Create experiment]**」をクリックして、次の操作を実行します。

   - リダイレクトするトラフィックの割合を指定します。

   - テストする各 **[!UICONTROL page variation]** の **[!UICONTROL Original Page URL]** と URL を指定します。

   - 他のオプションを入力します。

1. 実験を設定したら、「実 **[!UICONTROL Manually Insert the Code]**」をクリックして、コードスニペットをコピーします。

## 手順 4. コードスニペットを貼り付ける（Commerce）

1. Commerce インストールの管理者に戻り、商品、カテゴリ、ページの元のバージョンを編集モードで開きます。

1. 製品、カテゴリまたはページの「**[!UICONTROL View Optimization]**」セクションを展開します。

1. Google Analyticsからコピーしたコードスニペットを「**[!UICONTROL Experiment Code]**」テキストボックスに貼り付けます。

   >[!NOTE]
   >
   >コードスニペットを、どのバリエーションにも貼り付けないでください。

   ![ 製品表示の最適化 ](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 手順 5：実験のレビューと開始（Google）

1. [Google Analytics][2] アカウントに戻ります。

1. 実験の設定をレビューします。

1. 開始する準備ができたら、「開 **[!UICONTROL Start Experiment]**」をクリックします。

   それ以外の場合は、「**[!UICONTROL Save for Later]**」をクリックします。


[2]: https://analytics.google.com/
