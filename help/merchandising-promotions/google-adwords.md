---
title: Google AdWords
description: Google AdWords コンバージョントラッキング用にCommerce ストアを設定して、セールやその他の価値あるアクションにつながる広告クリック数を測定する方法について説明します。
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Google AdWords

[Google AdWords](https://www.google.com/adwords/) は、Googleの検索結果およびGoogle Display Network 内の企業のページに広告を掲載する際に使用できるサービスです。 AdWords ダッシュボードには、キャンペーンの管理、応答の追跡、結果の測定を行うためのツールが含まれています。

コンバージョントラッキングは、販売またはその他の価値のあるアクションにつながる広告クリック数を表示します。 注文送信後に顧客に表示される _成功_ ページは、販売後にのみ表示されるので、コンバージョンを追跡するために使用されます。 Commerceには既に必要な情報があるので、ストアのGoogle AdWords 設定が完了したら、コンバージョントラッキングスクリプトを成功ページにコピーする必要はありません。 詳しくは、[Google AdWords ヘルプ ](https://support.google.com/adwords/answer/6095821) を参照してください。

![Google検索結果のAdobe広告 ](./assets/google-adwords-adobe-ad.png){width="500"}

## 手順 1. Google AdWords キャンペーンの作成

1. [Google AdWords](https://ads.google.com/) にアクセスして、アカウントに新規登録します。

1. 手順に従ってキャンペーンを作成します。

1. キャンペーンのコンバージョントラッキングを設定するには、以下の手順を実行します。

   - AdWords ダッシュボードの「**[!UICONTROL Tools]**」タブで、「**[!UICONTROL Conversions]**」を選択し、「**[!UICONTROL Conversion]**」をクリックします。

   - 変換ソースの入力を求められたら、「**[!UICONTROL Website]**」を選択します。

   - 追跡するコンバージョンアクションの名前を入力し、「**[!UICONTROL Done]**」をクリックします。

   - 「**[!UICONTROL Value]**」をクリックし、該当する場合はコンバージョンに値を割り当てます。 例：

      - 各販売で$5 を稼ぐ場合は、`Each time it happens` を選択し、`$5` の値を割り当てます。
      - 各販売の値が異なる場合は、値を空白のままにします。

     完了するには、「**[!UICONTROL Done]**」をクリックします。

   - 「**[!UICONTROL Conversion windows]**」をクリックして設定を完了し、コンバージョンを追跡する期間、レポートカテゴリおよび属性モデルを決定します。

1. 完了したら、「**[!UICONTROL Save and Continue]**」をクリックします。

## 手順 2. コンバージョンタグを取得

1. 「**[!UICONTROL Install your tag]**」で、「**[!UICONTROL Page load]** でコンバージョンをカウント」を選択します。

1. オプションとして、コンバージョンページに **[!UICONTROL Google Site Stats]** 通知を追加できます。

   通知は、Googleのセキュリティ標準と cookie の使用へのリンクと共に下隅に表示されます。

1. AdWords タグの管理方法を選択するには、次のいずれかの操作を行います。

   - スクリプトを自分でストアに追加する場合は、「**[!UICONTROL Save instructions and tag]**」を選択します。
   - 他のユーザーにストアにスクリプトを追加してもらう予定がある場合は、「**[!UICONTROL Email instructions and tag]**」を選択します。

1. 完了したら、「**[!UICONTROL Done]**」をクリックします。

## 手順 3. ストアの設定

{{gtag-api-note}}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 特定のストア表示用にGoogle AdWords を設定する場合は、次の操作を行います。

   - 左上隅で、設定する **[!UICONTROL Store View]** を選択します。

   - 範囲の切り替えを確認するプロンプトが表示されたら、「**[!UICONTROL OK]**」をクリックします。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Google API]**」を選択します。

1. ![ のセクションの ](../assets/icon-display-expand.png) 展開セレクター **[!UICONTROL Google AdWords]** を展開し、以下を実行します。

   - **[!UICONTROL Enable]** を `Yes` に設定します。

   - Google AdWords スクリプトから **[!UICONTROL Conversion ID]** を入力します。

   ![Sales configuration - Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Google Sites の Stat 通知をフォーマットするには、次の手順を実行します。

   - Google AdWords スクリプトで識別される言語に **[!UICONTROL Conversion Language]** を設定します。

   - コンバージョンページでGoogle Sites の Stat 通知に使用する **[!UICONTROL Conversion Format]** を入力します。

      - `1` - Googleのトラッキングに関する詳細情報へのリンクを含む 1 行通知を表示します。
      - `2` - Googleのトラッキングに関する詳細情報へのリンクを含む 2 行の通知が表示されます。
      - `3` – 顧客通知を表示しません。

   - Google Site Stats の通知ラベルに使用する [ の ](https://www.w3schools.com/colors/colors_picker.asp){:target="_blank"}16 進コード **[!UICONTROL Conversion Color]** を入力します。

   - Google サイトの状況通知に表示される **[!UICONTROL Conversion Label]** の暗号化テキストを入力します。

     例：`MlEYCOKBnGoQz6CZoAM`

     **Google AdWords タグコードのサンプル**

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

1. **[!UICONTROL Conversion Value Type]** を次のいずれかに設定します。

   - `Dynamic` – 動的な注文金額の値に基づいてコンバージョンが発生したことを判断します。
   - `Constant` – 入力された特定の値に基づいてコンバージョンが発生したことを判別します。

   _定数_ のコンバージョン値の種類には、コンバージョンと見なされる **[!UICONTROL Value]** の特定の _[!UICONTROL Order Amount]_を入力します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 手順 4. 設定の確認

数時間以内に、Google AdWords ダッシュボードのトラッキングステータスが `Unverified` から `No recent conversions` または `Recording conversions` に変わります。 誰かが広告をクリックして購入すると、そのコンバージョンがダッシュボードおよびキャンペーンレポートの「コンバージョンアクション」ページに表示されます。
