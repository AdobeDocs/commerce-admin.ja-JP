---
title: 共有カタログを管理
description: '[ 共有カタログ ] ページから使用できる情報とツールについて説明します。'
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# 共有カタログを管理

The _[!UICONTROL Shared Catalogs]_ページから、共有カタログの管理に必要なツールにアクセスできます。 このページは、標準の管理ワークスペースに似ており、フィルターとアクションコントロールを備えています。 グリッドには、既定の公開共有カタログと、設定済みのカスタムカタログを含む、すべての共有カタログが一覧表示されます。

## 製品選択を更新

共有カタログ内の製品の選択は、 _[!UICONTROL Action]_共有カタロググリッドの列。 加えた変更は、関連する会社アカウントのメンバーに対して表示されます。 このプロセスは、新しい製品を選択する場合と同じです。 [カタログ構造](catalog-shared-pricing-structure.md)の範囲を変更できない点を除きます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. グリッド内の共有カタログについて、 **[!UICONTROL Action]** 列と選択 **[!UICONTROL Set Pricing and Structure]**.

   ![共有カタログのグリッドとアクションメニュー](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. 詳しくは、 [手順 2：製品の選択](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   最初の項目はスキップできます。共有カタログを初めて保存した後は、共有カタログの範囲を変更できないからです。

特定の製品を使用している場合、 _[!UICONTROL Products In Shared Catalog]_「 」セクションには、製品が使用可能な各共有カタログの一覧が表示されます。 詳しくは、 [共有カタログに商品を追加する](catalog-shared-product-add.md).

![共有カタログ内の商品](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## カスタム価格の更新

共有カタログの製品のカスタム価格は、共有カタロググリッドの「アクション」列から簡単に更新できます。 加えた変更は、関連する会社または顧客グループのメンバーに対してストアフロントに表示されます。 このプロセスは、基本的に、新しい [共有カタログ](catalog-shared-pricing-structure.md)の範囲を変更できない点を除きます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 更新するグリッド内の共有カタログについて、 **[!UICONTROL Action]** 列と選択 **[!UICONTROL Set Pricing and Structure]**.

1. 次の日： _[!UICONTROL Catalog Structure]_ページ、クリック&#x200B;**[!UICONTROL Configure]**次のいずれかの操作を行います。

   - ページ上部の進行状況インジケーターで、 **[!UICONTROL Pricing]**.
   - 右上隅で、 **[!UICONTROL Next]**.

1. 詳しくは、 [手順 3：カスタム価格を設定する](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## カテゴリ権限を更新

[カテゴリ権限](../catalog/category-permissions.md) は自動的にに設定されます。 `Allow` カテゴリツリーから共有カタログに追加される製品の場合。 必要に応じて、後で権限を調整したり、追加のルールを作成したりできます。

>[!NOTE]
>
>**[B2B リリース 1.3.0](release-notes.md#b2b-v130) およびその後**  — 共有カタログを作成する場合、 [カテゴリ権限](../catalog/category-permissions.md) ( カタログが `Allow` （の） _[!UICONTROL Display Product Prices]_および_[!UICONTROL Add to Cart]_ カタログ権限設定でこのアクセス権を割り当てられた顧客グループの場合。 以前は、これらの設定は自動的に `Deny` （カタログ権限がに設定されている場合も） `Allow`.

>[!IMPORTANT]
>
>すべての既存 [グループ権限設定](../configuration-reference/catalog/catalog.md#category-permissions) は次の項目で無視されます： **_すべて_** カタログのカテゴリ ( **_[!UICONTROL Shared Catalog]_** 機能が有効になっている。 [!UICONTROL Shared Catalog] は、カタログが有効な場合に、カタログ内のすべてのカテゴリ権限を完全に制御します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. カテゴリツリーで、更新する製品のカテゴリを選択します。

   すべての製品を含めるには、ツリーの最上位カテゴリを選択します。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Category Permissions]** 」セクションに入力します。

1. クリック **[!UICONTROL New Permission]** 次の操作を実行します。

   ![新しい権限](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Customer Group]** 共有カタログに対応し、必要に応じて権限設定を変更します。

     ![カテゴリ権限ルール](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - 別の顧客グループの権限ルールを作成するには、 **[!UICONTROL New Permissions]** プロセスを繰り返します。

   - 権限ルールを削除するには、 _削除_ ![ごみ箱](../assets/icon-delete-trashcan-solid.png) アイコン。

1. 完了したら、「 **[!UICONTROL Save]**.

## カタログの詳細を更新

共有カタログの詳細情報は、共有カタロググリッドの「アクション」列から簡単に更新できます。 加えた変更は、関連する会社アカウントに反映されます。

![一般設定](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 更新する共有カタログの場合は、 **[!UICONTROL Action]** 列と選択 **[!UICONTROL General Settings]**.

   ![カタログの詳細](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. 必要に応じて、カタログの詳細情報を更新します。

   - 共有カタログの名前を変更すると、対応する顧客グループの名前も変更されます。
   - カタログタイプの変更元 `Custom` から `Public` 既存の公開カタログをカスタムカタログに変換します。 元の公開カタログに関連付けられている会社は、すべて置換に再割り当てされます。 公開カタログをカスタムカタログに変換することはできません。

1. 完了したら、「 **[!UICONTROL Save]**.

## 共有カタログページの参照

### ボタンバー

| ボタン | 説明 |
|--- |--- |
| [!UICONTROL Back] | 新しい共有カタログを保存せずに、共有カタログページに戻ります。 |
| [!UICONTROL Delete] | カタログを削除し、関連する会社とそのメンバーを公開共有カタログに再割り当てします。 |
| [!UICONTROL Reset] | 未保存の変更のフォームをクリアし、元のカタログの詳細情報を復元します。 |
| [!UICONTROL Duplicate] | を作成します。 [カタログの複製コピー](catalog-shared-create.md). カスタムカタログの場合は、元の（会社の関連付けを除く）価格モデルと構造。 公開共有カタログが複製されると、重複するカタログの種類が `custom`. また、重複したカタログと同じ名前で、対応する顧客グループも作成されます。 デフォルトでは、重複したカタログには _複製_ 元のカタログ。 |
| [!UICONTROL Save and Continue Edit] | すべての変更を保存し、フォームを編集モードで開いたままにします。 |
| [!UICONTROL Save] | 変更を保存し、フォームを閉じて、[ 共有カタログ ] ページに戻ります。 |

{style="table-layout:auto"}

### カタログの詳細

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Name] | 管理者全体および使用可能な顧客アカウント内で共有カタログが特定されます。 カタログ名は説明的で、32 文字以内にしてください。 同じ名前の 2 つの共有カタログを持つことはできません。 最大文字数： 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]**  — 割り当て先の特定の会社にのみ利用可能なカスタム価格でカタログを識別します。<br/>**[!UICONTROL Public]**— すべてのゲスト訪問者と、会社に関連していないログイン済み顧客が使用できる共有カタログを識別します。 Adobe Commerce用 B2B のインストール時に「デフォルト」の公開共有カタログが作成されますが、管理者が設定する必要があります。 一度に存在できる公開共有カタログは 1 つだけです。 |
| [!UICONTROL Customer Tax Class] | カタログからの購入に使用される税区分を決定します。 オプションには、使用可能な税区分がすべて含まれます。 |
| [!UICONTROL Description] | カタログの使用方法に関する簡単な説明です。 |

{style="table-layout:auto"}
