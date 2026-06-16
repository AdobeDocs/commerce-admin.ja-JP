---
title: '[!UICONTROL Customers] > [!UICONTROL Gift Registry]'
description: Commerce管理者の[!UICONTROL Customers] > [!UICONTROL Gift Registry] ページで設定を確認します。
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
TQID: https://experienceleague.adobe.com/STCCRRp71FXvz-09LFiYKhJnsbdF8wokfdIa2Ij6-9A
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

これらの設定を使用してストアのお客様にギフトレジストリを有効にする方法について詳しくは、[&#x200B; ギフトレジストリの設定](../../merchandising-promotions/gift-registry-configure.md)を参照してください。 ストアフロントにギフトレジストリ検索を含める方法について詳しくは、[&#x200B; ギフトレジストリ検索を追加](../../merchandising-promotions/gift-registry-search.md)を参照してください。

## [!UICONTROL General Options]

![一般オプション &#x200B;](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | ストアビュー | ギフトレジストリが使用可能かどうかを指定します。 オプション：<br/>**`Yes`**– 選択したストアビューのギフトレジストリを有効にします。 「ギフトレジストリ」タブは、登録済みのお客様のアカウントダッシュボードに表示されます。<br/>**`No`** - ストア ビューではギフト レジストリを使用できません。 |
| [!UICONTROL Maximum Registrants] | ストアビュー | 顧客がギフトレジストリに追加できるユーザーの数を設定します。 お客様は、各登録者とギフトレジストリを共有します。 ストアフロントでは、最大数に達するまで、_登録者を追加_ ボタンを顧客が使用できます。 |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![所有者通知](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | ストアビュー | ギフトレジストリの作成時に送信される所有者通知メールに使用されるテンプレートを指定します。 デフォルトテンプレート：ギフトレジストリオーナー通知 |
| [!UICONTROL Email Sender] | ストアビュー | ギフトレジストリ所有者の通知メールの送信者として表示される[&#x200B; ストア連絡先](../../getting-started/store-details.md#store-email-addresses)を識別します。 デフォルト値：`General Contact` |

{style="table-layout:auto"}

## ギフトレジストリの共有

![&#x200B; ギフトレジストリの共有](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | ストアビュー | ギフトレジストリの作成時に送信されるギフトレジストリ共有メールに使用されるテンプレートを指定します。 所有者が&#x200B;_Share Gift Registry_&#x200B;をクリックすると、メールは各受信者に送信されます。 既定のテンプレート：`Gift Registry Sharing` |
| [!UICONTROL Email Sender] | ストアビュー | ギフトレジストリ共有メールの送信者として表示される[&#x200B; ストア連絡先](../../getting-started/store-details.md#store-email-addresses)を識別します。 デフォルト値：`General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | ストアビュー | 一度に送信できるギフトレジストリ共有メール通知メッセージの最大数。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![&#x200B; ギフトレジストリの更新](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | ストアビュー | ギフトレジストリから購入されたときにギフトレジストリ所有者に送信されるギフトレジストリ更新メールに使用されるテンプレートを決定します。 この更新には、購入した品目と数量に関する情報が含まれますが、注文を行った人の名前は含まれません。 既定のテンプレート：`Gift Registry Update` |
| [!UICONTROL Email Sender] | ストアビュー | ギフトレジストリ更新メールの送信者として表示される[&#x200B; ストア連絡先](../../getting-started/store-details.md#store-email-addresses)を特定します。 デフォルト値：`General Contact` |

{style="table-layout:auto"}
