---
title: Google AdWords
description: Google AdWords コンバージョン トラッキング用にCommerce ストアを設定して、セールやその他の価値のあるアクションにつながる広告クリックを測定する方法を説明します。
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# Google AdWords

[Google AdWords](https://www.google.com/adwords/)は、Googleの検索結果やGoogle ディスプレイ ネットワークの企業ページに広告を配置するために使用できるサービスです。 AdWords ダッシュボードには、キャンペーンの管理、レスポンスの追跡、結果の測定を行うためのツールが含まれています。

コンバージョン追跡は、売上やその他の価値あるアクションにつながる広告のクリック数を示します。 注文が送信された後に顧客に表示される&#x200B;_成功_ ページは、販売後にのみ表示されるため、コンバージョンの追跡に使用されます。 ストアのGoogle AdWords設定を完了した後、Commerceには必要な情報が既に用意されているため、コンバージョントラッキングスクリプトをSuccess ページにコピーする必要はありません。 詳しくは、[Google AdWords ヘルプ &#x200B;](https://support.google.com/adwords/answer/6095821)を参照してください。

![Googleの検索結果のAdobe広告](./assets/google-adwords-adobe-ad.png){width="500"}

## 手順1: Google AdWords キャンペーンの作成

1. [Google AdWords](https://ads.google.com/)にアクセスして、アカウントにサインアップしてください。

1. 手順に従ってキャンペーンを作成します。

1. キャンペーンのコンバージョントラッキングを設定するには、次の操作を行います。

   - AdWords ダッシュボードの&#x200B;**[!UICONTROL Tools]** タブで、**[!UICONTROL Conversions]**&#x200B;を選択し、**[!UICONTROL Conversion]**&#x200B;をクリックします。

   - コンバージョンソースの入力を求められたら、**[!UICONTROL Website]**&#x200B;を選択します。

   - 追跡する変換アクションの名前を入力し、**[!UICONTROL Done]**&#x200B;をクリックします。

   - **[!UICONTROL Value]**&#x200B;をクリックし、該当する場合は、コンバージョンに値を割り当てます。 例：

      - 各販売で$5を行う場合は、`Each time it happens`を選択し、値`$5`を割り当てます。
      - 各販売の値が異なる場合は、値を空白のままにします。

     完了するには、**[!UICONTROL Done]**&#x200B;をクリックします。

   - **[!UICONTROL Conversion windows]**&#x200B;をクリックし、設定を完了して、コンバージョンを追跡する期間、レポートカテゴリ、アトリビューションモデルを決定します。

1. 完了したら、**[!UICONTROL Save and Continue]**&#x200B;をクリックします。

## 手順2: コンバージョンタグを入手

1. **[!UICONTROL Install your tag]**&#x200B;で、**[!UICONTROL Page load]**&#x200B;のコンバージョンをカウントすることを選択します。

1. オプションとして、**[!UICONTROL Google Site Stats]**&#x200B;通知をコンバージョンページに追加できます。

   通知は下隅に表示され、Googleのセキュリティ標準とCookieの使用状況へのリンクが表示されます。

1. AdWords タグの管理方法を選択するには、次のいずれかの操作を行います。

   - スクリプトを自分のストアに追加する場合は、**[!UICONTROL Save instructions and tag]**&#x200B;を選択します。
   - 他のユーザーにスクリプトをストアに追加してもらう場合は、**[!UICONTROL Email instructions and tag]**&#x200B;を選択します。

1. 完了したら、**[!UICONTROL Done]**&#x200B;をクリックします。

## 手順3: ストアの設定

{{gtag-api-note}}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. Google AdWordsを特定のストアビューに設定する場合は、次の操作を行います。

   - 左上隅で、設定する&#x200B;**[!UICONTROL Store View]**&#x200B;を選択します。

   - 範囲の切り替えを確認するメッセージが表示されたら、**[!UICONTROL OK]**&#x200B;をクリックします。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Google API]**&#x200B;を選択します。

1. **[!UICONTROL Google AdWords]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - **[!UICONTROL Enable]**&#x200B;を`Yes`に設定します。

   - Google AdWords スクリプトから&#x200B;**[!UICONTROL Conversion ID]**&#x200B;を入力します。

   ![営業設定 – Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Google Sitesの統計通知を書式設定するには、次の操作を行います。

   - Google AdWords スクリプトで識別される言語に&#x200B;**[!UICONTROL Conversion Language]**&#x200B;を設定します。

   - コンバージョンページのGoogle Sitesのステータス通知に使用する&#x200B;**[!UICONTROL Conversion Format]**&#x200B;を入力します。

      - `1` - Google トラッキングの詳細へのリンクを含む1行の通知を表示します。
      - `2` - Google トラッキングの詳細へのリンクを含む2行の通知を表示します。
      - `3` – 顧客の通知を表示しません。

   - Google サイト統計の通知ラベルに使用する&#x200B;**[!UICONTROL Conversion Color]**&#x200B;の[16進数コード &#x200B;](https://www.w3schools.com/colors/colors_picker.asp){:target="_blank"}を入力します。

   - Google Sitesのステータス通知に表示される&#x200B;**[!UICONTROL Conversion Label]**&#x200B;の暗号化されたテキストを入力します。

     例：`MlEYCOKBnGoQz6CZoAM`

     **Google AdWords タグ コードの例**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. **[!UICONTROL Conversion Value Type]**&#x200B;を次のいずれかに設定します：

   - `Dynamic` – 動的な注文金額の値に基づいてコンバージョンが発生したことを確認します。
   - `Constant` – 入力された特定の値に基づいてコンバージョンが発生したことを判別します。

   _定数_&#x200B;のコンバージョン値タイプの場合は、_[!UICONTROL Order Amount]_&#x200B;の特定の&#x200B;**[!UICONTROL Value]**&#x200B;を入力して、コンバージョンとして認定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## 手順4: 設定の確認

数時間以内に、Google AdWords ダッシュボードのトラッキングステータスが`Unverified`から`No recent conversions`または`Recording conversions`に変わります。 誰かが広告をクリックして購入すると、ダッシュボードとキャンペーンレポートのコンバージョンアクションページにコンバージョンが表示されます。
