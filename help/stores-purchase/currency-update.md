---
title: 通貨レートを更新
description: 通貨レートを手動で設定する方法、またはストアに読み込む方法を説明します。
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 通貨レートを更新

通貨レートは手動で設定することも、ストアにインポートすることもできます。 ストアに最新の為替レートを確実に設定するには、スケジュールに従って自動的に更新されるように通貨レートを設定します。

通貨レートをインポートする前に、 [通貨レートの設定](currency-configuration.md) 使用する通貨を指定し、インポート接続とスケジュールを確立します。

![通貨レート](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## 通貨レートの手動更新

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. 変更するレートをクリックし、サポートされる各通貨に新しい値を入力します。

1. 完了したら、 **[!UICONTROL Save Currency Rates]**.

## 通貨レートのインポート

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. を設定 **[!UICONTROL Import Service]** 通貨レートプロバイダーに送信します。

   デフォルトのプロバイダーは `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >2.4.6 リリース以降、 [[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨（廃止予定）になり、に置き換えられました [[!DNL Fixer API] （APILayer）](https://apilayer.com/marketplace/fixer-api) サービス。 非推奨（廃止予定）ではなく、APILayer アカウントを使用することを強くお勧めします [!DNL Fixer.io] アカウント。

1. クリック **[!UICONTROL Import]**.

   更新されたレートは、 _[!UICONTROL Currency Rates]_リスト。 前回の更新以降にレートが変更されている場合は、参照用に古いレートが以下に表示されます。

1. 完了したら、 **[!UICONTROL Save Currency Rates]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** 無効なキャッシュをリンクして更新します。

   ![システムメッセージ – 無効なキャッシュを更新します](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## 通貨レートをスケジュールに従ってインポート

1. 次のことを確認します [Cron](../systems/cron.md) ストアに対してが有効になっています。

1. 受け入れてインポート接続およびスケジュールを確立する通貨を指定するには、次の手順を実行します [通貨レートの設定](currency-configuration.md).

1. レートがスケジュールどおりにインポートされていることを確認するには、 _[!UICONTROL Currency Rates]_リスト。

1. スケジュールに設定された頻度設定の期間が経過するのを待って、もう一度レートを確認します。
