---
title: 顧客アカウントの管理
description: 以下を使用します。 [!UICONTROL Customers] グリッドを使用して、個々の顧客アカウントの顧客アカウントとアクセス情報を検索します。
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# 顧客アカウントの管理

以下を使用します。 _[!UICONTROL Customers]_グリッドを使用して、任意の顧客アカウントを検索します。 標準 [職場の統制](../getting-started/admin-workspace.md) リストをフィルターするには、 [列レイアウト](../getting-started/admin-grid-controls.md)、ビューの保存、データの書き出しを行います。 The [アクションコントロール](../getting-started/admin-actions-control.md) グリッドの上にあるを使用して、操作を複数の顧客レコードに適用できます。

![すべての顧客](assets/customers-all-customers.png){width="700" zoomable="yes"}

詳しくは、 [顧客プロファイルを更新](update-account.md) を参照してください。

## 顧客アカウントアクション

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッドの最初の列で、更新する各レコードのチェックボックスをオンにします。

1. 適用するアクションの指示に従います。

   >[!INFO]
   >
   >次のアクションは、1 つのレコードまたは複数のレコードに適用できます。

1. 完了したら、「 **[!UICONTROL Save Config]**.

### ニュースレターを購読

グローバルを使用したマルチストアおよびマルチサイトの設定 [顧客アカウントの範囲](../customers/customer-account-scope.md)の場合、顧客アカウントをニュースレターの複数のサイトまたはストアに購読することができます。 次の条件を満たす場合、 _購読_ 顧客アカウントに対するアクションでは、デフォルトのサイト/ストア表示用のニュースレターの購読のみが有効化されます。

* を設定します。 **[!UICONTROL Actions]** ～を制御する `Subscribe to newsletter`.

詳しくは、 [購読者の管理](../merchandising-promotions/newsletter-subscribers.md) を参照してください。

### ニュースレターを購読解除

グローバルを使用したマルチストアおよびマルチサイトの設定 [顧客アカウントの範囲](customer-account-scope.md)の場合、顧客アカウントを複数のサイト/ストアのニュースレターに購読登録できます。 次の条件を満たす場合、 _配信停止_ アクションを顧客アカウントに追加すると、アクティブなすべての購読は購読解除されます。

1. を設定します。 **[!UICONTROL Actions]** ～を制御する `Unsubscribe to newsletter`.

1. 確認するメッセージが表示されたら、「 **OK**.

### 顧客グループの割り当て

1. を設定します。 **[!UICONTROL Actions]** ～を制御する `Assign a customer group`.

1. 選択したすべての顧客レコードを割り当てる顧客グループを選択します。

1. 確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.

### 顧客アカウントの削除

削除した顧客アカウントは復元できません。 顧客の活動とトランザクションに関する情報は、システムで保持されます。

1. を設定します。 **[!UICONTROL Actions]** ～を制御する `Delete`.

1. 確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.

## 顧客アカウントのエクスポート

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. テーブルヘッダーメニューで、 **[!UICONTROL Export]** をクリックし、目的の形式を選択します。

   * CSV
   * Excel XML

1. クリック **[!UICONTROL OK]**.

   ファイルは、デフォルトのダウンロードフォルダーに移動します。

上記の手順では、すべての顧客アカウントをエクスポートします。 限られたセットをエクスポートする場合は、エクスポートするアカウントのチェックボックスをオンにするか、コントロールパネルのフィルターを使用して、様々な顧客アカウントを選択します。

## アクション/コントロール

| オプション | 説明 |
|--- |--- |
| **[!UICONTROL Delete]** | 選択した顧客アカウントを削除します。 顧客アカウントが B2B ストアの会社管理者に属している場合、顧客アカウントを削除する前に、別の会社ユーザーを管理者として割り当てる必要があります。 |
| **[!UICONTROL Subscribe to Newsletter]** | 選択した顧客をニュースレターに購読します。 |
| **[!UICONTROL Unsubscribe from Newsletter]** | 選択した顧客をニュースレターから購読解除します。 |
| **[!UICONTROL Assign a Customer Group]** | 選択した顧客を顧客グループに割り当てます。 |
| **[!UICONTROL Edit]** | 選択した 1 つの顧客レコードの一部の値をグリッドから編集できます。 デフォルトでは、クイック編集には、E メール、グループ、電話、郵便番号、Web サイト、税金 VAT 番号、性別の値を使用できます。 |

{style="table-layout:auto"}

## 列

| 列 | 説明 |
|--- |--- |
| **[!UICONTROL Select]** | アクションを適用するための顧客レコードのチェックボックス選択を管理します。 また、列ヘッダーの選択コントロールを使用して、すべてを選択/選択解除することもできます。 |
| **[!UICONTROL ID]** | 顧客アカウントの作成時に割り当てられる一意の数値識別子。 |
| **[!UICONTROL Name]** | 顧客の姓と名。 |
| **[!UICONTROL Email]** | 顧客の電子メールアドレス。 |
| **[!UICONTROL Group]** | 顧客を割り当てる顧客グループ。 |
| **[!UICONTROL Phone]** | 顧客の電話番号。 |
| **[!UICONTROL ZIP]** | 顧客の郵便番号。 |
| **[!UICONTROL Country]** | 顧客の所在国。 |
| **[!UICONTROL State/Province]** | 顧客の所在地の都道府県。 |
| **[!UICONTROL Customer Since]** | 顧客アカウントが作成された日時。 |
| **[!UICONTROL Web Site]** | 顧客アカウントが関連付けられているストア階層の Web サイト。 |
| **[!UICONTROL Confirmed Email]** | 確認 E メールが必要かどうかを示します。 |
| **[!UICONTROL Account Created In]** | 顧客アカウントの作成元のストア表示を示します。 |
| **[!UICONTROL Date of Birth]** | 顧客の生年月日。 現在のセキュリティおよびプライバシーのベストプラクティスに従って、顧客の生年月日（月、日、年）と他の個人識別子を含むストレージに関連する、法的リスクおよびセキュリティリスクの可能性を認識しておきます。 顧客の完全な生年月日の保存を制限し、顧客の生年月日を代替として使用することをお勧めします。 |
| **[!UICONTROL Tax / VAT Number]** | 該当する場合は、税番号または [付加価値税](../stores-purchase/vat.md) 顧客に割り当てられる番号。 <br/><br/> このフィールドは VAT 番号と同じではありません。 |
| **[!UICONTROL Gender]** | 顧客の性別。 |
| **[!UICONTROL Action]** | 編集 — 会社アカウントを編集モードで開きます。 |

{style="table-layout:auto"}

### 追加の列

これらの列は、 [列レイアウト](../getting-started/admin-grid-controls.md) グリッドの。

| 列 | 説明 |
|--- |--- |
| **[!UICONTROL Company]** | 顧客の会社名。 |
| **[!UICONTROL Street Address]** | 顧客の住所。 |
| **[!UICONTROL City]** | 顧客が所在する市区町村。 |
| **[!UICONTROL Fax]** | 顧客の FAX 番号（該当する場合）。 |
| **[!UICONTROL Billing Firstname]** | 顧客の請求先住所の名。 |
| **[!UICONTROL Billing Lastname]** | 顧客の請求先住所の姓。 |
| **[!UICONTROL Billing Address]** | 請求情報を送信するアドレス。 |
| **[!UICONTROL Shipping Address]** | 注文が発送される住所。 |
| **[!UICONTROL VAT Number]** | 顧客の住所に関連付けられている付加価値税番号。 の場合 [デジタル商品](../stores-purchase/taxes.md) EU で販売された VAT は、顧客の請求先住所に基づきます。 <br/><br/> このフィールドは、税/VAT 番号と同じではありません。 |
| **[!UICONTROL Account Lock]** | アカウントのステータスを示します。 セキュリティ対策として、顧客アカウントは次のことが可能です。 [ロック済み](../customers/password-options.md) ログイン試行が多すぎた後。 値： `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | 現在のユーザーのステータス。 オプション： `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | 顧客の分類。 オプション： `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | 会社アカウントの連絡先として割り当てられ、会社に関連するすべての自動電子メールメッセージを受け取る営業担当者。 |

{style="table-layout:auto"}
