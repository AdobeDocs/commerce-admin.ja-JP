---
title: 顧客リスト
description: 顧客グリッドには、ストアにアカウントを登録したすべての顧客と、管理者によって追加されたすべての顧客が一覧表示されます。
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 顧客リスト

管理者では、[!UICONTROL Customers] グリッドに、ストアにアカウントを登録したすべての顧客と、管理者によって追加されたすべての顧客が一覧表示されます。 標準の [ グリッドコントロール ](../getting-started/admin-grid-controls.md) を使用して、リストをフィルタリングし、列のレイアウトを調整します。 詳しくは、[ 顧客アカウントの管理 ](../customers/manage-account.md) を参照してください。

![ 顧客リスト ](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## 顧客情報の更新

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL All Customers]** に移動します。

1. 顧客レコードを見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;[!UICONTROL **編集**]をクリックします。

1. 左側のパネルで、編集する情報を選択し、必要な変更を行います。

   >[!NOTE]
   >
   >詳しくは、[ 顧客アカウントの更新 ](../customers/update-account.md) を参照してください。

1. 完了したら、「**[!UICONTROL Save Customer]**」をクリックします。

## Workspaceの制御

| 制御 | 説明 |
| --- | --- |
| **[!UICONTROL Add New Customer]** | 顧客アカウントを作成します。 |
| **[!UICONTROL Search]** | 現在のフィルターに基づいて顧客の検索を開始します。 |
| **[!UICONTROL Filters]** | [ グリッド ](../getting-started/admin-grid-controls.md) に表示されるレコードのフィルターに使用する検索パラメーターのセットを定義します。 |
| **[!UICONTROL Default View]** | グリッドの既定の列 [ レイアウト ](../getting-started/admin-grid-controls.md) を決定します。 |
| **[!UICONTROL Columns]** | グリッド内の [ 列 ](../getting-started/admin-grid-controls.md) とそのアカウントの選択を決定します。 列のレイアウトは、変更して _ビュー_ として保存できます。 デフォルトでは、一部の列のみがグリッドに含まれます。 |
| **[!UICONTROL Export]** | 選択したレコードを CSV または Excel XML ファイルとしてエクスポートします。 |

{style="table-layout:auto"}

## 列

| 列 | 説明 |
| --- | --- |
| **[!UICONTROL Select]** | アクションを適用する顧客レコードのチェックボックス選択を管理します。 また、列ヘッダーの選択コントロールを使用して、すべてを選択/選択解除することもできます。 |
| **[!UICONTROL ID]** | 顧客アカウントの作成時に割り当てられる一意の数値 ID。 |
| **[!UICONTROL Name]** | 顧客の姓と名。 |
| **[!UICONTROL Email]** | 顧客の電子メールアドレス。 |
| **[!UICONTROL Group]** | 顧客が割り当てられている顧客グループ。 |
| **[!UICONTROL Phone]** | 顧客の電話番号。 |
| **[!UICONTROL ZIP]** | 顧客の郵便番号。 |
| **[!UICONTROL Country]** | 顧客が所在する国。 |
| **[!UICONTROL State/Province]** | 顧客が所在する都道府県。 |
| **[!UICONTROL Customer Since]** | 顧客アカウントが作成された日時。 |
| **[!UICONTROL Web Site]** | 顧客アカウントが関連付けられているストア階層内の Web サイト。 |
| **[!UICONTROL Confirmed Email]** | 確認メールが必要かどうかを示します。 |
| **[!UICONTROL Account Created In]** | 顧客アカウントが作成されたストア表示を示します。 |
| **[!UICONTROL Date of Birth]** | 顧客の生年月日。 <br><br>**_重要：_**&#x200B;現在のセキュリティおよびプライバシーのベストプラクティスに従い、顧客の完全な生年月日（月、日、年）を他の個人識別子と保存することに関連して、潜在的な法的およびセキュリティリスクがあることを認識しておいてください。 顧客の完全な生年月日の保存を制限し、代わりに顧客の生年月日を使用することをお勧めします。 |
| **[!UICONTROL Tax / VAT Number]** | 該当する場合、顧客に割り当てられた税金番号または [ 付加価値税 ](../stores-purchase/vat.md) 番号。 <br/><br/> このフィールドは VAT 番号とは異なります。 |
| **[!UICONTROL Gender]** | 顧客の性別。 |
| **[!UICONTROL Action]** | 編集 – 会社アカウントを編集モードで開きます。 |

{style="table-layout:auto"}

### 追加の列

これらの列は、グリッドの [ 列のレイアウト ](../getting-started/admin-grid-controls.md) を変更することで使用できます。

| 列 | 説明 |
| --- | --- |
| **[!UICONTROL Company]** | 顧客の会社名。 |
| **[!UICONTROL Street Address]** | 顧客の住所。 |
| **[!UICONTROL City]** | 顧客の所在地の市区町村。 |
| **[!UICONTROL Fax]** | 顧客の FAX 番号（該当する場合）。 |
| **[!UICONTROL Billing Firstname]** | 顧客の請求先住所の名。 |
| **[!UICONTROL Billing Lastname]** | 顧客の請求先住所の姓。 |
| **[!UICONTROL Billing Address]** | 請求情報が送信される住所。 |
| **[!UICONTROL Shipping Address]** | 注文を発送する住所。 |
| **[!UICONTROL VAT Number]** | 顧客の住所に関連付けられている付加価値税番号。 EU で販売されている [ デジタル商品 ](../stores-purchase/taxes.md) の場合、VAT は顧客の請求先住所に基づきます。 <br/><br/> このフィールドは税金/VAT 番号と同じではありません。 |
| **[!UICONTROL Account Lock]** | アカウントのステータスを示します。 セキュリティ対策として、ログインの試行が多すぎると、カスタマーアカウントを [ ロック ](../customers/password-options.md) することができます。 値：`Locked`/`Unlocked` |

{style="table-layout:auto"}
