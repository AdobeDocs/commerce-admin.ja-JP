---
title: PayPal決済レポート
description: PayPal トランザクションを管理するツールとしてのPayPal決済レポートについて説明します。
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/c7v5oSsVPmD6r6obfGEoxPiGkMI4KMWAmfJAW0-CCJk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# PayPal決済レポート

PayPal決済レポートは、資金決済に影響を与える各取引に関する情報を加盟店に提供します。

>[!NOTE]
>
>決済レポートを生成する前に、ストア管理者はPayPal Merchant Technical Servicesに対して、SFTP ユーザーアカウントの作成、決済レポートの生成の有効化、PayPal ビジネスアカウントでのSFTPの有効化をリクエストする必要があります。

PayPal加盟店アカウントで決済レポートを設定して有効にした後、Adobe CommerceとMagento Open Sourceは次の24時間にレポートの作成を開始します。 利用可能な決済レポートのリストは、管理者から表示できます。

**_決済レポートを表示するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**&#x200B;に移動します。

   ![PayPal決済レポート &#x200B;](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. 最新の更新については、右上隅の「**[!UICONTROL Fetch Updates]**」をクリックしてください。

   システムはPayPal SFTP サーバーに接続してレポートを取得します。 プロセスが完了すると、取得されたレポートの数を示すメッセージが表示されます。 このレポートには、各取引に関する次の情報が含まれます。

   | レポート列 | 説明 |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | 次のいずれかの参照コード：<br/> – 注文ID<br/>- トランザクション ID<br/>- サブスクリプション ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - PayPalでのトランザクションで加盟店が入力したテキスト。<br/>**[!UICONTROL Transaction Debit or Credit]**– 総金額の貨幣移動の方向。<br/>**[!UICONTROL Fee Debit or Credit]**  – 手数料のためのお金の動きの方向。 |

   {style="table-layout:auto"}
