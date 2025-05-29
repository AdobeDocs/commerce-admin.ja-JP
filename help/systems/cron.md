---
title: Cron （スケジュールされたタスク）
description: 管理者からCommerce cron ジョブの実行とスケジュールを制御する方法を説明します。
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '415'
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
>Commerce サービスを crontab にインストールして、コアコンポーネントと一部のサードパーティの拡張機能が期待どおりに機能することを確認する必要があります。 crontab へのサービスのインストールについて詳しくは、[_インストールガイドの手順_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=ja) を参照してください。

さらに、cron スケジュールに従って実行するように次を設定できます。

- システム グリッドの更新とインデックス再作成の注文
- 保留中の支払いの有効期間

Cron 操作中に生成される URL が正しくなるように、ストアの [ ベース URL](../stores-purchase/store-urls.md) が正しく設定されていることを確認します。 [ クラウドインフラストラクチャー上のAdobe Commerceについては、_クラウドインフラストラクチャー上のCommerce ガイド ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html?lang=ja)cron ジョブの設定_ を参照してください。 オンプレミスの場合は、[ 設定ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=ja) の _設定と実行コン_ を参照してください。

## Cron の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Cron]**」セクションを展開します。

   ![ 詳細設定 – cron タスク ](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. **[!UICONTROL Index]** グループと **[!UICONTROL Default]** グループに対して、次の設定を行います。

   設定は、各セクションで同じです。

   - **[!UICONTROL Generate Schedules Every]** - スケジュールを生成する頻度（分）を定義します。 スケジュールはデータベースに保存されます。
   - **[!UICONTROL Schedule Ahead for]** – 事前に cron ジョブをスケジュールする間隔（分単位）を定義します。 例えば、この設定が `10` に設定され、cron が実行される場合、cron ジョブは次の 10 分間にスケジュールされます。
   - **[!UICONTROL Missed if not Run Within]** – 失敗したジョブを特定するために使用する時間（分）を定義します。 Cron ジョブがスケジュールされた時刻に実行されず、指定された時間が経過した場合は、ジョブを実行できず、ジョブのステータスが `Missed` に設定されます。
   - **[!UICONTROL History Cleanup Every]** – 終了したタスクの履歴がデータベースからクリアされる時間（分単位）を定義します。
   - **[!UICONTROL Success History Lifetime]** - `Successful` ステータスの cron ジョブの履歴がデータベースに残る時間（分単位）を定義します。
   - **[!UICONTROL Failure History Lifetime]** - `Error` ステータスの cron ジョブの履歴がデータベースに残る時間（分単位）を定義します。
   - **[!UICONTROL Use Separate Process]** - グループのすべての cron ジョブを別のシステムプロセスで実行するかどうかを定義します。 オプション：`Yes` / `No`

   ![ 詳細設定 – cron グループインデックス ](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
