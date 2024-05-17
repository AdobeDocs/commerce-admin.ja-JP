---
title: 顧客属性プロパティ
description: 顧客属性プロパティを設定する方法を説明します。
exl-id: d464f846-6a1f-43bd-876a-6834605ef794
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1796'
ht-degree: 0%

---

# 顧客属性プロパティ

{{ee-feature}}

顧客属性は、注文、受け渡し、顧客管理の各プロセスをサポートするために必要な情報を提供します。 ビジネスは一意なので、システムから提供されるデフォルトの項目に加えて、フィールドが必要になる場合があります。 顧客のアカウントの「アカウント情報」、「アドレス帳」、「請求情報」の各セクションにカスタム属性を追加できます。 顧客 [アドレス属性](address-attributes.md) は、 _請求情報_ チェックアウト中、またはゲストがアカウントに登録する際のセクション。

![顧客属性](./assets/attributes-customer.png){width="700" zoomable="yes"}

## 手順 1：属性プロパティの入力

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Attribute]**.

   ![顧客属性プロパティ](./assets/attribute-customer-new.png){width="600" zoomable="yes"}

1. が含まれる **[!UICONTROL Attribute Properties]** セクションで、次の操作を行います。

   - を入力 **[!UICONTROL Default Label]** データ入力時に属性を識別します。

   - を入力 **[!UICONTROL Attribute Code]** は、システム内の属性を識別します。

   属性コードは文字で始まる必要があり、小文字（a ～ z）と数字（0 ～ 9）を任意に組み合わせることができます。 コードの長さは 30 文字未満にする必要があり、特殊文字やスペースを含めることはできません。 アンダースコア（`_`）を使用してスペースを示すことができます。

   >[!TIP]
   >
   >**ショートカット：** 必須フィールドのみに入力するには、以下までスクロールします。 _[!UICONTROL Storefront Properties]_を入力します_[!UICONTROL Sort Order]_&#x200B;を選択して保存します。

1. 次のデータ入力プロパティを入力します。

   - データ入力に使用される入力コントロールの種類を決定するには、次のように設定します **[!UICONTROL Input Type]** を次のいずれかに変更します。

     | タイプ | 説明 |
     |----|-----------|
     | `Text Field` | 1 行のテキストフィールド。 |
     | `Text Area` | 製品の説明など、テキストの段落を入力するための複数行の入力フィールド。 WYSIWYG エディターを使用して、HTMLタグでテキストの書式を設定したり、テキストにタグを直接入力したりできます。 |
     | `Multiple Line` | 複数行の番地と同様に、属性に複数行のテキスト行を作成します。 個別のデータ入力行の数は、2 ～ 20 の範囲で指定できます。 の使用 `Default Value` フィールドの初期値を指定します。 |
     | `Date` | 日付の値を優先日付形式およびタイムゾーンで表示します。 日付値は、リストまたはカレンダー（ ![カレンダーアイコン](../assets/icon-calendar.png) ）に設定します。 <br/><br/>**_注意：_**システム設定に応じて、_Admin _ユーザーは、フィールドに日付を直接入力したり、カレンダーやリストから日付を選択したりできます。 日付と時刻の値の指定については、を参照してください。 [日付と時刻のオプション](../catalog/attributes-input-types.md#date-and-time-options). |
     | `Yes/No` | 次のオプションがあらかじめ定義されたドロップダウン リストを表示 `Yes` および `No`. |
     | `Dropdown` | 1 つの選択のみを受け入れる値のドロップダウン リストを表示します。 ドロップダウン入力タイプは、の主要コンポーネントです [設定可能な製品](../catalog/product-create-configurable.md). |
     | `Multiple Select` | 複数の値の選択を受け入れるドロップダウンリスト。 |
     | `File (attachment)` | ファイルをアップロードし、顧客属性に添付ファイルとして関連付けることができるフィールド。 |
     | `Image File` | 画像をギャラリーにアップロードし、顧客属性に関連付けることができるフィールド。 |

   - 顧客がフィールドに値を入力する必要がある場合は、 **[!UICONTROL Values Required]** 対象： `Yes`.

   - フィールドに初期値を割り当てるには、 **[!UICONTROL Default Value]**.

   - レコードを保存する前に、フィールドに入力されたデータの正確性を確認するには、次のように設定します **[!UICONTROL Input Validation]** をフィールドで許可されるデータのタイプに変更します。 使用できる値は、 [!UICONTROL Input Type] 指定します。

     | 値 | 説明 |
     |-----|-----------|
     | `None` | フィールドには、データ入力時の入力検証はありません。 |
     | `Alphanumeric` | データ入力時に数字（0 ～ 9）と英字（a ～ z、A ～ Z）の任意の組み合わせを使用できます。 特殊文字を含めるには、を参照してください _HTMLエンティティのエスケープ_. |
     | `Alphanumeric with Space` | データ入力時に数字（0 ～ 9）、英字（a ～ z、A ～ Z）、スペースの任意の組み合わせを使用できます。 |
     | `Numeric Only` | データ入力時に使用できるのは数値（0 ～ 9）のみです。 |
     | `Alpha Only` | データ入力時に使用できる文字は、英字（a ～ z、A ～ Z）のみです。 |
     | `URL` | データ入力時に URL のみを受け入れます。 |
     | `Email` | データ入力時にメールアドレスのみを受け入れます。 |
     | `Length Only` | フィールドに入力されたデータの長さに基づいて入力を検証します。 |

   - テキストフィールドおよびテキスト領域の入力タイプのサイズを制限するには、 **[!UICONTROL Minimum Text Length]** および **[!UICONTROL Maximum Text Length]**.

   - テキストフィールド、テキスト領域、または複数行入力タイプに入力された値に前処理フィルターを適用するには、を設定します。 **[!UICONTROL Input/Output Filter]** を次のいずれかに変更します。

     | 値 | 説明 |
     |-----|-----------|
     | `None` | フィールドに入力されたテキストにフィルターを適用しません。 |
     | `Strip HTML Tags` | テキストからHTMLタグを削除します。 このフィルターは、HTMLタグを含む別のソースからフィールドに貼り付けられたデータをクリーンアップするのに役立ちます。 |
     | `Escape  HTML Entities` | テキスト内の特殊文字を有効なHTMLエスケープシーケンス（例：）に変換します `&;`. エスケープシーケンスは、アンパサンドとセミコロンで囲まれ、タイポグラファーのスマート引用符、著作権、商標の記号によく使用されます。 エスケープシーケンスは、より小さい（`<`）およびより大きい（`>`）、およびコード内でも使用されるアンパサンド文字。 このフィルタは、ワード プロセッサからデータベース フィールドに貼り付けられる特殊文字をクリーンアップするのに役立ちます。 |

1. 顧客グリッドとセグメントのプロパティを入力します。

   - 顧客グリッドに列を含めるには、次のように設定します **[!UICONTROL Add to Column Options]** 対象： `Yes`.

   - 顧客グリッドをこの属性でフィルタリングするには、次のように設定します **[!UICONTROL Use in Filter Options]** 対象： `Yes`.

   - 異なるフィルター一致条件を使用してテキスト属性で顧客グリッドをフィルタリングするには、を設定します **[!UICONTROL Grid Filter Condition Type]** 対象： `Partial Match`, `Prefix Match`、または `Full Match`. に影響しません。 _キーワードで検索_  グリッドのフィールド。

   - この属性で顧客グリッドを検索するには、次のように設定します **[!UICONTROL Use in Search Options]** 対象： `Yes`.

   - この属性を次のユーザーが使用できるようにします [顧客セグメント](customer-segments.md)、設定 **[!UICONTROL Use in Customer Segment]** 対象： `Yes`.

## 手順 2：ストアフロントのプロパティを完了する

1. にスクロール ダウンします。 **[!UICONTROL Storefront Properties]** セクション。

   ![顧客属性 – ストアフロントのプロパティ](./assets/attribute-customer-storefront-properties.png){width="600" zoomable="yes"}

1. 顧客に属性を表示するには、次のように設定します **[!UICONTROL Show on Storefront]** 対象： `Yes`.

1. に数値を入力してください **[!UICONTROL Sort Order]** フィールド。他の属性と共にリストされる場合の表示順序を決定します。

1. を設定 **[!UICONTROL Forms to Use]** を属性を含む各フォームに送信します。 複数のオプションを選択するには、Ctrl キーを押しながら各フォームをクリックします。

   - [&#39;顧客登録&#39;](customer-sign-in.md)
   - [&#39;顧客アカウントの編集&#39;](account-create.md)
   - [&#39;管理者チェックアウト&#39;](../stores-purchase/checkout-process.md)

## 手順 3：ラベルを完成させて保存する

1. 左パネルで、を選択します。 **[!UICONTROL Manage Labels/Options]**.

1. 次の下 **[!UICONTROL Manage Titles]**、それぞれの属性を識別するラベルを入力します [ストア表示](../getting-started/websites-stores-views.md).

1. 完了したら、 **[!UICONTROL Save Attribute]**.

   ![顧客属性 – ラベル/オプション](./assets/attribute-customer-manage-label-options.png){width="600" zoomable="yes"}

## フィールドの説明

### [!UICONTROL Attribute Properties]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Default Label] | 管理者およびストアフロントで属性を識別するデフォルトのラベル。 |
| [!UICONTROL Attribute Code] | システム内の属性を識別する一意のコード。 コードの長さは最大 60 文字で、スペースや特殊文字を含めることはできません。 アンダースコア記号はスペースの代わりに使用できます。 |
| [!UICONTROL Input Type] | データ入力に使用する入力コントロールを決定します。 オプション： <br/>**`Text Field`**- 1 行のテキストフィールド。<br/>**`Text Area`**  – 複数行テキスト領域。 <br/>**`Multiple Line`**– 複数行の住所と同様に、属性に対して複数行のテキストを作成します。 個別のデータ入力行の数は、2 ～ 20 の範囲で指定できます。<br/>**`Date`**  – 日付フィールドとポップアップカレンダーを表示します。<br/>**`Dropdown`**– 値の選択を 1 つだけ受け入れるドロップダウンリスト。<br/>**`Multiple Select`**  – 複数の値の選択を受け入れるドロップダウンリスト。 <br/>**`Yes/No`**– 次の選択肢のみを提供するフィールド `Yes` または `No` 値。<br/>**`File (attachment)`** - ファイルをアップロードし、顧客属性に添付ファイルとして関連付けることができるフィールド。 <br/>**`Image File`**– 画像をギャラリーにアップロードし、顧客属性に関連付けることができるフィールド。 |
| [!UICONTROL Values Required] | フィールドに値を入力する必要があるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Default Value] | 属性の初期値を指定します。 |
| [!UICONTROL Input Validation] | オプションの選択は、入力タイプによって決まります。 オプション： <br/>**`None`**- フィールドには、データ入力時の入力検証はありません。<br/>**`Alphanumeric`** - データ入力時に数字（0 ～ 9）と英字（a ～ z、A ～ Z）の任意の組み合わせを使用できます。 <br/>**`Alphanumeric with Space`**– 配送業者の最大長の要件に準拠するために、番地内のスペースを使用できます。 チェックアウト時に、お客様は数字（0 ～ 9）、英字（a ～ z、A ～ Z）、および受信者と送信者の住所のスペースを任意に組み合わせて入力できます。 アドレスを保存する際、余分なスペースは削除されます。<br/>**`Numeric Only`** - データ入力時に使用できるのは数値（0 ～ 9）のみです。 <br/>**`Alpha Only`**- データ入力時に使用できる文字は、英字（a ～ z、A ～ Z）のみです。<br/>**`URL`** - データ入力時に URL のみを受け入れます。 <br/>**`Email`**- データ入力時にメールアドレスのみを受け入れます。<br/>**`Length Only`** - フィールドに入力されたデータの長さに基づいて入力を検証します。 |
| [!UICONTROL Input/Output Filter] | レコードを保存する前に、テキスト フィールド、テキスト領域、または複数行の入力タイプに入力された値に前処理フィルタを適用します。 オプション： <br/>**`None`**- フィールドに入力されたテキストにフィルターを適用しません。<br/>**`Strip HTML Tags`** - テキストからHTMLタグを削除します。 このフィルターは、HTMLタグを含む別のソースからフィールドに貼り付けられたデータをクリーンアップするのに役立ちます。 <br/>**`Escape HTML Entities`**- テキスト内の特殊文字を、有効なHTMLエスケープシーケンス（など）に変換します `amp;`. エスケープシーケンスは、アンパサンドとセミコロンで囲まれ、タイポグラファーのスマート引用符、著作権記号、商標記号によく使用されます。 エスケープシーケンスは、より小さい（`<`）およびより大きい（`>`）、およびコード内でも使用されるアンパサンド文字。 このフィルタは、ワード プロセッサからデータベース フィールドに貼り付けられる特殊文字をクリーンアップするのに役立ちます。 |
| [!UICONTROL Add to Column Options] | 属性がの列として含まれるかどうかを指定します。 [顧客](customers-all.md) グリッド。 オプション： `Yes` / `No` |
| [!UICONTROL Use in Filter Options] | 属性をグリッドからの検索操作のフィルターとして使用できるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | グリッドからの検索操作の属性のフィルター一致条件を指定します。 に影響しません。 _キーワードで検索_ グリッドのフィールド。 オプション： `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | 属性値を検索操作でキーワードとして使用できるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | 属性がに含まれているかどうかを判断します。 [顧客セグメント](customer-segments.md) 条件。 オプション： `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Show on Storefront] | 属性がストアフロントの顧客情報にフィールドとして表示されるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Sort Order] | 他の顧客属性に対するこの属性の並べ替え順を指定します。 並べ替え順序は、キーボードナビゲーションを使用する際に、データ入力中にフィールドがフォーカスを受け取るシーケンスを決定します。 |
| [!UICONTROL Forms to Use in] | 属性が表示されるデータ入力フォームを含むページを決定します。 オプション： <br/>[`Customer Registration`](account-dashboard-account-information.md) <br/>[`Customer Account Edit`](account-create.md) <br/>[`Admin Checkout`](../stores-purchase/checkout-process.md) |

## デフォルトの顧客属性

| 属性コード | 説明 |
| --------------- | ------------------ |
| `created_at` | 顧客アカウントが作成された日付。 |
| `updated_at` | 顧客アカウントが最後に更新された日付。 |
| `website_id` | 顧客アカウントが作成されたサイトの Web サイト ID。 |
| `store_id` | 顧客アカウントが作成されたサイトのストア ID。 |
| `created_in` | アカウントが作成されたストア表示。 |
| `group_id` | 顧客が割り当てられている顧客グループの ID。 |
| `disable_auto_group_change` | 顧客グループを次の期間に動的に割り当てることができるかどうかを決定します [VAT ID の検証](../stores-purchase/vat.md#configure-vat-id-validation). |
| `prefix` | お客様の名前に使用されるプレフィックス（Mr.、Ms.、Dr.など）。 |
| `firstname` | 顧客の名。 |
| `middlename` | 顧客のミドルネームまたはミドルイニシャル。 |
| `lastname` | 顧客の姓。 |
| `suffix` | 顧客名で使用されるサフィックス。 （Jr.、Sr.、Esquire など） |
| `email` | 顧客の電子メールアドレス。 |
| `dob` | 顧客の生年月日。  <br><br>**_重要：_**現在のセキュリティおよびプライバシーのベストプラクティスに従い、顧客の完全な生年月日（月、日、年）を他の個人識別子と保存することに関連して、法的およびセキュリティ上の潜在的なリスクがあることを認識しておいてください。 顧客の完全な生年月日の保存を制限し、代替として顧客の生年月日の使用を提案することをお勧めします。 |
| `taxvat` | 顧客に割り当てられた付加価値税（VAT） ID。 この属性のデフォルトのラベルはです。 `VAT Number`. VAT 番号フィールドは、管理者から表示すると、常にすべての配送先顧客および請求先顧客の住所に表示されますが、必須フィールドではありません。 |
| `gender` | 顧客の性別。 |

## 顧客属性のデモ

顧客属性の作成のデモについては、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343661?quality=12)
