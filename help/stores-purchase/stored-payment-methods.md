---
title: 保存されている支払い方法
description: Commerceのストアフロントでストアド決済を使用する方法をご紹介します。
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
TQID: https://experienceleague.adobe.com/dYEYXgEIp83AKhHepfDQVNR9YBUQGbJ7B2zu8UTM-I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# 保存されている支払い方法

安全な保管庫にアクセスして支払い情報を保存できれば、毎回クレジットカード情報を入力することなく、チェックアウトをスピードアップすることができます。 [即時購入](checkout-instant-purchase.md)が有効になっている場合、お客様は2段階のチェックアウトプロセスをスキップして、製品ページから注文できます。

[Braintree](braintree.md)などのセキュアな保管サービスをサポートする支払い方法が必要です。 支払い方法の設定でセキュアな保管が有効になっている場合、お客様は、チェックアウト時にクレジットカード情報を保存済みの支払い方法として保存するオプションを利用できます。 顧客は、アカウントダッシュボードで支払い方法を管理できます。

![保存されたお支払い方法](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## チェックアウト時に保存されている支払い方法を追加

1. ストアフロントから、顧客は商品の詳細ページに移動します。

1. 商品をカートに追加します。

1. チェックアウトページに進みます。

1. _発送_ ステップを完了します。

1. **[!UICONTROL Braintree Credit Card]**&#x200B;支払い方法を選択します。

1. クレジットカード情報を入力します。

1. 「**[!UICONTROL Save for later use]**」チェックボックスを選択します。

1. **[!UICONTROL Place Order]**&#x200B;をクリックします。

保存された支払方法は、顧客ダッシュボードの「_[!UICONTROL Stored Payment Methods]_」タブに表示されます。

## 保存されている支払い方法の削除

以前に追加され、保存された支払い方法は、お客様が編集することはできず、削除することしかできません。 この操作は元に戻せません。

1. アカウントのサイドバーで、お客様が&#x200B;**[!UICONTROL Stored Payment Methods]**&#x200B;を選択します。

1. 削除する支払方法エントリを検索します。

1. **[!UICONTROL Delete]**&#x200B;をクリックします。

1. アクションを確認するには、**[!UICONTROL OK]**&#x200B;をクリックします。
