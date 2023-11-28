---
title: 設定範囲
description: コマース管理で設定の範囲を設定する方法について説明します。
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: eb61d90c0a3bf5cac976fc8b79b23dc717aca3e6
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# 設定範囲

多くの設定ページの左上隅にある Store View Chooser は、特定の範囲のページのビューをフィルタリングし、Commerce で使用されるエンティティの値を設定します。 階層内の各レベルを名前別にリストし、スコープを別のレベルに変更するために使用します。 現在のスコープを表す設定はグレー表示になるので、現在のスコープ設定を表す設定のみを使用できます。 スコープは最初に次の値に設定されます。 _デフォルトの設定_. アクセスが制限されている管理者ユーザーの場合、使用可能なストア表示のリストには、ユーザーが所有するストアのみが含まれます [権限](../systems/permissions.md) にアクセスします。

| レベル | 説明 |
|--- |--- |
| [!UICONTROL Default Config] | デフォルトのシステム設定です。 |
| [!UICONTROL Main Website] | 階層の最上部にある Web サイトの名前。 |
| [!UICONTROL Main Website Store] | 親 Web サイトに関連付けられているデフォルトのストアの名前。 |
| [!UICONTROL Default Store View] | 親ストアに関連付けられているデフォルトのストア表示の名前。 |
| [!UICONTROL Stores Configuration] | 「店舗」グリッドにジャンプします。これは、を選択した場合と同じです。 [!UICONTROL Stores] > [!UICONTROL All Stores] 管理者サイドバーから。 |

{:style=&quot;table-layout:auto&quot;}

![「Use System Value」チェックボックスがオンになっている](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

The _[!UICONTROL Use System Value]_多くの設定の右側にあるチェックボックスを使用して、現在の設定範囲内でデフォルトのフィールド値を適用または上書きします。 チェックボックスが選択されている場合、デフォルトのフィールド値は変更できません。 値を変更するには、チェックボックスをオフにして新しい値を入力します。 システム値を変更すると、確認を求めるメッセージが表示されます。

チェックボックスラベルは、現在のスコープに応じて変わり、常にスコープ階層の 1 つ上のステップにある親レベルを参照します。 親レベルは、そのレベルの下にあるすべての項目のコンテナなので、上書きされない限り、親レベルのスコープ設定が継承されます。

## デフォルト値のオプション

| チェックボックス | 説明 |
|--- |--- |
| [!UICONTROL Use system value] | このチェックボックスは、構成範囲が `Default Config`. |
| [!UICONTROL Use Default] | このチェックボックスは、構成範囲が [ メイン ] に設定されている場合に表示されます。 `Website`とは、Web サイトに割り当てられるデフォルトのストアを指します。 |
| [!UICONTROL Use Website] | このチェックボックスは、構成範囲が特定のストア表示に設定された場合に表示されます。 選択すると、ストア表示に関連付けられている親 Web サイトの設定が使用されます。 この場合、ストアレベルは、Web サイトに関連付けられているデフォルトのストアに適用されると理解されるので、スキップされます。 |

{:style=&quot;table-layout:auto&quot;}

## 範囲の設定

特定の Web サイト、ストア、またはストアの表示にのみ適用する設定を行う前に、次の手順を実行します。

1. 次の日： _管理者_ サイドバーで、次のいずれかの操作を行います。

   - ほとんどの設定については、次を参照してください。 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - の場合 [デザイン関連の設定](../content-design/configuration.md)に移動します。 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. 次に、グリッドで、適切なストアビューを選択します。

1. 変更する設定に移動し、次の手順を実行します。

   - 左上隅で、 **[!UICONTROL Store View]** 設定を適用する特定のビューに適用します。 範囲の切り替えを確認するメッセージが表示されたら、 **[!UICONTROL OK]**.

     各フィールドの後にチェックボックスが表示され、追加のフィールドが使用可能になる場合があります。

   - 次をクリア： **[!UICONTROL Use system value]** 」チェックボックスをオンにします。 次に、ビューの値を更新します。

   - ページ上の更新が必要なフィールドごとに、この手順を繰り返します。

   ![フランス語ストア表示の「国」オプションの設定](./assets/store-view-french.png){width="700" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 範囲のクイックリファレンス

| 範囲 | 説明 |
|--- |--- |
| **[!UICONTROL Global]** |  |
| 管理者 | インストール内のすべての Web サイト、ストア、ビューの保存は、同じ管理者から管理されます。 |
| デフォルトの設定 | グローバル [デフォルト設定](../getting-started/websites-stores-views.md#scope-settings) 設定は、下位レベルで上書きされない限り、ストア階層全体で使用されます。 |
| カタログ | 用語 _カタログ_ は、製品データベース全体を指し、インストール全体で使用できます。 |
| 製品価格 | 製品価格は、グローバルレベルまたは Web サイトレベルで、アプリケーション用に設定できます。 |
| 製品設定 | 次の用途で使用される属性 [設定可能な製品](../catalog/product-create-configurable.md) オプションはグローバルスコープを持つ必要があります。 |
| 顧客 | 顧客アカウントは、グローバルレベルまたは Web サイトレベルでアプリケーション用に設定できます。 各 Web サイトは、 [顧客アカウント](../customers/customer-account-scope.md) または、インストール内の他の web サイトと顧客アカウントを共有します。 |
| **[!UICONTROL Website]** |  |
| ドメイン | その他 [web サイト](../stores-purchase/introduction.md#store-structure) はプライマリドメインのサブドメインとして設定することも、別の IP アドレスと専用ドメインを持つこともできます。 |
| 顧客 | 顧客アカウントは、グローバルレベルまたは Web サイトレベルでアプリケーション用に設定できます。 各 Web サイトは、 [顧客アカウント](../customers/customer-account-scope.md) または、インストール内の他の web サイトと顧客アカウントを共有します。 |
| 通貨 | 各 Web サイトに異なる [基準通貨](../stores-purchase/currency-configuration.md). 基本通貨は、すべてのトランザクションの処理に使用されますが、店舗表示のロケールに応じて、顧客には異なる表示通貨が表示される場合があります。 |
| 製品 | 個々の製品は、Web サイトレベルで階層に割り当てられます。 「製品」グリッドには、カタログ内のすべての製品と、それらが使用可能な Web サイトが表示されます。 The [Web サイト内の製品](../catalog/settings-basic-websites.md) 設定は、製品が入手可能な各 web サイトを識別します。 |
| 製品価格 | [製品価格](../catalog/catalog-price-scope.md) は、グローバルレベルまたは web サイトレベルでアプリケーション用に設定できます。 |
| 支払い方法 | [支払い方法](../stores-purchase/payments.md) は web サイトレベルで設定されますが、タイトルと手順はストア表示ごとに設定できます。 |
| チェックアウト | The [チェックアウトプロセス](../stores-purchase/checkout-process.md) は web サイトレベルで実行されますが、一部の表示オプションはストアビューごとに設定できます。 Web サイトに関連付けられているすべてのストアは同じです [チェックアウト設定](../stores-purchase/checkout-process.md#checkout-options). |
| 許可された国 | 許可される国は、Web サイトレベルで設定できます。 The [許可された国](../getting-started/store-details.md#country-options) 設定は、顧客がどこから来るかを制限するためにチェックアウトで使用されます。 |
| **[!UICONTROL Store]** |  |
| ドメイン | 複数のストアがある場合、各ストアは同じドメイン、サブドメイン、または明確に異なるドメインを持つことができます。 詳しくは、 [ストアの追加](../stores-purchase/stores.md#add-stores). |
| ルートカテゴリ | 各ストアには、「ルート」カテゴリとサブカテゴリに基づく個別の製品とメインメニューのセットを含めることができます。 各カタログには [ルートカテゴリ](../catalog/category-root.md) これはストアレベルで割り当てられます。 |
| **[!UICONTROL Store View]** |  |
| サブカテゴリ | The [サブカテゴリ](../catalog/category-create.md#category-structure) メインメニュー（ルートの下）を構成するものが、ストアビューレベルで割り当てられます。 |
| ロケール | 各ストアビューに異なる [ロケール](../getting-started/store-details.md#locale-options). 表示通貨、測定単位、および管理インターフェイスは、ロケールに固有です。 |
| 言語 | 複数の言語をサポートするには、製品の説明を含むすべてのコンテンツが、 [翻訳済み](../stores-purchase/store-localize.md#localize-products) 各ストア表示に対して |
| 通貨を表示 | 別の [通貨を表示](../stores-purchase/currency-configuration.md) は各ストア表示に使用できますが、トランザクションは基本通貨を使用して web サイトレベルで処理されます。 |

{:style=&quot;table-layout:auto&quot;}
