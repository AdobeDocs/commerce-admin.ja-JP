---
title: Adobe Commerceの HIPAA 対応
description: Adobe Commerce HIPAA 対応モジュールを追加する方法、および HIPAA の義務を遵守するための追加の機能を取得する方法を説明します。
feature: Security, Compliance
hide: true
hidefromtoc: true
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# Adobe Commerceの HIPAA 対応

>[!IMPORTANT]
>
>**免責条項**<br/>
>この情報は、Adobeのお客様がAdobeの HIPAA 対応サービスに関する質問に答えるのに役立つように作成されています。 法的な助言とは言えません。 商人は、HIPAA に基づく義務と、Adobe製品の適切な使用と構成を理解するために、自社の法律顧問に相談する必要があります。

## 医療保険の移植性と責任に関する法律 (HIPAA)

HIPAA(Health Insurance Portability and Accountability Act) は、米国の主要な連邦医療プライバシー法で、米国保健福祉省 (HHS) によって施行されています。 HIPAA の適用対象： _対象エンティティ_ （医療機関、保険業者、清掃所など） _Business Associates_ （対象となるエンティティにサービスを提供する事業者など）。 HIPAA の要件は、プライバシールール、セキュリティルール、違反通知ルールの 3 つの異なるルールにまたがって設定されます。 Adobeは、特定の製品のビジネスアソシエートとして機能し、Adobeは「HIPAA 対応サービス」と分類します。 HIPAA に基づいて規制されるデータは、 _保護されたヘルス情報_ ファイだ。 PHI は、(1) 医療提供者、医療計画、医療清掃所が作成または受け取る医療情報のサブセットで、(2) 個人に対する医療の過去、現在、または将来の身体的・精神的健康状態、個人への医療の提供、過去、現在、将来の支払いに関する情報を使用して個人を特定できます。 HIPAA のプライバシーとセキュリティ規則では、被覆エンティティは、ビジネスアソシエート契約 (BAA) の形で、被覆エンティティの PHI のプライバシーとセキュリティを保護するために、ビジネスアソシエイトに書面で保証を受け取る必要があります。

## Adobe Commerce HIPAA 対応

Adobe Commerce HIPAA 対応には、マーチャントがそれぞれの HIPAA 義務に準拠できる機能が追加されています。 Adobe Commerce HIPAA 対応 (`magento/hipaa-ee`) モジュールをクラウドインフラストラクチャ上のAdobe Commerceに追加します。 また、HIPAA に準拠するには、無効にする必要がある機能もいくつかあります。

*これらの資料は、情報提供のみを目的としています。 この情報を提供しても、受信者に契約上の権利やその他の権利を付与する権利はありません。 情報の正確性を保証するための取り組みは行われていますが、正確かつ完全な情報を表現することはなく、Adobeは法やAdobeの製品が変更された場合に、この情報を更新する義務を負いません。 また、Adobeの書面による同意なしに、意図した受信者以外の当事者にこのドキュメントを配布することはできません。*

## 必要システム構成

Adobe Commerceの HIPAA 対応には、Adobe Commerceと同じシステム要件があり、さらに次の要件があります。

- Adobe Commerceバージョン 2.4.6-p3 以降（ベータ版以外）
- Adobe Commerce on cloud infrastructure またはAdobe Commerce on Managed Services
- の最新バージョン `magento/hipaa-ee` 拡張

## インストール

Adobeの HIPAA 対応サービスは、技術的にはコンポーザーのメタパッケージです `magento/hipaa-ee` には、特別なモジュールへのリンクが含まれています。 このメタパッケージはリポジトリ内に存在します [repo.magento.com](https://repo.magento.com).

1. インストール可能 `magento/hipaa-ee` metapackage、アクセス権が必要です。 キーの生成と必要な権限の取得については、 [認証キーの取得](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. パッケージをインストールする環境を確認し、一般的な [システム要件](#system-requirements).

1. メタパッケージを追加 `magento/hipaa-ee` をコンポーザー設定に追加します。

   最も簡単な方法は、コンポーザー CLI を使用することです。 例：

   ```shell
   composer require magento/hipaa-ee
   ```

1. Adobe Commerceがまだインストールされていない場合は、インストールを開始できます ( [インストール手順](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)) をクリックします。

   Adobe Commerceが既にインストールされている場合は、モジュールをダウンロードした後、を実行します。 `bin/magento setup:upgrade` コマンドを入力してから、推奨事項に従って操作します。

   ```shell
   bin/magento setup:upgrade
   ```

   このコマンドを実行すると、新しくダウンロードされたモジュールが有効になり、それらをインストールするスクリプトが起動します。 モジュール管理について詳しくは、 [モジュールの有効化または無効化](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. インストールまたは更新プロセスが完了したら、 `Hipaa*` 関連するモジュールが含まれています。

   次のコマンドを実行します。

   ```shell
   bin/magento module:status
   ```

   HIPAA コンポーザーパッケージが正しく追加された場合は、コマンドの出力に HIPAA モジュールが表示されます。 例：

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   <truncated for brevity>
   ```

   プレフィックスが付いたすべてのモジュール `Magento_Hipaa` は、「有効なモジュール」セクションにある必要があります。

## HIPAA 対応の機能強化

The `magento/hipaa-ee` パッケージでは、基本的な Commerce 製品に対する変更と機能強化がいくつか導入されています。 以下の節では、これらの変更点の詳細と、その基本製品の変更方法について説明します。

### アクションログ

監査ログは、HIPAA の要件です。 Adobe Commerceでは、 [アクションログ](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) の機能には、ストアで作業する管理者ユーザーによる変更がすべて記録されます。 監査ログに関する HIPAA 要件を満たすために、管理 UI および API 呼び出しを通じて実行されたすべての管理者ユーザーおよび顧客のアクションを記録する機能が変更されました。

#### アクションログレポート

The _アクションログ_ レポートグリッド (**[!UICONTROL System]** /アクションログ/レポート ) は、管理 UI および API を使用して実行された顧客のアクションに合わせて変更されます。

1. 次の 2 つの列が追加されます。
   - ***ソース***：アクションが実行された場所を表示します。\
     値： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***クライアントの種類***：クライアントタイプを表示します。\
     値：顧客 |管理者 |統合


2. 名前を変更 ***ユーザー名*** から ***クライアント識別子***
   - ***クライアント識別子***：アクションを実行したユーザーのログイン ID を表示します\
     値：
      - クライアントタイプが顧客の場合の電子メール
      - クライアントタイプが管理者の場合のユーザー名
      - クライアントタイプが統合の場合の名前

3. 名前を変更 ***フルアクション名*** から ***Target***
   - ***Target***：アクション名を表示します。\
     値：
      - ソースが REST API または SOAP API の場合はエンドポイント
      - GraphQL API の場合のクエリ名/ミューテーション名
      - 管理 UI または顧客 UI の場合のアクション名。

#### ログに対する管理者アクションの設定

すべてのアクションをデフォルトで記録する必要があるので、この機能は使用できません。

### インポート/エクスポート機能

読み込み/書き出し機能の機能強化は、管理エクスペリエンスの向上と、ユーザーアクションの可視性の向上に重点を置いています。

>[!NOTE]
>
>これら ***機能強化により、コアロジックの読み込み/書き出しが変更されない***&#x200B;の代わりに、機能を拡張して、より包括的なログ記録とデータ属性の改善を提供します。 インポート/エクスポートの基本機能は変わりません。 ユーザーは、中断することなく既存の機能とワークフローを引き続き使用できます。

#### 管理アクションのログ

読み込み/書き出し機能の主な改善点の 1 つは、管理アクションのログの機能強化です。 これにより、データの読み込み/書き出しに関連するアクティビティをさらに深く掘り下げ、トラッキングと監査性の向上に役立つ機能が導入されます。 以下のアクションがログに記録され、 **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**グリッド：

| タイプ | アクション |
| ---- | ------- |
| インポート | <ul><li>管理者ユーザーがインポートを実行します<li>管理者ユーザーがインポートされたファイルをダウンロードします<li>管理者ユーザーがエラーファイルをダウンロードします<ul/> |
| 書き出し | <ul><li>管理者ユーザーからのリクエスト<li>管理者ユーザーが書き出したファイルをダウンロードします<ul/> |
| 予定されているインポート/エクスポート | <ul><li>管理者ユーザーが書き出しのスケジュールを設定<li>管理者ユーザーがスケジュールされた書き出しを編集しました<li>管理者ユーザーがスケジュールされた書き出しを実行しました<li>管理者ユーザーがスケジュールされた書き出しを削除しました<li>管理者ユーザーがインポートのスケジュールを設定します<li>管理者ユーザーがスケジュール済みのインポートを編集しました<li>管理者ユーザーがスケジュールされたインポートを実行しました<li>管理者ユーザーがスケジュールされたインポートを削除しました<li>管理者ユーザーは、読み込み/書き出し操作の一括削除を実行します<ul/> |

### 表示の強化と改善されたフィルター/並べ替え

管理者ユーザーがより有益なグリッドを使用できるように、データの表示、フィルタリングおよび並べ替え機能がいくつか強化されました。

#### 履歴をインポート ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- 次を除くすべての列に対するフィルタリングを有効にしました： **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**、および **[!UICONTROL Summary]**.

#### 書き出し ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- 追加された **[!UICONTROL ID]** 列。
- が追加されました。 **[!UICONTROL Requested At]** 列 (_書き出しがリクエストされた日時_) をクリックします。
- が追加されました。 **[!UICONTROL User]** 列 (_リクエストを行った管理者のユーザー名_) をクリックします。
- 削除された **[!UICONTROL Action]** 列。
- を移動しました。 **[!UICONTROL Download]** リンク先： **[!UICONTROL File name]** 列 (_「履歴を読み込み」グリッドに類似_) をクリックします。
- 書き出されたファイルの削除を行うアクションを無効にしました (_追跡を改善する_) をクリックします。
- 以下を除くすべての列の並べ替えを有効にしました **[!UICONTROL File name]**.
- すべての列のフィルタリングを有効にしました。

#### 予定されているインポート/エクスポート ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- 追加された **[!UICONTROL ID]** 列。
- が追加されました。 **[!UICONTROL Scheduled At]** 列 (_インポートまたはエクスポートがスケジュールされた日時_) をクリックします。
- が追加されました。 **[!UICONTROL User]** 列 (_インポート/エクスポートをスケジュールした管理者ユーザーのユーザー名_) をクリックします。

## HIPAA 対応の無効化された機能

### SaaS サービス

Adobe Commerce向けに提供される SaaS サービスは、HIPAA 対応に基づくものではありません。 これには以下が含まれますが、これらに限定されません。

- ライブ検索
- API メッシュ
- App Builder
- カタログサービス

### デフォルトでゲストのチェックアウトを無効にしました

- ゲストチェックアウトは、HIPAA の様々な側面（ロギング、アクセス制御、PHI の衛生および系統など）に対する潜在的なリスクを提供します。
- ゲストのチェックアウトは、HIPAA 対応モジュールではデフォルトで無効になっていますが、マーチャント自身の責任で有効にすることができます。

### デフォルトでニュースレター機能を無効にしました

- ニュースレター機能は、マーケティングコンテキストで PHI が使用されないようにデフォルトで無効になっていますが、マーチャント自身が自ら有効にすることもできます。

### デフォルトで Advanced Reporting Service 設定を無効にしました

Advanced Reporting Service の設定は、PHI が分析やレポートに使用されないようにデフォルトで無効になっていますが、マーチャント自身が自ら有効にすることもできます。
