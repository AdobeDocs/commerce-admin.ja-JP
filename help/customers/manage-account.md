---
title: 顧客アカウントの管理
description: '[!UICONTROL Customers] グリッドを使用して、顧客アカウントを検索し、個々の顧客アカウントの情報にアクセスします。'
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# 顧客アカウントの管理

_[!UICONTROL Customers]_グリッドを使用して、任意の顧客アカウントを検索します。 標準の[職場向けコントロール ](../getting-started/admin-workspace.md)を使用して、リストのフィルタリング、[列レイアウト ](../getting-started/admin-grid-controls.md)の変更、ビューの保存、データの書き出しを行うことができます。 グリッドの上の[ アクション コントロール ](../getting-started/admin-actions-control.md)を使用して、操作を複数の顧客レコードに適用できます。

![すべてのお客様](assets/customers-all-customers.png){width="700" zoomable="yes"}

顧客アカウントを手動で更新する方法については、[顧客プロファイルの更新](update-account.md)を参照してください。

## 顧客アカウントのアクション

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**&#x200B;に移動します。

1. グリッドの最初の列で、更新する各レコードのチェックボックスを選択します。

1. 適用するアクションの手順に従います。

   >[!INFO]
   >
   >次のアクションは、単一または複数のレコードに適用できます。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

### ニュースレターを購読

グローバルな[顧客アカウントスコープ ](../customers/customer-account-scope.md)を持つマルチストアおよびマルチサイトの設定では、顧客アカウントを複数のサイトまたはストアのニュースレターに購読できます。 _購読_ アクションを顧客アカウントに適用すると、デフォルトのサイト/ストアビューでのみニュースレターサブスクリプションがアクティブになります。

* **[!UICONTROL Actions]** コントロールを`Subscribe to newsletter`に設定します。

お客様のニュースレター購読の管理について詳しくは、[購読者の管理](../merchandising-promotions/newsletter-subscribers.md)を参照してください。

### ニュースレターの購読を解除

グローバルな[顧客アカウントスコープ ](customer-account-scope.md)を持つマルチストアおよびマルチサイト設定では、顧客アカウントを複数のサイト/ストアのニュースレターに購読できます。 顧客アカウントに&#x200B;_登録解除_ アクションを適用すると、アクティブなすべてのサブスクリプションが登録解除されます。

1. **[!UICONTROL Actions]** コントロールを`Unsubscribe to newsletter`に設定します。

1. 確認を求められたら、**OK**&#x200B;をクリックします。

### 顧客グループの割り当て

1. **[!UICONTROL Actions]** コントロールを`Assign a customer group`に設定します。

1. 選択したすべての顧客レコードを割り当てる顧客グループを選択します。

1. 確認を求められたら、**[!UICONTROL OK]**&#x200B;をクリックします。

### 顧客アカウントの削除

削除された顧客アカウントは復元できません。 顧客のアクティビティとトランザクションに関する情報は、システムに保持されます。

1. **[!UICONTROL Actions]** コントロールを`Delete`に設定します。

1. 確認を求められたら、**[!UICONTROL OK]**&#x200B;をクリックします。

## 顧客アカウントの書き出し

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**&#x200B;に移動します。

1. テーブルヘッダーメニューで「**[!UICONTROL Export]**」をクリックし、目的の形式を選択します。

   * CSV
   * Excel XML

1. **[!UICONTROL OK]**&#x200B;をクリックします。

   ファイルはデフォルトのダウンロードフォルダーに移動します。

上記の指示は、すべての顧客アカウントを書き出します。 制限付きセットを書き出す場合は、書き出すアカウントのチェックボックスを選択するか、コントロールパネルのフィルターを使用して顧客アカウントの範囲を選択します。

## アクション/コントロール

| オプション | 説明 |
|--- |--- |
| **[!UICONTROL Delete]** | 選択した顧客アカウントを削除します。 顧客アカウントがB2B ストアの会社管理者に属している場合、顧客アカウントを削除する前に、別の会社ユーザーを管理者として割り当てる必要があります。 |
| **[!UICONTROL Subscribe to Newsletter]** | 選択した顧客をニュースレターに購読します。 |
| **[!UICONTROL Unsubscribe from Newsletter]** | ニュースレターから選択した顧客の購読を解除します。 |
| **[!UICONTROL Assign a Customer Group]** | 選択した顧客を顧客グループに割り当てます。 |
| **[!UICONTROL Edit]** | 選択された単一の顧客レコードの一部の値をグリッドから編集できるようにします。 デフォルトでは、電子メール、グループ、電話、ZIP、Web サイト、消費税VAT番号、性別の値を簡単に編集できます。 |

{style="table-layout:auto"}

## 列

| 列 | 説明 |
|--- |--- |
| **[!UICONTROL Select]** | アクションを適用するための顧客レコードのチェックボックスの選択を管理します。 列ヘッダーの選択コントロールを使用して、すべてを選択または選択解除することもできます。 |
| **[!UICONTROL ID]** | 顧客アカウントの作成時に割り当てられる一意の数値識別子。 |
| **[!UICONTROL Name]** | 顧客の姓と名。 |
| **[!UICONTROL Email]** | 顧客の電子メールアドレス。 |
| **[!UICONTROL Group]** | 顧客が割り当てられている顧客グループ。 |
| **[!UICONTROL Phone]** | 顧客の電話番号。 |
| **[!UICONTROL ZIP]** | お客様の郵便番号。 |
| **[!UICONTROL Country]** | 顧客が所在する国。 |
| **[!UICONTROL State/Province]** | 顧客が所在する州または都道府県。 |
| **[!UICONTROL Customer Since]** | 顧客アカウントが作成された日時。 |
| **[!UICONTROL Web Site]** | 顧客アカウントが関連付けられているストア階層のweb サイト。 |
| **[!UICONTROL Confirmed Email]** | 確認メールが必要かどうかを示します。 |
| **[!UICONTROL Account Created In]** | 顧客アカウントの作成元のストアビューを示します。 |
| **[!UICONTROL Date of Birth]** | 顧客の生年月日。 現在のセキュリティとプライバシーのベストプラクティスに従って、顧客の生年月日（月、日、年）を他の個人識別子と保管することに関連する潜在的な法的およびセキュリティリスクを認識してください。 お客様の生年月日の保存を制限し、お客様の生年月日を代替手段として使用することをお勧めします。 |
| **[!UICONTROL Tax / VAT Number]** | 該当する場合、お客様に割り当てられている税番号または[付加価値税](../stores-purchase/vat.md)番号。<br/><br/> このフィールドはVAT番号と同じではありません。 |
| **[!UICONTROL Gender]** | 顧客の性別。 |
| **[!UICONTROL Action]** | 編集 – 会社アカウントを編集モードで開きます。 |

{style="table-layout:auto"}

### その他の列

これらの列は、グリッドの[列レイアウト ](../getting-started/admin-grid-controls.md)を変更することで使用できます。

| 列 | 説明 |
|--- |--- |
| **[!UICONTROL Company]** | 顧客の会社名。 |
| **[!UICONTROL Street Address]** | 顧客の住所。 |
| **[!UICONTROL City]** | 顧客が所在する都市。 |
| **[!UICONTROL Fax]** | 顧客のFAX番号（該当する場合）。 |
| **[!UICONTROL Billing Firstname]** | お客様の請求先住所の名。 |
| **[!UICONTROL Billing Lastname]** | 顧客の請求先住所の姓。 |
| **[!UICONTROL Billing Address]** | 請求情報を送信するアドレス。 |
| **[!UICONTROL Shipping Address]** | 注文が発送される住所。 |
| **[!UICONTROL VAT Number]** | 顧客アドレスに関連付けられている付加価値税番号。 EUで販売された[ デジタル商品](../stores-purchase/taxes.md)の場合、VATは顧客の請求先住所に基づきます。<br/><br/> このフィールドは、税金/VAT番号と同じではありません。 |
| **[!UICONTROL Account Lock]** | アカウントのステータスを示します。 セキュリティ対策として、ログインの試行回数が多すぎると、顧客アカウントが[ ロック ](../customers/password-options.md)される可能性があります。 値：`Locked` / `Unlocked` |
| **[!UICONTROL Status]** | 現在のユーザーステータス。 オプション：`Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | 顧客の分類： オプション：`Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | 会社アカウントの連絡先として割り当てられ、会社に関連するすべての自動メールメッセージを受け取る営業担当者。 |

{style="table-layout:auto"}
