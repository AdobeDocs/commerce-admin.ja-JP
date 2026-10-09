---
title: 共有カタログの管理
description: 共有カタログ ページで使用できる情報とツールについて説明します。
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
last-update: 2026-10-01
TQID: 'https://experienceleague.adobe.com/q2dtQ-y3ByGhtMNp68-3lN-PqZJ-1mRX4BMCu0lfB54'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%
---
# 共有カタログの管理

_[!UICONTROL Shared Catalogs]_ページでは、商品の選択、カスタム価格、カテゴリ権限、カタログの詳細など、共有カタログの管理に必要なツールにアクセスできます。 このページは、フィルターとアクションコントロールを備えた標準的な管理者ワークスペースに似ています。 グリッドには、デフォルトのパブリック共有カタログを含むすべての共有カタログと、設定したカスタムカタログが一覧表示されます。

[!DNL Adobe Commerce Optimizer Connector for B2B]拡張機能がインストールされている場合、このページでは、コネクタが各共有カタログのデータを[!DNL Adobe Commerce Optimizer]に同期するときに作成された[!DNL Adobe Commerce Optimizer] カタログビューと、B2B ストアフロントエクスペリエンスのカタログビューを保護する制限付きアクセスキーにもアクセスできます。

## 製品の選択を更新

共有カタログ内の商品の選択は、共有カタロググリッドの&#x200B;_[!UICONTROL Action]_列から簡単に更新できます。 変更は、関連する会社アカウントのメンバーに対して表示されます。 このプロセスは、新しい[ カタログ構造](catalog-shared-pricing-structure.md)の製品を選択する場合と同じですが、設定の範囲を変更することはできません。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**&#x200B;に移動します。

1. グリッド内の共有カタログの場合は、**[!UICONTROL Action]**&#x200B;列に移動し、**[!UICONTROL Set Pricing and Structure]**&#x200B;を選択します。

   ![共有カタログ グリッドとアクション メニュー](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. [手順2：製品を選択](catalog-shared-pricing-structure.md#step-2-choose-the-products)の指示に従います。

   最初のアイテムはスキップできます。共有カタログの範囲は、初めて保存した後に変更できません。

特定の製品を使用している場合、_[!UICONTROL Products In Shared Catalog]_セクションには、製品が使用可能な各共有カタログが一覧表示されます。 詳しくは、[共有カタログに商品を追加](catalog-shared-product-add.md)を参照してください。

共有カタログ内の![製品](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## カスタム価格の更新

共有カタログ内の製品のカスタム価格は、共有カタログ グリッドの「アクション」列から簡単に更新できます。 変更は、関連する会社または顧客グループのメンバーに対して、ストアフロントに表示されます。 このプロセスは、新しい[共有カタログ ](catalog-shared-pricing-structure.md)のカスタム価格の設定と同じですが、設定の範囲を変更することはできません。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**&#x200B;に移動します。

1. 更新するグリッド内の共有カタログの場合は、**[!UICONTROL Action]**&#x200B;列に移動し、**[!UICONTROL Set Pricing and Structure]**&#x200B;を選択します。

1. _[!UICONTROL Catalog Structure]_ページで、**[!UICONTROL Configure]**をクリックし、次のいずれかの操作を行います。

   - ページの上部にある進行状況インジケーターで、**[!UICONTROL Pricing]**&#x200B;をクリックします。
   - 右上隅の「**[!UICONTROL Next]**」をクリックします。

1. [手順3: カスタム価格を設定](catalog-shared-pricing-structure.md#step-3-set-custom-prices)の手順に従います。

## カテゴリ権限の更新

カテゴリ ツリーから共有カタログに追加された製品の[ カテゴリ権限](../catalog/category-permissions.md)は、自動的に`Allow`に設定されます。 必要に応じて、後で権限を調整したり、追加のルールを作成したりできます。

>[!NOTE]
>
>**[B2B リリース 1.3.0](release-notes.md#b2b-v130)以降** – 共有カタログを作成する場合、割り当てられた顧客グループの&#x200B;_[!UICONTROL Display Product Prices]_と_[!UICONTROL Add to Cart]_&#x200B;について、各[ カテゴリ権限](../catalog/category-permissions.md)が`Allow`に設定されます。 以前は、カタログ権限が`Allow`に設定されていても、これらの設定は自動的に`Deny`に設定されていました。

>[!IMPORTANT]
>
>有効にすると、**_[!UICONTROL Shared Catalog]_**&#x200B;は、カタログ内の&#x200B;**_すべて_**&#x200B;のカテゴリに対する既存のすべての[ グループ権限設定](../configuration-reference/catalog/catalog.md#category-permissions)を置き換えます。 [!UICONTROL Shared Catalog]は、カタログが有効になっている場合に、カタログ内のすべてのカテゴリ権限を完全に制御します。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. カテゴリーツリーで、更新する製品のカテゴリを選択します。

   すべての製品を含めるには、ツリーの最上位カテゴリを選択します。

1. 下にスクロールして、**[!UICONTROL Category Permissions]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL New Permission]**&#x200B;をクリックし、次の操作を行います。

   ![新しい権限](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - 共有カタログに対応する&#x200B;**[!UICONTROL Customer Group]**&#x200B;を選択し、必要に応じて権限設定を変更します。

     ![ カテゴリ権限ルール ](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - 別の顧客グループの権限ルールを作成するには、**[!UICONTROL New Permissions]**&#x200B;をクリックして、プロセスを繰り返します。

   - 権限ルールを削除するには、_削除_ ![ごみ箱](../assets/icon-delete-trashcan-solid.png) アイコンをクリックします。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## カタログの詳細を更新

共有カタログの詳細情報は、共有カタログ グリッドの「アクション」列から簡単に更新できます。 変更は、関連する会社アカウントに反映されます。

![一般設定](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**&#x200B;に移動します。

1. 更新する共有カタログの場合は、**[!UICONTROL Action]**&#x200B;列に移動し、**[!UICONTROL General Settings]**&#x200B;を選択します。

   ![ カタログの詳細](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. 必要に応じて、カタログの詳細情報を更新します。

   - 共有カタログの名前を変更すると、対応する顧客グループの名前も変更されます。
   - カタログの種類を`Custom`から`Public`に変更すると、既存のパブリック カタログがカスタム カタログに変換されます。 元の公開カタログに関連付けられている会社は、置き換えに再割り当てされます。 パブリックカタログをカスタムカタログに変換することはできません。
   - 共有カタログを通じて行われた購入に適用される税分類を識別するには、[!UICONTROL Customer Tax Class]を選択します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## カタログビュー設定の管理

[!DNL Adobe Commerce Optimizer Connector for B2B]拡張機能がインストールされている場合、共有カタログの&#x200B;_[!UICONTROL Catalog Views]_セクションには、共有カタログから投影された[!DNL Adobe Commerce Optimizer] カタログビューが一覧表示され、それらを保護する制限付きアクセスキーを管理できます。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**&#x200B;に移動します。

1. 確認する共有カタログの場合は、**[!UICONTROL Action]**&#x200B;列に移動し、**[!UICONTROL General Settings]**&#x200B;を選択します。

1. _[!UICONTROL Shared Catalog Information]_パネルで、**[!UICONTROL Catalog Views]**を選択します。

カタログビューと制限付きアクセスキーの編集について詳しくは、[ カタログビュー設定の管理](catalog-views-manage.md)を参照してください。

## 共有カタログページ参照

### ボタンバー

| ボタン | 説明 |
| --- | --- |
| [!UICONTROL Back] | 新しい共有カタログを保存せずに、共有カタログページに戻ります。 |
| [!UICONTROL Delete] | カタログを削除し、関連する会社とそのメンバーをパブリック共有カタログに再割り当てします。 |
| [!UICONTROL Reset] | 保存されていない変更のフォームを消去し、元のカタログの詳細情報を復元します。 |
| [!UICONTROL Duplicate] | カタログの[複製コピー](catalog-shared-create.md)を作成します。 カスタムカタログの場合は、元の価格設定モデルと構造が使用されますが、会社の関連付けはありません。 公開されている共有カタログが複製されると、複製されたカタログの種類は`custom`に変更されます。 対応する顧客グループも、重複カタログと同じ名前で作成されます。 デフォルトでは、重複したカタログには、元のカタログの&#x200B;_個の_&#x200B;重複という名前が付けられます。 |
| [!UICONTROL Save and Continue Edit] | すべての変更を保存し、フォームを編集モードで開いたままにします。 |
| [!UICONTROL Save] | 変更を保存し、フォームを閉じて、共有カタログ ページに戻ります。 |

{style="table-layout:auto"}

### カタログの詳細

| フィールド | 説明 |
| --- | --- |
| [!UICONTROL Name] | 管理者全体および利用可能な顧客アカウント内の共有カタログを識別します。 カタログ名は説明的で、32文字以下にする必要があります。 同じ名前の2つの共有カタログを持つことはできません。 最大文字数：32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** – 割り当てられた特定の企業のみが利用できるカスタム価格設定のカタログを識別します。<br/>**[!UICONTROL Public]**– すべてのゲスト訪問者と、会社に関連付けられていないログイン顧客が利用できる共有カタログを識別します。 「デフォルト」の公開共有カタログは、Adobe Commerce B2Bのインストール時に作成されますが、管理者が設定する必要があります。 一度に存在できる公開共有カタログは1つだけです。 |
| [!UICONTROL Customer Tax Class] | カタログから作成された購入に使用される税区分を指定します。 オプションには、使用可能なすべての税区分が含まれます。 税区分は、共有カタログに作成または使用される顧客グループに関連付けられます。 [税区分](../stores-purchase/tax-class.md)を参照してください。 |
| [!UICONTROL Description] | カタログの使用方法を簡単に説明します。 |

{style="table-layout:auto"}

### カタログビュー

{{$include /help/_includes/catalog-views-reference-table.md}}
