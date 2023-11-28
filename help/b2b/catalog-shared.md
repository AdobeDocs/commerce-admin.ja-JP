---
title: 共有カタログの概要
description: B2B がAdobe Commerce用に提供する共有カタログと、それらを使用して様々な会社アカウント用のカスタム価格でゲーテッドカタログを維持する方法について説明します。
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# 共有カタログの概要

B2B for Adobe Commerceを使用すると、ゲーティングを維持できます _共有_ 様々な会社のカスタム価格を含むカタログ。 標準に加えて、 _プライマリ_、製品カタログ、異なる価格構造を持つ 2 種類の共有カタログに顧客がアクセスできるようにします。

次の場合、 [共有カタログ機能](enable-basic-features.md) を設定で有効にすると、元のプライマリカタログは管理者に表示されたままになりますが、デフォルト（一般）の公開共有カタログのみがストアフロントに表示されます。 また、特定のメンバーにのみ表示されるカスタムカタログを作成できます [会社](account-companies.md) アカウント。

の `Default (General)` 公開共有カタログを使用する場合は、ストアフロントにカタログを表示する商品を割り当てる必要があります。 デフォルトでは、空で、製品は含まれていません。

>[!NOTE]
>
>**[B2B リリース 1.3.0](release-notes.md#b2b-v130) およびその後**  — 共有カタログを作成する場合、 [カテゴリ権限](../catalog/category-permissions.md) ( カタログが _[!UICONTROL Allow for the Display Product Prices]_および_[!UICONTROL Add to Cart]_ カタログ権限設定でこのアクセス権を割り当てられた顧客グループの場合。 以前は、これらの設定は自動的に `Deny` （カタログ権限がに設定されている場合も） `Allow`.

>[!IMPORTANT]
>
>すべての既存 [グループ権限設定](../configuration-reference/catalog/catalog.md#category-permissions) は次の項目で無視されます： **_すべて_** カタログのカテゴリ ( **_[!UICONTROL Shared Catalog]_** 機能が有効になっている。 [!UICONTROL Shared Catalog] は、カタログが有効な場合に、カタログ内のすべてのカテゴリ権限を完全に制御します。

The _[!UICONTROL Shared Catalogs]_ページから、共有カタログの管理に使用するツールにアクセスできます。 このページは、標準の [管理ワークスペース](../getting-started/admin-workspace.md)、フィルターおよびアクションコントロールを使用します。 グリッドには、既定の公開共有カタログと、設定済みのカスタムカタログを含む、すべての共有カタログが一覧表示されます。

![共有カタログ](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## 次にアクセス： [!UICONTROL Shared Catalogs] ページ

次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## アクションコントロール

The [アクションコントロール](../getting-started/admin-actions-control.md) 左上隅では、マスアクションコントロールと共に使用して、不要になった選択した共有カタログを削除できます。 グリッドで、 _[!UICONTROL Actions]_列には、共有カタログを管理するためのツールがすべて含まれます。

![共有カタログアクション](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| 制御 | 説明 |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | 共有カタログで使用可能な製品の選択とカスタム価格を決定します。 |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | 共有カタログにアクセスできる会社を決定します。 |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | 名前、カタログタイプ、顧客税区分、説明など、カタログの詳細情報を決定します。 |
| [!UICONTROL Delete] | 選択した共有カタログを削除します。 |

{style="table-layout:auto"}

## 列の説明

| 見出し | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションを適用する共有カタログレコードを選択します。 ヘッダーのコントロールを使用して、グリッド内の共有カタログレコードをすべて選択したり、すべて選択を解除したりできます。 個々の共有カタログを選択するには、チェックボックスをオンにします。 |
| [!UICONTROL ID] | カタログの作成時に順に割り当てられる一意の数値識別子。 |
| [!UICONTROL Name] | 共有カタログの名前。 デフォルト（一般）の共有カタログが使用可能です。 |
| [!UICONTROL Type] | 共有カタログの種類を次のいずれかとして識別します。 <br/>**[!UICONTROL Public]**- B2B for Adobe Commerceのインストール時に、デフォルトの公開共有カタログが自動的に作成されます。 最初は `General` および `Not Logged In` 顧客グループに分類され、会社に関連付けられていないゲストおよび個人のログイン済み顧客に対して表示されます。 システムは、一度に 1 つの公開共有カタログのみをサポートします。<br/>**[!UICONTROL Custom]**  — カスタム共有カタログには、割り当てられた会社アカウントのログイン済みの関係者にのみ表示される価格設定が含まれます。 カスタム共有カタログは必要な数だけ作成できます。 |
| [!UICONTROL Customer Tax Class] | 対応する顧客グループに割り当てられる税区分。 この列は既定のグリッドには表示されませんが、列のレイアウトを変更して追加できます。 |
| [!UICONTROL Created At] | 共有カタログが作成された日時。 |
| [!UICONTROL Created By] | 共有カタログを作成したストア管理者の姓名です。 |
| [!UICONTROL Action] | 選択したカタログに適用されるアクションを一覧表示します。 オプション： `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
