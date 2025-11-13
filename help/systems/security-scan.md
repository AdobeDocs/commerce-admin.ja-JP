---
title: セキュリティスキャン
description: 強化されたセキュリティスキャンを実行し、Adobe CommerceとMagento Open Sourceの各サイトを監視する方法について説明します。
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 5dd564185975216361918bda4954ed4a6fc8fee4
workflow-type: tm+mt
source-wordcount: '1150'
ht-degree: 0%

---

# セキュリティスキャン

Adobe Commerce サイトとMagento Open Source サイトでセキュリティのリスクやマルウェアを監視し、セキュリティの更新や通知を受け取ります。

- ストアのリアルタイムのセキュリティステータスに関するinsightを取得します。
- 問題を解決するのに役立つ、ベストプラクティスに基づいた提案を受け取ります。
- 毎週、毎日、またはオンデマンドで実行するようにセキュリティスキャンをスケジュールします。
- 21,000 を超えるセキュリティテストを実行して、潜在的なマルウェアを特定します。
- サイトの進行状況を追跡および監視する履歴セキュリティレポートにアクセスします。
- 成功したチェックと失敗したチェックを表示するスキャン レポートにアクセスします。推奨されるアクションも表示されます。

セキュリティスキャンツールは、[Commerce/Magento アカウント ](../getting-started/commerce-account-create.md) のダッシュボードから無料で利用できます。 Commerce技術情報については、[2}Cloud Infrastructure ガイドのセキュリティスキャンツールの設定 ](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/launch/overview#set-up-the-security-scan-tool) を参照してください __

![ セキュリティスキャンツール ](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## ワークフロー

Adobe Commerce サイトまたはMagento Open Source サイトのセキュリティスキャンツールをセットアップおよび設定するには、次の 2 つの手順を実行します。

1. [セキュリティスキャン用のサイトの設定](#step-1-set-up-your-site-for-security-scanning)
2. [自動セキュリティ スキャンを構成する](#step-2-configure-automatic-security-scans)

### 手順 1：サイトのセキュリティスキャン用のセットアップ

1. Commerceのホームページから、[Commerce/Magento アカウント ](../getting-started/commerce-account-create.md) にログインします。

2. セキュリティ スキャン ツールの使用条件を確認し、同意します。

   1. 左側のパネルで「**[!UICONTROL Security Scan]**」を選択します。
   1. 「**[!UICONTROL Go to Security Scan]**」をクリックします。
   1. **[!UICONTROL Terms and Conditions]** を読んでください。
   1. 「**[!UICONTROL Agree]**」をクリックして続行します。

3. _[!UICONTROL Monitored Websites]_ページで「**[!UICONTROL +Add Site]**」をクリックします。

   異なるドメインを持つ複数のサイトがある場合は、ドメインごとに個別のスキャンを設定します。

   ![ 監視対象サイト ](./assets/monitored-website.png){width="600" zoomable="yes"}

4. 確認コードを生成してセキュリティ スキャン ツールに追加することにより、サイト ドメインの所有権を確認します。

   確認コードを追加するプロセスは、使用しているストアフロントのタイプによって異なります。 ストアフロントタイプの手順に従います。

>[!BEGINTABS]

>[!TAB Commerce ストアフロント ]

1. **[!UICONTROL Site URL]** と **[!UICONTROL Site Name]** を入力します。
1. 「**[!UICONTROL Generate Confirmation Code]**」をクリックします。
1. 「**コピー**」をクリックして、確認コードをクリップボードにコピーします。

   ![ 確認コードを生成 ](./assets/scan-site1.png){width="400" zoomable="yes"}

1. 完全な管理者権限を持つユーザーとしてストアの管理者にログインし、次の手順を実行します。

   1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**に移動します。
   1. リストでサイトを見つけて、「**[!UICONTROL Edit]**」をクリックします。
   1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL HTML Head]**」セクションを展開します。
   1. **[!UICONTROL Scripts and Style Sheets]** までスクロールし、既存のコードの末尾にあるテキストボックスをクリックします。 確認コードをテキストボックスに貼り付けます。

      ![ スクリプトとスタイルシート ](./assets/scan-paste-code.png){width="600" zoomable="yes"}

   1. 完了したら、「**[!UICONTROL Save Configuration]**」をクリックします。

1. Commerce アカウントの _[!UICONTROL Security Scan]_ページに戻り、「**[!UICONTROL Verify Confirmation Code]**」をクリックしてドメインの所有権を確立します。

>[!TAB PWA ストアフロント ]

1. **[!UICONTROL Site URL]** と **[!UICONTROL Site Name]** を入力します。

1. **[!UICONTROL Confirmation Code]** の場合は、`META Tag` オプションを選択し、「**[!UICONTROL Generate Code]**」をクリックします。

1. 「**[!UICONTROL Copy]**」をクリックして、生成された確認コードのMETAタグをクリップボードにコピーします。

   ![ 確認コードを生成 ](./assets/scan-site2.png){width="400" zoomable="yes"}

1. PWA Studio ストアフロントのプロジェクトディレクトリに移動して、次の手順を実行します。

   1. PWA Studio プロジェクトディレクトリの下で、`packages > venia-concept > template.html` に移動します。
   1. コピーした確認コード（生成されたMETA タグ）をHTMLのヘッドに追加し、変更内容を保存します。

      ![ 確認コードをコピー ](./assets/code-pwa.png){width="600" zoomable="yes"}

   1. PWA Studio CLI に戻り、yarn を使用してプロジェクトの依存関係をインストールし、project build コマンドを実行します。

      ```sh
      yarn install &&
      yarn build
      ```

   1. *クラウドプロジェクトで*、`pwa` フォルダーを作成し、ストアフロントプロジェクトの `dist` フォルダー内にコンテンツをコピーします。

      ```sh
      mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
      ```

   1. Git CLI ツールを使用して、これらの変更をステージング、コミットし、クラウドプロジェクトにプッシュします。

      ```sh
      git add . &&
      git commit -m "Added storefront file bundles" &&
      git push origin
      ```

      ビルドプロセスが完了すると、変更内容がPWA ストアフロントにデプロイされます。

1. Commerce アカウントの _[!UICONTROL Security Scan]_ページに戻り、「**[!UICONTROL Verify Confirmation Code]**」をクリックしてドメインの所有権を確立します。

>[!TAB AEM ストアフロント ]

1. **[!UICONTROL Site URL]** と **[!UICONTROL Site Name]** を入力します。

1. **[!UICONTROL Confirmation Code]** の場合は、「`HTML Content`」または「`META Tag`」オプションを選択し、「**[!UICONTROL Generate Code]**」をクリックします。

1. 「**[!UICONTROL Copy]**」をクリックして、生成された確認コードをクリップボードにコピーします。

   ![ 確認コードを生成 ](./assets/scan-site3.png){width="400" zoomable="yes"}

1. AEM ストアフロントのプロジェクトディレクトリに移動して、次の手順を実行します。

   1. AEM ストアフロントのプロジェクトディレクトリで、`head.html` に移動します。
   1. コピーした確認コード（生成されたHTML コンテンツまたはMETA タグ） `head.html` ファイルに追加し、変更内容を保存します。

   ![ 確認コードをコピー ](./assets/code-aem.png){width="600" zoomable="yes"}

1. Git CLI ツールを使用して、これらの変更をステージング、コミットし、プロジェクトリポジトリにプッシュします。

   ```sh
   git add . &&
   git commit -m "Added security scan confirmation code" &&
   git push origin
   ```

   ビルドプロセスが完了すると、変更内容がAEM ストアフロントにデプロイされます。

1. Commerce アカウントの _[!UICONTROL Security Scan]_ページに戻り、「**[!UICONTROL Verify Confirmation Code]**」をクリックしてドメインの所有権を確立します。

>[!ENDTABS]

### 手順 2：自動セキュリティ スキャンを構成する

1. サイトの所有権を正常に確認した後、次のいずれかのタイプに対して **[!UICONTROL Set Automatic Security Scan]** のオプションを設定します。

   **毎週スキャン （推奨）**:

   毎週スキャンを実行する **[!UICONTROL Week Day]**、**[!UICONTROL Time]**、**[!UICONTROL Time Zone]** を選択します。

   デフォルトでは、スキャンは毎週午前 0 時（土曜日、UTC）に開始され、毎週早朝（日曜日）まで継続するようにスケジュールされています。

   ![ 毎週スキャン ](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **毎日スキャン**:

   **[!UICONTROL Time]** を選択し、スキャンが毎日実行されることを **[!UICONTROL Time Zone]** 認します。

   デフォルトでは、スキャンは毎日、午前 0 時（UTC）に開始するようにスケジュールされています。

   ![ 毎日スキャン ](./assets/scan-daily.png){width="500" zoomable="yes"}

1. 完了したスキャンとセキュリティ更新の通知を受信する **[!UICONTROL Email Address]** を入力します。

   ![ メールアドレス ](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Submit]**」をクリックします。

   ドメインの所有権が確認されると、そのサイトはCommerce アカウントの監視対象 Web サイトリストに表示されます。

1. 異なるドメインを持つ複数の web サイトがある場合は、このプロセスを繰り返して、それぞれのセキュリティスキャンを設定します。

## スキャン エラーの管理

セキュリティスキャンツールを使用すると、レポート表示から直接スキャンの失敗を管理できます。 特定のスキャンの失敗を偽陽性としてマークし、リスクスコアから除外することができます。

### スキャン エラーを管理する利点

スキャンの失敗を管理することで、次の方法でストアのセキュリティの概要をより正確に維持できます。

- セキュリティレポートでの誤検出を減らす。
- 注意が必要な関連するセキュリティ問題に焦点を当てます。
- ストアの真のセキュリティ・ステータスをより明確に把握する。
- 既知の偽陽性について、サポートへの連絡を不要にします。
- 既に調査したスキャンの失敗を自己管理することで、時間を節約できます。

スキャンの失敗を偽陽性としてマークする一般的なシナリオを次に示します。

- 既にセキュリティパッチを適用していて、スキャンツールが検出されなかった場合。
- 検出された問題が特定のストア設定に適用できない場合。
- 問題に対処する別のセキュリティ対策を実装した場合。
- スキャンエラーが、ビジネスニーズに合わせて意図的に設定した設定に基づいている場合。

### スキャン エラーを無視する

誤検出と識別されたスキャンエラーを管理するには、次の手順に従います。

1. _[!UICONTROL Monitored Websites]_ページで、管理するサイトの&#x200B;**[!UICONTROL View Report]**をクリックします。

1. レポート ビューで、誤検出としてマークする失敗したスキャンを見つけます。

1. 特定のスキャン エラーの **[!UICONTROL Ignore]** をクリックします。

   ![ スキャン エラーを無視する ](assets/security-scan-ignore-failure.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Apply Changes]**」をクリックして選択内容を保存します。

無視されたスキャンエラーは _[!UICONTROL Ignored Results]_のセクションに移動し、リスクスコアから除外されます。

### スキャンの失敗を無視しない

以前に無視したスキャンの失敗をアクティブなモニタリングに復元する必要がある場合は、次の手順に従います。

1. レポート ビューで、[_[!UICONTROL Ignored Results]_] セクションまでスクロールします。

1. 復元するスキャン エラーの **[!UICONTROL Stop Ignoring]** をクリックします。

   ![ スキャン エラーの無視の解除 ](assets/security-scan-stop-ignoring-failure.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Apply Changes]**」をクリックして選択内容を保存します。

スキャンの失敗は _[!UICONTROL Failed Scans]_のセクションに戻り、リスクスコアに含まれます。

### 無視されたスキャン エラーの表示

無視された結果は、レポートの別のセクションに表示され、リスクスコアはアクティブなスキャンエラーのみを反映するように自動的に更新されます。 変更を適用する前に複数の項目を選択することで、複数のスキャン失敗を一度に管理できます。

![ 無視されたスキャン エラーの表示 ](assets/security-scan-view-ignored-failures.png){width="600" zoomable="yes"}
