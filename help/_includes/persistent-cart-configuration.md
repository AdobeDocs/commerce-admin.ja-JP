---
title: 永続的な買い物かごの設定参照
description: 永続的な買い物かごの設定参照の再利用可能なコンテンツ。
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![ 一般オプション ](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-persistent#configure-a-persistent-cart) -->

| フィールド | [ 範囲 ](/help/getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Web サイト | 永続性機能を有効にするかどうかを決定します。 |
| [!UICONTROL Persistence Lifetime (seconds)] | Web サイト | 永続 cookie の有効期間を秒単位で定義します。 許可される最大値は 34560000 秒（400 日）です。 これは、推奨される Cookie の最大有効期間の制限です。 |
| [!UICONTROL Enable "Remember Me"] | Web サイト | ストアのログインページと登録ページに _このアカウントを記憶する_ チェックボックスを表示するかどうかを定義します。 オプション：<br/>**`Yes`**- 「このアカウントを記憶する _チェックボックスを表示_ ます。<br/>**`No`** – 「_記憶する_」チェックボックスは表示されず、永続 cookie は既に持っているお客様にのみ使用されます。 |
| [!UICONTROL "Remember Me" Default Value] | Web サイト | 「このアカウントを記憶する _チェックボックスのデフォルト状態を定義し_ す。 |
| [!UICONTROL Clear Persistence on Log Out] | Web サイト | ストアの顧客がログアウトしたときに永続 cookie を削除するかどうかを定義します。 このオプションの設定方法にかかわらず、ユーザーがログアウトせず、セッション cookie が期限切れになった場合は、永続的な cookie が引き続き使用されます。 |
| [!UICONTROL Persist Shopping Cart] | Web サイト | 永続 cookie を使用して、対応するアカウントの買い物かごデータへのアクセス権を付与するかどうかを定義します。 オプション：<br/>**`Yes`**または&#x200B;**`No`**。 |
| [!UICONTROL Persist Wish List] | Web サイト | ![Adobe Commerce](/help/assets/adobe-logo.svg) （Adobe Commerceのみ）セッションの終了時に顧客ウィッシュリストのステータスを保持するかどうかを決定します。 オプション：<br/>**`Yes`**- セッションが終了すると、ウィッシュリストの内容が保存されます。<br/>**`No`** - セッションが終了しても、ウィッシュリストは保存されません。 |
| [!UICONTROL Persist Recently Ordered Items] | Web サイト | ![Adobe Commerce](/help/assets/adobe-logo.svg) （Adobe Commerceのみ）セッションが終了したときに、最近注文された商品のステータスを保存するかどうかを指定します。 オプション：<br/>**`Yes`**または&#x200B;**`No`**。 |
| [!UICONTROL Persist Currently Compared Products] | Web サイト | ![Adobe Commerce](/help/assets/adobe-logo.svg) （Adobe Commerceのみ）現在比較されている商品のステータスをセッションの終了時に保持するかどうかを指定します。 オプション：<br/>**`Yes`**または&#x200B;**`No`**。 |
| [!UICONTROL Persist Comparison History] | Web サイト | ![Adobe Commerce](/help/assets/adobe-logo.svg) （Adobe Commerceのみ）セッションが終了したときに比較履歴のステータスを保持するかどうかを指定します。 オプション：<br/>**`Yes`**または&#x200B;**`No`**。 |
| [!UICONTROL Persist Recently Viewed Products] | Web サイト | ![Adobe Commerce](/help/assets/adobe-logo.svg) （Adobe Commerceのみ）最近表示された商品のステータスをセッションの終了時に保持するかどうかを指定します。 オプション：<br/>**`Yes`**または&#x200B;**`No`**。 |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Web サイト | ![Adobe Commerce](/help/assets/adobe-logo.svg) （Adobe Commerceのみ）セッションが終了したときに、顧客のグループメンバーシップのステータスとセグメント化条件を保持するかどうかを決定します。 オプション：<br/>**`Yes`**– 顧客のグループメンバーシップの状態とセグメント化データは、セッションが終了すると保存されます。<br/>**`No`** – 顧客のグループメンバーシップの状態とセグメント化データは、セッションが終了しても保存されません。 |

{style="table-layout:auto"}
