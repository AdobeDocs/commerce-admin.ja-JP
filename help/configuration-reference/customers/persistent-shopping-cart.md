---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: 次のページで設定を確認します： [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] コマース管理のページ。
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>A [永続的な買い物かご](../../stores-purchase/cart-persistent.md) では、買い物かごに残っており、で設定した期間保存される未購入の品目を保持できます。 _永続化の有効期間_. 永続的な買い物かごを使用するには、顧客ブラウザーで cookie を許可する必要があります。

## [!UICONTROL General Options]

![一般オプション](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Web サイト | 永続性が有効かどうかを決定します。 |
| [!UICONTROL Persistence Lifetime (seconds)] | Web サイト | 永続的な cookie の有効期間を秒単位で定義します。 最大値は3153600000秒（100 年）です。 |
| [!UICONTROL Enable "Remember Me"] | Web サイト | を定義します。 _自分を記憶する_ チェックボックスがストアのログインページと登録ページに表示されます。 オプション： <br/>**`Yes`**- _自分を記憶する_ チェックボックス。<br/>**`No`**  — 表示しない _自分を記憶する_ 」チェックボックスに設定され、永続的な cookie は、既に持っている顧客に対してのみ使用されます。 |
| [!UICONTROL "Remember Me" Default Value] | Web サイト | のデフォルトの状態を定義します。 _自分を記憶する_ チェックボックス。 |
| [!UICONTROL Clear Persistence on Log Out] | Web サイト | ストアの顧客がログアウトしたときに永続的な cookie を削除するかどうかを定義します。 この設定に関係なく、顧客がログアウトせず、セッション cookie の有効期限が切れた場合でも、永続的な cookie は引き続き使用されます。 |
| [!UICONTROL Persist Shopping Cart] | Web サイト | 永続的な cookie を使用して、対応するアカウントの買い物かごデータにアクセスできるかどうかを定義します。 オプション： <br/>**`Yes`**— 買い物かごの内容は、セッションの終了後に保存されます。<br/>**`No`**  — セッションが終了した後、買い物かごの内容は保存されません。 |
| [!UICONTROL Persist Wish List] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) セッションが終了したときに、顧客ウィッシュリストの状態を保持するかどうかを指定します。 オプション： <br/>**`Yes`**— ウィッシュリストの内容は、セッションの終了時に保存されます。<br/>**`No`**  — セッションが終了したときにウィッシュリストは保存されません。 |
| [!UICONTROL Persist Recently Ordered Items] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) セッションが終了したときに、最近順序付けされた項目の状態を保持するかどうかを指定します。 オプション： <br/>**`Yes`**— 最近注文された項目の状態は、セッションが終了したときに保存されます。<br/>**`No`**  — セッションが終了したときに、最近注文された項目の状態が保存されません。 |
| [!UICONTROL Persist Currently Compared Products] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) 現在比較されている製品の状態が、セッションが終了しても保持されるかどうかを指定します。 オプション： <br/>**`Yes`**— セッションが終了すると、現在比較されている製品の状態が保存されます。<br/>**`No`**  — セッションが終了した場合、現在比較されている製品の状態は保存されません。 |
| [!UICONTROL Persist Comparison History] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) セッションが終了したときに比較履歴の状態を保持するかどうかを指定します。 オプション： <br/>**`Yes`**— 比較履歴の状態は、セッションが終了すると保存されます。<br/>**`No`**  — セッションが終了したときに、比較履歴の状態が保存されません。 |
| [!UICONTROL Persist Recently Viewed Products] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) セッションが終了したときに、最近表示した製品の状態を保持するかどうかを指定します。 オプション： <br/>**`Yes`**— 最近表示された製品の状態は、セッションが終了したときに保存されます。<br/>**`No`**  — セッションが終了したときに、最近表示された製品の状態が保存されません。 |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) セッションが終了しても、顧客のグループメンバーシップとセグメント化の条件の状態を保持するかどうかを指定します。 オプション： <br/>**`Yes`**— 顧客のグループメンバーシップとセグメント化データの状態は、セッションが終了したときに保存されます。<br/>**`No`**  — セッションが終了したときに、顧客のグループメンバーシップとセグメント化データの状態が保存されません。 |

{style="table-layout:auto"}
