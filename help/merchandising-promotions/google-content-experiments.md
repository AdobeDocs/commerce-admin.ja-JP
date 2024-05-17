---
title: '[!DNL Google Content Experiments]'
description: の使用方法を学ぶ [!DNL Google Content Experiments] Commerceの製品、カテゴリまたはコンテンツページに対して A/B テストを設定する。
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

次の例は、Google Analyticsコンテンツ実験を使用して、製品、カテゴリまたはコンテンツページの A/B テストを設定する方法を示しています。 手順を進めながら、2 つのブラウザータブを開いたままにすることをお勧めします。Commerceの管理者とあなたの [!DNL Google Analytics] アカウント。

>[!NOTE]
>
>[!DNL Google Content Experiments] は非推奨（廃止予定）となり、による交換が予定されています [Googleの最適化](https://support.google.com/optimize/answer/7084762?hl=en).

## 手順 1. コンテンツ実験を有効にする（Commerce）

1. Commerce インストールの管理者にログインします。

1. 指示に従って有効にします [Google Analytics](google-analytics.md) Commerce設定にコンテンツ実験を含む。

   ![Sales configuration - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## 手順 2. バリエーションの設定（Commerce）

同じ製品、カテゴリまたはページの複数のバリエーションを作成します。

- 各バリエーションは、一意である必要があります [URL キー](../catalog/catalog-urls.md).
- 各バリエーションは同じである必要があります [ストア表示](../getting-started/websites-stores-views.md#scope-settings) を選択しました。

テストする各エンティティのバリエーションを最大 10 個作成できます。 製品の場合、を使用します。 [保存して複製](../catalog/product-workspace.md) 時間を節約する。

## 手順 3. 実験の設定（Google）

>[!NOTE]
>
>実験を作成するには、Google アカウントに対する適切な権限が必要です。

1. 別のブラウザータブを開き、 [Google Analytics][2] アカウント。

   必要に応じて、に移動します **[!UICONTROL Account]** および **[!UICONTROL Property]**.

1. 左側のサイドバーで、 **[!UICONTROL Admin]** 次のいずれかの方法を使用します。

   **メソッド 1:** 既存のビューを選択

   のヘッダーで _[!UICONTROL View]_列で、下向き矢印をクリックし、実験のデータを提供するビューを選択します。

   **メソッド 2:** 新しいレポート ビューの作成

   - のヘッダーで _表示_ 列、クリック **[!UICONTROL Create View]** 次の手順を実行します。

      - 実験の場所を次のいずれかとして識別します `Website` または `Mobile app`.

      - 説明を入力 **[!UICONTROL Reporting View Name]**.

      - を指定 **[!UICONTROL Reporting Time Zone]**.

   - 完了したら、 **[!UICONTROL Create View]** 次に、戻る矢印をクリックして前のページに戻ります。

1. の下の左パネルで _[!UICONTROL Reports]_、を選択&#x200B;**[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. クリック **[!UICONTROL Create experiment]** 次の手順を実行します。

   - リダイレクトするトラフィックの割合を指定します。

   - を指定 **[!UICONTROL Original Page URL]** およびそれぞれの URL **[!UICONTROL page variation]** テストしたいこと。

   - 他のオプションを入力します。

1. 実験を設定したら、をクリックします **[!UICONTROL Manually Insert the Code]** コードスニペットをコピーします。

## 手順 4. コードスニペットを貼り付ける（Commerce）

1. Commerce インストールの管理者に戻り、商品、カテゴリ、ページの元のバージョンを編集モードで開きます。

1. を展開します。 **[!UICONTROL View Optimization]** 商品、カテゴリまたはページのセクション。

1. Google Analyticsからコピーしたコードスニペットを、に貼り付けます。 **[!UICONTROL Experiment Code]** テキストボックス。

   >[!NOTE]
   >
   >コードスニペットを、どのバリエーションにも貼り付けないでください。

   ![製品表示の最適化](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

## 手順 5：実験のレビューと開始（Google）

1. に戻る [Google Analytics][2] アカウント。

1. 実験の設定をレビューします。

1. 開始する準備ができたら、 **[!UICONTROL Start Experiment]**.

   それ以外の場合は、 **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
