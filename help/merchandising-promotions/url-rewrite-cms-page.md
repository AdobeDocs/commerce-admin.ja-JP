---
title: コンテンツページの URL の書き換え
description: コンテンツページの URL の書き換えを使用して、Commerce ストア内の別のコンテンツページの URL にリンクをリダイレクトする方法を説明します。
exl-id: e29c45fd-cf25-4b51-a8ae-9e188dc2a61c
feature: Page Content, Configuration
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# コンテンツページの URL の書き換え

開始する前に、リダイレクトの目的を正確に理解しておく必要があります。 _ターゲット_/_ソース_ または _リダイレクト先_/_リダイレクト元_ を考慮します。 検索エンジンや古いリンクから以前のページに移動する場合もありますが、リダイレクトによってストアが新しいターゲットに切り替わります。

![URL の書き換え – CMSページ &#x200B;](./assets/url-rewrite-cms-page.png){width="700" zoomable="yes"}

## 手順 1. 書き換えの計画

ミスを避けるために、_リダイレクト先_ ページと _リダイレクト元_ ページの URL キーを書き留めてください。

不明な場合は、ストアの各ページを開き、ブラウザーのアドレスバーからパスをコピーします。

### CMSページのパス

「`new-page`」にリダイレクト。

リダイレクト元：`old-page`

## 手順 2. 書き換えの作成

{{url-rewrite-params}}

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL SEO & Search]_/**[!UICONTROL URL Rewrites]**&#x200B;に移動します。

1. 続行する前に、次の手順を実行して、リクエストパスが使用可能であることを確認します。

   - **[!UICONTROL Request Path]** 列の上部にある検索フィルターで、リダイレクトするページの URL キーを入力し、「リダイレク **[!UICONTROL Search]**」をクリックします。

   - ページに複数のリダイレクトレコードがある場合は、該当するストア表示に一致するものを見つけて、編集モードで開きます。

   - 右上隅の「**[!UICONTROL Delete]**」をクリックします。 プロンプトが表示されたら、「**[!UICONTROL OK]**」をクリックして確認します。

1. 「URL の書き換え」ページに戻ったら、「**[!UICONTROL Add URL Rewrite]**」をクリックします。

1. **[!UICONTROL Create URL Rewrite]** を `for CMS page` に設定します。

1. グリッドで新しいターゲットページを見つけ、編集モードで開きます。

   ![URL 書き換えの追加 – CMS ページの場合 &#x200B;](./assets/url-rewrite-cms-page-add.png){width="700" zoomable="yes"}

1. [ URL 書き換え情報 ] で、次の操作を行います。

   - 複数のストア表示がある場合は、書き換えが適用される **[!UICONTROL Store]** を選択します。

   - **[!UICONTROL Request Path]**：顧客のリクエスト元のページの URL キーを入力します。 これは _リダイレクト元_ ページです。

     >[!NOTE]
     >
     >リクエストパスは、指定したストアに対して一意である必要があります。 同じリクエストパスを使用するリダイレクトが既に存在する場合、リダイレクトを保存しようとするとエラーが発生します。 作成する前に、前のリダイレクトを削除する必要があります。

   - **[!UICONTROL Redirect]** を次のいずれかに設定します。

      - `Temporary (302)`
      - `Permanent (301)`

   - 参照用に、書き換えの簡単な説明を入力します。

   ![URL 書き換え情報 &#x200B;](./assets/url-rewrite-cms-page-information.png){width="600" zoomable="yes"}

1. リダイレクトを保存する前に、以下を確認してください。

   - 左上隅のリンクには、ターゲットページの名前が表示されます。
   - リクエストパスには、元の _リダイレクト元_ ページのパスが含まれています。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   新しい書き換えが、リストの上部のグリッドに表示されます。

## 手順 3. 結果のテスト

1. ストアのホームページに移動します。

1. 次のいずれかの操作を行います。

   - 元の _リダイレクト元_ ページに移動します。
   - ブラウザーのアドレスバーで、ストア URL の直後に元の _リダイレクト元_ ページの名前を入力し、**Enter** キーを押します。

   元のページリクエストの代わりに、新しいターゲットページが表示されます。

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 書き換えのタイプを示します。 書き換えの作成後にタイプを変更することはできません。 オプション：`Custom`/`For category`/`For product`/`For CMS page` |
| [!UICONTROL Request Path] | リダイレクトされるCMSページ。 リクエストパスは一意である必要があり、別のリダイレクトで使用することはできません。 リクエストパスが存在するというエラーメッセージが表示された場合は、既存のリダイレクトを削除してから再試行してください。 |
| [!UICONTROL Target Path] | 宛先を指すためにシステムで使用される内部パス。 ターゲットパスは灰色表示になっており、編集できません。 |
| [!UICONTROL Redirect] | リダイレクトのタイプを決定します。 オプション：<br/>**[!UICONTROL No]**- リダイレクトが指定されていません。<br/>**[!UICONTROL Temporary (302)]** – 検索エンジンに対して、書き換えが期間限定であることを示します。 検索エンジンは通常、一時的な書き換えのページランク情報を保持しません。 <br/>**[!UICONTROL Permanent (301)]**– 検索エンジンに対して、書き換えが永続的であることを示します。 検索エンジンでは通常、永続的な書き換えの際にページランク情報が保持されます。 |
| [!UICONTROL Description] | 内部参照用の書き換えの目的について説明します。 |

{style="table-layout:auto"}
