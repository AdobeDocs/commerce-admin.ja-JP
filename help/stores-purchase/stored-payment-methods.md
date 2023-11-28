---
title: 保管済支払い方法
description: 顧客が保存された支払い方法をコマースストアフロントで使用する方法を説明します。
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# 保管済支払い方法

支払い情報を保存する安全な保管庫にアクセスできる顧客は、毎回クレジットカード情報を入力することなく、チェックアウトを迅速に実行できます。 次の場合 [即時購入](checkout-instant-purchase.md) を有効にすると、顧客は 2 段階のチェックアウトプロセスを回避して、製品ページから注文をおこなうことができます。

安全な Vault をサポートする支払い方法（例： ） [Braintree](braintree.md)、が必要です。 支払い方法の設定でセキュアなヴォールトが有効になっている場合、顧客は、クレジットカード情報を保存された支払い方法として保存するためのオプションをチェックアウト時に使用できます。 顧客は、自分のアカウントダッシュボードから保管済みの支払い方法を管理できます。

![保管済支払い方法](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## チェックアウト時に保存された支払い方法を追加

1. お客様はストアフロントから製品の詳細ページに移動します。

1. 買い物かごに商品を追加します。

1. 「チェックアウト」ページに進みます。

1. 次を完了します。 _送料_ 手順

1. を選択します。 **[!UICONTROL Braintree Credit Card]** 支払い方法。

1. クレジットカードのデータを入力します。

1. を選択します。 **[!UICONTROL Save for later use]** チェックボックス。

1. クリック数 **[!UICONTROL Place Order]**.

保存した支払い方法が _[!UICONTROL Stored Payment Methods]_」タブをクリックします。

## 保存された支払い方法を削除します

以前に追加された、保存された支払い方法は、顧客が編集できず、削除できるのは削除のみです。 この操作は元に戻せません。

1. 顧客がアカウントのサイドバーで **[!UICONTROL Stored Payment Methods]**.

1. 削除する支払方法のエントリを検索します。

1. クリック数 **[!UICONTROL Delete]**.

1. アクションを確定するには、「 」をクリックします。 **[!UICONTROL OK]**.
