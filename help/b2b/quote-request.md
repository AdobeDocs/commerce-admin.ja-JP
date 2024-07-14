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

[ 販売機能の構成 ](configure-quotes.md) で見積が有効になっている場合、会社から承認されたバイヤーは、買い物かごから見積を要求することで価格交渉処理を開始できます。 バイヤーがネゴシエーション用の見積を発行する準備ができていない場合は、その見積を草案として保存できます。

>[!NOTE]
>
>見積依頼には、割引コードやギフト カードを含めることはできません。

## 顧客の見積もり依頼エクスペリエンス

1. お客様は、見積もりを要求する [ 権限 ](account-company-roles-permissions.md) を持つ購入者としてユーザーアカウントにログインします。

1. 見積もりに含める商品を買い物かごに追加します。

   >[!TIP]
   > 
   >顧客は [ クイックオーダー ](quick-order.md) を使用して、製品 SKU のリストをより迅速に買い物かごに追加できます。

1. **[!UICONTROL Request a Quote]** を選択します。

   ![ 買い物かごからの見積りの依頼 ](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. **[!UICONTROL Add your comment]** のボックスに、お客様がリクエストを説明する簡単なメモを入力します。

1. **[!UICONTROL Quote Name]** を入力します。

   ![ 見積書のコメントと名前の入力 ](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. 必要に応じて、サポートするドキュメントまたは画像を見積もりに添付します。

   - **[!UICONTROL Attach file]** を選択します。
   - システムからファイルを選択します。

   デフォルトでは、[ 添付ファイル ](configure-quotes.md) は最大 2 MB で、次のファイル形式のいずれかで使用できます：DOC、DOCX、XLS、XLSX、PDF、TXT、JPGまたはJPEG、PNG。

1. 見積もりを作成および処理します。

   - **[!UICONTROL Request a Quote]** を選択して Quote を Seller に送信します。
   - [!BADGE 1.5.0 ベータ版機能 ]{type=Informative url="/help/b2b/release-notes.md" tooltip="Beta プログラム参加者のみ使用可能"}**[!UICONTROL Save as Draft]**。

     購買担当が見積を草案として保存すると、見積は [!UICONTROL My Quotes] の状態で使用可能 `Draft` なります。 下書きの見積りは、購入者がレビュー用に送信するまで、販売者には表示されません。
