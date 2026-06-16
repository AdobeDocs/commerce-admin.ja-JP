---
title: ADOBE COMMERCEでのHIPAAへの対応
description: Adobe Commerce HIPAA 対応拡張機能を追加し、HIPAA 義務を準拠できる追加機能を取得する方法について説明します。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/0K0f6Rb5ukFbiCj4ySxhl-4-OzJ4Luu2nKwhTHGeYW8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 2567
ht-degree: 1%

---

# ADOBE COMMERCEでのHIPAAへの対応

{{ee-feature}}

>[!IMPORTANT]
>
>**法的免責事項**<br/>
>この情報は、Adobeのお客様がAdobeのHIPAA対応サービスに関する質問に答えるのに役立つことを目的としています。これは法的な助言ではない。顧客は、自社の弁護士と相談して、HIPAA上の義務や、Adobe製品の適切な使用と構成について把握する必要があります。

>[!BEGINSHADEBOX]

**健康保険の相互運用性と説明責任に関する法律（HIPAA）**

健康保険の相互運用性と説明責任に関する法律（HIPAA）は、米国における主要な連邦医療プライバシー法であり、米国保健福祉省（HHS）によって施行されています。 HIPAAは、_対象事業者_ （医療提供者、保険会社、清掃会社など）および&#x200B;_ビジネスアソシエイト_ （対象事業者にサービスを提供する事業者など）に適用されます。 HIPAAの要件は、プライバシールール、セキュリティルール、侵害通知ルールの3つのルールで設定されます。 Adobeは、Adobeが「HIPAA対応サービス」に分類する特定の製品のビジネスアソシエイトとして機能します。 HIPAAで規制されるデータは、_保護された健康情報_&#x200B;またはPHIと呼ばれます。 PHIとは、（1）医療提供者、医療計画又はヘルスケアクリアリングハウスによって作成され又は受領される健康情報のサブセットであり、（2）個人の過去、現在、又は将来の身体又は精神状態、個人への医療の提供、又は個人への医療提供のための過去、現在、又は将来の支払いに関連し、（3）当該情報が個人を特定するために使用できると信じる合理的な根拠がある。 HIPAAのプライバシーとセキュリティ規則は、対象事業者がビジネスアソシエイト契約、またはBAAの形でビジネスアソシエイトから書面による保証を得ることを要求しており、ビジネスアソシエイトは対象事業者のPHIのプライバシーとセキュリティを保護する必要があります。 詳しくは、Adobe Trust Centerの[HIPAAおよびAdobeの製品とサービス &#x200B;](https://www.adobe.com/trust/compliance/hipaa-hds/hipaa-ready.html)を参照してください。

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA対応

Adobe Commerce HIPAA対応の拡張機能では、Adobe Commerceのインストールに追加の機能や機能が追加され、各販売者がそれぞれのHIPAA要件に準拠できるようになりました。

Adobe Commerce HIPAA対応の拡張機能`magento/hipaa-ee`は、Adobe Commerce オンクラウドインフラストラクチャまたはAdobe Managed Services プロジェクトで使用できます。 Adobe CommerceのHIPAA対応インストールプロセスでは、HIPAA要件に準拠するために、一部のネイティブサービスと機能が無効になります。 [無効なサービスと機能](#disabled-services-and-features)を参照してください。

>[!NOTE]
>
>HIPAA対応の機能にアクセスできるのは、Adobe Commerce用ヘルスケアアドオンを購入したマーチャントのみです。

*これらの資料は、情報提供のみを目的としています。 この情報の提供は、受信者に契約上またはその他の権利を与えるものではありません。 情報の提供日現在における正確性の確保に努めておりますが、当該情報が正確かつ完全であることを示すものではありません。 Adobeは、法律またはAdobe製品の変更に伴い、この情報を更新する義務を負いません。 また、この文書は、Adobeからの書面による同意なしに、意図した受領者以外の当事者に配布することはできません。*

## 必要システム構成

次の表は、Adobe CommerceのバージョンとHIPAA対応の拡張機能の互換性を示しています。

| Adobe Commerce | サポート対象 | メモ |
|----------------|-----------|-------|
| 2.4.8-p5 | 1.3.0 | 2.4.8-p5のサポートには[互換性パッチ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-cloud-kcs/kbarticles/ka-30555)が必要です |
| 2.4.7-p4以降 – p バージョン | 1.2.0 | 2.4.7-p4のサポートには[互換性パッチ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-cloud-kcs/kbarticles/ka-27147)が必要です |
| 2.4.6-p9 - 2.4.6-p10 | 1.2.0 | |
| 2.4.6-p8 | 1.1.0 | [data services](#adobe-commerce-services)のサポートは1.1.0で導入されました |
| 2.4.6-p3 - 2.4.6-p7 | 1.0.0 | |

>[!IMPORTANT]
>
>- HIPAA対応の拡張機能は、Adobe Commerce on CloudまたはAdobe Commerce Managed Services プロジェクトでのみ使用できます。
>- 拡張機能は、`repo.magento.com`からコンポーザーのメタパッケージとして利用できます。
>- HIPAA対応の機能を利用するには、Adobe Commerceのヘルスケアアドオンが必要です。
>- Adobe Commerceのベータ版はサポートされていません。

## インストール

**前提条件**

>[!BEGINSHADEBOX]

- Adobeは、HIPAA Ready拡張機能にアクセスするためにAdobe Commerce アカウントをプロビジョニングしました。
- 拡張機能をインストールするには、[repo.magento.com](https://repo.magento.com)にアクセスしてください。 キーの生成と必要な権限の取得については、[認証キーの取得](https://experienceleague.adobe.com/ja/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)を参照してください。

>[!ENDSHADEBOX]

サポートされているAdobe バージョンを実行しているインスタンスに、最新バージョンのAdobe Commerce HIPAA-Ready Services拡張機能（`magento/hipaa-ee`）をインストールします（[必要システム構成](#system-requirements)を参照）。 拡張機能は、[repo.magento.com](https://repo.magento.com) リポジトリからコンポーザーのメタパッケージとして配信されます。 メタパッケージには、Adobe Commerce インスタンスのHIPAA機能を有効にするモジュールのコレクションが含まれています。

>[!NOTE]
>
>Experience Platformに送信されるバックオフィスイベントデータがHIPAA対応であることを確認するには、[Data Connection拡張機能ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension)を参照してください。

1. ローカルワークステーションで、Adobe Commerce on cloud infrastructure プロジェクトのプロジェクトディレクトリに移動します。

   >[!NOTE]
   >
   >Commerce プロジェクト環境のローカル管理について詳しくは、_Adobe Commerce on Cloud Infrastructure ユーザーガイド_&#x200B;の「[CLIを使用した分岐の管理](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/develop/cli-branches)」を参照してください。

1. Adobe Commerce Cloud CLIを使用して更新する環境ブランチをチェックアウトします。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. コンポーザーCLIを使用して、メタパッケージ `magento/hipaa-ee`をコンポーザー設定に追加します。

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. パッケージの依存関係を更新します。

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. 更新されたコードを追加し、コミットして、クラウド環境にプッシュします。

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   更新をプッシュすると、[Commerce クラウド デプロイメント プロセス &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/develop/deploy/process)が開始され、変更が適用されます。 [&#x200B; デプロイ ログ &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/develop/test/log-locations)のデプロイメント ステータスを確認します。

### インストールを確認

更新をデプロイしたら、`Hipaa*`拡張機能がインストールされていることを確認します

1. SSHを使用してリモートクラウド環境にログインします。

   ```shell
   magento-cloud ssh
   ```

1. コマンドラインから、Adobe Commerce CLIを使用してモジュールのステータスを確認します。

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

   `Magento_Hipaa`でプレフィックスが付けられたすべてのモジュールは、「有効なモジュール」セクションに含まれている必要があります。

## HIPAA対応の機能強化

`magento/hipaa-ee`拡張機能では、ベースとなるCommerce製品に変更と機能強化が加えられています。 以下の節では、これらの変更の詳細と、ベース製品の変更方法について説明します。

### アクションログ

監査ログはHIPAA要件です。 Adobe Commerceでは、[&#x200B; アクションログ &#x200B;](../../systems/action-log.md)機能は、ストアで作業する管理者ユーザーが行ったすべての変更を記録します。 監査ログのHIPAA要件を満たすために、この機能が更新され、Admin UIおよびAPI呼び出しを通じて実行されたすべてのAdmin ユーザーおよび顧客アクションが記録されるようになりました。

また、アクションログは、Adobe サービスがストアデータにアクセスした際のイベントも記録します。 アクションログレポートの「外部に送信されたデータ」アクションをフィルタリングすることで、これらのイベントを特定できます。

#### アクションログレポート

_アクションログ_ レポートグリッド （**[!UICONTROL System]** > アクションログ > レポート）は、管理UIとAPIを通じて実行された顧客アクションに対応するように変更されます。

1. 2つの列を追加しました：
   - ***Source***: アクションが実行された場所を表示します。
値：`Admin UI` | `Customer UI` | `REST API` | `SOAP API` | `GraphQL API`
   - ***クライアントの種類***: クライアントの種類を表示します。
値：顧客|管理者|統合

2. ***ユーザー名***&#x200B;列の名前を&#x200B;***クライアント識別子***&#x200B;に変更しました
   - ***クライアント識別子***: アクションを実行したユーザーのログイン IDを表示します。
値：
      - クライアントタイプが「顧客」の場合は電子メール
      - クライアントタイプがAdminの場合のユーザー名
      - クライアントタイプが統合の場合は名前

3. ***フルアクション名***&#x200B;列の名前を&#x200B;***ターゲット***&#x200B;に変更しました
   - ***ターゲット***: アクション名を表示します。
値：
      - SourceがREST APIまたはSOAP APIである場合のエンドポイント
      - GraphQL APIの場合、クエリまたは変数名
      - 管理者UIまたは顧客UIの場合は、アクション名。

#### ログ記録のための管理者アクションの設定

すべてのアクションをデフォルトで記録する必要があるため、この機能は使用できません。

### HIPAA顧客検索結果の制限

Adobe CommerceのHIPAA顧客検索結果制限機能は、保護された医療情報（PHI）および個人情報（PII）へのアクセスを制限することで、HIPAA規制への準拠を保証します。 この機能は、ユーザーの役割に基づいて顧客レコードを検索および表示する機能を制限し、承認済みのユーザーのみがこの情報にアクセスできるようにします。

#### 主な機能

- **検索制限**：必要な役割を持たないユーザーは、顧客レコードを検索または表示できません。
- **アクセスの必須検索**: Adobe Commerceのデフォルトの動作とは異なり、検索を実行せずに顧客情報を確認することはできません。 これにより、利用者は、顧客に関する具体的な詳細を把握して、情報を見つける必要があります。
- **制限付き検索結果**：条件に一致する検索結果は10件に制限され、一度に管理可能な数のレコードのみが表示されます。
- **フィルターの最小数**：検索を実行するには、ユーザーが少なくとも3つのフィルター（電子メール、姓、状態など）を適用し、検索が具体的でターゲットを絞ったものである必要があります。
- **フィルター通知**：検索制限が有効になっている場合、フィルターを適用して検索結果を絞り込むようにユーザーに通知されます。

#### 設定

検索結果の顧客数を制限するための設定は、**[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**&#x200B;の下の管理パネルにあります。 この設定は、`hipaa-ee`拡張機能がインストールされている場合、デフォルトで有効になります。

- **グリッド内の顧客数の制限**：この設定を使用すると、グリッド検索結果に表示される顧客数の制限を有効または無効にできます。
- **顧客グリッド検索結果の制限**：この設定は、グリッド検索結果に表示できる顧客レコードの最大数を指定します。

#### 影響を受ける機能領域

検索結果制限機能は、管理者注文作成ページ （**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**）および顧客ページ （**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**）の顧客グリッドに適用されます。

- フィルターはデフォルトで開きます。
- ユーザーが検索を実行するには、最低3つのフィルターを適用する必要があります。
- 検索結果は、デフォルトで10件に制限されています。
- 検索条件に一致するレコードが他にも存在する場合、結果制限と検索を絞り込む必要性について通知がユーザーに通知されます。
- グリッドのページネーションは使用できません。
- ページから移動しても、以前に適用した検索結果とフィルターは保存されません。

検索結果制限機能は、顧客検索用REST API （`/V1/customers/search`）にも適用されます。

- フィルターが適用されていないか、フィルターが不十分な場合、APIは、検索を実行するために必要な数のフィルターが必要であることを示すエラーメッセージを返します。
- 十分なフィルターを適用する許可されたユーザーは、指定された制限内でAPI結果を受け取ります。
- 結果が制限されると、見つかったレコードの合計数と現在の適用制限を示すメッセージが応答に追加されます。

### 機能の読み込みと書き出し

読み込み機能と書き出し機能の機能強化は、管理者体験を向上させ、ユーザーのアクションをより詳細に可視化することに重点を置いています。

>[!NOTE]
>
>これらの&#x200B;***の機能強化は、インポートとエクスポートのコアロジック***&#x200B;を変更するものではなく、より包括的なログと改善されたデータアトリビューションを提供する機能を拡張します。 インポートとエクスポートの基本的な機能は変更されません。 ユーザーは、既存の機能やワークフローを中断することなく引き続き使用できます。

#### 管理アクションログ

読み込み機能と書き出し機能の主な改善点の1つは、管理操作のログの強化です。 この機能強化により、データの読み込みと書き出しに関連するアクティビティをより深く掘り下げる機能が導入され、追跡と監査可能性の向上に貢献します。 次のアクションがログに記録され、**[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**&#x200B;グリッドに反映されるようになりました。

| タイプ | アクション |
| ---- | ------- |
| インポート | <ul><li>管理者ユーザーがインポートを実行します<li>管理者ユーザーがインポートしたファイルをダウンロードします<li>管理者ユーザーがエラーファイルをダウンロードします<ul/> |
| 書き出し | <ul><li>管理者ユーザーのリクエスト<li>管理者ユーザーが書き出したファイルをダウンロードする<ul/> |
| 定期インポート/エクスポート | <ul><li>管理者ユーザーが書き出しをスケジュールします<li>管理者ユーザーは、スケジュールされた書き出しを編集します<li>管理者ユーザーは、スケジュールされた書き出しを実行します<li>管理者ユーザーは、スケジュールされた書き出しを削除します<li>管理者ユーザーがインポートをスケジュールします<li>管理者ユーザーは、スケジュールされた読み込みを編集します<li>管理者ユーザーは、スケジュールされたインポートを実行します<li>管理者ユーザーは、スケジュールされたインポートを削除します<li>管理者ユーザーは、インポート/エクスポート操作の一括削除を実行します<ul/> |

### 表示の機能強化とフィルターと並べ替えの改善

より有益なグリッドを管理者ユーザーに提供するために、HIPAA対応サービスには、データの表示、フィルタリング、並べ替えをおこなうための拡張機能がいくつか用意されています。

#### インポート履歴（[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History]）

- **[!UICONTROL Imported File]**、**[!UICONTROL Error File]**、**[!UICONTROL Execution Time]**、**[!UICONTROL Summary]**&#x200B;を除くすべての列に対してフィルタリングを有効にしました。

#### 書き出し（[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export]）

- **[!UICONTROL ID]**&#x200B;列を追加しました。
- **[!UICONTROL Requested At]**&#x200B;列（_書き出しがリクエストされた日時_）を追加しました。
- **[!UICONTROL User]**&#x200B;列（_リクエストを行った管理者のユーザー名_）を追加しました。
- **[!UICONTROL Action]**&#x200B;列を削除しました。
- **[!UICONTROL Download]** リンクを&#x200B;**[!UICONTROL File name]**&#x200B;列（_読み込み履歴グリッド_&#x200B;など）に移動しました。
- 書き出されたファイルを削除する操作を無効にしました（_トラッキングを改善するため_）。
- **[!UICONTROL File name]**&#x200B;を除くすべての列の並べ替えを有効にしました。
- すべての列に対してフィルターを有効にしました。

#### スケジュールされたインポートとエクスポート （[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export]）

- **[!UICONTROL ID]**&#x200B;列を追加しました。
- **[!UICONTROL Scheduled At]**&#x200B;列（インポートまたはエクスポートがスケジュールされた&#x200B;_日時_）を追加しました。
- **[!UICONTROL User]**&#x200B;列（インポートまたはエクスポートをスケジュールした管理者ユーザーの&#x200B;_ユーザー名_）を追加しました。

## HIPAA対応のサービスとツール

この節では、Adobe CommerceのHIPAA機能で使用できるHIPAA対応Adobe サービスについて説明します。 また、ストアの主要なセキュリティとコンプライアンスの制御を監視するために使用できるツールについても説明します。

| サービス | 本番 | ステージング | staging_for_support | 開発 |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce with Healthcare Add-on | はい | はい | はい | いいえ |
| SendGrid | いいえ | いいえ | いいえ | いいえ |
| AWS Simple Email Service | はい | はい | はい | いいえ |

### Adobe Commerce Services

次の表は、HIPAA対応ソリューションで使用できるAdobe Commerce サービスを示しています。 これらのサービスには、以下が含まれますが、これらに限定されません。

| サービス | 実稼動以外 | 本番 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/intro_and_overview/) | はい | はい |
| Adobe Developer App Builder[&#128279;](https://developer.adobe.com/graphql-mesh-gateway/)のAPI メッシュ | はい | はい |
| [SaaS データ書き出し](https://experienceleague.adobe.com/ja/docs/commerce/saas-data-export/overview) | はい | はい |
| [&#x200B; ライブサーチ &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/live-search/overview) | いいえ | いいえ |
| [商品レコメンデーション &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/overview) | いいえ | いいえ |
| [決済サービス &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/payment-services/guide-overview) | いいえ | いいえ |
| [&#x200B; データ接続バックオフィスイベント &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice) | はい | はい |
| [&#x200B; データ接続ストアフロント イベント &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#storefront-events) | いいえ | いいえ |
| [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | いいえ | いいえ |

### ツール

Adobe Commerceの[&#x200B; セキュリティスキャンツール &#x200B;](../../systems/security-scan.md)を使用すると、ストアを監視して、必要なすべてのセキュリティコントロールが有効で運用可能であることを確認できます。 Adobeでは、標準のセキュリティチェックに加えて、Adobe Commerce向けのHIPAA機能を使用するお客様に対して、HIPAA固有のチェックを表示するツールを強化しました。 セキュリティスキャンツールのHIPAA チェックは、次のことを確実に行えるように設計されています。

- 監査モジュールが無効になっていません
- 二段階認証（2FA）は無効になっていません
- マーケティング機能が無効です
- インストールされているすべての拡張機能が、定義済みの拡張機能許可リストと一致する
- サポートされていないAdobe サービスはインストールされていません

スケジュール済みのスキャンの詳細を含むメール通知を送信したり、[&#x200B; レポートを手動で表示したりするために、ツール &#x200B;](../../systems/security-scan.md#run-a-security-scan)を[設定できます](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/launch/overview)。

## 無効な機能

HIPAA要件に準拠するため、Adobe Commerceでサポートされている一部の機能は、デフォルトでは使用できないか無効になっています。 加盟店は、独自のリスクで、これらの機能を再度有効にするか、使用するオプションを有します。

HIPAA-readiness モジュールでは、次の機能がデフォルトで無効になっています。 顧客は独自のリスクで、これらの機能のいずれかを有効にすることができます。

- **[トランザクションメール &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-on-cloud/user-guide/project/sendgrid)** - サービスがHIPAA対応ではないため、SendGridはデフォルトで無効になっています。 Adobe Commerceには、独自の[AWS Simple Email Service](https://docs.aws.amazon.com/ses/) アカウントで使用できる統合オプションが用意されています。 設定の詳細については、カスタマーテクニカルアカウントマネージャーまたはAdobe Commerce サポートにお問い合わせください。

- **[ゲストチェックアウト](../../stores-purchase/checkout-guest.md)** – この機能は、ログ、アクセス制御、PHIのハイジーンとリネージ、その他の可能性を含む、HIPAAのさまざまな側面に対する潜在的なリスクを示します。

- **[ニュースレター機能](../../merchandising-promotions/newsletters.md)** – この機能は、マーケティングコンテキストでPHIが使用されないようにするために無効になっています。

- **[高度なレポートサービス設定](../../getting-started/business-intelligence.md)** – この設定設定は、分析とレポートにPHIを使用できないように無効になっています。
