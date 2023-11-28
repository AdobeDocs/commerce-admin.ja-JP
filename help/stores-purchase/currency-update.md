---
title: 通貨レートを更新
description: 通貨レートを手動で設定する方法、またはストアにインポートする方法を説明します。
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 通貨レートを更新

通貨レートは手動で設定することも、ストアにインポートすることもできます。 店舗で最新のレートを確保するには、予定に従って自動的に更新される通貨レートを設定します。

通貨レートをインポートする前に、 [通貨レートの設定](currency-configuration.md) をクリックして、受け入れる通貨を指定し、インポート接続とスケジュールを確立します。

![通貨レート](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## 通貨レートの手動更新

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. 変更するレートをクリックし、サポートされる各通貨の新しい値を入力します。

1. 完了したら、「 **[!UICONTROL Save Currency Rates]**.

## 通貨レートのインポート

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. 設定 **[!UICONTROL Import Service]** を通貨レートプロバイダーに追加します。

   デフォルトのプロバイダーは `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >2.4.6 リリース以降、 [[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨となり、 [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) サービス。 非推奨の [!DNL Fixer.io] アカウント。

1. クリック **[!UICONTROL Import]**.

   更新された率は、 _[!UICONTROL Currency Rates]_リスト。 前回の更新以降にレートが変更された場合は、参照用に以下に古いレートが表示されます。

1. 完了したら、「 **[!UICONTROL Save Currency Rates]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** 無効なキャッシュをリンクして更新します。

   ![システムメッセージ — 無効なキャッシュを更新します](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## 予定に従って通貨レートをインポート

1. 次を確認します。 [Cron](../systems/cron.md) がお客様のストアに対して有効になっている。

1. 受け入れ、インポート接続とスケジュールを確立する通貨を指定するには、 [通貨レートの設定](currency-configuration.md).

1. レートがスケジュールに従ってインポートされることを確認するには、 _[!UICONTROL Currency Rates]_リスト。

1. スケジュールに設定された頻度設定の期間を待ち、レートを再度確認します。
