---
title: カタログビュー同期ステータスの監視
description: B2B共有カタログのプロジェクションヘルスを監視し、Adobe Commerce Optimizer Connectorのカタログビュー、ポリシー、価格表、アクセスキーを調整します。
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
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
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%
---

# カタログビューの同期ステータスモニタリング

「カタログ表示の同期ステータス」ページを使用して、Adobe Commerce Optimizerに投影されたカタログ表示の同期とトラブルシューティングを監視します。 カスタム共有カタログごとに、[!DNL Adobe Commerce Optimizer Connector for B2B]は、共有カタログのweb サイト スコープ内の各ストア ビューのカタログ ビューを作成します。 各カタログビューには、品揃えポリシー、リンクされた価格表、アクセス制限トークンの検証に使用される公開鍵が設定されています。 Adobe Commerceは、秘密鍵とデフォルトの価格表IDを含む、対応するカタログビューメタデータを保持します。

>[!NOTE]
>
>カタログデータフィードの同期ステータスを追跡するには、[[!UICONTROL Data Feed Sync Status]](data-feed-sync-status.md) ページを使用します。

## オーディエンスと可用性 {#audience}

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud Infrastructureおよびオンプレミスプロジェクトにのみ適用されます。"}

[!UICONTROL Catalog View Sync Status] ページは、[!DNL Adobe Commerce Optimizer Connector for B2B]統合でB2B共有カタログを使用するAdobe Commerce on Cloud Infrastructureおよびオンプレミス マーチャントで利用できます。 コネクター拡張機能がインストールされると、ページが自動的にインストールされ、有効になります。

## カタログ ビュー同期ステータス ページにアクセスする {#access-catalog-view-sync-status-page}

管理領域から、**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Catalog View Sync Status]**&#x200B;に移動します。

![&#x200B; カタログ ビューの同期ステータス ページに、同期の正常性を示すカタログ ビューが一覧表示されます](assets/catalog-view-sync-status.png){width="600" zoomable="yes"}

このページには3つのタブがあります。

- **[!UICONTROL Catalog Views]** - コネクタによって作成されたカタログビューと、それぞれの同期状態。 [&#x200B; カタログ ビュー同期ステータスの概要](#catalog-view-sync-status-summary)を参照してください。
- **[!UICONTROL Orphaned in ACO]** – 対応する[!DNL Adobe Commerce] ソースがない[!DNL Adobe Commerce Optimizer]に存在するエンティティ。 「[孤立したACO タブ &#x200B;](#orphaned-in-aco-tab)」を参照してください。
- **[!UICONTROL Deleted]** – 共有カタログが削除されたため、カタログビューの予測のレコードが削除されました。 「[&#x200B; タブを削除しました](#deleted-tab)」を参照してください。

## カタログ ビュー同期ステータスの概要 {#catalog-view-sync-status-summary}

ページ上部の概要カードには、各ヘルスステートのカタログビュー数と、30日以内に有効期限が切れる制限付きアクセスキーの数が表示されます。

| カード | 説明 |
| --- | --- |
| **正常** | ドリフトが検出されないカタログビュー。 |
| **デグレード済み** | 修復可能なドリフトを使用したカタログビュー。 |
| **失敗** | 作成されなかった、または[!DNL Adobe Commerce Optimizer]で直接削除されたカタログビュー。 |
| **キー≤ 30D** | 制限付きアクセスキーが30日以内に期限切れになります。 |

グリッドには、カタログビューごとに1行が一覧表示されます。

| フィールド | 説明 |
| --- | --- |
| **カタログ ビュー** | [!DNL Adobe Commerce Optimizer]に投影されるカタログ ビューの識別子。 |
| **Source** | カタログビューの予測元の共有カタログ。 リンクを選択して、管理画面で共有カタログを開きます。 |
| **ストアビュー** | カタログビューが表すストアビュー。 |
| **企業** | このカタログ ビューに現在リンクされている会社の数。 |
| **ステータス** | カタログビューの全体的な同期状態。 [&#x200B; ステータス値の同期](#sync-status-values)を参照してください。 |
| **ポリシー** | このカタログ ビューに割り当てられた品揃えポリシーが[!DNL Adobe Commerce]設定と一致するかどうか。 |
| **価格表** | このカタログ ビューに割り当てられた価格表が[!DNL Adobe Commerce]設定と一致するかどうか。 |
| **アクセスキー** | 制限付きアクセス キーがこのカタログ ビューにリンクされているかどうか。 |
| **キーの有効期限** | カタログビューの制限付きアクセスキーの有効期限、残りの日数。 |
| **ドリフト** | 検出されたドリフトのタイプ（存在する場合）。 |
| **最終調整済み** | 紐付けプロセスが最後にこのカタログビューをチェックした際。 |
| **アクション** | **[!UICONTROL View details]**&#x200B;は、現在のステータス、ドリフト、アクセスキー、および最近のイベントを表示するカタログ表示同期ステータスの詳細ページを開きます。 **[!UICONTROL Open in ACO admin]**&#x200B;さんが[!DNL Adobe Commerce Optimizer] Studioでカタログビューの詳細ページを開きます。 **[!UICONTROL Copy ID]**&#x200B;は、参照のためにカタログ ビューIDをコピーします。 [調整と修復のドリフト &#x200B;](#reconcile-and-repair-drift)を参照してください。 |

## 同期ステータス値 {#sync-status-values}

| ステータス | 意味 |
| --- | --- |
| **正常** | ドリフトが検出されませんでした。 カタログ ビュー、ポリシー、価格表、およびキーは、[!DNL Adobe Commerce]設定と一致します。 |
| **デグレード済み** | Driftが検出され、修復可能です。たとえば、ポリシーまたは価格表が[!DNL Adobe Commerce Optimizer]で直接変更されました。 |
| **失敗** | カタログ ビューは作成されなかったか、[!DNL Adobe Commerce Optimizer]で直接削除されました。 |
| **保留中** | カタログ ビューはまだ調整されていないか、最初の投影を待っています。 |
| **期限切れ** | 共有カタログは[!DNL Adobe Commerce]に削除されました。カタログ ビューは削除猶予期間内です。 |
| **削除済み** | カタログ ビューの投影は、猶予期間の後に削除されました。 これは[!UICONTROL Deleted] タブのレコードとして90日間保持されます。 |
| **孤立** | カタログ ビューまたはキーは[!DNL Adobe Commerce Optimizer]に存在しますが、対応する[!DNL Adobe Commerce] ソースがありません。 「[孤立したACO タブ &#x200B;](#orphaned-in-aco-tab)」を参照してください。 |

### 削除猶予期間の設定 {#configure-the-deletion-grace-period}

削除猶予期間は、関連付けられた共有カタログを削除した後の、カタログビューと関連データのデータ保持ウィンドウを指定します。 デフォルトの値は7日間です。
ウィンドウの有効期限が切れると、すべてのデータが削除されます。

#### データ保持設定の変更

1. [!DNL Adobe Commerce]管理者を開きます。

1. **[!UICONTROL Stores]** メニューから、**[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Catalog View Sync]** > **[!UICONTROL Deletion]** > **[!UICONTROL Deletion Grace Period (days)]**&#x200B;を選択します。

1. 必要に応じて&#x200B;**[!UICONTROL Deletion Grace Period (days)]**&#x200B;値を更新します。

   共有カタログを削除した直後にカタログビューのACO投影を削除するには、この値を`0`に設定します。

1. **[!UICONTROL Save Config]**&#x200B;を選択します。

詳しくは、使用可能なすべての同期およびドリフト調整の設定について、[&#x200B; サービス/ACO カタログビュー同期](../configuration-reference/services/aco-catalog-view-sync.md)を参照してください。

## 設定の違いの調整と修復 {#reconcile-and-repair-drift}

[!DNL Adobe Commerce]は、B2B共有カタログ投影の信頼できるソースです。 紐付けは、[!DNL Adobe Commerce]設定を[!DNL Adobe Commerce Optimizer]と比較し、違いを報告または修復します。

>[!IMPORTANT]
>
>コネクタで管理されたカタログ ビュー、ポリシー、価格表、またはキーに対して[!DNL Adobe Commerce Optimizer]で直接行われた変更は、信頼できる唯一の情報源ではありません。 紐付けでは、これらは設定の違いとして報告され、修復すると、[!DNL Adobe Commerce]に一致するように元に戻されます。 [!DNL Adobe Commerce Optimizer]ではなく、[!DNL Adobe Commerce]で設定を変更します。 修復では、コネクタで管理されているポリシーと一緒に手動で追加したポリシーは削除されません。

ページレベルのボタンを使用して、調整します。

- **[!UICONTROL Reconcile]** – 設定の違いを確認し、[!DNL Adobe Commerce Optimizer]で変更を加えずに同期ステータスを更新します。

- **[!UICONTROL Reconcile & Repair]** – 設定の違いを確認し、修復可能な違いがあれば、予想される設定を自動的に復元します。

  **[!UICONTROL Reconcile & Repair]**&#x200B;を選択すると、非同期調整リクエストが送信され、修復が実行される前に返されます。 確認メッセージが表示され、ステータスがすぐに更新されますが、ページが自動的にリロードされません。 処理が終了するまで待ってから、グリッドを更新して結果を確認します。

行の&#x200B;**[!UICONTROL Action]** メニューを使用して、以下を行います。

- **[!UICONTROL View details]** - カタログ表示の同期ステータスの詳細ページを開いて、現在のステータス、ドリフト、アクセスキー、および最近のイベントを表示します。
- **[!UICONTROL Open in ACO admin]** - [!DNL Adobe Commerce Optimizer] Studioでカタログビューの詳細ページを開きます。
- **[!UICONTROL Copy ID]** – 参照のためにカタログ ビューIDをコピーします。

## 「ACO」タブで孤立 {#orphaned-in-aco-tab}

「**[!UICONTROL Orphaned in ACO]**」タブには、[!DNL Adobe Commerce Optimizer]に存在するが、対応する[!DNL Adobe Commerce] ソースを持たないカタログビューと制限付きアクセスキーが一覧表示されます。例えば、コネクタではなく[!DNL Adobe Commerce Optimizer] Studioで手動で作成されたエンティティが表示されます。 一致させる[!DNL Adobe Commerce] レコードがないため、これらのエンティティはメイングリッドに表示できません。

Adobe Commerce ソースを持たないエンティティを一覧表示するACO タブで![孤立しました](assets/catalog-view-sync-orphan.png){width="600" zoomable="yes"}

| フィールド | 説明 |
| --- | --- |
| **種類** | 孤立したエンティティのカテゴリ：[!UICONTROL Catalog View]または[!UICONTROL Access Key]。 |
| **ACO ID** | [!DNL Adobe Commerce Optimizer]のエンティティの識別子。 |
| **詳細** | エンティティに関する追加のコンテキスト（ポリシーなど）。 |
| **最初に見た** | 調整がこのエンティティを最初に検出したとき。 |
| **アクション** | エンティティ IDをコピーするには、**[!UICONTROL Copy ID]**&#x200B;を選択します。 コピーしたIDを使用して、[!DNL Adobe Commerce Optimizer] Studio カタログビューからエンティティを見つけて削除します。 |

>[!NOTE]
>
>このタブはレポート専用です。 紐付けでは、孤立したエンティティは削除されません。 不要になった場合は、[!DNL Adobe Commerce Optimizer] Studioで直接削除します。

## 削除済みタブ {#deleted-tab}

**[!UICONTROL Deleted]** タブには、共有カタログが[!DNL Adobe Commerce]で削除されたために削除されたカタログビューの予測が一覧表示されます。 共有カタログとそのカタログビューは存在しなくなったため、これらの行はどこにもリンクしません。 それらは削除されたものの記録としてのみ保持されます。

![共有カタログが削除された後に削除された、カタログビューの予測を一覧表示するタブを削除しました](assets/catalog-view-sync-deleted.png){width="600" zoomable="yes"}

| フィールド | 説明 |
| --- | --- |
| **カタログ ビュー** | 削除されたカタログビューの識別子。 |
| **Source** | 削除された共有カタログ。 |
| **ストアビュー** | 表されるカタログビューのストアビュー。 |
| **が**&#x200B;に削除されました | 突出部が削除されたとき。 |

このタブの行は、90日後に自動的に消去されます。

## 既知の制限事項

- [!DNL Adobe Commerce Optimizer] Studioには、コネクタで管理されたカタログ ビューと手動で作成されたカタログ ビューを区別する視覚的なインジケーターがありません。 コネクタが管理するものを決定するには、[!DNL Adobe Commerce Optimizer] Studio UIではなく、このページを使用します。
- **[!UICONTROL Orphaned in ACO]** タブの&#x200B;**[!UICONTROL ACO ID]**&#x200B;列は、一意の識別子ではなく、カタログ ビュー、ポリシー、またはアクセス キーを識別します。 列の命名は変更される可能性があります。

>[!MORELIKETHIS]
>
> - [&#x200B; カタログビュー設定の管理](/help/b2b/catalog-views-manage.md) – 共有カタログまたは会社アカウントからのカタログビューのレビュー
> - [&#x200B; データフィードの同期ステータス &#x200B;](data-feed-sync-status.md)
> - [&#x200B; サービス/ACO カタログ ビュー同期](../configuration-reference/services/aco-catalog-view-sync.md) – 削除と作成の猶予期間とドリフト調整を設定します
> - [制限付きアクセスキー管理](restricted-access-keys.md) – このページに有効期限が表示されるキーを管理します
> - *Adobe Commerce Optimizer コネクタ ガイド*&#x200B;の[B2B共有カタログのカタログ ビュー同期の監視](https://experienceleague.adobe.com/ja/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/catalog-view-sync-status)
> - [&#x200B; プライベートカタログビュー](https://experienceleague.adobe.com/ja/docs/commerce/optimizer/setup/private-catalog-view)
> - [制限付きアクセスキー](https://experienceleague.adobe.com/ja/docs/commerce/optimizer/setup/restricted-access-keys)
