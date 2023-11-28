---
title: 買い物かごの価格ルールの作成
description: 買い物かごまたは製品属性に基づいて買い物かごの価格ルールを作成する方法を説明します。
exl-id: 7260e7c3-3b1e-43e5-9c09-c40538e37378
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: bf52884cb0eccd4d9c7326a95f8600a3ed950918
workflow-type: tm+mt
source-wordcount: '2885'
ht-degree: 0%

---

# 買い物かごの価格ルールの作成

次の手順を実行して、ルールを追加し、条件を説明し、アクションを定義します。 また、ラベルを入力し、ルールをテストします。 価格ルールの条件は、買い物かごまたは [製品属性](../catalog/product-attributes.md) または [Real-Time CDP Audiences](#use-real-time-cdp-audiences-to-set-a-condition)、ではない [カスタマイズ可能なオプション](../catalog/settings-advanced-custom-options.md).

## 手順 1：ルールを追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

1. クリック **[!UICONTROL Add New Rule]** 次の操作を実行します。

   - の下 _[!UICONTROL Rule Information]_、**[!UICONTROL Rule Name]**および&#x200B;**[!UICONTROL Description]**.

   - ルールをすぐに有効にしたくない場合は、 **[!UICONTROL Active]** から `No`.

   ![買い物かごの価格ルール — ルール情報](./assets/price-rule-cart-new.png){width="600" zoomable="yes"}

1. 次の手順で [範囲](../getting-started/websites-stores-views.md#scope-settings) ルールの次の操作を実行します。

   - を選択します。 **[!UICONTROL Websites]** プロモーションを使用できる場所。

   - を選択します。 **[!UICONTROL Customer Groups]** プロモーションを適用する先に設定します。

     プロモーションを登録済みの顧客のみに提供する場合は、 **_しない_** を選択します。 `NOT LOGGED IN` オプション。

1. 適用するルールを設定します。このルールは、 [クーポン](price-rules-cart-coupon.md) 次のように指定します。

   - クーポンコードを使用せずに買い物かごルールを適用するには、 **[!UICONTROL Coupon]** から `No Coupon` 次に、手順 5 に進みます。

   - クーポンを価格ルールに関連付けるには、 **[!UICONTROL Coupon]** から `Specific Coupon` 次の操作を実行します。

      - フリーテキストを入力 **[!UICONTROL Coupon Code]** 顧客が割引を受け取るために入力する必要があることを示します。

      - クーポンの使用回数に制限を設定するには、次のオプションを設定します。

     | オプション | 説明 |
     |------|-----------|
     | `Uses per Coupon` | クーポンコードを使用できる回数を決定します。 制限がない場合は、フィールドを空白のままにします。 |
     | `Uses per Customer` | 選択した顧客グループのいずれかに属する同じ登録済み顧客が買い物かごの価格ルールを使用できる回数を決定します。 この設定は、「ログインしていない」顧客グループのメンバーであるゲスト買い物客、または自分のアカウントにログインせずに買い物をする顧客には適用されません。 制限がない場合は、フィールドを空白のままにします。 |

     {style="table-layout:auto"}

     詳しくは、 [クーポンコード](price-rules-cart-coupon.md).

     ![買い物かごの価格ルール — クーポン設定](./assets/price-rule-cart-coupon-settings-ee.png){width="600" zoomable="yes"}

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) _カレンダー_ (![カレンダーアイコン](../assets/icon-calendar.png)) をクリックして、 **[!UICONTROL From]** および **[!UICONTROL To]** プロモーションの日付範囲。

1. 数値を入力して **[!UICONTROL Priority]** 」の値を、同時にアクティブな他の価格ルールの「アクション」設定と関連付けます。

   >[!NOTE]
   >
   >優先度設定は、2 つの買い物かごのルール/クーポンコードが同時に同じ製品に対して有効な場合に重要です。 優先度が最も高いルール (`1` が最も高い ) が、買い物かごのアクションを制御します。 詳しくは、 _後続の価格ルールの破棄_ （内） _アクションの定義_ 手順

   >[!NOTE]
   >
   >同じ優先度を持つ買い物かごの価格ルールでは、組み合わせ割引はおこなわれません。 各ルールは、対応する製品に対して 1 つずつ個別に適用されます。

1. ルールを公開済みに適用するには、以下を実行します。 [RSS フィード](social-rss.md#rss-feeds)，設定 **RSS フィード内の公開** から `Yes`.

1. クリック **[!UICONTROL Save and Continue Edit]**.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) ルールを保存すると、買い物かごの価格ルールの名前がページの上部に表示されます。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) ルールを保存した後、買い物かごの価格ルールの名前と [予定されている変更](price-rule-cart-scheduled-changes.md) 」ボックスがページの上部に表示されます。

     ![買い物かごの価格ルール — 予定変更](./assets/price-rule-cart-scheduled-changes.png){width="600" zoomable="yes"}

## 手順 2：条件の説明

この手順では、プロモーションの条件を満たす必要がある条件を説明します。 ルールは、条件のセットを満たすたびに実行されます。

Real-Time CDPのオーディエンスを使用している場合は、次にスキップ： [この節](#use-real-time-cdp-audiences-to-set-a-condition).

>[!NOTE]
>
>買い物かごの価格ルールは次の場所に適用されます。 **_各_** 買い物かごに含まれる商品で、 _[!UICONTROL Conditions]_」タブが表示されます。 条件を_[!UICONTROL Actions]_ タブをクリックして、買い物かごの価格ルールの影響を受ける製品の数を制限します。

>[!NOTE]
>
>1 つ以上の条件付き製品属性の値が空の場合、買い物かごの価格ルールは製品に適用されません。

1. 左のパネルで、「 」を選択します。 **[!UICONTROL Conditions]**.

   ![買い物かごの価格ルール — 条件](./assets/conditions.png){width="600" zoomable="yes"}

   最初の条件がデフォルトで表示され、次の状態になります。

   `If **ALL** of these conditions are **TRUE**:`

   ステートメントには 2 つの太字のリンクがあり、このリンクをクリックすると、ステートメントのその部分のオプションの選択を表示できます。 これらの値の組み合わせを変更することで、異なる条件を作成できます。 次のいずれかの操作を行います。

   - クリック **[!UICONTROL ALL]** を選択し、 `ALL` または `ANY`.
   - クリック **[!UICONTROL TRUE]** を選択し、 `TRUE` または `FALSE`.
   - 条件を変更せずに、すべての製品にルールを適用します。

1. クリック _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) をクリックし、買い物かご属性、製品の下位選択、組み合わせなど、条件のオプションを選択します。

   この例では、条件の次の部分を次のように完了します。

   - 次のプロンプトが表示された場合： **[!UICONTROL Choose the condition to add]**&#x200B;を選択します。 `Products Subselection`.

     ![買い物かご価格ルールの条件 — 製品の再選択](./assets/price-rule-cart-condition-products-subselection.png){width="600" zoomable="yes"}

   - 条件文で、 **[!UICONTROL total quantity]** を選択し、 `total quantity` または `total amount`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Total amount] は行の合計なので、税は `total amount` （の） [!UICONTROL Products Subselection] 買い物かごの価格ルール条件。 以下を使用します。 [!UICONTROL Subtotal (Incl. Tax)] 税込み条件。

   - 条件文で、 **[!UICONTROL is]** を選択し、 `greater than`.

1. 条件の次の部分が表示されたら、文の要素をクリックし、変数値を持つ各リンクの場所を確認できます。

1. 「その他」(...) リンクをクリックし、「 `100`.

   この条件では、買い物かごの合計数量が `101` 以上

   ![買い物かごの価格ルール条件 — 合計数量の値](./assets/condition-products-subselection3.png){width="600" zoomable="yes"}

1. クリック **追加** (![追加アイコン](../assets/icon-add-green-circle.png)) を次の行の先頭に追加し、 **カテゴリ**.

   ![買い物かごの価格ルール条件 — 製品属性カテゴリ](./assets/condition-products-subselection4.png){width="600" zoomable="yes"}

1. 条件の次の部分で、 _その他_ (**...**) リンクをクリックして入力フィールドを表示し、 _選択_ (![リストアイコン](../assets/icon-list-chooser.png)) をクリックして、カテゴリツリーを表示します。

1. 価格ルールの条件として使用するカテゴリのチェックボックスを選択し、 ![追加アイコン](../assets/icon-checkmark-green-circle.png) アイコンをクリックして、カテゴリの選択を受け入れます。

   条件は、ストアの [ルートカテゴリ](../catalog/category-root.md).

   ![買い物かご価格ルールの条件 — 製品カテゴリ](./assets/subselection-category.png){width="600" zoomable="yes"}

1. 条件を追加するには、 _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) をクリックし、別の条件を定義します。

   この処理を必要な回数だけ繰り返し、価格ルールで満たす必要のある条件を説明できます。 次に例を示します。

   **例 1:** 地域別価格ルール

   地域の価格ルールを作成するには、次の買い物かご属性のいずれかを使用します。

   - `Shipping Postcode`
   - `Shipping Region`
   - `Shipping State/Province`
   - `Shipping Country`

   **例 2:** 買い物かごの合計

   買い物かごの合計に基づく条件を設定するには、次の買い物かご属性の 1 つを使用します。

   - `Subtotal`
   - `Total Items Quantity`
   - `Total Weight`

>[!NOTE]
>
>複数の並列プロモーションの場合、 _小計_ 条件が _ベース_ 買い物かごの小計 **_前_** 割引。

>[!IMPORTANT]
>
>**発注書のみ**:1 つ以上の特定の支払い方法に基づいて買い物かごの価格ルールを設定すると、発注書の作成時に合計に割引が適用されます。 発注書の作成後、支払い方法が買い物かごの価格ルールの対象でない支払い方法に変更された場合、割引は合計に適用されたままになります。

### 製品属性を買い物かごの価格ルールに追加

1. に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**製品属性を開きます。

1. 左のパネルで、「 」を選択します。 **[!UICONTROL Storefront Properties]**.

1. 設定 **[!UICONTROL Use for Promo Rule Conditions]** から `Yes`.

1. クリック **[!UICONTROL Save Attribute]**.

1. に移動します。 **[!UICONTROL Marketing]** > **[!UICONTROL Cart Price Rules]** 必要な買い物かごの価格ルールを開きます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Condition]** 「 」セクションで「 」を選択します。 **[!UICONTROL Product attribute combination]**.

1. この条件を次のいずれかの値に設定します。

   - クリック **[!UICONTROL FOUND]** を選択し、 `FOUND` または `NOT FOUND`.

   - クリック **[!UICONTROL ALL]** を選択し、 `ALL` または `ANY`.

1. 次をクリック： _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) アイコンをクリックし、「 **[!UICONTROL Product Attribute]** プロモーションルール条件用に設定した

1. クリック **[!UICONTROL Save]**.

>[!NOTE]
>
>を使用する場合、 `is not one of` ～との条件 _SKU_ 製品属性と設定可能な製品（親製品 SKU と子製品 SKU の両方を選択する必要があります）。 ルール内のすべての子 SKU がリストされないようにするには、 `does not contain` 設定可能な製品とその子製品の共通の SKU 部分を使用した条件。

### Real-Time CDPオーディエンスを使用した条件の設定

Real-Time CDPに基づく買い物かごの価格ルールの条件を設定できます [audience](../customers/audience-activation.md).

1. 展開 **[!UICONTROL Conditions]**&#x200B;をクリックし、「+」アイコンをクリックして、 **[!UICONTROL Real-Time CDP Audience]** を選択します。

   ![Real-Time CDP Audience Condition を選択](./assets/rtcdp-conditions.png){width="300"}

1. を選択します。 _その他_ (**...**) アイコンをクリックし、 **[!UICONTROL Open Chooser]**&#x200B;をクリックし、使用可能なすべてのReal-Time CDPオーディエンスを表示します。

   ![Real-Time CDP Audiences の表示](./assets/rtcdp-conditions-chooser.png){width="600" zoomable="yes"}

1. 買い物かごの価格ルールに使用するReal-Time CDPオーディエンスを選択します。

   | オプション | 説明 |
   |------|-----------|
   | `ID` | 管理者内で使用されるオーディエンスの内部識別子 |
   | `Real-Time CDP Audience ID` | オーディエンスがExperience Platformで作成された際の一意の識別子 |
   | `Name` | オーディエンスの名前（例： ） `Orders over $50` |
   | `Description` | オーディエンスの説明（例： ） `People who placed an order over $50 in the last month.`. |
   | `Source` | オーディエンスがどこから来たかを示します（例： ）。 `Experience Platform`. |
   | `Website` | オーディエンスを含むデータストリームにリンクした Web サイトを示します。 このリンクは、 [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html) 拡張子。 |

   {style="table-layout:auto"}

次の手順では、条件が満たされた場合に実行されるアクションを定義します。

## 手順 3：アクションの定義

買い物かごの価格ルールアクションでは、条件が満たされた場合の価格の更新方法を説明します。

1. 下にスクロールして **[!UICONTROL Actions]**、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) 「 」セクションに表示されます。

   ![買い物かごの価格ルール — アクション ](./assets/price-rule-cart-actions.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Apply]** を次のいずれかの割引オプションに設定します。

   | オプション | 説明 |
   |------|-----------|
   | `Percent of product price discount` | 元の価格から割合を引くことによる割引品目。 割引は、買い物かご内の各対象品目に適用されます。 例： `10` in [!UICONTROL Discount Amount] 元の価格より 10%安い更新価格。 |
   | `Fixed amount discount` | 割引品目。買い物かご内の対象となる各品目の元の価格から固定金額を引きます。 例： `10` in [!UICONTROL Discount Amount] 元の価格より 10 ドル安い更新価格。 |
   | 買い物かご全体の固定金額の割引 | 買い物かごの合計から固定金額を引くことで、買い物かご全体の割引を行います。 例： 10 in と入力します。 [!UICONTROL Discount Amount] 買い物かごの合計から$10 を引きます。 デフォルトでは、割引は買い物かごの小計にのみ適用されます。 割引を小計と配送に別々に適用するには、 _[!UICONTROL Apply to Shipping Amount]_オプション。 |
   | `Buy X get Y free` | 顧客が無料で数量を受け取るために購入する必要がある数量を定義します。 ( [!UICONTROL Discount Amount] は Y) |

   {style="table-layout:auto"}

   - 次を入力します。 **[!UICONTROL Discount Amount]** 数値（記号なし） 例えば、選択した割引オプションに応じて、数値 10 は、割合、固定金額または品目の数量を示します。

   - の _X を購入 Y を無料で取得_ 割引：数量を **[!UICONTROL Discount Qty Step (Buy X)]** 顧客が割引を受けるために購入する必要があるフィールド。

   - Adobe Analytics の **[!UICONTROL Maximum Qty Discount is Applied To]** 「 」フィールドに、同じ購入で割引を受けることができる同じ製品の最大数量を入力します。

   - 設定 **[!UICONTROL Apply to Shipping Amount]** (![オプション切り替え](../assets/toggle-yes.png)) を次のように指定します。

     | オプション | 説明 |
     |------|-----------|
     | `Yes` | 割引額を小計と配送額に個別に適用します。 |
     | `No` | 割引額を小計にのみ適用します。 |

     {style="table-layout:auto"}

   - このルールの適用後に他のルールの処理を停止するには、 **[!UICONTROL Discard Subsequent Rules]** (![オプション切り替え](../assets/toggle-yes.png)) から `Yes`. この設定は、同じ製品に複数の割引が適用されるのを防ぎます。

     | オプション | 説明 |
     |------|-----------|
     | `Yes` | 製品に適用される他の価格ルールが適用されるのを防ぎます。 複数の価格設定ルールが同じ製品に適用される場合、（ルール内で）最も優先度が高い価格設定ルールのみ [!UICONTROL Priority] 」フィールド ) が、対象となる製品に適用されます。 これにより、複数の価格ルールが積み重ならず、意図しない追加の割引が適用されるのを防ぎます。 |
     | `No` | 同じ製品に複数の価格ルールを適用できます。 その結果、積み重ねをおこない、上場価格に複数の割引を適用することができます。 |

     {style="table-layout:auto"}

     >[!IMPORTANT]
     >
     >以降のルールを破棄するには、価格設定ルールで各ルールの「優先度」フィールドで設定された定義済みの優先度を使用し、複数のルールで同じ優先度を定義しないようにする必要があります。 詳しくは、 **[!UICONTROL Priority]** （内） _新しいルールを追加_ 手順

1. 次の手順で **_正確_** 買い物かごの価格ルールの影響を受ける製品については、 **_追加_** アクションに必要な条件。

   条件を満たす注文に送料無料が適用されるかどうかを判断するには、 **[!UICONTROL Free Shipping]** を次のいずれかに変更します。

   | オプション | 説明 |
   |------|-----------|
   | `No` | 送料は無料です。 |
   | `For matching items only` | 送料無料は、ルールの条件に一致する品目に対してのみ利用できます。 |
   | `For shipment with matching items` | 該当する品目を含むすべての出荷に対して、無料の出荷が可能です。 The [送料無料](../stores-purchase/shipping-free.md) このオプションを使用するには、配信方法を有効にする必要があります。 |

   {style="table-layout:auto"}

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) **[!UICONTROL Add Rewards Points]**、顧客が獲得した固定ポイント数を入力します **_1 回_** ご注文ごと（買い物かごの価格ルールが適用される際に使用）

   報酬ポイントが有効になっていない場合、このフィールドは空白のままにします。

1. 完了したら、「 **[!UICONTROL Save and Continue Edit]**.

## 手順 4：ラベルを完成させる

ラベルは、割引を識別するために、注文の「合計」セクションに表示されます。 ラベルのテキストは、単語の後の丸括弧で囲まれます `Discount`. すべての店舗ビューにデフォルトのラベルを入力するか、ビューごとに異なるラベルを入力できます。

![ストアフロント買い物かご — 割引ラベル](./assets/order-totals-section-discount-special.png){width="600"}

1. 下にスクロールして **[!UICONTROL Labels]**、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png)「 」セクションに表示されます。

1. として使用するテキストを入力します。 **[!UICONTROL Default Rule Label for All Store Views]**.

   ![買い物かごの価格ルール — デフォルトラベル](./assets/label-default.png){width="600" zoomable="yes"}

1. ストアに複数のビューがある場合、または複数のビューを持つ複数の Web サイトの場合は、それぞれに適したラベルテキストを入力します。

   例えば、各ストア表示が異なる言語の場合、各表示のラベルの翻訳を入力します。

   ![特定のラベルを保存](./assets/label-store-specific.png){width="600" zoomable="yes"}

## 手順 5：関連する動的ブロックの追加（オプション）

{{ee-feature}}

[動的ブロック](../content-design/dynamic-blocks.md) ルールに関連付けられているは、条件が満たされるたびにストアフロントに表示されます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Related Dynamic Blocks]** 」セクションに入力します。

1. 以下を使用します。 [検索フィルター](../getting-started/admin-workspace.md) をクリックして、ルールに関連付けるブロックを見つけます。

1. ブロックをルールに関連付けるには、最初の列のチェックボックスをオンにします。

   詳しくは、 [価格ルールの動的ブロック](../content-design/dynamic-blocks-price-rules.md).

## 手順 6：ルールを保存してテストする

1. 完了したら、「 **[!UICONTROL Save Rule]**.

1. ルールをテストして、正しく動作することを確認します。

   価格ルールは、他のシステムルールと共に毎晩自動的に処理されます。 価格ルールを作成する場合は、システムに取り込むのに十分な時間を割いてください。 また、ルールをテストして、正しく動作することを確認します。 新しいルールが追加されると、Commerce は価格と優先度をそれに応じて再計算します。

## 買い物かご価格ルールのデモ

このビデオでは、買い物かごの価格ルールの作成について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/343835?quality=12)

## フィールドの説明

### [!UICONTROL Rule Information]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Rule Name] | （必須）ルールの名前は内部参照用です。 |
| [!UICONTROL Description] | ルールの説明には、ルールの目的と、ルールの使用方法を説明する必要があります。 |
| [!UICONTROL Active] | （必須）ルールがストア内でアクティブかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Websites] | （必須）ルールを使用できる Web サイトを識別します。 |
| [!UICONTROL Customer Groups] | （必須）ルールを適用する顧客グループを識別します。 |
| [!UICONTROL Coupon] | （必須）クーポンがルールに関連付けられているかどうかを示します。 オプション： <br/>**[!UICONTROL No Coupon]**— ルールにクーポンが関連付けられていません。<br/>**[!UICONTROL Specific Coupon]**  — 特定のクーポンはルールに関連付けられます。 <br/>**[!UICONTROL Coupon Code]**— プロモーションを活用するために顧客が入力する必要がある「クーポンコード」を入力します。<br/>**[!UICONTROL Use Auto Generation]** - 「 」チェックボックスを選択すると、プロモーションで使用できる複数のクーポンコードが自動的に生成されます。 <br/>**[!UICONTROL Auto]**- _[!UICONTROL Manage Coupon Codes]_セクションを使用して、生成するクーポンコードの形式を定義します。 |
| [!UICONTROL Uses per Coupon] | クーポンコードを使用できる回数を決定します。 制限がない場合は、フィールドを空白のままにします。 |
| [!UICONTROL Uses per Customer] | 選択した任意の顧客グループに属する同じ登録済み顧客が買い物かごの価格ルールを使用できる回数を決定します。 NOT LOGGED IN 顧客グループのメンバーであるゲスト買い物客、または自分のアカウントにログインせずに買い物をする顧客には適用されません。 制限なしの場合は、空白のままにします。 |
| [!UICONTROL Priority] | 他のルールに対するこのルールの優先度を示す数値。 最も優先度が高いのは数値です `1`. |
| [!UICONTROL Public in RSS Feed] | プロモーションをストアのパブリック RSS フィードに含めるかどうかを指定します。 オプション：  `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) クーポンを使用できる最初の日付。 |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Sourceのみ ) クーポンを使用できる最終日。 |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

買い物かごの価格ルールが実行される前に満たす必要がある条件を指定します。 空白の場合、ルールはカート内のすべての製品に適用されます。 条件は、買い物かごと製品属性の任意の組み合わせに基づいて設定できます。 しかし、 [カスタマイズ可能なオプション](../catalog/settings-advanced-custom-options.md) を買い物かごの価格ルール条件で参照することはできません。

### [!UICONTROL Actions]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Apply] | 購入に適用される計算のタイプを決定します。 オプション： <br/>**[!UICONTROL Percent of product price discount]**— 元の価格から割合を引くことで割引品目。 例： `10` in _[!UICONTROL Discount Amount]_元の価格より 10%安い更新価格。<br/>**[!UICONTROL Fixed amount discount]**— 買い物かご内の対象となる各品目の元の価格から固定金額を引くことによる割引品目。 例： `10` in_[!UICONTROL Discount Amount]_ 元の価格より 10 ドル安い更新価格。 <br/>**[!UICONTROL Fixed amount discount for whole cart]**— 買い物かごの小計から固定金額を引くことで、買い物かご全体の割引を行います。 例： `10` in _[!UICONTROL Discount Amount]_買い物かごの小計から$10 を減算する場合。 デフォルトでは、割引は買い物かごの小計にのみ適用されます。 割引を小計と配送に別々に適用するには、_発送金額に適用&#x200B;_.<br/>**[!UICONTROL Buy X Get Y Free (discount amount is Y)]**— 顧客が無料で受け取る数量を定義します。 (_[!UICONTROL Discount Amount]_ は Y) |
| [!UICONTROL Discount Amount] | （必須）提供される割引の金額。 |
| [!UICONTROL Maximum Qty Discount is Applied To] | 同じ購入で割引を適用できる製品の最大数を設定します。 |
| [!UICONTROL Discount Qty Step (Buy X)] | で表される製品の数を設定します。 `X` 内 `Buy X Get Y Free` 昇格。 |
| [!UICONTROL Apply to Shipping Amount] | 割引を小計と送料に別々に適用するかどうかを指定します。 それ以外の場合は、小計にのみ適用されます。 オプション： `Yes` / `No` |
| [!UICONTROL Discard Subsequent Rules] | この買い物かごの価格ルールが一致する場合に、低い優先度ルール（1 が最も高い優先度）を製品に適用できるかどうかを指定します。 同じ製品に複数の割引が適用されないようにするには、このオプションを有効にします。 オプション： `Yes` / `No` |
| [!UICONTROL Free Shipping] | プロモーションに送料が含まれるかどうか、および含まれる場合はその品目を指定します。 オプション： <br/>**[!UICONTROL No]**— 現在のルールでは、送料は無料です。<br/>**[!UICONTROL For matching items only]**  — 無料配送は、ルールに一致する買い物かご内の特定の品目に対してのみ利用できます。 <br/>**[!UICONTROL For shipment with matching items]**— カート内のすべての品目に無料で送料を提供します。 The [送料無料](../stores-purchase/shipping-free.md) このオプションを使用するには、配信方法を有効にする必要があります。 |
| [!UICONTROL Add Reward Points] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) [報酬ポイント](rewards-loyalty.md) 価格ルールが適用されるたびに顧客が獲得する。 |

{style="table-layout:auto"}

### [!UICONTROL Labels]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Default Rule Label for All Store Views] | 割引を識別するデフォルトのラベルで、すべてのストア表示に使用できます。 |
| [!UICONTROL Store View Specific Labels] | 該当する場合は、異なるラベルを指定して、各店舗ビューの割引を識別します。 |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

任意の [動的ブロック](../content-design/dynamic-blocks.md) ルールに関連付けられている
