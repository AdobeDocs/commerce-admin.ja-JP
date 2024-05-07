---
title: Adobe Commerceに対する HIPAA 対応
description: Adobe Commerce HIPAA 対応モジュールを追加し、HIPAA 義務に準拠できるその他の機能を取得する方法を説明します。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: c21c8b76e37e617885bae3492801b45093a6b5a5
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 0%

---

# Adobe Commerceに対する HIPAA 対応

>[!IMPORTANT]
>
>**免責事項**<br/>
>この情報は、Adobeのお客様がAdobeの HIPAA 対応サービスに関する質問に答えるのに役立ちます。 それは法的な助言にはならない。 マーチャントは、HIPAA の下での義務やAdobeの商品の適切な使用と設定を理解するために、自社の法務担当者に相談する必要があります。

## HIPAA （Health Insurance Portability and Accountability Act：医療保険の相互運用性と説明責任に関する法律）

HIPAA （Health Insurance Portability and Accountability Act：医療保険の携行性と責任に関する法律）は、米国では主要な連邦医療プライバシー法であり、米国保健福祉省（Department of Health and Human Services:HHS）によって施行されています。 HIPAA の適用先 _対象エンティティ_ （医療機関、保険会社、クリアリングハウスなど） _ビジネス・アソシエイツ_ （対象事業者に対してサービスを提供する事業者など） HIPAA の要件は、「Privacy Rule」、「Security Rule」、「Breach Notification Rule」の 3 つの異なるルールで設定されます。 Adobeは、特定の製品（Adobeが「HIPAA 対応サービス」に分類する）のビジネスアソシエイトとして機能します。 HIPAA で規制されるデータは次のとおりです _保護された医療情報_ または PHI。 PHI とは、（1）医療提供者、健康計画若しくは医療情報交換所が作成または受領した健康情報、（2）個人の過去、現在または将来の心身の健康若しくは状態、個人への医療提供または個人への医療提供の過去、現在または将来の支払いに関する情報、（3）個人または個人を識別するために利用できると信ずるに足る合理的な根拠を特定する情報です。 HIPAA のプライバシーおよびセキュリティに関するルールでは、対象となるエンティティは、ビジネス・アソシエイトからビジネス・アソシエイト契約（BAA）の形式で書面による保証を取得し、ビジネス・アソシエイトが対象となるエンティティの PHI のプライバシーおよびセキュリティを保護するʼとを求めています。

## Adobe Commerce HIPAA 対応

Adobe Commerce HIPAA 対応には、マーチャントがそれぞれの HIPAA 義務を遵守できる追加の機能があります。 Adobe Commerce HIPAA 対応（`magento/hipaa-ee`） モジュールをクラウドインフラストラクチャー上のAdobe Commerceに追加します。 また、HIPAA に準拠するために無効にする必要がある機能もあります。

*これらの資料は情報提供のみを目的としています。 この情報の提供は、受信者に契約上またはその他の権利を与えるものではありません。 また、Adobeは、提供日現在における正確な情報を提供しておりますが、正確かつ完全であることを表明するものではなく、Adobeの商品やサービスの変更に伴い情報を更新する義務を負うものではありません。 また、Adobeの書面による同意なく、対象者以外の者に配布することはできません。*

## 必要システム構成

Adobe Commerceでの HIPAA 対応には、Adobe Commerceと同じシステム要件に加えて、次の要件があります。

- Adobe Commerce バージョン 2.4.6-p3 以降（非ベータ版）
- クラウドインフラストラクチャー上のAdobe CommerceまたはManaged Services上のAdobe Commerce
- の最新バージョン `magento/hipaa-ee` 拡張子

## インストール

Adobeの HIPAA 対応サービスは、技術的にはコンポーザーのメタパッケージです `magento/hipaa-ee` 特別なモジュールへのリンクが含まれています。 このメタパッケージはリポジトリにあります [repo.magento.com](https://repo.magento.com).

1. インストールするには `magento/hipaa-ee` メタパッケージ、あなたはそれにアクセスする必要があります。 キーの生成と必要な権限の取得については、を参照してください。 [認証キーの取得](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. パッケージをインストールする環境を確認し、一般パッケージを満たしていることを確認します [必要システム構成](#system-requirements).

1. メタパッケージを追加 `magento/hipaa-ee` を composer 設定に追加します。

   最も簡単な方法は、composer CLI を使用することです。 例：

   ```shell
   composer require magento/hipaa-ee
   ```

1. Adobe Commerceがまだインストールされていない場合は、インストールを開始できます（以下に従います） [インストール手順](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)）に設定します。

   Adobe Commerceが既にインストールされている場合は、モジュールをダウンロードした後で、を実行します。 `bin/magento setup:upgrade` コマンドと推奨事項に従ってください。

   ```shell
   bin/magento setup:upgrade
   ```

   このコマンドを実行すると、新しくダウンロードしたモジュールが有効になり、モジュールをインストールするためのスクリプトが起動します。 モジュール管理の詳細については、を参照してください。 [モジュールの有効化または無効化](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. インストールまたは更新プロセスが完了したら、 `Hipaa*` 関連するモジュールが含まれています。

   次のコマンドを実行します。

   ```shell
   bin/magento module:status
   ```

   HIPAA コンポーザパッケージが正しく追加されている場合は、コマンドの出力に HIPAA モジュールが表示されます。 例：

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

この `magento/hipaa-ee` パッケージでは、Commerceの基本商品にいくつかの変更と機能強化が導入されています。 次のセクションでは、これらの変更の詳細と、基本製品の変更方法について説明します。

### アクションログ

監査ログは HIPAA 要件の 1 つです。 Adobe Commerceでは、 [アクションログ](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 機能は、ストアで作業する管理者ユーザーが行ったすべての変更を記録します。 監査ログに関する HIPAA 要件を満たすために、管理 UI および API 呼び出しを使用して実行されたすべての管理者ユーザーおよび顧客アクションを記録する機能が変更されました。

#### アクションログレポート

この _アクションログ_ レポートグリッド （**[!UICONTROL System]** / アクションログ / レポート）が変更され、管理 UI および API を使用して実行されたお客様のアクションに対応するようになりました。

1. 2 つの追加の列：
   - ***ソース***：アクションが実行された場所を表示します。\
     値： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***クライアントタイプ***：クライアントタイプが表示されます。\
     値：Customer |管理者 |統合


2. 名前を変更 ***ユーザー名*** 対象： ***クライアント識別子***
   - ***クライアント識別子***：アクションを実行したユーザーのログイン ID が表示されます\
     値：
      - クライアントタイプが「顧客」の場合はメール
      - 「Client Type」が「Admin」の場合のユーザー名
      - 「クライアントタイプ」が「統合」の場合の名前

3. 名前を変更 ***完全なアクション名*** 対象： ***ターゲット***
   - ***ターゲット***：アクション名を表示します\
     値：
      - ソースが REST API または SOAP API の場合のエンドポイント
      - GraphQL API の場合はクエリ/ミューテーション名
      - 管理 UI または顧客 UI の場合はアクション名。

#### ログ用の管理者アクションの設定

すべてのアクションがデフォルトで記録される必要があるので、この機能は使用できません。

### 機能のインポート/エクスポート

インポート/エクスポート機能の機能強化は、管理操作の改善と、ユーザーのアクションの可視性の向上に重点を置いています。

>[!NOTE]
>
>これら ***機能強化によってインポート/エクスポートのコアロジックが変更されることはありません***&#x200B;代わりに、機能を拡張して、より包括的なログと改善されたデータアトリビューションを提供します。 インポート/エクスポートの基本的な機能は変更されません。 ユーザーは、中断することなく既存の機能とワークフローを引き続き使用できます。

#### 管理アクションログ

読み込み/書き出し機能における重要な改善点の 1 つは、管理アクションのログの機能強化です。 これにより、データのインポート/エクスポートに関連するアクティビティをより深く掘り下げる機能が導入され、トラッキングと監査性の向上に貢献します。 以下のアクションがログに記録され、 **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**グリッド：

| タイプ | アクション |
| ---- | ------- |
| インポート | <ul><li>管理者ユーザーがインポートを実行します<li>管理者ユーザーが読み込んだファイルをダウンロードします<li>管理者ユーザーがエラーファイルをダウンロードする<ul/> |
| Export | <ul><li>管理者ユーザーからのリクエスト<li>管理者ユーザーが、書き出されたファイルをダウンロードします<ul/> |
| スケジュールされた読み込み/書き出し | <ul><li>管理者ユーザーは書き出しをスケジュールします<li>管理者ユーザーがスケジュールされた書き出しを編集した<li>管理者ユーザーがスケジュールされた書き出しを実行する<li>管理者ユーザーがスケジュールされた書き出しを削除する<li>管理者ユーザーが読み込みのスケジュールを設定<li>管理者ユーザーがスケジュール済み読み込みを編集したとき<li>管理者ユーザーがスケジュールされた読み込みを実行<li>管理者ユーザーがスケジュールされた読み込みを削除<li>管理者ユーザーがインポート/エクスポート操作の一括削除を実行します<ul/> |

### ディスプレイの強化と、フィルタリング/並べ替えの改善

管理者ユーザーにより多くの情報を提供するグリッドを提供するために、データの表示と、フィルタリングおよび並べ替え機能にいくつかの機能強化が加えられました。

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

#### スケジュールされた読み込み/書き出し（[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export]）

- さんがを追加しました **[!UICONTROL ID]** 列。
- がを追加しました **[!UICONTROL Scheduled At]** 列（_インポートまたはエクスポートがスケジュールされた日時_）に設定します。
- がを追加しました **[!UICONTROL User]** 列（_読み込み/書き出しをスケジュールした管理者ユーザーのユーザー名_）に設定します。

## HIPAA 対応の無効化された機能

### SaaS サービス

Adobe Commerceで提供される SaaS サービスは、HIPAA 対応のサービスでは利用できません。 これには以下が含まれますが、これらに限定されません。

- Live Search
- API メッシュ
- App Builder
- カタログサービス

### デフォルトでゲストチェックアウトを無効にした

- ゲストのチェックアウトは、ログ、アクセス制御、PHI ハイジーンと系統など、HIPAA の様々な側面に潜在的なリスクをもたらし、さらに多くの可能性があります。
- ゲストのチェックアウトは、HIPAA 対応モジュールではデフォルトで無効になっていますが、マーチャントが自分の責任で有効にすることができます。

### デフォルトでニュースレター機能を無効にした

- ニュースレター機能は、マーケティングコンテキストで PHI が使用されないようにするために、デフォルトで無効になっていますが、マーチャントが自分の責任で有効にすることができます。

### Advanced Reporting サービス設定をデフォルトで無効にした。

PHI が分析やレポートに使用されないように、Advanced Reporting サービス設定はデフォルトで無効になっていますが、マーチャントが自分の責任で有効にすることができます。

### Sendgrid サービスを既定で無効にしました

アプリケーションが HIPAA に準拠していないので、Sendgrid サービスはデフォルトで無効になっています。 マーチャントは、Sendgrid を有効にするためにサポートリクエストを送信できますが、サービスを使用するリスクを負うことを認める必要があります。
