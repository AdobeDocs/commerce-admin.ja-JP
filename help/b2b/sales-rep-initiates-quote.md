---
title: 購買担当の見積を開始します
description: 販売者が特定の購入者に対して見積もりを作成してネゴシエーションプロセスを開始する方法を説明します。 売り手は、選択した Web サイトの会社アカウントに関連付けられている顧客に対してのみ見積もりを送信できます。
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 8130ccb809a6aec80db63c5a6ea9f47488248805
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# 購買担当に対する見積の開始

で引用符が有効になっている場合 [セールス機能の構成](configure-quotes.md)営業担当者は、管理者から見積もりを作成することで、会社の購買担当とのネゴシエーション・プロセスを開始できます。

- ドラフトの引用符は売り手にのみ表示されます。
- 見積の下書きは、販売担当者が品目、関連する割引、メモを追加して購入者に最初のオファーを作成するまで送信できません。
- 販売者は、Quote または Customer Grid から見積を作成できます。

営業担当が見積を購買担当に送付して、ネゴシエーション・プロセスを開始します。 参照： [見積の交渉](quote-price-negotiation.md).

## 営業担当者の見積もりの作成エクスペリエンス

営業担当は、見積または顧客グリッドから見積を作成できます。

>[!NOTE]
>
>セラーがバイヤーの見積もりを作成するビデオ・デモについては、次を参照してください。 [営業担当者が見積を開始](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html) 。対象： _CommerceのビデオとTutorials_.

### 見積もりグリッドからの見積もりの作成

1. 営業担当者が、管理者としてにログインします。 [営業操作の権限](../systems/permissions.md) 見積を管理します。

1. 管理者で、に移動します。 [!UICONTROL Quotes] 選択によるグリッド **[!UICONTROL Sales]**&#x200B;を選択してから、 **[!UICONTROL Quotes]**.

1. 購買担当の見積を作成します。

   - 引用符グリッドから、を選択します。 **[!UICONTROL Create New Quote]**.

     ![管理者から購入者の見積もりを開始する販売者](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - 日 [!UICONTROL Create New Quote] ページで、見積を作成する顧客（会社の購買担当）を選択します。

     ![新規見積の顧客を選択](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     新しい見積もりが `Draft` ステータス。

     ![販売者によって作成された新しい下書き見積](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - 必要に応じて、見積書名を更新し、有効期限を変更します。

   - 見積もりを下書きとして保存します。

## 購買担当の見積を準備します

下書き見積もりを作成した後、商品品目を追加し、割引を適用し、見積もりにコメントや関連ファイルを追加して購入者と連絡を取ります。 次に、見積もりをレビュー用に購入者に送信するか、下書きとして保存します。

1. 次の項目を選択して、見積もりに項目を追加 **[!UICONTROL Add Product By SKU]**. SKU 番号と数量を入力し、 **[!UICONTROL Add Product]**.

   ![販売者が品目を購買担当の見積書作成に追加](./assets/quote-draft-add-items.png){width="675" zoomable="yes"}

1. 必要に応じて、品目の値引きを製品に適用します。

   - から [!UICONTROL Select] アクションメニュー、選択 **[!UICONTROL Discount Item]**.

   - 日 [!UICONTROL Discount Line item] フォームで、 **[!UICONTROL Discount Type]**.

     ![見積に品目割引を適用します](./assets/quote-discount-line-item.png){width="675" zoomable="yes"}

   - が含まれる [!UICONTROL Discount] フィールドに、割引タイプの値を入力します。 たとえば、パーセンテージ割引を選択した場合、10 と入力して、明細品目に 10% 割引を適用します。

   - [!BADGE 1.5.0 ベータ版機能]{type=Informative url="/help/b2b/release-notes.md" tooltip="ベータ版プログラムの参加者のみが使用できます"}

     変更を確認すると、製品グリッドの行項目属性が更新され、適用された割引額が表示されます。 割引がロックされている場合は、ロックアイコンが表示されます。

1. 必要に応じて、見積レベルの値引きを適用します。

   - が含まれる [!UICONTROL Quote Totals - Negotiated Price] セクションで、割引タイプを選択し、適用する値を入力します。

     ![販売者が見積もりレベルの割引を追加](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   商品グリッドが更新され、割引が表示されます。

1. 購買担当の追加情報を追加します。

   日 **[!UICONTROL Negotiation - Comments]** タブで、メモを追加し、購入者に必要なサポートファイルを添付します。

   ![売り手が買い手の情報を追加します](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   デフォルトでは、 [添付ファイル](configure-quotes.md) 次のファイル形式のいずれかで、最大 2 MB にすることができます：DOC、DOCX、XLS、XLSX、PDF、TXT、JPGまたはJPEG、PNG。

1. 見積もりを処理します。

   見積を下書きとして保存するか、購入者に送信します。

   - 見積を草案として保存すると、ステータスは次のように更新されます。 `Draft` 確認メッセージが表示されます。

   - 見積を購買担当に送付すると、ステータスが次のように変更されます。 `Submitted`. 購入者は、見積を確認するためのメール通知を受け取ります。 見積は、バイヤーが以降の交渉のために戻すまでロックされます。 販売者は、Quote グリッドまたは Customer グリッドから見積を表示できます。

## 顧客グリッドからの見積の表示および作成

1. 管理者で、に移動します。 [!UICONTROL Customer] 選択によるグリッド **[!UICONTROL Customers]**&#x200B;を選択してから、 **[!UICONTROL All Customers]**.

1. 会社バイヤーの顧客 ID を選択します。

   ![購買担当に送信された見積草案の確認](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. を選択 **[!UICONTROL Edit]** 顧客情報を表示します。

1. 次のように選択して、顧客の見積もりを作成します。 **[!UICONTROL Create Quote]** 見積もり草案を更新して顧客に送信するプロセスに従います。

1. 選択して既存の見積を表示する **[!UICONTROL Quotes]**.

   ![購買担当に送信された見積草案の確認](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. 選択して見積を開く **[!UICONTROL View]**.

見積ネゴシエーション・プロセスの管理の詳細は、次を参照してください [見積の交渉](quote-price-negotiation.md)
