---
title: Google AdWords
description: Google AdWords コンバージョントラッキング用にコマースストアを設定して、販売や他の貴重なアクションにつながった広告クリック数を測定する方法について説明します。
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1] は、広告をGoogleの検索結果や、Googleディスプレイネットワーク内の会社のページに配置するために使用できるサービスです。 AdWords ダッシュボードには、キャンペーンの管理、反応の追跡、結果の測定をおこなうためのツールが含まれています。

コンバージョントラッキングは、販売やその他の有益なアクションにつながった広告クリック数を示します。 The _成功_ 注文が送信された後に顧客に表示されるページは、販売の後にのみ表示されるので、コンバージョンの追跡に使用されます。 ストアのGoogle AdWords 設定を完了した後は、コマースに必要な情報が既に含まれているので、コンバージョントラッキングスクリプトを成功ページにコピーする必要はありません。 詳しくは、 [Google AdWords ヘルプ][2].

![Google検索結果のAdobe広告](./assets/google-adwords-adobe-ad.png){width="500"}

## 手順 1. Google AdWords キャンペーンを作成する

1. 訪問 [Google AdWords][3]」をクリックし、アカウントに新規登録します。

1. 指示に従って、キャンペーンを作成します。

1. キャンペーンのコンバージョントラッキングを設定するには、以下の手順を実行します。

   - 次の日： **[!UICONTROL Tools]** 」タブで、 **[!UICONTROL Conversions]** をクリックします。 **[!UICONTROL Conversion]**.

   - 変換ソースの入力を求められたら、を選択します。 **[!UICONTROL Website]**.

   - 追跡するコンバージョンアクションの名前を入力し、 **[!UICONTROL Done]**.

   - クリック **[!UICONTROL Value]** 必要に応じて、値を変換に割り当てます。 例：

      - 1 回の販売で$5 を作る場合は、 `Each time it happens` を割り当て、 `$5`.
      - 各販売の値が異なる場合は、値を空白のままにします。

     完了するには、 **[!UICONTROL Done]**.

   - クリック **[!UICONTROL Conversion windows]** および設定を完了して、コンバージョンの追跡期間、レポートカテゴリおよびアトリビューションモデルを決定します。

1. 完了したら、「 **[!UICONTROL Save and Continue]**.

## 手順 2. コンバージョンタグを取得する

1. の下 **[!UICONTROL Install your tag]**、でコンバージョンをカウントすることを選択します。 **[!UICONTROL Page load]**.

1. オプションとして、 **[!UICONTROL Google Site Stats]** 変換ページへの通知を送信します。

   通知は下隅に表示され、Googleのセキュリティ標準および cookie の使用状況へのリンクが示されます。

1. AdWords タグの管理方法を選択するには、次のいずれかの操作を行います。

   - 自分でストアにスクリプトを追加する場合は、 **[!UICONTROL Save instructions and tag]**.
   - 他のユーザーにストアにスクリプトを追加させる場合は、 **[!UICONTROL Email instructions and tag]**.

1. 完了したら、「 **[!UICONTROL Done]**.

## 手順 3. ストアを設定

{{gtag-api-note}}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 特定のストア表示用にGoogle AdWords を設定する場合は、次の手順を実行します。

   - 左上隅で、 **[!UICONTROL Store View]** を設定します。

   - 範囲の切り替えを確認するメッセージが表示されたら、 **[!UICONTROL OK]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Google API]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Google AdWords]** 」セクションで次の操作を実行します。

   - 設定 **[!UICONTROL Enable]** から `Yes`.

   - 次を入力します。 **[!UICONTROL Conversion ID]** をGoogle AdWords スクリプトから削除します。

   ![セールス設定 — Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Google Sites 統計通知の形式を設定するには、次の手順を実行します。

   - 設定 **[!UICONTROL Conversion Language]** をGoogle AdWords スクリプトで識別される言語に追加します。

   - 次を入力します。 **[!UICONTROL Conversion Format]** を使用して、変換ページ上のGoogle Sites Stat の通知に使用できます。

      - `1`  - 1 行の通知とGoogleトラッキングに関する詳細情報へのリンクを表示します。
      - `2` - 2 行の通知とGoogleトラッキングに関する詳細情報へのリンクを表示します。
      - `3`  — 顧客通知を表示しません。

   - 次を入力します。 [16 進数コード][4]{:target=&quot;_blank&quot;} の **[!UICONTROL Conversion Color]** Google Site Stats 通知ラベルに使用する

   - の暗号化されたテキストを入力 **[!UICONTROL Conversion Label]** Google Sites 統計通知に表示されます。

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

1. 設定 **[!UICONTROL Conversion Value Type]** を次のいずれかに変更します。

   - `Dynamic`  — 動的な注文額の値に基づいてコンバージョンが発生したかどうかを判断します。
   - `Constant`  — 入力された特定の値に基づいてコンバージョンが発生したかどうかを判断します。

   の _定数_ コンバージョン値のタイプ、特定の **[!UICONTROL Value]** （の） _[!UICONTROL Order Amount]_を選択して、コンバージョンと見なします。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 手順 4. 設定の確認

数時間以内に、Google AdWords ダッシュボードのトラッキングステータスが `Unverified` から `No recent conversions` または `Recording conversions`. 誰かが広告をクリックして購入すると、そのコンバージョンがダッシュボードとキャンペーンレポートのコンバージョンアクションページに表示されます。

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
