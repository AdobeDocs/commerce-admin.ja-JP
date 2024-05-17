---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: の設定を確認します。 [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] コマース管理者のページ。
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>A [永続ショッピングカート](../../stores-purchase/cart-persistent.md) 買い物かごに残っている未購入の品目を保持し、次で設定した期間保存できるようにします _永続性の有効期間_. 永続的な買い物かごを使用するには、カスタマーブラウザーで cookie を許可する必要があります。

## [!UICONTROL General Options]

![一般オプション](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Web サイト | 永続性が有効かどうかを判断します。 |
| [!UICONTROL Persistence Lifetime (seconds)] | Web サイト | 永続 cookie の有効期間を秒単位で定義します。 許容される最大値は 3153600000 秒（100 年）です。 |
| [!UICONTROL Enable "Remember Me"] | Web サイト | 次のかどうかを定義 _記録する_ チェックボックスは、ストアのログインページと登録ページに表示されます。 オプション： <br/>**`Yes`**– が表示されます _記録する_ チェックボックス。<br/>**`No`**  – を表示しない _記録する_ チェックボックスを選択し、永続 cookie を既に持っている顧客にのみ使用されます。 |
| [!UICONTROL "Remember Me" Default Value] | Web サイト | のデフォルトの状態を定義します _記録する_ チェックボックス。 |
| [!UICONTROL Clear Persistence on Log Out] | Web サイト | ストアの顧客がログアウトしたときに永続 cookie を削除するかどうかを定義します。 この設定方法にかかわらず、ユーザーがログアウトせず、セッション cookie の有効期限が切れた場合は、永続 cookie が引き続き使用されます。 |
| [!UICONTROL Persist Shopping Cart] | Web サイト | 永続的な cookie を使用して、対応するアカウントの買い物かごデータへのアクセス権を付与するかどうかを定義します。 オプション： <br/>**`Yes`**– 買い物かごの内容は、セッション終了後に保存されます。<br/>**`No`** - セッション終了後、買い物かごの内容が保存されない。 |
| [!UICONTROL Persist Wish List] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）セッションの終了時にカスタマーウィッシュリストのステータスを保持するかどうかを指定します。 オプション： <br/>**`Yes`**- セッションが終了すると、ウィッシュリストのコンテンツが保存されます。<br/>**`No`** - セッションが終了しても、ウィッシュリストは保存されません。 |
| [!UICONTROL Persist Recently Ordered Items] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）セッションが終了したときに、最近注文された商品のステータスを保持するかどうかを指定します。 オプション： <br/>**`Yes`**– 最近注文した項目の状態は、セッションが終了すると保存されます。<br/>**`No`**  – 最近注文した項目の状態は、セッションが終了しても保存されません。 |
| [!UICONTROL Persist Currently Compared Products] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）現在比較されている商品のステータスをセッション終了時も保持するかどうかを指定します。 オプション： <br/>**`Yes`**– 現在比較されている製品の状態は、セッションの終了時に保存されます。<br/>**`No`**  – 現在比較されている製品の状態は、セッションの終了時には保存されません。 |
| [!UICONTROL Persist Comparison History] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）セッションの終了時に比較履歴のステートを保持するかどうかを指定します。 オプション： <br/>**`Yes`**– 比較履歴の状態は、セッションの終了時に保存されます。<br/>**`No`** - セッションが終了しても、比較履歴の状態は保存されません。 |
| [!UICONTROL Persist Recently Viewed Products] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）セッションの終了時に、最近表示した商品のステータスを保持するかどうかを指定します。 オプション： <br/>**`Yes`**– 最近表示された製品の状態は、セッションの終了時に保存されます。<br/>**`No`**  – 最近表示した製品の状態は、セッションの終了時に保存されません。 |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）セッションが終了したときに、顧客のグループメンバーシップのステータスとセグメント化条件を保持するかどうかを決定します。 オプション： <br/>**`Yes`**– 顧客のグループメンバーシップとセグメント化データの状態は、セッションが終了すると保存されます。<br/>**`No`**  – 顧客のグループメンバーシップの状態とセグメント化データは、セッションが終了しても保存されません。 |

{style="table-layout:auto"}
