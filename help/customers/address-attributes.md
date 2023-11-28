---
title: 顧客住所属性
description: 顧客アドレス属性と、これらの属性プロパティの設定方法について説明します。
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%

---

# 顧客住所属性

{{ee-feature}}

顧客の住所属性セットによって、 [アドレス帳](account-dashboard-address-book.md) 顧客のアカウントから、または [checkout](../stores-purchase/checkout-process.md).

カスタムアドレス属性を設定して、オプションのメールアドレス、Skype アカウント、代替電話番号、建物、国などの追加情報を提供することができます。 その後、カスタム属性を [アドレステンプレート](address-templates.md) 販売書類の作成に使用される カスタムアドレス属性を作成するプロセスは、 [顧客属性](attribute-properties.md).

顧客アドレス属性は、次の形式で使用されます。

- [顧客の住所の登録](account-create.md)
- [顧客アカウントの住所](account-dashboard-address-book.md)

![管理者 — 顧客住所属性](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## 手順 1：属性プロパティの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**.

1. 右上隅で、 **[!UICONTROL Add New Attribute]**.

   ![顧客属性プロパティ](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Attribute Properties]** セクションで、以下の操作を実行します。

   - を入力します。 **[!UICONTROL Default Label]** は、データ入力時に属性を識別します。

   - を入力します。 **[!UICONTROL Attribute Code]** は、システム内の属性を識別します。

     属性コードは、文字で始まる必要があり、小文字 (a ～ z) と数字 (0 ～ 9) の任意の組み合わせを含めることができます。 コードの長さは 30 文字未満にする必要があり、特殊文字やスペースを含めることはできません。 アンダースコア文字 (_) は、スペースを示すために使用できます。

     >[!TIP]
     >
     >**_ショートカット：_** 必須フィールドのみを入力するには、下にスクロールして [!UICONTROL Storefront Properties]、 [!UICONTROL Sort Order]、をクリックして保存します。

1. データ入力に使用される入力コントロールの種類を判断するには、 **[!UICONTROL Input Type]** を次のいずれかに変更します。

   - `Text Field` - 1 行のテキストフィールド。
   - `Text Area`  — 複数行のテキスト領域。
   - `Multiple Line`  — 複数行の番地に似た、属性に対して複数のテキスト行を作成します。 データ入力行の数は、2 ～ 20 の範囲で指定できます。 以下を使用します。 `Default Value` をクリックして、フィールドの初期値を指定します。
   - `Date`  — ポップアップカレンダー付きの日付フィールドを表示します。 追加のプロパティ：を使用します。 `Default Value` をクリックして、フィールドの初期値を指定します。 <br/>用途 `Minimal Value` ：入力可能な最も早い日付を指定します。  用途 `Maximum Value` をクリックして、入力可能な最新の日付を指定します。
   - `Dropdown` - 1 つの値のみを選択できるドロップダウンリスト。
   - `Multiple Select`  — 複数の値を選択できるドロップダウンリスト。
   - `Yes/No`  — 選択肢のみを提供するフィールド `Yes` または `No` 値。
   - `File (attachment)`  — ファイルをアップロードし、顧客属性を添付ファイルとして関連付けることを許可するフィールド。
   - `Image File`  — 画像をギャラリーにアップロードし、顧客属性に関連付けることを許可するフィールド。

1. 顧客がフィールドに値を入力する必要がある場合は、 **[!UICONTROL Values Required]** から `Yes`.

1. 初期値をフィールドに割り当てるには、 **[!UICONTROL Default Value]**.

1. レコードを保存する前に、フィールドに入力されたデータが正確かどうかを確認するには、 **[!UICONTROL Input Validation]** を「 」フィールドに入力します。 使用可能な値は、 _[!UICONTROL Input Type]_指定済み

   - `None`  — データ入力時の入力検証がフィールドにありません。
   - `Alphanumeric`  — データ入力時に、数字 (0 ～ 9) と英字 (a ～ z、A ～ Z) の組み合わせを使用できます。 特殊文字を含めるには、 [!UICONTROL Escape HTML Entities] 次の手順で使用します。
   - `Alphanumeric with Space`  — データ入力時に、数字 (0 ～ 9)、英字 (a ～ z、A ～ Z)、およびスペースの組み合わせを使用できます。
   - `Numeric Only`  — データ入力時には数値 (0 ～ 9) のみを使用できます。
   - `Alpha Only`  — データ入力時には英字 (a ～ z、A ～ Z) のみを使用できます。
   - `URL`  — データ入力時に URL のみを受け入れます。
   - `Email`  — データ入力時に電子メールアドレスのみを受け入れます。
   - `Length Only`  — フィールドに入力されたデータの長さに基づいて入力を検証します。

1. テキストフィールド、テキスト領域、または複数行の入力タイプに入力した値に前処理フィルターを適用するには、 **[!UICONTROL Input/Output Filter]** を次のいずれかに変更します。

   - `None`  — フィールドに入力されたテキストにフィルターを適用しません。
   - `Strip HTML Tags`  — テキストからHTMLタグを削除します。 このフィルターは、HTMLタグを含む別のソースからフィールドに貼り付けられたデータをクリーンアップするのに役立ちます。
   - `Escape  HTML Entities`   — テキスト内の特殊文字を、次のような有効なHTMLエスケープシーケンスに変換します。 `&;`. エスケープシーケンスは、アンパサンドとセミコロンで囲まれ、タイポグラフのスマート引用符、著作権、商標記号によく使用されます。 エスケープシーケンスは、より小さい (`<`) およびより大きい (`>`) 記号と、コード内でも使用されるアンパサンド文字。 このフィルタは、ワードプロセッサからデータベースフィールドに貼り付けられる特殊文字をクリーンアップするのに役立ちます。

1. 顧客グリッドおよびセグメントのプロパティを入力します。

   - 顧客グリッドに列を含めるには、 **[!UICONTROL Add to Column Options]** から `Yes`.

   - この属性で顧客グリッドをフィルターするには、 **[!UICONTROL Use in Filter Options]** から `Yes`.

   - 様々なフィルター一致条件を持つテキスト属性で顧客グリッドをフィルターするには、 **[!UICONTROL Grid Filter Condition Type]** から `Partial Match`, `Prefix Match`または `Full Match`. これは、 _キーワードで検索_ グリッドのフィールド。

   - この属性で顧客グリッドを検索するには、 **[!UICONTROL Use in Search Options]** から `Yes`.

   - この属性を次の場所で使用できるようにするには： [顧客セグメント](customer-segments.md)，設定 **[!UICONTROL Use in Customer Segment]** から `Yes`.

## 手順 2：ストアフロントのプロパティを完了する

1. 下にスクロールして、 **[!UICONTROL Storefront Properties]** 」セクションに入力します。

   ![顧客アドレス属性 — Storefront プロパティ](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. 属性を顧客に表示するには、 **[!UICONTROL Show on Storefront]** から `Yes`.

1. 数値を **[!UICONTROL Sort Order]** フィールド：他の属性と共に表示される際の出現順序を決定します。

1. 設定 **[!UICONTROL Forms to Use]** 属性を含める各フォームに追加します。

   両方のオプションを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各フォームをクリックします。

   - [顧客の住所の登録](account-create.md)
   - [顧客アカウントの住所](account-dashboard-address-book.md)

## 手順 3：ラベルを入力して保存する

1. 左側のパネルで、を選択します。 **[!UICONTROL Manage Labels/Options]**.

1. の下 **[!UICONTROL Manage Titles]**、各属性を識別するラベルを入力します [ストア表示](../getting-started/websites-stores-views.md).

1. 完了したら、「 **[!UICONTROL Save Attribute]**.

   ![顧客住所属性 — ラベル/オプション](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## フィールドの説明

### [!UICONTROL Attribute Properties]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Default Label] | Admin および Storefront で属性を識別するデフォルトのラベル。 |
| [!UICONTROL Attribute Code] | システム内の属性を識別する一意のコード。 コードの長さは 21 文字までで、スペースや特殊文字は使用できません。 スペースの代わりにアンダースコア記号を使用できます。 |
| [!UICONTROL Input Type] | を決定します。 [入力制御](../catalog/attributes-input-types.md) データ入力に使用される オプション： <br/>**`Text Field`**- 1 行のテキストフィールド。<br/>**`Text Area`**  — 複数行のテキスト領域。 <br/>**`Multiple Line`**— 複数行の番地に似た、属性に対して複数のテキスト行を作成します。 データ入力行の数は、2 ～ 20 の範囲で指定できます。<br/>**`Date`**  — ポップアップカレンダー付きの日付フィールドを表示します。<br/>**`Dropdown`**- 1 つの値のみを選択できるドロップダウンリスト。<br/>**`Multiple Select`**  — 複数の値を選択できるドロップダウンリスト。 <br/>**`Yes/No`**— 選択肢のみを提供するフィールド `Yes` または `No` 値。<br/>**`File (attachment)`**  — ファイルをアップロードし、顧客属性を添付ファイルとして関連付けることを許可するフィールド。 <br/>**`Image File`**— 画像をギャラリーにアップロードし、顧客属性に関連付けることを許可するフィールド。 |
| [!UICONTROL Values Required] | 値をフィールドに入力する必要があるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Default Value] | 属性の初期値を指定します。 |
| [!UICONTROL Input Validation] | オプションの選択は、入力タイプによって決まります。 オプション： <br/>**`None`**— データ入力時の入力検証がフィールドにありません。<br/>**`Alphanumeric`**  — データ入力時に、数字 (0 ～ 9) と英字 (a ～ z、A ～ Z) の組み合わせを使用できます。 <br/>**`Alphanumeric with Space`**— 通りの住所のスペースを使用して、通信事業者の最大長要件に準拠できます。 チェックアウト時に、顧客は任意の数字の組み合わせ (0 ～ 9)、英字 (a ～ z、A ～ Z)、および受信者と送信者の住所のスペースを入力できます。 アドレスを保存すると、余分なスペースは削除されます。<br/>**`Numeric Only`**  — データ入力時には数値 (0 ～ 9) のみを使用できます。 <br/>**`Alpha Only`**— データ入力時には英字 (a ～ z、A ～ Z) のみを使用できます。<br/>** URL **— データ入力時に URL のみを受け入れます。<br/>**`Email`**  — データ入力時に電子メールアドレスのみを受け入れます。 <br/>**`Length Only`**— フィールドに入力されたデータの長さに基づいて入力を検証します。 |
| [!UICONTROL Input/Output Filter] | レコードを保存する前に、テキストフィールド、テキスト領域、または複数行の入力タイプに入力した値に前処理フィルターを適用します。 オプション： <br/>**`None`**— フィールドに入力されたテキストにフィルターを適用しません。<br/>**`Strip HTML Tags`**  — テキストからHTMLタグを削除します。 このフィルターは、HTMLタグを含む別のソースからフィールドに貼り付けられたデータをクリーンアップするのに役立ちます。 <br/>**`Escape HTML Entities`**— テキスト内の特殊文字を、次のような有効なHTMLエスケープシーケンスに変換します。 `amp;`. エスケープシーケンスは、アンパサンドとセミコロンで囲まれ、タイポグラフのスマート引用符、著作権記号、商標記号によく使用されます。 エスケープシーケンスは、より小さい (`<`) およびより大きい (`>`) 記号と、コード内でも使用されるアンパサンド文字。 このフィルタは、ワードプロセッサからデータベースフィールドに貼り付けられる特殊文字をクリーンアップするのに役立ちます。 |
| [!UICONTROL Add to Column Options] | 属性が [顧客](./customers-all.md) グリッド。 オプション： `Yes` / `No` |
| フィルターオプションで使用 | 属性をグリッドから検索操作のフィルターとして使用できるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | グリッドからの検索操作で、属性のフィルタ一致条件を指定します。 これは、 _[!UICONTROL Search by keyword]_グリッドのフィールド。 オプション： `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | 属性値を検索操作でキーワードとして使用できるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | 属性が [顧客セグメント](./customer-segments.md) 条件。 オプション： `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Show on Storefront] | 属性がストアフロントの顧客情報のフィールドとして表示されるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Sort Order] | 他の顧客属性との関連で、この属性の並べ替え順を指定します。 並べ替え順は、キーボードナビゲーションを使用する際に、データ入力中にフィールドがフォーカスを受け取る順序を決定します。 |
| [!UICONTROL Forms to Use in] | 属性が表示されるデータ入力フォームを持つページを決定します。 オプション： <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
