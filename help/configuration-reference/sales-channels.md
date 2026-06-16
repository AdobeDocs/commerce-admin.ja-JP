---
title: '[!UICONTROL Sales Channels] > [!UICONTROL Global Settings]'
description: Commerce管理者の[!UICONTROL Sales Channels] > [!UICONTROL Global Settings] ページで設定を確認します。
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
TQID: https://experienceleague.adobe.com/jnjAspEdJbx3unjmoqgH12JEiLz4ThbgFGeFOArOonU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

これらの設定は、[[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=ja)がインストールされている場合に使用できます。

![Sales Channel設定](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-----|---------|------|
| [!UICONTROL Clear Log History] | グローバル | オプション：<br/><br/>**`Once Daily`**: ストアのアクティビティ履歴を1日1回クリアするには、このオプションを選択します。<br/><br/>**`Once Weekly`**：このオプションを選択すると、1週間に1回、ストアのアクティビティ履歴をクリアできます。<br/><br/>**`Once Monthly`**: （デフォルト）このオプションを選択すると、ストアのアクティビティ履歴を1か月に1回消去できます。 |
| [!UICONTROL Background Tasks (CRON) Source] | グローバル | 「`Magento CRON`」を選択して、[!DNL Amazon Sales Channel]がCommerceのcron設定を使用して、Amazon Seller Centralとの通信およびデータ同期の間隔を決定することを指定します。 |
| [!UICONTROL Enable Debug Logging] | グローバル | トラブルシューティングが必要な場合に追加の同期データを収集するには、`Enabled`を選択します。<br/><br/>このオプションはデフォルトでは無効になっており、継続的なログはパフォーマンスに悪影響を及ぼすため、トラブルシューティングに必要な場合にのみ有効にする必要があります。 トラブルシューティングに対して有効にした場合、完了時に無効にする必要があります。 |
| [!UICONTROL Read-Only Mode] | グローバル | `Enabled`を選択して、すべての送信する状態を変更するAPI要求をブロックします。 読み取り専用モードが無効になるまで、変更の可能性は保存されますが、送信されません。 データ転送を再度開始するには、`Disabled`を選択します。<br/><br/> データベースがインスタンスの新しいコピーに移行されると（ストアのURLが設定で変更されたときに検出されます）、読み取り専用モードが自動的に有効になります。<br/><br/>これは、_ステージング_&#x200B;や&#x200B;_QA_&#x200B;など、実稼動インスタンスのコピーで使用するように設計されており、実稼動インスタンスでは使用しないでください。<br/><br/>**_注&#x200B;_**：有効にするには、[!UICONTROL Read-Only Mode]で設定キャッシュをクリアする必要があります。 |

{style="table-layout:auto"}
