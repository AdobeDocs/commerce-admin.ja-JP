---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: 次のページで設定を確認します： [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] コマース管理のページ。
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

これらの設定を使用して店舗の顧客向けのギフトレジストリを有効にする方法について詳しくは、 [ギフトレジストリの設定](../../merchandising-promotions/gift-registry-configure.md). ストアフロントにギフトレジストリ検索を含める方法については、 [ギフトレジストリ検索を追加](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![一般オプション](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | ストア表示 | ギフトレジストリを使用できるかどうかを指定します。 オプション： <br/>**`Yes`**— 選択したストア表示のギフトレジストリを有効にします。 「ギフトレジストリ」タブは、登録ユーザーのアカウントダッシュボードに表示されます。<br/>**`No`**  — 店舗ではギフトレジストリはご利用いただけません。 |
| [!UICONTROL Maximum Registrants] | ストア表示 | 顧客がギフトレジストリに追加できる人数を設定します。 顧客は、各登録者とギフトレジストリを共有します。 店頭では、 _登録者を追加_ 」ボタンは、の最大数に達するまで、ユーザーに提供されます。 |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![所有者への通知](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | ストア表示 | ギフトレジストリの作成時に送信される所有者通知 E メールに使用するテンプレートを決定します。 デフォルトテンプレート：ギフトレジストリ所有者の通知 |
| [!UICONTROL Email Sender] | ストア表示 | を識別します。 [ストア連絡先](../../getting-started/store-details.md#store-email-addresses) ギフトレジストリ所有者通知メールの送信者として表示されます。 デフォルト値： `General Contact` |

{style="table-layout:auto"}

## ギフトレジストリ共有

![ギフトレジストリ共有](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | ストア表示 | ギフトレジストリの作成時に送信されるギフトレジストリ共有電子メールに使用するテンプレートを決定します。 所有者が _ギフトレジストリの共有_&#x200B;の場合、各受信者に E メールが送信されます。 デフォルトのテンプレート： `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | ストア表示 | を識別します。 [ストア連絡先](../../getting-started/store-details.md#store-email-addresses) ギフトレジストリ共有メールの送信者として表示されます。 デフォルト値： `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | ストア表示 | 一度に送信できるギフトレジストリ共有電子メール通知メッセージの最大数です。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![ギフトレジストリの更新](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | ストア表示 | ギフトレジストリから購入が行われた際にギフトレジストリ所有者に送信されるギフトレジストリの更新メールに使用するテンプレートを決定します。 更新には、購入した品目と数量に関する情報が含まれますが、注文した人の名前は含まれません。 デフォルトのテンプレート： `Gift Registry Update` |
| [!UICONTROL Email Sender] | ストア表示 | を識別します。 [ストア連絡先](../../getting-started/store-details.md#store-email-addresses) ギフトレジストリの更新メールの送信者として表示されます。 デフォルト値： `General Contact` |

{style="table-layout:auto"}
