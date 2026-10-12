---
title: '[!UICONTROL Customers] > [!UICONTROL Wish List]'
description: Commerce管理者の[!UICONTROL Customers] > [!UICONTROL Wish List] ページで設定を確認します。
exl-id: 33ff428c-03e3-4698-a01e-f007b4e1688e
feature: Configuration, Customers, Storefront
TQID: 'https://experienceleague.adobe.com/Qtxe8KavYOeudVvJe1ojXj6ZStlNVeAtAUtZOkRox8E'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 3%
---
# [!UICONTROL Customers] > [!UICONTROL Wish List]

{{config}}

>[!NOTE]
>
>ウィッシュリストでは、登録した顧客が将来購入したい商品の独自のコレクションを作成できます。 ウィッシュリストは顧客間で共有できます。

## [!UICONTROL General Options]

![一般オプション &#x200B;](./assets/wishlist-general-options.png)<!-- zoom -->

<!--[General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/wish-lists/wishlist-configuration) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストアビュー | ストアのウィッシュリストモジュールをアクティブ化します。 オプション：`Yes` / `No` |
| [!UICONTROL Show in Sidebar] | ストアビュー | サイドバーでのウィッシュリストの表示を指定します。 <br/> オプション：`Yes` / `No` |
| [!UICONTROL Enable Multiple Wish Lists] | ストアビュー | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）を`Yes`に設定すると、お客様は複数のウィッシュリストを作成および管理できます。 オプション：`Yes` / `No` |
| [!UICONTROL Number of Multiple Wish Lists] | ストアビュー | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）複数のウィッシュリストが有効になっている場合は、お客様がアカウントに関連付けることができるウィッシュリストの最大数を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Share Options]

![共有オプション &#x200B;](./assets/wishlist-share-options.png)<!-- zoom -->

<!-- [Share Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/wish-lists/wishlist-configuration) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Sender] | ストアビュー | ウィッシュリストの共有時に送信されるメッセージの送信者として表示されるストア連絡先を指定します。 既定の連絡先：`General Contact` |
| [!UICONTROL Email Template] | ストアビュー | 欲しいものリストを共有するときに送信されるメッセージに使用される電子メールテンプレートを決定します。 既定のテンプレート：`Share Wishlist` |
| [!UICONTROL Max Emails Allowed to be Sent] | ストアビュー | バッチで送信できるメールの最大数を指定します。 最大制限を設定すると、サーバーの負荷を軽減できます。 許可される最大数は10,000です。 デフォルト値：`10` |
| [!UICONTROL Email Text Length Limit] | ストアビュー | メッセージに含めることができる最大文字数を指定します。 許可される最大数は10,000です。 デフォルト値：`255` |

{style="table-layout:auto"}

## [!UICONTROL My Wish List Link]

![希望リストのリンク &#x200B;](./assets/wishlist-my-wishlist-link.png)<!-- zoom -->

<!--[My Wish List Link](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/wish-lists/wishlist-configuration) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display Wish List Summary] | web サイト | 顧客アカウントダッシュボードでのウィッシュリストの概要の表示を設定します。 オプション：`Display number of items in wish list` / `Display item quantities` |

{style="table-layout:auto"}
