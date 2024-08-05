---
title: Adobe Commerceに対する HIPAA 対応
description: Adobe Commerce HIPAA 対応拡張機能を追加し、HIPAA 義務を準拠できる追加機能を取得する方法について説明します。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: bce0e581e89139875e09b671038a21976eccebca
workflow-type: tm+mt
source-wordcount: '1568'
ht-degree: 1%

---

# Adobe Commerceに対する HIPAA 対応

>[!IMPORTANT]
>
>**免責事項**<br/>
>この情報は、Adobeのお客様がAdobeの HIPAA 対応サービスに関する質問に答えるのに役立ちます。 それは法的な助言にはならない。 マーチャントは、HIPAA の下での義務やAdobeの商品の適切な使用と設定を理解するために、自社の法務担当者に相談する必要があります。

>[!BEGINSHADEBOX]

**HIPAA （Health Insurance Portability and Accountability Act：医療保険の相互運用性と説明責任に関する法律）**

医療保険の相互運用性と説明責任に関する法律(HIPAA)は、米国の主要な連邦医療プライバシー法であり、米国保健・人間サービス省(HHS)によって施行されています。 HIPAAは _対象事業体_ (医療提供者、保険会社、クリアリングハウスなど)および _法人アソシエイツ_ (対象事業体にサービスを提供する事業体など)に適用されます。 HIPAA 要件は、プライバシー ルール、セキュリティ ルール、および違反通知ルールの 3 つの個別のルールにわたって設定されます。 Adobe Systemsは、「HIPAA対応サービス」として分類Adobe Systems特定の製品の法人アソシエイトとして機能します。 HIPAAの下で規制されているデータは、 _保護された健康情報_ またはPHIと呼ばれます。 PHIは、(1)医療提供者、健康保険、または医療クリアリングハウスによって作成または受信される、(2)個人の過去、現在、または将来の身体的または精神的健康または状態、個人への医療の提供、または個人への医療提供に対する過去、現在、または将来の支払いに関連する健康情報のサブセットです。 (3)情報が個人を特定するために使用できると信じる合理的な根拠がある個人またはそれに関して特定します。 HIPAAプライバシーおよびセキュリティルールは、対象事業体が法人アソシエイト契約(BAA)の形式で法人アソシエイトから書面による保証を取得することを要求し、法人アソシエイトが対象事業体のPHIのプライバシーとセキュリティを保護することを要求します。 詳細については、「 [HIPAA とAdobe Systems 製品」および「Adobe Systems セキュリティ センターのサービス](https://www.adobe.com/trust/compliance/hipaa-ready.html) 」を参照してください。

>[!ENDSHADEBOX]

## Adobe Systemsコマース HIPAA 対応

Adobe Commerce HIPAA 対応の拡張機能により、Adobe Commerceのインストールに機能が追加され、マーチャントが HIPAA の各義務に準拠できるようになりました。

Adobe Commerce HIPAA 対応の拡張機能は、クラウドインフラストラクチャー上のAdobe CommerceまたはAdobeのManaged Services プロジェクトで利用で `magento/hipaa-ee` ます。 Adobe Commerce HIPAA 対応のインストールプロセスは、HIPAA の要件に準拠するために、一部のネイティブサービスと機能を無効にします。 [ 無効にされたサービスと機能 ](#disabled-services-and-features) を参照してください。

>[!NOTE]
>
>HIPAA 対応の機能へのアクセスは、Adobe Commerce用ヘルスケアアドオンを購入したマーチャントのみが利用できます。

*これらの資料は情報提供のみを目的としています。 この情報の提供は、受信者に契約上またはその他の権利を与えるものではありません。 また、提供日現在の情報の正確性については保証しておりますが、正確かつ完全なものであることを示すものではありません。 Adobeは、法令またはAdobeの商品の変更に伴い、この情報を更新する義務を負いません。 また、Adobeの書面による同意なく、対象者以外の者に配布することはできません。*

## 必要システム構成

Adobe Commerceは、クラウドインフラストラクチャのAdobe Commerce、またはバージョン 2.4.6-p3 以降（ベータ版なし）のAdobe Commerce Managed Servicesにデプロイする必要があります。

## インストール

**前提条件**

>[!BEGINSHADEBOX]

- Adobe Systems は、HIPAA Ready 拡張機能にアクセスするための Adobe Systems Commerce アカウント をプロビジョニングしました。
- 拡張機能をインストールするための [repo.magento.com](https://repo.magento.com) へのアクセス。 キーの生成と必要な権限の取得については、 [認証キーの取得](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)を参照してください。

>[!ENDSHADEBOX]

Commerce バージョン 2.4.6-p3 以降を実行しているインスタンスに、Adobe Systems の HIPAA 対応サービス拡張機能 (`magento/hipaa-ee`) の最新バージョンAdobe Systemsをインストールします。 この拡張機能は、コンポーザーメタパッケージとして [repo.magento.com](https://repo.magento.com) リポジトリー から提供されています。 メタパッケージには、Adobe Systemsコマースインスタンスの HIPAA 機能を有効にするモジュールのコレクションが含まれています。

1. ローカルワークステーションで、クラウドインフラストラクチャープロジェクトの Adobe Systems Commerce のプロジェクトディレクトリに移動します。

   >[!NOTE]
   >
   >Commerce Adobe Commerce プロジェクト環境のローカル管理について詳しくは、_クラウドインフラストラクチャユーザーガイドの [CLI を使用したブランチの管理 ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) を参照してください_。

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

1. 追加、コミットして、更新したコードをクラウド 環境にプッシュします。

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   更新をプッシュすると、[Commerce クラウドデプロイメントプロセス ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) が開始され、変更が適用されます。 [ デプロイメントログ ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log) からデプロイメントステータスを確認します。

### インストールの確認

更新プログラムが展開されたら、 `Hipaa*` 拡張機能がインストールされていることを確認します

1. SSH を使用してリモート クラウド 環境 にログインします。

   ```shell
   magento-cloud ssh
   ```

1. コマンドラインから、Adobe Systems Commerce CLI を使用してモジュールステータスを確認します。

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

   すべてを選択 モジュールの先頭に `Magento_Hipaa` を付けると、「使用可能モジュール」セクションに入力する必要が生じます。

## HIPAA 対応の機能強化

`magento/hipaa-ee`拡張機能では、基本コマース製品にいくつかの変更と機能強化が導入されています。次のセクションでは、これらの変更の詳細と、それらによってベース製品がどのように変更されるかについて説明します。

### アクションログ

監査ログは HIPAA 要件の 1 つです。 Adobe Commerceでは、[ アクションログ ](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 機能は、ストアで作業している管理者ユーザーが行ったすべての変更を記録します。 監査ログの HIPAA 要件を満たすために、機能が更新され、管理 UI および API 呼び出しを使用して実行されたすべての管理ユーザーおよび顧客操作を記録するようになりました。

#### アクションログレポート

_アクションログ_ レポートグリッド（**[!UICONTROL System]**/アクションログ/レポート）は、管理 UI および API を使用して実行された顧客のアクションに対応するように変更されます。

1. 次の 2 つの列を追加しました。
   - ***出力元***: アクションが実行された場所を表示します。値：`Admin UI`/`Customer UI`/`REST API`/`SOAP API`/`GraphQL API`
   - ***クライアントの種類***: クライアントの種類を表示します。
値：Customer |管理者 |統合

2. ***ユーザー名*** 列の名前を ***クライアント識別子*** に変更しました
   - ***クライアント 識別情報***:アクションを実行したユーザーのログイン ID を表示します。価値観：
      - クライアント 書式 ＜例外＞Photoshop のみ「テキスト」がお客様の場合は電子メール
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

### 機能の読み込みと書き出し

インポート機能とエクスポート機能の強化は、管理エクスペリエンスの向上とユーザーアクションの可視性の向上に重点を置いています。

>[!NOTE]
>
>これらの ***機能強化は、インポートおよび書き出しコアロジックを変更するものではなく***&#x200B;機能を拡張して、より包括的なログと改善されたデータ属性オファーします。 インポートとエクスポートの基本的な機能に変更はありません。 ユーザーは、中断することなく既存の機能とワークフローを引き続き使用できます。

#### 管理アクションログ

インポートおよびエクスポート機能の主な改善点の 1 つは、管理アクションのログの強化です。 この機能強化により、データのインポートとエクスポートに関連するアクティビティをより深く掘り下げる機能が導入され、トラッキングと監査性の向上に貢献します。 以下のアクションがログに記録され、**[!UICONTROL System]/ _[!UICONTROL Action Logs]_/[!UICONTROL Report]**グリッドに反映されるようになりました。

| タイプ | アクション |
| ---- | ------- |
| インポート | <ul><li>管理者ユーザーがインポートを実行します<li>管理者ユーザーが読み込んだファイルをダウンロードします<li>管理者ユーザーがエラーファイルをダウンロードする<ul/> |
| Export | <ul><li>管理者ユーザーからのリクエスト<li>管理者ユーザーが、書き出されたファイルをダウンロードします<ul/> |
| スケジュールされた読み込み/書き出し | <ul><li>管理者ユーザーは書き出しをスケジュールします<li>管理者はスケジュールされた書き出しを編集するユーザー<li>管理者ユーザースケジュールされた書き出しを実行します<li>管理者ユーザースケジュールされた書き出しを削除する<li>管理者はユーザーインポートをスケジュールします<li>管理者ユーザーがスケジュール済み読み込みを編集したとき<li>管理者ユーザーがスケジュールされた読み込みを実行<li>管理者ユーザーがスケジュールされた読み込みを削除<li>管理者ユーザーがインポート/エクスポート操作の一括削除を実行します<ul/> |

### ディスプレイの強化と、フィルタリングと並べ替えの改善

管理者ユーザーがより多くの情報を持つグリッドを使用できるように、HIPAA 対応サービスでは、データの表示、フィルタリング、並べ替えにいくつかの機能強化を提供しています。

#### インポート履歴（[!UICONTROL System]/_[!UICONTROL Data Transfer]_/[!UICONTROL Import History]）

- **[!UICONTROL Imported File]**、**[!UICONTROL Error File]**、**[!UICONTROL Execution Time]**、**[!UICONTROL Summary]** を除くすべての列に対してフィルターを有効にしました。

#### 書き出し（[!UICONTROL System]/_[!UICONTROL Data Transfer]_/[!UICONTROL Export]）

- **[!UICONTROL ID]** 列を追加しました。
- **[!UICONTROL Requested At]** 列（_書き出しがリクエストされた日時_）を追加しました。
- **[!UICONTROL User]** 列（_リクエストを行った管理者のユーザー名_）を追加しました。
- **[!UICONTROL Action]**&#x200B;列を削除しました。
- **[!UICONTROL Download]** リンクを&#x200B;**[!UICONTROL File name]**&#x200B;列(_インポート ヒストリーグリッドなど_)に移動しました。
- エクスポートされたファイルの削除を担当するアクション無効(_トラッキング_&#x200B;を向上させるため)。
- **[!UICONTROL File name]**&#x200B;列を除くすべての列の並べ替え有効。
- すべての列のフィルタリング有効。

#### スケジュールされたインポートおよびエクスポート（[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export]）

- **[!UICONTROL ID]** 列を追加しました。
- **[!UICONTROL Scheduled At]** 列（_読み込みまたは書き出しがスケジュールされた日時_）を追加しました。
- **[!UICONTROL User]** の列（_読み込みまたは書き出しをスケジュールした管理者ユーザーのユーザー名_）を追加しました。

## 無効にされたサービスと機能

HIPAA 要件に準拠するために、Adobe Systems Commerce でサポートされている一部のサービスと機能は、既定で使用できないか無効になっています。 マーチャントは、自己責任でこれらのサービスや機能を再度有効にするか、使用するかを選択できます。

### サービス

- **Adobe Commerce サービス** - HIPAA 対応のサービスでは、Adobe Commerce サービスまたは拡張サービスは利用できません。 これらのサービスには以下が含まれますが、これらに限定されません。

   - ライブ サーチです
   - API メッシュ
   - アプリケーションビルダー

- **[SendGrid サービス ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** - アプリケーションが HIPAA に準拠していないので、このサービスはデフォルトで無効になっています。

### デフォルトで無効になっている機能

次の機能は、HIPAA 対応モジュールでデフォルトで無効になっています。 マーチャントは、独自の責任でこれらの機能のいずれかを有効にすることができます。

- **[ゲストのチェックアウト](../stores-purchase/checkout-guest.md)** – この機能は、ログ、アクセス制御、PHI 衛生と系統など、HIPAA の様々な側面で発生する可能性のあるリスクであり、さらに多くの可能性があります。

- **[ニュースレター機能](../merchandising-promotions/newsletters.md)** – この機能は、マーケティングコンテキストで PHI が使用されないようにするために無効になっています。

- **[詳細レポート サービス設定](../getting-started/business-intelligence.md)** – この構成設定は、PHI が分析およびレポートに使用されるのを防ぐために無効になっています。
