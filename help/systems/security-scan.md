---
title: セキュリティスキャン
description: 拡張セキュリティスキャンを実行し、Adobe CommerceおよびMagento Open Sourceサイトのそれぞれを監視する方法を説明します。
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# セキュリティスキャン

拡張セキュリティスキャンを使用すると、PWAを含むAdobe CommerceおよびMagento Open Sourceサイトを監視し、既知のセキュリティリスクやマルウェアを確認し、パッチ更新やセキュリティ通知を受け取ることができます。

- ストアのリアルタイムのセキュリティステータスを把握します。
- 問題の解決に役立つベストプラクティスに基づいて提案を受け取ります。
- 週次、日次、またはオンデマンドでセキュリティスキャンを実行するようにスケジュールします。
- 21,000 件を超えるセキュリティテストを実施し、潜在的なマルウェアの特定に役立てます。
- サイトの進行状況を追跡および監視する履歴セキュリティレポートにアクセスします。
- 推奨されるアクションと共に、成功したチェックと失敗したチェックを示すスキャンレポートにアクセスします。

セキュリティスキャンツールは、 [コマースアカウント](../getting-started/commerce-account-create.md). 技術情報については、 [セキュリティスキャンツールの設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) （内） _Commerce on Cloud Infrastructure ガイド_.

![セキュリティスキャンツール](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## セキュリティスキャンを実行する

1. コマースホームページに移動し、 [コマースアカウント](../getting-started/commerce-account-create.md) 次の操作を実行します。

   - 左側のパネルで、を選択します。 **[!UICONTROL Security Scan]**.
   - クリック **[!UICONTROL Go to Security Scan]**.
   - 詳しくは、 **[!UICONTROL Terms and Conditions]**.
   - クリック **[!UICONTROL Agree]** をクリックして続行します。

1. 次の日： _[!UICONTROL Monitored Websites]_ページ、クリック&#x200B;**[!UICONTROL +Add Site]**.

   異なるドメインを持つ複数のサイトがある場合、ドメインごとに別々のスキャンを設定する必要があります。

   ![監視対象サイト](./assets/monitored-website.png){width="600" zoomable="yes"}

1. 確認コードを追加して、サイトドメインの所有権を検証するには、次のいずれかの操作を行います。

   **Commerce ストアフロント**:

   - 次を入力します。 **[!UICONTROL Site URL]** および **[!UICONTROL Site Name]**.
   - クリック **[!UICONTROL Generate Confirmation Code]**.
   - クリック **コピー** 確認コードをクリップボードにコピーします。

     ![確認コードを生成](./assets/scan-site1.png){width="400" zoomable="yes"}

   - 完全な管理者権限を持つユーザーとしてストアの管理者にログインし、次の操作を実行します。

      - Adobe Analytics の _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - リストでサイトを見つけ、 **[!UICONTROL Edit]**.
      - 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL HTML Head]** 」セクションに入力します。
      - 下にスクロールして **[!UICONTROL Scripts and Style Sheets]** 既存のコードの末尾にあるテキストボックスをクリックし、確認コードをテキストボックスに貼り付けます。

        ![スクリプトおよびスタイルシート](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - 完了したら、「 **[!UICONTROL Save Configuration]**.

   **PWAストアフロント**:

   - 次を入力します。 **[!UICONTROL Site URL]** および **[!UICONTROL Site Name]**.

   - の場合 **[!UICONTROL Confirmation Code]**、選択 `META Tag` オプションを選択し、 **[!UICONTROL Generate Code]**.

   - クリック **[!UICONTROL Copy]** をクリックして、生成された確認コード META タグをクリップボードにコピーします。

     ![確認コードを生成](./assets/scan-site2.png){width="400" zoomable="yes"}

   - ストアフロントPWA Studioのプロジェクトディレクトリに移動し、次の操作を行います。

      - PWA Studioプロジェクトディレクトリの下で、に移動します。 `packages > venia-concept > template.html`.
      - コピーした確認コード（生成された META タグ）をHTMLのヘッドに追加し、変更を保存します。

        ![確認コードをコピー](./assets/code-pwa.png){width="600" zoomable="yes"}

      - PWA StudioCLI に戻り、yarn を使用してプロジェクトの依存関係をインストールし、プロジェクトのビルドコマンドを実行します。

        ```sh
        yarn install &&
        yarn build
        ```

      - *クラウドプロジェクト内*、 `pwa` フォルダーを作成し、ストアフロントプロジェクトの `dist` フォルダー。

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Git CLI ツールを使用して、これらの変更をクラウドプロジェクトにステージング、コミット、プッシュします。

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        ビルドプロセスが完了すると、変更がPWAストアフロントにデプロイされます。

1. に戻ります。 _[!UICONTROL Security Scan]_ページを開き、「**[!UICONTROL Verify Confirmation Code]**ドメインの所有権を確立します。

1. 確認が正常に完了したら、 **[!UICONTROL Set Automatic Security Scan]** 次のいずれかのタイプのオプション：

   **毎週スキャン（推奨）**:

   - を選択します。 **[!UICONTROL Week Day]**, **[!UICONTROL Time]**、および **[!UICONTROL Time Zone]** 毎週スキャンが行われることを
   - デフォルトでは、スキャンは毎週土曜日の午前 0 時 (UTC) に開始され、日曜日の初めから続行されるようにスケジュールされています。

     ![毎週スキャン](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **毎日スキャン**:

   - を選択します。 **[!UICONTROL Time]**、および **[!UICONTROL Time Zone]** 毎日スキャンが行われることを
   - デフォルトでは、スキャンは毎日午前 0 時 (UTC) に開始するようにスケジュールされています。

     ![毎日スキャン](./assets/scan-daily.png){width="500" zoomable="yes"}

1. 次を入力します。 **[!UICONTROL Email Address]** 完了したスキャンとセキュリティ更新の通知を受け取る場所です。

   ![電子メールアドレス](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Submit]**.

   ドメインの所有権が検証されると、そのサイトがコマースアカウントの監視済み Web サイトリストに表示されます。

1. 異なるドメインを持つ複数の Web サイトがある場合、このプロセスを繰り返して、それぞれに対してセキュリティスキャンを設定します。
