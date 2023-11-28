---
title: 予定されているインポートおよびエクスポート
description: スケジュールされたデータのインポートおよびエクスポート操作を管理する方法について説明します。
exl-id: 74ba40f1-a540-4425-9500-2c730c1145e7
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2371'
ht-degree: 0%

---

# 予定されているインポートおよびエクスポート

{{ee-feature}}

予定されているインポートおよびエクスポートは、日単位、週単位、月単位で実行できます。 インポートまたはエクスポートするファイルは、ローカルのAdobe Commerceサーバー上またはリモートの FTP サーバー上に配置できます。 スケジュールされたインポート/エクスポートはデフォルトで実装され、追加の設定は必要ありません。 スケジュールされたすべてのインポートおよびエクスポートは、Cron ジョブスケジューラーで管理されます。

## 予定されているインポート/エクスポートにアクセス

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Imports/Exports]**.

   ![予定されているデータのインポート/エクスポート](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. 新しいスケジュール済みのインポートジョブまたはエクスポートジョブを作成するには、適切なボタンをクリックし、スケジュール済みジョブのタイプの指示に従います。

   - [予定書き出しの追加](#schedule-an-export)
   - [予定インポートの追加](#schedule-an-import)

1. レコードを保存すると、ジョブが _[!UICONTROL Scheduled Import/Export]_グリッド。

   >[!NOTE]
   >
   >スケジュールされたインポート/エクスポートを作成または更新すると、システム設定が変更されます。 保存後、管理ページの上部に表示されるキャッシュの無効化通知に必ず対処し、新しいスケジュールや更新されたスケジュールを適用するためにキャッシュをフラッシュします。

1. スケジュールされた各ジョブの後、ファイルのコピーが `var/log/import_export` Adobe Commerceローカルサーバー上のディレクトリ。

   各操作の詳細はログに書き込まれません。 エラーが発生した場合、エラーの説明と共に、失敗したインポート/エクスポートジョブに関する通知が送信されます。

## インポートのスケジュール設定

使用可能なインポート・ファイル・フォーマットおよびインポート・エンティティのタイプに関しては、予定インポート処理は手動インポート処理に似ています。

- インポートファイルは.CSV 形式にする必要があります
- 製品および顧客データをインポートできます

スケジュールされたインポートを使用する利点は、インポートパラメーターとスケジュールを 1 回だけ指定した後で、データファイルを複数回自動的にインポートできることです。

各インポート操作の詳細はログに書き込まれませんが、エラーが発生した場合は、 _読み込みに失敗しました_ 電子メールとエラーの説明。 最後にスケジュールされたインポートジョブの結果が、「スケジュールされたインポート/エクスポート」ページの「最終結果」列に表示されます。

インポート操作のたびに、インポートファイルのコピーが `var/log/import_export` Adobe CommerceまたはMagento Open Sourceがデプロイされているサーバー上のディレクトリ。 インポートファイル名に、タイムスタンプ、インポートしたエンティティ（製品または顧客）のマーカー、操作のタイプ（この場合はインポート）が追加されます。

スケジュールされたインポートジョブのたびに、再インデックス操作が自動的に実行されます。 フロントエンドでは、更新データがデータベースに送られた後に、説明の変更やその他のテキスト情報が反映され、価格の変更はインデックス再作成後にのみ反映されます。

### 手順 1：インポート設定を完了する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. 右上隅で、 **[!UICONTROL Add Scheduled Import]**.

1. スケジュールおよびインポートのオプションを設定します。

   - **[!UICONTROL Name]**  — スケジュールされたインポートの名前を入力します。

   - **[!UICONTROL Description]**  — インポートの目的と使用方法を説明する簡単な説明を入力します。

   - **[!UICONTROL Entity Type]**  — 次のいずれかに設定します。

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - **[!UICONTROL Import Behavior]**  — 次のいずれかに設定します。

      - `Add/Update Complex Data`  — データベース内の既存のエントリに対して、新しい複雑なデータを既存の複雑なデータに追加または更新します。 これはデフォルト値です。
      - `Replace`  — データベース内の既存のエンティティの既存の複合体を書き込みます。
      - `Delete Entities`  — データベース内の既存のエントリを削除します。
      - `Custom Action`  — データベース内の既存のエンティティをカスタマイズします。

     >[!NOTE]
     >
     >の _[!UICONTROL Advanced Pricing]_,_[!UICONTROL Products]_, _[!UICONTROL Customers and Addresses (single file)]_、および_[!UICONTROL Stock Sources]_ エンティティタイプの場合は、次の読み込み動作が表示されます。 `Add/Update`, `Replace`、および `Delete`. の _顧客の財政状況_, _顧客のメインファイル_、および _顧客と住所_ エンティティタイプの場合は、次の読み込み動作が表示されます。 `Add/Update Complex Data`, `Delete Entities`、および `Custom Action`.

   - **[!UICONTROL Start Time]**  — インポートの開始がスケジュールされている時間、分、秒を設定します。

   - **[!UICONTROL Frequency]**  — 次のいずれかに設定します。 `Daily`, `Weekly`または `Monthly`

   - **[!UICONTROL On Error]**  — 次のいずれかに設定します。 `Stop Import` または `Continue Processing`

   - **[!UICONTROL Status]**  — スケジュールされたインポートを有効にするには、をに設定します。 `Enabled`.

   - **[!UICONTROL Field Separator]**  — インポートファイルのフィールドを区切る文字を入力します。 デフォルトの文字はコンマです。

   - **[!UICONTROL Multiple Value Separator]**  — フィールド内で複数の値を区切るために使用する文字を入力します。

   ![データのインポート — 予定インポート設定](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### 手順 2：インポートファイル情報の入力

1. 設定 **[!UICONTROL Server Type]** を次のいずれかに変更します。

   - `Local Server` - Adobe Commerceがインストールされているサーバーと同じサーバーからデータをインポートします。
   - `Remote FTP`  — リモートサーバーからデータをインポートします。

   ![データのインポート — 予定インポートファイル情報](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >リモートストレージモジュールが有効な場合、 `Local Server` 自動的に切り替える `Remote Storage`.

1. 次を入力します。 **[!UICONTROL File Directory]** 読み込みファイルの元の場所。

   - `Local Server`  — コマースインストールに相対パスを入力します。 例： `var/import`. リモートストレージモジュールが構成されている場合は、 `import_export/import`.
   - `Remote FTP server`  — リモートサーバー上のインポートフォルダーの完全な URL とパスを入力します。

1. 次を入力します。 **[!UICONTROL File Name]** を読み込みます。

1. の場合 **[!UICONTROL Images File Directory]**&#x200B;には、製品画像が保存されるディレクトリのパスを入力します。

   ローカルサーバー上で、次のような相対パスを入力します。 `var/import`. リモート・ストレージで、次のような相対パスを入力します。 `import_export/import` または `import_export/import/some/dir`.

### 手順 3：インポートに失敗した E メールを設定する

![データのインポート — 失敗した電子メールのインポートに失敗しました](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Failed Email Receiver]** インポート中にエラーが発生した場合に通知を受け取るストア連絡先。

1. 設定 **[!UICONTROL Failed Email Sender]** 通知の送信者として表示されるストア連絡先に追加します。

1. 設定 **[!UICONTROL Failed Email Template]** 通知に使用するテンプレートに追加します。

1. の場合 **[!UICONTROL Send Failed Email Copy To]**「 」には、通知のコピーを受け取る人の電子メールアドレスを入力します。

   複数の電子メールアドレスはコンマで区切ります。

1. 設定 **[!UICONTROL Failed Email Copy Method]** を次のいずれかに変更します。

   - `Bcc`  — 失敗したインポート通知の非表示のコピーを送信します。 受信者の名前とアドレスは、元の E メール配布に含まれますが、表示には表示されません。
   - `Separate Email`  — 失敗したインポート通知のコピーを別の電子メールとして送信します。

1. 完了したら、「 **[!UICONTROL Save]**.

   新しくスケジュールされたインポートジョブが、 _[!UICONTROL Scheduled Import/Export]_ページに貼り付けます。 このページから、テストや編集を行うためにすぐに実行できます。 インポートファイルは、各インポートジョブの実行前に検証されます。

>[!NOTE]
>
>スケジュールされたインポート/エクスポートを作成または更新すると、システム設定が変更されます。 保存後、管理ページの上部に表示されるキャッシュの無効化通知に必ず対処し、新しいスケジュールや更新されたスケジュールを適用するためにキャッシュをフラッシュします。

### フィールドの説明

#### [!UICONTROL Import Settings]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Name] | インポートの名前。 多数の異なるスケジュール済みインポートが作成された場合、これを区別するのに役立ちます。 |
| [!UICONTROL Description] | （オプション）説明を入力できます。 |
| [!UICONTROL Entity Type] | インポートするデータを定義します。 |
| [!UICONTROL Import Behavior] | インポートするエンティティがデータベースに存在する場合の複雑なデータの処理方法を定義します。 製品の複雑なデータには、カテゴリ、Web サイト、カスタムオプション、階層価格、関連製品、アップセル、クロスセル、関連製品データなどがあります。 顧客向けの複雑なデータには、住所が含まれます。 オプション：<br>**[!UICONTROL Add/Update Complex Data]**— 新しい複合データが、データベース内の既存のエントリの既存の複合データに追加または更新されます。 これはデフォルト値です。<br>**[!UICONTROL Add/Update]**  — 新しいデータは、データベース内の既存のエントリに追加されます。 以下を除くすべてのフィールド `sku` は製品に対して更新できます。 カテゴリや Web サイトなど、CSV ファイルにリストされない複数のフィールド値は、読み込み後もデータベースに残ります。<br>**[!UICONTROL Replace]**— 既存のエンティティの既存の複雑なデータが置き換えられます。<br>**[!UICONTROL Delete Entities]**  — インポートされたエンティティがデータベース内に存在する場合は、データベースから削除されます。<br>**[!UICONTROL Custom Action]**— インポートプロセス中に、既存の複雑なエンティティがカスタマイズされます。 |
| [!UICONTROL Start Time] | インポートの開始時間、分、秒を設定します。 |
| [!UICONTROL Frequency] | インポートの実行頻度を定義します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL On Error] | ファイルの検証中にエラーが見つかった場合のシステムの動作を定義します。 オプション：<br>**インポートを停止**  — 検証中にエラーが見つかった場合、ファイルはインポートされません。 これはデフォルト値です。<br>**処理を続行**  — 検証中にエラーが見つかったが、インポートが可能な場合は、ファイルがインポートされます。 |
| [!UICONTROL Status] | インポートはデフォルトで有効になっています。 「ステータス」を「 `Disabled`. |
| [!UICONTROL Field Separator] | フィールドの区切りに使用する文字を決定します。 デフォルト値： `,` （コンマ） |
| [!UICONTROL Multiple Value Separator] | フィールド内の複数の値を区切る文字を決定します。 デフォルト値： `,` （コンマ） |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Server Type] | コマースがデプロイされているサーバーと同じサーバー上のファイルからインポートできます (「 `Local Server`) またはリモート FTP サーバー ( `Remote FTP`) をクリックします。 次を選択した場合、 _[!UICONTROL Remote FTP]_に設定すると、資格情報とファイル転送設定の追加オプションが表示されます。 リモートストレージモジュールが有効な場合、 `Local Server` タイプは自動的に次に切り替わります： `Remote Storage`. |
| [!UICONTROL File Directory] | インポートファイルが存在するディレクトリを指定します。 Server Type が _[!UICONTROL Local Server]_に設定し、Commerce インストールディレクトリを基準とした相対パスを指定します。 例： `var/import` または `import_export/import` リモートストレージ用。 |
| [!UICONTROL File Name] | インポートファイルの名前を指定します。 |
| [!UICONTROL Images File Directory] | 製品画像が保存されるディレクトリのパスを入力します。 ローカルサーバーの場合は、相対パスを入力します。 例： `var/import` または `import_export/import` リモートストレージ用。 |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | インポートに失敗した場合に電子メール通知（インポートに失敗した電子メール）を送信する電子メールアドレスを指定します。 |
| [!UICONTROL Failed Email Sender] | インポートに失敗した電子メールの送信者として使用する電子メールアドレスを指定します。 |
| [!UICONTROL Failed Email Template] | インポートに失敗した E メールのテンプレートを選択します。 デフォルトでは、「読み込みに失敗しました」（「ロケールのデフォルトテンプレート」オプションを使用できます）オプションのみ使用できます。 カスタムテンプレートは以下に作成できます。 _[!UICONTROL System]_>_[!UICONTROL Transactional Emails]_. |
| [!UICONTROL Send Failed Email Copy To] | インポートに失敗した電子メールのコピーの送信先の電子メールアドレス。 |
| [!UICONTROL Send Failed Email Copy Method] | インポートに失敗した E メールのコピー送信方法を選択します。 |

{style="table-layout:auto"}

## エクスポートのスケジュール設定

スケジュールされた書き出しは、手動の [書き出し](data-export.md) エクスポート可能なエクスポートファイルフォーマットとエクスポート可能なエンティティのタイプ：

- CSV 形式に書き出すことができます
- 製品および顧客データを書き出すことができます

スケジュールされたエクスポートを使用する利点は、エクスポートパラメーターを指定し、スケジュールを 1 回だけ実行した後で、データを複数回自動的にエクスポートできることです。

各エクスポートの詳細はログに書き込まれませんが、エラーが発生した場合は、エラーの説明を含む「エクスポート失敗」の電子メールが送信されます。 最後のエクスポートジョブの結果は、「スケジュールされたインポート/エクスポート」ページの「最終結果」列に表示されます。

エクスポートのたびに、エクスポートファイルはユーザー定義の場所に配置され、コピーは `var/log/import_export` Adobe CommerceまたはMagento Open Sourceがデプロイされているサーバー上のディレクトリ。 エクスポートするエンティティ（製品または顧客）のタイムスタンプとマーカー、操作のタイプ（この場合はエクスポート）がエクスポートファイル名に追加されます。

### 手順 1：書き出し設定を完了する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. 右上隅で、 **[!UICONTROL Add Scheduled Export]** 次の操作を実行します。

   - を入力します。 **[!UICONTROL Name]** スケジュールされた書き出し用。

   - 概要を入力 **[!UICONTROL Description]** これが、輸出の目的とその使い方を説明する。

   - 設定 **[!UICONTROL Entity Type]** を次のいずれかに変更します。

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     The _[!UICONTROL Entity Attributes]_」セクションが更新され、選択したエンティティタイプが反映されます。

   - 設定 **[!UICONTROL Start Time]** 書き出しがスケジュールされている時間、分、秒を指定します。

   - 設定 **[!UICONTROL Frequency]** を次のいずれかに変更します。

      - `Daily`
      - `Weekly`
      - `Monthly`

1. スケジュールされたエクスポートを有効にするには、 **[!UICONTROL Status]** から `Enabled`.

1. 確定 `CSV` をデフォルトとして **[!UICONTROL File Format]**.

   ![予定書き出し設定](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### 手順 2：エクスポートファイル情報の入力

1. 設定 **[!UICONTROL Server Type]** を次のいずれかに変更します。

   - `Local Server` - Commerce がインストールされているサーバーと同じサーバーにエクスポートファイルを保存します。
   - `Remote FTP`  — エクスポートファイルをリモートサーバーに保存します。

   ![スケジュールされた書き出しファイル情報](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >リモートストレージモジュールが有効な場合、 `Local Server` 自動的に切り替える `Remote Storage`.

1. の場合 **[!UICONTROL File Directory]**&#x200B;をクリックし、エクスポートファイルを保存するディレクトリを次のように入力します。

   - の場合 **[!UICONTROL Local Server]**、コマースインストール内の相対パスを入力します。例： `var/export`. リモートストレージモジュールが構成されている場合は、 `import_export/export`.
   - の場合 **[!UICONTROL Remote FTP server]**」に、宛先サーバー上のターゲットフォルダーの完全な URL とパスを入力します。

1. 次の場合、 _[!UICONTROL Remote FTP]_サーバを選択し、サーバへの接続資格情報を入力して、追加設定を選択します。

   - の場合 **[!UICONTROL FTP Host[:Port]]**、リモート FTP ホストアドレスを入力します。
   - の場合 **[!UICONTROL User Name]**」に、リモートサーバーへのアクセスに使用するユーザー名を入力します。
   - の場合 **[!UICONTROL Password]**、指定したユーザー名アカウントのパスワードを入力します。
   - の場合 **[!UICONTROL File Mode]**&#x200B;を選択します。 `Binary` または `ASCII`.
   - の場合 **[!UICONTROL Passive Mode]**&#x200B;を選択します。 `No` または `Yes`.

### 手順 3：書き出しエラーの電子メールを設定する

1. 設定 **[!UICONTROL Failed Email Receiver]** エクスポート中にエラーが発生した場合に通知を受け取るストア連絡先。

1. 設定 **[!UICONTROL Failed Email Sender]** 通知の送信者として表示されるストア連絡先に追加します。

1. 設定 **[!UICONTROL Failed Email Template]** 通知に使用するテンプレートに追加します。

1. の場合 **[!UICONTROL Send Failed Email Copy To]**「 」には、通知のコピーを受け取る人の電子メールアドレスを入力します。

   複数の電子メールアドレスの場合は、コンマで区切ります。

1. 設定 **[!UICONTROL Failed Email Copy Method]** を次のいずれかに変更します。

   - `Bcc`  — ブラインドのコピーを送信します。 受信者の名前とアドレスは、元の E メール配布に含まれますが、表示には表示されません。
   - `Separate Email`  — コピーを別の E メールとして送信します。

### 手順 4：エンティティ属性の選択

1. Adobe Analytics の _[!UICONTROL Entity Attributes]_「 」セクションで、エクスポートデータに含める属性を選択します。

   - 書き出しデータを属性値でフィルタするには、 _[!UICONTROL Filter]_列。
   - 特定の属性値を持つ製品や顧客を除外するには、除外する属性の値を入力し、「スキップ」列のチェックボックスをオンにします。

1. 完了したら、「 **[!UICONTROL Save]**.

   新しいスケジュール済み書き出しジョブが、 _[!UICONTROL Scheduled Import/Export]_ページに貼り付けます。 このページから、テスト用、編集用に、即座に実行できます。

>[!NOTE]
>
>スケジュールされたインポート/エクスポートを作成または更新すると、システム設定が変更されます。 保存後、管理ページの上部に表示されるキャッシュの無効化通知に必ず対処し、新しいスケジュールや更新されたスケジュールを適用するためにキャッシュをフラッシュします。

### フィールドの説明

#### [!UICONTROL Export Settings]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Name] | エクスポートの名前。 スケジュールされた多数の書き出しが作成された場合、区別するのに役立ちます。 |
| [!UICONTROL Description] | （オプション）スケジュールされたエクスポートの説明。 |
| [!UICONTROL Entity Type] | 書き出すデータを指定します。 選択を行うと、エンティティ属性が下に表示されます。 オプション： `Advanced Pricing` / `Products` / `Customer Finances` / `Customers Main File` / `Customer Addresses` / `Stock Sources` |
| [!UICONTROL Start Time] | エクスポートの開始時間、分、秒を設定します。 |
| [!UICONTROL Frequency] | 書き出しジョブの実行頻度を定義します。 オプション： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Status] | 新しいスケジュール済み書き出しは、デフォルトで有効になっています。 「ステータス」を「無効」に設定すると、この機能を休止できます。 オプション： `Enabled` / `Disabled` |
| [!UICONTROL File Format] | エクスポートファイルの形式を選択します。 現在、 `.CSV` オプションが使用可能です。 |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Server Type] | 書き出しファイルの場所を決定します。 オプション：<br>**ローカルサーバー** — Commerce がデプロイされているサーバーと同じサーバーにエクスポートファイルを配置します。 リモートストレージモジュールが有効な場合、 `Local Server` は、 `Remote Storage`.<br>**リモート FTP**  — エクスポートファイルをリモートサーバーに配置します。 資格情報とファイル転送設定の追加オプションが表示されます。 |
| [!UICONTROL File Directory] | エクスポートファイルを配置するディレクトリを指定します。 ケース _[!UICONTROL Server Type]_が `Local Server`に設定し、Commerce インストールパスを基準とした相対パスを指定します。 例： `var/export`または `import_export/export` リモートストレージ用。 |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| フィールド | 説明 |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | 書き出しが失敗した場合に電子メール通知（書き出しに失敗した電子メール）を送信する電子メールアドレスを指定します。 |
| [!UICONTROL Failed Email Sender] | 書き出しに失敗した電子メールの送信者として使用する電子メールアドレスを指定します。 |
| [!UICONTROL Failed Email Template] | 失敗した書き出し E メールのテンプレートを選択します。 デフォルトでは、 `Export Failed (Default Template from Locale)` オプションが使用可能です。 |
| [!UICONTROL Send Failed Email Copy To] | 失敗した書き出し電子メールのコピーの送信先の電子メールアドレス。 |
| [!UICONTROL Send Failed Email Copy Method] | 書き出しに失敗した電子メールのコピー送信方法を指定します。 |

{style="table-layout:auto"}
