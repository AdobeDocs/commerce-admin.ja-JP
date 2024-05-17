---
title: Google AdWords
description: Google AdWords コンバージョントラッキング用にCommerce ストアを設定して、セールやその他の価値あるアクションにつながる広告クリック数を測定する方法について説明します。
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1] は、Google検索結果や、Google Display Network 内の企業のページに広告を配置するために使用できるサービスです。 AdWords ダッシュボードには、キャンペーンの管理、応答の追跡、結果の測定を行うためのツールが含まれています。

コンバージョントラッキングは、販売またはその他の価値のあるアクションにつながる広告クリック数を表示します。 この _成功_ 注文送信後に顧客に表示されるページは、販売後にのみ表示されるので、コンバージョンを追跡するために使用されます。 Commerceには既に必要な情報があるので、ストアのGoogle AdWords 設定が完了したら、コンバージョントラッキングスクリプトを成功ページにコピーする必要はありません。 詳しくは、 [Google AdWords ヘルプ][2].

![Google検索結果のAdobe広告](./assets/google-adwords-adobe-ad.png){width="500"}

## 手順 1. Google AdWords キャンペーンの作成

1. 訪問 [Google AdWords][3]、およびアカウントに新規登録します。

1. 手順に従ってキャンペーンを作成します。

1. キャンペーンのコンバージョントラッキングを設定するには、以下の手順を実行します。

   - 日 **[!UICONTROL Tools]** タブをクリックし、AdWords ダッシュボードで **[!UICONTROL Conversions]** をクリックして、 **[!UICONTROL Conversion]**.

   - 変換ソースの入力を求められたら、次を選択します **[!UICONTROL Website]**.

   - 追跡するコンバージョンアクションの名前を入力し、クリックします **[!UICONTROL Done]**.

   - クリック **[!UICONTROL Value]** また、該当する場合は、値をコンバージョンに割り当てます。 例：

      - 各セールで 5 ドルを稼ぐ場合は、次のいずれかを選択します `Each time it happens` およびの値を割り当てます。 `$5`.
      - 各販売の値が異なる場合は、値を空白のままにします。

     完了するには、 **[!UICONTROL Done]**.

   - クリック **[!UICONTROL Conversion windows]** 設定を完了して、コンバージョンを追跡する期間、レポートカテゴリおよび属性モデルを決定します。

1. 完了したら、 **[!UICONTROL Save and Continue]**.

## 手順 2. コンバージョンタグを取得

1. 次の下 **[!UICONTROL Install your tag]**、コンバージョン数のカウントを選択 **[!UICONTROL Page load]**.

1. オプションとして、を追加できます **[!UICONTROL Google Site Stats]** コンバージョンページに対する通知。

   通知は、Googleのセキュリティ標準と cookie の使用へのリンクと共に下隅に表示されます。

1. AdWords タグの管理方法を選択するには、次のいずれかの操作を行います。

   - スクリプトを自分でストアに追加する場合は、次を選択します **[!UICONTROL Save instructions and tag]**.
   - 他のユーザーにストアにスクリプトを追加してもらう予定がある場合は、次を選択します **[!UICONTROL Email instructions and tag]**.

1. 完了したら、 **[!UICONTROL Done]**.

## 手順 3. ストアの設定

{{gtag-api-note}}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 特定のストア表示用にGoogle AdWords を設定する場合は、次の操作を行います。

   - 左上隅のを選択します **[!UICONTROL Store View]** この設定は必須です。

   - 範囲の切り替えを確認するプロンプトが表示されたら、 **[!UICONTROL OK]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Google API]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Google AdWords]** を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Enable]** 対象： `Yes`.

   - を入力 **[!UICONTROL Conversion ID]** Google AdWords スクリプトから。

   ![Sales configuration - Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Google Sites の Stat 通知をフォーマットするには、次の手順を実行します。

   - を設定 **[!UICONTROL Conversion Language]** をGoogle AdWords スクリプトで識別される言語に変更します。

   - を入力 **[!UICONTROL Conversion Format]** 変換用ページのGoogle サイトの Stat 通知に使用されます。

      - `1`  - Googleのトラッキングに関する詳細情報へのリンクを含む単行通知を表示します。
      - `2` - Googleのトラッキングに関する詳細情報へのリンクを含む 2 行の通知を表示します。
      - `3`  – 顧客通知が表示されません。

   - を入力 [16 進コード][4]例：{:target=&quot;_blank&quot;} **[!UICONTROL Conversion Color]** Googleのサイト統計の通知ラベルに使用する。

   - の暗号化テキストを入力 **[!UICONTROL Conversion Label]** Google サイトの状況通知に表示されます。

     例： `MlEYCOKBnGoQz6CZoAM`

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

1. を設定 **[!UICONTROL Conversion Value Type]** を次のいずれかに変更します。

   - `Dynamic`  – 動的な注文金額の値に基づいてコンバージョンが発生したことを判断します。
   - `Constant`  – 入力された特定の値に基づいて、コンバージョンが発生したことを判別します。

   の場合 _定数_ コンバージョン値のタイプ、特定のを入力します **[!UICONTROL Value]** の場合 _[!UICONTROL Order Amount]_をコンバージョンと見なします。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 手順 4. 設定の確認

数時間以内に、Google AdWords ダッシュボードのトラッキングステータスが次のように変更されます `Unverified` 対象： `No recent conversions` または `Recording conversions`. 誰かが広告をクリックして購入すると、そのコンバージョンがダッシュボードおよびキャンペーンレポートの「コンバージョンアクション」ページに表示されます。

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
