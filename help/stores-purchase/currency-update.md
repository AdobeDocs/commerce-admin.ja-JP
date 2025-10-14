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

通貨レートをインポートする前に、[&#x200B; 通貨レートの設定 &#x200B;](currency-configuration.md) を完了して、使用可能な通貨を指定し、インポート接続とスケジュールを確立します。

![&#x200B; 通貨レート &#x200B;](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## 通貨レートの手動更新

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Currency]_/**[!UICONTROL Currency Rates]**&#x200B;に移動します。

1. 変更するレートをクリックし、サポートされる各通貨に新しい値を入力します。

1. 完了したら、「**[!UICONTROL Save Currency Rates]**」をクリックします。

## 通貨レートのインポート

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Currency]_/**[!UICONTROL Currency Rates]**&#x200B;に移動します。

1. 通貨レートプロバイダーに **[!UICONTROL Import Service]** を設定します。

   デフォルトのプロバイダーは `fixer.io (legacy)` です。

   >[!IMPORTANT]
   >
   >2.4.6 リリース以降、[[!DNL Fixer.io]](https://fixer.io/) サービスは非推奨（廃止予定）となり、[[!DNL Fixer API]  （APILayer） &#x200B;](https://apilayer.com/marketplace/fixer-api) サービスに置き換わります。 非推奨の [!DNL Fixer.io] アカウントではなく、APILayer アカウントを使用することを強くお勧めします。

1. 「**[!UICONTROL Import]**」をクリックします。

   更新されたレートが _[!UICONTROL Currency Rates]_&#x200B;のリストに表示されます。 前回の更新以降にレートが変更されている場合は、参照用に古いレートが以下に表示されます。

1. 完了したら、「**[!UICONTROL Save Currency Rates]**」をクリックします。

1. キャッシュを更新するように求められたら、**[!UICONTROL Cache Management]** のリンクをクリックして無効なキャッシュを更新します。

   ![&#x200B; システムメッセージ – 無効なキャッシュを更新します &#x200B;](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## 通貨レートをスケジュールに従ってインポート

1. ストアで [Cron](../systems/cron.md) が有効になっていることを確認します。

1. インポートの接続とスケジュールを承認および確立する通貨を指定するには、[&#x200B; 通貨レートの設定 &#x200B;](currency-configuration.md) を完了します。

1. レートがスケジュールどおりにインポートされていることを確認するには、_[!UICONTROL Currency Rates]_&#x200B;のリストを確認します。

1. スケジュールに設定された頻度設定の期間が経過するのを待って、もう一度レートを確認します。
