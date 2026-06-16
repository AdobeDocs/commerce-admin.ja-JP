---
title: 設定範囲
description: Commerce Adminでの設定の範囲の設定について説明します。
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
TQID: https://experienceleague.adobe.com/dOH8zNrJuH26wVQDh3aQP6P8xJ5qM7lEcLphkoxLnn4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1033
ht-degree: 0%

---

# 設定範囲

多くのコンフィギュレーションページの左上隅にあるストアビュー選択ツールでは、特定の範囲のページのビューがフィルタリングされ、Commerceで使用される一部のエンティティの値が設定されます。 階層内の各レベルを名前でリスト化し、スコープを別のレベルに変更するために使用します。 現在のスコープを表す設定はすべてグレー表示されるので、現在のスコープ設定を表す設定のみが使用できます。 スコープは最初に&#x200B;_Default Config_&#x200B;に設定されます。 アクセスが制限された管理者ユーザーの場合、使用可能なストアビューのリストには、ユーザーがアクセス権[権限](../systems/permissions.md)を持つストアビューのみが含まれます。

| レベル | 説明 |
|--- |--- |
| [!UICONTROL Default Config] | デフォルトのシステム設定。 |
| [!UICONTROL Main Website] | 階層の上部にあるweb サイトの名前。 |
| [!UICONTROL Main Website Store] | 親Web サイトに関連付けられているデフォルトストアの名前。 |
| [!UICONTROL Default Store View] | 親ストアに関連付けられているデフォルトのストアビューの名前。 |
| [!UICONTROL Stores Configuration] | ストアグリッドにジャンプし、管理者サイドバーから[!UICONTROL Stores] > [!UICONTROL All Stores]を選択するのと同じです。 |

{style="table-layout:auto"}

![&#x200B; システム値のチェックボックスを選択](./assets/store-view-control.png){width="700" zoomable="yes"}使用

## [!UICONTROL Use system value]

多くの設定設定の右側にある&#x200B;_[!UICONTROL Use System Value]_&#x200B;チェックボックスは、現在の設定スコープ内のデフォルトのフィールド値を適用または上書きするために使用されます。 チェックボックスを選択すると、デフォルトのフィールド値を変更できません。 値を変更するには、チェックボックスをオフにして新しい値を入力します。 システム値を変更するたびに確認を求められます。

チェックボックスラベルは、現在のスコープに応じて変更され、常にスコープ階層の上位の親レベルを指します。 親レベルはそのレベルより下のすべての項目のコンテナであるため、親レベルのスコープ設定は上書きされない限り継承されます。

## デフォルト値オプション

| チェックボックス | 説明 |
|--- |--- |
| [!UICONTROL Use system value] | このチェックボックスは、設定範囲が`Default Config`に設定されている場合に表示されます。 |
| [!UICONTROL Use Default] | このチェックボックスは、設定範囲がメイン `Website`に設定され、web サイトに割り当てられている既定のストアを参照する場合に表示されます。 |
| [!UICONTROL Use Website] | このチェックボックスは、設定範囲が特定のストアビューに設定されている場合に表示されます。 選択すると、ストアビューに関連付けられている親web サイトの設定が使用されます。 この場合、ストアレベルはスキップされます。これは、web サイトに関連付けられているデフォルトストアに適用されると理解されているためです。 |

{style="table-layout:auto"}

## 範囲の設定

特定のweb サイト、ストア、またはストアビューにのみ適用される設定設定を行う前に、次の操作を行います。

1. _管理者_ サイドバーで、次のいずれかの操作を行います。

   - ほとんどの構成設定については、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動してください。

   - [&#x200B; デザイン関連の設定](../content-design/configuration.md)について、**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;に移動します。 次に、グリッドで、該当するストアビューを選択します。

1. 変更する設定に移動し、次の操作を行います。

   - 左上隅で、設定が適用される特定のビューに&#x200B;**[!UICONTROL Store View]**&#x200B;を設定します。 範囲の切り替えを確認するメッセージが表示されたら、**[!UICONTROL OK]**&#x200B;をクリックします。

     各フィールドの後にチェックボックスが表示され、追加のフィールドが使用可能になる場合があります。

   - 編集するフィールドの後にある&#x200B;**[!UICONTROL Use system value]** チェックボックスをオフにします。 次に、ビューの値を更新します。

   - ページ上で更新する必要があるすべてのフィールドに対して、このプロセスを繰り返します。

   ![&#x200B; フランスのストアビューの国オプションの設定](./assets/store-view-french.png){width="700" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## 範囲クイックリファレンス

| 範囲 | 説明 |
|--- |--- |
| **[!UICONTROL Global]** |  |
| 管理者 | インストール内のすべてのweb サイト、ストア、ストアビューは、同じ管理者から管理されます。 |
| デフォルト設定 | グローバル設定[&#x200B; デフォルト設定](../getting-started/websites-stores-views.md#scope-settings)は、下位レベルで上書きされない限り、ストア階層を通じて使用されます。 |
| カタログ | _カタログ_&#x200B;という用語は、製品データベース全体を指し、インストール全体で使用できます。 |
| 製品の価格 | 製品の価格は、グローバルレベルまたはweb サイトレベルで適用するように設定できます。 |
| 製品設定 | [設定可能な製品](../catalog/product-create-configurable.md) オプションとして使用される属性には、グローバル スコープが必要です。 |
| 顧客 | 顧客アカウントは、グローバルレベルまたはweb サイトレベルでアプリケーション用に設定できます。 各web サイトは、個別の[顧客アカウント &#x200B;](../customers/customer-account-scope.md)のセットを持つことも、インストール中の他のweb サイトと顧客アカウントを共有することもできます。 |
| **[!UICONTROL Website]** |  |
| ドメイン | 追加の[web サイト &#x200B;](../stores-purchase/introduction.md#store-structure)は、プライマリドメインのサブドメインとして設定するか、個別のIP アドレスと専用ドメインを持つことができます。 |
| 顧客 | 顧客アカウントは、グローバルレベルまたはweb サイトレベルでアプリケーション用に設定できます。 各web サイトは、個別の[顧客アカウント &#x200B;](../customers/customer-account-scope.md)のセットを持つことも、インストール中の他のweb サイトと顧客アカウントを共有することもできます。 |
| 通貨 | 各web サイトに異なる[基本通貨](../stores-purchase/currency-configuration.md)を割り当てることができます。 ストアビューのロケールに従って、すべてのトランザクションを処理するために基本通貨が使用されますが、顧客には異なる表示通貨が表示される場合があります。 |
| 特定可能 | 個々の製品は、web サイトレベルで階層に割り当てられます。 「製品」グリッドには、カタログ内のすべての製品と、その製品が使用可能なweb サイトが一覧表示されます。 Web サイトの[製品](../catalog/settings-basic-websites.md)設定は、製品が使用可能な各Web サイトを識別します。 |
| 製品の価格 | [製品価格](../catalog/catalog-price-scope.md)は、グローバル レベルまたはweb サイト レベルでアプリケーション用に設定できます。 |
| お支払い方法 | [支払い方法](../stores-purchase/payments.md)はweb サイト レベルで設定されますが、タイトルと手順はストアビューごとに設定できます。 |
| チェックアウト | [&#x200B; チェックアウトプロセス &#x200B;](../stores-purchase/checkout-process.md)は、web サイト レベルで実行されますが、ストアビューごとに一部の表示オプションを設定できます。 Web サイトに関連付けられているすべてのストアには、同じ[&#x200B; チェックアウト設定](../stores-purchase/checkout-process.md#checkout-options)があります。 |
| 許可されている国 | 許可される国は、web サイトレベルで設定できます。 チェックアウトでは、[許可された国](../getting-started/store-details.md#country-options)の設定を使用して、顧客の出身地を制限します。 |
| **[!UICONTROL Store]** |  |
| ドメイン | 複数のストアでは、各ストアに同じドメイン、サブドメイン、または異なるドメインを割り当てることができます。 詳しくは、[&#x200B; ストアの追加](../stores-purchase/stores.md#add-stores)を参照してください。 |
| ルートカテゴリ | 各ストアには、「ルート」カテゴリとサブカテゴリに基づいた製品とメインメニューの個別のセットがあります。 各カタログには、ストアレベルで割り当てられた[&#x200B; ルートカテゴリ &#x200B;](../catalog/category-root.md)があります。 |
| **[!UICONTROL Store View]** |  |
| サブカテゴリ | メインメニュー（ルートの下）を構成する[&#x200B; サブカテゴリ &#x200B;](../catalog/category-create.md#category-structure)は、ストアビューレベルで割り当てられます。 |
| ロケール | 各ストアビューには、異なる[&#x200B; ロケール &#x200B;](../getting-started/store-details.md#locale-options)を割り当てることができます。 表示通貨、測定単位、管理者インターフェイスは、ロケールに固有です。 |
| 言語 | 複数の言語をサポートするには、商品説明を含むすべてのコンテンツを、各ストアビューに対して[translated](../stores-purchase/store-localize.md#localize-products)にする必要があります。 |
| 表示通貨 | ストアビューごとに異なる[表示通貨](../stores-purchase/currency-configuration.md)を使用できますが、トランザクションは基本通貨を使用してweb サイトレベルで処理されます。 |

{style="table-layout:auto"}
