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

Adobe Commerce B2B を使用すると、ゲート接続を維持できます _共有_ 異なる会社のカスタム価格が設定されたカタログ。 標準に加えて、 _プライマリ_、製品カタログの順にクリックします。価格構造が異なる 2 種類の共有カタログに顧客がアクセスできます。

次の場合 [共有カタログ機能](enable-basic-features.md) が設定で有効になっている場合、元のプライマリカタログは管理者からは表示されますが、ストアフロントからはデフォルト（一般）の公開共有カタログのみ表示されます。 さらに、特定のメンバーのみに表示されるカスタムカタログを作成できます [会社](account-companies.md) アカウント。

の場合 `Default (General)` 公開共有カタログ。ストアフロントにカタログを表示するには、製品を割り当てる必要があります。 デフォルトでは空で、製品は含まれていません。

>[!NOTE]
>
>**[B2B リリース 1.3.0](release-notes.md#b2b-v130) 以降**  – 共有カタログを作成する場合、次の各項目 [カテゴリ権限](../catalog/category-permissions.md) カタログがに設定されている場合 _[!UICONTROL Allow for the Display Product Prices]_および_[!UICONTROL Add to Cart]_ カタログ権限設定でこのアクセス権が割り当てられている顧客グループの場合。 以前は、これらの設定は、自動的にに設定されていました `Deny` カタログの権限がに設定されている場合でも `Allow`.

>[!IMPORTANT]
>
>既存のすべて [グループ権限設定](../configuration-reference/catalog/catalog.md#category-permissions) は無視されます **_all_** 次の場合にカタログのカテゴリ **_[!UICONTROL Shared Catalog]_** この機能は有効です。 [!UICONTROL Shared Catalog] カタログが有効な場合、カタログのすべてのカテゴリ権限を完全に制御します。

この _[!UICONTROL Shared Catalogs]_共有カタログの管理に使用するツールにアクセスできます。 ページは標準に類似しています [管理ワークスペース](../getting-started/admin-workspace.md)フィルターおよびアクションコントロールを使用する場合。 グリッドには、既定のパブリック共有カタログを含むすべての共有カタログと、設定したカスタム カタログが一覧表示されます。

![共有カタログ](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## へのアクセス [!UICONTROL Shared Catalogs] ページ

日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## アクション制御

この [アクション制御](../getting-started/admin-actions-control.md) 左上コーナーでは、マス アクション コントロールと一緒に使用して、不要になった共有カタログを選択して削除できます。 グリッドで、 _[!UICONTROL Actions]_列には、共有カタログを管理するためのすべてのツールが含まれています。

![共有カタログのアクション](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

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
| [!UICONTROL Type] | 共有カタログのタイプは次のいずれかとして識別されます。 <br/>**[!UICONTROL Public]**- Adobe Commerce B2B がインストールされると、デフォルトの公開共有カタログが自動的に作成されます。 最初に、に割り当てられます `General` および `Not Logged In` 顧客グループ。会社に関連付けられていないゲストおよびログインしている個々の顧客に表示されます。 システムは一度に 1 つの公開共有カタログのみをサポートします。<br/>**[!UICONTROL Custom]** - カスタム共有カタログには、割り当てられた会社アカウントのログインした担当者にのみ表示される価格が含まれています。 カスタムの共有カタログは、必要な数だけ作成できます。 |
| [!UICONTROL Customer Tax Class] | 対応する顧客グループに割り当てられる税区分。 この列はデフォルトのグリッドには表示されませんが、列のレイアウトを変更することで追加できます。 |
| [!UICONTROL Created At] | 共有カタログが作成された日時。 |
| [!UICONTROL Created By] | 共有カタログを作成したストア管理者の姓と名。 |
| [!UICONTROL Action] | 選択したカタログに適用されるアクションを一覧表示します。 オプション： `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
