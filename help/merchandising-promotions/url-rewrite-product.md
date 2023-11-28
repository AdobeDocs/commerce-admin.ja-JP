---
title: 製品 URL の書き換え
description: 製品 URL の書き換えを使用して、コマースストア内の別の製品の URL にリンクをリダイレクトする方法を説明します。
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# 製品 URL の書き換え

開始する前に、リダイレクトが達成すべきことを正確に理解しておく必要があります。 考え方を _ターゲット_ / _オリジナルリクエスト_ または _リダイレクト_ / _リダイレクト_. ユーザーは引き続き検索エンジンや古いリンクから前のページに移動する可能性がありますが、リダイレクトによってストアが新しいターゲットに切り替わります。

次の場合 [自動リダイレクト](url-redirect-product-automatic.md) がストアに対して有効になっているので、製品を書き換える際に書き換えを作成する必要はありません [URL キー](../catalog/catalog-urls.md) が変更されました。

{{url-rewrite-skip}}

## 手順 1. 書き換えの計画

間違いを避けるには、 _リダイレクト_ パスと _リダイレクト_ パスおよび URL キーおよびサフィックスを含めます（該当する場合）。

不明な場合は、ストアの各製品ページを開き、ブラウザーのアドレスバーからパスをコピーします。 製品リダイレクトを作成する際に、 [カテゴリパス](../catalog/catalog-urls.md). この例では、カテゴリパスを含まない製品のリダイレクトを作成します。

### カテゴリパスを含む製品

リダイレクト先： `gear/bags/impulse-duffle.html`

リダイレクト元： `gear/bags/overnight-duffle.html`

### カテゴリパスのない製品

リダイレクト先： `impulse-duffle.html`

リダイレクト元： `overnight-duffle.html`

## 手順 2. 書き換えの作成

{{url-rewrite-params}}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. 続行する前に、次の手順を実行して、リクエストパスが使用可能であることを確認します。

   - 」をクリックします。 **[!UICONTROL Request Path]** 列で、リダイレクトするページの URL キーを入力し、 **[!UICONTROL Search]**.

   - ページに複数のリダイレクトレコードがある場合は、該当するストアビューと一致するレコードを探し、編集モードで開きます。

   - 右上隅で、 **[!UICONTROL Delete]**. プロンプトが表示されたら、「 **[!UICONTROL OK]** をクリックして確定します。

1. URL の書き換えページの右上隅にある、 **URL 書き換えを追加**.

1. 設定 **[!UICONTROL Create URL Rewrite]** から `For product`.

1. グリッドで、リダイレクトのターゲット（宛先）となる製品を探し、行をクリックします。

   ![URL の書き換え — product](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. カテゴリツリーの下で、 **[!UICONTROL Skip Category Selection]**.

   この例では、リダイレクトにカテゴリは含まれていません。

   ![製品 URL の書き換え — カテゴリ選択をスキップ](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   製品の URL を書き換えを追加ページの左上隅にターゲットへのリンクが表示され、「ターゲットパス」フィールドにはパスのシステムバージョンが表示されます。このリンクは変更できません。 最初に、「リダイレクトパス」フィールドにもターゲットパスが表示されます。

   - 複数のストアビューがある場合、 **[!UICONTROL Store]** を、書き換えが適用されるビューに追加します。 それ以外の場合は、各ビューに対して書き換えが作成されます。

   - の場合 **[!UICONTROL Request Path]**&#x200B;に置き換え、元の製品リクエストの URL キーとサフィックス（該当する場合）を入力して、デフォルトを置き換えます。 これが _リダイレクト_ 計画ステップで特定した製品。

     >[!NOTE]
     >
     >リクエストパスは、指定したストアに対して一意である必要があります。 同じリクエストパスを使用するリダイレクトが既に存在する場合、リダイレクトを保存しようとするとエラーが表示されます。 以前のリダイレクトを作成する前に、削除する必要があります。

   - 設定 **[!UICONTROL Redirect Type]** を次のいずれかに変更します。

      - `Temporary (302)`
      - `Permanent (301)`

   - 参照用に、簡単な情報を入力します。 **[!UICONTROL Description]** 書き換えの

   ![製品 URL の書き換え — 情報](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. リダイレクトを保存する前に、以下を確認します。

   - 左上隅のリンクには、ターゲット製品の名前が表示されます。
   - リクエストパスには、元の _リダイレクト_ 製品。

1. 完了したら、「 **[!UICONTROL Save]**.

   新しい製品の書き換えが「 URL の書き換え」グリッドの上部に表示されるようになりました。

## 手順 3. 結果をテストする

1. ストアのホームページに移動します。

1. 次のいずれかの操作を行います。

   - 元のページに移動 _リダイレクト_ 製品リクエストページ。
   - ブラウザーのアドレスバーに、元の _リダイレクト_ ストア URL の直後に表示される製品で、 **入力**.

   元の製品リクエストの代わりに新しいターゲット製品が表示されます。

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 書き換えのタイプを示します。 書き換えの作成後は、タイプを変更できません。 オプション： `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | リダイレクトする製品。 設定によっては、リクエストパスに `.html` または `.htm` サフィックス、およびカテゴリ。 リクエストパスは一意である必要があり、別のリダイレクトで使用することはできません。 リクエストパスが存在するというエラーが表示された場合は、既存のリダイレクトを削除して、もう一度試してください。 |
| [!UICONTROL Target Path] | リダイレクト先を指すためにシステムで使用される内部パス。 ターゲットパスはグレー表示になっており、編集できません。 |
| [!UICONTROL Redirect] | リダイレクトのタイプを決定します。 オプション： <br/>**[!UICONTROL No]**— リダイレクトが指定されていません。 多くの操作では、このタイプのリダイレクトリクエストが作成されます。 例えば、製品をカテゴリに追加するたびに、 `No` ストアビューごとにタイプが作成されます。<br/>**[!UICONTROL Temporary (302)]**  — 書き換えが期間限定であることを検索エンジンに示します。 一般に、検索エンジンでは、一時的な書き換えのためにページのランク情報が保持されません。 <br/>**[!UICONTROL Permanent (301)]**— 書き換えが永続的であることを検索エンジンに示します。 通常、検索エンジンは、永続的な書き換えのためにページのランク情報を保持します。 |
| [!UICONTROL Description] | 内部参照用に書き換えの目的を記述します。 |

{style="table-layout:auto"}

## 複数の URL の書き換え

次の手順を使用して、複数またはすべての製品の URL 書き換えをすばやく更新できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. URL の書き換えを更新するすべての製品を選択します。

1. の下 _[!UICONTROL Actions]_を選択します。**[!UICONTROL Update attributes]**をクリックして、複数またはすべての書き換えを更新します。

1. の下 _[!UICONTROL PRODUCTS INFORMATION]_をクリックし、**[!UICONTROL Websites]**タブをクリックします。

1. Adobe Analytics の _[!UICONTROL Add Product To Websites]_「 」セクションで、URL の書き換えを復元するすべての Web サイトを選択します。

1. 更新の準備が整ったら、「 **[!UICONTROL Save]**.

>[!NOTE]
>
>選択したすべての製品が選択した Web サイトに読み込まれ、URL の書き換えが再生成されます。

![属性を更新 — 複数の URL の書き換えを更新](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
