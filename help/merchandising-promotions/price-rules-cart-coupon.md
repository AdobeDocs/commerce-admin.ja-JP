---
title: クーポンコード
description: 買い物かごの価格ルールでクーポンコードを使用して、一連の条件を満たした場合に割引を適用する方法を説明します。
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 7407df02ca62e36b4dd60dba418eae3e6aa34491
workflow-type: tm+mt
source-wordcount: '1839'
ht-degree: 0%

---

# クーポンコード

クーポンコードはで使用されます [買い物かご価格ルール](price-rules-cart.md) 一連の条件を満たした場合に割引を適用する。 例えば、特定の顧客グループ向けに、または特定の金額を超えて購入するユーザー向けに、クーポンコードを作成できます。 クーポンを購入に適用するには、お客様はカートにクーポンコードを入力するか、場合によってはあなたのレジでクーポンコードを入力することができます _れんがとモルタル_ ストア。 ストアでクーポンを使用する方法はいくつかあります。

- 顧客へのメールクーポン
- 印刷されたクーポンを作成する
- モバイルユーザー用の店舗内クーポンの作成

クーポンコードは、メールで送信することも、ニュースレター、カタログ、広告に含めることもできます。 クーポンコードのリストをエクスポートして、商用プリンターに送信できます。 また、買い物客がスマートフォンでスキャンできるクイックレスポンスコードを含んだ店舗内クーポンを作成することもできます。 QR コードは、プロモーションに関する詳細を含むサイトのページにリンクできます。

Commerce 2.4.7 以降、買い物客は 1 つの買い物かごに複数のクーポンを適用できます。 マーチャントは、買い物の支援を使用して複数のクーポンを適用することもできます。

## クーポンコードの設定

自動生成されたクーポンコードの長さと形式は、この構成によって制御されます。 文字は、すべての数字、すべての文字、またはそれらの組み合わせに設定できます。 設定した間隔でダッシュを挿入して読みやすくしたり、プレフィックスとサフィックスを追加してコードを特定のキャンペーンやイニシアチブに関連付けたりできます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Promotions]**.

   ![顧客設定 – 自動生成された特定のクーポンコード](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. を展開します。 **[!UICONTROL Auto Generated Specific Coupon Codes]** セクション。

   ![顧客設定 – 自動生成された特定のクーポンコード](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. を入力 **[!UICONTROL Code Length]**（プレフィックス、サフィックス、区切り文字を含む）。

1. を **[!UICONTROL Code Format]** を次のいずれかに変更します。

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. の場合 **[!UICONTROL Code Prefix]**&#x200B;すべてのクーポンコードの先頭に表示する値を入力します。

1. の場合 **[!UICONTROL Code Suffix]**&#x200B;すべてのクーポンコードの末尾に表示する値を入力します。

1. の場合 **[!UICONTROL Dash Every X Characters]**&#x200B;を入力し、各ダッシュの間の文字数を入力します。

   異なるダッシュパターンを持つクーポンコードは、番号が同じであっても、異なるコードと見なされます。

1. 完了したら、 **[!UICONTROL Save Config]**.

## クーポンの作成

>[!NOTE]
>
>クーポンを作成する前に、 `bin/magento cron:run` cron が実行中であることを確認するコマンド。 参照： [コマンドラインから cron を実行します](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) が含まれる _設定ガイド_ を参照してください。

### 方法 1：特定のクーポンの作成

1. 手順に従ってを作成します [買い物かご価格ルール](price-rules-cart.md).

1. が含まれる **[!UICONTROL Rule Information]** セクション、設定 **[!UICONTROL Coupon]** 対象： `Specific Coupon`.

1. を入力 **[!UICONTROL Coupon Code]** プロモーションで使用されます。

   コードの形式（数値、英数字またはアルファベット）は、 [設定](#configure-coupon-codes).

1. クーポンの使用回数を制限するには、次の操作を行います。

   - 次の数を入力 **[!UICONTROL Uses per Coupon]**.
   - 次の数を入力 **[!UICONTROL Uses per Customer]**.

   無制限に使用するには、これらのフィールドを空白のままにします。

   ![買い物かご価格ルール – クーポン情報](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >複数の顧客が同時に同じクーポンを使用している場合、クーポン処理の遅延により、設定されている使用制限を超える可能性があります。

1. クーポンを一定期間有効にするには、次の操作を行います。

   - ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）次を完了します **送信元** および **終了** 日付。 日付を選択するには、 **カレンダー** （![カレンダーアイコン](../assets/icon-calendar.png)）アイコンをクリックします。 日付範囲を空のままにすると、ルールは期限切れになりません。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）次のいずれかの操作をおこないます。

     **オプション 1:** 新しい更新をスケジュール

      - クリック **[!UICONTROL Schedule New Update]** をページの右上隅に表示します。

        ![更新をスケジュール](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - を入力 **[!UICONTROL Update Name]** および **[!UICONTROL Description]**.

      - を選択します。 **開始日** および **[!UICONTROL End Date]** カレンダー（ ![カレンダーアイコン](../assets/icon-calendar.png) ）に設定します。 日付範囲を空のままにすると、ルールは期限切れになりません。

      - 完了したら、 **[!UICONTROL Save]**.

        ![買い物かご価格ルール – 予定された変更](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **オプション 2:** 既存の更新プログラムに割り当てる：

      - を選択 **[!UICONTROL Assign to Another Update]**.

      - リストで更新を探し、をクリックします **[!UICONTROL Select]**.

1. を完了する [買い物かご価格ルール](price-rules-cart.md) 必要に応じて。

### 方法 2：クーポンのバッチを生成する

割引クーポンの生成は非同期操作であり、バックグラウンドで実行されるので、操作が完了するのを待たずに管理者で作業を続行できます。 タスクが完了すると、メッセージが表示されます。

1. 手順に従ってを作成します [買い物かご価格ルール](price-rules-cart.md).

1. 次の下 **[!UICONTROL Coupon Code]**&#x200B;を選択し、 **[!UICONTROL Use Auto Generation]** チェックボックス。

1. 各顧客がクーポンを使用できる回数を制限するには、次の数を入力します **[!UICONTROL Uses per Customer]**.

   ![買い物かご価格ルール – 自動番号クーポンを生成します](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >複数の顧客が同時に同じクーポンを使用している場合、クーポン処理の遅延により、設定されている使用制限を超える可能性があります。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Manage Coupon Codes]** を選択し、次の操作を実行します。

   ![買い物かご価格ルール – クーポンコードの管理](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - の場合 **[!UICONTROL Coupons Qty]**：生成するクーポンの数を入力します。

   - を入力 **[!UICONTROL Code Length]**&#x200B;プレフィックス、サフィックス、区切り文字は含めません。

   - を **[!UICONTROL Code Format]** を次のいずれかに変更します。

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - （任意） a と入力します **[!UICONTROL Code Prefix]** コードの先頭に追加されます。

   - （任意） a と入力します **[!UICONTROL Code Suffix]** コードの最後に追加されます。

   - （オプション） **[!UICONTROL Dash Every X Characters]**&#x200B;を入力し、各ダッシュの間の文字数を入力します。 例えば、コードの長さが 12 文字で、4 文字ごとにダッシュがある場合は、次のようになります `xxxx-xxxx-xxxx`. 点線を使用すると、コードを読みやすく、入力しやすくなります。

1. 完了したら、 **[!UICONTROL Generate]**.

   システムに次が表示されます `Message is added to queue, wait to get your coupons soon`.

   Cron ジョブが完了すると、生成されたコードのリストが表示されます。

   | フィールド | 説明 |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | 作成され、特別な条件を受け取るために使用できるクーポンコード。 |
   | [!UICONTROL Created] | クーポンコードが作成された日付。 |
   | [!UICONTROL Used] | クーポンが使用されたかどうかを示します。 |
   | [!UICONTROL Times Used] | クーポンコードが使用された回数を示します。 |

   {style="table-layout:auto"}

クーポンコードを CSV または Excel XML ファイルにエクスポートするには、ファイル形式を選択し、をクリックします **[!UICONTROL Export]**.

クーポンコードを削除するには、リストから 1 つ以上のコードを選択します。 を選択 `Delete` から **[!UICONTROL Actions]**  セレクターを選択し、 **[!UICONTROL Submit]**.

>[!NOTE]
>
>Commerce では複数のクーポンコードを設定できますが、顧客が買い物かごで使用できるクーポンコードは 1 つだけです。 カート内の複数のクーポンコードを同時に使用できるようにするには、から対応する拡張機能の使用を検討します [Commerce Marketplace](https://marketplace.magento.com/).

## クーポンレポート

この _クーポン_ レポートは、特定の日付範囲内で使用される各クーポンからデータを集計します。 クーポンは買い物かごから適用されるので、レポートには、に関係なく、引き換えられるすべてのクーポンのデータが含まれます [注文ステータス](../stores-purchase/order-status.md). その結果、レポートには見込み合計と実際の合計の両方が含まれる場合があります。 レポートは、特定のストア表示、期間、注文ステータス、買い物かご価格ルールに合わせてフィルタリングできます。

次の例では、クーポンコード「H20」を 2 人の顧客が使用しています。 注文の 1 つが請求されていますが、もう 1 つはまだ残っています _保留中_. 見込み売上小計、売上割引、および売上合計の列には、両方の注文の集計金額が表示されますが、小計、割引、および合計の列には、実際の請求済み注文のみが表示されます。 レポートの各行は、1 つのクーポンプロモーションを表します。

![クーポンレポート](./assets/reports-coupons.png){width="600" zoomable="yes"}

### レポートの実行

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. 複数のストア表示がある場合、を設定します **[!DNL Store View]** 左上隅のをクリックして、レポートの範囲を確定します。

1. 売上をリフレッシュする手順は、次のとおりです。 [statistics](../getting-started/sales-reports.md#refresh-statistics) その日に対して、 _最終更新日_ ワークスペースの上部にあるメッセージ。

   次に、をクリックして選択します **[!UICONTROL Coupons]** チェックボックスをオンにして、 **[!UICONTROL Refresh]**.

   ![クーポンレポート – 統計の更新](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. データをフィルターするには、次の手順を実行します。

   ![クーポンレポート – フィルター](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Date Used]** を次のいずれかに変更します。

      - `Order Created`
      - `Order Updated`

     この _注文が更新されました_ レポートはリアルタイムで作成され、更新の必要はありません。

   - レポートの対象期間を定義するには、次のように設定します **[!UICONTROL Period]** を次のいずれかに変更します。

      - `Day`
      - `Month`
      - `Year`

   - レポートの日付範囲を定義するには、 **送信元** および **終了** m/D/YY 形式の日付。

   - 特定のレポートを印刷するには [注文ステータス](../stores-purchase/order-status.md)、設定 **[!UICONTROL Order Status]** 対象： `Specified` リストから注文ステータスを選択します。

   - レポートからデータのない行を省略するには、次のように設定します **[!UICONTROL Empty Rows]** 対象： `No`.

   - レポートに含まれるクーポンアクティビティを定義するには、次のいずれかの操作を行います。

      - すべての価格ルールからすべてのクーポン・アクティビティを含めるには、次のように設定します **[!UICONTROL Cart Price Rule]** 対象： `Any`.
      - 特定の価格ルールに関連するアクティビティのみを含めるには、次のように設定します **[!UICONTROL Cart Price Rule]** 対象： `Specified` リストで買い物かご価格ルールを選択します。

1. レポートを実行する準備ができたら、 **[!UICONTROL Show Report]**.

   レポートがページの下部に表示されます。

### フィルターオプション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Date Used] | レポートの基礎として使用される日付フィールドを識別します。 オプション：<br/>**[!UICONTROL Order Created]**：顧客による注文日に基づいてレポートを生成します。 最新のデータが含まれていることを確認するには、メッセージ内のリンクをクリックして統計を更新します。<br/>**[!UICONTROL Order Updated]**：注文が最後に更新された日付に基づいてレポートを生成します。 このレポートは、リアルタイムデータを使用するので、統計を更新する必要はありません。 |
| [!UICONTROL Period] | レポートに使用する日付範囲のタイプを決定します。 オプション： `Day` / `Month` / `Year` |
| [!UICONTROL From] | レポートに含まれる注文データ範囲の最初の日付を示します。 |
| [!UICONTROL To] | レポートに含まれる注文データの範囲の最終日を示します。 |
| [!UICONTROL Order Status] | 注文ステータスでレポートをフィルタリングします。 レポートは、すべての注文に対して生成することも、特定の注文ステータスに制限することもできます。 オプション： <br/>**[!UICONTROL Any]**：ステータスに関係なく、すべての注文が含まれます。<br/>**[!UICONTROL Specified]**：指定されたステータスの注文のみを含めます。 キャンセルされた注文はレポートに含まれません。 |
| [!UICONTROL Empty Rows] | 取得される可能性のある空のデータ行がレポートに含まれているかどうかを判断します。 オプション： `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | レポートに含めるクーポンプロモーションを決定します。 オプション：<br/>**[!UICONTROL Any]**：指定した日付範囲内に使用されたクーポンプロモーションに関する注文情報が含まれます。<br/>**[!UICONTROL Specified]**：選択したクーポンプロモーションに関する、指定した日付範囲の注文情報のみを含めます。 |

{style="table-layout:auto"}

### レポート列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Interval] | レポートに含めるクーポン使用の日付範囲を示します。 間隔には、特定の日、月、年、または日付の範囲を指定できます。 間隔の日付は、に設定された値に応じて、次の例のようにフォーマットされます。 **[!UICONTROL Period]** 設定：<br/>`Day`: 6/21/19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | 買い物かごに顧客が入力して割引を受ける割引コード。 |
| [!UICONTROL Price Rule] | クーポンに関連付けられている価格ルールの名前。 |
| [!UICONTROL Uses] | レポートに指定された日付範囲でクーポンが使用された回数。 |
| [!UICONTROL Sales Subtotal] | クーポンで行われたすべての注文の予測小計。 <br/>Sales Subtotal は、対象となるすべてのオーダーから集計された Subtotal を表し、次の情報が含まれます `Pending` まだ請求されていない販売注文。 |
| [!UICONTROL Sales Discount] | クーポンで行われたすべての注文の予測割引金額。 <br/>割引は、対象となるすべての注文の集計割引額を表し、次のものが含まれます `Pending` まだ請求されていない販売注文。 |
| [!UICONTROL Sales Total] | クーポンで行われたすべての注文から予測される総計。 売上合計には、送料と手数料から割引額を差し引いた金額が含まれます。 <br/>売上合計は、対象となるすべての注文の総計の集計値を表し、次の金額が含まれます `Pending` まだ請求されていない販売注文。 値には、小計に配送料と手数料を加えた値から、ディスカウントと税金を差し引いた値が含まれます。 <br/> 集計基準： `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | クーポンを使用したすべての請求済み注文から集計された小計。 |
| [!UICONTROL Discount] | クーポンを使用したすべての請求済み注文からの集計割引。 |
| [!UICONTROL Total] | クーポンを使用したすべての請求済み注文の集計注文合計。 |

{style="table-layout:auto"}
