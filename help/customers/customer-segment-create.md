---
title: 顧客セグメントの作成および削除
description: お客様は、注文に関連する払い戻し情報を顧客アカウントダッシュボードで確認できます。
exl-id: 8a13271d-d0b5-4fc6-a701-3edfae04bfca
feature: Customers, Configuration
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# 顧客セグメントの作成および削除

{{ee-feature}}

顧客セグメントの作成は、オプションに [ 顧客セグメント固有の属性 ](../merchandising-promotions/price-rules-cart.md) が含まれることを除けば、[ 買い物かご価格ルール ](../customers/customer-segments.md) の作成に似ています。

![ 顧客セグメントリスト ](assets/customer-segments.png){width="700" zoomable="yes"}

_&#x200B;**[!UICONTROL Customer Segments]グリッド&#x200B;**&#x200B;_

| 列 | 説明 |
|--- |--- |
| **[!UICONTROL ID]** | 顧客セグメントの一意の ID。 |
| **[!UICONTROL Segment]** | 顧客セグメントの名前。 |
| **[!UICONTROL Status]** | 顧客セグメントが _[!UICONTROL Active]_&#x200B;か_[!UICONTROL Inactive]_ かを示します。 |
| **[!UICONTROL Website]** | 顧客セグメントが属する web サイトを示します。 |

{style="table-layout:auto"}

## 前提条件：顧客セグメントを有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Customer Configuration]**」を選択します。

1. 「**[!UICONTROL Customer Segments]**」セクションを展開します。

1. **[!UICONTROL Enable Customer Segment Functionality]** が `Yes` に設定されていることを確認します。

   ![ 顧客設定 – 顧客セグメント ](../configuration-reference/customers/assets/customer-configuration-customer-segments.png){width="600" zoomable="yes"}

1. （任意）顧客セグメントのリアルタイム検証を無効にするには、**[!UICONTROL Real-time Check if Customer is Matched by Segment]** を `No` に設定します。

   リアルタイム検証を無効にすると、顧客セグメントは、単一の組み合わせ条件 SQL クエリによって検証されます。 この機能を無効にすると、システム内に多数の顧客セグメントがある場合に、セグメント検証のパフォーマンスが向上します。 ただし、分割データベースを使用している場合や、登録済みの顧客が存在しない場合は、検証は機能しません。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## セグメントの作成

以下の手順では、ロサンゼルスの女性の顧客をターゲットとする顧客セグメントを作成する例を使用します。

### 手順 1：顧客セグメントの追加

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Segments]** に移動します。

1. 右上隅の「**[!UICONTROL Add Segment]**」をクリックします。

1. 管理者で作業する際の顧客セグメントを識別する **[!UICONTROL Segment Name]** を入力します。

1. セグメントの目的を説明する簡単な **[!UICONTROL Description]** を入力します。

1. 顧客セグメントを使用できる web サイトの **[!UICONTROL Assigned to Website]** を設定します。

1. **[!UICONTROL Status]** を _アクティブ_ または _非アクティブ_ に設定します。

1. セグメントの適用に使用する顧客タイプを識別するには、**[!UICONTROL Apply to]** を次のいずれかに設定します。

   - `Visitors and Registered Customers` - アカウントにログインしているかどうかに関係なく、すべての買い物客が含まれます。
   - `Registered Customers` - アカウントにログインしている買い物客のみを含めます。
   - `Visitors` - アカウントにログインしていない買い物客のみを含めます。

   >[!TIP]
   >
   >顧客アカウントに保存された顧客属性に基づいてセグメントを作成する場合は、登録済みの顧客にのみセグメントを適用することをお勧めします。

   >[!NOTE]
   >
   > セグメントが `Visitors and Registered Customers` に適用される場合、[!UICONTROL Matched Customers] には `Registered Customers` のみが表示されます。 これは、訪問者に適用される条件に基づいて訪問者をターゲットにできる場合でも当てはまります。 セグメント `Visitors` みの場合、`Matched Customers` タブは表示されません。


1. 「**[!UICONTROL Save and Continue Edit]**」をクリックします。

   セグメント _[!UICONTROL General Properties]_&#x200B;を保存すると、左パネルで追加のオプションが使用できるようになります。

   ![ セグメントのプロパティ ](assets/customer-segment-saved.png){width="600" zoomable="yes"}

**_[!UICONTROL General Properties]_**

| フィールド | 説明 |
|--- |---|
| **[!UICONTROL Segment Name]** | 内部参照用のセグメントを識別する名前。 |
| **[!UICONTROL Description]** | 内部参照用のセグメントの目的を説明する簡単な説明。 |
| **[!UICONTROL Assigned to Website]** | セグメントを使用できる単一の web サイト。 |
| **[!UICONTROL Status]** | セグメントをアクティブ化または非アクティブ化します。 関連する価格ルールとバナーは、セグメントが無効になると非アクティブになります。 オプション：`Active` / `Inactive` |
| **[!UICONTROL Apply to]** | セグメントを適用する顧客タイプを定義します。 選択は、セグメントの作成に使用できる一連の条件に影響を与えます。 セグメントを保存した後は、設定を変更できません。 |

{style="table-layout:auto"}

### 手順 2：条件の定義

>[!NOTE]
>
> 訪問者の場合は、次の条件のみを適用できます：買い物かごの条件（買い物かごの小計額、買い物かごの行項目、買い物かごの製品数）、製品ルール（買い物かごや製品履歴で見つかった製品）、およびこれらの項目の組み合わせ。 あるセグメントが訪問者と登録済み顧客の両方に適用される必要がある場合、訪問者はリストに表示された条件にのみ基づいて追跡されます。


1. 左側のウィンドウで、[**[!UICONTROL Conditions]**] をクリックします。

   デフォルトの条件はページの _[!UICONTROL If ALL of these conditions are TRUE:]_&#x200B;で始まります。

   ![ 条件 ](assets/customer-segment-conditions.png){width="600" zoomable="yes"}

1. 女性の顧客をターゲットにする条件を作成します。

   - **[!UICONTROL Add]** アイコンをクリックして条件のリストを表示し、「`Gender`」を選択します。

   - デフォルトの **is** 条件制御オプションはそのままにしておきます。

   - 「**...**」をクリックし、「`female`」を選択します。

   ![ 条件 1 行目 ](assets/customer-segment-condition-line1.png){width="600" zoomable="yes"}

1. ロサンゼルスの住民をターゲットにするもう 1 つの条件を作成します。

   - 次の行で、「**[!UICONTROL Add]**」アイコンをクリックし、「`Customer Address`」を選択します。

     このアクションにより、一致する 1 つ以上のアドレスフィールドを定義できる親条件が作成されます。

   - **[!UICONTROL Add]** アイコンをクリックしてアドレスフィールドのリストを表示し、「`City`」を選択します。

   - 「**is**」をクリックして条件制御オプションを表示し、`contains` を選択します。

   - 「**...**」をクリックし、`Los Angeles` と入力します。

   - 次の行で、「**[!UICONTROL Add]**」アイコンをクリックし、「`State/Province`」を選択します。

   - デフォルトの **is** 条件制御オプションはそのままにしておきます。

   - 「**...**」をクリックし、「`United States > California`」を選択します。

   ![ カリフォルニア州ロサンゼルスの女性の条件 ](assets/customer-segment-conditions-la-ladies.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save and Continue Edit]**」をクリックします。

### 手順 3：一致した顧客のリストの確認

1. 左側のウィンドウで、[**[!UICONTROL Matched Customers]**] をクリックすると、条件に一致するすべての顧客が表示されます。

   ![ マッチした顧客 ](assets/customer-segment-matched-customers.png){width="600" zoomable="yes"}

1. 顧客のリストが目標を満たしている場合は、「**[!UICONTROL Save]**」をクリックして顧客セグメントを完了します。

1. 顧客セグメントを使用して、プロモーション、コンテンツ、メールのターゲティングを行えるようになりました。

_&#x200B;**[!UICONTROL Matched Customers]グリッド&#x200B;**&#x200B;_

| 列 | 説明 |
|--- |--- |
| **[!UICONTROL ID]** | 登録済みの顧客の顧客 ID。 |
| **[!UICONTROL Name]** | 登録された顧客の名前。 |
| **[!UICONTROL Email]** | 登録された顧客の電子メールアドレス。 |
| **[!UICONTROL Group]** | 顧客が割り当てられている顧客グループ。 |
| **[!UICONTROL Phone]** | 顧客の電話番号。 |
| **[!UICONTROL ZIP]** | 顧客の郵便番号。 |
| **[!UICONTROL Country]** | 顧客が所在する国。 |
| **[!UICONTROL State / Province]** | 顧客が所在する都道府県。 |
| **[!UICONTROL Customer Since]** | 顧客アカウントが作成された日時。 |

{style="table-layout:auto"}

## 顧客セグメントの削除

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Segments]** に移動します。

1. 削除するセグメントを見つけて選択します。

1. メニューバーで、「」ボタン **[!UICONTROL Delete]** クリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。

## ボタンバー

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに _[!UICONTROL Customer Segments]_&#x200B;ページに戻ります。 |
| **[!UICONTROL Delete]** | 現在の顧客セグメントを削除します。 セグメント内の顧客に関連付けられている顧客または完了済み注文は削除されません。 |
| **[!UICONTROL Reset]** | 顧客セグメントフォーム内の未保存の変更を以前の値にリセットします。 |
| **[!UICONTROL Refresh Segment Data]** | セグメントデータを最近保存した値に更新します。 使用できないセグメントデータや古いセグメントデータがある場合に関連します。 |
| **[!UICONTROL Save and Continue Edit]** | 変更を保存し、顧客セグメントを開いたままにします。 |
| **[!UICONTROL Save]** | 変更を保存し、顧客セグメントを閉じます。 |

{style="table-layout:auto"}

## 顧客セグメントのデモ

顧客セグメントの作成に関するデモについては、このビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343659/?quality=12&learn=on)
