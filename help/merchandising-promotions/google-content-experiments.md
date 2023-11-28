---
title: '[!DNL Google Content Experiments]'
description: 使用方法を学ぶ [!DNL Google Content Experiments] ：コマース製品、カテゴリ、コンテンツページの A/B テストを設定します。
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

次の例は、製品、カテゴリ、コンテンツページの A/B テストを、Google AnalyticsContent Experiment を使用して設定する方法を示しています。 コマース管理者と [!DNL Google Analytics] アカウント。

>[!NOTE]
>
>[!DNL Google Content Experiments] は廃止され、による置き換えが予定されています。 [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en).

## 手順 1. コンテンツ実験（コマース）を有効にする

1. コマースインストールの管理者にログインします。

1. 指示に従ってを有効にします。 [Google Analytics](google-analytics.md) とコマース設定の Content Experiment を組み合わせる必要があります。

   ![セールス設定 — Google API -Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## 手順 2. バリエーションの設定（コマース）

同じ製品、カテゴリまたはページの複数のバリエーションを作成します。

- 各バリエーションには、一意の [URL キー](../catalog/catalog-urls.md).
- 各バリエーションは同じである必要があります [ストア表示](../getting-started/websites-stores-views.md#scope-settings) 選択済み

テストする各エンティティには、最大で 10 個のバリエーションを作成できます。 製品の場合は、 [保存して複製](../catalog/product-workspace.md) 時間を節約できます。

## 手順 3. 実験の設定 (Google)

>[!NOTE]
>
>実験を作成するには、Googleアカウントに対する適切な権限が必要です。

1. 別のブラウザータブを開き、 [Google Analytics][2] アカウント。

   必要に応じて、 **[!UICONTROL Account]** および **[!UICONTROL Property]**.

1. 左側のサイドバーで、を選択します。 **[!UICONTROL Admin]** およびは、次のいずれかの方法を使用します。

   **メソッド 1:** 既存のビューを選択

   のヘッダー _[!UICONTROL View]_「 」列で下向き矢印をクリックし、実験のデータを提供するビューを選択します。

   **方法 2:** 新しいレポートビューの作成

   - のヘッダー _表示_ 列、クリック **[!UICONTROL Create View]** 次の操作を実行します。

      - 実験の場所を次のいずれかとして特定します。 `Website` または `Mobile app`.

      - 説明的な **[!UICONTROL Reporting View Name]**.

      - 次を指定します。 **[!UICONTROL Reporting Time Zone]**.

   - 完了したら、「 **[!UICONTROL Create View]** その後、戻る矢印をクリックして前のページに戻ります。

1. の下の左側のパネル _[!UICONTROL Reports]_を選択します。**[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. クリック **[!UICONTROL Create experiment]** 次の操作を実行します。

   - リダイレクトするトラフィックの割合を指定します。

   - 次を指定します。 **[!UICONTROL Original Page URL]** と各 **[!UICONTROL page variation]** テストしたいと思う

   - その他のオプションを設定します。

1. 実験を設定したら、 **[!UICONTROL Manually Insert the Code]** コードスニペットをコピーします。

## 手順 4. コードスニペットを貼り付け (Commerce)

1. コマースインストールの管理者に戻り、製品、カテゴリまたはページの元のバージョンを編集モードで開きます。

1. を展開します。 **[!UICONTROL View Optimization]** セクションに表示されます。

1. Google Analyticsからコピーしたコードスニペットをに貼り付けます。 **[!UICONTROL Experiment Code]** テキストボックス。

   >[!NOTE]
   >
   >コードスニペットをどのバリエーションにも貼り付けないでください。

   ![製品表示の最適化](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save]**.

## 手順 5：実験を確認し、開始します (Google)

1. に戻ります。 [Google Analytics][2] アカウント。

1. 実験設定を確認します。

1. 開始する準備が整ったら、「 **[!UICONTROL Start Experiment]**.

   それ以外の場合は、「 **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
