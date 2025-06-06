---
title: 発注承認ルール
description: 発注書の承認ルールと、会社の管理者がストアフロントで定義する方法について説明します。
exl-id: e8d8bbc9-41cf-4024-85cc-92f0b0ce32d6
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 0%

---

# 発注承認ルール

ほとんどの会社では、発注書に対して注文の承認が必要です。 会社アカウントの承認ルールを追加することで、誰が発注書を作成でき、どのくらいの金額を使用できるかを制御できます。 例：

* X 値未満の発注は自動的に承認されます。
* X 値を超え Q 未満の発注は、Y による承認が必要です。
* X を超える発注の値は、Y と Z による承認が必要です。
* Director レベル以上のユーザーが作成した発注は自動承認されます。

会社の役割と権限に応じて、ユーザーは承認ルールを作成、編集、削除または表示できます。

>[!IMPORTANT]
>
>承認ルールの設定には、購買顧客のマネージャによる承認を指定するために、定義された [ 会社構造 ](account-company-structure.md) が必要です。

## 支払い方法

発注承認フローでは、オンラインとオフラインの両方の支払方法がサポートされています。 発注承認では、すべてのデフォルトのオフライン支払方法がサポートされています。 オンライン支払いの場合、次の方法がサポートされています。

* PayPal Express
* Braintree支払い


## 承認ルールの設定

B2B の顧客は、必要な [ 自分の役割の権限 ](account-company-roles-permissions.md) を使用して、顧客アカウントの左側のパネルの **[!UICONTROL Approval Rules]** をクリックすると、会社ポリシーを適用する承認ルールを設定できます。

![ 会社承認規程 ](./assets/approval-rules.png){width="700" zoomable="yes"}

顧客が承認ルールを作成するには、次の手順を実行します。

1. **[!UICONTROL Add New Rule]** をクリックしてルールを作成します。

1. 必要に応じて、ルールを **[!UICONTROL Enabled]** から **[!UICONTROL Disabled]** に変更します。

   ルールはデフォルトで有効になっていますが、顧客は、無効にした設定を使用してルールを作成し、後で適用する準備が整ったら有効にすることができます。

1. **[!UICONTROL Rule name]** の場合は、ルールの短くわかりやすい名前（`Orders less than $100` など）を入力します。

   ルール名は一意である必要があります。

1. **[!UICONTROL Description]**：ルールの詳細な説明を入力します。

1. **[!UICONTROL Applies to]** の場合、ルールの適用に使用する 1 つ以上の会社の役割を選択します。

1. **[!UICONTROL Rule Type]** を選択し、ルールを定義します。

   次のセクションでは、各ルールタイプについて詳細に説明し、例を示します。

   ![ 新しい承認ルールの作成 ](./assets/approval-rules-create.png){width="700" zoomable="yes"}

1. **[!UICONTROL Requires approval from]** の場合、は承認のタイプに応じて 1 人以上の必要な承認者を選択します。

   >[!NOTE]
   >
   >* 承認者として役割を割り当てる場合は、その役割に少なくとも 1 人のユーザーが存在することを確認します。
   >* 同じ承認者の役割を持つユーザーが 2 人以上いる場合、発注書の作成者はその発注書を承認できません。 この場合、この承認者の役割を持つその他のユーザーには、手動による承認が必要です。 ただし、`Auto-approve POs created within this role` のオプションが [ 役割の権限 ](account-company-roles-permissions.md) で設定されている場合、発注書は自動的に承認されます。
   >* 承認者の役割を持つユーザーが 1 人だけで、そのユーザーが作成者の場合、発注書は常に自動的に承認されます。`Auto-approve POs created within this role` の権限設定は無視されます。

1. 「**[!UICONTROL Save]**」をクリックします。

### [!UICONTROL Order Total]

このルール タイプは、税を含む注文合計に基づいて発注の承認を要求するために使用されます。

1. **[!UICONTROL Order Total amount]** オプションを選択します。

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. 通貨タイプを選択し、金額を入力します。

![ 受注合計承認ルール ](./assets/approval-rules-order-total.png){width="600" zoomable="yes"}

### [!UICONTROL Shipping Cost]

このルール タイプは、多くの会社が要求する出荷原価に基づく発注の承認を要求するために使用されます。

1. **[!UICONTROL Shipping cost value]** を設定します。

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. 希望する配送料を設定します。

![ 出荷原価承認ルール ](./assets/approval-rules-shipping-cost.png){width="600" zoomable="yes"}

### [!UICONTROL Number of SKUs]

このルールタイプは、SKU の数または注文の一意の製品に基づいて発注承認を要求するために使用されます。 注文される品目の数ではなく、個別の品目タイプの数を制御します。 例えば、発注には次が含まれます。

* 2 枚の大きな白いシャツ
* 白シャツ （中） 3 枚

この例では、5 つの項目を指定しますが、2 つの異なる SKU を指定します。

1. **[!UICONTROL Number of SKUs]** の値を設定します。

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. SKU の数を設定します。

![SKU 数承認ルール ](./assets/approval-rules-number-skus.png){width="600" zoomable="yes"}

## 承認ルールの編集

既存の承認ルールを変更する場合、顧客は次の手順を実行できます。

1. アカウントのサイドバーで、顧客が「**[!UICONTROL Approval Rules]**」を選択します。

1. 編集対象の承認ルールエントリを検索します。

1. **[!UICONTROL Edit]** をクリックします。

1. 必要な変更をすべて加え、**[!UICONTROL Save]** をクリックします。

## 承認ルールの削除

既存の承認ルールを削除する場合、顧客は次の手順を実行できます。

1. アカウントのサイドバーにある「**[!UICONTROL Approval Rules]**」を選択します。

1. 削除する承認ルールエントリを検索します。

1. **[!UICONTROL Delete]** をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。

## 発注承認デモ

発注書の承認について詳しくは、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/3410767?quality=12&learn=on&captions=jpn)
