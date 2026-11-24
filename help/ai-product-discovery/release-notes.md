---
title: AI製品発見リリースノート
description: カタログとPDPのエンリッチメント機能、修正、アップグレードガイダンス、サポートされているCommerceバージョン、既知の問題について、AI製品発見リリースノートを確認します。
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# AI製品発見リリースノート

このリリースノートでは、新機能、修正、アップグレード要件、既知の問題など、カタログのエンリッチメントとPDPのエンリッチメントに関するアップデートについて説明します。 各バージョンエントリは、影響を受ける拡張機能またはワークフローを特定します。

![新機能](../assets/new.svg)
![修正された問題](../assets/fix.svg)修正と改善
![既知の問題](../assets/bug.svg)既知の問題

## リリース 2.1.3 {#release-2-1-3}

*2026年11月30日*

[!BADGE &#x200B; サポート対象]{type=Informative tooltip="サポート対象"} [!DNL Adobe Commerce] 2.4.9、2.4.8、および2.4.7 （PHP 8.3から8.5まで）。[!DNL Adobe Commerce as a Cloud Service]

バージョン 2.1.3では、製品詳細ページのエンリッチメントとカタログのエンリッチメントが、**AI Product Discovery**&#x200B;という新しい管理メニュー項目に統合されています。 さらに、サポートは[!DNL Adobe Commerce as a Cloud Service]に拡張されます。

## リリース 2.1.2 {#release-2-1-2}

*2026年10月22日*

[!BADGE &#x200B; サポートされている]{type=Informative tooltip="サポート対象"} [!DNL Adobe Commerce] 2.4.9、2.4.8、および2.4.7 （PHP 8.3から8.5まで）。

バージョン 2.1.2では、カタログのエンリッチメントが自己完結型の拡張機能になります。 これで、別の[!DNL Adobe Brand Visibility]拡張機能（`magento/llm-optimizer`）によって以前に提供されたすべてのものが含まれるようになりました。承認済みの提案をカタログに適用し、それらをロールバックし、独自の編集を上書きから保護します。

### 以前のバージョンからのアップグレード {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>バージョン 2.1.2を[!DNL Adobe Brand Visibility]拡張機能と一緒にインストールすることはできません。 インストールされている場合は、アップグレードの一環として削除します。

1. [!DNL Adobe Brand Visibility]拡張機能がインストールされている場合は、削除します。

   ```bash
   composer remove magento/llm-optimizer
   ```

   拡張機能が`Magento/LlmoCatalog`を`app/code`にコピーまたはシンボリックしてインストールされた場合は、そのディレクトリを削除します。 モジュールを無効にするだけでなく、まだディスク上にある無効なモジュールは、エンリッチされた製品の元の値を格納するテーブルを`setup:upgrade`がドロップする可能性があります。

1. カタログのエンリッチメントを更新し、変更を適用します。

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   アップグレード後にキャッシュをフラッシュします。 アップグレードにより、既存のアクセス許可が新しい権限リソースに移動され、それらの許可はキャッシュがクリアされるまで有効になりません。

### 要件定義

![新規](../assets/new.svg) **PHP 8.3および[!DNL Adobe Commerce] 2.4.7以降**—PHP 8.1は提供終了となり、PHP 8.2は2026年12月31日に提供終了となります。そのため、どちらもサポートされていません。[!DNL Adobe Commerce] 2.4.6以前はサポートされていません。

### 新機能

![新規](../assets/new.svg) **[!UICONTROL AI Product Discovery]メニュー** - カタログ強化ページには、管理サイドバーに独自のセクションが追加されました。 **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**&#x200B;に移動します。 以前は、ページは&#x200B;**[!UICONTROL Catalog]**&#x200B;未満でした。

![新規](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="まだ一般公開されていません"} **[!UICONTROL Product Details Page Enrichment (Beta)]** – 製品詳細ページのエンリッチメントの提案をレビューするための&#x200B;**[!UICONTROL AI Product Discovery]**&#x200B;の下の新しいページ。 製品の詳細ページエンリッチメントはベータ版で、まだ一般公開されていません。

![新規](../assets/new.svg) **承認済みの提案を適用してロールバックする** – 承認済みの名前と説明の更新は、この拡張機能によってカタログに書き込まれます。 Commerceは、エンリッチメントされた各属性の元の値を最初に変更したときに記録するので、ロールバックでは、同じ属性に複数の提案が適用された後でも、エンリッチメント前の値が常に復元されます。

![新規](../assets/new.svg) **あなたの編集は尊重されます** – 管理者製品フォームで&#x200B;**[!UICONTROL Update Attributes]**&#x200B;を使用して、またはインポートを通じてエンリッチされた名前または説明を変更すると、値が保持され、関連する提案が&#x200B;*古い*&#x200B;とマークされます。 デフォルトのスコープで行われた変更は、値を継承するストアビューにのみ影響します。

![新規](../assets/new.svg) **提案の読み取り専用カタログアクセス**—[!DNL Commerce Catalog Agent]は、製品、カテゴリ、属性セット、製品タイプデータを読み取り、分析用の製品を選択できます。 読み取りは、**[!UICONTROL Used in Product Listing]**&#x200B;とマークされた属性と、エンリッチ可能な属性のみを返します。 カタログデータは変更できません。

### 修正と改善

![修正済みの問題](../assets/fix.svg) **再試行済みの適用が成功したことを報告** – 適用リクエストが既に完了した後に再試行された場合、再試行では、変更を報告せずに適用された変更が報告されるようになりました。 2回は何も書きません。

![修正された問題](../assets/fix.svg) **承認済みサービスのみがカタログを変更できます** – 適用およびロールバックは[!DNL Commerce Catalog Agent]からのみ要求を受け入れます。 以前は、有効なAdobe IMSトークンはすべて受け入れられました。 同じチェックがSOAP リクエストにも適用されるようになりました。

![修正済みの問題](../assets/fix.svg) **より明確なエラー** - Adobe IMSの停止により、`500`ではなく`401`が返されるようになったため、リクエストはカタログに対して再試行されず、認識できないAdobe IMS環境はステージングとして扱われるのではなく拒否されます。

![修正済みの問題](../assets/fix.svg) **Adobe IMS環境** - カタログのエンリッチメントが、実稼動以外の[!DNL Commerce Services] データスペースに接続されたインスタンスを含め、デフォルトで実稼動Adobe IMS環境にサインインするようになりました。 以前は、これらのインスタンスはステージング環境に送信されていました。

![修正された問題](../assets/fix.svg) **[!DNL Adobe Brand Visibility] ドメイン変更後のサインイン** - カタログの強化ページが`abv.adobe.com`から読み込まれるようになりました。これにより、前のドメインがリダイレクトを開始した後のサインインループが修正されます。

### 既知の問題

![既知の問題](../assets/bug.svg) **完全な[!UICONTROL Catalog] アクセス権を持つ役割** – このリリースの前に保存され、すべての&#x200B;**[!UICONTROL Catalog]**&#x200B;が付与されたユーザー役割は&#x200B;**[!UICONTROL Catalog Enrichment Service API]** リソースへのアクセスを保持します。 **[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]**&#x200B;でそのような役割を確認し、必要のないリソースをクリアします。

## リリース 1.0.2 {#release-1-0-2}

カタログエンリッチメント管理ページの最初のリリース。 カタログに提案を適用するには、[!DNL Adobe Brand Visibility]拡張機能が必要です。
