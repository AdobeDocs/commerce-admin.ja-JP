---
title: 顧客の住所属性
description: 顧客アドレス属性と、これらの属性プロパティの設定方法について説明します。
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# 顧客の住所属性

{{ee-feature}}

顧客住所属性セットは、顧客のアカウントまたは [&#x200B; チェックアウト &#x200B;](../stores-purchase/checkout-process.md) 中に [&#x200B; アドレス帳 &#x200B;](account-dashboard-address-book.md) に入力された住所のプロパティを決定します。

カスタム アドレス属性は、オプションの E メール アドレス、Skype アカウント、代替電話番号、建物、郡などの追加情報を提供するように設定できます。 カスタム属性は、販売ドキュメントの作成に使用される [&#x200B; アドレステンプレート &#x200B;](address-templates.md) に組み込むことができます。 カスタムアドレス属性を作成するプロセスは、[&#x200B; 顧客属性 &#x200B;](attribute-properties.md) を作成するプロセスとほとんど同じです。

顧客の住所属性は、次の形式で使用されます。

- [顧客の住所の登録](account-create.md)
- [顧客アカウントの住所](account-dashboard-address-book.md)

![Admin - Customer address attributes](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## 手順 1：属性プロパティの完了

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Customer Address]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add New Attribute]**」をクリックします。

   ![&#x200B; 顧客属性のプロパティ &#x200B;](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. **[!UICONTROL Attribute Properties]** セクションで、次の操作を行います。

   - データ入力時に属性を識別する **[!UICONTROL Default Label]** を入力します。

   - システム内の属性を識別する **[!UICONTROL Attribute Code]** を入力します。

     属性コードは文字で始まる必要があり、小文字（a ～ z）と数字（0 ～ 9）を任意に組み合わせることができます。 コードの長さは 30 文字未満にする必要があり、特殊文字やスペースを含めることはできません。 アンダースコア文字（_）はスペースを示すために使用できます。

     >[!TIP]
     >
     >**_ショートカット：_** 必須フィールドのみを入力するには、下にスクロールして [!UICONTROL Storefront Properties] に移動し、[!UICONTROL Sort Order] を入力して保存します。

1. データ入力に使用される入力コントロールの種類を決定するには、**[!UICONTROL Input Type]** を次のいずれかに設定します。

   - `Text Field` - 1 行のテキストフィールド。
   - `Text Area` – 複数行のテキスト領域。
   - `Multiple Line` – 複数行の住所のように、属性に対して複数のテキスト行を作成します。 個別のデータ入力行の数は、2 ～ 20 の範囲で指定できます。 フィールドの初期値を指定するには、`Default Value` を使用します。
   - `Date` – 日付フィールドとポップアップカレンダーを表示します。 追加のプロパティ：フィールドの初期値を指定するには、`Default Value` を使用します。 <br/>`Minimal Value` を使用して、入力できる最も早い日付を指定します。  `Maximum Value` を使用して、入力可能な最新の日付を指定します。
   - `Dropdown` – 値の選択を 1 つだけ受け入れるドロップダウンリスト。
   - `Multiple Select` – 複数の値の選択を受け入れるドロップダウンリスト。
   - `Yes/No` - `Yes` 値または `No` 値の選択のみを提供するフィールド。
   - `File (attachment)` - ファイルをアップロードし、顧客属性に添付ファイルとして関連付けることができるフィールド。
   - `Image File` – 画像をギャラリーにアップロードし、顧客属性に関連付けることができるフィールド。

1. 顧客がフィールドに値を入力する必要がある場合は、**[!UICONTROL Values Required]** を `Yes` に設定します。

1. フィールドに初期値を割り当てるには、**[!UICONTROL Default Value]** を入力します。

1. レコードを保存する前に、フィールドに入力されたデータの正確性を確認するには、**[!UICONTROL Input Validation]** をフィールドで許可されるデータのタイプに設定します。 使用できる値は、指定した _[!UICONTROL Input Type]_&#x200B;によって異なります。

   - `None` - フィールドには、データ入力時の入力検証はありません。
   - `Alphanumeric` - データ入力時に数字（0 ～ 9）と英字（a ～ z、A ～ Z）の任意の組み合わせを使用できます。 特殊文字を含めるには、次の手順の [!UICONTROL Escape HTML Entities] を参照してください。
   - `Alphanumeric with Space` - データ入力時に数字（0 ～ 9）、英字（a ～ z、A ～ Z）、スペースの任意の組み合わせを使用できます。
   - `Numeric Only` - データ入力中は数字（0 ～ 9）のみを使用できます。
   - `Alpha Only` - データ入力時に使用できる文字は、英字（a ～ z、A ～ Z）のみです。
   - `URL` - データ入力時に URL のみを受け入れます。
   - `Email` - データ入力時にメールアドレスのみを受け入れます。
   - `Length Only` - フィールドに入力されたデータの長さに基づいて入力を検証します。

1. テキストフィールド、テキスト領域、または複数行の入力タイプに入力された値に前処理フィルターを適用するには、**[!UICONTROL Input/Output Filter]** を次のいずれかに設定します。

   - `None` - フィールドに入力されたテキストにフィルターを適用しません。
   - `Strip HTML Tags` - テキストからHTMLタグを削除します。 このフィルターは、HTMLタグを含む別のソースからフィールドに貼り付けられたデータをクリーンアップするのに役立ちます。
   - `Escape  HTML Entities` - テキスト内の特殊文字を、`&;` などの有効なHTMLエスケープシーケンスに変換します。 エスケープシーケンスは、アンパサンドとセミコロンで囲まれ、タイポグラファーのスマート引用符、著作権、商標の記号によく使用されます。 エスケープシーケンスは、より小さい（`<`）記号や大きい（`>`）記号などの文字、およびコードでも使用されるアンパサンド文字の識別にも使用されます。 このフィルタは、ワード プロセッサからデータベース フィールドに貼り付けられる特殊文字をクリーンアップするのに役立ちます。

1. 顧客グリッドとセグメントのプロパティを入力します。

   - 顧客グリッドに列を含めるには、**[!UICONTROL Add to Column Options]** を `Yes` に設定します。

   - 顧客グリッドをこの属性でフィルタリングするには、**[!UICONTROL Use in Filter Options]** を `Yes` に設定します。

   - 異なるフィルター一致条件を持つテキスト属性で顧客グリッドをフィルタリングするには、**[!UICONTROL Grid Filter Condition Type]** を `Partial Match`、`Prefix Match` または `Full Match` に設定します。 グリッドの _キーワードで検索_ フィールドには影響しません。

   - この属性で顧客グリッドを検索するには、**[!UICONTROL Use in Search Options]** を `Yes` に設定します。

   - この属性を [&#x200B; 顧客セグメント &#x200B;](customer-segments.md) で使用できるようにするには、**[!UICONTROL Use in Customer Segment]** を `Yes` に設定します。

## 手順 2：ストアフロントのプロパティを完了する

1. **[!UICONTROL Storefront Properties]** セクションまで下にスクロールします。

   ![&#x200B; 顧客アドレス属性 – Storefront プロパティ &#x200B;](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. 顧客に属性を表示するには、**[!UICONTROL Show on Storefront]** を `Yes` に設定します。

1. **[!UICONTROL Sort Order]** フィールドに数値を入力します。この数値は、他の属性と共にリストされるときの表示順序を決定します。

1. 属性を含める各フォームに **[!UICONTROL Forms to Use]** を設定します。

   両方を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら各フォームをクリックします。

   - [顧客の住所の登録](account-create.md)
   - [顧客アカウントの住所](account-dashboard-address-book.md)

## 手順 3：ラベルを完成させて保存する

1. 左側のパネルで「**[!UICONTROL Manage Labels/Options]**」を選択します。

1. **[!UICONTROL Manage Titles]** の下に、各 [&#x200B; ストア表示 &#x200B;](../getting-started/websites-stores-views.md) の属性を識別するラベルを入力します。

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。

   ![&#x200B; 顧客住所属性 – ラベル/オプション &#x200B;](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## フィールドの説明

### [!UICONTROL Attribute Properties]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Default Label] | 管理者およびストアフロントで属性を識別するデフォルトのラベル。 |
| [!UICONTROL Attribute Code] | システム内の属性を識別する一意のコード。 コードの長さは最大 21 文字で、スペースや特殊文字を含めることはできません。 アンダースコア記号はスペースの代わりに使用できます。 |
| [!UICONTROL Input Type] | データ入力に使用する [&#x200B; 入力コントロール &#x200B;](../catalog/attributes-input-types.md) を決定します。 オプション：<br/>**`Text Field`**- 1 行のテキストフィールド。<br/>**`Text Area`** – 複数行のテキスト領域。 <br/>**`Multiple Line`**– 複数行の住所のように、属性に対して複数のテキスト行を作成します。 個別のデータ入力行の数は、2 ～ 20 の範囲で指定できます。<br/>**`Date`** – 日付フィールドとポップアップカレンダーを表示します。<br/>**`Dropdown`**– 値の選択を 1 つだけ受け入れるドロップダウンリスト。<br/>**`Multiple Select`** – 複数の値の選択を受け入れるドロップダウンリスト。 <br/>**`Yes/No`**- `Yes` 値または `No` 値の選択のみを提供するフィールド。<br/>**`File (attachment)`** - ファイルをアップロードし、顧客属性に添付ファイルとして関連付けることができるフィールド。 <br/>**`Image File`**– 画像をギャラリーにアップロードし、顧客属性に関連付けることができるフィールド。 |
| [!UICONTROL Values Required] | フィールドに値を入力する必要があるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Default Value] | 属性の初期値を指定します。 |
| [!UICONTROL Input Validation] | オプションの選択は、入力タイプによって決まります。 オプション：<br/>**`None`**- フィールドには、データ入力時に入力検証はありません。<br/>**`Alphanumeric`** - データ入力時に数字（0 ～ 9）と英字（a ～ z、A ～ Z）の任意の組み合わせを使用できます。 <br/>**`Alphanumeric with Space`**– 配送業者の最大長の要件に準拠するために、番地内のスペースを許可します。 チェックアウト時に、お客様は数字（0 ～ 9）、英字（a ～ z、A ～ Z）、および受信者と送信者の住所のスペースを任意に組み合わせて入力できます。 アドレスを保存する際、余分なスペースは削除されます。<br/>**`Numeric Only`** - データ入力中は数字（0 ～ 9）のみを使用できます。 <br/>**`Alpha Only`**- データ入力時に使用できる文字は、英字（a ～ z、A ～ Z）のみです。<br/>**&#x200B; URL &#x200B;**- データ入力時に URL のみを受け入れます。<br/>**`Email`** - データ入力時にメールアドレスのみを受け入れます。 <br/>**`Length Only`**- フィールドに入力されたデータの長さに基づいて入力を検証します。 |
| [!UICONTROL Input/Output Filter] | レコードを保存する前に、テキスト フィールド、テキスト領域、または複数行の入力タイプに入力された値に前処理フィルタを適用します。 オプション：<br/>**`None`**- フィールドに入力されたテキストにフィルターを適用しません。<br/>**`Strip HTML Tags`** - テキストからHTMLタグを削除します。 このフィルターは、HTMLタグを含む別のソースからフィールドに貼り付けられたデータをクリーンアップするのに役立ちます。 <br/>**`Escape HTML Entities`**- テキスト内の特殊文字を、`amp;` などの有効なHTMLエスケープシーケンスに変換します。 エスケープシーケンスは、アンパサンドとセミコロンで囲まれ、タイポグラファーのスマート引用符、著作権記号、商標記号によく使用されます。 エスケープシーケンスは、より小さい（`<`）記号や大きい（`>`）記号などの文字、およびコードでも使用されるアンパサンド文字の識別にも使用されます。 このフィルタは、ワード プロセッサからデータベース フィールドに貼り付けられる特殊文字をクリーンアップするのに役立ちます。 |
| [!UICONTROL Add to Column Options] | 属性が [Customers](./customers-all.md) グリッドの列として含まれるかどうかを指定します。 オプション：`Yes` / `No` |
| フィルターオプションで使用 | 属性をグリッドからの検索操作のフィルターとして使用できるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | グリッドからの検索操作で、属性のフィルター一致条件を指定します。 グリッドの _[!UICONTROL Search by keyword]_&#x200B;フィールドには影響しません。 オプション：`Partial Match`/`Prefix Match`/`Full Match` |
| [!UICONTROL Use in Search Options] | 属性値を検索操作でキーワードとして使用できるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | 属性が [&#x200B; 顧客セグメント &#x200B;](./customer-segments.md) 条件に含まれるかどうかを決定します。 オプション：`Yes` / `No` |

### [!UICONTROL Storefront Properties]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Show on Storefront] | 属性がストアフロントの顧客情報にフィールドとして表示されるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Sort Order] | 他の顧客属性に対するこの属性の並べ替え順を指定します。 並べ替え順序は、キーボードナビゲーションを使用する際に、データ入力中にフィールドがフォーカスを受け取るシーケンスを決定します。 |
| [!UICONTROL Forms to Use in] | 属性が表示されるデータ入力フォームを含むページを決定します。 オプション：<br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
