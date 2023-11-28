---
title: クーポンコード
description: 一連の条件が満たされた場合に割引を適用するための買い物かごの価格ルールでクーポンコードを使用する方法を説明します。
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 0%

---

# クーポンコード

クーポンコードは、 [買い物かご価格ルール](price-rules-cart.md) ：一連の条件が満たされたときに割引を適用します。 例えば、特定の顧客グループや、一定金額で購入したすべてのユーザー向けにクーポンコードを作成できます。 クーポンを購入に適用するには、顧客は、買い物かごにクーポンコードを入力できます。また、場合によっては、 _れんがとモルタル_ ストア。 ストアでクーポンを使用する方法を次に示します。

- 顧客へのクーポンの電子メール送信
- 印刷されたクーポンの作成
- モバイルユーザー向けのストア内クーポンの作成

クーポンコードは、電子メールで送信したり、ニュースレター、カタログ、広告に含めたりできます。 クーポンコードのリストは、書き出して商用プリンターに送信できます。 また、買い物客がスマートフォンでスキャンできるクイックレスポンスコードを使用して、店舗内クーポンを作成することもできます。 QR コードは、プロモーションの詳細情報と共に、サイト上のページにリンクできます。

## クーポンコードの設定

自動的に生成されるクーポンコードの長さと形式は、設定で制御します。 文字は、すべての数字、すべての文字、または組み合わせに設定できます。 設定した間隔でダッシュを挿入して読みやすくし、プレフィックスとサフィックスを追加して、コードを特定のキャンペーンまたはイニシアチブに関連付けることができます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Promotions]**.

   ![顧客設定 — 自動生成された特定のクーポンコード](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. を展開します。 **[!UICONTROL Auto Generated Specific Coupon Codes]** 」セクションに入力します。

   ![顧客設定 — 自動生成された特定のクーポンコード](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. 次を入力します。 **[!UICONTROL Code Length]**（プレフィックス、サフィックス、区切り文字を含む）

1. を設定します。 **[!UICONTROL Code Format]** を次のいずれかに変更します。

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. の場合 **[!UICONTROL Code Prefix]**」には、すべてのクーポンコードの先頭に表示する値を入力します。

1. の場合 **[!UICONTROL Code Suffix]**」には、すべてのクーポンコードの末尾に表示する値を入力します。

1. の場合 **[!UICONTROL Dash Every X Characters]**」の場合は、各ダッシュの間の文字数を入力します。

   ダッシュパターンが異なるクーポンコードは、数値が同じでも、異なるコードと見なされます。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## クーポンの作成

>[!NOTE]
>
>クーポンを作成する前に、 `bin/magento cron:run` コマンドを使用して、cron が実行されていることを確認します。 詳しくは、 [コマンドラインから cron を実行します。](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) （内） _設定ガイド_ を参照してください。

### 方法 1：特定のクーポンを作成する

1. 手順に従って、 [買い物かごの価格ルール](price-rules-cart.md).

1. Adobe Analytics の **[!UICONTROL Rule Information]** セクション、設定 **[!UICONTROL Coupon]** から `Specific Coupon`.

1. を入力します。 **[!UICONTROL Coupon Code]** を使用して、プロモーションで使用できます。

   コードの形式（数値、英数字、アルファベット順）は、 [設定](#configure-coupon-codes).

1. クーポンの使用回数を制限するには、次の操作を行います。

   - 次の数を入力： **[!UICONTROL Uses per Coupon]**.
   - 次の数を入力： **[!UICONTROL Uses per Customer]**.

   無制限に使用する場合は、これらのフィールドを空白のままにします。

   ![買い物かごの価格ルール — クーポン情報](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >複数の顧客が同時に同じクーポンを同時に使用する場合、クーポン処理の遅れにより、設定された使用制限を超える可能性があります。

1. クーポンを特定の期間有効にするには、次の手順を実行します。

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) **送信者** および **宛先** 日付。 日付を選択するには、 **カレンダー** (![カレンダーアイコン](../assets/icon-calendar.png)) アイコンをクリックします。 日付範囲を空のままにした場合、ルールは期限切れになりません。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 次のいずれかの操作をおこないます。

     **オプション 1:** 新しい更新のスケジュール設定

      - クリック **[!UICONTROL Schedule New Update]** をクリックします。

        ![更新をスケジュール](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - 次を入力します。 **[!UICONTROL Update Name]** および **[!UICONTROL Description]**.

      - を選択します。 **開始日** および **[!UICONTROL End Date]** カレンダー ( ![カレンダーアイコン](../assets/icon-calendar.png) ) をクリックします。 日付範囲を空のままにした場合、ルールは期限切れになりません。

      - 完了したら、「 **[!UICONTROL Save]**.

        ![買い物かごの価格ルール — 予定変更](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **オプション 2:** 既存の更新に割り当て：

      - 選択 **[!UICONTROL Assign to Another Update]**.

      - リストで更新を見つけ、 **[!UICONTROL Select]**.

1. 次を完了： [買い物かごの価格ルール](price-rules-cart.md) 必要に応じて。

### 方法 2：クーポンのバッチを生成する

割引クーポンの生成は非同期操作です。この操作はバックグラウンドで実行されるので、操作が完了するのを待たずに管理者で作業を続行できます。 タスクが完了すると、メッセージが表示されます。

1. 手順に従って、 [買い物かごの価格ルール](price-rules-cart.md).

1. の下 **[!UICONTROL Coupon Code]**&#x200B;を選択し、 **[!UICONTROL Use Auto Generation]** チェックボックス。

1. 各顧客がクーポンを使用できる回数を制限するには、 **[!UICONTROL Uses per Customer]**.

   ![買い物かごの価格ルール — 自動番号付きクーポンを生成します](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >複数の顧客が同時に同じクーポンを同時に使用する場合、クーポン処理の遅れにより、設定された使用制限を超える可能性があります。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Manage Coupon Codes]** 」セクションで次の操作を実行します。

   ![買い物かごの価格ルール — クーポンコードの管理](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - の場合 **[!UICONTROL Coupons Qty]**」に、生成するクーポンの数を入力します。

   - 次を入力します。 **[!UICONTROL Code Length]**&#x200B;には、プレフィックス、サフィックス、区切り文字は含まれません。

   - を設定します。 **[!UICONTROL Code Format]** を次のいずれかに変更します。

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - （オプション） **[!UICONTROL Code Prefix]** をコードの先頭に追加する必要があります。

   - （オプション） **[!UICONTROL Code Suffix]** をコードの末尾に追加する必要があります。

   - （オプション）の場合 **[!UICONTROL Dash Every X Characters]**」の場合は、各ダッシュの間の文字数を入力します。 例えば、コードの長さが 12 文字で、4 文字に 1 ダッシュが含まれている場合、次のようになります。 `xxxx-xxxx-xxxx`. ダッシュを使用すると、コードを読みやすく、入力しやすくなります。

1. 完了したら、「 **[!UICONTROL Generate]**.

   システムが表示されます。 `Message is added to queue, wait to get your coupons soon`.

   Cron ジョブが完了すると、生成されたコードのリストが表示されます。

   | フィールド | 説明 |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | 特別な条件を受け取るために作成および使用できる、一意のクーポンコード。 |
   | [!UICONTROL Created] | クーポンコードが作成された日付。 |
   | [!UICONTROL Used] | クーポンが使用されたかどうかを示します。 |
   | [!UICONTROL Times Used] | クーポンコードが使用された回数を示します。 |

   {style="table-layout:auto"}

クーポンコードを CSV または Excel XML ファイルに書き出すには、ファイル形式を選択し、「 **[!UICONTROL Export]**.

クーポンコードを削除するには、リストから 1 つ以上のコードを選択します。 選択 `Delete` から **[!UICONTROL Actions]**  セレクターをクリックし、 **[!UICONTROL Submit]**.

>[!NOTE]
>
>Commerce では複数のクーポンコードを設定できますが、顧客は買い物かごで 1 つのクーポンコードのみを使用できます。 買い物かごで複数のクーポンコードを同時に使用できるようにするには、次のような、対応する拡張機能を使用することを検討します。 [Commerce Marketplace](https://marketplace.magento.com/).

## クーポンレポート

The _クーポン_ レポートは、特定の日付範囲で使用された各クーポンのデータを集計します。 クーポンは買い物かごから適用されるので、レポートには、 [注文ステータス](../stores-purchase/order-status.md). その結果、レポートには、推定された合計と実際の合計の両方が含まれる場合があります。 レポートは、特定のストア表示、期間、注文状況および買い物かご価格のルールに対してフィルタリングできます。

次の例では、2 人の顧客がクーポンコード「H20」を使用しています。 注文の 1 つが請求済みですが、もう 1 つはまだです _保留中_. 推定販売小計、販売割引、販売合計の各列には、両方の注文から集計された金額が表示されますが、実際の請求済注文のみが「小計」、「割引」、「合計」の各列に表示されます。 レポートの各行は、1 つのクーポンプロモーションを表します。

![クーポンレポート](./assets/reports-coupons.png){width="600" zoomable="yes"}

### レポートの実行

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. 複数のストアビューがある場合、 **[!DNL Store View]** をクリックして、レポートの範囲を設定します。

1. 販売を更新するには [統計](../getting-started/sales-reports.md#refresh-statistics) 日の場合は、 _最終更新日_ メッセージを表示します。

   次に、「 」をクリックして、 **[!UICONTROL Coupons]** チェックボックスをオンにして「 」をクリックします。 **[!UICONTROL Refresh]**.

   ![クーポンレポート — 統計の更新](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. データをフィルターするには、次の手順を実行します。

   ![クーポンレポート — フィルター](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Date Used]** を次のいずれかに変更します。

      - `Order Created`
      - `Order Updated`

     The _注文更新済み_ レポートはリアルタイムで作成され、更新は必要ありません。

   - レポートの対象期間を定義するには、 **[!UICONTROL Period]** を次のいずれかに変更します。

      - `Day`
      - `Month`
      - `Year`

   - レポートの日付範囲を定義するには、 **送信者** および **宛先** M/D/YY 形式の日付。

   - 特定のレポートを印刷するには [注文ステータス](../stores-purchase/order-status.md)，設定 **[!UICONTROL Order Status]** から `Specified` をクリックし、リストから注文ステータスを選択します。

   - データのない行をレポートから除外するには、 **[!UICONTROL Empty Rows]** から `No`.

   - レポートに含めるクーポンアクティビティを定義するには、次のいずれかの操作を行います。

      - すべての価格ルールからすべてのクーポン活動を含めるには、 **[!UICONTROL Cart Price Rule]** から `Any`.
      - 特定の価格ルールに関連する活動のみを含めるには、 **[!UICONTROL Cart Price Rule]** から `Specified` をクリックし、リストから買い物かごの価格ルールを選択します。

1. レポートを実行する準備が整ったら、 **[!UICONTROL Show Report]**.

   レポートがページの下部に表示されます。

### フィルターオプション

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Date Used] | レポートの基準として使用される日付フィールドを識別します。 オプション：<br/>**[!UICONTROL Order Created]**：顧客が注文した日付に基づいてレポートを生成します。 最新のデータが確実に含まれるようにするには、メッセージ内のリンクをクリックして、統計を更新します。<br/>**[!UICONTROL Order Updated]**：注文が最後に更新された日付に基づいてレポートを生成します。 このレポートは、リアルタイムデータを使用し、統計を更新する必要はありません。 |
| [!UICONTROL Period] | レポートに使用する日付範囲のタイプを決定します。 オプション： `Day` / `Month` / `Year` |
| [!UICONTROL From] | レポートに含まれる注文データの範囲の最初の日付を示します。 |
| [!UICONTROL To] | レポートに含まれる注文データの範囲の最後の日付を示します。 |
| [!UICONTROL Order Status] | 注文ステータスでレポートをフィルターします。 レポートは、すべての注文に対して生成できます。また、特定の注文ステータスに限定することもできます。 オプション： <br/>**[!UICONTROL Any]**：ステータスに関係なく、すべての注文が含まれます。<br/>**[!UICONTROL Specified]**：指定されたステータスの注文のみが含まれます。 キャンセルされた注文はレポートに含まれません。 |
| [!UICONTROL Empty Rows] | レポートに、取得される可能性のある空のデータの行が含まれているかどうかを判断します。 オプション： `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | レポートに含めるクーポンプロモーションを決定します。 オプション：<br/>**[!UICONTROL Any]**：指定した日付範囲で使用されたクーポンプロモーションの注文情報が含まれます。<br/>**[!UICONTROL Specified]**：指定した日付範囲で、選択したクーポンのプロモーションの注文情報のみが含まれます。 |

{style="table-layout:auto"}

### レポート列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Interval] | レポートに含めるクーポン使用の日付範囲を示します。 期間には、特定の日、月、年、または日付の範囲を指定できます。 間隔の日付は、 **[!UICONTROL Period]** 設定：<br/>`Day`: 6/21/19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | 割引を受け取るために買い物かごに顧客が入力した割引コード。 |
| [!UICONTROL Price Rule] | クーポンに関連付けられている価格ルールの名前。 |
| [!UICONTROL Uses] | レポートに指定した日付範囲でクーポンが使用された回数。 |
| [!UICONTROL Sales Subtotal] | クーポンで配置されたすべての注文からの推定小計。 <br/>販売小計は、すべての適格な注文から集計された小計を表し、次を含みます。 `Pending` まだ請求されていない販売注文。 |
| [!UICONTROL Sales Discount] | クーポン付きで行われたすべての注文からの推定割引額。 <br/>「割引」は、すべての適格な注文から集計された割引額を表し、次を含みます。 `Pending` まだ請求されていない販売注文。 |
| [!UICONTROL Sales Total] | クーポンで行われたすべての注文からの推定総計。 販売合計には、すべての送料と手数料が含まれ、割引額が少なくなります。 <br/>合計販売額は、すべての適格な注文から集計された総計額を表し、次を含みます `Pending` まだ請求されていない販売注文。 値には、小計+送料と処理、割引、税額が含まれます。 <br/> 計算基準： `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | クーポンを使用したすべての請求済み注文からの集計された小計。 |
| [!UICONTROL Discount] | クーポンを使用したすべての請求済み注文からの集計された割引。 |
| [!UICONTROL Total] | クーポンを使用したすべての請求済み注文の集計された注文合計。 |

{style="table-layout:auto"}
