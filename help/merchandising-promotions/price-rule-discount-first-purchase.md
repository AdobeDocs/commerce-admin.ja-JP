---
title: 買い物かご価格ルールの例 – 初回購入による割引
description: 買い物かごの価格ルールを使用して、初めての顧客に割引を提供する例を説明します。
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# 買い物かご価格ルールの例 – 初回購入による割引

{{ee-feature}}

買い物かご価格ルールを使用すると、クーポンを必要とせずに、最初の購入で顧客に割引を自動的に提供できます。

初めての顧客を対象とした割引を提供するには、次の操作を行います。

- _注文のない購入者_ として定義された顧客セグメントを作成し、
- 新しい顧客セグメントをターゲットにする買い物かご価格ルールを作成します。

>[!NOTE]
>
>顧客セグメント機能が有効になっていることを確認します。 [ 顧客セグメントの作成 ](../customers/customer-segment-create.md) を参照してください。

## 手順 1. 顧客セグメントの作成

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Segments]** に移動します。

1. 右上隅の「**[!UICONTROL Add Segment]**」をクリックします。

1. **[!UICONTROL General Properties]** を定義します。

   - 顧客セグメントを識別する **[!UICONTROL Segment Name]** を入力します（例：_初回顧客_）。

   - **[!UICONTROL Assigned to Website]**：顧客セグメントを使用できる web サイトを選択します。

   - **[!UICONTROL Status]** の場合、「`Active`」を選択します。

   - **[!UICONTROL Apply to]** の場合、「`Visitors and Registered Customers`」を選択します。

   - 完了したら、「**[!UICONTROL Save and Continue Edit]**」をクリックします。

     左側のパネルで、追加のオプションを使用できるようになります。

   ![ 顧客セグメントのプロパティ ](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. **[!UICONTROL Conditions]** を定義します。

   この例では、条件は _合計注文数が 1 未満_ の顧客をターゲットにします。

   - 左側のパネルで「**[!UICONTROL Conditions]**」を選択します。

     デフォルトの条件は、「これらの条件がすべて TRUE の場合」から始まります。

   - _追加_ （![ 追加アイコン ](../assets/icon-add-green-circle.png)）をクリックし、`Number of Orders` を選択します。

   - 「**[!UICONTROL is]**」をクリックし、「`less than`」を選択します。

   - 「**...**」をクリックし、フィールドに `1` と入力します。

   - 緑のチェックマーク（![ 緑のチェックマーク ](../assets/icon-checkmark-green-circle.png)）をクリックして、条件設定を保存します。

   ![ 顧客セグメントの状況 ](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save]**」をクリックします。

顧客セグメントが作成され、_[!UICONTROL Customer Segments]_グリッドに表示されます。

>[!TIP]
>
>セグメント ID をメモします。 この ID 番号を使用して、買い物かご価格ルールを作成します。

## 手順 2. 買い物かご価格ルールの作成

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Promotions]_/**[!UICONTROL Cart Price Rule]**に移動します。

1. 右上隅の「**[!UICONTROL Add New Rule]**」をクリックします。

   既定では、**[!UICONTROL Rule Information]** セクションが表示され、**[!UICONTROL Conditions]** と **[!UICONTROL Conditions]** の展開可能なセクションが表示されます。

1. **[!UICONTROL Rule Information]** を定義します。

   - 「**[!UICONTROL Rule Name]**」フィールドと「**[!UICONTROL Description]**」フィールドに入力します。 これらのフィールドは内部参照用です。

   - **[!UICONTROL Websites]**：ルールを使用できる web サイトを選択します。

   - **[!UICONTROL Customer Groups]**：このルールを適用する顧客グループを選択します。

     複数のグループを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

     >[!NOTE]
     >
     >このリストのオプションは、**[!UICONTROL Customers]**/**[!UICONTROL Customer Groups]** で作成および管理する顧客グループによって異なります。

   - **[!UICONTROL Coupon]** の場合、「`No Coupon`」を選択します。

   - **[!UICONTROL Uses per Customer]** には、`1` と入力します。

   - **[!UICONTROL Priority]**：他のルールに対するこのルールの優先度を設定する数値を入力します。

     >[!NOTE]
     >
     >同じカタログ製品が複数の価格ルールに設定された条件を満たす場合、優先度設定は重要です。 優先度の設定が最も高いルールが、顧客に対してアクティブになります。 優先度は最大で 1 です。 この例では、「`1`」と入力すると、このルールが他のどの価格ルールよりも先に適用されます。 この値は、**[!UICONTROL Action]** セクションの **[!UICONTROL Discard Subsequent Rules]** 設定で使用されます。

   - 完了したら、「**[!UICONTROL Save and Continue Edit]**」をクリックします。

     左側のパネルで、追加のオプションを使用できるようになります。

   ![ 買い物かご価格ルール情報 ](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. **[!UICONTROL Conditions]** を定義します。

   - 下にスクロールして、「**[!UICONTROL Conditions]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

     デフォルトのルールは、「これらの条件がすべて TRUE の場合：」から始まります。

   - _追加_ （![ 追加アイコン ](../assets/icon-add-green-circle.png)）をクリックし、`Customer Segment` を選択します。

     「修飾子」フィールドのデフォルトは `matches` です。

   - 「**...**」をクリックし、ターゲットにする顧客セグメントのセグメント ID を入力します。

     この例では、手順 1 で作成した新しいセグメントのセグメント ID は `2` です。

     >[!NOTE]
     >
     >セグメント ID が不明な場合は、選択アイコン（![ リストアイコン ](../assets/icon-list-chooser.png)）をクリックして、顧客セグメントリストを表示します。 フィールドに ID を手動で入力するか、目的のセグメントのチェックボックスを選択して、フィールドに自動入力できます。

   - 緑のチェックマーク（![ 緑のチェックマーク ](../assets/icon-checkmark-green-circle.png)）をクリックして、条件設定を保存します。

   - 完了したら、「**[!UICONTROL Save and Continue Edit]**」をクリックします。

     このルールの行は、顧客セグメント ID 2 に一致するすべての顧客に適用されます。

   ![ 顧客セグメントの状況 ](./assets/customer-segment-matches.png){width="400"}

1. 下にスクロールして、「![ 展開セレクター ](../assets/icon-display-expand.png)」 **[!UICONTROL Conditions]** クションを展開し、ルールのアクションを定義します。

   このセクションでは、初回顧客に適用する割引のタイプと値/金額を定義します。 この例では、定義された条件を満たすすべての顧客に対して 10% の割引を定義します。 その他の使用可能なオプションについては、[ 買い物かご価格ルールの作成 ](price-rules-cart-create.md) を参照してください。

   - **[!UICONTROL Apply]** しくは、「製品価格割引率」を選択します。

   - **[!UICONTROL Discount Amount]** には、`10` と入力します。

   - この価格ルールを製品金額にのみ適用するには、**[!UICONTROL Apply to Shipping Amount]** を `No` に設定します。

   - システムが同じ製品に複数の価格ルールを適用しないようにするには、**[!UICONTROL Discard Subsequent Rules]** を `Yes` に設定します。

   - 完了したら、「**[!UICONTROL Save]**」をクリックします。

   ![ 買い物かご価格ルールアクション ](./assets/actions-first-time.png){width="600" zoomable="yes"}

新しいルールは通常、1 時間以内に利用可能になります。 ルールをテストし、定義したとおりに機能することを確認します。

## 手順 3：ルールを保存してテストする

{{new-price-rule}}

1. ルールが完成したら、「**[!UICONTROL Save Rule]**」をクリックします。

1. ルールをテストして、正しく動作することを確認します。
