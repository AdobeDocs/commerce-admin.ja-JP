---
title: Adobe Commerceに対する HIPAA 対応
description: Adobe Commerce HIPAA 対応拡張機能を追加し、HIPAA 義務を準拠できる追加機能を取得する方法について説明します。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: afb6b4ca31675f6e549282749ef032ef1cd2f9f9
workflow-type: tm+mt
source-wordcount: '2391'
ht-degree: 1%

---

# Adobe Commerceに対する HIPAA 対応

{{ee-feature}}

>[!IMPORTANT]
>
>**免責事項**<br/>
>&#x200B;>この情報は、Adobeのお客様がAdobeの HIPAA 対応サービスに関する質問に答えるのを支援することを目的としています。 それは法的な助言にはならない。 マーチャントは、HIPAA の下での義務やAdobe製品の適切な使用と設定について理解するために、自社の法務担当者に相談する必要があります。

>[!BEGINSHADEBOX]

**HIPAA （Health Insurance Portability and Accountability Act：医療保険の相互運用性と説明責任に関する法律）**

HIPAA （Health Insurance Portability and Accountability Act：医療保険の携行性と責任に関する法律）は、米国では主要な連邦医療プライバシー法であり、米国保健福祉省（Department of Health and Human Services:HHS）によって施行されています。 HIPAA は、_対象事業者_ （医療機関、保険会社、クリアリングハウスなど）および _ビジネスアソシエイト_ （対象事業者にサービスを提供する事業者など）に適用されます。 HIPAA の要件は、「Privacy Rule」、「Security Rule」、「Breach Notification Rule」の 3 つの異なるルールで設定されます。 Adobeは、特定の製品のビジネスアソシエイトとして機能します。Adobeはこれを HIPAA 対応サービスに分類しています。 HIPAA で規制されるデータは、_保護された医療情報_ PHI と呼ばれます。 PHI とは、（1）医療提供者、健康計画若しくは医療情報交換所が作成または受領した健康情報、（2）個人の過去、現在または将来の心身の健康若しくは状態、個人への医療提供または個人への医療提供の過去、現在または将来の支払いに関する情報、（3）個人または個人を識別するために利用できると信ずるに足る合理的な根拠を特定する情報です。 HIPAA のプライバシーおよびセキュリティに関するルールでは、対象となるエンティティは、ビジネス・アソシエイトからビジネス・アソシエイト契約（BAA）の形式で書面による保証を取得し、ビジネス・アソシエイトが対象となるエンティティの PHI のプライバシーおよびセキュリティを保護するʼとを求めています。 詳しくは、Adobeのセキュリティセンターにある [HIPAA およびAdobe製品およびサービス &#x200B;](https://www.adobe.com/trust/compliance/hipaa-hds/hipaa-ready.html) を参照してください。

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA 対応

Adobe Commerce HIPAA 対応の拡張機能により、Adobe Commerceのインストールに機能が追加され、マーチャントが HIPAA の各義務に準拠できるようになりました。

Adobe Commerce HIPAA 対応の拡張機能は、クラウドインフラストラクチャー上のAdobe CommerceまたはAdobe Managed Services プロジェクトで利用で `magento/hipaa-ee` ます。 Adobe Commerce HIPAA 対応のインストールプロセスは、HIPAA の要件に準拠するために、一部のネイティブサービスと機能を無効にします。 [&#x200B; 無効にされたサービスと機能 &#x200B;](#disabled-services-and-features) を参照してください。

>[!NOTE]
>
>HIPAA 対応の機能へのアクセスは、Adobe Commerce用ヘルスケアアドオンを購入したマーチャントのみが利用できます。

*これらの資料は情報提供のみを目的としています。 この情報の提供は、受信者に契約上またはその他の権利を与えるものではありません。 また、提供日現在の情報の正確性については保証しておりますが、正確かつ完全なものであることを示すものではありません。 Adobeは、法令またはAdobeの商品の変更に伴い、この情報を更新する義務を負いません。 また、Adobeの書面による同意なく、対象者以外の者に配布してはなりません。*

## 必要システム構成

次の表に、Adobe Commerceのバージョンと HIPAA 対応の拡張機能の互換性を示します。

| Adobe Commerce | サポート | 備考 |
|----------------|-----------|-------|
| 2.4.7-p4 以降 | 1.2.0 | 2.4.7-p4 のサポートには、[&#x200B; ホットフィックス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-cloud-kcs/kbarticles/ka-27147) が必要です |
| 2.4.6-p9 - 2.4.6-p10 | 1.2.0 | |
| 2.4.6-p8 | 1.1.0 | [&#x200B; データサービス &#x200B;](#adobe-commerce-services) のサポートは、1.1.0 で導入されました |
| 2.4.6-p3 - 2.4.6-p7 | 1.0.0 | |

>[!IMPORTANT]
>
>- HIPAA 対応の拡張機能は、Cloud 上のAdobe CommerceまたはAdobe Commerce Managed Services プロジェクトでのみ使用できます。
>- 拡張機能は、`repo.magento.com` から Composer メタパッケージとして使用できます。
>- HIPAA に対応した機能にアクセスするには、Adobe Commerce用のヘルスケアアドオンが必要です。
>- Adobe Commerceのベータ版はサポートされていません。

## インストール

**前提条件**

>[!BEGINSHADEBOX]

- Adobeによって、HIPAA 対応拡張機能にアクセスするためのAdobe Commerce アカウントがプロビジョニングされました。
- [repo.magento.com](https://repo.magento.com) にアクセスして拡張機能をインストールします。 キーの生成と必要な権限の取得については、[&#x200B; 認証キーの取得 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) を参照してください。

>[!ENDSHADEBOX]

Adobe バージョン 2.4.7-p5 または 2.4.6-p3 から 2.4.6-p8 を実行しているインスタンスに、Adobe Commerceの最新バージョンの HIPAA 対応サービス拡張機能（`magento/hipaa-ee`）をインストールします。 拡張機能は、[repo.magento.com](https://repo.magento.com) リポジトリからコンポーザメタパッケージとして提供されます。 メタパッケージには、Adobe Commerce インスタンスに対して HIPAA 機能を有効にするモジュールのコレクションが含まれています。

>[!NOTE]
>
>Experience Platformに送信されるバックオフィスイベントデータが HIPAA に対応していることを確認するには、[Data Connection Extension ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension) を参照してください。

1. ローカルワークステーションで、Adobe Commerce on cloud infrastructure プロジェクトのプロジェクトディレクトリに移動します。

   >[!NOTE]
   >
   >Commerce Adobe Commerce プロジェクト環境のローカル管理について詳しくは、[&#x200B; クラウドインフラストラクチャユーザーガイドの &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/develop/cli-branches)CLI を使用したブランチの管理 _を参照してください_。

1. Adobe Commerce Cloud CLI を使用して、更新する環境ブランチをチェックアウトします。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Composer CLI を使用して、metapackage `magento/hipaa-ee` を composer 設定に追加します。

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. パッケージの依存関係を更新します。

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. 更新されたコードを追加、コミットおよびクラウド環境にプッシュします。

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   更新をプッシュすると、[Commerce クラウドデプロイメントプロセス &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/develop/deploy/process) が開始され、変更が適用されます。 [&#x200B; デプロイメントログ &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/develop/test/log-locations) からデプロイメントステータスを確認します。

### インストールの確認

アップデートがデプロイされたら、`Hipaa*` 拡張機能がインストールされていることを確認します

1. SSH を使用してリモートクラウド環境にログインします。

   ```shell
   magento-cloud ssh
   ```

1. コマンドラインから、Adobe Commerce CLI を使用して、モジュールのステータスを確認します。

   ```shell
   bin/magento module:status
   ```

1. HIPAA モジュールが有効なモジュールのリストに含まれていることを確認します。

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
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   プレフィックスが `Magento_Hipaa` のすべてのモジュールは、「有効なモジュール」セクションに配置する必要があります。

## HIPAA 対応の機能の強化

`magento/hipaa-ee` 拡張機能では、Commerceの基本製品にいくつかの変更と機能強化が導入されています。 次のセクションでは、これらの変更の詳細と、基本製品の変更方法について説明します。

### アクションログ

監査ログは HIPAA 要件の 1 つです。 Adobe Commerceでは、[&#x200B; アクションログ &#x200B;](../../systems/action-log.md) 機能は、ストアで作業している管理者ユーザーが行ったすべての変更を記録します。 監査ログの HIPAA 要件を満たすために、機能が更新され、管理 UI および API 呼び出しを使用して実行されたすべての管理ユーザーおよび顧客操作を記録するようになりました。

アクションログでは、Adobe サービスがストアデータにアクセスする際のイベントも取り込みます。 アクションログレポートの「外部に送信されたデータ」アクションをフィルタリングすることで、これらのイベントを識別できます。

#### アクションログレポート

_アクションログ_ レポートグリッド（**[!UICONTROL System]**/アクションログ/レポート）は、管理 UI および API を使用して実行された顧客のアクションに対応するように変更されます。

1. 次の 2 つの列を追加しました。
   - ***Source***：アクションが実行された場所を表示します。
値：`Admin UI` | `Customer UI` | `REST API` | `SOAP API` | `GraphQL API`
   - ***クライアントの種類***: クライアントの種類を表示します。
値：Customer |管理者 |統合

2. ***ユーザー名*** 列の名前を ***クライアント識別子*** に変更しました
   - ***クライアント識別子***：アクションを実行したユーザーのログイン ID を表示します。
値：
      - クライアントタイプが「顧客」の場合はメール
      - 「Client Type」が「Admin」の場合のユーザー名
      - 「クライアントタイプ」が「統合」の場合の名前

3. ***フルアクション名*** 列の名前を ***ターゲット*** に変更しました
   - ***ターゲット***：アクション名を表示します。
値：
      - Sourceが REST API またはSOAP API の場合のエンドポイント
      - GraphQL API の場合はクエリまたはミューテーション名
      - 管理 UI または顧客 UI の場合はアクション名。

#### ログ用の管理者アクションの設定

すべてのアクションがデフォルトで記録される必要があるので、この機能は使用できません。

### HIPAA 顧客検索結果制限

Adobe Commerceの HIPAA 顧客検索結果制限機能は、保護された医療情報（PHI）および個人を特定できる情報（PII）へのアクセスを制限することで、HIPAA 規制へのコンプライアンスを確保します。 この機能により、ユーザーの役割に基づいて顧客レコードを検索および表示する機能が制限され、許可されたユーザーのみがこの情報にアクセスできるようになります。

#### 主な機能

- **検索制限**：必要な役割を持たないユーザーは、顧客レコードを検索または表示できません。
- **アクセスの必須検索**:Adobe Commerceのデフォルトの動作とは異なり、検索を行わない限り顧客情報を表示することはできません。 これにより、ユーザーは自分の情報を見つけるために、顧客に関する特定の詳細を知る必要があります。
- **検索結果の制限**：条件に一致する検索結果は 10 件のレコードに制限され、一度に管理できる数のレコードのみが表示されます。
- **フィルターの最小数**：ユーザーは、検索を実行するために、少なくとも 3 つのフィルター（メール、姓、状態など）を適用し、検索が具体的でターゲット設定されるようにする必要があります。
- **フィルター通知**：検索制限が有効になると、検索結果を絞り込むためのフィルターを適用するようユーザーに通知されます。

#### 設定

検索結果の顧客数を制限する設定は、管理パネルの **[!UICONTROL Stores]**/**[!UICONTROL Configuration]**/**[!UICONTROL Advanced]**/**[!UICONTROL Admin]**/**[!UICONTROL Admin Grids]** にあります。 この設定は、`hipaa-ee` 拡張機能がインストールされる際にデフォルトで有効になります。

- **グリッドの顧客数を制限**：この設定を使用すると、グリッド検索結果に表示される顧客数の制限を有効または無効にできます。
- **顧客グリッド検索結果制限**：この設定では、グリッド検索結果に表示できる顧客レコードの最大数を指定します。

#### 影響を受けた機能領域

検索結果の制限機能は、管理者による注文の作成ページ（**[!UICONTROL Sales]**/**[!UICONTROL Orders]**/**[!UICONTROL Create New Order]**）と顧客ページ（**[!UICONTROL Customers]**/**[!UICONTROL All Customers]**）の顧客グリッドに適用されます。

- フィルターは、デフォルトで開きます。
- 検索を実行するには、少なくとも 3 つのフィルターを適用する必要があります。
- デフォルトでは、検索結果は 10 レコードに制限されています。
- 検索条件に一致するレコードが他にもある場合、通知は、結果の制限と検索を絞り込む必要があることをユーザーに通知します。
- グリッドのページネーションは使用できません。
- ページから移動する際、適用された以前の検索結果とフィルターが保存されません。

検索結果の制限機能は、顧客検索の REST API （`/V1/customers/search`）にも適用されます。

- フィルターが適用されていない場合、またはフィルターが不十分な場合、API は検索の実行に必要なフィルター数を示すエラーメッセージを返します。
- 十分なフィルターを適用する承認済みユーザーは、指定された制限内に API 結果を受け取ります。
- 結果に制限がある場合、検出されたレコードの合計数と適用された現在の制限を示すメッセージが応答に追加されます。

### 機能の読み込みと書き出し

読み込み機能と書き出し機能の強化は、管理エクスペリエンスの向上と、ユーザーのアクションの可視性の向上に重点を置いています。

>[!NOTE]
>
>これらの ***機能強化は、インポートとエクスポートのコアロジックを変更するものではありません***。むしろ、より包括的なログ記録と改善されたデータアトリビューションを提供するために機能を拡張するものです。 インポートとエクスポートの基本的な機能は変更されません。 ユーザーは、中断することなく既存の機能とワークフローを引き続き使用できます。

#### 管理アクションログ

読み込みおよび書き出し機能における主な改善点の 1 つは、管理アクションのログの機能強化です。 この機能強化により、データのインポートとエクスポートに関連するアクティビティをより深く掘り下げる機能が導入され、トラッキングと監査性の向上に貢献します。 以下のアクションがログに記録され、**[!UICONTROL System]/ _[!UICONTROL Action Logs]_/[!UICONTROL Report]**&#x200B;グリッドに反映されるようになりました。

| タイプ | アクション |
| ---- | ------- |
| インポート | <ul><li>管理者ユーザーがインポートを実行します<li>管理者ユーザーが読み込んだファイルをダウンロードします<li>管理者ユーザーがエラーファイルをダウンロードする<ul/> |
| Export | <ul><li>管理者ユーザーからのリクエスト<li>管理者ユーザーが、書き出されたファイルをダウンロードします<ul/> |
| スケジュールされた読み込み/書き出し | <ul><li>管理者ユーザーは書き出しをスケジュールします<li>管理者ユーザーがスケジュールされた書き出しを編集した<li>管理者ユーザーがスケジュールされた書き出しを実行する<li>管理者ユーザーがスケジュールされた書き出しを削除する<li>管理者ユーザーが読み込みのスケジュールを設定<li>管理者ユーザーがスケジュール済み読み込みを編集したとき<li>管理者ユーザーがスケジュールされた読み込みを実行<li>管理者ユーザーがスケジュールされた読み込みを削除<li>管理者ユーザーがインポート/エクスポート操作の一括削除を実行します<ul/> |

### ディスプレイの強化と、フィルタリングと並べ替えの改善

管理者ユーザーがより多くの情報を持つグリッドを使用できるように、HIPAA 対応サービスでは、データの表示、フィルタリング、並べ替えにいくつかの機能強化を提供しています。

#### インポート履歴（[!UICONTROL System]/_[!UICONTROL Data Transfer]_/[!UICONTROL Import History]）

- **[!UICONTROL Imported File]**、**[!UICONTROL Error File]**、**[!UICONTROL Execution Time]**、**[!UICONTROL Summary]** を除くすべての列に対してフィルターを有効にしました。

#### 書き出し（[!UICONTROL System]/_[!UICONTROL Data Transfer]_/[!UICONTROL Export]）

- **[!UICONTROL ID]** 列を追加しました。
- **[!UICONTROL Requested At]** 列（_書き出しがリクエストされた日時_）を追加しました。
- **[!UICONTROL User]** 列（_リクエストを行った管理者のユーザー名_）を追加しました。
- **[!UICONTROL Action]** 列を削除しました。
- **[!UICONTROL Download]** リンクを **[!UICONTROL File name]** 列に移動しました（_履歴の読み込みグリッド_）。
- 書き出されたファイルの削除を行うアクションを無効にしました（_トラッキングを改善するため_）。
- **[!UICONTROL File name]** 以外のすべての列の並べ替えが有効になりました。
- すべての列に対してフィルターを有効にしました。

#### スケジュールされたインポートおよびエクスポート（[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export]）

- **[!UICONTROL ID]** 列を追加しました。
- **[!UICONTROL Scheduled At]** 列（_読み込みまたは書き出しがスケジュールされた日時_）を追加しました。
- **[!UICONTROL User]** の列（_読み込みまたは書き出しをスケジュールした管理者ユーザーのユーザー名_）を追加しました。

## HIPAA 対応のサービスとツール

ここでは、Adobe Commerceの HIPAA 製品で使用できる HIPAA 対応のAdobe サービスについて説明します。 また、ストアの主要なセキュリティとコンプライアンス制御の監視に役立つツールについても説明します。

| サービス | 実稼動 | ステージング | staging_for_support | 開発 |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerceとヘルスケアアドオン | はい | はい | はい | 不可 |
| SendGrid | 不可 | 不可 | 不可 | 不可 |
| AWS Simple Email Service | はい | はい | はい | 不可 |

### Adobe Commerce サービス

次の表に、HIPAA 対応ソリューションで使用可能なAdobe Commerce サービスを示します。 これらのサービスには以下が含まれますが、これらに限定されません。

| サービス | 実稼動以外 | 実稼動 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/intro_and_overview/) | はい | はい |
| [Adobe Developer App Builderの API メッシュ &#x200B;](https://developer.adobe.com/graphql-mesh-gateway/) | はい | はい |
| [SaaS データのエクスポート &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/saas-data-export/overview) | はい | はい |
| [Live Search](https://experienceleague.adobe.com/ja/docs/commerce/live-search/overview) | 不可 | 不可 |
| [&#x200B; 製品の推奨事項 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/product-recommendations/overview) | 不可 | 不可 |
| [&#x200B; 資金決済 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/payment-services/guide-overview) | 不可 | 不可 |
| [&#x200B; データ接続バックオフィスイベント &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-backoffice) | はい | はい |
| [&#x200B; データ接続ストアフロントイベント &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#storefront-events) | 不可 | 不可 |
| [Audience Activation](https://experienceleague.adobe.com/ja/docs/commerce-admin/customers/audience-activation) | 不可 | 不可 |

### ツール

Adobe Commerceの [&#x200B; セキュリティスキャンツール &#x200B;](../../systems/security-scan.md) を使用すると、ストアを監視して、必要なすべてのセキュリティコントロールが有効で機能していることを確認できます。 Adobeでは、標準のセキュリティチェックに加えて、Adobe Commerceの HIPAA 製品を使用しているお客様に対して HIPAA 固有のチェックを表示するツールを強化しました。 セキュリティスキャンツールの HIPAA チェックは、次のことを保証するように設計されています。

- 監査モジュールは無効ではありません
- 2 要素認証（2FA）は無効ではありません
- マーケティング機能が無効になっています
- インストールされているすべての拡張機能が、定義済みの許可リストに一致します。
- サポートされていないAdobe サービスはインストールされていません

[&#x200B; ツールを設定 &#x200B;](../../systems/security-scan.md#run-a-security-scan) して、スケジュールされたスキャンの詳細を含むメール通知を送信したり、[&#x200B; レポートを手動で表示 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/launch/overview) したりできます。

## 無効にされた機能

HIPAA の要件に準拠するために、Adobe Commerceでサポートされている一部の機能は、デフォルトでは使用できないか無効になっています。 マーチャントは、これらの機能を自分の責任で再度有効化または使用するオプションがあります。

次の機能は、HIPAA 対応モジュールでデフォルトで無効になっています。 マーチャントは、独自の責任でこれらの機能のいずれかを有効にすることができます。

- **[トランザクションメール &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/project/sendgrid)** - サービスが HIPAA に対応していないので、SendGrid はデフォルトで無効になっています。 Adobe Commerceには、独自の [AWS Simple Email Service](https://docs.aws.amazon.com/ses/) アカウントで使用できる統合オプションが用意されています。 設定について詳しくは、カスタマーテクニカルアカウントマネージャーまたはAdobe Commerce サポートにお問い合わせください。

- **[ゲストのチェックアウト](../../stores-purchase/checkout-guest.md)** – この機能は、ログ、アクセス制御、PHI 衛生と系統など、HIPAA の様々な側面で発生する可能性のあるリスクであり、さらに多くの可能性があります。

- **[ニュースレター機能](../../merchandising-promotions/newsletters.md)** – この機能は、マーケティングコンテキストで PHI が使用されないようにするために無効になっています。

- **[Advanced Reporting service setting](../../getting-started/business-intelligence.md)**：この構成設定は、PHI が分析およびレポートに使用されるのを防ぐために無効になっています。
