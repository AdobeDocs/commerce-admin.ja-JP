---
title: Cron（予定タスク）
description: 管理者からコマース cron ジョブの実行とスケジュールを制御する方法を説明します。
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Cron（予定タスク）

Adobe CommerceとMagento Open Sourceは、スクリプトを定期的に実行することで、スケジュールに従っていくつかの操作を実行します。 管理者から、コマース cron ジョブの実行とスケジュールを制御できます。 Cron スケジュールに従って実行されるストア操作には、次のものが含まれますが、これらに限定されません。

- [電子メール](email-communications.md)
- [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md)
- [ニュースレター](../merchandising-promotions/newsletters.md)
- [XML サイトマップの生成](../merchandising-promotions/sitemap-xml.md)
- [通貨レートの更新](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>コマースサービスを crontab にインストールして、コアコンポーネントと一部のサードパーティ拡張機能が期待どおりに動作するようにする必要があります。 詳しくは、 [説明は、 _インストールガイド_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) crontab にサービスをインストールする方法の詳細

さらに、Cron スケジュールに従って実行するように次の設定を行うことができます。

- システムグリッドの更新とインデックス再作成の順序付け
- 保留中の支払い有効期間

次を確認します。 [ベース URL](../stores-purchase/store-urls.md) ストアのが正しく設定され、cron 操作中に生成される URL が正しく設定されている場合。 クラウドインフラストラクチャ上のAdobe Commerceについては、 [Cron ジョブの設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) （内） _Commerce on Cloud Infrastructure ガイド_. オンプレミスの場合は、 [設定および実行アイコン](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) （内） _設定ガイド_.

## cron の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Cron]** 」セクションに入力します。

   ![詳細設定 — cron タスク](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. 次の設定を行います： **[!UICONTROL Index]** および **[!UICONTROL Default]** グループ。

   設定は、各セクションで同じです。

   - **[!UICONTROL Generate Schedules Every]**  — スケジュールの生成頻度を定義します（分単位）。 スケジュールは、データベースに保存されます。
   - **[!UICONTROL Schedule Ahead for]**  — 事前に Cron ジョブをスケジュールする範囲を定義します（分単位）。 例えば、この設定が `10` cron が実行され、cron ジョブは次の 10 分間スケジュールされます。
   - **[!UICONTROL Missed if not Run Within]**  — ミスしたジョブの特定に使用する時間（分単位）を定義します。 Cron ジョブがスケジュールされた時刻に実行されず、指定された時間が経過した場合は、ジョブを実行できず、ステータスがに設定されます。 `Missed`.
   - **[!UICONTROL History Cleanup Every]**  — 終了したタスクの履歴がデータベースからクリアされる時間（分単位）を定義します。
   - **[!UICONTROL Success History Lifetime]**  — を使用した cron ジョブの履歴の時間（分単位）を定義します。 `Successful` ステータスはデータベースに残ります。
   - **[!UICONTROL Failure History Lifetime]**  — を使用して cron ジョブの履歴（分単位）を定義します。 `Error` ステータスはデータベースに残ります。
   - **[!UICONTROL Use Separate Process]**  — グループのすべての cron ジョブを別のシステムプロセスで実行するかどうかを定義します。 オプション： `Yes` / `No`

   ![高度な設定 — cron グループインデックス](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.
