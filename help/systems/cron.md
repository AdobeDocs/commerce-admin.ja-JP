---
title: Cron （スケジュールされたタスク）
description: 管理者からCommerce cron ジョブの実行とスケジュールを制御する方法について説明します。
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/6zjak78aoXbzoHzdnOL4tvXgq4KAAjwMNLlLPax4ovE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# Cron （スケジュールされたタスク）

Adobe CommerceとMagento Open Sourceは、スクリプトを定期的に実行することで、スケジュールに従って一部の操作を実行します。 Commerce cron ジョブの実行とスケジュール設定は、管理者から制御できます。 cron スケジュールに従って実行されるストアオペレーションには、次のものが含まれますが、これらに限定されません。

- [メール](email-communications.md)
- [カタログ価格ルール](../merchandising-promotions/price-rules-catalog.md)
- [ニュースレター](../merchandising-promotions/newsletters.md)
- [XML サイトマップ生成](../merchandising-promotions/sitemap-xml.md)
- [通貨レートの更新](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>コアコンポーネントと一部のサードパーティの拡張機能が期待どおりに機能するように、Commerce サービスをcrontabにインストールする必要があります。 crontabへのサービスのインストールについて詳しくは、_インストールガイド_[&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html)の手順を参照してください。

さらに、cron スケジュールに従って実行するように次の設定を行うことができます。

- システムグリッドの更新とインデックス再作成の順序
- 保留中の支払い期間

ストアの[&#x200B; ベース URL](../stores-purchase/store-urls.md)が正しく設定されていることを確認して、cronの操作中に生成されるURLが正しいことを確認します。 Adobe Commerce on Cloud Infrastructureについては、_Commerce on Cloud Infrastructure ガイド_&#x200B;の「[cron ジョブの設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html)」を参照してください。 オンプレミスについては、_設定ガイド_&#x200B;の「[設定と実行](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html)」を参照してください。

## cronの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL System]**&#x200B;を選択します。

1. **[!UICONTROL Cron]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![詳細設定 – cron タスク &#x200B;](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. **[!UICONTROL Index]**&#x200B;および&#x200B;**[!UICONTROL Default]** グループの次の設定を完了します。

   設定は各セクションで同じです。

   - **[!UICONTROL Generate Schedules Every]** - スケジュールが生成される頻度（分単位）を定義します。 スケジュールはデータベースに保存されます。
   - **[!UICONTROL Schedule Ahead for]** – 事前にcron ジョブをスケジュールする時間を定義します（分単位）。 例えば、この設定が`10`に設定されていてcronが実行されている場合、cron ジョブは次の10分間スケジュールされます。
   - **[!UICONTROL Missed if not Run Within]** – 欠落したジョブの決定に使用される時間（分単位）を定義します。 cron ジョブがスケジュールされた時間に実行されず、指定された時間が経過した場合、実行できず、ステータスは`Missed`に設定されます。
   - **[!UICONTROL History Cleanup Every]** – 終了したタスクの履歴がデータベースから消去される時間（分単位）を定義します。
   - **[!UICONTROL Success History Lifetime]** - `Successful` ステータスのcron ジョブの履歴がデータベースに残る時間（分単位）を定義します。
   - **[!UICONTROL Failure History Lifetime]** - `Error` ステータスのcron ジョブの履歴がデータベースに残る時間（分単位）を定義します。
   - **[!UICONTROL Use Separate Process]** - グループのすべてのcron ジョブを別のシステム プロセスで実行するかどうかを定義します。 オプション：`Yes` / `No`

   ![詳細設定 – cron グループ インデックス &#x200B;](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
