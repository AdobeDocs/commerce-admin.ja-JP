---
title: 買い物かごの価格ルール
description: 一連の条件に基づいて買い物かご内の品目に割引を適用する買い物かごの価格ルールについて説明します。
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 買い物かごの価格ルール

買い物かごの価格ルールは、一連の条件に基づいて、買い物かご内の品目に割引を適用します。 割引は、条件が満たされた場合や、顧客が有効なクーポンコードを入力した場合に、自動的に適用されます。 適用すると、割引は買い物かごの小計の下に表示されます。 買い物かごの価格ルールは、シーズンやプロモーションの必要に応じて、ステータスと日付範囲を変更することで使用できます。

>[!NOTE]
>
>クーポンカートルールに、特定の送料や支払い方法など、チェックアウトオプションを指定する条件がある場合、特定の送料や支払い方法が選択された後、条件はチェックアウトでのみ満たされます。 この場合、クーポンは、最後の手順のチェックアウト時に適用できます。

![ストアフロントの例 — 買い物かごへのクーポンの適用](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## 買い物かごの価格ルールへのアクセス

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![買い物かごの価格ルール](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. 多数のルールがある場合は、各列の上部にあるフィルターオプションを使用してリストを効率化し、「 **[!UICONTROL Search]** フィルターを適用します。

1. すべてのフィルターオプションをクリアして完全なリストを表示するには、 **[!UICONTROL Reset Filter]**.

1. ルールのプロパティを更新します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) クリック **[!UICONTROL Edit]** をクリックして、ルール情報ページを表示します。

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) リストでルールをクリックして、ルール情報ページを表示します。

   （ルールの作成と同様に）ルールの設定を変更できます。

## 列でオプションをフィルター

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 特定のルール ID 番号のリストをフィルターするテキストを入力します。 |
| [!UICONTROL Rule] | テキストを入力し、ルールが作成された際に定義されたルール名に基づいてリストをフィルタリングします。 |
| [!UICONTROL Coupon Code] | テキストを入力し、ルールの作成時に定義されたコード名に基づいてリストをフィルタリングします。 |
| [!UICONTROL Priority] | ルールに対して定義された優先度に基づいてリストをフィルタリングする自由テキストフィールド。 |
| [!UICONTROL Status] | このオプションを使用して、ルールのステータス (`Active` または `Inactive`) をクリックします。 |
| [!UICONTROL Web Site] | ルールに対して定義された Web サイトに基づいてリストをフィルタリングするには、このオプションを使用します。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) クリック **[!UICONTROL Edit]** 表示する _[!UICONTROL Rule Information]_」ページを開き、ルール設定を更新します（ルールの作成と同様）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) 動的カレンダーフィールド (_[!UICONTROL To:]_および_[!UICONTROL From:]_) をクリックして、ルールが作成された際に定義されたルールの開始日に基づいてリストをフィルタリングします。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) 動的カレンダーフィールド (_[!UICONTROL To:]_および_[!UICONTROL From:]_) をクリックして、ルールの作成日時に定義されたルールの終了日に基づいてリストをフィルタリングします。 |

{style="table-layout:auto"}

## Real-Time CDPオーディエンスを使用して買い物かごの価格ルールの通知を送信する

方法を学ぶ [アクティブ化](../customers/audience-activation.md) Real-Time CDPオーディエンスをAdobe Commerceインスタンスに取り込んで、買い物かごの価格ルールに通知します。
