---
title: Adobe Commerceに対する HIPAA 対応
description: Adobe Commerce HIPAA 対応の拡張機能を追加し、HIPAA の義務に準拠できるその他の機能を取得する方法について説明します。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: b7ce092f843992b1e4d0ca23981c70d854ded5f9
workflow-type: tm+mt
source-wordcount: '1570'
ht-degree: 0%

---

# Adobe Commerceに対する HIPAA 対応

>[!IMPORTANT]
>
>**免責事項**<br/>
>この情報は、Adobeのお客様がAdobeの HIPAA 対応サービスに関する質問に答えるのに役立ちます。 それは法的な助言にはならない。 マーチャントは、HIPAA の下での義務やAdobeの商品の適切な使用と設定を理解するために、自社の法務担当者に相談する必要があります。

>[!BEGINSHADEBOX]

**HIPAA （Health Insurance Portability and Accountability Act：医療保険の相互運用性と説明責任に関する法律）**

HIPAA （Health Insurance Portability and Accountability Act：医療保険の携行性と責任に関する法律）は、米国では主要な連邦医療プライバシー法であり、米国保健福祉省（Department of Health and Human Services:HHS）によって施行されています。 HIPAA の適用先 _対象エンティティ_ （医療機関、保険会社、クリアリングハウスなど） _ビジネス・アソシエイツ_ （対象事業者に対してサービスを提供する事業者など） HIPAA の要件は、「Privacy Rule」、「Security Rule」、「Breach Notification Rule」の 3 つの異なるルールで設定されます。 Adobeは、特定の製品（Adobeが「HIPAA 対応サービス」に分類する）のビジネスアソシエイトとして機能します。 HIPAA で規制されるデータは次のとおりです _保護された医療情報_ または PHI。 PHI とは、（1）医療提供者、健康計画若しくは医療情報交換所が作成または受領した健康情報、（2）個人の過去、現在または将来の心身の健康若しくは状態、個人への医療提供または個人への医療提供の過去、現在または将来の支払いに関する情報、（3）個人または個人を識別するために利用できると信ずるに足る合理的な根拠を特定する情報です。 HIPAA のプライバシーおよびセキュリティに関するルールでは、対象となるエンティティは、ビジネス・アソシエイトからビジネス・アソシエイト契約（BAA）の形式で書面による保証を取得し、ビジネス・アソシエイトが対象となるエンティティの PHI のプライバシーおよびセキュリティを保護するʼとを求めています。 詳しくは、を参照してください [HIPAA およびAdobe製品とサービス](https://www.adobe.com/trust/compliance/hipaa-ready.html) Adobeトラストセンターで。

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA 対応

Adobe Commerce HIPAA 対応の拡張機能により、Adobe Commerceのインストールに機能が追加され、マーチャントが HIPAA の各義務に準拠できるようになりました。

Adobe Commerce HIPAA 対応の拡張機能 `magento/hipaa-ee` は、クラウドインフラストラクチャー上のAdobe CommerceまたはAdobe Managed Services プロジェクトで使用できます。 Adobe Commerce HIPAA 対応のインストールプロセスは、HIPAA の要件に準拠するために、一部のネイティブサービスと機能を無効にします。 参照： [無効にされたサービスと機能](#disabled-services-and-features).

>[!NOTE]
>
>HIPAA 対応の機能へのアクセスは、Adobe Commerce用ヘルスケアアドオンを購入したマーチャントのみが利用できます。

*これらの資料は情報提供のみを目的としています。 この情報の提供は、受信者に契約上またはその他の権利を与えるものではありません。 また、提供日現在の情報の正確性については保証しておりますが、正確かつ完全なものであることを示すものではありません。 Adobeは、法令またはAdobeの商品の変更に伴い、この情報を更新する義務を負いません。 また、Adobeの書面による同意なく、対象者以外の者に配布することはできません。*

## 必要システム構成

Adobe Commerceは、クラウドインフラストラクチャのAdobe Commerce、またはバージョン 2.4.6-p3 以降（ベータ版なし）のAdobe Commerce Managed Servicesにデプロイする必要があります。

## インストール

**前提条件**

>[!BEGINSHADEBOX]

- Adobeは、HIPAA 対応拡張機能にアクセスするためのAdobe Commerce アカウントをプロビジョニングしました。
- アクセス先 [repo.magento.com](https://repo.magento.com) をクリックして拡張機能をインストールします。 キーの生成と必要な権限の取得については、を参照してください。 [認証キーの取得](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

Adobeの HIPAA 対応サービス拡張機能の最新バージョンをインストールします（`magento/hipaa-ee`Adobe Commerce）を選択する必要があります。 拡張機能は、からコンポーザメタパッケージとして提供されます。 [repo.magento.com](https://repo.magento.com) リポジトリ。 メタパッケージには、Adobe Commerce インスタンスに対して HIPAA 機能を有効にするモジュールのコレクションが含まれています。

1. ローカルワークステーションで、Adobe Commerce on cloud infrastructure プロジェクトのプロジェクトディレクトリに移動します。

   >[!NOTE]
   >
   >Commerce プロジェクト環境のローカル管理については、を参照してください。  [CLI によるブランチの管理](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) が含まれる _Adobe Commerce on Cloud Infrastructure ユーザーガイド_.

1. Adobe Commerce Cloud CLI を使用して、更新する環境ブランチをチェックアウトします。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. メタパッケージを追加 `magento/hipaa-ee` composer CLI を使用して composer を設定します。

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

   更新をプッシュすると、が開始されます [Commerce cloud のデプロイメントプロセス](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) 変更を適用します。 からデプロイメントステータスを確認します。 [ログをデプロイ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### インストールの確認

アップデートをデプロイした後、 `Hipaa*` 拡張機能がインストールされました

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
   <truncated for brevity>
   ```

   プレフィックスが付いたすべてのモジュール `Magento_Hipaa` 有効なモジュールセクションに配置する必要があります。

## HIPAA 対応の機能の強化

この `magento/hipaa-ee` 拡張機能では、基本Commerce製品に変更と機能強化がいくつか導入されています。 次のセクションでは、これらの変更の詳細と、基本製品の変更方法について説明します。

### アクションログ

監査ログは HIPAA 要件の 1 つです。 Adobe Commerceでは、 [アクションログ](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 機能は、ストアで作業する管理者ユーザーが行ったすべての変更を記録します。 監査ログの HIPAA 要件を満たすために、機能が更新され、管理 UI および API 呼び出しを使用して実行されたすべての管理ユーザーおよび顧客操作を記録するようになりました。

#### アクションログレポート

この _アクションログ_ レポートグリッド （**[!UICONTROL System]** / アクションログ / レポート）が変更され、管理 UI および API を使用して実行されたお客様のアクションに対応するようになりました。

1. 次の 2 つの列を追加しました。
   - ***ソース***：アクションが実行された場所を表示します。
値： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***クライアントタイプ***：クライアントタイプが表示されます。
値：Customer |管理者 |統合

2. の名前を変更 ***ユーザー名*** ～に列を成す ***クライアント識別子***
   - ***クライアント識別子***：アクションを実行したユーザーのログイン ID が表示されます。
値：
      - クライアントタイプが「顧客」の場合はメール
      - 「Client Type」が「Admin」の場合のユーザー名
      - 「クライアントタイプ」が「統合」の場合の名前

3. の名前を変更 ***完全なアクション名*** 列を ***ターゲット***
   - ***ターゲット***：アクション名を表示します。
値：
      - ソースが REST API または SOAP API の場合のエンドポイント
      - GraphQL API の場合はクエリまたはミューテーション名
      - 管理 UI または顧客 UI の場合はアクション名。

#### ログ用の管理者アクションの設定

すべてのアクションがデフォルトで記録される必要があるので、この機能は使用できません。

### 機能の読み込みと書き出し

読み込み機能と書き出し機能の強化は、管理エクスペリエンスの向上と、ユーザーのアクションの可視性の向上に重点を置いています。

>[!NOTE]
>
>これら ***機能強化によってインポートおよびエクスポートのコアロジックが変更されることはありません***&#x200B;代わりに、機能を拡張して、より包括的なログと改善されたデータアトリビューションを提供します。 インポートとエクスポートの基本的な機能は変更されません。 ユーザーは、中断することなく既存の機能とワークフローを引き続き使用できます。

#### 管理アクションログ

読み込みおよび書き出し機能における主な改善点の 1 つは、管理アクションのログの機能強化です。 この機能強化により、データのインポートとエクスポートに関連するアクティビティをより深く掘り下げる機能が導入され、トラッキングと監査性の向上に貢献します。 以下のアクションがログに記録され、 **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**グリッド：

| タイプ | アクション |
| ---- | ------- |
| インポート | <ul><li>管理者ユーザーがインポートを実行します<li>管理者ユーザーが読み込んだファイルをダウンロードします<li>管理者ユーザーがエラーファイルをダウンロードする<ul/> |
| Export | <ul><li>管理者ユーザーからのリクエスト<li>管理者ユーザーが、書き出されたファイルをダウンロードします<ul/> |
| スケジュールされた読み込み/書き出し | <ul><li>管理者ユーザーは書き出しをスケジュールします<li>管理者ユーザーがスケジュールされた書き出しを編集した<li>管理者ユーザーがスケジュールされた書き出しを実行する<li>管理者ユーザーがスケジュールされた書き出しを削除する<li>管理者ユーザーが読み込みのスケジュールを設定<li>管理者ユーザーがスケジュール済み読み込みを編集したとき<li>管理者ユーザーがスケジュールされた読み込みを実行<li>管理者ユーザーがスケジュールされた読み込みを削除<li>管理者ユーザーがインポート/エクスポート操作の一括削除を実行します<ul/> |

### ディスプレイの強化と、フィルタリングと並べ替えの改善

管理者ユーザーがより多くの情報を持つグリッドを使用できるように、HIPAA 対応サービスでは、データの表示、フィルタリング、並べ替えにいくつかの機能強化を提供しています。

#### 履歴を読み込み（[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History]）

- を除くすべての列に対してフィルターを有効にしました **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**、および **[!UICONTROL Summary]**.

#### エクスポート （[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export]）

- さんがを追加しました **[!UICONTROL ID]** 列。
- がを追加しました **[!UICONTROL Requested At]** 列（_エクスポートが要求された日時_）に設定します。
- がを追加しました **[!UICONTROL User]** 列（_リクエストを行った管理者のユーザー名_）に設定します。
- が削除されました **[!UICONTROL Action]** 列。
- がを移動しました **[!UICONTROL Download]** へのリンク **[!UICONTROL File name]** 列（_[ 履歴を読み込み ] グリッドに似ています_）に設定します。
- 書き出されたファイル（_トラッキングを改善するには_）に設定します。
- を除くすべての列で並べ替えが有効になりました **[!UICONTROL File name]**.
- すべての列に対してフィルターを有効にしました。

#### スケジュールされた読み込みと書き出し（[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export]）

- さんがを追加しました **[!UICONTROL ID]** 列。
- がを追加しました **[!UICONTROL Scheduled At]** 列（the _インポートまたはエクスポートがスケジュールされた日時_）に設定します。
- がを追加しました **[!UICONTROL User]** 列（the _インポートまたはエクスポートをスケジュールした管理者ユーザーのユーザー名_）に設定します。

## 無効にされたサービスと機能

HIPAA の要件に準拠するために、Adobe Commerceでサポートされている一部のサービスや機能は、デフォルトでは使用できないか無効になっています。 マーチャントは、これらのサービスや機能を自分の責任で再度有効化または使用するオプションがあります。

### サービス

- **Adobe Commerce サービス**—HIPAA 対応ソリューションでは、Adobe Commerce サービスや拡張サービスは利用できません。 これらのサービスには以下が含まれますが、これらに限定されません。

   - Live Search
   - API メッシュ
   - App Builder
   - カタログサービス

- **[SendGrid サービス](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** – アプリケーションが HIPAA に準拠していないので、このサービスはデフォルトで無効になっています。

### デフォルトで無効になっている機能

次の機能は、HIPAA 対応モジュールでデフォルトで無効になっています。 マーチャントは、独自の責任でこれらの機能のいずれかを有効にすることができます。

- **[ゲストのチェックアウト](../stores-purchase/checkout-guest.md)** – この機能は、ログ、アクセス制御、PHI ハイジーンと系統など、HIPAA の様々な側面に対する潜在的なリスクをもたらし、さらに多くの可能性があります。

- **[ニュースレター機能](../merchandising-promotions/newsletters.md)** – この機能は、マーケティングコンテキストで PHI が使用されるのを防ぐために無効になっています。

- **[高度なレポートサービス設定](../getting-started/business-intelligence.md)** – この構成設定は、PHI が分析およびレポートに使用されるのを防ぐために無効になっています。
