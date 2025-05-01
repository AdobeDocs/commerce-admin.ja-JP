---
title: カスタム URL の書き換え
description: カスタム URL リライトを使用して、Commerce ストア内のその他のリダイレクトを管理する方法について説明します。
exl-id: b15054be-e463-48e6-b6c1-0a8a2141cc01
feature: Search, Configuration
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# カスタム URL の書き換え

カスタムの書き換えを使用して、ストアから外部 web サイトにページをリダイレクトするなど、その他のリダイレクトを管理できます。 例えば、2 つのCommerce web サイトがあり、それぞれに独自のドメインを持っている場合があります。 カスタムリダイレクトを使用すると、製品、カテゴリまたはページのリクエストを別の web サイトにリダイレクトできます。 他のリダイレクトタイプとは異なり、カスタムリダイレクトのターゲットは、ストア内の既存のページのリストから選択されません。

開始する前に、リダイレクトの目的を正確に理解しておく必要があります。 _ターゲット_/_ソース_ または _リダイレクト先_/_リダイレクト元_ を考慮します。 検索エンジンや古いリンクから以前のページに移動する場合もありますが、リダイレクトによってストアが新しいターゲットに切り替わります。

## 手順 1. 書き換えの計画

ミスを避けるために、_リダイレクト先_ ページの URL と、_リダイレクト元_ ページの URL キーを書き留めてください。

不明な場合は各ページを開き、ブラウザーのアドレスバーから URL をコピーします。

**例**

リダイレクト：

    http://www.different-website.com/page.html

リダイレクト元：

    cms-page
    category.html
    category/subcategory.html
    product.html
    category/product.html

## 手順 2. 書き換えの作成

{{url-rewrite-params}}

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL SEO & Search]_/**[!UICONTROL URL Rewrites]**に移動します。

1. 続行する前に、次の手順を実行して、リクエストパスが使用可能であることを確認します。

   - **[!UICONTROL Request Path]** 列の上部にある検索フィルターで、リダイレクトするページの URL キーを入力し、「リダイレク **[!UICONTROL Search]**」をクリックします。

   - ページに複数のリダイレクトレコードがある場合は、該当するストア表示に一致するものを見つけて、編集モードで開きます。

   - 右上隅の「**[!UICONTROL Delete]**」をクリックします。 プロンプトが表示されたら、「**[!UICONTROL OK]**」をクリックして確認します。

1. 「URL の書き換え」ページに戻ったら、「**[!UICONTROL Add URL Rewrite]**」をクリックします。

1. **[!UICONTROL Create URL Rewrite]** を `Custom` に設定します。

   ![URL の書き換え – カスタム ](./assets/url-rewrite-custom.png){width="600" zoomable="yes"}

1. [ URL 書き換え情報 ] で、次の操作を行います。

   - 複数のストア表示がある場合は、書き換えが適用される **[!UICONTROL Store]** を選択します。

   - **[!UICONTROL Request Path]** しくは、リダイレクトする商品、カテゴリまたはCMSページの URL キーとパス（該当する場合）を入力します。

     >[!NOTE]
     >
     >リクエストパスは、指定したストアに対して一意である必要があります。 同じリクエストパスを使用するリダイレクトが既に存在する場合、リダイレクトを保存しようとするとエラーが発生します。 作成する前に、前のリダイレクトを削除する必要があります。

   - **[!UICONTROL Target Path]**：宛先の URL を入力します。 ターゲットが別の web サイト上にある場合は、完全修飾 URL を入力します。

   - **リダイレクト** を次のいずれかに設定します。

      - `Temporary (302)`
      - `Permanent (301)`

   - 参照用に、書き換えの簡単な説明を入力します。

1. リダイレクトを保存する前に、以下を確認してください。

   - [!UICONTROL Request Path] には、元の _リダイレクト元_ ページの URL キーまたはパスが含まれます。
   - [!UICONTROL Target Path] には、_リダイレクト先_ ページの URL が含まれます。

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
| [!UICONTROL Request Path] | リダイレクトされるページ。 リクエストパスは一意である必要があり、別のリダイレクトで使用することはできません。 リクエストパスが存在するというエラーメッセージが表示された場合は、既存のリダイレクトを削除してもう一度試してください。 |
| [!UICONTROL Target Path] | 宛先を指すためにシステムで使用される内部パス。 ターゲットパスは灰色表示になっており、編集できません。 |
| [!UICONTROL Redirect] | リダイレクトのタイプを決定します。 オプション：<br/>**いいえ** - リダイレクトは指定されません。 <br/>**[!UICONTROL Temporary (302)]**– 検索エンジンに対して、書き換えが期間限定であることを示します。 検索エンジンは通常、一時的な書き換えのページランク情報を保持しません。<br/>**[!UICONTROL Permanent (301)]** – 検索エンジンに対して、書き換えが永続的であることを示します。 検索エンジンでは通常、永続的な書き換えの際にページランク情報が保持されます。 |
| [!UICONTROL Description] | 内部参照用の書き換えの目的について説明します。 |

{style="table-layout:auto"}
