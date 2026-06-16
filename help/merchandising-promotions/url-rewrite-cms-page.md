---
title: コンテンツページ URLの書き換え
description: コンテンツページ URLの書き換えを使用して、Commerce ストア内の別のコンテンツページのURLにリンクをリダイレクトする方法を説明します。
exl-id: e29c45fd-cf25-4b51-a8ae-9e188dc2a61c
feature: Page Content, Configuration
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/qqavUzi-GFdvuM5YhKm0sxXHnJOJAX4fMvFDqZrM89A
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 634
ht-degree: 0%

---

# コンテンツページ URLの書き換え

始める前に、リダイレクトが何を達成するのかを正確に理解していることを確認してください。 _target_ / _source_&#x200B;または&#x200B;_リダイレクト先_ / _リダイレクト先_&#x200B;を考えてみましょう。 人々は、検索エンジンや古いリンクから以前のページに移動する可能性はありますが、このリダイレクトにより、ストアは新しいターゲットに切り替わります。

![URLの書き換え – CMS ページ &#x200B;](./assets/url-rewrite-cms-page.png){width="700" zoomable="yes"}

## 手順1: 書き換えの計画

間違いを避けるには、_リダイレクト先_ ページと&#x200B;_リダイレクト先_ ページのURL キーを書き留めます。

不明な場合は、ストアの各ページを開き、ブラウザーのアドレスバーからパスをコピーします。

### CMS ページパス

次にリダイレクト：`new-page`

`old-page`からリダイレクト

## 手順2: 書き換えを作成

{{url-rewrite-params}}

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**&#x200B;に移動します。

1. 続行する前に、次の手順を実行して、リクエストパスが使用可能であることを確認します。

   - **[!UICONTROL Request Path]**&#x200B;列の上部にある検索フィルターで、リダイレクトするページのURL キーを入力し、**[!UICONTROL Search]**&#x200B;をクリックします。

   - ページに複数のリダイレクトレコードがある場合は、該当するストアビューに一致するレコードを見つけて、編集モードで開きます。

   - 右上隅の「**[!UICONTROL Delete]**」をクリックします。 プロンプトが表示されたら、**[!UICONTROL OK]**&#x200B;をクリックして確認します。

1. URL書き換えページに戻ったら、**[!UICONTROL Add URL Rewrite]**&#x200B;をクリックします。

1. **[!UICONTROL Create URL Rewrite]**&#x200B;を`for CMS page`に設定します。

1. グリッドで新しいターゲットページを見つけ、編集モードで開きます。

   ![CMS ページのURL書き換えを追加](./assets/url-rewrite-cms-page-add.png){width="700" zoomable="yes"}

1. 「URL書き換え情報」で、次の操作を行います。

   - 複数のストアビューがある場合は、書き換えが適用される&#x200B;**[!UICONTROL Store]**&#x200B;を選択します。

   - **[!UICONTROL Request Path]**&#x200B;に、顧客がリクエストした元のページのURL キーを入力します。 これは、_ページからの_ リダイレクトです。

     >[!NOTE]
     >
     >リクエストパスは、指定されたストアに対して一意である必要があります。 同じリクエストパスを使用するリダイレクトが既に存在する場合、リダイレクトを保存しようとするとエラーが表示されます。 前のリダイレクトは、作成する前に削除する必要があります。

   - **[!UICONTROL Redirect]**&#x200B;を次のいずれかに設定します：

      - `Temporary (302)`
      - `Permanent (301)`

   - 参照用に、書き換えの簡単な説明を入力します。

   ![URL書き換え情報](./assets/url-rewrite-cms-page-information.png){width="600" zoomable="yes"}

1. リダイレクトを保存する前に、次の点を確認してください。

   - 左上隅のリンクには、ターゲットページの名前が表示されます。
   - リクエストパスには、元の&#x200B;_ページからの_ リダイレクトのパスが含まれます。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   新しい書き換えは、リストの上部にあるグリッドに表示されます。

## 手順3: 結果のテスト

1. ストアのホームページに移動します。

1. 次のいずれかの操作を行います。

   - 元の&#x200B;_ページから_ リダイレクトに移動します。
   - ブラウザーのアドレスバーで、ストア URLの直後に元の&#x200B;_リダイレクト元_ ページの名前を入力し、**Enter**&#x200B;を押します。

   元のページリクエストの代わりに、新しいターゲットページが表示されます。

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 書き換えの種類を示します。 書き換え作成後にタイプを変更することはできません。 オプション：`Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | リダイレクトするCMS ページ。 リクエストパスは一意である必要があり、別のリダイレクトで使用することはできません。 リクエストパスが存在するというエラーメッセージが表示された場合は、既存のリダイレクトを削除して、もう一度試してください。 |
| [!UICONTROL Target Path] | システムが宛先を指すために使用する内部パス。 ターゲットパスはグレー表示され、編集できません。 |
| [!UICONTROL Redirect] | リダイレクトのタイプを指定します。 オプション：<br/>**[!UICONTROL No]**- リダイレクトが指定されていません。<br/>**[!UICONTROL Temporary (302)]** – 書き換えが期間限定であることを検索エンジンに示します。 検索エンジンは通常、一時的な書き換え用のページランク情報を保持しません。<br/>**[!UICONTROL Permanent (301)]**– 書き換えが永続的であることを検索エンジンに示します。 検索エンジンは、通常、永続的な書き換えに使用するページランク情報を保持します。 |
| [!UICONTROL Description] | 内部参照用に書き換える目的を説明します。 |

{style="table-layout:auto"}
