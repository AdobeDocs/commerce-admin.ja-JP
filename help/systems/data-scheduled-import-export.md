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

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Imports/Exports]**.

   ![スケジュールされたデータのインポート/エクスポート](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. 新しいスケジュール済みインポートまたはエクスポートジョブを作成するには、該当するボタンをクリックし、スケジュール済みジョブのタイプの指示に従います。

   - [スケジュール済み書き出しを追加](#schedule-an-export)
   - [スケジュールされた読み込みを追加](#schedule-an-import)

1. レコードを保存すると、ジョブがに表示されます _[!UICONTROL Scheduled Import/Export]_グリッド。

   >[!NOTE]
   >
   >スケジュールされたインポート/エクスポートを作成または更新すると、システム設定が変更されます。 保存後、管理ページの上部に表示されるキャッシュ無効化通知に対処し、キャッシュをフラッシュして、新しいスケジュールまたは更新されたスケジュールを適用してください。

1. スケジュールされた各ジョブの後に、ファイルのコピーが `var/log/import_export` Adobe Commerce ローカルサーバー上のディレクトリ。

   各操作の詳細はログには書き込まれません。 エラーが発生した場合は、失敗したインポート/エクスポートジョブの通知が、エラーの説明と共に送信されます。

## 読み込みのスケジュール

使用可能なインポートファイル形式およびインポートエンティティのタイプの場合、スケジュールされたインポートプロセスは手動インポートプロセスに類似しています。

- 読み込みファイルは.CSV 形式にする必要があります。
- 製品および顧客データを読み込むことができます

スケジュール設定されたインポートを使用する利点は、インポート パラメータを指定した後にデータ ファイルを自動的に複数回インポートし、1 回だけスケジュールできることです。

各インポート操作の詳細はログに書き込まれませんが、エラーが発生した場合は、 _インポートに失敗しました_ エラーの説明を記載したメール。 最後にスケジュールされた読み込みジョブの結果は、スケジュールされた読み込み/書き出しページの最後の結果列に表示されます。

インポート操作のたびに、インポートファイルのコピーがに配置されます。 `var/log/import_export` Adobe CommerceまたはMagento Open Sourceがデプロイされているサーバー上のディレクトリ。 タイムスタンプ、読み込まれたエンティティ（製品または顧客）のマーカー、操作のタイプ（この場合は import）がインポートファイル名に追加されます。

スケジュールされた各インポートジョブの後、再インデックス操作が自動的に実行されます。 フロントエンドでは、記述などのテキスト情報の変更は更新されたデータがデータベースに送信された後に反映され、価格の変更は再インデックス操作の後にのみ反映されます。

### 手順 1：読み込み設定の完了

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Scheduled Import]**.

1. スケジュールと読み込みのオプションを設定します。

   - **[!UICONTROL Name]** — スケジュールされたインポートの名前を入力します。

   - **[!UICONTROL Description]**  – 読み込みの目的と使用方法を説明する簡単な説明を入力します。

   - **[!UICONTROL Entity Type]**  – 次のいずれかに設定します。

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - **[!UICONTROL Import Behavior]**  – 次のいずれかに設定します。

      - `Add/Update Complex Data` - データベース内の既存のエントリの既存の複合データに対して、新しい複合データを追加または更新します。 これがデフォルト値です。
      - `Replace` — データベース内の既存のエンティティの既存の複合に上書きします。
      - `Delete Entities` — データベース内の既存のエントリを削除します。
      - `Custom Action` - データベース内の既存のエンティティをカスタマイズします。

     >[!NOTE]
     >
     >の場合 _[!UICONTROL Advanced Pricing]_,_[!UICONTROL Products]_, _[!UICONTROL Customers and Addresses (single file)]_、および_[!UICONTROL Stock Sources]_ エンティティタイプの場合、次のインポート動作が表示されます。 `Add/Update`, `Replace`、および `Delete`. の場合 _顧客の財務_, _顧客のメインファイル_、および _顧客と住所_ エンティティタイプの場合、次のインポート動作が表示されます。 `Add/Update Complex Data`, `Delete Entities`、および `Custom Action`.

   - **[!UICONTROL Start Time]**  – 読み込みを開始するようにスケジュールされている時間、分、および秒に設定します。

   - **[!UICONTROL Frequency]**  – 次のいずれかに設定します。 `Daily`, `Weekly`、または `Monthly`

   - **[!UICONTROL On Error]**  – 次のいずれかに設定します。 `Stop Import` または `Continue Processing`

   - **[!UICONTROL Status]** — スケジュールされたインポートをアクティブにするには、をに設定します。 `Enabled`.

   - **[!UICONTROL Field Separator]** - インポートファイル内のフィールドの区切りに使用する文字を入力します。 デフォルトの文字はコンマです。

   - **[!UICONTROL Multiple Value Separator]** - フィールド内で複数の値を区切るために使用する文字を入力します。

   ![データの読み込み – スケジュールされた読み込み設定](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### 手順 2：インポートファイル情報の完了

1. を設定 **[!UICONTROL Server Type]** を次のいずれかに変更します。

   - `Local Server` - Adobe Commerceがインストールされているサーバーと同じサーバーからデータをインポートします。
   - `Remote FTP` - リモートサーバーからデータをインポートします。

   ![データのインポート – スケジュールされたインポート ファイル情報](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >リモート記憶域モジュールが有効な場合、 `Local Server` 自動的にに切り替え `Remote Storage`.

1. を入力 **[!UICONTROL File Directory]** 読み込みファイルの作成元。

   - `Local Server` - Commerceのインストール環境での相対パスを入力します。 例： `var/import`. リモートストレージモジュールが設定されている場合は、を使用します。 `import_export/import`.
   - `Remote FTP server` - リモート サーバー上のインポート フォルダーの完全な URL とパスを入力します。

1. を入力 **[!UICONTROL File Name]** をインポートします。

1. の場合 **[!UICONTROL Images File Directory]**&#x200B;製品画像が保存されているディレクトリのパスを入力します。

   ローカルサーバーで、次のように相対パスを入力します。 `var/import`. リモートストレージで、次のような相対パスを入力します。 `import_export/import` または `import_export/import/some/dir`.

### 手順 3：読み込みに失敗したメールの設定

![データのインポート – 失敗したインポート失敗メール](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Failed Email Receiver]** インポート中にエラーが発生した場合に通知を受け取るストアの連絡先に送信します。

1. を設定 **[!UICONTROL Failed Email Sender]** 通知の送信者として表示される店舗連絡先に送信されます。

1. を設定 **[!UICONTROL Failed Email Template]** 通知に使用されるテンプレート。

1. の場合 **[!UICONTROL Send Failed Email Copy To]**&#x200B;に、通知のコピーを受信するユーザーのメールアドレスを入力します。

   複数のメールアドレスを指定する場合はコンマで区切ります。

1. を設定 **[!UICONTROL Failed Email Copy Method]** を次のいずれかに変更します。

   - `Bcc`  – 失敗したインポート通知の詳細なコピーを送信します。 受信者の名前とアドレスは元のメール配信に含まれますが、非表示になります。
   - `Separate Email`  – 失敗した読み込み通知のコピーを別のメールとして送信します。

1. 完了したら、 **[!UICONTROL Save]**.

   新しいスケジュールされたインポートジョブがリスト _[!UICONTROL Scheduled Import/Export]_ページ。 このページからすぐに実行してテストし、編集できます。 インポートファイルは、各インポートジョブの実行前に検証されます。

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
| [!UICONTROL Import Behavior] | インポートするエンティティがデータベース内に存在する場合の、複雑なデータの処理方法を定義します。 製品の複雑なデータには、カテゴリ、web サイト、カスタムオプション、階層価格、関連製品、アップセル、クロスセル、関連製品データが含まれます。 顧客の複雑なデータにはアドレスが含まれます。 オプション：<br>**[!UICONTROL Add/Update Complex Data]**– 新しい複合データが、データベース内の既存のエントリの既存の複合データに追加または更新されます。 これがデフォルト値です。<br>**[!UICONTROL Add/Update]**  – 新しいデータがデータベース内の既存のエントリに追加されます。 を除くすべてのフィールド `sku` 製品に関して更新可能です。 CSV ファイルにリストされていない複数のフィールド値（カテゴリや web サイトなど）は、読み込み後もデータベースに残ります。<br>**[!UICONTROL Replace]**– 既存のエンティティの既存の複合データが置き換えられます。<br>**[!UICONTROL Delete Entities]** - インポートされたエンティティがデータベースに存在する場合、データベースから削除されます。<br>**[!UICONTROL Custom Action]**– 既存の複合エンティティは、読み込みプロセス中にカスタマイズされます。 |
| [!UICONTROL Start Time] | 読み込みの開始時刻（時、分、秒）を設定します。 |
| [!UICONTROL Frequency] | 読み込みの実行頻度を定義します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL On Error] | ファイル検証中にエラーが見つかった場合のシステム動作を定義します。 オプション：<br>**読み込みを停止**  – 検証中にエラーが見つかった場合、ファイルはインポートされません。 これがデフォルト値です。<br>**処理を続行**  – 検証中にエラーが見つかったが、インポートが可能な場合、ファイルがインポートされます。 |
| [!UICONTROL Status] | 読み込みはデフォルトで有効になっています。 ステータスをに設定すると、ワークフローを中断できます。 `Disabled`. |
| [!UICONTROL Field Separator] | フィールドの区切りに使用する文字を指定します。 デフォルト値 `,` （コンマ） |
| [!UICONTROL Multiple Value Separator] | フィールド内の複数の値を区切るために使用する文字を指定します。 デフォルト値 `,` （コンマ） |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Commerceがデプロイされているのと同じサーバー上のファイルから読み込むことができます（ `Local Server`）またはリモート FTP サーバーから（ `Remote FTP`）に設定します。 を選択する場合 _[!UICONTROL Remote FTP]_に変わり、資格情報とファイル転送設定の追加オプションが表示されます。 リモートストレージモジュールが有効になっている場合、 `Local Server` タイプは自動的にに切り替わります `Remote Storage`. |
| [!UICONTROL File Directory] | インポート ファイルがあるディレクトリを指定してください。 サーバーの種類がに設定されている場合 _[!UICONTROL Local Server]_を選択し、Commerce インストールディレクトリへの相対パスを指定します。 例： `var/import` または `import_export/import` （リモートストレージの場合）。 |
| [!UICONTROL File Name] | 読み込みファイルの名前を指定します。 |
| [!UICONTROL Images File Directory] | 製品画像が保存されているディレクトリのパスを入力します。 ローカルサーバーには、相対パスを入力します。 例： `var/import` または `import_export/import` （リモートストレージの場合）。 |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | 読み込みが失敗した場合にメール通知（読み込みに失敗したメール）を送信するメールアドレスを指定します。 |
| [!UICONTROL Failed Email Sender] | 読み込みに失敗したメールの送信者として使用するメールアドレスを指定します。 |
| [!UICONTROL Failed Email Template] | インポートに失敗したメールのテンプレートを選択します。 デフォルトでは、「読み込みに失敗しました（ロケールからのデフォルトテンプレート）」オプションのみ使用できます。 カスタムテンプレートは次の場所で作成できます _[!UICONTROL System]_>_[!UICONTROL Transactional Emails]_. |
| [!UICONTROL Send Failed Email Copy To] | 読み込みに失敗したメールのコピーの送信先のメールアドレス。 |
| [!UICONTROL Send Failed Email Copy Method] | 読み込みに失敗したメールのコピー送信方法を選択します。 |

{style="table-layout:auto"}

## 書き出しのスケジュール

スケジュールされた書き出しは、手動に似ています [Export](data-export.md) 使用可能なエクスポートファイル形式と、エクスポート可能なエンティティのタイプで以下を行います。

- CSV 形式に書き出すことができます
- 製品および顧客データをエクスポートできます

スケジュールされた書き出しを使用する利点は、書き出しパラメーターを指定した後にデータを複数回、自動的に書き出すことができ、スケジュールは 1 回だけできることです。

各エクスポートの詳細はログに書き込まれませんが、エラーが発生した場合は、エラーの説明が記載されたエクスポート失敗のメールが届きます。 最後のエクスポートジョブの結果は、スケジュールされたインポート/エクスポートページの最後の結果列に表示されます。

エクスポートのたびに、エクスポートファイルはユーザー定義の場所に配置され、コピーはに配置されます。 `var/log/import_export` Adobe CommerceまたはMagento Open Sourceがデプロイされているサーバー上のディレクトリ。 エクスポートされたエンティティ（製品または顧客）のタイムスタンプとマーカー、および操作のタイプ（この場合はエクスポート）がエクスポートファイル名に追加されます。

### 手順 1：書き出し設定の完了

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Scheduled Export]** 次の手順を実行します。

   - を入力 **[!UICONTROL Name]** スケジュールされた書き出し用。

   - 概要を入力 **[!UICONTROL Description]** 書き出しの目的と使用方法について説明します。

   - を設定 **[!UICONTROL Entity Type]** を次のいずれかに変更します。

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     この _[!UICONTROL Entity Attributes]_ページの下部のセクションが更新され、選択したエンティティタイプが反映されます。

   - を設定 **[!UICONTROL Start Time]** エクスポートを開始するスケジュールの時、分、および秒。

   - を設定 **[!UICONTROL Frequency]** を次のいずれかに変更します。

      - `Daily`
      - `Weekly`
      - `Monthly`

1. スケジュールされた書き出しを有効にするには、次を設定します **[!UICONTROL Status]** 対象： `Enabled`.

1. 承諾 `CSV` デフォルトとして **[!UICONTROL File Format]**.

   ![スケジュールされた書き出し設定](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### 手順 2：書き出しファイル情報の完了

1. を設定 **[!UICONTROL Server Type]** を次のいずれかに変更します。

   - `Local Server` - Commerceがインストールされているサーバーにエクスポートファイルを保存する
   - `Remote FTP` — エクスポート・ファイルをリモート・サーバに保存します。

   ![スケジュールされた書き出しファイル情報](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >リモートストレージモジュールが有効な場合、 `Local Server` 自動的にに切り替え `Remote Storage`.

1. の場合 **[!UICONTROL File Directory]**&#x200B;で、エクスポートファイルを保存するディレクトリを次のように入力します。

   - の場合 **[!UICONTROL Local Server]**&#x200B;を選択し、Commerceのインストール内の相対パス（例：）を入力します `var/export`. リモート・ストレージ・モジュールが構成されている場合は、 `import_export/export`.
   - の場合 **[!UICONTROL Remote FTP server]**&#x200B;に、宛先サーバー上のターゲットフォルダーの完全な URL とパスを入力します。

1. 次の場合 _[!UICONTROL Remote FTP]_「サーバー」を選択し、サーバーへの接続資格情報を入力して、追加の設定を選択します。

   - の場合 **[!UICONTROL FTP Host[:Port]]**&#x200B;にリモート FTP ホストアドレスを入力します。
   - の場合 **[!UICONTROL User Name]**&#x200B;に移動し、リモートサーバーへのアクセスに使用するユーザー名を入力します。
   - の場合 **[!UICONTROL Password]**&#x200B;に入力し、指定したユーザー名アカウントのパスワードを入力します。
   - の場合 **[!UICONTROL File Mode]**、を選択 `Binary` または `ASCII`.
   - の場合 **[!UICONTROL Passive Mode]**、を選択 `No` または `Yes`.

### 手順 3：書き出し失敗メールの設定

1. を設定 **[!UICONTROL Failed Email Receiver]** エクスポート中にエラーが発生した場合に通知を受け取るストアの連絡先に送信されます。

1. を設定 **[!UICONTROL Failed Email Sender]** 通知の送信者として表示される店舗連絡先に送信されます。

1. を設定 **[!UICONTROL Failed Email Template]** 通知に使用されるテンプレート。

1. の場合 **[!UICONTROL Send Failed Email Copy To]**&#x200B;に、通知のコピーを受信するユーザーのメールアドレスを入力します。

   複数のメールアドレスの場合は、コンマで区切ります。

1. を設定 **[!UICONTROL Failed Email Copy Method]** を次のいずれかに変更します。

   - `Bcc`  – 参考にならないコピーを送信します。 受信者の名前とアドレスは元のメール配信に含まれますが、表示されません。
   - `Separate Email` - コピーを別のメールとして送信します。

### 手順 4：エンティティ属性の選択

1. が含まれる _[!UICONTROL Entity Attributes]_セクションで、書き出しデータに含める属性を選択します。

   - 書き出しデータを属性値でフィルタリングするには、属性値を _[!UICONTROL Filter]_列。
   - 特定の属性値を持つ製品または顧客を除外するには、除外する属性の値を入力し、「スキップ」列のチェックボックスを選択します。

1. 完了したら、 **[!UICONTROL Save]**.

   新しいスケジュールされた書き出しジョブが _[!UICONTROL Scheduled Import/Export]_ページ。 このページから、テスト用にすぐに実行し、編集できます。

>[!NOTE]
>
>スケジュールされたインポート/エクスポートを作成または更新すると、システム設定が変更されます。 保存後、管理ページの上部に表示されるキャッシュ無効化通知に対処し、キャッシュをフラッシュして、新しいスケジュールまたは更新されたスケジュールを適用してください。

### フィールドの説明

#### [!UICONTROL Export Settings]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Name] | エクスポートの名前。 スケジュールされた書き出しが異なる多数の書き出しが作成される場合に、書き出しを区別するのに役立ちます。 |
| [!UICONTROL Description] | （任意）スケジュールされた書き出しの説明。 |
| [!UICONTROL Entity Type] | 書き出すデータを識別します。 選択後、エンティティ属性が下に表示されます。 オプション： `Advanced Pricing` / `Products` / `Customer Finances` / `Customers Main File` / `Customer Addresses` / `Stock Sources` |
| [!UICONTROL Start Time] | 書き出しの開始時刻（時、分、秒）を設定します。 |
| [!UICONTROL Frequency] | エクスポートジョブの実行頻度を定義します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Status] | 新しいスケジュール済み書き出しは、デフォルトで有効になっています。 ステータスを無効に設定すると、ワークフローを中断できます。 オプション： `Enabled` / `Disabled` |
| [!UICONTROL File Format] | エクスポートファイルの形式を選択します。 現在のみ `.CSV` オプションを利用できます。 |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Server Type] | 書き出しファイルの場所を決定します。 オプション：<br>**ローカルサーバー** - Commerceがデプロイされているサーバーと同じサーバーにエクスポートファイルを配置します。 リモートストレージモジュールが有効になっている場合、 `Local Server` がに切り替えられました `Remote Storage`.<br>**リモート FTP** — エクスポート・ファイルをリモート・サーバに配置します。 資格情報とファイル転送設定の追加オプションが表示されます。 |
| [!UICONTROL File Directory] | エクスポートファイルを配置するディレクトリを指定します。 Case _[!UICONTROL Server Type]_はに設定されています。 `Local Server`を選択し、Commerceのインストールパスを基準とした相対パスを指定します。 例： `var/export`、または `import_export/export` （リモートストレージの場合）。 |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | 書き出しが失敗した場合にメール通知（書き出しに失敗したメール）を送信するメールアドレスを指定します。 |
| [!UICONTROL Failed Email Sender] | エクスポートに失敗したメールの送信者として使用するメールアドレスを指定します。 |
| [!UICONTROL Failed Email Template] | 失敗した書き出しメールのテンプレートを選択します。 デフォルトでは、 `Export Failed (Default Template from Locale)` オプションを利用できます。 |
| [!UICONTROL Send Failed Email Copy To] | 失敗した書き出しメールのコピーの送信先のメールアドレス。 |
| [!UICONTROL Send Failed Email Copy Method] | エクスポートに失敗したメールのコピー送信方法を指定します。 |

{style="table-layout:auto"}
