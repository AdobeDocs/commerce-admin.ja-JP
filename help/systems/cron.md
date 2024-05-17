---
title: Cron （スケジュールされたタスク）
description: 管理者からCommerce cron ジョブの実行とスケジュールを制御する方法を説明します。
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Cron （スケジュールされたタスク）

Adobe CommerceとMagento Open Sourceは、スクリプトを定期的に実行することで、スケジュールに従っていくつかの操作を実行します。 管理者からCommerce cron ジョブの実行とスケジュールを制御できます。 Cron スケジュールに従って実行されるストア操作には以下が含まれますが、これらに限定されません。

- [電子メール](email-communications.md)
- [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md)
- [ニュースレター](../merchandising-promotions/newsletters.md)
- [XML サイトマップの生成](../merchandising-promotions/sitemap-xml.md)
- [通貨レートの更新](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce サービスを crontab にインストールして、コアコンポーネントと一部のサードパーティの拡張機能が期待どおりに機能することを確認する必要があります。 を参照してください。 [の説明 _インストールガイド_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) crontab へのサービスのインストールに関する詳細情報

さらに、cron スケジュールに従って実行するように次を設定できます。

- システム グリッドの更新とインデックス再作成の注文
- 保留中の支払いの有効期間

次のことを確認します [ベース URL](../stores-purchase/store-urls.md) ストアのは、cron 操作中に生成される URL が正しくなるように正しく設定されています。 クラウドインフラストラクチャー上のAdobe Commerceについては、以下を参照してください。 [cron ジョブの設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) が含まれる _クラウドインフラストラクチャー上のCommerce ガイド_. オンプレミスについては、を参照してください。 [の設定と実行](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) が含まれる _設定ガイド_.

## Cron の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Cron]** セクション。

   ![詳細設定 – cron タスク](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. の次の設定を行います **[!UICONTROL Index]** および **[!UICONTROL Default]** グループ。

   設定は、各セクションで同じです。

   - **[!UICONTROL Generate Schedules Every]** - スケジュールを生成する頻度（分）を定義します。 スケジュールはデータベースに保存されます。
   - **[!UICONTROL Schedule Ahead for]** - cron ジョブが事前にスケジュールされる期間（分単位）を定義します。 例えば、この設定がに設定されている場合 `10` cron が実行されると、cron ジョブは次の 10 分間にスケジュールされます。
   - **[!UICONTROL Missed if not Run Within]**  – 失敗したジョブを特定するために使用する時間（分）を定義します。 Cron ジョブがスケジュールされた時間に実行されず、指定された時間が経過した場合は、実行できず、ステータスが「」に設定されます `Missed`.
   - **[!UICONTROL History Cleanup Every]**  – 終了したタスクの履歴がデータベースからクリアされる時間（分単位）を定義します。
   - **[!UICONTROL Success History Lifetime]** - cron ジョブの履歴に次の値が含まれる時間（分単位）を定義します `Successful` ステータスはデータベースに残ります。
   - **[!UICONTROL Failure History Lifetime]** - cron ジョブの履歴がである期間（分単位）を `Error` ステータスはデータベースに残ります。
   - **[!UICONTROL Use Separate Process]** - グループのすべての cron ジョブを別のシステムプロセスで実行するかどうかを定義します。 オプション： `Yes` / `No`

   ![詳細設定 – cron グループインデックス](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.
