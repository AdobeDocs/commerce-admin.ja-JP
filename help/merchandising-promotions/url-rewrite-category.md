---
title: カテゴリ URL の書き換え
description: カテゴリ URL の書き換えを使用して、Commerce ストア内の別のカテゴリの URL にリンクをリダイレクトする方法を説明します。
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# カテゴリ URL の書き換え

カタログからカテゴリが削除された場合、カテゴリの書き換えを使用して、ストア内の別のカテゴリの URL へのリンクをリダイレクトできます。 _ターゲット_/_元のリクエスト_ または _リダイレクト_/_リダイレクト元_ を考慮します。 検索エンジンや古いリンクから以前のページに移動する場合もありますが、リダイレクトによってストアが新しいターゲットに切り替わります。

ストアで [ 自動リダイレクト ](url-redirect-product-automatic.md) が有効になっている場合、カテゴリ [URL キー ](../catalog/catalog-urls.md) が変更されたときに書き換えを作成する必要はありません。

{{url-rewrite-skip}}

## 手順 1. 書き換えの計画

ミスを避けるために、_リダイレクト先_ パスと _リダイレクト元_ パスを書き留め、URL キーとサフィックス（該当する場合）を含めます。

不明な場合は、各カテゴリページをストアで開き、ブラウザーのアドレスバーからパスをコピーします。

**例：**

「`gear/backpacks-and-bags.html`」にリダイレクト。

リダイレクト元：`gear/bags.html`

## 手順 2. 書き換えの作成

{{url-rewrite-params}}

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL SEO & Search]_/**[!UICONTROL URL Rewrites]**&#x200B;に移動します。

1. 続行する前に、次の手順を実行して、リクエストパスが使用可能であることを確認します。

   - **[!UICONTROL Request Path]** 列の上部にある検索フィルターで、リダイレクトするカテゴリの URL キーを入力し、「リダイレク **[!UICONTROL Search]**」をクリックします。

   - ページに複数のリダイレクトレコードがある場合は、該当するストア表示に一致するものを見つけ、リダイレクトレコードを編集モードで開きます。

   - 右上隅の「**[!UICONTROL Delete]**」をクリックします。 プロンプトが表示されたら、「**[!UICONTROL OK]**」をクリックして確認します。

1. _[!UICONTROL URL Rewrites]_&#x200B;ページに戻ったら、「**[!UICONTROL Add URL Rewrite]**」をクリックします。

1. **[!UICONTROL Create URL Rewrite]** を `For category` に設定して、リダイレクトの宛先となるツリー内のターゲットカテゴリを選択します。

   ![URL 書き換え – カテゴリの選択 ](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. _URL 書き換え_ セクションで、次の操作を行います。

   - 複数のストアがある場合は、書き換えが適用される **[!UICONTROL Store]** を選択します。

   - **[!UICONTROL Request Path]**：顧客がリクエストするカテゴリの URL キーを入力します。 これは _リダイレクト元_ カテゴリです。

     >[!NOTE]
     >
     >リクエストパスは、指定したストアに対して一意である必要があります。 同じリクエストパスを使用するリダイレクトが既に存在する場合、リダイレクトを保存しようとするとエラーが発生します。 作成する前に、前のリダイレクトを削除する必要があります。

   - **[!UICONTROL Redirect]** を次のいずれかに設定します。

      - `Temporary (302)`
      - `Permanent (301)`

   - 参照用に、書き換えの簡単な説明を入力します。

   ![ カテゴリの URL 書き換えを追加 ](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. リダイレクトを保存する前に、以下を確認してください。

   - 左上隅のリンクには、ターゲットカテゴリの名前が表示されます。
   - リクエストパスには、元の _リダイレクト元_ カテゴリのパスが含まれています。

1. 完了したら、ボタン **[!UICONTROL Save]** クリックします。

   新しいカテゴリの書き換えは、URL の書き換えグリッドの上部に表示されます。

## 手順 3. 結果のテスト

1. ストアのホームページに移動します。

1. 次のいずれかの操作を行います。

   - 元の _リダイレクト元_ カテゴリに移動します。
   - ブラウザーのアドレスバーで、ストア URL の直後に元の _リダイレクト元_ カテゴリへのパスを入力し、**[!UICONTROL Enter]** キーを押します。

   元のカテゴリリクエストの代わりに、新しいターゲットカテゴリが表示されます。

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 書き換えのタイプを示します。 書き換えの作成後にタイプを変更することはできません。 オプション：`Custom`/`For category`/`For product`/`For CMS page` |
| [!UICONTROL Request Path] | リダイレクトされるカテゴリ。 設定に応じて、リクエストパスには.html または.htm サフィックス、親カテゴリが含まれる場合があります。 リクエストパスは一意である必要があり、別のリダイレクトで使用することはできません。 リクエストパスが存在するというエラーが表示された場合は、既存のリダイレクトを削除してから再試行してください。 |
| [!UICONTROL Target Path] | リダイレクトの宛先を指すためにシステムで使用される内部パス。 ターゲットパスは灰色表示になっており、編集できません。 |
| [!UICONTROL Redirect] | リダイレクトのタイプを決定します。 オプション：<br/>**[!UICONTROL No]**- リダイレクトが指定されていません。 多くの操作では、このタイプのリダイレクトリクエストが作成されます。 例えば、商品をカテゴリに追加するたびに、`No` タイプのリダイレクトが各ストア表示に作成されます。<br/>**[!UICONTROL Temporary (302)]** – 検索エンジンに対して、書き換えが期間限定であることを示します。 検索エンジンは通常、一時的な書き換えのページランク情報を保持しません。 <br/>**[!UICONTROL Permanent (301)]**– 検索エンジンに対して、書き換えが永続的であることを示します。 検索エンジンでは通常、永続的な書き換えの際にページランク情報が保持されます。 |
| [!UICONTROL Description] | 内部参照用の書き換えの目的について説明します。 |

{style="table-layout:auto"}
