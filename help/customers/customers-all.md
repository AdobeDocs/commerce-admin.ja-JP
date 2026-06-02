---
title: 顧客リスト
description: 「顧客」グリッドには、ストアにアカウントを登録したか、管理者によって追加されたすべての顧客が一覧表示されます。
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# 顧客リスト

管理画面では、[!UICONTROL Customers] グリッドには、ストアにアカウントを登録したか、管理者によって追加されたすべての顧客が一覧表示されます。 標準の[&#x200B; グリッドコントロール &#x200B;](../getting-started/admin-grid-controls.md)を使用して、リストをフィルタリングし、列レイアウトを調整します。 詳しくは、[顧客アカウントの管理](../customers/manage-account.md)を参照してください。

![顧客リスト &#x200B;](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## 顧客情報の更新

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**&#x200B;に移動します。

1. 顧客レコードを検索し、_[!UICONTROL Action]_&#x200B;列の&#x200B;[!UICONTROL **編集**]をクリックします。

1. 左側のパネルで、編集する情報を選択し、必要な変更を加えます。

   >[!NOTE]
   >
   >詳しくは、[顧客アカウントの更新](../customers/update-account.md)を参照してください。

1. 完了したら、**[!UICONTROL Save Customer]**&#x200B;をクリックします。

## Workspaceコントロール

| 制御 | 説明 |
| --- | --- |
| **[!UICONTROL Add New Customer]** | 顧客アカウントを作成します。 |
| **[!UICONTROL Search]** | 現在のフィルターに基づいて顧客の検索を開始します。 |
| **[!UICONTROL Filters]** | [&#x200B; グリッド &#x200B;](../getting-started/admin-grid-controls.md)に表示されるレコードをフィルタリングするために使用される検索パラメーターのセットを定義します。 |
| **[!UICONTROL Default View]** | グリッドのデフォルト列[layout](../getting-started/admin-grid-controls.md)を決定します。 |
| **[!UICONTROL Columns]** | グリッド内の[列](../getting-started/admin-grid-controls.md)とそのアカウントの選択範囲を決定します。 列レイアウトを変更し、_ビュー_&#x200B;として保存できます。 デフォルトでは、グリッドに含まれるのは一部の列のみです。 |
| **[!UICONTROL Export]** | 選択したレコードをCSVまたはExcel XML ファイルとして書き出します。 |

{style="table-layout:auto"}

## 列

| 列 | 説明 |
| --- | --- |
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
| **[!UICONTROL Date of Birth]** | 顧客の生年月日。 <br><br>**_Important:_**&#x200B;現在のセキュリティとプライバシーのベストプラクティスに従って、お客様の生年月日（月、日、年）を他の個人IDと共に保存することに関連する潜在的な法的およびセキュリティ上のリスクを認識してください。 お客様の完全な生年月日の保存を制限し、お客様の生年月日を代替手段として使用することをお勧めします。 |
| **[!UICONTROL Tax / VAT Number]** | 該当する場合、お客様に割り当てられている税番号または[付加価値税](../stores-purchase/vat.md)番号。 <br/><br/>このフィールドはVAT番号と同じではありません。 |
| **[!UICONTROL Gender]** | 顧客の性別。 |
| **[!UICONTROL Action]** | 編集 – 会社アカウントを編集モードで開きます。 |

{style="table-layout:auto"}

### その他の列

これらの列は、グリッドの[列レイアウト &#x200B;](../getting-started/admin-grid-controls.md)を変更することで使用できます。

| 列 | 説明 |
| --- | --- |
| **[!UICONTROL Company]** | 顧客の会社名。 |
| **[!UICONTROL Street Address]** | 顧客の住所。 |
| **[!UICONTROL City]** | 顧客が所在する都市。 |
| **[!UICONTROL Fax]** | 顧客のFAX番号（該当する場合）。 |
| **[!UICONTROL Billing Firstname]** | お客様の請求先住所の名。 |
| **[!UICONTROL Billing Lastname]** | 顧客の請求先住所の姓。 |
| **[!UICONTROL Billing Address]** | 請求情報を送信するアドレス。 |
| **[!UICONTROL Shipping Address]** | 注文が発送される住所。 |
| **[!UICONTROL VAT Number]** | 顧客アドレスに関連付けられている付加価値税番号。 EUで販売された[&#x200B; デジタル商品](../stores-purchase/taxes.md)の場合、VATは顧客の請求先住所に基づきます。 <br/><br/>このフィールドは、税金/VAT番号と同じではありません。 |
| **[!UICONTROL Account Lock]** | アカウントのステータスを示します。 セキュリティ対策として、ログインの試行回数が多すぎると、顧客アカウントが[&#x200B; ロック &#x200B;](../customers/password-options.md)される可能性があります。 値：`Locked` / `Unlocked` |

{style="table-layout:auto"}
