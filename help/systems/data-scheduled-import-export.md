---
title: スケジュールされた読み込みと書き出し
description: スケジュールされたデータのインポートおよびエクスポート操作を管理する方法について説明します。
exl-id: 74ba40f1-a540-4425-9500-2c730c1145e7
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2378'
ht-degree: 0%

---

# スケジュールされた読み込みと書き出し

{{ee-feature}}

スケジュールされた読み込みと書き出しは、日単位、週単位または月単位で実行できます。 インポートまたはエクスポートするファイルは、ローカルのAdobe Commerce サーバーまたはリモート FTP サーバーに置くことができます。 スケジュールされたインポート/エクスポートはデフォルトで実装されており、追加の設定は必要ありません。 スケジュールされたすべてのインポートとエクスポートは、Cron ジョブスケジューラーによって管理されます。

## スケジュールされたインポート/エクスポートへのアクセス

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Scheduled Imports/Exports]**に移動します。

   ![ スケジュールされたデータのインポート/エクスポート ](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. 新しいスケジュール済みインポートまたはエクスポートジョブを作成するには、該当するボタンをクリックし、スケジュール済みジョブのタイプの指示に従います。

   - [スケジュール済み書き出しを追加](#schedule-an-export)
   - [スケジュールされた読み込みを追加](#schedule-an-import)

1. レコードを保存すると、ジョブが _[!UICONTROL Scheduled Import/Export]_グリッドに表示されます。

   >[!NOTE]
   >
   >スケジュールされたインポート/エクスポートを作成または更新すると、システム設定が変更されます。 保存後、管理ページの上部に表示されるキャッシュ無効化通知に対処し、キャッシュをフラッシュして、新しいスケジュールまたは更新されたスケジュールを適用してください。

1. スケジュールされた各ジョブの後、ファイルのコピーがAdobe Commerce ローカルサーバーの `var/log/import_export` ディレクトリに配置されます。

   各操作の詳細はログには書き込まれません。 エラーが発生した場合は、失敗したインポート/エクスポートジョブの通知が、エラーの説明と共に送信されます。

## 読み込みのスケジュール

使用可能なインポートファイル形式およびインポートエンティティのタイプの場合、スケジュールされたインポートプロセスは手動インポートプロセスに類似しています。

- 読み込みファイルは.CSV 形式にする必要があります。
- 製品および顧客データを読み込むことができます

スケジュール設定されたインポートを使用する利点は、インポート パラメータを指定した後にデータ ファイルを自動的に複数回インポートし、1 回だけスケジュールできることです。

各インポート操作の詳細はログに書き込まれませんが、エラーが発生した場合は、エラーの説明を記載した _インポートに失敗しました_ メールが届きます。 最後にスケジュールされた読み込みジョブの結果は、スケジュールされた読み込み/書き出しページの最後の結果列に表示されます。

インポート操作のたびに、Adobe CommerceまたはMagento Open Sourceがデプロイされているサーバー上の `var/log/import_export` ディレクトリにインポートファイルのコピーが配置されます。 タイムスタンプ、読み込まれたエンティティ（製品または顧客）のマーカー、操作のタイプ（この場合は import）がインポートファイル名に追加されます。

スケジュールされた各インポートジョブの後、再インデックス操作が自動的に実行されます。 フロントエンドでは、記述などのテキスト情報の変更は更新されたデータがデータベースに送信された後に反映され、価格の変更は再インデックス操作の後にのみ反映されます。

### 手順 1：読み込み設定の完了

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Scheduled Import/Export]**に移動します。

1. 右上隅の「**[!UICONTROL Add Scheduled Import]**」をクリックします。

1. スケジュールと読み込みのオプションを設定します。

   - 「**[!UICONTROL Name]**」 – スケジュールされたインポートの名前を入力します。

   - **[!UICONTROL Description]** – 読み込みの目的と使用方法を説明する簡単な説明を入力します。

   - 「**[!UICONTROL Entity Type]**」 – 次のいずれかに設定します。

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - 「**[!UICONTROL Import Behavior]**」 – 次のいずれかに設定します。

      - `Add/Update Complex Data` - データベース内の既存のエントリの既存の複合データに対して、新しい複合データを追加または更新します。 これがデフォルト値です。
      - `Replace` - データベース内の既存のエンティティの既存の複合に上書きします。
      - `Delete Entities` - データベース内の既存のエントリを削除します。
      - `Custom Action` - データベース内の既存のエンティティをカスタマイズします。

     >[!NOTE]
     >
     >_[!UICONTROL Advanced Pricing]_、_[!UICONTROL Products]_、_[!UICONTROL Customers and Addresses (single file)]_および_[!UICONTROL Stock Sources]_ エンティティタイプの場合、`Add/Update`、`Replace` および `Delete` の読み込み動作が表示されます。 _顧客の財務_、_顧客のメイン ファイル_、および _顧客とアドレス_ エンティティ タイプの場合、`Add/Update Complex Data`、`Delete Entities`、および `Custom Action` のインポート動作が表示されます。

   - **[!UICONTROL Start Time]**：読み込みの開始がスケジュールされている時間、分、および秒に設定します。

   - **[!UICONTROL Frequency]** — `Daily`、`Weekly`、`Monthly` のいずれかに設定します。

   - **[!UICONTROL On Error]** - `Stop Import` または `Continue Processing` のいずれかに設定します。

   - **[!UICONTROL Status]**：スケジュールされたインポートをアクティブにするには、`Enabled` に設定します。

   - 「**[!UICONTROL Field Separator]**」 – インポートファイル内のフィールドの区切りに使用する文字を入力します。 デフォルトの文字はコンマです。

   - 「**[!UICONTROL Multiple Value Separator]**」 – フィールド内で複数の値を区切るために使用する文字を入力します。

   ![ データのインポート – スケジュールされたインポート設定 ](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### 手順 2：インポートファイル情報の完了

1. **[!UICONTROL Server Type]** を次のいずれかに設定します。

   - `Local Server` - Adobe Commerceがインストールされているのと同じサーバーからデータをインポートします。
   - `Remote FTP` - リモートサーバーからデータをインポートします。

   ![ データのインポート – スケジュールされたインポート ファイル情報 ](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >リモート記憶域モジュールが有効になると、`Local Server` は自動的に `Remote Storage` に切り替わります。

1. インポート ファイルの作成元の **[!UICONTROL File Directory]** を入力してください。

   - `Local Server` - Commerce インストール内の相対パスを入力します。 例：`var/import`。 リモートストレージモジュールが設定されている場合は、`import_export/import` を使用します。
   - `Remote FTP server` - リモートサーバー上のインポートフォルダーの完全な URL とパスを入力します。

1. インポートする **[!UICONTROL File Name]** を入力してください

1. **[!UICONTROL Images File Directory]**：製品画像が保存されているディレクトリのパスを入力します。

   ローカルサーバーで、`var/import` のような相対パスを入力します。 リモートストレージで、`import_export/import` または `import_export/import/some/dir` などの相対パスを入力します。

### 手順 3：読み込みに失敗したメールの設定

![ データの読み込み – 読み込みに失敗したため、メールが失敗しました ](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. 読み込み中にエラーが発生した場合に通知を受け取るストアの連絡先に **[!UICONTROL Failed Email Receiver]** を設定します。

1. 通知の送信者として表示されるストアの連絡先に **[!UICONTROL Failed Email Sender]** を設定します。

1. 通知に使用するテンプレートに **[!UICONTROL Failed Email Template]** を設定します。

1. **[!UICONTROL Send Failed Email Copy To]**：通知のコピーを受信するユーザーのメールアドレスを入力します。

   複数のメールアドレスを指定する場合はコンマで区切ります。

1. **[!UICONTROL Failed Email Copy Method]** を次のいずれかに設定します。

   - `Bcc` – 失敗した読み込み通知のブラインドコピーを送信します。 受信者の名前とアドレスは元のメール配信に含まれますが、非表示になります。
   - `Separate Email` – 失敗した読み込み通知のコピーを別のメールとして送信します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   新しいスケジュール済みインポートジョブが _[!UICONTROL Scheduled Import/Export]_ページのリストに追加されます。 このページからすぐに実行してテストし、編集できます。 インポートファイルは、各インポートジョブの実行前に検証されます。

>[!NOTE]
>
>スケジュールされたインポート/エクスポートを作成または更新すると、システム設定が変更されます。 保存後、管理ページの上部に表示されるキャッシュ無効化通知に対処し、キャッシュをフラッシュして、新しいスケジュールまたは更新されたスケジュールを適用してください。

### フィールドの説明

#### [!UICONTROL Import Settings]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Name] | 読み込みの名前。 スケジュールされた読み込みが異なる多数の読み込みが作成される場合に区別するのに役立ちます。 |
| [!UICONTROL Description] | （オプション）説明を入力できます。 |
| [!UICONTROL Entity Type] | インポートするデータを定義します。 |
| [!UICONTROL Import Behavior] | インポートするエンティティがデータベース内に存在する場合の、複雑なデータの処理方法を定義します。 製品の複雑なデータには、カテゴリ、web サイト、カスタムオプション、階層価格、関連製品、アップセル、クロスセル、関連製品データが含まれます。 顧客の複雑なデータにはアドレスが含まれます。 オプション：<br>**[!UICONTROL Add/Update Complex Data]**– 新しい複合データが、データベース内の既存のエントリの既存の複合データに追加または更新されます。 これがデフォルト値です。<br>**[!UICONTROL Add/Update]** – 新しいデータがデータベース内の既存のエントリに追加されます。 製品の場合、`sku` 以外のすべてのフィールドを更新できます。 CSV ファイルにリストされていない複数のフィールド値（カテゴリや web サイトなど）は、読み込み後もデータベースに残ります。<br>**[!UICONTROL Replace]**– 既存のエンティティの既存の複合データが置き換えられます。<br>**[!UICONTROL Delete Entities]** - インポートされたエンティティがデータベースに存在する場合、データベースから削除されます。<br>**[!UICONTROL Custom Action]**– 既存の複合エンティティは、読み込みプロセス中にカスタマイズされます。 |
| [!UICONTROL Start Time] | 読み込みの開始時刻（時、分、秒）を設定します。 |
| [!UICONTROL Frequency] | 読み込みの実行頻度を定義します。 オプション：`Daily`/`Weekly`/`Monthly` |
| [!UICONTROL On Error] | ファイル検証中にエラーが見つかった場合のシステム動作を定義します。 Options:<br>**Stop Import** – 検証中にエラーが見つかった場合、ファイルはインポートされません。 これがデフォルト値です。<br>**処理を続行** – 検証中にエラーが見つかったがインポートが可能な場合、ファイルがインポートされます。 |
| [!UICONTROL Status] | 読み込みはデフォルトで有効になっています。 ステータスを `Disabled` に設定すると、ワークフローを休止できます。 |
| [!UICONTROL Field Separator] | フィールドの区切りに使用する文字を指定します。 デフォルト値：`,` （コンマ） |
| [!UICONTROL Multiple Value Separator] | フィールド内の複数の値を区切るために使用する文字を指定します。 デフォルト値：`,` （コンマ） |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Commerceがデプロイされているサーバーと同じサーバー上のファイル（`Local Server` を選択）またはリモート FTP サーバーからインポート（`Remote FTP` を選択）できます。 _[!UICONTROL Remote FTP]_を選択すると、資格情報とファイル転送設定の追加オプションが表示されます。 リモート・ストレージ・モジュールが有効な場合、`Local Server` のタイプは自動的に `Remote Storage` に切り替わります。 |
| [!UICONTROL File Directory] | インポート ファイルがあるディレクトリを指定してください。 「サーバータイプ」が「_[!UICONTROL Local Server]_」に設定されている場合は、Commerce インストールディレクトリを基準とした相対パスを指定します。 例：リモートストレージの場合は `var/import` または `import_export/import`。 |
| [!UICONTROL File Name] | 読み込みファイルの名前を指定します。 |
| [!UICONTROL Images File Directory] | 製品画像が保存されているディレクトリのパスを入力します。 ローカルサーバーには、相対パスを入力します。 例：リモートストレージの場合は `var/import` または `import_export/import`。 |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | 読み込みが失敗した場合にメール通知（読み込みに失敗したメール）を送信するメールアドレスを指定します。 |
| [!UICONTROL Failed Email Sender] | 読み込みに失敗したメールの送信者として使用するメールアドレスを指定します。 |
| [!UICONTROL Failed Email Template] | インポートに失敗したメールのテンプレートを選択します。 デフォルトでは、「読み込みに失敗しました（ロケールからのデフォルトテンプレート）」オプションのみ使用できます。 カスタムテンプレートは、_[!UICONTROL System]_/_[!UICONTROL Transactional Emails]_ で作成できます。 |
| [!UICONTROL Send Failed Email Copy To] | 読み込みに失敗したメールのコピーの送信先のメールアドレス。 |
| [!UICONTROL Send Failed Email Copy Method] | 読み込みに失敗したメールのコピー送信方法を選択します。 |

{style="table-layout:auto"}

## 書き出しのスケジュール

スケジュールされた書き出しは、使用可能な書き出しファイル形式や書き出し可能なエンティティのタイプにおいて、手動の [ 書き出し ](data-export.md) に似ています。

- CSV 形式に書き出すことができます
- 製品および顧客データをエクスポートできます

スケジュールされた書き出しを使用する利点は、書き出しパラメーターを指定した後にデータを複数回、自動的に書き出すことができ、スケジュールは 1 回だけできることです。

各エクスポートの詳細はログに書き込まれませんが、エラーが発生した場合は、エラーの説明が記載されたエクスポート失敗のメールが届きます。 最後のエクスポートジョブの結果は、スケジュールされたインポート/エクスポートページの最後の結果列に表示されます。

各エクスポート後、エクスポートファイルはユーザー定義の場所に配置され、コピーはAdobe CommerceまたはMagento Open Sourceがデプロイされているサーバー上の `var/log/import_export` ディレクトリに配置されます。 エクスポートされたエンティティ（製品または顧客）のタイムスタンプとマーカー、および操作のタイプ（この場合はエクスポート）がエクスポートファイル名に追加されます。

### 手順 1：書き出し設定の完了

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Scheduled Import/Export]**に移動します。

1. 右上隅の「**[!UICONTROL Add Scheduled Export]**」をクリックして、次の操作を行います。

   - スケジュールされたエクスポートの **[!UICONTROL Name]** を入力します。

   - 書き出しの目的と使用方法を説明する簡単な **[!UICONTROL Description]** を入力します。

   - **[!UICONTROL Entity Type]** を次のいずれかに設定します。

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     ページ下部の _[!UICONTROL Entity Attributes]_のセクションが更新され、選択したエンティティタイプが反映されます。

   - 書き出しを開始するスケジュールの時、分、秒に **[!UICONTROL Start Time]** を設定します。

   - **[!UICONTROL Frequency]** を次のいずれかに設定します。

      - `Daily`
      - `Weekly`
      - `Monthly`

1. スケジュールされた書き出しを有効にするには、**[!UICONTROL Status]** を `Enabled` に設定します。

1. `CSV` をデフォルトの **[!UICONTROL File Format]** として使用します。

   ![ スケジュールされた書き出し設定 ](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### 手順 2：書き出しファイル情報の完了

1. **[!UICONTROL Server Type]** を次のいずれかに設定します。

   - `Local Server` - Commerceがインストールされているサーバーにエクスポートファイルを保存する
   - `Remote FTP` — エクスポート・ファイルをリモート・サーバに保存します。

   ![ スケジュールされた書き出しファイル情報 ](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >リモート記憶域モジュールが有効になると、`Local Server` は自動的に `Remote Storage` に切り替わります。

1. **[!UICONTROL File Directory]** に、次のようにエクスポートファイルを保存するディレクトリを入力します。

   - **[!UICONTROL Local Server]**:Commerce インストール内の相対パス（例：`var/export`）を入力します。 リモートストレージモジュールが設定されている場合は、`import_export/export` を使用します。
   - **[!UICONTROL Remote FTP server]**：宛先サーバーのターゲットフォルダーの完全な URL とパスを入力します。

1. _[!UICONTROL Remote FTP]_サーバーが選択されている場合は、そのサーバーへの接続資格情報を入力し、追加の設定を選択します。

   - **[!UICONTROL FTP Host[:Port]]**: リモート FTP ホスト・アドレスを入力します。
   - **[!UICONTROL User Name]**: リモート・サーバへのアクセスに使用するユーザー名を入力します。
   - **[!UICONTROL Password]**：指定したユーザー名アカウントのパスワードを入力します。
   - **[!UICONTROL File Mode]** の場合は、「`Binary`」または「`ASCII`」を選択します。
   - **[!UICONTROL Passive Mode]** の場合は、「`No`」または「`Yes`」を選択します。

### 手順 3：書き出し失敗メールの設定

1. 書き出し中にエラーが発生した場合に通知を受け取るストアの連絡先に **[!UICONTROL Failed Email Receiver]** を設定します。

1. 通知の送信者として表示されるストアの連絡先に **[!UICONTROL Failed Email Sender]** を設定します。

1. 通知に使用するテンプレートに **[!UICONTROL Failed Email Template]** を設定します。

1. **[!UICONTROL Send Failed Email Copy To]**：通知のコピーを受信するユーザーのメールアドレスを入力します。

   複数のメールアドレスの場合は、コンマで区切ります。

1. **[!UICONTROL Failed Email Copy Method]** を次のいずれかに設定します。

   - `Bcc` - ブラインドの表敬用コピーを送信します。 受信者の名前とアドレスは元のメール配信に含まれますが、表示されません。
   - `Separate Email` - コピーを別のメールとして送信します。

### 手順 4：エンティティ属性の選択

1. _[!UICONTROL Entity Attributes]_セクションで、エクスポート データに含める属性を選択します。

   - 書き出しデータを属性値でフィルタリングするには、_[!UICONTROL Filter]_列に属性値を入力します。
   - 特定の属性値を持つ製品または顧客を除外するには、除外する属性の値を入力し、「スキップ」列のチェックボックスを選択します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   新しいスケジュールされた書き出しジョブが _[!UICONTROL Scheduled Import/Export]_ページのリストに追加されます。 このページから、テスト用にすぐに実行し、編集できます。

>[!NOTE]
>
>スケジュールされたインポート/エクスポートを作成または更新すると、システム設定が変更されます。 保存後、管理ページの上部に表示されるキャッシュ無効化通知に対処し、キャッシュをフラッシュして、新しいスケジュールまたは更新されたスケジュールを適用してください。

### フィールドの説明

#### [!UICONTROL Export Settings]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Name] | エクスポートの名前。 スケジュールされた書き出しが異なる多数の書き出しが作成される場合に、書き出しを区別するのに役立ちます。 |
| [!UICONTROL Description] | （任意）スケジュールされた書き出しの説明。 |
| [!UICONTROL Entity Type] | 書き出すデータを識別します。 選択後、エンティティ属性が下に表示されます。 オプション：`Advanced Pricing` / `Products` / `Customer Finances` / `Customers Main File` / `Customer Addresses` / `Stock Sources` |
| [!UICONTROL Start Time] | 書き出しの開始時刻（時、分、秒）を設定します。 |
| [!UICONTROL Frequency] | エクスポートジョブの実行頻度を定義します。 オプション：`Daily`/`Weekly`/`Monthly` |
| [!UICONTROL Status] | 新しいスケジュール済み書き出しは、デフォルトで有効になっています。 ステータスを無効に設定すると、ワークフローを中断できます。 オプション：`Enabled` / `Disabled` |
| [!UICONTROL File Format] | エクスポートファイルの形式を選択します。 現在、`.CSV` オプションのみが使用可能です。 |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Server Type] | 書き出しファイルの場所を決定します。 Options:<br>**Local Server** - Commerceがデプロイされているサーバーにエクスポートファイルを配置します。 リモート・ストレージ・モジュールが有効な場合、`Local Server` は `Remote Storage` に切り替わります。<br>**リモート FTP** - エクスポート・ファイルをリモート・サーバに配置します。 資格情報とファイル転送設定の追加オプションが表示されます。 |
| [!UICONTROL File Directory] | エクスポートファイルを配置するディレクトリを指定します。 _[!UICONTROL Server Type]_が `Local Server` に設定されている場合は、Commerceのインストールパスを基準とした相対パスを指定します。 例えば、リモートストレージの場合は `var/export` や `import_export/export` です。 |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | 書き出しが失敗した場合にメール通知（書き出しに失敗したメール）を送信するメールアドレスを指定します。 |
| [!UICONTROL Failed Email Sender] | エクスポートに失敗したメールの送信者として使用するメールアドレスを指定します。 |
| [!UICONTROL Failed Email Template] | 失敗した書き出しメールのテンプレートを選択します。 デフォルトでは、`Export Failed (Default Template from Locale)` オプションのみ使用できます。 |
| [!UICONTROL Send Failed Email Copy To] | 失敗した書き出しメールのコピーの送信先のメールアドレス。 |
| [!UICONTROL Send Failed Email Copy Method] | エクスポートに失敗したメールのコピー送信方法を指定します。 |

{style="table-layout:auto"}
