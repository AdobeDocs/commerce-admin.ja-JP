---
title: PayPal 決済レポート
description: PayPal トランザクションを管理するツールとしての PayPal 決済レポートについて説明します。
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# PayPal 決済レポート

PayPal 決済レポートは、資金の決済に影響を与える各取引に関する情報をマーチャントに提供します。

>[!NOTE]
>
>店舗管理者は、決済レポートを生成する前に、PayPal Merchant Technical Services に対して、SFTP ユーザーアカウントの作成、決済レポートの生成の有効化、および PayPal ビジネスアカウントでの SFTP の有効化をリクエストする必要があります。

PayPal マーチャントアカウントで決済レポートを設定して有効にすると、Adobe CommerceとMagento Open Sourceは次の 24 時間以内にレポートの生成を開始します。 使用可能な決済レポートのリストは、管理者から表示できます。

**_決済レポートを表示する手順は、次のとおりです。_**

1. _管理者_ サイドバーで、**[!UICONTROL Reports]**/_[!UICONTROL Sales]_/**[!UICONTROL PayPal Settlement]**&#x200B;に移動します。

   ![PayPal 決済レポート ](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. 最新の更新については、右上隅の「**[!UICONTROL Fetch Updates]**」をクリックします。

   システムは、レポートを取得するために PayPal SFTP サーバーに接続します。 処理が完了すると、取得したレポート数を示すメッセージが表示されます。 レポートには、各トランザクションに関する次の情報が含まれます。

   | レポート列 | 説明 |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | 次のいずれかの参照コード：<br/> – 注文 IDT<br/>- トランザクション ID<br/> – 購読 ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - PayPal でのトランザクションでマーチャントが入力したテキスト。<br/>**[!UICONTROL Transaction Debit or Credit]**– 総額の金銭移動方向。<br/>**[!UICONTROL Fee Debit or Credit]** – 手数料のためのお金の動きの方向。 |

   {style="table-layout:auto"}
