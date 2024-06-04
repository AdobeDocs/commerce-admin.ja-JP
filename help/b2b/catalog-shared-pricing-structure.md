---
title: 共有カタログの価格と構造の設定
description: Adobe Commerce B2B では、共有カタログの価格と構造の設定について説明します。
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# 共有カタログの価格と構造の設定

共有カタログの価格と構造を設定するには、次の 2 つの手順があります。 プロセス内の現在の場所がハイライト表示され、ページ上部のプログレスバーに数字が表示されます。 進行状況バーをクリックすると、プロセスの他のステップをいつでも表示できます。 例えば、カスタム価格を設定している場合は、製品選択ページに戻って参照することができます。 クリックするだけで済みます **[!UICONTROL Products]** をクリックし、 **[!UICONTROL Pricing]** カスタム価格ページに戻ります。 このプロセスではあなたの仕事は失われません。

![カタログ内の製品](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}

標準カテゴリツリーでは、ルートカテゴリが最上位のコンテナであり、と呼ばれます _既定のカテゴリ_ サンプルデータ内。 ただし、共有カタログが有効な場合、カテゴリ ツリーにはという外側のコンテナがあります _ルートカタログ_. ルート カタログには、システムに存在するその他すべてのカテゴリ構造が含まれます。 詳しくは、を参照してください [カタログ範囲](../catalog/introduction.md#catalog-scope).

## 手順 1：共有カタログの価格と構造の設定を開く

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**

1. グリッド内の共有カタログについては、 _[!UICONTROL Action]_列を選択してクリック&#x200B;**[!UICONTROL Set Pricing and Structure]**.

   ![共有カタログの価格と構造の設定](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. 共有カタログを初めて設定する場合は、 **[!UICONTROL Configure]** に移動して、次の手順を続行します。

## 手順 2：製品を選択する

プロセスの最初の手順は、共有カタログに含める製品を選択することです。 製品選択ページには、 [カテゴリツリー](../catalog/category-create.md) 左側に同期済み製品グリッド、右側に同期済み製品グリッド ツリーでカテゴリをクリックすると、カテゴリ内の製品がグリッドに表示されます。

製品が選択されているカテゴリのみが [上部ナビゲーション](../catalog/navigation-top.md) 共有カタログがストアフロントから表示された場合。 デフォルトでは、ストアフロントナビゲーションには最初の 3 つのカテゴリレベルのみが含まれ、ルートカテゴリは含まれません。

1. の使用 **ストア** を選択して、 [範囲](../catalog/introduction.md#product-scope) ：設定。

   設定の範囲は、共有カタログが初めて保存される前にのみ設定できます。 後で製品の選択を編集する場合、ストアの選択は使用できません。

   ![ストアを選択](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. カテゴリ ツリーで、次のいずれかの操作を行います。

   - すべての製品を含めるには、 **[!UICONTROL Select all]** 親カテゴリのチェックボックスをオンにします。
   - 製品の特定のカテゴリを含めるには、含める各カテゴリのチェックボックスをオンにします。
   - 個々の製品を含めるか除外するには、製品のチェックボックスを選択または選択解除します。

   ツリーの各カテゴリの下の表記は、共有カタログに現在含まれているカテゴリの製品数を示しています。 以下の表記 [ルートカテゴリ](../catalog/category-root.md) 共有カタログ用に現在選択されているすべてのカテゴリの製品の合計数が表示されます。

1. グリッドにカテゴリ製品を表示するには、ツリーでカテゴリの名前をクリックします。 カテゴリを選択すると、次の処理が行われます。

   - グリッドの最初の列の切替スイッチは緑に設定されています _日付：_ 選択した各製品の位置。
   - 製品が複数のカテゴリに割り当てられ、そのいずれかで選択されていない場合、他のカテゴリからも、また使用時にも使用できます [カタログ検索](../catalog/search.md).
   - 自動的に設定されます [カテゴリ権限](../catalog/category-permissions.md) 対象： `Allow` （選択した製品について）。

1. 必要に応じて、フィルターやその他のグリッド コントロールを使用して、共有カタログに含める製品を検索します。

   最初の列の切り替えをクリックして、個々の製品を個別に選択または除外できます。

   製品を持たないが、CMS コンテンツまたは外部リンクにリンクされているカテゴリを選択した場合、そのカテゴリはストアフロントの上部のナビゲーションに表示されます。

   作成したカテゴリ設定は、設定が保存されるまで、永続的にはデータベースに記録されません。 ただし、構造と価格を操作する際には、これらは一時的に保存されます。

1. クリック **[!UICONTROL Next]**.

   ![カタログに使用する製品を選択](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 手順 3：カスタム価格の設定

各製品のカスタム価格を個別に設定することも、 _[!UICONTROL Action]_複数の商品レコードに対して固定金額または固定率としてカスタム価格を設定するコントロール。

- **[!UICONTROL Fixed]**：最終製品価格を指定します。 例えば、$10.00 の固定価格を入力した場合、対応する会社のストアフロントの価格は$10.00 です。

  >[!NOTE]
  >
  >基本価格と入力された固定値の間の最小値が、最終製品価格として使用されます。

  >[!NOTE]
  >
  >**_固定価格_** 製品のカスタマイズ可能なオプション _ではない_ グループ価格、階層価格、特別価格、カタログ価格ルールの影響を受けます。

- **[!UICONTROL Percentage]**：割引率に基づいてカスタム価格を決定します。 例えば、10% の割引を提供するには、カスタム価格タイプをに設定します。 `Percentage` を入力します `10`. 値引きされるカスタム価格は、元の製品価格の 90% です。

以下の商品タイプについて、割引額を固定金額またはパーセンテージに設定するには、 _[!UICONTROL Custom Price]_グリッドの列：

- [シンプル](../catalog/product-create-simple.md) （設定可能な製品バリエーションを含む）
- [バンドル](../catalog/product-create-bundle.md)
- [ダウンロード可能](../catalog/product-create-downloadable.md)
- [仮想](../catalog/product-create-virtual.md)

の「カスタム価格」列は空白です [設定可能](../catalog/product-create-configurable.md) および [グループ化](../catalog/product-create-grouped.md) 製品タイプと [ギフトカード](../catalog/product-gift-card-create.md).

グリッド内の製品の選択は、 _カスタム価格_ ページ。 ただし、ページの上部にある進行状況インジケーターを使用して、前のステップに戻り、製品の選択を変更することができます。

![カタログに使用する製品を選択](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### カスタム価格を適用

1. マルチサイトインストールの場合、次のように設定します **[!UICONTROL Website]** をカスタム価格が適用される web サイトに追加します。

   ![Web サイトを選択](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. 次のいずれかの方法を使用して、カスタム価格を適用する製品を選択します。

   - カテゴリツリーを使用して、特定のカテゴリに含まれるすべての製品を選択します。
   - を _[!UICONTROL Mass Actions]_ヘッダーのコントロール `Select All`.
   - 個々の製品のチェックボックスを選択します。

   グリッドには、現在選択されているカテゴリの製品が表示されます。標準のコントロールを使用して、製品を検索したり、リストをフィルタしたりできます。

   ![すべて選択](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Actions]** を次のいずれかに変更します。

   - `Set Discount`  – 選択したすべての製品に割引率を適用します。 影響を受ける各製品価格は、 **_割引_** 価格。
   - `Adjust Fixed Price`  – 選択したすべての製品に固定価格割引率を適用します。 影響を受ける各製品価格は、 **_調整済み固定_** 価格。

   ![アクション管理 – 割引の設定](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. プロンプトが表示されたら、割引または価格調整を入力し、 **[!UICONTROL Apply]**.

   ![割引の設定](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![固定価格の調整](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   割引は、選択したすべての製品に適用され、 _カスタム価格_ 列には、適用された割引と金額のタイプが反映されます。

   ![値引き付きカスタム価格列](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### 階層価格を適用

[階層の価格](../catalog/product-price-tier.md) 共有カタログ内の製品に対して数量割引を提供できます。 この _階層価格_ グリッドの列には、へのリンクが含まれます _詳細価格_ 特に共有カタログに適用されるオプション。 製品に既に階層の価格が含まれている場合、既存の階層の数がリンクの後の括弧内に表示されます。

次の手順は、1 つの製品に階層価格を適用する方法を示しています。 複数の製品に階層価格を適用するには、次を参照してください [階層の価格のインポート](../systems/data-import-price-tier.md).

1. グリッド内の製品について、 _階層価格_ 列を選択してクリック **[!UICONTROL Configure]**.

   ![階層価格の設定](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. 日 _詳細価格_ ページ、クリック **[!UICONTROL Add Price]** 次の手順を実行します。

   ![カタログと階層の価格](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Website]** を Tier 価格が適用される Web サイトに送信します。
   - 割引を受けるために購入する必要がある商品の数量を入力します。
   - を設定 **[!UICONTROL Price]** 次のいずれかの割引タイプに適用されます。
      - `Fixed`
      - `Discount`
   - 割引額を入力します。
   - 別の階層に入るには、をクリックします **価格を追加** 次の層を定義するプロセスを繰り返します。

   ![複数の階層の価格](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Done]**.

   グリッドでは、階層の数が次の括弧内に表示されます _[!UICONTROL Tier Price]_列。

   ![複数の層](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## 構造と価格の保存

カスタム価格が終了したら、 **[!UICONTROL Generate Catalog]** その後 **[!UICONTROL Save]**.

これで、共有カタログがデータベースに保存されました。 その名前は _[!UICONTROL Shared Catalog]_の列_[!UICONTROL Products]_ グリッド。 次のステップは次のとおりです。 [共有カタログを会社に割り当てる](./catalog-shared-assign-companies.md).
