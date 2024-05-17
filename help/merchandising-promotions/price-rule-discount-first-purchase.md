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

- として定義された顧客セグメントの作成 _注文のない買い手_、次に
- 新しい顧客セグメントをターゲットにする買い物かご価格ルールを作成します。

>[!NOTE]
>
>顧客セグメント機能が有効になっていることを確認します。 こちらを参照してください [顧客セグメントの作成](../customers/customer-segment-create.md).

## 手順 1. 顧客セグメントの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Segment]**.

1. の定義 **[!UICONTROL General Properties]**.

   - を入力 **[!UICONTROL Segment Name]** 顧客セグメントを識別する手順は次のとおりです（例： _初めての顧客_）に設定します。

   - の場合 **[!UICONTROL Assigned to Website]**&#x200B;を選択し、顧客セグメントを使用できる web サイトを選択します。

   - の場合 **[!UICONTROL Status]**&#x200B;を選択 `Active`.

   - の場合 **[!UICONTROL Apply to]**&#x200B;を選択 `Visitors and Registered Customers`.

   - 完了したら、 **[!UICONTROL Save and Continue Edit]**.

     左側のパネルで、追加のオプションを使用できるようになります。

   ![顧客セグメントプロパティ](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. の定義 **[!UICONTROL Conditions]**.

   この例では、条件は次の条件を満たす顧客をターゲットにします _合計注文数が 1 未満_ が true である。

   - 左側のパネルで、を選択します。 **[!UICONTROL Conditions]**.

     デフォルトの条件は、「これらの条件がすべて TRUE の場合」から始まります。

   - クリック _追加_ （![アイコンを追加](../assets/icon-add-green-circle.png)）に設定し、 `Number of Orders`.

   - クリック **[!UICONTROL is]** を選択して、 `less than`.

   - クリック **...** を入力します `1` フィールドに移動します。

   - 緑のチェックマーク（ ![緑のチェックマーク](../assets/icon-checkmark-green-circle.png) ）を選択して、条件設定を保存します。

   ![顧客セグメントの条件](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.

顧客セグメントが作成され、に表示されます _[!UICONTROL Customer Segments]_グリッド。

>[!TIP]
>
>セグメント ID をメモします。 この ID 番号を使用して、買い物かご価格ルールを作成します。

## 手順 2. 買い物かご価格ルールの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Rule]**.

   この **[!UICONTROL Rule Information]** 既定では、セクションが表示され、展開可能なセクションが表示されます **[!UICONTROL Conditions]** および **[!UICONTROL Conditions]**.

1. の定義 **[!UICONTROL Rule Information]**.

   - を完了する **[!UICONTROL Rule Name]** および **[!UICONTROL Description]** フィールド。 これらのフィールドは内部参照用です。

   - の場合 **[!UICONTROL Websites]**&#x200B;で、ルールを使用できる web サイトを選択します。

   - の場合 **[!UICONTROL Customer Groups]**&#x200B;で、このルールを適用する顧客グループを選択します。

     複数のグループを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

     >[!NOTE]
     >
     >このリストのオプションは、で作成および管理する顧客グループによって異なります **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - の場合 **[!UICONTROL Coupon]**&#x200B;を選択 `No Coupon`.

   - の場合 **[!UICONTROL Uses per Customer]**、と入力します `1`.

   - の場合 **[!UICONTROL Priority]**&#x200B;を入力し、他のルールと比較してこのルールの優先度を決定します。

     >[!NOTE]
     >
     >同じカタログ製品が複数の価格ルールに設定された条件を満たす場合、優先度設定は重要です。 優先度の設定が最も高いルールが、顧客に対してアクティブになります。 優先度は最大で 1 です。 この例では、と入力します。 `1` は、このルールが他の価格ルールの前に適用されることを意味します。 これは、 **[!UICONTROL Discard Subsequent Rules]** での設定 **[!UICONTROL Action]** セクション。

   - 完了したら、 **[!UICONTROL Save and Continue Edit]**.

     左側のパネルで、追加のオプションを使用できるようになります。

   ![買い物かご価格ルールの情報](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. の定義 **[!UICONTROL Conditions]**.

   - 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Conditions]** セクション。

     デフォルトのルールは、「これらの条件がすべて TRUE の場合：」から始まります。

   - クリック _追加_ （![アイコンを追加](../assets/icon-add-green-circle.png)）に設定し、 `Customer Segment`.

     「修飾子」フィールドのデフォルトはです。 `matches`.

   - クリック **...** ターゲット設定したい顧客セグメントのセグメント ID を入力します。

     この例では、手順 1 で作成した新しいセグメントのセグメント ID はです。 `2`.

     >[!NOTE]
     >
     >セグメント ID が不明な場合は、選択アイコン（ ![リストアイコン](../assets/icon-list-chooser.png) ）を選択して、顧客セグメントリストを表示します。 フィールドに ID を手動で入力するか、目的のセグメントのチェックボックスを選択して、フィールドに自動入力できます。

   - 緑のチェックマーク（ ![緑のチェックマーク](../assets/icon-checkmark-green-circle.png) ）を選択して、条件設定を保存します。

   - 完了したら、 **[!UICONTROL Save and Continue Edit]**.

     このルールの行は、顧客セグメント ID 2 に一致するすべての顧客に適用されます。

   ![顧客セグメントの条件](./assets/customer-segment-matches.png){width="400"}

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png)この **[!UICONTROL Conditions]** セクションに移動して、ルールのアクションを定義します。

   このセクションでは、初回顧客に適用する割引のタイプと値/金額を定義します。 この例では、定義された条件を満たすすべての顧客に対して 10% の割引を定義します。 その他の使用可能なオプションについては、を参照してください [買い物かご価格ルールの作成](price-rules-cart-create.md).

   - の場合 **[!UICONTROL Apply]**、製品価格割引の割合を選択します。

   - の場合 **[!UICONTROL Discount Amount]**、と入力します `10`.

   - この価格ルールを製品金額にのみ適用するには、次の値を設定します **[!UICONTROL Apply to Shipping Amount]** 対象： `No`.

   - システムが同じ製品に複数の価格ルールを適用しないようにするには、次のように設定します **[!UICONTROL Discard Subsequent Rules]** 対象： `Yes`.

   - 完了したら、 **[!UICONTROL Save]**.

   ![買い物かご価格ルールアクション](./assets/actions-first-time.png){width="600" zoomable="yes"}

新しいルールは通常、1 時間以内に利用可能になります。 ルールをテストし、定義したとおりに機能することを確認します。

## 手順 3：ルールを保存してテストする

{{new-price-rule}}

1. ルールが完了したら、 **[!UICONTROL Save Rule]**.

1. ルールをテストして、正しく動作することを確認します。
