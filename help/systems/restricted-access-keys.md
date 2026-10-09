---
title: Commerceでの制限付きアクセスキーの管理
description: Adobe Adobe Commerce Optimizerに同期されたB2B共有カタログビューを保護するための制限付きアクセスキーを作成、割り当て、削除します。
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
last-update: 2026-10-01
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: 601e4abe-d9bf-58de-a779-32ed6794dcbe
    internal-label: Data Import/Export
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%
---

# 制限付きアクセスキーの管理

制限付きアクセスキーのページを使用して、[!DNL Adobe Commerce Optimizer Connector for B2B]によって作成されたプライベートカタログビューのアクセスキーを管理します。 このコネクタは、B2B共有カタログ設定をAdobe CommerceからAdobe Commerce Optimizerに同期します。

>[!NOTE]
>
>パートナーポータルなど、B2B以外のシナリオでプライベートカタログの管理に使用される手動で作成されたキーの場合、[[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/ja/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"}からキーを管理します。

## オーディエンスと可用性 {#audience}

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud Infrastructureおよびオンプレミスプロジェクトにのみ適用されます。"}

[!UICONTROL Restricted Access Keys] ページは、[!DNL Adobe Commerce Optimizer Connector for B2B]でB2B共有カタログを使用するAdobe Commerce on Cloud Infrastructureおよびオンプレミス マーチャントで利用できます。 コネクターは、ページを自動的にインストールして有効にします。

共有カタログに対して最初にカタログビューを作成すると、コネクタは1つのキーを自動的に生成して割り当てます。 このページを使用すると、そのキーを表示したり、追加のキーを作成、割り当て、削除したりできます。

## 制限付きアクセスキーのページへのアクセス {#access-restricted-access-keys-page}

管理領域から、**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**&#x200B;に移動します。

![制限付きアクセスキーのページに、キーと割り当てられたカタログビューが一覧表示される](assets/restricted-access-keys.png){width="600" zoomable="yes"}

このページには、カタログ ビューに割り当てられているかどうかにかかわらず、すべてのキーが一覧表示されます。 特定のカタログ ビューにキーを割り当てるには、代わりにそのカタログ ビューで[!UICONTROL Edit Restricted Access Keys] アクションを使用します。 「[&#x200B; カタログ ビューにキーを割り当て](#assign-keys-to-a-catalog-view)」を参照してください。

## 制限付きアクセスキーの概要 {#restricted-access-keys-summary}

グリッドには、行ごとに1つのキーが含まれています。

| フィールド | 説明 |
| --- | --- |
| **キーID** | 一意のキー識別子。 |
| **タイトル** | キーを識別するために指定するラベル。 |
| **割り当てられたカタログ ビュー** | このキーが現在割り当てられているカタログビュー。 |
| **有効期限** | キーの有効期限。 |
| **アクション** | 行レベルのアクション： [&#x200B; キーの管理](#manage-keys)を参照してください。 |

## キーの管理 {#manage-keys}

- **[!UICONTROL Create Key]** – 割り当てられていない新しいキーペアを生成します。 Commerceはキーペアを生成し、秘密鍵を保存します。 カタログ ビューにキーを割り当てるまで、公開鍵は[!DNL Adobe Commerce Optimizer]に登録されません。
- **[!UICONTROL View Public Key]** - キーの公開鍵の読み取り専用ビューを開き、必要に応じてキーを再登録または再同期するためにコピーできます。 秘密鍵は表示されません。
- **[!UICONTROL Delete]** - キーを削除し、[!DNL Adobe Commerce Optimizer]のリモート登録を取り消します。 このキーですでに発行されたストアフロントトークンは、有効期限が切れるまで有効です。 この操作は元に戻せません。

>[!NOTE]
>
>期限切れのキーは削除できません。 期限切れのキーを割り当てたり、割り当て解除したりすることはできません。

## キーを作成

[!UICONTROL Restricted Access Keys] ページで、**[!UICONTROL Create Key]**&#x200B;を選択してキーを作成します。

Commerceは新しいキーペアを生成し、秘密鍵を保存します。 制限付きアクセスキーのテーブルは、一意のキーIDを示す新しいキーのエントリで更新されます。 この[!UICONTROL Key ID]は、カタログ ビューにキーを割り当てる場合に使用します。

カタログ ビューにキーを割り当てるまで、公開鍵は[!DNL Adobe Commerce Optimizer]に登録されません。 登録後、制限付きアクセスキーのテーブルエントリが更新され、カタログの割り当てと有効期限が表示されます。

## 制限付きアクセスキーの割り当てまたは削除 {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## キーの選択とローテーション {#key-selection-and-rotation}

カタログ ビューに複数のキーが割り当てられている場合、[!DNL Adobe Commerce]は、割り当てられた期限切れでないキーを自動的に使用して、最新の有効期限でトークンに署名します。

>[!IMPORTANT]
>
>自動キーローテーションはまだ利用できません。 キーのデフォルトは長い有効期限です。 キーを手動で回転するには、新しいキーを作成し、既存のキーと並行してカタログビューに割り当てます。 新しいキーが使用されていることを確認したら、古いキーを削除します。

新しく作成したキーに適用されるデフォルトの有効期限を変更するには、**[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**&#x200B;に移動します。 [&#x200B; サービス/ACO制限付きアクセスキー](../configuration-reference/services/aco-restricted-access-keys.md)を参照してください。

## 既知の制限事項 {#known-limitations}

- メインの[!UICONTROL Restricted Access Keys] グリッドにアクティブまたはステータス インジケーターがありません。

  リンクのステータスは、[!UICONTROL Edit Restricted Access Keys] ページで確認できます。 ドロップダウンを使用して、使用可能なキーとそのステータスを表示します。 キーがカタログ ビューに割り当てられている場合、そのキーはリンクされます。 割り当てられていない場合、ステータスはありません。 これらのキーは、編集中のカタログビューに割り当てることができます。

  [!UICONTROL Catalog View Sync Status] ページでは、カタログビューの詳細ページ（**[!UICONTROL View details]** アクション）から、カタログビューにリンクされたキーを表示できます。 詳細ページには、カタログ ビューに割り当てられたか割り当てられていないかを含む、キー履歴も表示されます。

- 自動キーローテーションはまだ利用できません。

>[!MORELIKETHIS]
>
> - [&#x200B; カタログ ビュー設定の管理](/help/b2b/catalog-views-manage.md) – 共有カタログまたは会社アカウントからこれらのキーを割り当てます
> - [&#x200B; カタログ ビュー同期ステータス監視](catalog-view-sync-status.md) – これらのキーで保護されているカタログ ビューを監視および調整します
> - [&#x200B; サービス/ACO制限付きアクセス キー](../configuration-reference/services/aco-restricted-access-keys.md) — デフォルトのキー有効期限を設定します
> - [&#x200B; サービス/ACO カタログビュー](../configuration-reference/services/aco-catalog-view.md) — ストアフロントのアクセストークンの有効期間を設定し、発行を有効または無効にします
> - *Adobe Commerce Optimizer コネクタ ガイド*&#x200B;の[制限付きアクセス キーの管理](https://experienceleague.adobe.com/ja/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} – これらのキーをB2B共有カタログ同期に適合させる方法について説明します
> - *Adobe Commerce Optimizer ガイド*&#x200B;の[制限付きアクセスキー](https://experienceleague.adobe.com/ja/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} — B2B以外のユースケース向けのACO Studio ベースの手動キーフロー
