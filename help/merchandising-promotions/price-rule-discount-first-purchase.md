---
title: 買い物かごの価格ルールの例 — 初回購入時の割引
description: 買い物かごの価格ルールを使用して初めての顧客に割引を提供する例を確認します。
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# 買い物かごの価格ルールの例 — 初回購入時の割引

{{ee-feature}}

買い物かごの価格ルールを使用すると、クーポンを必要とせずに、最初の購入時に顧客に割引を自動的にオファーできます。

初めての顧客に対して割引を提供するには、次の操作を実行します。

- 次のように定義された顧客セグメントの作成 _注文のない購入者_&#x200B;を、
- 新しい顧客セグメントをターゲットにする買い物かごの価格ルールを作成します。

>[!NOTE]
>
>顧客セグメント機能が有効になっていることを確認します。 参照： [顧客セグメントの作成](../customers/customer-segment-create.md).

## 手順 1. 顧客セグメントの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. 右上隅で、 **[!UICONTROL Add Segment]**.

1. 次を定義： **[!UICONTROL General Properties]**.

   - を入力します。 **[!UICONTROL Segment Name]** 顧客セグメントを特定する ( 例： _初めての顧客_) をクリックします。

   - の場合 **[!UICONTROL Assigned to Website]**「 」で、顧客セグメントを使用できる Web サイトを選択します。

   - の場合 **[!UICONTROL Status]**&#x200B;を選択します。 `Active`.

   - の場合 **[!UICONTROL Apply to]**&#x200B;を選択します。 `Visitors and Registered Customers`.

   - 完了したら、「 **[!UICONTROL Save and Continue Edit]**.

     左側のパネルで、追加のオプションを使用できるようになります。

   ![顧客セグメントのプロパティ](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. 次を定義： **[!UICONTROL Conditions]**.

   この例では、条件は、の顧客をターゲットにします。 _合計注文数が 1 未満です_ が True の場合は無効です。

   - 左側のパネルで、を選択します。 **[!UICONTROL Conditions]**.

     デフォルトの条件は、「次の条件のすべてが TRUE の場合：」と表示されます。

   - クリック _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) をクリックし、「 `Number of Orders`.

   - クリック **[!UICONTROL is]** を選択し、 `less than`.

   - クリック **...** と入力します。 `1` 」と入力します。

   - 緑のチェックマーク ( ![緑のチェックマーク](../assets/icon-checkmark-green-circle.png) ) をクリックして、条件の設定を保存します。

   ![顧客セグメント条件](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.

顧客セグメントが作成され、 _[!UICONTROL Customer Segments]_グリッド。

>[!TIP]
>
>セグメント ID をメモしておきます。 この ID 番号を使用して、買い物かごの価格ルールを作成します。

## 手順 2. 買い物かごの価格ルールを作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. 右上隅で、 **[!UICONTROL Add New Rule]**.

   The **[!UICONTROL Rule Information]** セクションはデフォルトで表示され、次のセクションが拡大可能です： **[!UICONTROL Conditions]** および **[!UICONTROL Conditions]**.

1. 次を定義： **[!UICONTROL Rule Information]**.

   - 次を完了： **[!UICONTROL Rule Name]** および **[!UICONTROL Description]** フィールド。 これらのフィールドは、内部参照用です。

   - の場合 **[!UICONTROL Websites]**」で、ルールを使用できる Web サイトを選択します。

   - の場合 **[!UICONTROL Customer Groups]**「 」で、このルールを適用する顧客グループを選択します。

     複数のグループを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

     >[!NOTE]
     >
     >このリストのオプションは、で作成および管理する顧客グループによって異なります。 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - の場合 **[!UICONTROL Coupon]**&#x200B;を選択します。 `No Coupon`.

   - の場合 **[!UICONTROL Uses per Customer]**，と入力します。 `1`.

   - の場合 **[!UICONTROL Priority]**」と入力し、他のルールとの関連でこのルールの優先度を設定する数値を入力します。

     >[!NOTE]
     >
     >同じカタログ製品が複数の価格ルールに設定された条件を満たす場合、優先度設定は重要です。 優先度が最も高いルールが、顧客に対してアクティブになります。 最も優先度が高いのは 1 です。 この例では、 `1` は、このルールが他の価格ルールより前に適用されることを意味します。 この値は、 **[!UICONTROL Discard Subsequent Rules]** 設定を **[!UICONTROL Action]** 」セクションに入力します。

   - 完了したら、「 **[!UICONTROL Save and Continue Edit]**.

     左側のパネルで、追加のオプションを使用できるようになります。

   ![買い物かごの価格ルール情報](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. 次を定義： **[!UICONTROL Conditions]**.

   - 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Conditions]** 」セクションに入力します。

     デフォルトのルールは、「If ALL of these conditions is TRUE:」と表示されます。

   - クリック _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) をクリックし、「 `Customer Segment`.

     クオリファイアフィールドのデフォルト値はです。 `matches`.

   - クリック **...** をクリックし、ターゲットにする顧客セグメントのセグメント ID を入力します。

     この例では、手順 1 で作成した新しいセグメントのセグメント ID はです。 `2`.

     >[!NOTE]
     >
     >セグメント ID が不明な場合は、選択アイコン ( ![リストアイコン](../assets/icon-list-chooser.png) ) をクリックして、顧客セグメントリストを表示します。 フィールドに ID を手動で入力するか、目的のセグメントのチェックボックスをオンにしてフィールドに自動入力できます。

   - 緑のチェックマーク ( ![緑のチェックマーク](../assets/icon-checkmark-green-circle.png) ) をクリックして、条件の設定を保存します。

   - 完了したら、「 **[!UICONTROL Save and Continue Edit]**.

     このルールの行は、顧客セグメント ID 2 に一致するすべての顧客に適用されます。

   ![顧客セグメント条件](./assets/customer-segment-matches.png){width="400"}

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png)の **[!UICONTROL Conditions]** 」セクションに移動して、ルールのアクションを定義します。

   このセクションでは、初めての顧客に適用する割引のタイプと値/金額を定義します。 次の例では、定義された条件を満たすすべての顧客に対して 10%の割引を定義します。 使用可能なその他のオプションについて詳しくは、 [買い物かごの価格ルールの作成](price-rules-cart-create.md).

   - の場合 **[!UICONTROL Apply]**、製品価格の割引のパーセントを選択します。

   - の場合 **[!UICONTROL Discount Amount]**，と入力します。 `10`.

   - この価格ルールを製品金額にのみ適用するには、 **[!UICONTROL Apply to Shipping Amount]** から `No`.

   - システムが同じ製品に複数の価格ルールを適用しないようにするには、 **[!UICONTROL Discard Subsequent Rules]** から `Yes`.

   - 完了したら、「 **[!UICONTROL Save]**.

   ![買い物かご価格ルールのアクション](./assets/actions-first-time.png){width="600" zoomable="yes"}

新しいルールは、通常、1 時間以内に利用できます。 ルールをテストし、定義したとおりに動作することを確認します。

## 手順 3：ルールを保存してテストする

{{new-price-rule}}

1. ルールが完了したら、「 **[!UICONTROL Save Rule]**.

1. ルールをテストして、正しく動作することを確認します。
