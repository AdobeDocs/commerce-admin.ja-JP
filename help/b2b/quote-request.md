---
title: 見積依頼
description: 会社アカウントに関連付けられている顧客が見積依頼を送信する方法を説明します。
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: b53d77364f09e587813c50221ebd85ac633f1296
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 見積依頼

で引用符が有効になっている場合 [セールス機能の構成](configure-quotes.md)を選択すると、権限を持つ買い手は、買い物かごからの見積もりを要求することで、価格交渉プロセスを開始できます。 バイヤーがネゴシエーション用の見積を発行する準備ができていない場合は、その見積を草案として保存できます。

>[!NOTE]
>
>見積依頼には、割引コードやギフト カードを含めることはできません。

## 顧客の見積もり依頼エクスペリエンス

1. 顧客は、次を使用して、購入者としてユーザーアカウントにログインします [権限](account-company-roles-permissions.md) 見積を依頼します。

1. 見積もりに含める商品を買い物かごに追加します。

   >[!TIP]
   > 
   >顧客は次を使用して、製品 SKU のリストをより迅速に買い物かごに追加できます [クイック注文](quick-order.md).

1. を選択 **[!UICONTROL Request a Quote]**.

   ![買い物かごからの見積もりのリクエスト](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. が含まれる **[!UICONTROL Add your comment]** ボックスに、顧客が要求を説明する簡単なメモを入力します。

1. エントリ数：a **[!UICONTROL Quote Name]**.

   ![見積のコメントと名前の入力](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. 必要に応じて、サポートするドキュメントまたは画像を見積もりに添付します。

   - を選択 **[!UICONTROL Attach file]**.
   - システムからファイルを選択します。

   デフォルトでは、 [添付ファイル](configure-quotes.md) 次のファイル形式のいずれかで、最大 2 MB にすることができます：DOC、DOCX、XLS、XLSX、PDF、TXT、JPGまたはJPEG、PNG。

1. 見積もりを作成および処理します。

   - 次の項目を選択して、販売者に見積もりを送信します **[!UICONTROL Request a Quote]**.
   - [!BADGE 1.5.0 ベータ版の機能]{type=Informative url="/help/b2b/release-notes.md" tooltip="ベータ版プログラムの参加者のみが使用できます"}**[!UICONTROL Save as Draft]**.

     購買担当が見積を草案として保存すると、見積は次の場所で使用可能になります。 [!UICONTROL My Quotes] 。対象： `Draft` 都道府県。 下書きの見積りは、購入者がレビュー用に送信するまで、販売者には表示されません。
