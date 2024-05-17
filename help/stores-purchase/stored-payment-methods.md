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

支払い情報を保存するための安全なコンテナにアクセスできるお客様は、毎回クレジットカード情報を入力することなく、チェックアウトをスピードアップできます。 次の場合 [即時購入](checkout-instant-purchase.md) を有効にすると、お客様は 2 ステップのチェックアウトプロセスを回避して、製品ページから注文できます。

セキュアなコンテナをサポートする支払方法（例：） [Braintree](braintree.md)、は必須です。 支払い方法の設定で Secure Vault が有効になっている場合、お客様はチェックアウト時にクレジットカード情報を保存された支払い方法として保存するオプションを使用できます。 顧客は、アカウントダッシュボードから保存済みの支払い方法を管理できます。

![保存されている支払方法](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## チェックアウト時に保存されている支払方法を追加する

1. ストアフロントから、お客様は商品の詳細ページに移動します。

1. 商品を買い物かごに追加します。

1. チェックアウトページに進みます。

1. 完了： _送料_ ステップ。

1. 選択します。 **[!UICONTROL Braintree Credit Card]** 支払い方法。

1. クレジットカードのデータを入力します。

1. 選択します。 **[!UICONTROL Save for later use]** チェックボックス。

1. クリック数 **[!UICONTROL Place Order]**.

保存された支払い方法が _[!UICONTROL Stored Payment Methods]_顧客ダッシュボードの「」タブ。

## 保存されている支払方法の削除

以前に追加された保存済みの支払い方法は、顧客が編集することはできません。削除のみが可能です。 このアクションは取り消しできません。

1. アカウントのサイドバーで、顧客が次を選択します。 **[!UICONTROL Stored Payment Methods]**.

1. 削除する支払方法エントリを検索します。

1. クリック数 **[!UICONTROL Delete]**.

1. アクションを確定するには、をクリックします **[!UICONTROL OK]**.
