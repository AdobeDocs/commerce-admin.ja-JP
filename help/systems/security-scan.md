---
title: セキュリティスキャン
description: 強化されたセキュリティスキャンを実行し、Adobe CommerceとMagento Open Sourceの各サイトを監視する方法について説明します。
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 8e634311cd84a9e797a36218c29abb4699d72835
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# セキュリティスキャン

拡張されたセキュリティスキャンを使用すると、PWAを含むAdobe CommerceおよびMagento Open Sourceの各サイトを監視して、既知のセキュリティリスクやマルウェアを調べ、パッチの更新およびセキュリティ通知を受け取ることができます。

- ストアのリアルタイムのセキュリティステータスに関するinsightを取得します。
- 問題を解決するのに役立つ、ベストプラクティスに基づいた提案を受け取ります。
- セキュリティスキャンをスケジュールして、毎週、毎日、またはオンデマンドで実行します。
- 21,000 を超えるセキュリティテストを実行して、潜在的なマルウェアを特定します。
- サイトの進行状況を追跡および監視する履歴セキュリティレポートにアクセスします。
- 成功したチェックと失敗したチェックを表示するスキャン レポートにアクセスします。推奨されるアクションも表示されます。

セキュリティスキャンツールは、[Commerce/Magento アカウント ](../getting-started/commerce-account-create.md) のダッシュボードから無料で使用できます。 技術情報については、『 [2&rbrace;Cloud Infrastructure ガイドのCommerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) セキュリティスキャンツールの設定 _を参照してください。_

![ セキュリティスキャンツール ](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## セキュリティスキャンを実行

1. [Commerce/Magento アカウント ](../getting-started/commerce-account-create.md) にログインします。

1. 左側のパネルで、「[!UICONTROL Security Scan]」タブをクリックします。 （必要に応じて、セキュリティスキャンツールを使用するために更新された条項を確認して同意してください。）

   - 左側のパネルで「**[!UICONTROL Security Scan]**」を選択します。
   - 「**[!UICONTROL Go to Security Scan]**」をクリックします。
   - **[!UICONTROL Terms and Conditions]** を読んでください。
   - 「**[!UICONTROL Agree]**」をクリックして続行します。

1. _[!UICONTROL Monitored Websites]_&#x200B;ページで「**[!UICONTROL +Add Site]**」をクリックします。

   異なるドメインを持つ複数のサイトがある場合は、ドメインごとに個別のスキャンを設定します。

   ![ 監視対象サイト ](./assets/monitored-website.png){width="600" zoomable="yes"}

1. 確認コードを追加してサイト ドメインの所有権を確認するには、次のいずれかの操作を行います。

   **Commerce ストアフロント**:

   - **[!UICONTROL Site URL]** と **[!UICONTROL Site Name]** を入力します。
   - 「**[!UICONTROL Generate Confirmation Code]**」をクリックします。
   - 「**コピー**」をクリックして、確認コードをクリップボードにコピーします。

     ![ 確認コードを生成 ](./assets/scan-site1.png){width="400" zoomable="yes"}

   - 完全な管理者権限を持つユーザーとしてストアの管理者にログインし、次の手順を実行します。

      - _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**&#x200B;に移動します。
      - リストでサイトを見つけて、「**[!UICONTROL Edit]**」をクリックします。
      - 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL HTML Head]**」セクションを展開します。
      - **[!UICONTROL Scripts and Style Sheets]** までスクロールし、既存のコードの末尾にあるテキストボックスをクリックして、確認コードをテキストボックスに貼り付けます。

        ![ スクリプトとスタイルシート ](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - 完了したら、「**[!UICONTROL Save Configuration]**」をクリックします。

   **PWA ストアフロント**:

   - **[!UICONTROL Site URL]** と **[!UICONTROL Site Name]** を入力します。

   - **[!UICONTROL Confirmation Code]** の場合は、`META Tag` オプションを選択し、「**[!UICONTROL Generate Code]**」をクリックします。

   - 「**[!UICONTROL Copy]**」をクリックして、生成された確認コードの META タグをクリップボードにコピーします。

     ![ 確認コードを生成 ](./assets/scan-site2.png){width="400" zoomable="yes"}

   - PWA Studio ストアフロントのプロジェクトディレクトリに移動して、次の手順を実行します。

      - PWA Studio プロジェクトディレクトリの下で、`packages > venia-concept > template.html` に移動します。
      - コピーした確認コード（生成された META タグ）をHTMLの先頭に追加し、変更内容を保存します。

        ![ 確認コードをコピー ](./assets/code-pwa.png){width="600" zoomable="yes"}

      - PWA Studio CLI に戻り、yarn を使用してプロジェクトの依存関係をインストールし、project build コマンドを実行します。

        ```sh
        yarn install &&
        yarn build
        ```

      - *クラウドプロジェクトで*、`pwa` フォルダーを作成し、ストアフロントプロジェクトの `dist` フォルダー内にコンテンツをコピーします。

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Git CLI ツールを使用して、これらの変更をステージング、コミットし、クラウドプロジェクトにプッシュします。

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        ビルドプロセスが完了すると、変更内容がPWA ストアフロントにデプロイされます。

1. Commerce アカウントの _[!UICONTROL Security Scan]_&#x200B;ページに戻り、「**[!UICONTROL Verify Confirmation Code]**」をクリックしてドメインの所有権を確立します。

1. 確認が正常に完了したら、次のいずれかのタイプで **[!UICONTROL Set Automatic Security Scan]** のオプションを設定します。

   **毎週スキャン （推奨）**:

   - 毎週スキャンを実行する **[!UICONTROL Week Day]**、**[!UICONTROL Time]**、**[!UICONTROL Time Zone]** を選択します。
   - デフォルトでは、スキャンは毎週午前 0 時（土曜日、UTC）に開始され、毎週早朝（日曜日）まで継続するようにスケジュールされています。

     ![ 毎週スキャン ](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **毎日スキャン**:

   - **[!UICONTROL Time]** を選択し、スキャンが毎日実行されることを **[!UICONTROL Time Zone]** 認します。
   - デフォルトでは、スキャンは毎日、午前 0 時（UTC）に開始するようにスケジュールされています。

     ![ 毎日スキャン ](./assets/scan-daily.png){width="500" zoomable="yes"}

1. 完了したスキャンとセキュリティ更新の通知を受信する **[!UICONTROL Email Address]** を入力します。

   ![ メールアドレス ](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Submit]**」をクリックします。

   ドメインの所有権が確認されると、そのサイトはCommerce アカウントの監視対象 Web サイトリストに表示されます。

1. 異なるドメインを持つ複数の web サイトがある場合は、このプロセスを繰り返して、それぞれのセキュリティスキャンを設定します。

## セキュリティ スキャンを削除する

>[!NOTE]
>
>スキャンを最初に設定したユーザーのみが、アカウントから削除できます。 2022 年 8 月以降 [ アカウント ](https://account.magento.com) にログインしていない場合は、まず [Adobe IDに登録 ](https://account.magento.com) していることを確認する必要があります。

**スキャンの削除**

1. [Commerce/Magento アカウント ](../getting-started/commerce-account-create.md) にログインします。

1. 左側のパネルで、「[!UICONTROL Security Scan]」タブをクリックします。 （必要に応じて、セキュリティスキャンツールを使用するために更新された条項を確認して同意してください。）

   - 「**[!UICONTROL Go to Security Scan]**」をクリックします。
   - **[!UICONTROL Terms and Conditions]** を読んでください。
   - 「**[!UICONTROL Agree]**」をクリックして続行します。

1. _[!UICONTROL Monitored Websites]_&#x200B;ページで、「[!UICONTROL Actions]」列の下のドロップダウンを見つけ、適切な web サイトの「**[!UICONTROL Delete]**」を選択します。
