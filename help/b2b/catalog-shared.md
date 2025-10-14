---
title: 共有カタログの概要
description: Adobe Commerce B2B が提供する共有カタログと、それらを使用して、様々な会社アカウントのカスタム価格でゲート付きカタログを管理する方法について説明します。
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# 共有カタログの概要

Adobe Commerce B2B を使用すると、様々な会社のカスタム価格でゲート _共有_ カタログを管理できます。 標準の _プライマリ_ 製品カタログに加えて、価格構造が異なる 2 種類の共有カタログへのアクセスが顧客に提供されます。

設定で [&#x200B; 共有カタログ機能 &#x200B;](enable-basic-features.md) が有効になっている場合、元のプライマリカタログは管理者には表示されますが、ストアフロントにはデフォルト（一般）の公開共有カタログのみが表示されます。 さらに、特定の [&#x200B; 会社 &#x200B;](account-companies.md) アカウントのメンバーにのみ表示されるカスタムカタログを作成できます。

`Default (General)` の公開共有カタログの場合、ストアフロントにカタログを表示するには製品を割り当てる必要があります。 デフォルトでは空で、製品は含まれていません。

>[!NOTE]
>
>**[B2B リリース 1.3.0](release-notes.md#b2b-v130) 以降** – 共有カタログを作成すると、カタログの各 [&#x200B; カテゴリ権限 &#x200B;](../catalog/category-permissions.md) は _[!UICONTROL Allow for the Display Product Prices]_&#x200B;に設定され、カタログ権限設定でこのアクセス権が割り当てられた顧客グループの&#x200B;_[!UICONTROL Add to Cart]_ に設定されます。 以前は、カタログ権限が `Deny` に設定されている場合でも、これらの設定は自動的に `Allow` に設定されていました。

>[!IMPORTANT]
>
>**_[!UICONTROL Shared Catalog]_** 機能が有効な場合、既存のすべての [&#x200B; グループ権限設定 &#x200B;](../configuration-reference/catalog/catalog.md#category-permissions) は、カタログ内の **_すべて_** カテゴリで無視されます。 カタログ [!UICONTROL Shared Catalog] 有効にすると、カタログのすべてのカテゴリ権限が完全に制御されます。

_[!UICONTROL Shared Catalogs]_&#x200B;ページでは、共有カタログの管理に使用するツールにアクセスできます。 このページは、フィルターとアクションコントロールを備えた、標準の [&#x200B; 管理ワークスペース &#x200B;](../getting-started/admin-workspace.md) に似ています。 グリッドには、既定のパブリック共有カタログを含むすべての共有カタログと、設定したカスタム カタログが一覧表示されます。

![&#x200B; 共有カタログ &#x200B;](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## [!UICONTROL Shared Catalogs] ページへのアクセス

_管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Shared Catalogs]** に移動します。

## アクション制御

左上隅の [&#x200B; アクション コントロール &#x200B;](../getting-started/admin-actions-control.md) をマス アクション コントロールと一緒に使用して、不要になった選択した共有カタログを削除できます。 グリッドの _[!UICONTROL Actions]_&#x200B;の列には、共有カタログを管理するためのツールがすべて表示されます。

![&#x200B; 共有カタログのアクション &#x200B;](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| 制御 | 説明 |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | 共有カタログで利用できる製品の選択とカスタム価格を決定します。 |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | 共有カタログにアクセスできる会社を決定します。 |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | カタログの詳細情報（名称、カタログ・タイプ、顧客税金クラスおよび摘要を含む）を決定します。 |
| [!UICONTROL Delete] | 選択した共有カタログを削除します。 |

{style="table-layout:auto"}

## 列の説明

| 見出し | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションを適用する共有カタログ レコードを選択します。 ヘッダーのコントロールを使用して、グリッド内のすべての共有カタログレコードを選択または選択解除できます。 個々の共有カタログを選択するには、チェックボックスをオンにします。 |
| [!UICONTROL ID] | カタログの作成時に順番に割り当てられる一意の数値識別子。 |
| [!UICONTROL Name] | 共有カタログの名前。 デフォルトでは、デフォルト（一般）の共有カタログを使用できます。 |
| [!UICONTROL Type] | <br/>**[!UICONTROL Public]**- Adobe Commerce B2B がインストールされると、デフォルトの公開共有カタログが自動的に作成されます。 最初は `General` と `Not Logged In` の顧客グループに割り当てられ、会社に関連付けられていないゲストおよびログインしている個々の顧客に表示されます。 システムは一度に 1 つの公開共有カタログのみをサポートします。<br/>**[!UICONTROL Custom]** - カスタム共有カタログには、割り当てられた会社アカウントのログインした担当者にのみ表示される価格が含まれています。 カスタムの共有カタログは、必要な数だけ作成できます。 |
| [!UICONTROL Customer Tax Class] | 対応する顧客グループに割り当てられる税区分。 この列はデフォルトのグリッドには表示されませんが、列のレイアウトを変更することで追加できます。 |
| [!UICONTROL Created At] | 共有カタログが作成された日時。 |
| [!UICONTROL Created By] | 共有カタログを作成したストア管理者の姓と名。 |
| [!UICONTROL Action] | 選択したカタログに適用されるアクションを一覧表示します。 オプション：`Set Pricing and Structure`/`Assign Companies`/`General Settings`/`Delete` |

{style="table-layout:auto"}
