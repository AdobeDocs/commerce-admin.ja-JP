---
title: 通貨レートの更新
description: 通貨レートを手動で設定するか、ストアに読み込む方法について説明します。
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
TQID: https://experienceleague.adobe.com/tEt15Mzt7MeDtf6MZfu9n6EsvJKUCNBdGhUo0-RK3zk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 通貨レートの更新

通貨レートは手動で設定することも、店舗に読み込むこともできます。 ストアが最新のレートを保持していることを確認するために、通貨レートをスケジュール通りに自動的に更新するように設定できます。

通貨レートを読み込む前に、[通貨レート設定](currency-configuration.md)を完了して、受け入れる通貨を指定し、読み込み接続とスケジュールを確立します。

![通貨レート ](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## 通貨レートを手動で更新する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**に移動します。

1. 変更するレートをクリックし、サポートされている各通貨の新しい値を入力します。

1. 完了したら、**[!UICONTROL Save Currency Rates]**&#x200B;をクリックします。

## 通貨レートのインポート

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**に移動します。

1. 通貨レート プロバイダーに&#x200B;**[!UICONTROL Import Service]**&#x200B;を設定します。

   既定のプロバイダーは`fixer.io (legacy)`です。

   >[!IMPORTANT]
   >
   >2.4.6 リリース以降、[[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨となり、[[!DNL Fixer API]  （APILayer） ](https://apilayer.com/marketplace/fixer-api) サービスに置き換えられます。 非推奨の[!DNL Fixer.io] アカウントの代わりにAPILayer アカウントを使用することを強くお勧めします。

1. **[!UICONTROL Import]**&#x200B;をクリックします。

   更新された料金が&#x200B;_[!UICONTROL Currency Rates]_リストに表示されます。 前回の更新以降に料金が変更された場合は、以下に古い料金が表示されます。

1. 完了したら、**[!UICONTROL Save Currency Rates]**&#x200B;をクリックします。

1. キャッシュの更新を求めるメッセージが表示されたら、**[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

   ![ システムメッセージ – 無効なキャッシュを更新します](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## スケジュールの通貨レートのインポート

1. お使いのストアで[Cron](../systems/cron.md)が有効になっていることを確認してください。

1. 受け入れ、インポート接続とスケジュールを設定する通貨を指定するには、[通貨レート設定](currency-configuration.md)を完了します。

1. 料金がスケジュール通りに読み込まれることを確認するには、_[!UICONTROL Currency Rates]_リストを確認してください。

1. スケジュール用に設定された周波数設定の時間帯を待ち、再度レートを確認します。
