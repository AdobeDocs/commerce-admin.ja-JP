---
title: 非表示の税の計算
description: 税が埋め込まれた割引がある場合に、非表示の税金計算を設定する方法を説明します。
exl-id: be2000b1-09d7-4a28-814a-f5da7591e387
feature: Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# 非表示の税の計算

_非表示の税金_ は、割引額に含まれる VAT の金額です。 次の条件のすべてが真の場合は、ゼロ以外の値になります。

- カタログ価格に税が含まれます
- VAT 率がゼロではありません
- 値引きの贈り物がある

税が組み込まれた割引がある場合、Commerce は _隠し税_ 割引価格の計算用に再び追加されます。

`discountedItemPrice = fullPriceWithoutTax - discountAmountOnFullPriceWithoutTax + vatAmountOnDiscountedPrice + hiddenTax`

## 例

1. 品目の定価（税込）: $100
1. VAT: 20%
1. 品目価格を除く税金に 10%適用される割引：

### 予期された結果が無効です

- 税引き後の品目価格（割引なし=100 米ドル）
- 税引前品目価格（割引なし）=100/1.2=83.33 USD
- 割引=83.33 \ *0.1=8.33 USD
- Tax=(83.33-8.33) \ *0.2=**15 USD （無効）**
- 受注合計（税金を除く）=83.33-8.33=**75 USD （無効）**
- 注文合計（税=75+15=を含む）**90 USD （無効）**

### 買い物かご内の有効な実際の結果

![買い物かご内の非表示の税金計算](./assets/hidden-tax.png){width="700" zoomable="yes"}

### 有効な計算

1. 税金のない品目の完全価格は$100 / 1.2 = **$83.33**

1. 全品目価格の VAT 金額は、$100 ～ $83.33 = $16.67 です。

   _また、$100 \ * (1 - 1/1.2) として計算することもできます。_

1. $83.33 に対する 10%の割引は次のとおりです。 **8.33 ドル** （税引きをしない場合）

1. 税付き品目の割引価格は$100 ～ $8.33 = $91.67 です

   >[!NOTE]
   >
   >この式は、割引が適用される方法に関する顧客の認識を示します。

1. 税金のない品目の割引価格は$91.67 / 1.2 = $76.39 です

1. 割引価格の VAT 金額は、$91.67 ～ $76.39 =です **$15.28 （有効）**

   _また、$91.67 \ * (1 - 1/1.2) として計算することもできます。_

1. 非表示の税または _割引税の報酬_ は定価と割引価格の VAT 金額の差です： $16.67 - $15.28 = **1.39 ドル**

   _これを見る別の方法：隠し税は、$8.33 割引： $8.33 \* (1 - 1/1.2) 内に持ち込まれた VAT 金額です。_

1. 顧客が通常、割引価格（注文の合計）を理解する方法：

   _税込品目の定価&#x200B;**より小さい**割引額： $100 ～ $8.33 = $91.67_

1. **Commerce が割引価格を計算する方法** （式については、前述の説明を参照）。

   _$83.33 - $8.33 + 15.28 + 1.39 =**$91.67***_
