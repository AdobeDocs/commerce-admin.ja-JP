---
title: 設定スコープ
description: Commerce Admin での設定範囲の設定について説明します。
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# 設定スコープ

多くの設定ページの左上隅にあるストア表示の選択は、特定の範囲についてページの表示をフィルタリングし、Commerceで使用される一部のエンティティの値を設定します。 階層内の各レベルが名前で一覧表示され、スコープを別のレベルに変更するために使用されます。 現在のスコープを表す設定はすべてグレー表示されるため、現在のスコープ設定を表す設定のみが使用可能になります。 範囲は最初に _デフォルト設定_ に設定されます。 制限付きアクセスを使用する管理者ユーザーの場合、使用可能なストア表示のリストには、ユーザーがアクセスする [ 権限 ](../systems/permissions.md) を持っているストア表示のみが含まれます。

| レベル | 説明 |
|--- |--- |
| [!UICONTROL Default Config] | デフォルトのシステム設定。 |
| [!UICONTROL Main Website] | 最上位の web サイトの名前。 |
| [!UICONTROL Main Website Store] | 親 web サイトに関連付けられているデフォルトストアの名前。 |
| [!UICONTROL Default Store View] | 親ストアに関連付けられているデフォルトのストア表示の名前。 |
| [!UICONTROL Stores Configuration] | ストア グリッドにジャンプします。これは、管理サイドバーから [!UICONTROL Stores] > [!UICONTROL All Stores] を選択する場合と同じです。 |

{style="table-layout:auto"}

![ 「システム値を使用」チェックボックスをオンにする ](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

多くの設定の右側にある _[!UICONTROL Use System Value]_&#x200B;チェックボックスは、現在の設定範囲内のデフォルトフィールド値を適用または上書きするために使用されます。 チェックボックスが選択されている場合、デフォルトフィールド値は変更できません。 値を変更するには、このチェックボックスをオフにして新しい値を入力します。 システム値を変更するたびに確認を求められます。

チェックボックスのラベルは、現在のスコープに応じて変わり、スコープ階層の 1 ステップ上の親レベルを常に参照します。 親レベルは、そのレベルの下にあるすべての項目のコンテナであるため、親レベルのスコープ設定は上書きされない限り継承されます。

## デフォルト値オプション

| Checkbox | 説明 |
|--- |--- |
| [!UICONTROL Use system value] | このチェックボックスは、設定範囲が `Default Config` に設定されている場合に表示されます。 |
| [!UICONTROL Use Default] | このチェックボックスは、設定範囲がメイン `Website` ージに設定されている場合に表示され、web サイトに割り当てられているデフォルトのストアを参照します。 |
| [!UICONTROL Use Website] | このチェックボックスは、設定範囲が特定のストア表示に設定されている場合に表示されます。 選択した場合は、ストア表示に関連付けられている親 web サイトの設定が使用されます。 この場合、ストアレベルは、web サイトに関連付けられたデフォルトストアに適用されると理解されるので、スキップされます。 |

{style="table-layout:auto"}

## 範囲を設定

特定の web サイト、ストア、ストア表示のみに適用する設定を行う前に、次の操作を行います。

1. _管理者_ サイドバーで、次のいずれかの操作を行います。

   - ほとんどの設定は、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

   - [ デザイン関連の設定 ](../content-design/configuration.md) については、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**&#x200B;に移動します。 次に、グリッドで、該当するストア表示を選択します。

1. 変更する設定に移動して、次の手順を実行します。

   - 左上隅で、設定が適用される特定のビューに **[!UICONTROL Store View]** を設定します。 範囲の切り替えを確認するプロンプトが表示されたら、「**[!UICONTROL OK]**」をクリックします。

     各フィールドの後にチェックボックスが表示され、追加のフィールドが使用可能になる場合があります。

   - 編集するフィールドの後の「**[!UICONTROL Use system value]**」チェックボックスをオフにします。 次に、ビューの値を更新します。

   - ページ上で更新する必要があるすべてのフィールドに対して、このプロセスを繰り返します。

   ![ フランスのストア表示の国オプションの設定 ](./assets/store-view-french.png){width="700" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 範囲のクイックリファレンス

| 範囲 | 説明 |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Admin | インストール内のすべての web サイト、ストア、ストア表示は、同じ管理者から管理されます。 |
| デフォルトの設定 | グローバル [ デフォルト設定 ](../getting-started/websites-stores-views.md#scope-settings) 設定は、下位レベルで上書きされない限り、ストア階層を通じて使用されます。 |
| カタログ | _カタログ_ という用語は、製品データベース全体を指し、インストール全体で使用できます。 |
| 製品価格 | 製品価格は、グローバルレベルまたは web サイトレベルでアプリケーションに対して設定できます。 |
| 製品設定 | [ 設定可能な製品 ](../catalog/product-create-configurable.md) オプションとして使用する属性には、グローバルスコープが必要です。 |
| 顧客 | 顧客アカウントは、グローバルレベルまたは web サイトレベルでアプリケーション用に設定できます。 各 web サイトには、個別の [ 顧客アカウント ](../customers/customer-account-scope.md) のセットを持たせたり、インストール内の他の web サイトと顧客アカウントを共有したりできます。 |
| **[!UICONTROL Website]** |  |
| ドメイン | 追加の [web サイト ](../stores-purchase/introduction.md#store-structure) は、プライマリドメインのサブドメインとして設定することも、個別の IP アドレスと専用ドメインを持つこともできます。 |
| 顧客 | 顧客アカウントは、グローバルレベルまたは web サイトレベルでアプリケーション用に設定できます。 各 web サイトには、個別の [ 顧客アカウント ](../customers/customer-account-scope.md) のセットを持たせたり、インストール内の他の web サイトと顧客アカウントを共有したりできます。 |
| 通貨 | 各 web サイトには、異なる [ 基本通貨 ](../stores-purchase/currency-configuration.md) を割り当てることができます。 基本通貨は、すべてのトランザクションを処理するために使用されますが、ストア表示のロケールに応じて、異なる表示通貨が顧客に表示される場合があります。 |
| 製品 | 個々の製品は、web サイトレベルで階層に割り当てられます。 製品グリッドには、カタログ内のすべての製品と、それらの製品が使用可能な Web サイトが一覧表示されます。 [Web サイト内の製品 ](../catalog/settings-basic-websites.md) 設定は、製品が使用可能な各 web サイトを識別します。 |
| 製品価格 | [ 製品価格 ](../catalog/catalog-price-scope.md) は、グローバルレベルまたは web サイトレベルでアプリケーションに対して設定できます。 |
| 支払い方法 | [ 支払い方法 ](../stores-purchase/payments.md) は web サイトレベルで設定されますが、タイトルと手順はストア表示ごとに設定できます。 |
| チェックアウト | [ チェックアウトプロセス ](../stores-purchase/checkout-process.md) は web サイトレベルで行われますが、ストア表示ごとに一部の表示オプションを設定できます。 Web サイトに関連付けられているすべてのストアは同じ [ チェックアウト設定 ](../stores-purchase/checkout-process.md#checkout-options) を持ちます。 |
| 許可されている国 | 許可する国は、web サイトレベルで設定できます。 [ 許可される国 ](../getting-started/store-details.md#country-options) 設定は、顧客の出所を制限するためにチェックアウトで使用されます。 |
| **[!UICONTROL Store]** |  |
| ドメイン | 複数のストアがある場合、各ストアは同じドメイン、サブドメインまたは明確に異なるドメインを持つことができます。 詳しくは、[ ストアの追加 ](../stores-purchase/stores.md#add-stores) を参照してください。 |
| ルートカテゴリ | 各店舗には、「ルート」カテゴリとサブカテゴリに基づく製品とメインメニューの別々のセットを持つことができます。 各カタログには [ ルートカテゴリ ](../catalog/category-root.md) があり、ストアレベルで割り当てられます。 |
| **[!UICONTROL Store View]** |  |
| サブカテゴリ | メインメニュー [&#128279;](../catalog/category-create.md#category-structure) ルートの下）を構成する  サブカテゴリ）は、ストア表示レベルで割り当てられます。 |
| Locale | 各ストア表示には、異なる [ ロケール ](../getting-started/store-details.md#locale-options) を割り当てることができます。 表示通貨、測定単位、管理インターフェイスはロケールに固有です。 |
| 言語 | 複数の言語をサポートするには、製品の説明を含むすべてのコンテンツを、ストア表示ごとに [ 翻訳 ](../stores-purchase/store-localize.md#localize-products) する必要があります。 |
| 通貨を表示 | ストア表示ごとに異なる [ 表示通貨 ](../stores-purchase/currency-configuration.md) を使用できますが、トランザクションはベース通貨を使用して web サイトレベルで処理されます。 |

{style="table-layout:auto"}
