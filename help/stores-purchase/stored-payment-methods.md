---
title: 保存されている支払い方法
description: お客様がCommerce ストアフロントで保存済みの支払い方法を使用する方法について説明します。
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# 保存されている支払い方法

支払い情報を保存するための安全なコンテナにアクセスできるお客様は、毎回クレジットカード情報を入力することなく、チェックアウトをスピードアップできます。 [ 即時購入 ](checkout-instant-purchase.md) が有効になっている場合、お客様は 2 ステップのチェックアウトプロセスを回避し、製品ページから注文を行うことができます。

[Braintree](braintree.md) など、セキュリティで保護されたコンテナーをサポートする支払い方法が必要です。 支払い方法の設定で Secure Vault が有効になっている場合、お客様はチェックアウト時にクレジットカード情報を保存された支払い方法として保存するオプションを使用できます。 顧客は、アカウントダッシュボードから保存済みの支払い方法を管理できます。

![ 保管支払方法 ](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## チェックアウト時に保存されている支払方法を追加する

1. ストアフロントから、お客様は商品の詳細ページに移動します。

1. 商品を買い物かごに追加します。

1. チェックアウトページに進みます。

1. _出荷_ 手順を完了します。

1. **[!UICONTROL Braintree Credit Card]** の支払方法を選択します。

1. クレジットカードのデータを入力します。

1. **[!UICONTROL Save for later use]** チェックボックスを選択します。

1. **[!UICONTROL Place Order]** をクリックします。

保存された支払い方法が、顧客ダッシュボードの「_[!UICONTROL Stored Payment Methods]_」タブに表示されます。

## 保存されている支払方法の削除

以前に追加された保存済みの支払い方法は、顧客が編集することはできません。削除のみが可能です。 このアクションは取り消しできません。

1. アカウントのサイドバーで、顧客が「**[!UICONTROL Stored Payment Methods]**」を選択します。

1. 削除する支払方法エントリを検索します。

1. **[!UICONTROL Delete]** をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。
