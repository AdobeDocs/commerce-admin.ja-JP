---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL System]'
description: 次のページで設定を確認します： [!UICONTROL Advanced] &gt; [!UICONTROL System] コマース管理のページ。
exl-id: ffdaf7b5-c508-4fab-93ec-21f28cff6d3d
role: Admin, Developer
feature: Configuration, System
source-git-commit: 3a113d162f13c659ee52ae3cbff2c7a3873d3857
workflow-type: tm+mt
source-wordcount: '1636'
ht-degree: 1%

---

# [!UICONTROL Advanced] > [!UICONTROL System]

{{config}}

## [!UICONTROL Cron (Scheduled Tasks)]

![高度な設定 — Cron（予定タスク）](./assets/system-cron.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [Cron（予定タスク）](../../systems/cron.md).

### [!UICONTROL index]

![高度な設定 — Cron グループ：インデックス](./assets/system-cron-group-index.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Generate Schedules Every] | グローバル | スケジュールが生成される頻度を分単位で指定します。 |
| [!UICONTROL Schedule Ahead for] | グローバル | スケジュールが生成されるまでの時間（分）を指定します。 |
| [!UICONTROL Missed if Not Run Within] | グローバル | まだ実行されていない Cron ジョブが未実行とマークされるまでの分数を決定します。 |
| [!UICONTROL History Cleanup Every] | グローバル | Cron 履歴がクリーンアップされるまでに経過する時間（分）を決定します。 |
| [!UICONTROL Success History Lifetime] | グローバル | 正常に完了した cron ジョブのレコードをデータベースに保持する時間（分）を決定します。 |
| [!UICONTROL Failure History Lifetime] | グローバル | 失敗した cron ジョブのレコードをデータベースに保持する時間（分）を決定します。 |
| [!UICONTROL Use Separate Process] | グローバル | cron ジョブを別々のプロセスとして並行して実行するかどうかを指定します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL default]

![Cron グループ：デフォルト](./assets/system-cron-group-default.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Generate Schedules Every] | グローバル | スケジュールが生成される頻度を分単位で指定します。 |
| [!UICONTROL Schedule Ahead for] | グローバル | スケジュールが生成されるまでの時間（分）を指定します。 |
| [!UICONTROL Missed if Not Run Within] | グローバル | まだ実行されていない Cron ジョブが未実行とマークされるまでの分数を決定します。 |
| [!UICONTROL History Cleanup Every] | グローバル | Cron 履歴がクリーンアップされるまでに経過する時間（分）を決定します。 |
| [!UICONTROL Success History Lifetime] | グローバル | 正常に完了した cron ジョブのレコードをデータベースに保持する時間（分）を決定します。 |
| [!UICONTROL Failure History Lifetime] | グローバル | 失敗した cron ジョブのレコードをデータベースに保持する時間（分）を決定します。 |
| [!UICONTROL Use Separate Process] | グローバル | cron ジョブを別々のプロセスとして並行して実行するかどうかを指定します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL MySQL Message Queue Cleanup]

{{ee-feature}}

![詳細設定 — MySQL メッセージキューのクリーンアップ](./assets/system-mysql-message-queue-cleanup.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Successful Messages Lifetime] | グローバル | 成功したメッセージの有効期間を分単位で決定します。 ゼロを入力してクリーンアップをスキップします。 デフォルト： `10080` （7 日） |
| [!UICONTROL New Messages Lifetime] | グローバル | 新しいメッセージの有効期間を分単位で指定します。 ゼロを入力してクリーンアップをスキップします。 デフォルト： `10080` （7 日） |
| [!UICONTROL Failed Messages Lifetime] | グローバル | 失敗したメッセージの有効期間を分単位で指定します。 ゼロを入力してクリーンアップをスキップします。 デフォルト： `10080` （7 日） |
| [!UICONTROL Retry Messages in Progress After] | グローバル | システムが処理中のメッセージを待機してから再試行する時間を指定します。 デフォルト： `1440` （24 時間） |

{style="table-layout:auto"}

## [!UICONTROL Mail Sending Settings]

![詳細設定 — メール送信設定](./assets/system-mail-sending-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [電子メール通信の設定](../../systems/email-communications.md) （内） _管理システムガイド_.

>[!IMPORTANT]
>
>**セキュリティ通知** 最近特定されたリモートコード実行の悪用から保護するために、すべてのマーチャントがすぐにメール送信設定を行うことをお勧めします。 この問題が解決されるまでは、 [!DNL Sendmail] （電子メール通信用） Adobe Analytics の [!UICONTROL Mail Sending Settings]、次の点を確認します。 [!UICONTROL Set Return Path] が `No`.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Disable Email Communications] | ストア表示 | ストアの電子メール通信を有効にするかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Transport] | ストア表示 | ストアからの E メール通信のトランスポートタイプを決定します。 オプション： `Sendmail` / `SMTP` |
| [!UICONTROL Host] | ストア表示 | （SMTP および Windows サーバーのみ）ホストを参照するために使用される名前を決定します。 デフォルト値： `localhost` |
| [!UICONTROL Port (25)] | ストア表示 | （SMTP および Windows サーバーのみ）電子メール通信に使用するポートを識別します。 デフォルト値： `25` |
| [!UICONTROL Set Return-Path] | ストア表示 | 返された E メールにルーティングアドレスを使用するかどうかを指定します。 オプション： `No` / `Yes` / `Specified` |

{style="table-layout:auto"}

### SMTP オプション

トランスポートの種類で「 SMTP 」を選択した場合は、SMTP サーバー接続を設定するための追加のオプションを使用できます。

![詳細設定 — SMTP を使用したメール送信設定](./assets/system-mail-sending-settings-smtp.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Username] | ストア表示 | SMTP サーバーのログインユーザー名。 |
| [!UICONTROL Password] | ストア表示 | SMTP サーバーログインのパスワード。 |
| [!UICONTROL Auth] | ストア表示 | SMTP サーバー接続の認証の種類を決定します。 オプション： `NONE` / `PLAIN` / `LOGIN` |
| [!UICONTROL SSL] | ストア表示 | ホストセキュリティ証明書の検証の種類を決定します。 オプション： `SSL` / `TLS` |

{style="table-layout:auto"}

## [!UICONTROL Currency]

![詳細設定 — 通貨](./assets/system-currency.png)<!-- zoom -->

この設定の変更の詳細については、 [通貨設定](../../stores-purchase/currency-configuration.md) （内） _店舗および購入エクスペリエンスガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Installed Currencies] | グローバル | Commerce のインストールで現在使用可能な通貨を示します。 オプションには、使用可能なすべての通貨が含まれ、インストール済みの通貨が選択されます。 |

{style="table-layout:auto"}

## [!UICONTROL Security]

![高度な設定 — セキュリティ](./assets/system-security.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [セッション管理](../../systems/security-session-management.md) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Max Session Size in Admin] | グローバル | 最大セッションサイズをバイト単位で制限します。 用途 `0` を無効にします。 |
| [!UICONTROL Max Session Size in Storefront] | グローバル | 最大セッションサイズをバイト単位で制限します。 用途 `0` を無効にします。 |

{style="table-layout:auto"}

## [!UICONTROL Notifications]

![詳細設定 — 通知](./assets/system-notifications.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [システム通知](../../systems/notifications.md) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Use HTTPS to Get Feed] | グローバル | セキュリティで保護されたチャネルを介して管理者通知を配信するかどうかを指定します。 オプション： `Yes` / `No` |
| 更新頻度 | グローバル | 管理メッセージの更新頻度を決定します。 オプション： `1 Hour` / `2 Hours` / `6 Hours` / `12 Hours` / `24 Hours` |
| [!UICONTROL Last Update] | グローバル | 最後のメッセージ更新の日時を示します。 |

{style="table-layout:auto"}

## [!UICONTROL Backup Settings]

![詳細設定 — バックアップ設定](./assets/system-scheduled-backup-settings.png)<!-- zoom -->

{{$include /help/_includes/backups-note.md}}

これらの設定の変更について詳しくは、 [システムのバックアップ](../../systems/backups.md) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Backup] | グローバル | コマースインスタンスがバックアップを許可するかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Scheduled Backup] | グローバル | （次の場合に表示） _[!UICONTROL Enable Backup]_が `Yes`.) コマースインスタンスを定期的に自動的にバックアップするかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Scheduled Backup Type] | グローバル | （次の場合に表示） _[!UICONTROL Enable Scheduled Backup]_が `Yes`.) バックアップに含まれる Commerce インスタンスの要素を決定します。 オプション： `Database` / `Database and Media` / `System` / `System (excluding Media)` |
| [!UICONTROL Start Time] | グローバル | （次の場合に表示） [!UICONTROL Enable Scheduled Backup] が `Yes`.) スケジュールされたバックアップを開始する時間、分、秒を指定します。 |
| [!UICONTROL Frequency] | グローバル | （次の場合に表示） [!UICONTROL Enable Scheduled Backup] が `Yes`.) スケジュールされたバックアップの実行頻度を決定します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Maintenance Mode] | グローバル | （次の場合に表示） [!UICONTROL Enable Scheduled Backup] が `Yes`.) スケジュールされたバックアップ中にストアをメンテナンスモードにするかどうかを指定します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Log Archiving]

{{ee-feature}}

![高度な設定 — 管理アクションログのアーカイブ](./assets/system-admin-actions-log-archiving.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [アクションログのアーカイブ](../../systems/action-log-archive.md) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Log Entry Lifetime, Days] | ストア表示 | 管理アクションが管理アクションアーカイブに保持される日数を決定します。 デフォルト： `60` |
| [!UICONTROL Log Archiving Frequency] | ストア表示 | 管理アクションログをアーカイブする頻度を決定します。 オプション： `Daily` / `Weekly` / `Monthly` |

{style="table-layout:auto"}

## [!UICONTROL Full Page Cache]

{{beta2-patches-updates}}

![詳細設定 — フルページキャッシュ](./assets/system-full-page-cache.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [フルページキャッシュ](../../systems/cache-management.md#full-page-caching) （内） _管理システムガイド_.

![高度な構成 — ワニス構成](./assets/system-full-page-cache-varnish.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Caching Application] | グローバル | フルページキャッシュの管理に使用するアプリケーションを決定します。 オプション： <br/>**`Built-in Application`**— 実稼動環境にはお勧めしません。<br/>**`Varnish Caching`**  — 実稼動環境に推奨されます。 |
| [!UICONTROL TTL for public content] | グローバル | パブリックコンテンツキャッシュの有効期間を秒単位で指定します。 デフォルト値： `120` |
| **[!UICONTROL Varnish Configuration]** |  |  |
| [!UICONTROL Access list] | グローバル | Vanish 構成をパージして設定ファイルを生成できる IP アドレスを指定します。 複数のエントリはコンマで区切ります。 デフォルト値： `localhost` |
| [!UICONTROL Backend host] | グローバル | 設定ファイルを生成するバックエンドホストを指定します。 デフォルト値： `localhost` |
| [!UICONTROL Backend port] | グローバル | 設定ファイルの生成に使用するバックエンドポートを指定します。 デフォルト値： `8080` |
| [!UICONTROL Grace period] | グローバル | 設定ファイルを生成する猶予時間を秒単位で指定します。 デフォルト値： `300` |
| **[!UICONTROL Export Configuration]** |  |  |
| [!UICONTROL Export VCL for Varnish 4] | グローバル | を書き出します。 `varnish.vcl` ファイル（バージョン 4 用） |
| [!UICONTROL Export VCL for Varnish 5] | グローバル | を書き出します。 `varnish.vcl` ファイルのバージョン 5. |
| [!UICONTROL Export VCL for Varnish 6] | グローバル | を書き出します。 `varnish.vcl` ファイル（バージョン 6 用） |

{style="table-layout:auto"}

## [!UICONTROL Storage Configuration for Media]

![高度な構成：メディアのストレージ構成：ファイル・システム](./assets/system-storage-config-media.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [メディアデータベースを使用](../../content-design/media-storage-database.md) （内） _コンテンツおよびデザインガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Media Storage] | グローバル | メディアファイルの保存に使用する方法を決定します。 デフォルト設定： `File System` |
| [!UICONTROL Environment Update Time] | グローバル | メディアファイル環境の更新頻度を秒単位で決定します。 デフォルト値： `3600` |

{style="table-layout:auto"}

![詳細設定 — メディアのストレージ設定 — データベース](./assets/database-storage-deprecated.png)<!-- zoom -->

>[!IMPORTANT]
>
>データベースメディアストレージ方法は、Adobe CommerceおよびMagento Open Source2.4.3 で廃止されました。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Media Storage] | グローバル | メディアファイルの保存に使用する方法として、データベースを指定します。 |
| [!UICONTROL Select Media Database] | グローバル | メディアストレージに使用されるデータベースの名前を示します。 デフォルト設定： `default_setup` |
| [!UICONTROL Synchronize] |  | 指定したデータベースの場所にすべてのメディアの転送を同期します。 |
| 環境の更新時間 | グローバル | メディアファイル環境の更新頻度を秒単位で決定します。 デフォルト値： `3600` |

{style="table-layout:auto"}

## [!UICONTROL Bulk Actions]

{{ee-feature}}

![高度な設定 — 一括アクション](./assets/system-bulk-actions.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [バルクアクション](../../systems/action-log-bulk-actions.md) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Days Saved in Log] | グローバル | バルクアクションが _バルクアクションログ_ アーカイブ。 デフォルト： `60` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import/Export File History Cleaning]

{{ee-feature}}

![高度な設定 — スケジュールされたインポート/エクスポートファイル履歴のクリーニング](./assets/system-schedule-history-cleaning.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [予定されているインポートおよびエクスポート](../../systems/data-scheduled-import-export.md) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Save File, Days] | グローバル | 履歴ファイルのインポート/エクスポートが保存される日数を決定します。 |
| [!UICONTROL Enable Scheduled File History Cleaning] | グローバル | インポート/エクスポートファイルのスケジュールされたファイルのクリーンアップを有効にします。 オプション： `Yes` / `No` |
| [!UICONTROL Clean Now] |  | スケジュールされたクリーンアップを上書きし、インポート/エクスポート履歴ファイルを直ちにクリーンアップします。 |
| [!UICONTROL Start Time] | グローバル | インポート/エクスポート履歴ファイルのクリーンアップの時間、分、秒を指定します。 |
| [!UICONTROL Frequency] | グローバル | インポート/エクスポート履歴ファイルをクリーンアップする頻度を決定します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | グローバル | インポート/エクスポートファイル履歴の消去中にエラーが発生した場合に通知を受け取る人の電子メールアドレス。 複数のアドレスを指定する場合は、コンマで区切ります。 |
| [!UICONTROL Error Email Sender] | グローバル | 通知の送信者として表示されるストアの連絡先を識別します。 デフォルトの送信者： `General Contact` |
| [!UICONTROL Error Email Template] | グローバル | インポート/エクスポートファイルのクリーニングエラー通知に使用する電子メールテンプレートを識別します。 デフォルトのテンプレート： `File History Clean Failed` |

{style="table-layout:auto"}

## [!UICONTROL Image Upload Configuration]

![高度な設定 — 画像のアップロード設定](./assets/system-image-upload-configuration.png)<!-- zoom -->

<!-- [Image Upload Configuration](https://docs.magento.com/user-guide/system/action-log-bulk-actions.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Quality] | グローバル | サイズ変更されたJPGの画像の画質を指定します。 低い品質を指定すると、ファイルサイズが小さくなります。 80 ～ 90 %を使用して、高品質でファイルサイズを削減します。 デフォルト： `80` |
| [!UICONTROL Enable Frontend Resize] | グローバル | この設定を有効にすると、Commerce で、大きくて大きすぎるサイズの画像のサイズを変更し、 _製品の詳細_ ページに貼り付けます。 Commerce は、ファイルをアップロードする前に、JavaScript を使用して画像ファイルのサイズを変更します。 画像のサイズが変更された場合、画像は正確な比率を維持し、「最大の幅」または「最大の高さ」の最大サイズを超えないようにします。 デフォルト： `Yes` |
| [!UICONTROL Maximum Width] | グローバル | 画像の最大ピクセル幅を決定します。 画像のサイズが変更されても、この幅を超えることはありません。 デフォルト： `1920` |
| [!UICONTROL Maximum Height] | グローバル | 画像の最大ピクセル高を決定します。 画像のサイズが変更されても、この高さを超えることはありません。 デフォルト： `1200` |

{style="table-layout:auto"}

## [!UICONTROL Media Gallery]

![詳細設定 — メディアギャラリー](./assets/system-media-gallery.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Old Media Gallery] | グローバル | 古いメディアギャラリーを有効または無効にします。 |

{style="table-layout:auto"}

## [!UICONTROL Media Gallery Image Optimization]

![高度な設定 — メディアギャラリーの画像の最適化](./assets/system-media-image-optimization.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Image Optimization] | グローバル | コンテンツに挿入される画像のファイルサイズを小さくするように画像をサイズ変更するかどうかを指定します。 元の画像はメディアギャラリーに保持されます。 |
| [!UICONTROL Maximum Width] | グローバル | メディアギャラリーからコンテンツに挿入される画像の最大幅（ピクセル単位）です。 |
| [!UICONTROL Maximum Height] | グローバル | メディアギャラリーからコンテンツに挿入される画像の最大の高さ（ピクセル単位）です。 |

{style="table-layout:auto"}

## [!UICONTROL Adobe Stock Integration]

![高度な設定 — Adobe Stock統合](./assets/system-adobe-stock-integration.png)<!-- zoom -->

これらの設定について詳しくは、 [Adobe Stock統合](../../content-design/adobe-stock.md) （内） _コンテンツおよびデザインガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled Adobe Stock] | グローバル | Adobe Stock統合を有効または無効にします。 |
| [!UICONTROL API Key (Client ID)] | グローバル | ストアをAdobe Stockサービスに接続するには、API キーが必要です。 |
| [!UICONTROL Client Secret] | グローバル | Adobe Stock統合用のクライアント秘密鍵が必要です。 |
| [!UICONTROL Test Connection] |  | API キーがAdobe Stockサービスでの使用に有効であることを確認するためのテストを実行します。 |

{style="table-layout:auto"}
