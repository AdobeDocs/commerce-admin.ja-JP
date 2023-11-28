---
title: 電子メールテンプレートのカスタマイズ
description: Web サイト、ストア、ストアの各表示用に電子メールテンプレートをカスタマイズする方法を説明します。
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# 電子メールテンプレートのカスタマイズ

Commerce には、システムから送信される各メッセージの本文セクション用のデフォルトの電子メールテンプレートが含まれています。 本文コンテンツのテンプレートとヘッダーおよびフッターテンプレートを組み合わせて、完全なメッセージを作成します。 コンテンツはHTMLと CSS でフォーマットされ、 [変数](variables-predefined.md) および [widgets](../content-design/widgets.md). 電子メールテンプレートは、Web サイト、ストア、ストアの各ビューに合わせてカスタマイズできます。 カスタムテンプレートを使用する場合は、必ず [システム構成](email-templates.md#configure-email-templates) をクリックして、正しいテンプレートが使用されていることを確認します。

![例 — お知らせメールのプレビュー](./assets/email-template-preview.png){width="500" zoomable="yes"}

デフォルトのテンプレートには、ロゴと保存情報が含まれており、それ以上カスタマイズしなくても使用できます。 ただし、ベストプラクティスとしては、各テンプレートを表示し、必要に応じて変更してから、顧客に送信する必要があります。

- [ヘッダーテンプレート](email-template-custom.md#header-template)
- [フッターテンプレート](email-template-custom.md#footer-template)
- [メッセージテンプレート](email-template-custom.md#message-templates)

![電子メールテンプレート](./assets/email-templates.png){width="700" zoomable="yes"}

## テンプレート情報

| フィールド | 説明 |
| ----- | ----------- |
| [!UICONTROL Template Name] | カスタムテンプレートの名前。 |
| [!UICONTROL Insert Variable] | テンプレートのカーソル位置に変数を挿入します。 |
| [!UICONTROL Template Subject] | [ 件名 ] 列に [ テンプレートの件名 ] が表示され、リスト内のテンプレートの並べ替えとフィルタリングに使用できます。 |
| [!UICONTROL Template Content] | HTML内のテンプレートのコンテンツ。 |
| [!UICONTROL Template Styles] | テンプレートの書式設定に必要な CSS スタイル宣言は、 _[!UICONTROL Template Styles]_ボックス。 |

{style="table-layout:auto"}

## ヘッダーテンプレート

完了後、 [設定](email-templates.md#configure-email-templates)を使用する場合、電子メールヘッダーテンプレートには、ストアにリンクされたロゴが含まれます。 HTMLに関する基本的な知識を持っている場合は、 [定義済み変数](variables-predefined.md) をクリックして、ストアの連絡先情報をヘッダーに追加します。

### 手順 1. デフォルトのテンプレートを読み込む

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. クリック **[!UICONTROL Add New Template]**.

1. Adobe Analytics の **[!UICONTROL Load default template]** セクションで、 **[!UICONTROL Template]** セレクターと選択 `Magento_Email` > `Header`.

   ![電子メールテンプレートヘッダー — デフォルトテンプレートの読み込み](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Load Template]**.

   HTMLのテンプレートコードと変数がフォームに表示されます。

### 手順 2. テンプレートのカスタマイズ

1. 次を入力します。 **[!UICONTROL Template Name]** カスタムヘッダー用。

1. を入力します。 **[!UICONTROL Template Subject]** を参照してください。

   グリッドでは、テンプレートのリストを並べ替え、 _[!UICONTROL Subject]_列。

   ![電子メールテンプレートヘッダー情報](./assets/email-template-information.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Template Content]** ボックスで、必要に応じてHTMLを変更します。

   >[!NOTE]
   >
   >テンプレートコードで作業する際は、中括弧で囲まれた内容が上書きされないように注意してください。

1. を挿入するには [変数](variables-reference.md)で、変数を配置するコードにカーソルを置き、 **[!UICONTROL Insert Variable]**.

1. 挿入する変数を選択します。

   ![ヘッダーテンプレート — 変数の挿入](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   変数を選択すると、 [マークアップタグ](markup-tags.md) 変数がコードに挿入される場合に使用します。

   「 Store Email Address 」変数は、ヘッダーで最も頻繁に使用される変数ですが、任意のシステムまたは [カスタム変数](variables-custom.md) をテンプレートに直接挿入します。

1. CSS 宣言を行う必要がある場合は、 **[!UICONTROL Template Styles]** ボックス。

1. 作業内容を確認する準備が整ったら、「 **[!UICONTROL Preview Template]**.

   必要に応じて、テンプレートに変更を加えます。

1. 完了したら、「 **[!UICONTROL Save Template]**.

   これで、使用可能な電子メールテンプレートのリストにカスタムヘッダーが表示されます。

### 手順 3. 設定を更新します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. グリッドで、設定するストア表示を探し、 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Transactional Emails]** 」セクションに入力します。

1. を選択します。 **[!UICONTROL Header Template]** 電子メール通知のデフォルトとして使用される。

1. 完了したら、「 **[!UICONTROL Save Config]**.

![トランザクション E メールデザインの設定 — ヘッダーテンプレート](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## フッターテンプレート

電子メールテンプレートフッターには、電子メールメッセージの終了行と署名行が含まれます。 スタイルに合わせて終了を変更し、名前の下に会社名や住所などの追加情報を追加できます。

### 手順 1. デフォルトのテンプレートを読み込む

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. クリック **[!UICONTROL Add New Template]**.

1. Adobe Analytics の **[!UICONTROL Load default template]** セクションで、 **[!UICONTROL Template]** セレクターと選択 `Magento_Email` > `Footer`.

1. クリック **[!UICONTROL Load Template]**.

   HTMLのテンプレートコードと変数がフォームに表示されます。

### 手順 2. テンプレートのカスタマイズとプレビュー

1. 次を入力します。 **[!UICONTROL Template Name]** を設定します。

1. を入力します。 **[!UICONTROL Template Subject]** を参照してください。

   グリッドでは、テンプレートを並べ替え、 _[!UICONTROL Subject]_列。

   ![電子メールテンプレートフッター — 情報](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Template Content]** ボックスで、必要に応じてHTMLを変更します。

   >[!NOTE]
   >
   >テンプレートコードで作業する際は、中括弧で囲まれた内容が上書きされないように注意してください。

1. を挿入するには [変数](variables-reference.md)で、変数を配置するコードにカーソルを置き、 **[!UICONTROL Insert Variable]**.

1. 挿入する変数を選択します。

   変数を選択すると、 [マークアップタグ](markup-tags.md) 変数がコードに挿入される場合に使用します。

   「連絡先を保存」変数はフッターに含まれる頻度が最も高いものですが、任意のシステムまたは [カスタム変数](variables-custom.md) をテンプレートに直接挿入します。

1. CSS 宣言を行う必要がある場合は、 **[!UICONTROL Template Styles]** ボックス。

### 手順 3. 設定を更新します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. グリッドで、設定するストア表示を探し、 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Transactional Emails]** 」セクションに入力します。

1. を選択します。 **[!UICONTROL Footer Template]** 電子メール通知でデフォルトのフッターとして使用される

1. 完了したら、「 **[!UICONTROL Save Config]**.

![トランザクション E メールデザインの設定 — フッターテンプレート](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## メッセージテンプレート

各メッセージの本文をカスタマイズするプロセスは、ヘッダーやフッターをカスタマイズするプロセスと同じです。 唯一の違いは、通知をトリガーする各アクティビティまたはイベントのメッセージテンプレートです。 テンプレートをそのまま使用することも、声やブランドに合わせてカスタマイズすることもできます。 テンプレートテキストに加えて、様々な選択肢を使用できます [定義済み](variables-predefined.md) 変数と [カスタム](variables-custom.md) 変数を作成して、テンプレートに組み込むことができます。

### 手順 1. デフォルトのテンプレートを読み込む

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. クリック **[!UICONTROL Add New Template]**.

   ![電子メールテンプレート — デフォルトテンプレートを読み込み](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. 次の操作を実行します。

   - の下 **[!UICONTROL Load default template]**、選択 **[!UICONTROL Template]** を選択します。

   - クリック **[!UICONTROL Load Template]**.

### 手順 2. テンプレートのカスタマイズ

1. の場合 **[!UICONTROL Template Name]**」で、カスタムテンプレートの名前を入力します。

1. 必要に応じて、 **[!UICONTROL Template Subject]**.

   これはメッセージの最初の行で、デフォルトでは敬称です。 そのままにしておくことも、わかりやすいものを入力することもできます。

1. 次の項目をメモします。 **[!UICONTROL Currently Used For]** 設定の更新に使用するパスであるテンプレートへのパス。

   ![電子メールテンプレート — テンプレート情報](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. Adobe Analytics の **[!UICONTROL Template Content]** ボックスで、必要に応じてHTMLを変更します。

   コンテンツは、HTMLタグ、CSS ディレクティブ、変数、テキストの組み合わせで構成されます。

   >[!NOTE]
   >
   >テンプレートコードで作業する際は、二重中括弧で囲まれたコードを誤って入力しないように注意してください。

1. 変数を挿入するには、変数を表示するコード内にカーソルを置きます。

   変数の選択は、テンプレートによって異なり、使用できる変数も含まれます。 [定義済み](variables-predefined.md) および [カスタム](variables-custom.md) 変数（使用可能な場合）

1. クリック **[!UICONTROL Insert Variable]** を選択し、挿入する変数を選択します。

   変数を挿入するコマンドは中括弧で囲み、カーソル位置のコードに追加します。 例：

   `customVar code=my_custom_variable`

1. CSS 宣言を行うには、 **[!UICONTROL Template Styles]**.

   ![電子メールテンプレート — カスタムスタイルの追加](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >カスタムスタイルは、 `{{template config_path="design/email/header_template"}}` が _[!UICONTROL Template Styles]_. デフォルトのヘッダーテンプレートを使用せずにカスタム CSS を使用するには、それらを `<style>` HTMLタグ。

### 手順 3. 設定を更新します。

The _[!UICONTROL Currently Used For]_パンくずリストには、テンプレートが使用されている場所が表示されます。 この例では、テンプレート設定は、_[!UICONTROL Customer Configuration]_ ページの _[!UICONTROL Create New Account Options]_セクション、および_[!UICONTROL Default Welcome Email]_ フィールドに入力します。

- ページ — [!UICONTROL Customer Configuration]
- セクション — [!UICONTROL Create New Account Options]
- フィールド — [!UICONTROL Default Welcome Email]

1. Adobe Analytics の **[!UICONTROL Currently Used For]** パンくずリストで、リンクをクリックしてテンプレート設定ページを開きます。

   ![現在のメールテンプレート](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) 「 」セクションに移動して、カスタマイズした e メールテンプレートのフィールドを探します。

1. 次をクリア： **[!UICONTROL Use system value]** チェックボックスをオンにして、カスタムテンプレートの名前をクリックします。

   ![顧客設定 — デフォルトのお知らせメールテンプレート](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. ワークスペース上部のメッセージで、 **[!UICONTROL Cache Management]** 無効なキャッシュをクリアします。

### 手順 4. テンプレートをプレビューして保存します。

1. 作業内容を確認する準備が整ったら、「 **[!UICONTROL Preview Template]**.

1. 必要に応じて、テンプレートを更新します。

1. 完了したら、「 **[!UICONTROL Save Template]**.

   これで、カスタムテンプレートが E メールテンプレートのリストに表示されます。
